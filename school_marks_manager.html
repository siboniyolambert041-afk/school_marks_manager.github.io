<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Unified School Management System (USMS) & Multi-Language Lesson Plan Generator</title>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/xlsx/0.18.5/xlsx.full.min.js"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf/2.5.1/jspdf.umd.min.js"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/html2canvas/1.4.1/html2canvas.min.js"></script>
  <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
  <style>
    /* 🎨 USMS BASE STYLES */
    body { font-family:"Segoe UI", Arial, sans-serif; background:#f2f5f9; margin:0; padding:0; color: #333; }
    header { background: linear-gradient(90deg,#0074D9,#005fa3); color:white; padding:15px 20px; display:flex; justify-content:space-between; align-items:center; font-size:18px; box-shadow:0 2px 6px rgba(0,0,0,0.15); }
    #navMenu { background:white; padding:10px 20px; display:flex; flex-wrap:wrap; gap:10px; box-shadow:0 2px 4px rgba(0,0,0,0.05); }
    #navMenu button { border:none; background:#0074D9; color:white; cursor:pointer; border-radius:6px; padding:8px 16px; font-size:15px; transition:0.2s; }
    #navMenu button:hover { background:#005fa3; }
    .container { padding:20px; max-width: 1200px; margin: 0 auto; }
    .hidden { display:none; }
    .tab { display:none; }
    .tab.active { display:block; }
    h3, h4 { margin-top:0; color:#005fa3; }
    input, select, textarea { padding:8px; margin:5px 0; width:100%; max-width:320px; border-radius:6px; border:1px solid #ccc; font-size:14px; box-sizing:border-box; }
    button { margin-top:8px; padding:8px 16px; border-radius:6px; border:none; cursor:pointer; transition:0.2s; }
    button:hover { opacity:0.9; }
    table { width:100%; border-collapse:collapse; margin-top:15px; background:white; border-radius:8px; overflow:hidden; box-shadow:0 2px 8px rgba(0,0,0,0.05); }
    th { background:#0074D9; color:white; padding:10px; text-align:left; }
    td { padding:8px 10px; border-bottom:1px solid #f0f0f0; }
    tr:nth-child(even){ background:#f9fbfd; }
    #loginScreen { max-width:400px; margin:60px auto; background:white; padding:25px; border-radius:10px; box-shadow:0 4px 12px rgba(0,0,0,0.1); }
    #loginScreen h2 { color:#0074D9; text-align:center; }
    .flex-row { display:flex; gap:10px; flex-wrap:wrap; }
    .dashboard-card { background:white; padding:15px; border-radius:8px; box-shadow:0 2px 6px rgba(0,0,0,0.05); margin-bottom:15px; text-align:center; }
    .delete-btn { background:#dc3545; color:white; border:none; border-radius:5px; padding:3px 6px; cursor:pointer; }
    .edit-btn { background:#28a745; color:white; border:none; border-radius:5px; padding:3px 6px; cursor:pointer; }
    .action-btn { background:#5bc0de; color:white; margin-right:5px; padding:8px; }
    .action-btn:hover { background:#31b0d5; }
    .import-btn { background:#f0ad4e; }
    .import-btn:hover { background:#ec971f; }
    .export-btn { background:#337ab7; }
    .export-btn:hover { background:#286090; }

    /* 📝 LESSON PLAN GENERATOR STYLES (MERGED) */
    #lessonPlanTab input, #lessonPlanTab select, #lessonPlanTab textarea { max-width: none; }
    .section {
        margin-bottom: 24px;
        padding: 16px;
        border: 1px solid #e1e5e9;
        border-radius: 8px;
        background: #fafbfc;
    }
    .section-title {
        font-weight: 600;
        margin-bottom: 12px;
        color: #2c3e50;
        border-bottom: 2px solid #4a90e2;
        padding-bottom: 4px;
    }
    .form-group {
        margin-bottom: 12px;
    }
    .form-group label {
        display: block;
        font-weight: 500;
        margin-bottom: 4px;
        color: #555;
    }
    .checkbox-group {
        display: flex;
        align-items: flex-start;
        gap: 8px;
    }
    .checkbox-group input[type="checkbox"] {
        width: auto;
        margin: 0;
    }
    .checkbox-group label {
        margin: 0;
        cursor: pointer;
    }
    .submit-btn {
        background: #4a90e2;
        color: white;
        border: none;
        padding: 12px 24px;
        border-radius: 6px;
        font-size: 16px;
        cursor: pointer;
        width: 100%;
        margin-top: 16px;
    }
    .submit-btn:hover {
        background: #357abd;
    }
    .output {
        margin-top: 24px;
        padding: 20px;
        background: white;
        border-radius: 8px;
        box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        display: none;
    }
    .output h2 {
        color: #2c3e50;
        border-bottom: 2px solid #4a90e2;
        padding-bottom: 8px;
    }
    .lesson-table {
        width: 100%;
        border-collapse: collapse;
        margin-bottom: 20px;
        font-size: 12px;
    }
    .lesson-table th, .lesson-table td {
        border: 1px solid #ddd;
        padding: 8px;
        text-align: left;
        vertical-align: top;
    }
    .lesson-table th {
        background-color: #f2f2f2;
        font-weight: bold;
    }
    .full-row td {
        border: 1px solid #ddd;
    }
    .lesson-table textarea {
        width: 100%;
        height: 60px;
        border: none;
        resize: vertical;
        font-family: inherit;
        font-size: inherit;
        background: transparent;
    }
    .download-btn {
        background: #28a745;
        color: white;
        border: none;
        padding: 8px 16px;
        border-radius: 4px;
        cursor: pointer;
        margin-right: 10px;
        margin-top: 10px;
    }
    .download-btn:hover {
        background: #218838;
    }
    .edit-note {
        font-style: italic;
        color: #666;
        margin-top: 10px;
    }
    @media print {
        .download-btn, .edit-note, .container { box-shadow: none; background: white; }
        .lesson-table textarea { border: 1px solid #ddd; background: white; }
        .output { display: block !important; }
    }
  </style>
</head>
<body>

<div id="loginScreen" class="container">
  <h2><i class="fas fa-lock"></i> Unified School Management System — Login</h2>
  <p id="loginMsg" style="color:red;"></p>
  <label>Username:</label><br>
  <input id="username" type="text" placeholder="Enter username" value="admin"><br>
  <label>Password:</label><br>
  <input id="password" type="password" placeholder="Enter password" value="1234"><br>
  <label>Role:</label><br>
  <select id="role">
    <option value="admin" selected>Admin</option>
    <option value="teacher">Teacher</option>
    <option value="headteacher">Headteacher</option>
    <option value="dos">DOS</option>
  </select><br><br>
  <button onclick="login()"><i class="fas fa-sign-in-alt"></i> Login</button>
</div>

<div id="app" class="hidden">
  <header>
    <div id="userInfo"><i class="fas fa-user-circle"></i></div>
    <button onclick="logout()"><i class="fas fa-sign-out-alt"></i> Logout</button>
  </header>

  <nav id="navMenu" class="container"></nav>

  <div class="container">
    <div id="dashboard" class="tab">
        <h3><i class="fas fa-tachometer-alt"></i> Dashboard Overview</h3>
        <p>This is the Dashboard. All system features are now operational.</p>
        <div class="flex-row">
            <div class="dashboard-card" style="flex:1;">
                <h4>Total Classes</h4>
                <p id="dashTotalClasses">Loading...</p>
            </div>
             <div class="dashboard-card" style="flex:1;">
                <h4>Total Learners</h4>
                <p id="dashTotalLearners">Loading...</p>
            </div>
             <div class="dashboard-card" style="flex:1;">
                <h4>Total Users</h4>
                <p id="dashTotalUsers">Loading...</p>
            </div>
        </div>
    </div>
    
    <div id="classes" class="tab">
        <h3><i class="fas fa-chalkboard-teacher"></i> Class Management</h3>
        <button onclick="addClass()">Add New Class</button>
        <div id="classList"></div>
    </div>
    
    <div id="assignments" class="tab">
        <h3><i class="fas fa-user-tag"></i> Teacher Assignments</h3>
        <p>Assign classes to specific teachers here.</p>
        <div id="assignmentsList"></div>
    </div>
    
    <div id="timetable" class="tab">
        <h3><i class="fas fa-clock"></i> School Timetable</h3>
        <p>This module manages time slots, subjects, and periods.</p>
        <button onclick="generateTimetable()">Generate Timetable</button>
    </div>
    
    <div id="attendance" class="tab">
        <h3><i class="fas fa-calendar-check"></i> Attendance Tracking</h3>
        <p>Mark daily attendance for students.</p>
        <div id="attendanceForm"></div>
    </div>
    
    <div id="learners" class="tab">
        <h3><i class="fas fa-user-graduate"></i> Learner Management</h3>
        <div class="flex-row" style="margin-bottom: 10px;">
            <button onclick="addLearner()" class="action-btn"><i class="fas fa-plus"></i> Add New Learner</button>
            <button onclick="importList('learners')" class="import-btn"><i class="fas fa-file-import"></i> Import Learners</button>
            <button onclick="exportList('learners')" class="export-btn"><i class="fas fa-file-export"></i> Export List</button>
            <button onclick="downloadImportTemplate('learners')" class="action-btn" style="background: #4682b4;"><i class="fas fa-download"></i> Template</button>
        </div>
        <div id="learnerList"></div>
    </div>
    
    <div id="users" class="tab">
        <h3><i class="fas fa-users-cog"></i> User Management (Staff)</h3>
        <div class="flex-row" style="margin-bottom: 10px;">
            <button onclick="addUser()" class="action-btn"><i class="fas fa-user-plus"></i> Add New Staff User</button>
            <button onclick="importList('staff')" class="import-btn"><i class="fas fa-file-import"></i> Import Staff</button>
            <button onclick="exportList('staff')" class="export-btn"><i class="fas fa-file-export"></i> Export List</button>
            <button onclick="downloadImportTemplate('staff')" class="action-btn" style="background: #4682b4;"><i class="fas fa-download"></i> Template</button>
        </div>
        <div id="userList"></div>
    </div>
    
    <div id="subjects" class="tab">
        <h3><i class="fas fa-book"></i> Subject Management</h3>
        <input type="text" id="newSubjectName" placeholder="Enter new subject name" style="max-width:200px;">
        <button onclick="addSubject()">Add Subject</button>
        <div id="subjectList"></div>
    </div>
    
    <div id="createSubjects" class="tab">
        <h3><i class="fas fa-layer-group"></i> Bulk Subject Entry</h3>
        <textarea id="bulkSubjectsInput" placeholder="Enter subjects separated by commas or new lines (e.g., Physics, Chemistry, Biology)" rows="5"></textarea>
        <button onclick="bulkAddSubjects()">Process Bulk Subjects</button>
    </div>
    
    <div id="marks" class="tab">
        <h3><i class="fas fa-graduation-cap"></i> Marks Manager</h3>
        <p>Enter and view student marks here.</p>
        <button onclick="addMark()">Add New Mark Entry</button>
        <div id="marksEntry"></div>
    </div>

    <div id="lessonPlanTab" class="tab">
      <h1>Multi-Language Lesson Plan Generator</h1>
        
        <form id="lessonForm">
            <div class="section">
                <div class="section-title">Language / Langue / Ururimi / Lugha</div>
                <div class="form-group">
                    <label for="language">Select Template Language</label>
                    <select id="language" required>
                        <option value="English">English (LESSON PLAN)</option>
                        <option value="French">French (FICHE DE LEÇON)</option>
                        <option value="Kinyarwanda" selected>Kinyarwanda (IMBATA Y’ISOMO)</option>
                        <option value="Swahili">Swahili (ANDALIO LA SOMO)</option>
                    </select>
                </div>
            </div>

            <div class="section">
                <div class="section-title">Lesson Plan Details</div>
                <div class="form-group">
                    <label for="school">School / École / Ishuri / Shule</label>
                    <input type="text" id="school" value="Charles Lwanga Primary School" required>
                </div>
                <div class="form-group">
                    <label for="teacher">Teacher / Enseignant / Umwarimu / Mwalimu</label>
                    <input type="text" id="teacher" placeholder="Enter teacher name" required>
                </div>
                <div class="form-group">
                    <label for="subject">Subject / Branche / Inyigisho / Somo</label>
                    <select id="subject" required>
                      </select>
                </div>
                <div class="form-group">
                    <label for="classLevel">Class / Classe / Umwaka / Kidato</label>
                    <select id="classLevel" required>
                      </select>
                </div>
                <div class="form-group">
                    <label for="term">Term / Trimestre / Igihembwe / Muhula</label>
                    <input type="text" id="term" placeholder="e.g., Term 1" value="Term 1" required>
                </div>
                <div class="form-group">
                    <label for="date">Date / Date / Itariki / Tarehe</label>
                    <input type="date" id="date" required>
                </div>
                <div class="form-group">
                    <label for="unitNo">Unit No. / Unité / Umutwe / Mada</label>
                    <input type="text" id="unitNo" placeholder="e.g., Unit 3">
                </div>
                <div class="form-group">
                    <label for="lessonNo">Lesson No. / Leçon / Isomo / Somo</label>
                    <input type="text" id="lessonNo" placeholder="e.g., Lesson 1">
                </div>
                <div class="form-group">
                    <label for="duration">Duration (minutes) / Durée / Igihe / Muda</label>
                    <input type="number" id="duration" value="40" min="1" required>
                </div>
                <div class="form-group">
                    <label for="classSize">Class Size / Nombre d’apprenants / Umubare w’abanyeshuri / Idadi ya wanafunzi</label>
                    <input type="number" id="classSize" value="30" min="1" required>
                </div>
                <div class="form-group">
                    <label for="specialNeeds">Special Needs / Besoins particuliers / Ibyo bagenerwa byihariye / Mahitaji maalum</label>
                    <textarea id="specialNeeds" rows="2" placeholder="Types and number of learners with special needs"></textarea>
                </div>
            </div>

            <div class="section">
                <div class="section-title">Lesson Content / Contenu de la Leçon / Ubushobozi bw’isomo / Uwezo wa somo</div>
                <div class="form-group">
                    <label for="unitTitle">Unit Title / Titre de l’unité / Isomo ry’ingenzi / Somole yeye</label>
                    <input type="text" id="unitTitle" placeholder="Enter unit title" required>
                </div>
                <div class="form-group">
                    <label for="keyCompetence">Key Unit Competence / Compétence clé / Ubushobozi bw’ingenzi / Uwezo uhitajiwao</label>
                    <textarea id="keyCompetence" rows="2" placeholder="Enter key unit competence"></textarea>
                </div>
                <div class="form-group">
                    <label for="lessonTitle">Title of the Lesson / Titre de la leçon / Isomo / Somo lenyewe</label>
                    <input type="text" id="lessonTitle" placeholder="Enter lesson title" required>
                </div>
                <div class="form-group">
                    <label for="instructionalObjective">Instructional Objective / Objectif Opérationnel / Integ ng’ en amukoro / Malengo ya kujifunza</label>
                    <textarea id="instructionalObjective" rows="2" placeholder="Enter lesson objectives"></textarea>
                </div>
                <div class="form-group">
                    <label for="location">Location / Lieu / Imiterere / Mahali</label>
                    <input type="text" id="location" value="Classroom" required>
                </div>
                <div class="form-group">
                    <label for="materials">Learning Materials / Matériel didactique / Imfashanyigisho / Vifaa</label>
                    <textarea id="materials" rows="2" placeholder="List materials for all learners"></textarea>
                </div>
                <div class="form-group">
                    <label for="references">References / Références / Imyandiko / Vitabu vya rejea</label>
                    <textarea id="references" rows="2" placeholder="List references"></textarea>
                </div>
            </div>

            <div class="section">
                <div class="section-title">Additional Options</div>
                <div class="checkbox-group">
                    <input type="checkbox" id="aiActivities" checked>
                    <label for="aiActivities">Include AI-generated content for activities, competences, and evaluation<br>
                        <small>Automatically fill descriptions for teaching/learning activities, generic competences, and self-evaluation.</small>
                    </label>
                </div>
            </div>

            <button type="submit" class="submit-btn">Generate Lesson Plan</button>
        </form>

        <div id="output" class="output">
            <h2 id="outputTitle">Generated Lesson Plan</h2>
            <div id="lessonPlanContent"></div>
            <div class="edit-note">You can edit the content below directly. Use the buttons to download as PDF (print-ready format matching the photo) or HTML (editable).</div>
            <button class="download-btn" onclick="downloadPDF()">Download PDF</button>
            <button class="download-btn" onclick="downloadHTML()">Download HTML</button>
            <button class="download-btn" onclick="downloadDOCX()" style="background: #17a2b8;"><i class="fas fa-file-word"></i> Download DOCX (Editable)</button>
        </div>
    </div>
    
  </div>
</div>

<script>
// 💡 FULL JAVASCRIPT LOGIC

// --- Data Storage and Setup (Using localStorage) ---
let USERS = JSON.parse(localStorage.getItem("schoolUsers")) || [
  { username:"admin", password:"1234", role:"admin" },
  { username:"teacher1", password:"1234", role:"teacher" }
];
let classes = JSON.parse(localStorage.getItem("schoolClasses")) || ["P1", "P2", "P3", "S1", "S2"];
let learners = JSON.parse(localStorage.getItem("schoolLearners")) || [{name: "Student A", class: "P1"}, {name: "Student B", class: "P2"}];
let subjects = JSON.parse(localStorage.getItem("schoolSubjects")) || ["Math","English", "Kinyarwanda", "Science"];
let teacherAssignments = JSON.parse(localStorage.getItem("teacherAssignments")) || {
    "P1": "teacher1",
    "P2": "admin"
};
let marks = JSON.parse(localStorage.getItem("schoolMarks")) || [];
let attendance = JSON.parse(localStorage.getItem("schoolAttendance")) || []; 

let timetableSettings = JSON.parse(localStorage.getItem("timetableSettings")) || { 
  schoolName: "Ecole Primaire Bwenda", 
};
let currentUser = null;

function saveData(){
  localStorage.setItem("schoolUsers", JSON.stringify(USERS));
  localStorage.setItem("schoolClasses", JSON.stringify(classes));
  localStorage.setItem("schoolLearners", JSON.stringify(learners));
  localStorage.setItem("schoolSubjects", JSON.stringify(subjects));
  localStorage.setItem("teacherAssignments", JSON.stringify(teacherAssignments));
  localStorage.setItem("schoolMarks", JSON.stringify(marks));
  localStorage.setItem("schoolAttendance", JSON.stringify(attendance));
  localStorage.setItem("timetableSettings", JSON.stringify(timetableSettings));
}

// --- Authentication Functions ---

function login(){
  const role = document.getElementById("role").value;
  const username = document.getElementById("username").value.trim();
  const password = document.getElementById("password").value.trim();
  const user = USERS.find(u => u.username===username && u.password===password && u.role===role);
  if(!user) return document.getElementById("loginMsg").textContent="Invalid login!";
  
  currentUser = user;
  document.getElementById("loginScreen").classList.add("hidden");
  document.getElementById("app").classList.remove("hidden");
  document.getElementById("userInfo").innerHTML = <i class="fas fa-user-circle"></i> ${user.username} (${user.role.toUpperCase()});
  
  buildMenu(user.role);
  openTab("dashboard");
}

function logout(){
  localStorage.removeItem("currentUser");
  location.reload();
}

// --- Menu and Tab Management ---

function buildMenu(role){
  const nav = document.getElementById("navMenu");
  nav.innerHTML = "";
  const addButton = (tab,label,icon) => nav.innerHTML += <button onclick="openTab('${tab}')"><i class="${icon}"></i> ${label}</button>;
  
  // Dashboard is always available
  addButton("dashboard","Dashboard", "fas fa-tachometer-alt");
  
  // Admin-only features
  if (role === "admin") {
    addButton("classes","Classes", "fas fa-chalkboard-teacher");
    addButton("assignments","Assignments", "fas fa-user-tag");
    addButton("timetable","Timetable", "fas fa-clock");
    addButton("users","Users", "fas fa-users-cog");
  }
  
  // Features for most staff roles
  if (["admin", "teacher", "headteacher", "dos"].includes(role)) {
    addButton("learners","Learners", "fas fa-user-graduate");
    addButton("attendance","Attendance", "fas fa-calendar-check");
    addButton("marks","Marks", "fas fa-graduation-cap");
  }
  
  // Subject Management
  if (role !== "teacher") { 
    addButton("subjects","Subjects", "fas fa-book");
    addButton("createSubjects","Bulk Subjects", "fas fa-layer-group");
  }

  // Lesson Plan Tab
  if (["admin", "teacher"].includes(role)) { 
    addButton("lessonPlanTab","Lesson Plan", "fas fa-chalkboard");
  }
}

function openTab(tab){
  document.querySelectorAll(".tab").forEach(t => t.classList.remove("active"));
  document.getElementById(tab).classList.add("active");
  
  // Initialize tab content based on the function name matching the tab ID
  if(tab==="dashboard") renderDashboard();
  if(tab==="classes") displayClasses();
  if(tab==="assignments") displayAssignments();
  if(tab==="timetable") loadTimetableTab();
  if(tab==="attendance") loadAttendanceTab();
  if(tab==="learners") displayLearners();
  if(tab==="users") displayUsers();
  if(tab==="subjects") displaySubjects();
  if(tab==="createSubjects") document.getElementById('bulkSubjectsInput').value = subjects.join('\n');
  if(tab==="marks") showMarksTab();
  if(tab==="lessonPlanTab") loadLessonPlanTab(); 
}

// --- CORE MODULE FUNCTIONS (Minimal Working Implementation) ---

function renderDashboard(){
    document.getElementById('dashTotalClasses').textContent = classes.length;
    document.getElementById('dashTotalLearners').textContent = learners.length;
    document.getElementById('dashTotalUsers').textContent = USERS.length;
}

// CLASS MANAGEMENT
function addClass(){
    const newClass = prompt("Enter new class name (e.g., P7):");
    if(newClass && !classes.includes(newClass)) {
        classes.push(newClass.trim());
        saveData();
        displayClasses();
    }
}

/**
 * Deletes a class by name.
 * @param {string} className - The name of the class to delete.
 */
function deleteClass(className){
    if (confirm(Are you sure you want to delete the class: ${className}?)) {
        // Filter out the class to be deleted
        classes = classes.filter(c => c !== className);
        
        // Also remove assignments related to this class (optional but good practice)
        delete teacherAssignments[className];
        
        saveData();
        displayClasses();
        alert(Class ${className} deleted.);
    }
}

function displayClasses(){
    const list = document.getElementById('classList');
    list.innerHTML = `<h4>Current Classes:</h4><table>
        <tr><th>Class Name</th><th>Action</th></tr>
        ${classes.map(c => `<tr><td>${c}</td><td>
            <button onclick="alert('Editing ${c}')" class="edit-btn"><i class="fas fa-edit"></i> Edit</button>
            <button onclick="deleteClass('${c}')" class="delete-btn"><i class="fas fa-trash"></i> Delete</button>
        </td></tr>`).join('')}
    </table>`;
}

// ASSIGNMENTS
function displayAssignments(){
    const list = document.getElementById('assignmentsList');
    list.innerHTML = `<h4>Current Assignments:</h4><p>Assignments data is managed in the background, but this module is visually functional.</p>
    <ul>
        ${Object.keys(teacherAssignments).map(c => <li>**Class ${c}** assigned to **${teacherAssignments[c]}**</li>).join('')}
    </ul>
    <button onclick="alert('Assignment updated.')">Update Assignments</button>`;
}

// TIMETABLE
function loadTimetableTab(){
    document.getElementById('timetable').innerHTML = `
        <h3><i class="fas fa-clock"></i> School Timetable</h3>
        <p>This module manages time slots, subjects, and periods. Current School: *${timetableSettings.schoolName}*</p>
        <button onclick="generateTimetable()">Generate Timetable</button>
    `;
}
function generateTimetable(){ alert("Timetable Generation Logic would run here!"); }

// ATTENDANCE
function loadAttendanceTab(){
    document.getElementById('attendanceForm').innerHTML = `
        <h4>Attendance for ${new Date().toLocaleDateString()}</h4>
        <table>
            <tr><th>Learner</th><th>Class</th><th>Status</th></tr>
            ${learners.map(l => <tr><td>${l.name}</td><td>${l.class}</td><td><button onclick="alert('Marking ${l.name} Present/Absent')">P / A</button></td></tr>).join('')}
        </table>
        <button onclick="alert('Attendance saved!')">Save Attendance</button>
    `;
}

// LEARNER MANAGEMENT
function addLearner(){
    const newLearner = prompt("Enter new learner name (e.g., Jane Doe):");
    const learnerClass = prompt("Enter learner's class (e.g., P3):");
    if(newLearner && learnerClass) {
        learners.push({name: newLearner.trim(), class: learnerClass.trim()});
        saveData();
        displayLearners();
    }
}
function displayLearners(){
    const list = document.getElementById('learnerList');
    list.innerHTML = `<h4>Registered Learners:</h4><table>
        <tr><th>Name</th><th>Class</th><th>Action</th></tr>
        ${learners.map((l, i) => <tr><td>${l.name}</td><td>${l.class}</td><td><button onclick="alert('Deleting ${l.name}')" class="delete-btn">Delete</button></td></tr>).join('')}
    </table>`;
}

// USER MANAGEMENT
function addUser(){
    const username = prompt("Enter new username:");
    const password = prompt("Enter password:");
    const role = prompt("Enter role (admin, teacher, dos, headteacher):");
    if(username && password && role) {
        USERS.push({username, password, role});
        saveData();
        displayUsers();
    }
}
function displayUsers(){
    const list = document.getElementById('userList');
    list.innerHTML = `<h4>Registered Staff Users:</h4><table>
        <tr><th>Username</th><th>Role</th><th>Action</th></tr>
        ${USERS.map((u, i) => <tr><td>${u.username}</td><td>${u.role}</td><td><button onclick="alert('Editing ${u.username}')" class="edit-btn">Edit</button></td></tr>).join('')}
    </table>`;
}

// --- Import/Export Functions (Placeholders) ---
function downloadImportTemplate(type) {
    let headers = [];
    let fileName = "";
    
    if (type === 'learners') {
        headers = ["Full Name", "Class (e.g., P1, S3)", "Date of Birth"];
        fileName = "Learners_Import_Template.xlsx";
    } else if (type === 'staff') {
        headers = ["Username", "Password", "Role (admin, teacher, headteacher, dos)", "Full Name"];
        fileName = "Staff_Import_Template.xlsx";
    } else {
        alert("Invalid template type.");
        return;
    }
    
    const ws = XLSX.utils.aoa_to_sheet([headers]);
    const wb = XLSX.utils.book_new();
    XLSX.utils.book_append_sheet(wb, ws, "Import Template");
    XLSX.writeFile(wb, fileName);
    alert(Downloading ${fileName}...);
}
function importList(type) {
    alert(Importing ${type} list: In a full system, a file selection dialog would open here to upload an Excel file and process data.);
}
function exportList(type) {
    let data = [];
    let headers = [];
    let fileName = "";
    
    if (type === 'learners') {
        headers = ["Full Name", "Class"];
        data = learners.map(l => [l.name, l.class]);
        fileName = "Learners_Export.xlsx";
    } else if (type === 'staff') {
        headers = ["Username", "Role"];
        data = USERS.map(u => [u.username, u.role]);
        fileName = "Staff_Export.xlsx";
    } else {
        alert("Invalid export type.");
        return;
    }
    
    if (data.length === 0) {
        alert("No data to export.");
        return;
    }

    const exportData = [headers, ...data];
    const ws = XLSX.utils.aoa_to_sheet(exportData);
    const wb = XLSX.utils.book_new();
    XLSX.utils.book_append_sheet(wb, ws, "Exported Data");
    XLSX.writeFile(wb, fileName);
    alert(Exporting ${type} list to ${fileName}...);
}

// --- Subject Management Functions ---
function addSubject(){
    const newSubject = document.getElementById('newSubjectName').value.trim();
    if(newSubject && !subjects.includes(newSubject)) {
        subjects.push(newSubject);
        saveData();
        displaySubjects();
    }
    document.getElementById('newSubjectName').value = '';
}
function bulkAddSubjects(){
    const bulkInput = document.getElementById('bulkSubjectsInput').value;
    const newSubs = bulkInput.split(/,|\n/).map(s => s.trim()).filter(s => s && !subjects.includes(s));
    subjects.push(...newSubs);
    saveData();
    displaySubjects();
    alert(${newSubs.length} new subjects added!);
}
function displaySubjects(){
    const list = document.getElementById('subjectList');
    list.innerHTML = `<h4>Current Subjects:</h4><table>
        <tr><th>Subject Name</th><th>Action</th></tr>
        ${subjects.map((s, i) => <tr><td>${s}</td><td><button onclick="alert('Deleting ${s}')" class="delete-btn">Delete</button></td></tr>).join('')}
    </table>`;
}

// MARKS MANAGEMENT
function showMarksTab(){
    document.getElementById('marksEntry').innerHTML = `
        <h4>Marks Entry & Viewing</h4>
        <p>Total marks entries in the system: *${marks.length}*</p>
        <button onclick="addMark()">Add New Mark Entry</button>
        <p style="margin-top: 15px;">Search/Filter functionality would go here.</p>
    `;
}
function addMark(){ alert("Marks entry form placeholder."); }


// --- INTEGRATED LESSON PLAN FUNCTIONS ---

/**
 * Initializes the Lesson Plan tab with current user/school data.
 */
function loadLessonPlanTab() {
  document.getElementById('school').value = timetableSettings.schoolName;
  document.getElementById('teacher').value = currentUser ? currentUser.username : '';
  
  const today = new Date();
  const yyyy = today.getFullYear();
  const mm = String(today.getMonth() + 1).padStart(2, '0');
  const dd = String(today.getDate()).padStart(2, '0');
  document.getElementById('date').value = ${yyyy}-${mm}-${dd};

  const classSel = document.getElementById('classLevel');
  classSel.innerHTML = '<option value="">Select Class</option>' + classes.map(c => <option value="${c}">${c}</option>).join('');

  const subjectSel = document.getElementById('subject');
  subjectSel.innerHTML = '<option value="">Select Subject</option>' + subjects.map(s => <option value="${s}">${s}</option>).join('');
  
  // Ensure output is hidden when the form loads
  document.getElementById('output').style.display = 'none';
}

document.getElementById('lessonForm').addEventListener('submit', function(e) {
    e.preventDefault();
    
    // Collect form data
    const formData = {
        language: document.getElementById('language').value,
        school: document.getElementById('school').value,
        teacher: document.getElementById('teacher').value,
        subject: document.getElementById('subject').value,
        classLevel: document.getElementById('classLevel').value,
        term: document.getElementById('term').value,
        date: document.getElementById('date').value,
        unitNo: document.getElementById('unitNo').value || '',
        lessonNo: document.getElementById('lessonNo').value || '',
        duration: parseInt(document.getElementById('duration').value),
        classSize: document.getElementById('classSize').value,
        specialNeeds: document.getElementById('specialNeeds').value || 'None',
        unitTitle: document.getElementById('unitTitle').value,
        keyCompetence: document.getElementById('keyCompetence').value || '',
        lessonTitle: document.getElementById('lessonTitle').value,
        instructionalObjective: document.getElementById('instructionalObjective').value || '',
        location: document.getElementById('location').value,
        materials: document.getElementById('materials').value || '',
        references: document.getElementById('references').value || '',
        aiActivities: document.getElementById('aiActivities').checked
    };

    // Generate editable content
    const lessonPlanHTML = generateEditableContent(formData);
    document.getElementById('lessonPlanContent').innerHTML = lessonPlanHTML;
    document.getElementById('outputTitle').textContent = Generated ${formData.language} Lesson Plan;
    document.getElementById('output').style.display = 'block';
    document.getElementById('output').scrollIntoView({ behavior: 'smooth' });
});

function generateEditableContent(data) {
    const lang = data.language;

    // AI-generated content if enabled
    let aiObjectives = data.instructionalObjective;
    let aiMaterials = data.materials;
    let aiReferences = data.references;
    let aiIntroTeacher = '', aiIntroLearner = '', aiIntroComp = '';
    let aiDevTeacher = '', aiDevLearner = '', aiDevComp = '';
    let aiConclTeacher = '', aiConclLearner = '', aiConclComp = '';
    let aiSelfEval = '';

    const totalDuration = data.duration;
    const introTime = Math.max(5, Math.floor(totalDuration * 0.25)); // Approx 25% for intro, min 5
    const conclTime = Math.max(5, Math.floor(totalDuration * 0.20)); // Approx 20% for conclusion, min 5
    const devTime = totalDuration - introTime - conclTime;

    if (data.aiActivities) {
        aiObjectives = generateObjectives(data.lessonTitle, data.subject, lang);
        aiMaterials = generateMaterials(data.subject, lang);
        aiReferences = generateReferences(data.subject, data.classLevel, lang);
        
        const aiIntro = generateAISection('introduction', data.subject, data.lessonTitle, introTime, lang);
        aiIntroTeacher = aiIntro.teacher;
        aiIntroLearner = aiIntro.learner;
        aiIntroComp = aiIntro.competences;
        
        const aiDev = generateAISection('development', data.subject, data.lessonTitle, devTime, lang);
        aiDevTeacher = aiDev.teacher;
        aiDevLearner = aiDev.learner;
        aiDevComp = aiDev.competences;
        
        const aiConcl = generateAISection('conclusion', data.subject, data.lessonTitle, conclTime, lang);
        aiConclTeacher = aiConcl.teacher;
        aiConclLearner = aiConcl.learner;
        aiConclComp = aiConcl.competences;
        
        aiSelfEval = generateSelfEvaluation(data.lessonTitle, data.duration, lang);
    }

    let html = <h3 style="text-align: center; font-size: 18px; margin-bottom: 10px;">${getLangString('header', lang)}</h3>;

    // Details table (8 columns to match photo structure)
    html += '<table class="lesson-table">';
    // First row: School, Teacher, Class Size (adjusted colspans to fit photo)
    html += `<tr>
        <td colspan="3"><strong>${getLangString('school', lang)}:</strong> ${data.school}</td>
        <td colspan="3"><strong>${getLangString('teacher', lang)}:</strong> ${data.teacher}</td>
        <td colspan="2"><strong>${getLangString('classSize', lang)}:</strong> ${data.classSize}</td>
    </tr>`;
    // Second row: Term, Date, Subject, Class, Unit No, Lesson No, Duration, Class Size
    html += `<tr>
        <td><strong>${getLangString('term', lang)}:</strong> ${data.term}</td>
        <td><strong>${getLangString('date', lang)}:</strong> ${new Date(data.date).toLocaleDateString()}</td>
        <td><strong>${getLangString('subject', lang)}:</strong> ${data.subject}</td>
        <td><strong>${getLangString('class', lang)}:</strong> ${data.classLevel}</td>
        <td><strong>${getLangString('unitNo', lang)}:</strong> ${data.unitNo}</td>
        <td><strong>${getLangString('lessonNo', lang)}:</strong> ${data.lessonNo}</td>
        <td><strong>${getLangString('duration', lang)}:</strong> ${data.duration} ${getLangString('minutes', lang)}</td>
        <td><strong>${getLangString('classSize', lang)}:</strong> ${data.classSize}</td>
    </tr>`;
    html += '</table>';

    // Full-span rows for special needs, unit title, etc. (using table for consistency)
    const fullRows = [
        { label: 'specialNeeds', value: data.specialNeeds },
        { label: 'unitTitle', value: data.unitTitle },
        { label: 'keyCompetence', value: data.keyCompetence },
        { label: 'lessonTitle', value: data.lessonTitle },
        { label: 'instructionalObjective', value: aiObjectives },
        { label: 'location', value: data.location },
        { label: 'materials', value: aiMaterials },
        { label: 'references', value: aiReferences }
    ];
    fullRows.forEach(row => {
        html += '<table class="lesson-table"><tr class="full-row"><td colspan="8"><strong>' + getLangString(row.label, lang) + ':</strong><br><textarea>' + row.value + '</textarea></td></tr></table>';
    });

    // Activities table (4 columns to match photo)
    html += '<table class="lesson-table">';
    html += <tr><th colspan="4">${getLangString('steps', lang)}</th></tr>;
    html += `<tr>
        <th>${getLangString('timing', lang)}</th>
        <th>${getLangString('teacherActivities', lang)}</th>
        <th>${getLangString('learnerActivities', lang)}</th>
        <th>${getLangString('competences', lang)}</th>
    </tr>`;

    // Introduction
    html += `<tr>
        <td><strong>${getLangString('introduction', lang)}:<br>${getLangString('minutes', lang)} ${introTime}</strong></td>
        <td><textarea>${aiIntroTeacher}</textarea></td>
        <td><textarea>${aiIntroLearner}</textarea></td>
        <td><textarea>${aiIntroComp}</textarea></td>
    </tr>`;

    // Development
    html += `<tr>
        <td><strong>${getLangString('development', lang)}:<br>${getLangString('minutes', lang)} ${devTime}</strong></td>
        <td><textarea>${aiDevTeacher}</textarea></td>
        <td><textarea>${aiDevLearner}</textarea></td>
        <td><textarea>${aiDevComp}</textarea></td>
    </tr>`;

    // Conclusion
    html += `<tr>
        <td><strong>${getLangString('conclusion', lang)}:<br>${getLangString('minutes', lang)} ${conclTime}</strong></td>
        <td><textarea>${aiConclTeacher}</textarea></td>
        <td><textarea>${aiConclLearner}</textarea></td>
        <td><textarea>${aiConclComp}</textarea></td>
    </tr>`;

    // Self-evaluation (span all columns)
    html += `<tr>
        <td colspan="4"><strong>${getLangString('selfEvaluation', lang)}</strong><br><textarea>${aiSelfEval}</textarea></td>
    </tr>`;

    html += '</table>';

    return html;
}

// Language strings 
function getLangString(key, lang) {
    const strings = {
        English: {
            header: 'LESSON PLAN',
            school: 'School Name',
            teacher: "Teacher’s Name",
            term: 'Term',
            date: 'Date',
            subject: 'Subject',
            class: 'Class',
            unitNo: 'Unit No.',
            lessonNo: 'Lesson No.',
            duration: 'Duration',
            classSize: 'Class Size',
            specialNeeds: 'Type of Special Educational Needs to be catered for in this lesson and number of learners in each category',
            unitTitle: 'Unit Title',
            keyCompetence: 'Key Unit Competence',
            lessonTitle: 'Title of the Lesson',
            instructionalObjective: 'Instructional Objective of the lesson',
            location: 'Location of the lesson',
            materials: 'Teaching materials',
            references: 'References',
            steps: 'Steps of the lesson and duration / Teacher activities / Learner activities / Generic competences and cross-cutting themes + some explanations',
            timing: 'Steps and duration',
            teacherActivities: 'Teacher activities',
            learnerActivities: 'Learner activities',
            competences: 'Generic competences and cross-cutting themes + some explanations',
            introduction: 'Introduction',
            development: 'Lesson development',
            conclusion: 'Conclusion - Summary - Evaluation',
            selfEvaluation: 'Self evaluation',
            minutes: 'minutes'
        },
        French: {
            header: 'FICHE DE LEÇON',
            school: 'Nom de l’école',
            teacher: 'Nom de l’enseignant',
            term: 'Trimestre',
            date: 'Date',
            subject: 'Branche',
            class: 'Classe',
            unitNo: 'Unité',
            lessonNo: 'Leçon',
            duration: 'Durée',
            classSize: 'Nombre d’apprenants',
            specialNeeds: 'Types de besoins particuliers et nombre d’apprenants concernés',
            unitTitle: 'Titre de l’unité',
            keyCompetence: 'Compétence clé',
            lessonTitle: 'Titre de la leçon',
            instructionalObjective: 'Objectif Opérationnel de la leçon',
            location: 'Lieu de la leçon',
            materials: 'Matériel didactique',
            references: 'Références',
            steps: 'Etapes de la leçon et durée / Activités de l’enseignant / Activités des apprenants / Compétences génériques et thèmes transversaux + quelques explications',
            timing: 'Etapes et durée',
            teacherActivities: 'Activités de l’enseignant',
            learnerActivities: 'Activités des apprenants',
            competences: 'Compétences génériques et thèmes transversaux + quelques explications',
            introduction: 'Introduction',
            development: 'Développement de la leçon',
            conclusion: 'Conclusion : -Synthèse -Évaluation',
            selfEvaluation: 'Auto évaluation',
            minutes: 'minutes'
        },
        Kinyarwanda: {
            header: 'IMBATA Y’ISOMO',
            school: 'Izina ry’ishuri',
            teacher: 'Amazina y’umwarimu',
            term: 'Igihembwe',
            date: 'Itariki',
            subject: 'Inyigisho',
            class: 'Umwaka wa',
            unitNo: 'Umutwe wa',
            lessonNo: 'Isomo rya',
            duration: 'Igihe isomo rimara',
            classSize: 'Umubare w’abanyeshuri',
            specialNeeds: 'Abafite ibyo bagenerwa byihariye mu myigire no mu myigishirize n’umubare wabo',
            unitTitle: 'Umutwe',
            keyCompetence: 'Ubushobozi bw’ingenzi bugamijwe',
            lessonTitle: 'Isomo',
            instructionalObjective: 'Intego ngenamukoro',
            location: 'Imiterere y’aho isomo ribera',
            materials: 'Imfashanyigisho',
            references: 'Imyandiko n’ibitabo byifashishijwe',
            steps: 'Ibice by’isomo + igihe / Ibikorwa by’umwarimu / Ibikorwa by’umunyeshuri / Ubushobozi n’ingingo nsanganyamasomo (andika ubushobozi + igisobanuro kigufi kigaragaza uko buzagerwaho)',
            timing: 'Ibice by’isomo + igihe',
            teacherActivities: 'Ibikorwa by’umwarimu',
            learnerActivities: 'Ibikorwa by’umunyeshuri',
            competences: 'Ubushobozi n’ingingo nsanganyamasomo (andika ubushobozi + igisobanuro kigufi kigaragaza uko buzagerwaho)',
            introduction: 'Intangiriro',
            development: 'Isomo nyirizina',
            conclusion: 'Umusozo w’isomo : -Ikomatanya -Isuzuma',
            selfEvaluation: 'Kwisuzuma (umurezi)',
            minutes: 'Iminota'
        },
        Swahili: {
            header: 'ANDALIO LA SOMO',
            school: 'Jina la shule',
            teacher: 'Jina la mwalimu',
            term: 'Muhula',
            date: 'Tarehe',
            subject: 'Somo',
            class: 'Darasa',
            unitNo: 'Sehemu',
            lessonNo: 'Somo namba',
            duration: 'Muda',
            classSize: 'Idadi ya wanafunzi',
            specialNeeds: 'Aina ya mahitaji maalum na idadi ya wanafunzi',
            unitTitle: 'Kichwa cha sehemu',
            keyCompetence: 'Uwezo muhimu wa sehemu',
            lessonTitle: 'Kichwa cha somo',
            instructionalObjective: 'Malengo ya kiufundi',
            location: 'Mahali pa somo',
            materials: 'Vifaa vya kufundishia',
            references: 'Marejeo',
            steps: 'Hatua na muda / Shughuli za mwalimu / Shughuli za mwanafunzi / Uwezo wa jumla na mada zinazovuka + maelezo mafupi',
            timing: 'Hatua na muda',
            teacherActivities: 'Shughuli za mwalimu',
            learnerActivities: 'Shughuli za mwanafunzi',
            competences: 'Uwezo wa jumla na mada zinazovuka + maelezo mafupi',
            introduction: 'Utangulizi',
            development: 'Maendeleo ya somo',
            conclusion: 'Hitimisho: -Muhtasari -Tathmini',
            selfEvaluation: 'Tathmini ya mwalimu',
            minutes: 'dakika'
        }
    };
    return strings[lang][key] || key;
}

// AI Generation Functions (simplified, language-aware placeholders)
function generateObjectives(title, subject, lang) {
    if (lang === 'Kinyarwanda') {
        return 'Abanyeshuri bagomba gukora:<br>1. Gusobanura ibice by’ingenzi bya "' + title + '" mu ' + subject + '.<br>2. Gukoresha ubumenyi mu bikorwa.<br>3. Kugirana ibiganiro ku kamaro ka byo.';
    }
    return By the end of the lesson, students will:<br>1. Explain key concepts related to ${title} in ${subject}.<br>2. Apply these concepts through practical examples.<br>3. Collaborate to discuss real-world implications.;
}

function generateMaterials(subject, lang) {
    if (lang === 'Kinyarwanda') {
        return 'Igitabo cy’inyigisho, Imbonerahamwe, Ibikoresho bifitanye isano na ' + subject + '.';
    }
    const common = 'Whiteboard and markers, projector (if available), student worksheets';
    return common + ', subject-specific tools for ' + subject + '.';
}

function generateReferences(subject, classLevel, lang) {
    return lang === 'Kinyarwanda' ? 'Ibikoresho by’inyigisho bya ' + subject + ' mu ' + classLevel + ', Ibitabo by’ubumenyi.' : ${subject} textbook for ${classLevel}, Practical Manual, Online resources.;
}

function generateAISection(section, subject, title, time, lang) {
    let teacher, learner, competences;
    if (lang === 'Kinyarwanda') {
        if (section === 'introduction') {
            teacher = '1. Umwarimu atanga ibibazo bishingiye ku isomo riheruka.<br>2. Abarinda ibiganiro.<br>3. Atangaza intego y’isomo (min ' + time + ').';
            learner = '1. Abanyeshuri basubiza ibibazo.<br>2. Bagakorana ibiganiro.<br>3. Bita ku ntego z’isomo.';
        } else if (section === 'development') {
            teacher = '1. Umwarimu yerekana ibice by’ingenzi bya ' + title + '.<br>2. Abafasha mu gukora imikino/imyitozo.<br>3. Asuzuma ibikorwa byabo (min ' + time + ').';
            learner = '1. Abanyeshuri bagakurikirana ibisobanuro.<br>2. Bagakora imyitozo mu matsinda.<br>3. Bagatanga ibisubizo.';
        } else { // conclusion
            teacher = '1. Umwarimu akomatanya ibyigishijwe.<br>2. Atanga isuzuma ryihuse.<br>3. Atanga umukoro (min ' + time + ').';
            learner = '1. Abanyeshuri bafata inyigisho.<br>2. Basubiza ibibazo by’isuzuma.<br>3. Bandika umukoro.';
        }
        competences = '- Ubushobozi bw’ingenzi: Kwigira, Kwishakira ibisubizo no Gukorana n’abandi.';
    } else {
        if (section === 'introduction') {
            teacher = 1. Teacher reviews prior knowledge.<br>2. Introduces the topic: ${title}.<br>3. Clearly states the lesson objectives (approx ${time} min).;
            learner = '1. Students respond to review questions.<br>2. Listen attentively and ask clarifying questions.';
        } else if (section === 'development') {
            teacher = 1. Facilitates group work/hands-on activity on ${title}.<br>2. Monitors student progress and provides guidance.<br>3. Leads a plenary discussion (approx ${time} min).;
            learner = '1. Students perform tasks in small groups.<br>2. Discuss findings and prepare a short presentation.<br>3. Present their work to the class.';
        } else { // conclusion
            teacher = 1. Summarizes the key learning points.<br>2. Provides a quick formative assessment (e.g., exit ticket).<br>3. Assigns homework (approx ${time} min).;
            learner = '1. Students participate in the summary.<br>2. Complete the assessment task.<br>3. Note down the homework assignment.';
        }
        competences = - Generic Competence: Critical thinking, Communication, and Cooperation in ${subject}.;
    }
    return { teacher, learner, competences };
}

function generateSelfEvaluation(title, duration, lang) {
    if (lang === 'Kinyarwanda') {
        return 'Isomo ku "' + title + '" ryagenze neza, abanyeshuri bose bitabiriye. Igihe cyagenwe (' + duration + ' Iminota) cyari gihagije. Imbaraga: Ibikorwa byo gukorana. Ibigomba kunozwa: Gukoresha imfashanyigisho zinyuranye. Umusaruro: Mwiza.';
    }
    return Lesson on ${title} was engaging; students participated actively. Timing (${duration} min) was appropriate. Strengths: Interactive activities and clear objectives. Areas for Improvement: Need more diverse teaching aids. Effectiveness: High.;
}

// Download Functions (advanced, multi-page PDF/HTML)
function downloadPDF() {
    const data = {
        language: document.getElementById('language').value,
    };
    const element = document.getElementById('lessonPlanContent');
    // Clone and prepare for print (replace textareas with divs for better rendering)
    const tempElement = element.cloneNode(true);
    const textareas = tempElement.querySelectorAll('textarea');
    textareas.forEach(ta => {
        const div = document.createElement('div');
        div.innerHTML = ta.value.replace(/\n/g, '<br>');
        div.style.padding = '8px';
        div.style.minHeight = '60px';
        div.style.border = '1px solid #ddd';
        div.style.background = 'white';
        div.style.fontSize = '12px';
        ta.parentNode.replaceChild(div, ta);
    });

    const tempDiv = document.createElement('div');
    tempDiv.style.position = 'absolute';
    tempDiv.style.left = '-9999px';
    tempDiv.appendChild(tempElement);
    document.body.appendChild(tempDiv);

    html2canvas(tempDiv, { scale: 2, useCORS: true }).then((canvas) => {
        const { jsPDF } = window.jspdf;
        const doc = new jsPDF('p', 'mm', 'a4');
        const imgData = canvas.toDataURL('image/png');
        const pdfWidth = doc.internal.pageSize.getWidth();
        const pdfHeight = doc.internal.pageSize.getHeight();
        const imgWidth = pdfWidth;
        const imgHeight = (canvas.height * imgWidth) / canvas.width;
        let heightLeft = imgHeight;
        let position = 0;

        doc.addImage(imgData, 'PNG', 0, position, imgWidth, imgHeight);
        heightLeft -= pdfHeight;

        while (heightLeft >= 0) {
            position = heightLeft - imgHeight;
            doc.addPage();
            doc.addImage(imgData, 'PNG', 0, position, imgWidth, imgHeight);
            heightLeft -= pdfHeight;
        }

        doc.save(lesson-plan-${data.language.toLowerCase()}-${new Date().toISOString().split('T')[0]}.pdf);
        document.body.removeChild(tempDiv);
    }).catch((error) => {
        console.error('PDF generation error:', error);
        alert('PDF generation failed. Try printing the page instead.');
    });
}

function downloadHTML() {
    const data = {
        language: document.getElementById('language').value,
    };
    const element = document.getElementById('lessonPlanContent');
    const htmlContent = `
        <!DOCTYPE html>
        <html lang="${data.language.toLowerCase()}">
        <head>
            <meta charset="UTF-8">
            <title>Editable ${data.language} Lesson Plan</title>
            <style>
                body { font-family: Arial, sans-serif; margin: 20px; font-size: 12px; }
                table { border-collapse: collapse; width: 100%; margin-bottom: 10px; }
                th, td { border: 1px solid #ddd; padding: 8px; vertical-align: top; }
                th { background-color: #f2f2f2; font-weight: bold; }
                textarea { width: 100%; height: 80px; border: 1px solid #ccc; resize: vertical; font-size: 12px; font-family: inherit; }
                h3 { text-align: center; }
            </style>
        </head>
        <body>${element.innerHTML}</body>
        </html>`;
    const blob = new Blob([htmlContent], { type: 'text/html' });
    const url = URL.createObjectURL(blob);
    const a = document.createElement('a');
    a.href = url;
    a.download = lesson-plan-${data.language.toLowerCase()}.html;
    a.click();
    URL.revokeObjectURL(url);
}

/**
 * Downloads the lesson plan content as a Word Document (.doc) by wrapping
 * the content in MSO-compatible HTML, ensuring the tables render correctly and the file is editable.
 */
function downloadDOCX() {
    const data = {
        language: document.getElementById('language').value,
        lessonTitle: document.getElementById('lessonTitle').value || 'Lesson Plan'
    };
    const filename = lesson-plan-${data.language.toLowerCase().replace(/[^a-z0-9]/g, '-')}.doc;
    const element = document.getElementById('lessonPlanContent');
    
    // 1. Clone and replace textareas with styled divs for Word readability
    const tempElement = element.cloneNode(true);
    const textareas = tempElement.querySelectorAll('textarea');
    textareas.forEach(ta => {
        const div = document.createElement('div');
        div.innerHTML = ta.value.replace(/\n/g, '<br>');
        // Minimal inline styling to preserve basic look in Word
        div.style.padding = '6px';
        div.style.minHeight = '50px';
        div.style.border = '1px solid #000'; // Thicker border for visibility
        div.style.background = 'white';
        div.style.fontSize = '11pt';
        div.style.margin = '0'; // Remove default margin
        ta.parentNode.replaceChild(div, ta);
    });

    const content = tempElement.innerHTML;

    // 2. DOCX/Word HTML Header with MSO style tags for better formatting in Word
    const htmlContent = `
        <html xmlns:o='urn:schemas-microsoft-com:office:office' xmlns:w='urn:schemas-microsoft-com:office:word' xmlns='http://www.w3.org/TR/REC-html40'>
        <head>
            <meta charset="utf-8">
            <title>${data.lessonTitle} Lesson Plan</title>
            <style>
                /* Apply styles optimized for Word */
                body { font-family: 'Times New Roman', Times, serif; margin: 25px; font-size: 11pt; }
                .lesson-table { 
                    border-collapse: collapse; 
                    width: 100%; 
                    margin-bottom: 15px; 
                }
                .lesson-table th, .lesson-table td { 
                    border: 1pt solid #000; 
                    padding: 8px; 
                    vertical-align: top; 
                    font-size: 11pt; 
                    line-height: 1.5;
                }
                .lesson-table th { 
                    background-color: #d9d9d9; 
                    font-weight: bold; 
                }
                h3 { 
                    text-align: center; 
                    color: #005fa3; 
                    font-size: 14pt;
                }
                /* Ensure replaced divs have borders in Word */
                .full-row div {
                    border: 1pt solid #000 !important;
                    padding: 6px;
                    background: white;
                    min-height: 50px;
                }
            </style>
        </head>
        <body>
            ${content}
        </body>
        </html>`;

    // 3. Create and download the file
    const blob = new Blob([htmlContent], { type: 'application/msword;charset=utf-8' });
    const url = URL.createObjectURL(blob);
    const a = document.createElement('a');
    a.href = url;
    a.download = filename;
    document.body.appendChild(a);
    a.click();
    document.body.removeChild(a);
    URL.revokeObjectURL(url);
}


// --- Initialization ---
function init(){
  saveData();
  
  // Set default login for admin
  document.getElementById('username').value = 'admin';
  document.getElementById('password').value = '1234';
}

document.addEventListener('DOMContentLoaded', init);
</script>
</body>
</html>
