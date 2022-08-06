#1 Can we nest the Scaffold widget? Why or Why not?
We should not nest the scaffold because for each page the scoffold should be one.
We can use it though but it can have some side effects like the keyboard overlap.

#2 What are the different ways we can create a custom widget ?
1. we can create custom widget by combining or using the simpler widgets 
2. we can use the CustomPanter to draw and create the widget.
3. we can use the RenderObject which is used internally to create the widget.

#3 How can I access platform(iOS or Android) specific code from Flutter?
We can create Method channel to communicate to the native platform specific code 
and get the result from the method return value.

#4 What is BuildContext? What is its importance?
The BuildContext is used to locate a particular widget in a widget tree and every widget has its own BuidContext 
i.e. a particular BuildContext is associated with only one widget.

##Coding
#1 Refactor the code below so that the children will wrap to the next line when
the display width is small for them to fit.

class LongStringWidget extends StatelessWidget {
  const LongStringWidget({Key? key}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    return Wrap(
      alignment: WrapAlignment.start,
      children: [
        Chip(label: Text('I')),
        Chip(label: Text('am')),
        Chip(label: Text('looking')),
        Chip(label: Text('for')),
        Chip(label: Text('a')),
        Chip(label: Text('Job')),
        Chip(label: Text('and')),
        Chip(label: Text('I')),
        Chip(label: Text('need')),
        Chip(label: Text('a')),
        Chip(label: Text('Job'))
      ],
    );
  }
}
//add image

#2  Identify the problem in the following code block and correct it.

Code is working fine , did not see anyting wrong.

#3 In the below code, list1 declared with var, list2 with final and list3 with const.
What is the difference between these lists? Will the last two lines compile?

last line will not work,it will give runtime error as - "Cannot modify an unmodifiable list"
1. var list - its mutable type with all its elements are also immutable
2. final list - we can assign the list once but we can not reassign the list again but we can reassign the item in the list.
3. const list - must be initialized with const value and we can not change its elements value.