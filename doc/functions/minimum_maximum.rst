Minimum/Maximum
===============

.. function:: Minimum(clip clip[, int[] planes=[0, 1, 2], int threshold=65535, int[] coordinates=[1, 1, 1, 1, 1, 1, 1, 1]])
   :module: std

   Replaces each pixel with the smallest value in its 3x3 neighbourhood.
   This operation is also known as erosion.

   *clip*
      Clip to process. It must have integer sample type, and bit depth
      between 8 and 16. If there are any frames with float samples or
      bit depth greater than 16, an error will be returned.

   *planes*
      Specifies which planes will be processed. Any unprocessed planes
      will be simply copied.

   *threshold*
      Allows to limit how much pixels are changed. Output pixels will not
      become less than ``input - threshold``. With the default value of
      65535 there is no limit.

   *coordinates*
      Specifies which pixels from the 3x3 neighbourhood are considered.
      If an element of this array is 0, the corresponding pixel is not
      considered when finding the minimum value. This must contain exactly
      8 numbers.

      Here is how each number corresponds to a pixel in the 3x3
      neighbourhood::

         [    top left,    top center,    top right,
           middle left,                middle right,
           bottom left, bottom center, bottom right ]


.. function:: Maximum(clip clip[, int[] planes=[0, 1, 2], int threshold=65535, int[] coordinates=[1, 1, 1, 1, 1, 1, 1, 1]])
   :module: std

   Replaces each pixel with the largest value in its 3x3 neighbourhood.
   This operation is also known as dilation.

   *clip*
      Clip to process. It must have integer sample type, and bit depth
      between 8 and 16. If there are any frames with float samples or
      bit depth greater than 16, an error will be returned.

   *planes*
      Specifies which planes will be processed. Any unprocessed planes
      will be simply copied.

   *threshold*
      Allows to limit how much pixels are changed. Output pixels will not
      become greater than ``input + threshold``. With the default value
      of 65535 there is no limit.

   *coordinates*
      Specifies which pixels from the 3x3 neighbourhood are considered.
      If an element of this array is 0, the corresponding pixel is not
      considered when finding the maximum value. This must contain exactly
      8 numbers.

      Here is how each number corresponds to a pixel in the 3x3
      neighbourhood::

         [    top left,    top center,    top right,
           middle left,                middle right,
           bottom left, bottom center, bottom right ]
