---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Multiple Parson's Problems on One Page
---
# Parsons - Programmering 2

## Blandade klasser


<div id="sortableTrash" class="sortable-code"></div> 
<div id="sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="feedbackLink" value="Get Feedback" type="button" /> 
    <input id="newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "class Animal:\n" +
    "    def __init__(self, length, weight, age, gender, species):\n" +
    "        self.length = length\n" +
    "        self.weight = weight\n" +
    "        self.age = age\n" +
    "        self.gender = gender\n" +
    "        self.species = species\n" +
    "    def age_up(self):\n" +
    "        self.age += 1\n" +
    "class Fish(Animal):\n" +
    "    def __init__(self, length, weight, age, gender, fin_count, watertype):\n" +
    "        super(Fish, self).__init__(length, weight, age, gender, &quot;Fish&quot;)\n" +
    "        self.fin_count = fin_count\n" +
    "        self.watertype = watertype\n" +
    "class Monkey(Animal):\n" +
    "    def __init__(self, length, weight, age, gender, tail_length):\n" +
    "        super(Monkey, self).__init__(length, weight, age, gender, &quot;Monkey&quot;)\n" +
    "        self.tail_length = tail_length\n" +
    "class Elephant(Animal):\n" +
    "    def __init__(self, length, weight, age, gender, trunk_length):\n" +
    "        super(Elephant, self).__init__(length, weight, age, gender, &quot;Elephant&quot;)\n" +
    "        self.trunk_length = trunk_length\n" +
    "class Pokemon:\n" +
    "    def __init__(self, name, hp, level=1):\n" +
    "        self.name = name\n" +
    "        self.hp = hp\n" +
    "        self.level = level\n" +
    "        self.happiness = -2\n" +
    "    def __str__(self):\n" +
    "        return f&quot;Name: {self.name} \nHP: {self.hp} \nLevel: {self.level}&quot;\n" +
    "    def levelup(self):\n" +
    "        self.level += 1\n" +
    "        self.hp = round(self.hp * 1.05)\n" +
    "        self.happiness -= 1\n" +
    "        print(f&quot;{self.name} has leveled up to level {self.level}.&quot;)\n" +
    "class Elev:\n" +
    "    def __init__(self, name, grade, personnr):\n" +
    "        self.name = name\n" +
    "        self.grade = grade\n" +
    "        self.personnr = personnr\n" +
    "    def raise_grade(self):\n" +
    "        self.grade += 1\n" +
    "        print(f&quot;Grade raised to {self.grade}&quot;)";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "sortable",
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
  $("#newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#feedbackLink").click(function(event){ 
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
