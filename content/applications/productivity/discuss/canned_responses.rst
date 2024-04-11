================
Canned responses
================

*Canned responses* are customizable inputs where a shortcut stands in for a longer response. A user
enters a keyword shortcut, which is then automatically replaced by the expanded substitution
response.

Canned responses consist of two main components: the *shortcut* and the *substitution*. The shortcut
is the keyword or key phrase that is to be replaced. The substitution is the longer message that
replaces the shortcut.

Canned responses are available :ref:`to use <discuss/use-cases>` in *Live Chat* conversations, the
*Discuss* app, and in the *Chatter* composer.

Creating canned responses
=========================

Canned responses are managed through the *Discuss* application. To create a new canned response, or
to manage the list of existing responses, navigate to :menuselection:`Discuss app --> Configuration
--> Canned Responses`.

To create a new canned response, click :guilabel:`New` at the top-left of the list.

Canned responses consist of two main components, a shortcut the user enters, and the substitution
that replaces the shortcut.

Type a shortcut command in the :guilabel:`Shortcut` field. Next, click to the
:guilabel:`substitution` field and type the message that will replace the shortcut.

.. tip::
   Try to connect the shortcut to the topic of the substitution. Not only does this make it easier
   to use the responses, it prevents the list of responses from becoming disorganized and
   overwhelming.

In the :guilabel:`Description` field, add any information the provides context for this response,
such as guidelines for when it should or should not be used.

.. important::
   If the :guilabel:`Authorized Group` field is left blank, the response can **only** be used by the
   user that created it.

  Canned responses that are created by the database automatically are credited as created by
  *OdooBot*. Until they are assigned to an *authorized group*, they cannot be used by **any** users.

.. _discuss/sharing-responses:

Sharing responses
=================

Canned responses, by default, are made available **only** to the user that creates them. To make a
canned response available for others to use,

.. note::
   Users with Administrator access rights are able to view and edit canned responses created by
   other users through the *Discuss* app. However, they are **not** able to use them unless added
   as an authorized group.

Filter for shared responses
---------------------------

Canned responses


.. _discuss/use-cases:

Use cases
=========

.. tip::
   Typing `:` in the chatter window on its own generates a drop-down list of available canned
   responses. A response can be selected from the list, in addition to the use of shortcuts.
