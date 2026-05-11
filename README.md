<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Engineering College Administration Management System</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <!-- Login Page -->
    <div id="loginPage" class="page active">
        <div class="container">
            <div class="login-box">
                <h1>College Administration System</h1>
                <p class="subtitle">Welcome to Engineering College</p>
                
                <form id="loginForm">
                    <div class="form-group">
                        <label for="loginInput">Name / Email / Phone Number</label>
                        <input type="text" id="loginInput" placeholder="Enter name, email, or phone number" required>
                    </div>

                    <div class="form-group">
                        <label for="password">Password</label>
                        <input type="password" id="password" placeholder="Enter your password" required>
                    </div>

                    <!-- OTP Section (shown only when phone is entered) -->
                    <div id="otpSection" class="form-group hidden">
                        <label for="otp">OTP</label>
                        <input type="text" id="otp" placeholder="Enter OTP sent to your phone" maxlength="6">
                        <button type="button" class="btn-secondary" id="sendOtpBtn">Send OTP</button>
                    </div>

                    <button type="submit" class="btn-primary">Login</button>
                </form>

                <p class="signup-link">Don't have an account? <a href="#" onclick="showPage('signupPage')">Sign Up</a></p>
            </div>
        </div>
    </div>

    <!-- Signup Page -->
    <div id="signupPage" class="page">
        <div class="container">
            <div class="login-box">
                <h1>Create Account</h1>
                <p class="subtitle">Register with Engineering College</p>
                
                <form id="signupForm">
                    <div class="form-group">
                        <label for="signupName">Full Name</label>
                        <input type="text" id="signupName" placeholder="Enter your full name" required>
                    </div>

                    <div class="form-group">
                        <label for="signupEmail">Email</label>
                        <input type="email" id="signupEmail" placeholder="Enter your email" required>
                    </div>

                    <div class="form-group">
                        <label for="signupPhone">Phone Number</label>
                        <input type="tel" id="signupPhone" placeholder="Enter your phone number" required>
                    </div>

                    <div class="form-group">
                        <label for="signupPassword">Password</label>
                        <input type="password" id="signupPassword" placeholder="Create a password" required>
                    </div>

                    <button type="submit" class="btn-primary">Sign Up</button>
                </form>

                <p class="signup-link">Already have an account? <a href="#" onclick="showPage('loginPage')">Login</a></p>
            </div>
        </div>
    </div>

    <!-- Department Selection Page -->
    <div id="departmentPage" class="page">
        <div class="container">
            <div class="header-section">
                <h1>Select Your Department</h1>
                <button class="btn-logout" onclick="logout()">Logout</button>
            </div>

            <div class="departments-grid">
                <div class="dept-card" onclick="selectDepartment('CSE')">
                    <h3>Computer Science & Engineering</h3>
                    <p>CSE</p>
                </div>
                <div class="dept-card" onclick="selectDepartment('ECE')">
                    <h3>Electronics & Communication</h3>
                    <p>ECE</p>
                </div>
                <div class="dept-card" onclick="selectDepartment('MECH')">
                    <h3>Mechanical Engineering</h3>
                    <p>MECH</p>
                </div>
                <div class="dept-card" onclick="selectDepartment('CIVIL')">
                    <h3>Civil Engineering</h3>
                    <p>CIVIL</p>
                </div>
                <div class="dept-card" onclick="selectDepartment('EEE')">
                    <h3>Electrical & Electronics</h3>
                    <p>EEE</p>
                </div>
                <div class="dept-card" onclick="selectDepartment('AERO')">
                    <h3>Aerospace Engineering</h3>
                    <p>AERO</p>
                </div>
            </div>
        </div>
    </div>

    <!-- Course Selection Page -->
    <div id="coursePage" class="page">
        <div class="container">
            <div class="header-section">
                <h1>Select Your Course</h1>
                <p class="department-info" id="deptInfo"></p>
                <button class="btn-logout" onclick="showPage('departmentPage')">Back to Departments</button>
            </div>

            <div class="courses-grid">
                <div class="course-card" onclick="selectCourse('B.Tech 4-Year')">
                    <h3>B.Tech (4-Year Program)</h3>
                    <p>Full-time engineering degree</p>
                </div>
                <div class="course-card" onclick="selectCourse('Diploma 3-Year')">
                    <h3>Diploma (3-Year Program)</h3>
                    <p>Part-time engineering course</p>
                </div>
                <div class="course-card" onclick="selectCourse('Advanced Certification')">
                    <h3>Advanced Certification</h3>
                    <p>Specialized technical courses</p>
                </div>
                <div class="course-card" onclick="selectCourse('Research Program')">
                    <h3>Research Program</h3>
                    <p>M.Tech and PhD opportunities</p>
                </div>
            </div>
        </div>
    </div>

    <!-- Fee Structure & Pre-booking Page -->
    <div id="feeStructurePage" class="page">
        <div class="container">
            <div class="header-section">
                <h1>Fee Structure & Pre-booking</h1>
                <p class="course-info" id="courseInfo"></p>
                <button class="btn-logout" onclick="showPage('coursePage')">Back to Courses</button>
            </div>

            <div class="fee-section">
                <h2>Course Fee Structure</h2>
                <table class="fee-table">
                    <tr>
                        <th>Year</th>
                        <th>Tuition Fee</th>
                        <th>Hostel Fee</th>
                        <th>Lab Fee</th>
                        <th>Total</th>
                    </tr>
                    <tr>
                        <td>Year 1</td>
                        <td>₹150,000</td>
                        <td>₹60,000</td>
                        <td>₹20,000</td>
                        <td>₹230,000</td>
                    </tr>
                    <tr>
                        <td>Year 2</td>
                        <td>₹150,000</td>
                        <td>₹60,000</td>
                        <td>₹25,000</td>
                        <td>₹235,000</td>
                    </tr>
                    <tr>
                        <td>Year 3</td>
                        <td>₹160,000</td>
                        <td>₹60,000</td>
                        <td>₹30,000</td>
                        <td>₹250,000</td>
                    </tr>
                    <tr>
                        <td>Year 4</td>
                        <td>₹160,000</td>
                        <td>₹60,000</td>
                        <td>₹30,000</td>
                        <td>₹250,000</td>
                    </tr>
                </table>
            </div>

            <div class="marks-section">
                <h2>Academic Qualification Details</h2>
                <form id="qualificationForm">
                    <div class="form-row">
                        <div class="form-group">
                            <label for="tenthMarks">10th Class Marks (out of 100)</label>
                            <input type="number" id="tenthMarks" min="0" max="100" placeholder="Enter marks" required>
                        </div>
                        <div class="form-group">
                            <label for="twelfthMarks">12th Class Marks (out of 100)</label>
                            <input type="number" id="twelfthMarks" min="0" max="100" placeholder="Enter marks" required>
                        </div>
                    </div>

                    <div class="form-row">
                        <div class="form-group">
                            <label for="keamRank">KEAM Rank (if applicable)</label>
                            <input type="number" id="keamRank" placeholder="Enter KEAM rank" min="1">
                        </div>
                        <div class="form-group">
                            <label for="jeeRank">JEE Rank (if applicable)</label>
                            <input type="number" id="jeeRank" placeholder="Enter JEE rank" min="1">
                        </div>
                    </div>

                    <button type="button" class="btn-primary" onclick="saveQualifications()">Save Qualifications</button>
                </form>
            </div>

            <div class="prebooking-section">
                <h2>Pre-book Your Course</h2>
                <div class="prebooking-form">
                    <div class="form-group">
                        <label for="startDate">Preferred Start Date</label>
                        <input type="date" id="startDate" required>
                    </div>
                    <div class="form-group">
                        <label for="batch">Select Batch</label>
                        <select id="batch" required>
                            <option value="">Choose a batch</option>
                            <option value="Morning (8 AM - 12 PM)">Morning (8 AM - 12 PM)</option>
                            <option value="Afternoon (2 PM - 6 PM)">Afternoon (2 PM - 6 PM)</option>
                            <option value="Weekend">Weekend</option>
                        </select>
                    </div>
                    <button type="button" class="btn-primary" onclick="prebookCourse()">Pre-book Course</button>
                </div>
            </div>

            <button class="btn-next" onclick="showPage('facultyPage')">Next: Faculty Details →</button>
        </div>
    </div>

    <!-- Faculty Details Page -->
    <div id="facultyPage" class="page">
        <div class="container">
            <div class="header-section">
                <h1>Faculty Members</h1>
                <button class="btn-logout" onclick="showPage('feeStructurePage')">Back</button>
            </div>

            <div class="search-section">
                <input type="text" id="facultySearch" placeholder="Search faculty by name or specialization..." onkeyup="searchFaculty()">
            </div>

            <div class="faculty-grid" id="facultyGrid">
                <!-- Faculty cards will be dynamically generated -->
            </div>

            <button class="btn-next" onclick="showPage('hostelPage')">Next: Hostel Booking →</button>
        </div>
    </div>

    <!-- Hostel Room Booking Page -->
    <div id="hostelPage" class="page">
        <div class="container">
            <div class="header-section">
                <h1>Hostel Room Booking</h1>
                <button class="btn-logout" onclick="showPage('facultyPage')">Back</button>
            </div>

            <div class="hostel-booking">
                <div class="room-selection">
                    <h2>Select Your Room</h2>
                    <div class="rooms-grid" id="roomsGrid">
                        <!-- Rooms will be dynamically generated -->
                    </div>
                </div>

                <div class="booking-details">
                    <h2>Booking Summary</h2>
                    <div id="bookingSummary" class="summary-box">
                        <p>Select a room to see details</p>
                    </div>

                    <div class="payment-section">
                        <h3>Advance Payment</h3>
                        <div class="form-group">
                            <label for="advanceAmount">Advance Amount (%)</label>
                            <select id="advanceAmount" required>
                                <option value="">Select advance payment</option>
                                <option value="25">25% - ₹15,000</option>
                                <option value="50">50% - ₹30,000</option>
                                <option value="100">100% - ₹60,000</option>
                            </select>
                        </div>
                        <button type="button" class="btn-primary" onclick="processPayment()">Proceed to Payment</button>
                    </div>
                </div>
            </div>

            <button class="btn-next" onclick="showPage('exitPage')">Next: Confirm & Exit →</button>
        </div>
    </div>

    <!-- Exit/Confirmation Page -->
    <div id="exitPage" class="page">
        <div class="container">
            <div class="exit-container">
                <h1>Application Summary</h1>
                
                <div class="summary-section">
                    <h2>Your Selected Options:</h2>
                    <div id="finalSummary" class="summary-details">
                        <!-- Summary will be populated here -->
                    </div>
                </div>

                <div class="action-buttons">
                    <button class="btn-primary" onclick="confirmApplication()">Confirm & Submit Application</button>
                    <button class="btn-secondary" onclick="downloadPDF()">Download as PDF</button>
                    <button class="btn-logout" onclick="logout()">Logout</button>
                </div>
            </div>
        </div>
    </div>

    <script src="script.js"></script>
