# TheDevilIsInTheDetails

This repository was my testing ground for assests and fnctionality before I would implement them into our group repo.
This repository is my first programing project (excluding a pong tutorial I made in unity and some flash I did 10years ago).
This repository also was a testing ground when it comes to using github. I had many problems and learned the hard way. 
I lost about 50 comits, destroyed my .git folder, lost maps and assets. It has been paynfull but the learning curve was fantastic.

About our project:
The Devil Is In The Details

<p align="center">
  <img src="" width="350"/>

</p>

First person adventure puzzles game.

Droped in the garden of a country manor you have to find the three lost gnomes while being chased by a demon. You are helped in this task by magical spectacles that reveal indications and clues. Wile you are wearing the specs, you can't see the monster chasing you. Luckely he is quite vocal and not very discret.


-Workflow, process and organisation
-My role
-Conclusion


There is three puzzles in our game and they are following similar principals (find the combinaison to open a gate).

In the puzzle I created, invisible runes show you the way and reveal a code that will unlock your way to the gnome.  


let contents = ["Slide 1", "Slide 2", "Slide 3"].map { title -> Content in
  let label = UILabel(frame: CGRect(x: 0, y: 0, width: 200, height: 100))
  label.text = title

  let position = Position(left: 0.3, top: 0.4)

  return Content(view: label, position: position)
}

var slides = [SlideController]()

for index in 0...2 {
  let content = contents[index]
  let controller = SlideController(contents: [content])
  let animation = TransitionAnimation(
    content: content,
    destination: Position(left: 0.5, top: content.initialPosition.top),
    duration: 2.0,
    dumping: 0.8,
    reflective: true)
  controller.add(animations: [animation])

  slides.append(controller)
}

presentationController.add(slides)
