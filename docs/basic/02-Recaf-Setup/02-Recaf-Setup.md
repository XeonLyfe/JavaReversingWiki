# Chapter 2 - Getting to Know Recaf

## 1. What is Recaf?

Recaf is an open source Java bytecode editor, Recaf greatly reduces the difficulty of editing Java bytecode. Difficult tasks like updating the frame stack are done automatically.

<br/>
## 2. Download Recaf

https://github.com/Col-E/Recaf

<br/>
## 3. Configure Recaf:

![image-20210424170434518](image/Recaf Display Config.png)

Change the Class Mode to Table, so that each Class will be read in table mode by default (only table mode can be used for Java bytecode editing)

<br/>
![image-20210424170722970](image/Recaf Keybinds Config.png)

Modify the shortcut key to save the modification, you can change whatever you want, because sometimes Ctrl+S will be occupied by other applications TAT

<br/>
![image-20210424171245403](image/Recaf Assemble cfg.png)

Turn off Use existing data, this function may be interfered by crasher, other default

<br/>
![image-20210424171406825](image/Recaf temporary switching mode.png)

The method of temporarily switching decompilation/table/hexadecimal code mode is shown in the figure

<br/>

## 4. Use Recaf:

(Mode: Table table mode):

![image-20210430215754254](image/Recaf expVariable Table Class.png)

The Class tab displays the properties of the selected class

The Fields field (that is, member variables) tab is empty because no member variables are defined in this class

The Methods method (ie member function) tab is as follows

![](image/ExampleVariableTable.png)

Put the mouse pointer on the icon in the Access column to obtain the access permission of the corresponding method (public, static, etc.)

Return is the method return value type

The Name column is the name of the method

Arguments are the parameters required by the method

Right-click the method to perform Remove (delete method), search reference (find out the reference to this method), Rename (rename method), Edit with assembler ("edit assembly code")

![image-20210430222052872](image/ExampleVariableASM.png)