</body>
</html>



* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

:root {
    --primary-color: #2c3e50;
    --secondary-color: #3498db;
    --accent-color: #e74c3c;
    --success-color: #27ae60;
    --light-bg: #ecf0f1;
    --white: #ffffff;
    --dark-text: #2c3e50;
    --border-radius: 8px;
    --shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    --transition: all 0.3s ease;
}

body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    color: var(--dark-text);
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 20px;
}

.container {
    width: 100%;
    max-width: 1200px;
}

/* Page System */
.page {
    display: none;
    animation: fadeIn 0.5s ease;
}

.page.active {
    display: block;
}

@keyframes fadeIn {
    from {
        opacity: 0;
        transform: translateY(20px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

.hidden {
    display: none !important;
}

/* Login Box */
.login-box {
    background: var(--white);
    padding: 40px;
    border-radius: var(--border-radius);
    box-shadow: var(--shadow);
    max-width: 450px;
    margin: 0 auto;
    text-align: center;
}

.login-box h1 {
    color: var(--primary-color);
    margin-bottom: 10px;
    font-size: 28px;
}

.subtitle {
    color: #7f8c8d;
    margin-bottom: 30px;
    font-size: 14px;
}

/* Forms */
.form-group {
    margin-bottom: 20px;
    text-align: left;
}

.form-group label {
    display: block;
    margin-bottom: 8px;
    font-weight: 600;
    color: var(--primary-color);
    font-size: 14px;
}

.form-group input,
.form-group select {
    width: 100%;
    padding: 12px;
    border: 2px solid var(--light-bg);
    border-radius: var(--border-radius);
    font-size: 14px;
    transition: var(--transition);
    font-family: inherit;
}

.form-group input:focus,
.form-group select:focus {
    outline: none;
    border-color: var(--secondary-color);
    box-shadow: 0 0 0 3px rgba(52, 152, 219, 0.1);
}

.form-row {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 20px;
    margin-bottom: 20px;
}

@media (max-width: 768px) {
    .form-row {
        grid-template-columns: 1fr;
    }
}

/* Buttons */
.btn-primary {
    width: 100%;
    padding: 12px;
    background: var(--secondary-color);
    color: var(--white);
    border: none;
    border-radius: var(--border-radius);
    font-size: 16px;
    font-weight: 600;
    cursor: pointer;
    transition: var(--transition);
    margin-top: 10px;
}

.btn-primary:hover {
    background: #2980b9;
    transform: translateY(-2px);
    box-shadow: 0 6px 12px rgba(52, 152, 219, 0.3);
}

.btn-secondary {
    padding: 8px 16px;
    background: var(--light-bg);
    color: var(--primary-color);
    border: 2px solid var(--secondary-color);
    border-radius: var(--border-radius);
    font-size: 14px;
    cursor: pointer;
    transition: var(--transition);
    margin-top: 10px;
}

.btn-secondary:hover {
    background: var(--secondary-color);
    color: var(--white);
}

.btn-logout {
    padding: 10px 20px;
    background: var(--accent-color);
    color: var(--white);
    border: none;
    border-radius: var(--border-radius);
    cursor: pointer;
    transition: var(--transition);
    font-weight: 600;
}

.btn-logout:hover {
    background: #c0392b;
    transform: translateY(-2px);
}

.btn-next {
    width: 100%;
    padding: 12px;
    background: var(--success-color);
    color: var(--white);
    border: none;
    border-radius: var(--border-radius);
    font-size: 16px;
    font-weight: 600;
    cursor: pointer;
    transition: var(--transition);
    margin-top: 30px;
}

.btn-next:hover {
    background: #229954;
    transform: translateY(-2px);
}

/* Links */
.signup-link {
    margin-top: 20px;
    color: #7f8c8d;
    font-size: 14px;
}

.signup-link a {
    color: var(--secondary-color);
    text-decoration: none;
    font-weight: 600;
    cursor: pointer;
}

.signup-link a:hover {
    text-decoration: underline;
}

/* Header Section */
.header-section {
    background: var(--white);
    padding: 20px;
    border-radius: var(--border-radius);
    margin-bottom: 30px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    box-shadow: var(--shadow);
}

.header-section h1 {
    color: var(--primary-color);
    margin: 0;
}

.department-info,
.course-info {
    font-size: 14px;
    color: #7f8c8d;
    margin-bottom: 10px;
}

/* Grid Layouts */
.departments-grid,
.courses-grid,
.faculty-grid,
.rooms-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 20px;
    margin-bottom: 30px;
}

/* Department Cards */
.dept-card,
.course-card {
    background: var(--white);
    padding: 30px;
    border-radius: var(--border-radius);
    cursor: pointer;
    transition: var(--transition);
    box-shadow: var(--shadow);
    text-align: center;
    border-left: 4px solid var(--secondary-color);
}

.dept-card:hover,
.course-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 8px 15px rgba(52, 152, 219, 0.3);
    background: #f8f9fa;
}

.dept-card h3,
.course-card h3 {
    color: var(--primary-color);
    margin-bottom: 10px;
}

.dept-card p,
.course-card p {
    color: #7f8c8d;
    font-size: 14px;
}

/* Faculty Cards */
.faculty-card {
    background: var(--white);
    padding: 20px;
    border-radius: var(--border-radius);
    box-shadow: var(--shadow);
    transition: var(--transition);
}

.faculty-card:hover {
    transform: translateY(-3px);
    box-shadow: 0 8px 15px rgba(0, 0, 0, 0.15);
}

.faculty-avatar {
    width: 80px;
    height: 80px;
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    border-radius: 50%;
    margin: 0 auto 15px;
    display: flex;
    align-items: center;
    justify-content: center;
    color: var(--white);
    font-size: 32px;
    font-weight: bold;
}

.faculty-name {
    font-weight: 600;
    color: var(--primary-color);
    margin-bottom: 5px;
}

.faculty-specialization {
    color: var(--secondary-color);
    font-size: 12px;
    margin-bottom: 10px;
}

.faculty-contact {
    color: #7f8c8d;
    font-size: 13px;
    line-height: 1.6;
}

/* Fee Table */
.fee-table {
    width: 100%;
    border-collapse: collapse;
    background: var(--white);
    border-radius: var(--border-radius);
    overflow: hidden;
    box-shadow: var(--shadow);
    margin-bottom: 30px;
}

.fee-table th,
.fee-table td {
    padding: 15px;
    text-align: left;
    border-bottom: 1px solid var(--light-bg);
}

.fee-table th {
    background: var(--primary-color);
    color: var(--white);
    font-weight: 600;
}

.fee-table tr:hover {
    background: #f8f9fa;
}

/* Sections */
.fee-section,
.marks-section,
.prebooking-section {
    background: var(--white);
    padding: 25px;
    border-radius: var(--border-radius);
    margin-bottom: 25px;
    box-shadow: var(--shadow);
}

.fee-section h2,
.marks-section h2,
.prebooking-section h2 {
    color: var(--primary-color);
    margin-bottom: 20px;
    font-size: 20px;
    border-bottom: 2px solid var(--secondary-color);
    padding-bottom: 10px;
}

/* Search Section */
.search-section {
    margin-bottom: 30px;
}

.search-section input {
    width: 100%;
    padding: 15px;
    border: 2px solid var(--light-bg);
    border-radius: var(--border-radius);
    font-size: 16px;
    background: var(--white);
    transition: var(--transition);
}

.search-section input:focus {
    outline: none;
    border-color: var(--secondary-color);
}

/* Room Selection */
.room-card {
    background: var(--white);
    padding: 20px;
    border-radius: var(--border-radius);
    border: 2px solid var(--light-bg);
    cursor: pointer;
    transition: var(--transition);
    text-align: center;
}

.room-card:hover {
    border-color: var(--secondary-color);
    box-shadow: 0 6px 12px rgba(52, 152, 219, 0.2);
}

.room-card.selected {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    color: var(--white);
    border-color: #667eea;
}

.room-type {
    font-weight: 600;
    margin-bottom: 8px;
}

.room-price {
    color: var(--secondary-color);
    font-size: 18px;
    font-weight: bold;
}

.room-card.selected .room-price {
    color: var(--white);
}

/* Hostel Booking */
.hostel-booking {
    display: grid;
    grid-template-columns: 2fr 1fr;
    gap: 30px;
    margin-bottom: 30px;
}

@media (max-width: 768px) {
    .hostel-booking {
        grid-template-columns: 1fr;
    }
}

.room-selection,
.booking-details {
    background: var(--white);
    padding: 25px;
    border-radius: var(--border-radius);
    box-shadow: var(--shadow);
}

.booking-details h2 {
    color: var(--primary-color);
    margin-bottom: 20px;
    font-size: 18px;
}

.summary-box {
    background: var(--light-bg);
    padding: 15px;
    border-radius: var(--border-radius);
    margin-bottom: 20px;
    color: #7f8c8d;
}

.payment-section {
    background: #f8f9fa;
    padding: 15px;
    border-radius: var(--border-radius);
    margin-top: 20px;
}

/* Exit/Confirmation */
.exit-container {
    background: var(--white);
    padding: 40px;
    border-radius: var(--border-radius);
    box-shadow: var(--shadow);
    max-width: 600px;
    margin: 0 auto;
}

.exit-container h1 {
    color: var(--primary-color);
    text-align: center;
    margin-bottom: 30px;
}

.summary-section {
    background: var(--light-bg);
    padding: 20px;
    border-radius: var(--border-radius);
    margin-bottom: 30px;
}

.summary-section h2 {
    color: var(--primary-color);
    margin-bottom: 15px;
}

.summary-details {
    color: #2c3e50;
    line-height: 1.8;
}

.summary-details p {
    margin-bottom: 10px;
}

.summary-details strong {
    color: var(--secondary-color);
}

.action-buttons {
    display: flex;
    flex-direction: column;
    gap: 12px;
}

.action-buttons .btn-primary {
    margin-top: 0;
}

.action-buttons .btn-secondary,
.action-buttons .btn-logout {
    width: 100%;
    padding: 12px;
    font-size: 16px;
}

/* Responsive */
@media (max-width: 768px) {
    .login-box {
        padding: 25px;
    }

    .header-section {
        flex-direction: column;
        gap: 15px;
        text-align: center;
    }

    .departments-grid,
    .courses-grid,
    .faculty-grid,
    .rooms-grid {
        grid-template-columns: 1fr;
    }

    .exit-container {
        padding: 20px;
    }
}

/* Success Message */
.success-message {
    background: #d4edda;
    color: #155724;
    padding: 15px;
    border-radius: var(--border-radius);
    margin-bottom: 20px;
    border-left: 4px solid var(--success-color);
}

/* Error Message */
.error-message {
    background: #f8d7da;
    color: #721c24;
    padding: 15px;
    border-radius: var(--border-radius);
    margin-bottom: 20px;
    border-left: 4px solid var(--accent-color);
}



// Global Data Structure
let appData = {
    user: {
        name: '',
        email: '',
        phone: '',
        credentials: ''
    },
    department: '',
    course: '',
    qualifications: {
        tenthMarks: null,
        twelfthMarks: null,
        keamRank: null,
        jeeRank: null
    },
    prebooking: {
        startDate: '',
        batch: ''
    },
    hostel: {
        roomType: '',
        roomNumber: '',
        roomPrice: 0,
        advancePayment: 0
    }
};

// Faculty Data
const facultyData = [
    {
        id: 1,
        name: 'Dr. Rajesh Kumar',
        specialization: 'Artificial Intelligence & Machine Learning',
        phone: '+91-9876543210',
        email: 'rajesh.kumar@college.edu',
        office: 'CSE Block - 301',
        avatar: 'RK'
    },
    {
        id: 2,
        name: 'Prof. Priya Sharma',
        specialization: 'Data Structures & Algorithms',
        phone: '+91-9876543211',
        email: 'priya.sharma@college.edu',
        office: 'CSE Block - 302',
        avatar: 'PS'
    },
    {
        id: 3,
        name: 'Dr. Arun Singh',
        specialization: 'Web Development & Cloud Computing',
        phone: '+91-9876543212',
        email: 'arun.singh@college.edu',
        office: 'CSE Block - 303',
        avatar: 'AS'
    },
    {
        id: 4,
        name: 'Prof. Neha Gupta',
        specialization: 'Database Management Systems',
        phone: '+91-9876543213',
        email: 'neha.gupta@college.edu',
        office: 'CSE Block - 304',
        avatar: 'NG'
    },
    {
        id: 5,
        name: 'Dr. Vikram Patel',
        specialization: 'Embedded Systems',
        phone: '+91-9876543214',
        email: 'vikram.patel@college.edu',
        office: 'ECE Block - 301',
        avatar: 'VP'
    },
    {
        id: 6,
        name: 'Prof. Anjali Desai',
        specialization: 'Signal Processing',
        phone: '+91-9876543215',
        email: 'anjali.desai@college.edu',
        office: 'ECE Block - 302',
        avatar: 'AD'
    }
];

// Hostel Rooms Data
const hostelRooms = [
    { type: 'Single AC', number: 'A101', price: 60000, beds: 1, features: ['AC', 'WiFi', 'Attached Bathroom'] },
    { type: 'Double AC', number: 'A102', price: 90000, beds: 2, features: ['AC', 'WiFi', 'Shared Bathroom'] },
    { type: 'Triple Non-AC', number: 'B101', price: 45000, beds: 3, features: ['Fans', 'WiFi', 'Shared Bathroom'] },
    { type: 'Double AC Premium', number: 'A103', price: 120000, beds: 2, features: ['AC', 'WiFi', 'Attached Bathroom', 'Mini Fridge'] },
    { type: 'Single Non-AC', number: 'B102', price: 30000, beds: 1, features: ['Fans', 'WiFi', 'Shared Bathroom'] },
    { type: 'Deluxe Suite', number: 'A104', price: 150000, beds: 2, features: ['AC', 'WiFi', 'Attached Bathroom', 'Kitchen', 'Study Table'] }
];

// Show/Hide Pages
function showPage(pageId) {
    const pages = document.querySelectorAll('.page');
    pages.forEach(page => page.classList.remove('active'));
    document.getElementById(pageId).classList.add('active');
    window.scrollTo(0, 0);
}

// Login Form Handler
document.getElementById('loginForm')?.addEventListener('submit', function(e) {
    e.preventDefault();
    
    const loginInput = document.getElementById('loginInput').value.trim();
    const password = document.getElementById('password').value;
    
    if (!loginInput || !password) {
        alert('Please fill in all fields');
        return;
    }

    // Detect input type
    const emailPattern = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
    const phonePattern = /^\d{10}$/;

    if (phonePattern.test(loginInput)) {
        // Phone number entered - show OTP
        document.getElementById('otpSection').classList.remove('hidden');
        appData.user.phone = loginInput;
        alert('OTP has been sent to your phone');
    } else if (emailPattern.test(loginInput)) {
        appData.user.email = loginInput;
        handleLoginSuccess(loginInput);
    } else {
        appData.user.name = loginInput;
        handleLoginSuccess(loginInput);
    }
});

// Send OTP Handler
document.getElementById('sendOtpBtn')?.addEventListener('click', function() {
    const otp = document.getElementById('otp').value;
    if (!otp || otp.length !== 6) {
        alert('Please enter a valid 6-digit OTP');
        return;
    }
    handleLoginSuccess(appData.user.phone);
});

// Handle Login Success
function handleLoginSuccess(credentials) {
    appData.user.credentials = credentials;
    document.getElementById('loginForm').reset();
    showPage('departmentPage');
}

// Signup Form Handler
document.getElementById('signupForm')?.addEventListener('submit', function(e) {
    e.preventDefault();
    
    const name = document.getElementById('signupName').value;
    const email = document.getElementById('signupEmail').value;
    const phone = document.getElementById('signupPhone').value;
    const password = document.getElementById('signupPassword').value;

    if (!name || !email || !phone || !password) {
        alert('Please fill in all fields');
        return;
    }

    appData.user.name = name;
    appData.user.email = email;
    appData.user.phone = phone;

    alert('Account created successfully! Please login.');
    document.getElementById('signupForm').reset();
    showPage('loginPage');
});

// Department Selection
function selectDepartment(dept) {
    appData.department = dept;
    document.getElementById('deptInfo').textContent = `Selected Department: ${dept}`;
    showPage('coursePage');
}

// Course Selection
function selectCourse(course) {
    appData.course = course;
    document.getElementById('courseInfo').textContent = `Department: ${appData.department} | Course: ${course}`;
    showPage('feeStructurePage');
}

// Save Qualifications
function saveQualifications() {
    const tenthMarks = document.getElementById('tenthMarks').value;
    const twelfthMarks = document.getElementById('twelfthMarks').value;
    const keamRank = document.getElementById('keamRank').value;
    const jeeRank = document.getElementById('jeeRank').value;

    if (!tenthMarks || !twelfthMarks) {
        alert('Please enter 10th and 12th marks');
        return;
    }

    appData.qualifications = {
        tenthMarks: parseFloat(tenthMarks),
        twelfthMarks: parseFloat(twelfthMarks),
        keamRank: keamRank ? parseInt(keamRank) : null,
        jeeRank: jeeRank ? parseInt(jeeRank) : null
    };

    alert('Qualifications saved successfully!');
}

// Pre-book Course
function prebookCourse() {
    const startDate = document.getElementById('startDate').value;
    const batch = document.getElementById('batch').value;

    if (!startDate || !batch) {
        alert('Please select start date and batch');
        return;
    }

    appData.prebooking.startDate = startDate;
    appData.prebooking.batch = batch;

    alert('Course pre-booked successfully!');
}

// Load Faculty Details
function loadFacultyDetails() {
    const facultyGrid = document.getElementById('facultyGrid');
    facultyGrid.innerHTML = '';

    facultyData.forEach(faculty => {
        const card = document.createElement('div');
        card.className = 'faculty-card';
        card.innerHTML = `
            <div class="faculty-avatar">${faculty.avatar}</div>
            <div class="faculty-name">${faculty.name}</div>
            <div class="faculty-specialization">${faculty.specialization}</div>
            <div class="faculty-contact">
                <p><strong>Phone:</strong> <a href="tel:${faculty.phone}">${faculty.phone}</a></p>
                <p><strong>Email:</strong> <a href="mailto:${faculty.email}">${faculty.email}</a></p>
                <p><strong>Office:</strong> ${faculty.office}</p>
            </div>
        `;
        facultyGrid.appendChild(card);
    });
}

// Search Faculty
function searchFaculty() {
    const searchTerm = document.getElementById('facultySearch').value.toLowerCase();
    const facultyCards = document.querySelectorAll('.faculty-card');

    facultyCards.forEach(card => {
        const text = card.textContent.toLowerCase();
        card.style.display = text.includes(searchTerm) ? 'block' : 'none';
    });
}

// Load Hostel Rooms
function loadHostelRooms() {
    const roomsGrid = document.getElementById('roomsGrid');
    roomsGrid.innerHTML = '';

    hostelRooms.forEach(room => {
        const card = document.createElement('div');
        card.className = 'room-card';
        card.innerHTML = `
            <div class="room-type">${room.type}</div>
            <p style="color: #7f8c8d; font-size: 12px; margin: 8px 0;">Room: ${room.number}</p>
            <p style="color: #7f8c8d; font-size: 12px; margin: 8px 0;">${room.beds} ${room.beds === 1 ? 'Bed' : 'Beds'}</p>
            <div class="room-price">₹${room.price.toLocaleString()}/year</div>
            <div style="font-size: 11px; color: #95a5a6; margin-top: 8px;">
                ${room.features.join(', ')}
            </div>
        `;
        card.onclick = () => selectRoom(room, card);
        roomsGrid.appendChild(card);
    });
}

// Select Room
function selectRoom(room, cardElement) {
    document.querySelectorAll('.room-card').forEach(card => card.classList.remove('selected'));
    cardElement.classList.add('selected');

    appData.hostel = {
        roomType: room.type,
        roomNumber: room.number,
        roomPrice: room.price,
        advancePayment: 0
    };

    const summary = `
        <p><strong>Room Type:</strong> ${room.type}</p>
        <p><strong>Room Number:</strong> ${room.number}</p>
        <p><strong>Beds:</strong> ${room.beds}</p>
        <p><strong>Annual Rent:</strong> ₹${room.price.toLocaleString()}</p>
        <p style="margin-top: 10px; font-size: 12px; color: #7f8c8d;">
            Features: ${room.features.join(', ')}
        </p>
    `;
    document.getElementById('bookingSummary').innerHTML = summary;
}

// Process Payment
function processPayment() {
    const advanceAmount = document.getElementById('advanceAmount').value;

    if (!advanceAmount) {
        alert('Please select advance payment amount');
        return;
    }

    appData.hostel.advancePayment = (parseInt(advanceAmount) / 100) * appData.hostel.roomPrice;
    alert(`Payment of ₹${appData.hostel.advancePayment.toLocaleString()} will be processed. This is a demo.`);
}

// Generate Final Summary
function generateFinalSummary() {
    const summary = `
        <p><strong>Name:</strong> ${appData.user.name || appData.user.email || appData.user.phone}</p>
        <p><strong>Department:</strong> ${appData.department}</p>
        <p><strong>Course:</strong> ${appData.course}</p>
        <p><strong>10th Marks:</strong> ${appData.qualifications.tenthMarks || 'Not entered'}</p>
        <p><strong>12th Marks:</strong> ${appData.qualifications.twelfthMarks || 'Not entered'}</p>
        ${appData.qualifications.keamRank ? `<p><strong>KEAM Rank:</strong> ${appData.qualifications.keamRank}</p>` : ''}
        ${appData.qualifications.jeeRank ? `<p><strong>JEE Rank:</strong> ${appData.qualifications.jeeRank}</p>` : ''}
        <p><strong>Preferred Start Date:</strong> ${appData.prebooking.startDate || 'Not selected'}</p>
        <p><strong>Batch:</strong> ${appData.prebooking.batch || 'Not selected'}</p>
        <p><strong>Hostel Room:</strong> ${appData.hostel.roomType} (${appData.hostel.roomNumber})</p>
        <p><strong>Room Rent:</strong> ₹${appData.hostel.roomPrice.toLocaleString()}/year</p>
        <p><strong>Advance Paid:</strong> ₹${appData.hostel.advancePayment.toLocaleString()}</p>
    `;
    document.getElementById('finalSummary').innerHTML = summary;
}

// Confirm Application
function confirmApplication() {
    if (!appData.hostel.roomType) {
        alert('Please complete all steps before confirming');
        return;
    }

    alert('Application submitted successfully!\n\nYour application has been received. You will receive a confirmation email shortly.');
    console.log('Final Application Data:', appData);
}

// Download PDF
function downloadPDF() {
    let content = 'ENGINEERING COLLEGE ADMINISTRATION\nAPPLICATION SUMMARY\n\n';
    content += `Name: ${appData.user.name || appData.user.email || appData.user.phone}\n`;
    content += `Department: ${appData.department}\n`;
    content += `Course: ${appData.course}\n`;
    content += `10th Marks: ${appData.qualifications.tenthMarks}\n`;
    content += `12th Marks: ${appData.qualifications.twelfthMarks}\n`;
    content += `KEAM Rank: ${appData.qualifications.keamRank || 'N/A'}\n`;
    content += `JEE Rank: ${appData.qualifications.jeeRank || 'N/A'}\n`;
    content += `Start Date: ${appData.prebooking.startDate}\n`;
    content += `Batch: ${appData.prebooking.batch}\n`;
    content += `Room: ${appData.hostel.roomType} (${appData.hostel.roomNumber})\n`;
    content += `Room Rent: ₹${appData.hostel.roomPrice}\n`;
    content += `Advance Paid: ₹${appData.hostel.advancePayment}\n`;

    const element = document.createElement('a');
    element.setAttribute('href', 'data:text/plain;charset=utf-8,' + encodeURIComponent(content));
    element.setAttribute('download', 'application_summary.txt');
    element.style.display = 'none';
    document.body.appendChild(element);
    element.click();
    document.body.removeChild(element);
}

// Logout
function logout() {
    if (confirm('Are you sure you want to logout?')) {
        appData = {
            user: { name: '', email: '', phone: '', credentials: '' },
            department: '',
            course: '',
            qualifications: { tenthMarks: null, twelfthMarks: null, keamRank: null, jeeRank: null },
            prebooking: { startDate: '', batch: '' },
            hostel: { roomType: '', roomNumber: '', roomPrice: 0, advancePayment: 0 }
        };
        document.getElementById('loginForm')?.reset();
        document.getElementById('signupForm')?.reset();
        document.getElementById('otpSection').classList.add('hidden');
        showPage('loginPage');
    }
}

// Initialize on page load
document.addEventListener('DOMContentLoaded', function() {
    showPage('loginPage');
    
    // Load faculty details when faculty page is shown
    const observer = new MutationObserver(function(mutations) {
        if (document.getElementById('facultyPage').classList.contains('active')) {
            loadFacultyDetails();
        }
        if (document.getElementById('hostelPage').classList.contains('active')) {
            loadHostelRooms();
        }
        if (document.getElementById('exitPage').classList.contains('active')) {
            generateFinalSummary();
        }
    });

    observer.observe(document.getElementById('facultyPage'), { attributes: true, attributeFilter: ['class'] });
    observer.observe(document.getElementById('hostelPage'), { attributes: true, attributeFilter: ['class'] });
    observer.observe(document.getElementById('exitPage'), { attributes: true, attributeFilter: ['class'] });
});

