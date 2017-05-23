======
Models
======

``fbchat`` uses these models as both input parameters and return values.

Overview
========

- `models.User(data)`_
- `models.ThreadType(Enum)`_
- `models.TypingStatus(Enum)`_
- `models.EmojiSize(Enum)`_
- `models.ThreadColor(Enum)`_
- `models.MessageReaction(Enum)`_

models.User(data)
-----------------


models.ThreadType(Enum)
-----------------------

**Values:**

- ``USER``
- ``GROUP``

Used to specify what type of Facebook thread is being used

**Example Usage**

.. code-block:: python

    client.sendMessage('Hi there USER', thread_id=user_id, thread_type=ThreadType.USER)
    client.sendMessage('Hi there GROUP', thread_id=group_id, thread_type=ThreadType.GROUP)


models.TypingStatus(Enum)
-------------------------

**Values:**

- ``STOPPED``
- ``TYPING``

Used to specify whether the user is typing or has stopped typing

**Example Usage**

.. code-block:: python

    client.setTypingStatus(TypingStatus.TYPING, thread_id=user_id, thread_type=ThreadType.USER)


models.EmojiSize(Enum)
----------------------

**Values:**

- ``LARGE``
- ``MEDIUM``
- ``SMALL``

Used to specify the size of a sent emoji

**Example Usage**

.. code-block:: python

    client.setEmoji('👍', size=EmojiSize.LARGE, thread_id=user_id, thread_type=ThreadType.USER)


models.ThreadColor(Enum)
------------------------

**Values:**

- ``MESSENGER_BLUE``
- ``VIKING``
- ``GOLDEN_POPPY``
- ``RADICAL_RED``
- ``SHOCKING``
- ``PICTON_BLUE``
- ``FREE_SPEECH_GREEN``
- ``PUMPKIN``
- ``LIGHT_CORAL``
- ``MEDIUM_SLATE_BLUE``
- ``DEEP_SKY_BLUE``
- ``FERN``
- ``CAMEO``
- ``BRILLIANT_ROSE``
- ``BILOBA_FLOWER``

Used to specify a thread colors

**Example Usage**

.. code-block:: python

    client.changeThreadColor(ThreadColor.BILOBA_FLOWER, thread_id=group_id)


models.MessageReaction(Enum)
----------------------------

**Values:**

- ``LOVE``
- ``SMILE``
- ``WOW``
- ``SAD``
- ``ANGRY``
- ``YES``
- ``NO``

Used to specify a message reaction

**Example Usage**

.. code-block:: python

    message_id = client.sendMessage('Wow', thread_id=user_id, thread_type=ThreadType.USER)
    client.reactToMessage(message_id, MessageReaction.WOW)


See :download:`this example script <../example.py>`.
