Download Link: https://assignmentchef.com/product/solved-itis-cs-5180-assignment2-task-organizer
<br>
In this assignment you will get familiar with Android intents (Explicit/Implicit), data passing between activities, starting activity for result, alert dialogs and dynamic UI management. This is a To-Do List App, where user gets to enter a task title, the time and date, along with other task details. User should be able edit, display and delete tasks. This is a multi screen application, the Main Activity is displayed in Figure 1.

<strong>Important App Requirements: </strong>

<ol>

 <li>Your assignment will not be graded if it does not meet these requirements, and you will not be granted any points on your submission.</li>

 <li>All strings should be read from your strings.xml.The string values used for the text labels, and button labels should be read from the strings.xml file and should not be hardwired in the layout file.</li>

 <li><strong>You should not use static variables to share data between activities, and should use intent extras to share data between activities.</strong></li>

</ol>

<table width="534">

 <tbody>

  <tr>

   <td width="223"></td>

   <td rowspan="2" width="88"> </td>

   <td width="223"></td>

  </tr>

  <tr>

   <td width="223">                          <strong>Task Title              </strong>Task Date Task TimeTask Priority<strong>Task 1 of 5</strong></td>

   <td width="223">TitlePriority:HighMediumLow</td>

  </tr>

 </tbody>

</table>

(a) Main Activity                                                 (b) Create Task Activity

<strong>Figure 1, App Wireframe</strong>

<strong>Main Activity (50 Points) </strong>

The Main Activity (View Tasks) enables the user to display the currently stored tasks as show in Figure 1(a). The Main Activity should maintain a LinkedList of the current Task Objects. The activity requirements are as follows:

<ul>

 <li>The task list should be stored in the Main Activity. The task list should be ordered by task date and time, ordered in <strong>ASCENDING</strong></li>

 <li>Each stored task should be displayed as shown in Figure 1(a). Note the buttons at the top and button of the screen.</li>

 <li>At the bottom of the interface should indicate “Task M of N”, where M is the current task index and N is the total number of tasks. These numbers should be dynamically updated when tasks are added or deleted, or you navigate to another task.</li>

 <li>The buttons at the bottom of the interface described from left to right:</li>

 <li><strong>Goto first task:</strong> Should display the first task stored in the linked list.</li>

 <li><strong>Goto previous task:</strong> Should go to the previous task. If the currently displayed task is the first task, then display a toast indicating that the current task is the first task.</li>

 <li><strong>Edit current task:</strong> Should display the Edit Task activity.</li>

 <li><strong>Delete current task:</strong> Should delete the currently displayed task, update the interface and display the first task.</li>

 <li><strong>Goto next task:</strong> Should display the next task, if the currently displayed task is the last task in the list then should display a toast indicating that the current task is the last task.</li>

 <li><strong>Goto last task: </strong>Should display the last task stored in the linked list.</li>

 <li>At the top of the Main Activity should display a “+” button to allow the creation of new tasks. Clicking the “+” button should start the Create Task Activity, you should consider using the start activity for result, as the Create Task Activity should send back the created task to the Main Activity. Upon returning from the Create Task Activity the list of tasks should be updated and redisplayed to show the newly added task in displayed layout.</li>

</ul>

<strong><u>Create Task Activity (30 Points)</u> </strong>

The Create Task Activity is displayed in Figure 2. Implement the following requirements:

<ul>

 <li>When the user selects “+” button in the Main Activity, the Create Task Activity should be started as shown in Figure 2.</li>

 <li>The task title should not exceed 20 characters. The date and time EditTexts should not be editable, you should set their key listeners to null, (setKeyListener(null)). When the date and time EditTexts are the corresponding date picker or time picker dialog boxes should be displayed to enable the user to pick the date or time respectively. Figure 2, shows the date and time picker displayed when the date and time edit text is clicked. The selected time and date should be displayed in their corresponding edit text as shown in Figure 2.</li>

 <li>For information related to the time picker check <a href="https://developer.android.com/reference/android/app/TimePickerDialog.html">http://developer.android.com/ </a><a href="https://developer.android.com/reference/android/app/TimePickerDialog.html">reference/android/app/TimePickerDialog.html</a></li>

 <li>For information related to the date picker check <a href="https://developer.android.com/reference/android/app/DatePickerDialog.html">http://developer.android.com/ </a><a href="https://developer.android.com/reference/android/app/DatePickerDialog.html">reference/android/app/DatePickerDialog.html</a></li>

 <li>Clicking the Save button should save the fields and selected Priority level as a Task object and send it back as a result to the Main Activity so that it can be stored and displayed in the task list. The Main Activity should navigate to the newly stored task and display it.</li>

</ul>

<strong>Figure 2, Create Task</strong>

<strong><u>Edit Task Activity (20 Points)</u> </strong>

The edit task activity is displayed in Figure 3. Implement the following requirements:

<ul>

 <li>When the user selects a Task in the Main Activity, and clicks the“Edit”, the Edit Task Activity should be started as shown in Figure 3.</li>

 <li>The task info should be populated in the Edit Task Activity as shown in Figure 3.</li>

 <li>The UI for this activity is similar to the Create Task Activity and should follow the same text size, and time/date picker implementation and restrictions.</li>

 <li>Clicking the Save button should save the fields as a Task object and send it back as a result to the Main Activity. The Main Activity should display the edited task to show the latest updates.</li>

</ul>

<strong>Figure 3, Edit Task</strong>