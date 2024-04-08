=============
Upgrade utils
=============

`Upgrade utils <https://github.com/odoo/upgrade-util/>`_ is a library that contains helper functions
to facilitate the writing of upgrade scripts. This library, used by Odoo for the upgrade scripts of
standard modules, provides reliability and helps speed up the upgrade process:

- The helper functions help make sure the data is consistent in the database.
- It takes care of indirect references of the updated records.
- Allows calling functions and avoid writing code, saving time and reducing development risks.
- Helpers allow to focus on what is important for the upgrade and not think of details.

Installation
============

Clone the `Upgrade utils repository <https://github.com/odoo/upgrade-util/>`_ locally and start
``odoo`` with the ``src`` directory prepended to the ``--upgrade-path`` option.

.. code-block:: console

   $ ./odoo-bin --upgrade-path=/path/to/upgrade-util/src,/path/to/other/upgrade/script/directory [...]

On platforms where you do not manage Odoo yourself, you can install this library via `pip`:

.. code-block:: console

   $ python3 -m pip install git+https://github.com/odoo/upgrade-util@master

On `Odoo.sh <https://www.odoo.sh/>`_ it is recommended to add it to the :file:`requirements.txt` of
the custom repository. For this, add the following line inside the file::

   odoo_upgrade @ git+https://github.com/odoo/upgrade-util@master

Using Upgrade utils
===================

Once installed, the following packages are available for the upgrade scripts:

- :mod:`odoo.upgrade.util`: the helper itself.
- :mod:`odoo.upgrade.testing`: base TestCase classes.

To use it in upgrade scripts, simply import it:

.. code-block:: python

   from odoo.upgrade import util


   def migrate(cr, version):
      # Rest of the script

Now, the helper functions are available to be called through ``util``.

Util functions
==============

Upgrade utils provides many useful functions to ease the upgrade process. Here, we describe some
of the most useful ones. Refer to the `util folder
<https://github.com/odoo/upgrade-util/tree/master/src/util>`_ for the comprehensive declaration of
helper functions.

.. note::

   The :attr:`cr` parameter in util functions always refers to the database cursor. Pass the one
   received as a parameter in :meth:`migrate`. Not all functions need this parameter.

.. currentmodule:: odoo.upgrade.util

Modules
-------

.. automodule:: odoo.upgrade.util.modules
.. autofunction:: modules_installed
.. autofunction:: module_installed
.. autofunction:: uninstall_module
.. autofunction:: uninstall_theme
.. autofunction:: remove_module
.. autofunction:: remove_theme
.. autofunction:: rename_module
.. autofunction:: merge_module
.. autofunction:: force_install_module
.. autofunction:: force_upgrade_of_fresh_module
.. autofunction:: move_model


Models
------

.. automodule:: odoo.upgrade.util.models
.. autofunction:: remove_model
.. autofunction:: rename_model
.. autofunction:: merge_model


Fields
------

.. automodule:: odoo.upgrade.util.fields
.. autofunction:: remove_field
.. autofunction:: rename_field
.. autofunction:: move_field_to_module
.. autofunction:: change_field_selection_values


Records
-------

.. automodule:: odoo.upgrade.util.records
.. autofunction:: ref
.. autofunction:: remove_record
.. autofunction:: rename_xmlid
.. autofunction:: ensure_xmlid_match_record
.. autofunction:: update_record_from_xml
.. autofunction:: force_noupdate
.. autofunction:: replace_record_references_batch
.. autofunction:: replace_in_all_jsonb_values


ORM
---

.. automodule:: odoo.upgrade.util.orm
.. autofunction:: env
.. autofunction:: recompute_fields
.. autoclass:: iter_browse
   :members: create

.. automodule:: odoo.upgrade.util.domains
.. autofunction:: adapt_domains


SQL
---

.. automodule:: odoo.upgrade.util.pg
.. autofunction:: explode_execute
.. autofunction:: format_query
.. autofunction:: get_columns
.. autoclass:: ColumnList
   :members: using, iter_unquoted
.. autoclass:: PGRegexp


Misc
----

.. automodule:: odoo.upgrade.util.misc
.. autofunction:: expand_braces
.. autofunction:: import_script
.. autofunction:: version_gte
.. autofunction:: version_between
.. autofunction:: chunks
