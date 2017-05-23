======
Models
======

``fbchat`` uses these models as both input parameters and return values.

Overview
========

- `models.User <#user>`_
- `models.ThreadType <#thread-type>`_
- `models.TypingStatus <#typing-status>`_
- `models.EmojiSize <#emoji-size>`_
- `models.ThreadColor <#thread-color>`_
- `models.MessageReaction <#message-reaction>`_

.. _user:
models.User(data)
-----------------

[MISSING]

.. _thread-type:
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

    
.. _typing-status:
models.TypingStatus(Enum)
-------------------------

**Values:**

- ``STOPPED``
- ``TYPING``

Used to specify whether the user is typing or has stopped typing

**Example Usage**

.. code-block:: python

    client.setTypingStatus(TypingStatus.TYPING, thread_id=user_id, thread_type=ThreadType.USER)

    
.. _emoji-size:
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


.. _thread-color:
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

.. _message-reaction:
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

