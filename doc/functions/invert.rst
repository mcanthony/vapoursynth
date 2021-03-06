Invert
======

.. function:: Invert(clip clip[, int[] planes=[0, 1, 2]])
   :module: std

   Inverts the pixel values. Specifically, it subtracts the value of the
   input pixel from the format's maximum allowed value.

   *clip*
      Clip to process. It must have integer sample type, and bit depth
      between 8 and 16. If there are any frames with float samples or
      bit depth greater than 16, an error will be returned.

   *planes*
      Specifies which planes will be processed. Any unprocessed planes
      will be simply copied.
