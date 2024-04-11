:show-content:
:show-toc:

====================
Manage user accounts
====================

In Odoo's *Lunch* application, users pay for products directly from their *Lunch* app account. In
order for funds to appear in their account, a *Lunch* app manager must transfer funds into each
users account.

The *Lunch* application does **not** directly interface in any way with software or products linked
to any monetary accounts or billing. Money **cannot** be transferred from user's bank accounts, nor
are users credit cards able to be charged.

Odoo's *Lunch* application **only** allows for manual entries of cash exchanges that are handled by
the *Lunch* app manager. It is up to each individual company to create the method with which lunch
accounts are replenished.

.. example::
   Some examples of how money can be organized and transferred within a company:

   - Cash is handed to the *Lunch* app manager, who then updates the users account.
   - Money is automatically deducted from users paychecks, then the *Lunch* app manager updates the
     account when paychecks are issued. This requires :ref:`adding a salary attachment
     <payroll/worked-days-inputs>` for the user's payslip in the *Payroll* app.
   - Companies can sell "lunch tickets" at a set price (for example, once ticket costs $5.00). Users
     can purchase tickets from a *Lunch* app manager, who then updates the users account.

.. important::
   In order to add funds and manage user accounts, the user must have :guilabel:`Administrator`
   rights set for the :guilabel:`Lunch` application. This is verified by navigating to
   :menuselection:`Settings app --> → Manage Users`. Then click on a user to view the various
   settings. For more information on access rights, refer to the :doc:`Access rights
   </applications/general/users/access_rights/>` documentation.

Add funds
=========

To add funds to user accounts, each cash move must be individually logged. To record a cash deposit,
navigate to :menuselection:`Lunch app --> Manager --> Cash Moves`.

All cash moves are presented in a list view, displaying the :guilabel:`Date`, :guilabel:`User`,
:guilabel:`Description`, and :guilabel:`Amount` for each record.

