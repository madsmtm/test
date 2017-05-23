======
Models
======

`fbchat` uses these models as both input parameters and return values.

Index
-----

- `<fbchat.models.User(data)>`_


fbchat.models.User(data)
========================



.. function:: food(x)
              food(y, z)
              food(x, y, z)
   :module: some.module.name

   Return a line of text input from the user.

.. function:: foo(x)
              foo(y, z)
   :module: no

   Return a line of text input from the user.


.. py:function:: spam(eggs)
                ham(eggs)

   Spam or ham the foo.


The function :py:func:`spam` does a similar thing.

wda

Lorem ipsum [#]_ dolor sit |caution| (|name|) amet ... [#]_

.. |name| replace:: replacement *text*

.. |caution| image:: warning.png
             :alt: Warning!

.. This is a comment.

..
   This whole indented block
   is a comment.

   Still in the comment.

.. rubric:: Footnotes

.. [#] Text of the first footnote.
.. [#] Text of the second footnote.


This is a normal text paragraph. The next paragraph is a code sample
::

   It is not processed in any way, except
   that the indentation is removed.

   It can span multiple lines.

This is a normal text paragraph again.

.. code-block:: python

    test = 2
    test2 = 3
    class A(object):
        def test(self):
            return 0


View relative_

.. _relative link: otherdoc.rst


View relative2_

.. _relative2 link: doc/otherdoc.rst






======
Models
======

`fbchat` uses these models as both input parameters and return values.

Index
=====

- `models.User(data)`_
- `models.ThreadType(Enum)`_
- `models.TypingStatus(Enum)`_
- `models.EmojiSize(Enum)`_
- `models.ThreadColor(Enum)`_
- `models.MessageReaction(Enum)`_

models.User(data)
=================


models.ThreadType(Enum)
=======================

**Values:**

- `USER`
- `GROUP`

Used to specify what type of Facebook thread is being used

Example Usage
-------------

.. code-block:: python

    client.sendMessage('Hi there USER', thread_id=user_id, thread_type=ThreadType.USER)
    client.sendMessage('Hi there GROUP', thread_id=group_id, thread_type=ThreadType.GROUP)


models.TypingStatus(Enum)
=========================

**Values:**

- `STOPPED`
- `TYPING`

Used to specify whether the user is typing or has stopped typing

Example Usage
-------------

.. code-block:: python

    client.setTypingStatus(TypingStatus.TYPING, thread_id=user_id, thread_type=ThreadType.USER)


models.EmojiSize(Enum)
======================

**Values:**

- `LARGE`
- `MEDIUM`
- `SMALL`

Used to specify the size of a sent emoji

Example Usage
-------------

.. code-block:: python

    client.setEmoji('👍', size=EmojiSize.LARGE, thread_id=user_id, thread_type=ThreadType.USER)


models.ThreadColor(Enum)
======================

**Values:**

- `MESSENGER_BLUE`
- `VIKING`
- `GOLDEN_POPPY`
- `RADICAL_RED`
- `SHOCKING`
- `PICTON_BLUE`
- `FREE_SPEECH_GREEN`
- `PUMPKIN`
- `LIGHT_CORAL`
- `MEDIUM_SLATE_BLUE`
- `DEEP_SKY_BLUE`
- `FERN`
- `CAMEO`
- `BRILLIANT_ROSE`
- `BILOBA_FLOWER`

Used to specify a thread colors

Example Usage
-------------

.. code-block:: python

    client.changeThreadColor(ThreadColor.BILOBA_FLOWER, thread_id=group_id)


models.MessageReaction(Enum)
======================

**Values:**

- `LOVE`
- `SMILE`
- `WOW`
- `SAD`
- `ANGRY`
- `YES`
- `NO`

Used to specify a message reaction

Example Usage
-------------

.. code-block:: python

    message_id = client.sendMessage('Wow', thread_id=user_id, thread_type=ThreadType.USER)
    client.reactToMessage(message_id, MessageReaction.WOW)

