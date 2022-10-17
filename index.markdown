---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Multiple Parson's Problems on One Page
---
# Parsons Practice

## Parsons 1 (Line Based Grader)
Re-arrange the blocks below so they print out "Hello World!"

<div id="travelbag-sortableTrash" class="sortable-code"></div> 
<div id="travelbag-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="travelbag-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="travelbag-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "travelbag = []\n" +
    "while True:\n" +
    "   menyval = input(&quot;1. Kolla i resväskan\n&quot;\n" +
    "                   &quot;2. Lägg sak i resväskan\n&quot;\n" +
    "                   &quot;3. Ta bort sak i resväskan\n&quot;\n" +
    "                   &quot;4. Avsluta program&quot;)\n" +
    "   if menyval == &quot;1&quot;:\n" +
    "       pass\n" +
    "   elif menyval == &quot;2&quot;:\n" +
    "       pass\n" +
    "   elif menyval == &quot;3&quot;:\n" +
    "       pass\n" +
    "   elif menyval == &quot;4&quot;:\n" +
    "       break";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "travelbag-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#travelbag-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#travelbag-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>


      
      
### Implementation Notes

When you host multiple Parson's problems on a single markdown page, you need to add a unique prefix. You can easily do this in the Codio generator by typing a unique prefix into the "Prefix" textbox and pressing Enter/Return. Then you can simply copy-paste like normal.

If want each problem to be it's own page, you can use relative path links at the bottom of each of your markdown pages as seen below. If you want students to be able to return to previous problems in this format, consider adding previous links or link to a table of contents like page.

### Example Next Link
[Next](./parsons/example1.html)

