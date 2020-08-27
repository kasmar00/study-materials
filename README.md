# Study Materials
Simple webpage for storing links to materials provided by teachers.

Preview: https://kasmar00.github.io/study-materials/

Each material should be encased inside an object (preferably div) with "subject" class and provided with a link (`<a></a>`) inside.

Each material can have one (or none) of currently three classes each correspoding to one form of teaching:
- Lecture: for materials corresponding to lectures (polish: Wykład)
- Classes: for materials for auditory/seminar classes (polish: Ćwiczenia)
- Lab: for materials on laboratory/project claseses (polish: Laboratoria)

Additionaly to form related classes, each material should have one (and only one) type related class:
- Drive: adds Google Drive icon, for materials kept on cloud drives
- Github: adds Github icon, for materials (ex. source code) kept on git and other repositories
- Moodle: adds Moodle icon (an img), for materials provided by teachers on moodle and other cms systems
- Latex: adds an icon symbolising mathematical writing (X with subscirpt 1), for latex source code on online environments (ex. Overleaf)
- Video: adds a camera icon, for video conferences (Zoom, Teams, Big Blue Button) or video materials (Youtube, Twitch)
- Link: adds a globe icon, general class for all links not covered by above classes (ex. teachers website)

The above mentioned type related classes add an icon (from Font Awesome, unless otherwise stated) and a polish text corresponding to material type. The text is overturned by form related classes wich add a text consisiting of form name (in polish)

Some of the type classes will stick to subject name banner on low width screens, currently those are: moodle, drive, github, but only if they don't have a form class (lecture, lab, classes).

The classes are styled in css, so feel free to add extra classes for other forms and types. Each form class consists of background-color and order properties and a correspoding a::after element for content. Each type class has a correspoding a::before element for icon and an a::after element for text content.

Currently all subjects and materials must be added in html, but in future they may be imported from a csv file using JS.

Exapmle code:
```html
<div class="wrapper">
      <div class="subject">
        <div class="name">Metody Probabilistyczne</div>
        <div class="short">MP</div>
        <div class="lecture link">
          <a href="#"></a>
        </div>
        <div class="classes link">
          <a href="#"></a>
        </div>
        <div class="moodle classes">
          <a href="#"></a>
        </div>
        <div class="latex">
          <a href="#"></a>
        </div>
        <div class="drive">
          <a href="#"></a>
        </div>
        <div class="github">
          <a href="#"></a>
        </div>
      </div>
</div>
```
