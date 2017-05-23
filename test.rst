Test: `<docs/CONTRIBUTING.md>`__

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
