 #Database Frame
Frame_Database = tk.Frame(Frame_Data, bg="#e3f4f1", bd=11, relief=tk.GROOVE)
Frame_Database.pack(fill=tk.BOTH, expand=True)
 
Scroll_X = tk.Scrollbar(Frame_Database, orient=tk.HORIZONTAL)
Scroll_Y = tk.Scrollbar(Frame_Database, orient=tk.VERTICAL)
 
Student_table = ttk.Treeview(Frame_Database, columns=("Name", "Roll No", "Gender", "Class","Contact No","D.O.B", "Address"), yscrollcommand= Scroll_Y.set,xscrollcommand= Scroll_X.set)
 
Scroll_X.config(command=Student_table.xview)
Scroll_X.pack(side=tk.BOTTOM, fill=tk.X)
Scroll_Y.config(command=Student_table.yview)
Scroll_Y.pack(side=tk.RIGHT, fill=tk.Y)
 
Student_table.heading("Roll No", text="Roll No")
Student_table.heading("Name", text="Name")
Student_table.heading("Gender", text="Gender")
Student_table.heading("Class", text="Class")
Student_table.heading("Contact No", text="Contact No")
Student_table.heading("D.O.B", text="D.O.B")
Student_table.heading("Address", text="Address")
 
Student_table['show']='headings'
Student_table.column("Roll No",width= 100)
Student_table.column("Name",width= 100)
Student_table.column("Gender",width= 100)
Student_table.column("Class",width= 100)
Student_table.column("Contact No",width= 100)
Student_table.column("D.O.B",width= 100)
Student_table.column("Address",width= 150)
 
Student_table.pack(fill=tk.BOTH, expand=True)
