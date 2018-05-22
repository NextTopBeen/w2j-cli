# W2J-CLI

JavaWeb Command-line Framework, help you easily build a command line javaWeb System.

## Why need it
- Some functions are provided to professional and do not want to invest in developing front-end.
- Quick development of a simple management system
-  provided some tools by whe Web
- Quick,simple,fun and so on



## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

What things you need to install the software and how to install them


## Some examples

#### Base
Base input and output,Text-table, Confirm,Auto-Complete,
```
@HJRoot(name="task",help = "task related operation")
public class TaskTest {
    @HJCommand(name = "list",help = "get the list of task")
    public String list(
            @HJValue(name="start",help = "start time. example：2017-12-1")
                    String start,
            @HJValue(name="end",help = "end time. example：2018-12-1")
                    String end
    ) throws WjException {
        TextTable table =  TextTable.create();
        table.config("id");
        table.config("name");
        table.config("status");
        table.config("createTime");

        table.add(Arrays.asList("1","task-1","open","2017-12-1"));
        table.add(Arrays.asList("2","task-2","open","2017-12-2" ));

        return View.text(table.buildTable());
    }

    @HJCommand(name = "stop",ask = true,help = "stop the task")
    public String close(
            @HJValue(name="id",help = "the task id",req = true)
                    String id,
            @HJContext()
                    Context context

    ){
        return View.text("task is closed");
    }
}```
![image](https://raw.githubusercontent.com/wiki/frost373/w2j-cli/img/base.gif)

#### Html Table and Ascii Table



#### Help

#### Login

#### Animation

#### Script
