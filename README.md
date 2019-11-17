# homeTask
### task's goal:
For a given contour and a point (x,y), return:<br>
True   if the point is inside the contour <br>
False  otherwise.<br>
</p>
### pseudo code:

1. input validation<br>
2. if point on contour: return FALSE<br>
3. if min (p_x, image_with-p_x) == p_x: go from point to left image border.<br>
   else: go from point to right image border. <br>
   counter = 0 <br>
   inside = FALSE <br>
4. for i from point to border:<br>
   <pre> vertex_flag = 0</pre> <br>
   <pre> if cross contour:</pre> <br>
    <pre> <pre> if current pixel < image_width:</pre></pre>  <br>
      <pre> <pre> <pre> vertex_flag <- check if the currnt pixel is vertex or part of edge</pre> </pre> </pre> <br>
    <pre> <pre> else: (current black pixel on the rightmost pixel)</pre> </pre> <br>
     <pre> <pre> <pre>  counter += 0.5</pre> </pre> </pre> <br>
    <pre> <pre> if current pixel not vertex or part of edge:</pre> </pre> <br>
     <pre> <pre> <pre>  counter +=0.5</pre> </pre> </pre> <br>
 5. if counter odd: inside = TRUE<br>
    else: inside = FALSE <br>
     
