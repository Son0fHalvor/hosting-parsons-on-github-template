---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Multiple Parson's Problems on One Page
---
# Parsons Practice
### Instructions
rearrange the code to make Volume = 3120

<div id="problem1-sortableTrash" class="sortable-code"></div> 
<div id="problem1-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="problem1-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="problem1-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "let height = $$toggle::20::10$$\n" +
    "let width = $$toggle::15::12$$\n" +
    "let length = $$toggle::25::13$$\n" +
    "let volume = height*width*length";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "problem1-sortable",
    "max_wrong_lines": 1,
    "grader": ParsonsWidget._graders.LanguageTranslationGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "problem1-sortableTrash",
    "executable_code": "height = $$toggle::20::10$$\nwidth = $$toggle::15::12$$\nlength = $$toggle::25::13$$\nvolume = height*width*length",
    "programmingLang": "java",
    "vartests": [
        {
            "message": "The volume = 3120",
            "initcode": "",
            "code": "",
            "variables": {
                "volume": 3120
            }
        }
    ]
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#problem1-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#problem1-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
# Parsons Practice
### Instructions
rearrange the code so that myArray is squared and then display the original array and the squared array to the console.
<div id="problem2-sortableTrash" class="sortable-code"></div> 
<div id="problem2-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="problem2-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="problem2-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "let myArray = [1, 2, 3, 4, 5];\n" +
    "let newArray = [];\n" +
    "for (let i = 0; i &lt; myArray.length; i++) {\n" +
    "    let squaredValue = myArray[i] ** 2;\n" +
    "    newArray.push(squaredValue);\n" +
    "}\n" +
    "console.log(&quot;Original Array:&quot;, myArray);\n" +
    "console.log(&quot;Squared Values:&quot;, newArray);\n" +
    "myArray.push(squaredValue); #distractor\n" +
    "for (let i = 0; i &lt; newArray.length; i++) { #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "problem2-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "trashId": "problem2-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#problem2-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#problem2-feedbackLink").click(function(event){ 
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
