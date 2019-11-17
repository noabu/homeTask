# homeTask
### task's goal:
For a given contour and a point (x,y), return:<br>
True   if the point is inside the contour <br>
False  otherwise.<br>
<br>
### pseudo code:
1. input validation<br>
2. if point on contour: return FALSE<br>
3. if min (p_x, image_with-p_x) == p_x: go from point to left image border.<br>
   else: go from point to right image border. <br>
   counter = 0 <br>
   inside = FALSE <br>
4. for i from point to border:<br>
    vertex_flag = 0 <br>
    if cross contour: <br>
      if current pixel < image_width:<br>
         vertex_flag <- check if the currnt pixel is vertex or part of edge <br>
      else: (current black pixel on the rightmost pixel)<br>
         counter += 0.5 <br>
      if current pixel not vertex or part of edge: <br>
         counter +=0.5<br>
 5. if counter odd: inside = TRUE<br>
    else: inside = FALSE <br>
     
     הסבר לפסאודו קוד:
     1. בדיקת תקינות קלט - שגודל התמונה שהוכנס הוא אכן גודל התמונה שהתקבלה, ושהנקודה נמצאת בתוך גבולות התמונה.
     בנוסף בדקתי שהתמונה בגודל מינימלי של 3 על 3 (ככה יכולה בטוח להיות בה צורה סגורה) <br>
     kmk
     
