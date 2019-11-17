# homeTask
### task's goal:
For a given contour and a point (x,y), return:<br>
True   if the point is inside the contour <br>
False  otherwise.<br>
<br>
### pseudo code:
<img src="psuedo.PNG" height=350 weight=250><br>
     
     הסבר לפסאודו קוד:
     1. בדיקת תקינות קלט - שגודל התמונה שהוכנס הוא אכן גודל התמונה שהתקבלה, ושהנקודה נמצאת בתוך גבולות התמונה.
     בנוסף בדקתי שהתמונה בגודל מינימלי של 3 על 3 (ככה יכולה בטוח להיות בה צורה סגורה) <br>
     2. בדיקה אם קבלנו נקודה שהפיקסל שלה בצבע שחור - כלומר היא על הצורה ולכן נחזיר שקר <br>
     3.  בדיקה לאיזה כיוון הכי קצר למתוח את הקרן (כדי לחסוך במספר האיטרציות ולקצר בזמן ריצה) מהנקודה לשמאל או מהנקודה לימין.<br>
     * הערה: ניתן לבדוק עדיפות גם כלפי מעלה ומטה ולממש שיטה שבודקת קודקודים וצלעות בכיוון זה<br>
     איתחול המשתנים - מונה = 0, המשתנה הבוליאני = שקר<br>
     4. רצים לאורך הקרן ובודקים האם נתקלנו בצורה, אם כן בודקים מקרים שאותם לא נרצה לספור (קוקוד עליון או תחתון, או חלק מצלע אופקית כלפי מטה או חלק מצלע אופקית כלפי מעלה) מצורפת למטה תמונה להמחשה . <br>
     אם הכל תקין נעלה את המונה בחצי (מעלים בחצי בגלל שפעם אחת השינוי הוא מלבן לשחור ובפעם השניה זה משחור לבן, ככה שבסוף המעבר על הצורה הקאונטר יעלה ב1). <br>
     5. בודקים האם המונה זוגי- אם כן אנחנו מחוץ לצורה ונחזיר שקר, אחרת נחזיר אמת.
     
  ### :יעילות
  כפי שציינתי - ניתן לבחור את המסלול הקצר ביותר מהנקודה לאחד הגבולות של התמונה. ולכן במקרה הכי גרוע נרוץ חצי מרוחב התמונה או חצי מאורך התמונה (הנמוך מבינהם) כלומר:<br>
  o(h/2) = o(h) או o(w/2) = o(W) <br>
  h - אורך התמונה w- רוחב התמונה <br>
     

    
#### סוגי קודקודים שבדקתי:<br>
<img src="vertex_types.PNG" height=350 weight=250><br>
     
