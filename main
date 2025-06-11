<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Work Order Submission Form</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            padding: 20px;
        }

        .container {
            max-width: 600px;
            margin: 0 auto;
            background: white;
            border-radius: 12px;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
            overflow: hidden;
        }

        .header {
            background: linear-gradient(135deg, #2c3e50, #3498db);
            color: white;
            padding: 30px;
            text-align: center;
        }

        .header h1 {
            font-size: 28px;
            margin-bottom: 10px;
            font-weight: 300;
        }

        .header p {
            opacity: 0.9;
            font-size: 16px;
        }

        .form-container {
            padding: 40px;
        }

        .form-group {
            margin-bottom: 25px;
        }

        label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
            color: #2c3e50;
            font-size: 14px;
        }

        input[type="text"], input[type="email"], textarea {
            width: 100%;
            padding: 12px 16px;
            border: 2px solid #e1e8ed;
            border-radius: 8px;
            font-size: 16px;
            transition: all 0.3s ease;
            background: #f8f9fa;
        }

        input[type="text"]:focus, input[type="email"]:focus, textarea:focus {
            outline: none;
            border-color: #3498db;
            background: white;
            box-shadow: 0 0 0 3px rgba(52, 152, 219, 0.1);
        }

        textarea {
            resize: vertical;
            min-height: 120px;
            font-family: inherit;
        }

        .required {
            color: #e74c3c;
        }

        .submit-btn {
            background: linear-gradient(135deg, #3498db, #2980b9);
            color: white;
            padding: 15px 30px;
            border: none;
            border-radius: 8px;
            font-size: 16px;
            font-weight: 600;
            cursor: pointer;
            width: 100%;
            transition: all 0.3s ease;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .submit-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 20px rgba(52, 152, 219, 0.3);
        }

        .submit-btn:disabled {
            background: #bdc3c7;
            cursor: not-allowed;
            transform: none;
            box-shadow: none;
        }

        .verification-screen {
            display: none;
            text-align: center;
            padding: 40px;
        }

        .company-verification-screen {
            display: none;
            text-align: center;
            padding: 40px;
        }

        .company-verification-screen h2 {
            color: #f39c12;
            margin-bottom: 20px;
            font-size: 24px;
        }

        .company-verification-screen p {
            color: #7f8c8d;
            line-height: 1.6;
            margin-bottom: 20px;
        }

        .verification-options {
            background: #f8f9fa;
            border: 1px solid #e1e8ed;
            border-radius: 8px;
            padding: 20px;
            margin: 20px 0;
        }

        .verification-option {
            background: white;
            border: 1px solid #ddd;
            border-radius: 6px;
            padding: 15px;
            margin: 10px 0;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .verification-option:hover {
            border-color: #3498db;
            background: #f8f9fa;
        }

        .verification-option.selected {
            border-color: #3498db;
            background: #e8f4fd;
        }

        .company-code-input {
            width: 100%;
            padding: 12px;
            border: 2px solid #e1e8ed;
            border-radius: 6px;
            margin-top: 10px;
            display: none;
        }

        .company-email-input {
            width: 100%;
            padding: 12px;
            border: 2px solid #e1e8ed;
            border-radius: 6px;
            margin-top: 10px;
            display: none;
        }

        .verify-company-btn {
            background: #f39c12;
            color: white;
            padding: 12px 24px;
            border: none;
            border-radius: 6px;
            cursor: pointer;
            margin-top: 15px;
            font-size: 14px;
        }

        .back-btn {
            background: #95a5a6;
            color: white;
            padding: 10px 20px;
            border: none;
            border-radius: 6px;
            cursor: pointer;
            margin-right: 10px;
        }

        .verification-screen h2 {
            color: #27ae60;
            margin-bottom: 20px;
            font-size: 24px;
        }

        .verification-screen p {
            color: #7f8c8d;
            line-height: 1.6;
            margin-bottom: 20px;
        }

        .email-preview {
            background: #f8f9fa;
            border: 1px solid #e1e8ed;
            border-radius: 8px;
            padding: 20px;
            margin-top: 20px;
            text-align: left;
        }

        .email-preview h3 {
            color: #2c3e50;
            margin-bottom: 15px;
        }

        .email-content {
            background: white;
            padding: 15px;
            border-radius: 6px;
            font-family: monospace;
            font-size: 12px;
            white-space: pre-wrap;
            overflow-x: auto;
        }

        .verify-btn {
            background: #27ae60;
            color: white;
            padding: 10px 20px;
            border: none;
            border-radius: 6px;
            cursor: pointer;
            margin-top: 10px;
        }

        .success-screen {
            display: none;
            text-align: center;
            padding: 40px;
        }

        .success-screen h2 {
            color: #27ae60;
            margin-bottom: 20px;
        }

        .parsed-data {
            background: #f8f9fa;
            border: 1px solid #e1e8ed;
            border-radius: 8px;
            padding: 20px;
            margin-top: 20px;
            text-align: left;
        }

        .parsed-data h3 {
            color: #2c3e50;
            margin-bottom: 15px;
        }

        .regex-output {
            background: white;
            padding: 15px;
            border-radius: 6px;
            font-family: monospace;
            font-size: 12px;
            white-space: pre-wrap;
        }

        .qr-info {
            background: #e8f4fd;
            border: 1px solid #3498db;
            border-radius: 8px;
            padding: 15px;
            margin-bottom: 20px;
        }

        .qr-info h3 {
            color: #2980b9;
            margin-bottom: 10px;
            font-size: 16px;
        }

        .qr-info p {
            color: #34495e;
            margin-bottom: 8px;
            font-size: 14px;
        }

        .prefilled-field {
            background: #e8f5e8 !important;
            border-color: #27ae60 !important;
        }

        .prefilled-label::after {
            content: " ✓ (Pre-filled from QR)";
            color: #27ae60;
            font-size: 12px;
            font-weight: normal;
        }

        .qr-demo {
            background: #f8f9fa;
            border: 1px solid #e1e8ed;
            border-radius: 8px;
            padding: 20px;
            margin-top: 20px;
        }

        .qr-demo h3 {
            color: #2c3e50;
            margin-bottom: 15px;
        }

        .qr-example {
            background: white;
            padding: 15px;
            border-radius: 6px;
            font-family: monospace;
            font-size: 12px;
            margin-bottom: 10px;
        }

        .test-qr-btn {
            background: #9b59b6;
            color: white;
            padding: 8px 16px;
            border: none;
            border-radius: 6px;
            cursor: pointer;
            margin-right: 10px;
            margin-bottom: 5px;
            font-size: 12px;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>Work Order Submission</h1>
            <p>Please complete all required fields to submit your work order</p>
        </div>

        <!-- Main Form -->
        <div id="mainForm" class="form-container">
            <!-- QR Code Info Section -->
            <div id="qrInfo" class="qr-info" style="display: none;">
                <h3>📱 QR Code Detected</h3>
                <p>Some information has been automatically filled from your QR code scan.</p>
                <div id="qrDataInfo"></div>
                <p>You can still edit any visible pre-filled fields if needed.</p>
            </div>

            <form id="workOrderForm">
                <div class="form-group">
                    <label for="technicianName">Technician Name <span class="required">*</span></label>
                    <input type="text" id="technicianName" name="technicianName" required>
                </div>

                <div class="form-group">
                    <label for="companyName">Company Name <span class="required">*</span></label>
                    <input type="text" id="companyName" name="companyName" required>
                </div>

                <div class="form-group">
                    <label for="workOrderNumber">Work Order # <span class="required">*</span></label>
                    <input type="text" id="workOrderNumber" name="workOrderNumber" required>
                </div>

                <div class="form-group">
                    <label for="panelAccount">Panel Account # <span class="required">*</span></label>
                    <input type="text" id="panelAccount" name="panelAccount" required>
                </div>

                <!-- Hidden fields populated by QR code -->
                <input type="hidden" id="referenceId" name="referenceId">
                <input type="hidden" id="locationAddress" name="locationAddress">

                <div class="form-group">
                    <label for="technicianEmail">Your Email Address <span class="required">*</span></label>
                    <input type="email" id="technicianEmail" name="technicianEmail" required>
                </div>

                <div class="form-group">
                    <label for="workDetail">Detail of Work Being Performed <span class="required">*</span></label>
                    <textarea id="workDetail" name="workDetail" placeholder="Please provide detailed description of the work being performed..." required></textarea>
                </div>

                <button type="submit" class="submit-btn">Submit Work Order</button>
            </form>
        </div>

        <!-- Company Verification Screen -->
        <div id="companyVerificationScreen" class="company-verification-screen">
            <h2>🏢 Company Verification Required</h2>
            <p>Please verify your association with <strong id="companyNameDisplay"></strong> before proceeding.</p>
            
            <div class="verification-options">
                <h3>Choose verification method:</h3>
                
                <div class="verification-option" id="emailDomainOption" onclick="selectVerificationMethod('email')">
                    <strong>📧 Company Email Verification</strong>
                    <p>Use your official company email address</p>
                    <input type="email" id="companyEmailInput" class="company-email-input" placeholder="Enter your @company.com email address">
                </div>
                
                <div class="verification-option" id="companyCodeOption" onclick="selectVerificationMethod('code')">
                    <strong>🔑 Company Access Code</strong>
                    <p>Enter your company's work order access code</p>
                    <input type="text" id="companyCodeInput" class="company-code-input" placeholder="Enter company access code">
                </div>
                
                <div class="verification-option" id="managerApprovalOption" onclick="selectVerificationMethod('manager')">
                    <strong>👤 Manager Approval</strong>
                    <p>Request approval from your company manager</p>
                    <input type="email" id="managerEmailInput" class="company-email-input" placeholder="Enter manager's email for approval">
                </div>
            </div>
            
            <button class="back-btn" onclick="goBackToForm()">← Back to Form</button>
            <button class="verify-company-btn" id="verifyCompanyBtn" onclick="verifyCompany()">Verify Company</button>
        </div>

        <!-- Email Verification Screen -->
        <div id="verificationScreen" class="verification-screen">
            <h2>📧 Check Your Email</h2>
            <p>We've sent a verification email to <strong id="emailAddress"></strong></p>
            <p>Please click the verification link in the email to confirm your submission.</p>
            
            <div class="email-preview">
                <h3>📧 Email Preview (for demonstration):</h3>
                <div class="email-content" id="emailContent"></div>
                <button class="verify-btn" onclick="simulateVerification()">🔗 Simulate Verification Click</button>
            </div>
        </div>

        <!-- Success Screen -->
        <div id="successScreen" class="success-screen">
            <h2>✅ Submission Verified & Processed</h2>
            <p>Your work order has been successfully submitted and verified.</p>
            
            <div class="parsed-data">
                <h3>📋 Structured Data for Your Application:</h3>
                <div class="regex-output" id="structuredData"></div>
            </div>

            <div class="qr-demo">
                <h3>📱 QR Code URL Examples:</h3>
                <p>Generate QR codes with these URL formats to prefill form data:</p>
                
                <div class="qr-example">
Example 1: Basic Panel with Location
https://yourdomain.com/form?panel=PA-12345&company=ABC%20Corp&location=123%20Main%20St,%20Anytown%20USA

Example 2: Complete Work Order with Reference
https://yourdomain.com/form?panel=PA-67890&company=XYZ%20Industries&wo=WO-2024-001&tech=John%20Doe&ref=REF-789&location=456%20Industrial%20Blvd,%20Metro%20City

Example 3: Equipment Maintenance with All Fields
https://yourdomain.com/form?panel=PA-99999&company=Tech%20Solutions&detail=Replace%20main%20control%20board&location=789%20Factory%20Ave,%20Production%20Town&ref=MAINT-2024-15
                </div>

                <p><strong>Test the QR functionality:</strong></p>
                <button class="test-qr-btn" onclick="testQR1()">Test Basic QR</button>
                <button class="test-qr-btn" onclick="testQR2()">Test QR + Company Verification</button>
                <button class="test-qr-btn" onclick="testQR3()">Test Equipment QR</button>
                
                <p style="margin-top: 15px; font-size: 12px; color: #7f8c8d;">
                    <strong>Note:</strong> "ABC Corp", "XYZ Industries", and "Tech Solutions" require company verification. Other companies skip this step.
                </p>
            </div>
            
            <button class="submit-btn" onclick="resetForm()" style="margin-top: 20px; width: auto; padding: 10px 20px;">Submit Another Order</button>
        </div>
    </div>

    <script>
        let formData = {};
        let verificationToken = '';
        let prefilledFields = [];
        let selectedVerificationMethod = '';
        let companyVerified = false;

        // Company configuration - you can customize this
        const companyConfig = {
            'ABC Corp': {
                domains: ['abc-corp.com', 'abccorp.com'],
                accessCode: 'ABC2024',
                managers: ['manager@abc-corp.com', 'supervisor@abc-corp.com']
            },
            'XYZ Industries': {
                domains: ['xyzind.com', 'xyzindustries.com'],
                accessCode: 'XYZ789',
                managers: ['admin@xyzind.com']
            },
            'Tech Solutions': {
                domains: ['techsol.com', 'tech-solutions.net'],
                accessCode: 'TECH2024',
                managers: ['manager@techsol.com']
            }
        };

        // Check for URL parameters when page loads
        document.addEventListener('DOMContentLoaded', function() {
            console.log('DOM loaded, setting up form'); // Debug log
            
            // Verify form exists
            const form = document.getElementById('workOrderForm');
            if (form) {
                console.log('Form found successfully'); // Debug log
            } else {
                console.error('Form not found!');
                return;
            }
            
            checkForQRParameters();
            console.log('Setup complete'); // Debug log
        });

        function checkForQRParameters() {
            const urlParams = new URLSearchParams(window.location.search);
            let hasQRData = false;
            let qrDataInfo = [];

            // Map URL parameters to form fields
            const paramMap = {
                'panel': 'panelAccount',
                'company': 'companyName', 
                'wo': 'workOrderNumber',
                'tech': 'technicianName',
                'email': 'technicianEmail',
                'detail': 'workDetail',
                'ref': 'referenceId',
                'location': 'locationAddress'
            };

            // Populate fields from URL parameters
            for (const [param, fieldId] of Object.entries(paramMap)) {
                const value = urlParams.get(param);
                if (value) {
                    const field = document.getElementById(fieldId);
                    if (field) {
                        field.value = decodeURIComponent(value);
                        
                        // Only add visual styling to visible fields
                        if (fieldId !== 'referenceId' && fieldId !== 'locationAddress') {
                            field.classList.add('prefilled-field');
                            
                            // Update label to show it's prefilled
                            const label = document.querySelector(`label[for="${fieldId}"]`);
                            if (label) {
                                label.classList.add('prefilled-label');
                            }
                        } else {
                            // For hidden fields, add to info display
                            if (fieldId === 'referenceId') {
                                qrDataInfo.push(`<strong>Reference ID:</strong> ${decodeURIComponent(value)}`);
                            } else if (fieldId === 'locationAddress') {
                                qrDataInfo.push(`<strong>Location:</strong> ${decodeURIComponent(value)}`);
                            }
                        }
                        
                        prefilledFields.push(fieldId);
                        hasQRData = true;
                    }
                }
            }

            // Show QR info banner if any data was prefilled
            if (hasQRData) {
                document.getElementById('qrInfo').style.display = 'block';
                
                // Display hidden field info
                if (qrDataInfo.length > 0) {
                    document.getElementById('qrDataInfo').innerHTML = 
                        '<p><strong>Automatically captured:</strong><br>' + qrDataInfo.join('<br>') + '</p>';
                }
            }
        }

        // Test QR functions for demo
        function testQR1() {
            window.location.href = window.location.pathname + '?panel=PA-12345&company=ABC%20Corp&location=123%20Main%20St,%20Anytown%20USA';
        }

        function testQR2() {
            window.location.href = window.location.pathname + '?panel=PA-67890&company=XYZ%20Industries&wo=WO-2024-001&tech=John%20Doe&ref=REF-789&location=456%20Industrial%20Blvd,%20Metro%20City';
        }

        function testQR3() {
            window.location.href = window.location.pathname + '?panel=PA-99999&company=Tech%20Solutions&detail=Replace%20main%20control%20board&location=789%20Factory%20Ave,%20Production%20Town&ref=MAINT-2024-15';
        }

        document.getElementById('workOrderForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            console.log('Form submitted!'); // Debug log
            
            try {
                // Collect form data
                formData = {
                    technicianName: document.getElementById('technicianName').value,
                    companyName: document.getElementById('companyName').value,
                    workOrderNumber: document.getElementById('workOrderNumber').value,
                    panelAccount: document.getElementById('panelAccount').value,
                    referenceId: document.getElementById('referenceId').value,
                    locationAddress: document.getElementById('locationAddress').value,
                    technicianEmail: document.getElementById('technicianEmail').value,
                    workDetail: document.getElementById('workDetail').value
                };

                console.log('Form data collected:', formData); // Debug log

                // Check if company verification is needed
                if (needsCompanyVerification()) {
                    console.log('Company verification needed'); // Debug log
                    showCompanyVerificationScreen();
                } else {
                    console.log('Skipping company verification'); // Debug log
                    // Skip company verification, go directly to email verification
                    companyVerified = false; // No verification needed
                    selectedVerificationMethod = 'none';
                    proceedToEmailVerification();
                }
            } catch (error) {
                console.error('Error in form submission:', error);
                alert('Error submitting form. Please check console for details.');
            }
        });

        function needsCompanyVerification() {
            // Check if this company requires verification
            return companyConfig.hasOwnProperty(formData.companyName);
        }

        function showCompanyVerificationScreen() {
            document.getElementById('mainForm').style.display = 'none';
            document.getElementById('companyVerificationScreen').style.display = 'block';
            document.getElementById('companyNameDisplay').textContent = formData.companyName;
            
            // Reset verification method
            selectedVerificationMethod = '';
            clearVerificationInputs();
        }

        function selectVerificationMethod(method) {
            selectedVerificationMethod = method;
            
            // Clear all inputs and styling
            clearVerificationInputs();
            document.querySelectorAll('.verification-option').forEach(opt => opt.classList.remove('selected'));
            
            // Show selected method
            if (method === 'email') {
                document.getElementById('emailDomainOption').classList.add('selected');
                document.getElementById('companyEmailInput').style.display = 'block';
                document.getElementById('companyEmailInput').focus();
            } else if (method === 'code') {
                document.getElementById('companyCodeOption').classList.add('selected');
                document.getElementById('companyCodeInput').style.display = 'block';
                document.getElementById('companyCodeInput').focus();
            } else if (method === 'manager') {
                document.getElementById('managerApprovalOption').classList.add('selected');
                document.getElementById('managerEmailInput').style.display = 'block';
                document.getElementById('managerEmailInput').focus();
            }
        }

        function clearVerificationInputs() {
            document.getElementById('companyEmailInput').style.display = 'none';
            document.getElementById('companyCodeInput').style.display = 'none';
            document.getElementById('managerEmailInput').style.display = 'none';
            document.getElementById('companyEmailInput').value = '';
            document.getElementById('companyCodeInput').value = '';
            document.getElementById('managerEmailInput').value = '';
        }

        function verifyCompany() {
            if (!selectedVerificationMethod) {
                alert('Please select a verification method.');
                return;
            }

            const company = companyConfig[formData.companyName];
            
            if (selectedVerificationMethod === 'email') {
                const email = document.getElementById('companyEmailInput').value;
                const domain = email.split('@')[1];
                
                if (company.domains.includes(domain)) {
                    companyVerified = true;
                    // Update the technician email if they used company email for verification
                    if (email !== formData.technicianEmail) {
                        formData.technicianEmail = email;
                    }
                    proceedToEmailVerification();
                } else {
                    alert(`Email domain @${domain} is not authorized for ${formData.companyName}. Please use an official company email or contact your manager.`);
                }
                
            } else if (selectedVerificationMethod === 'code') {
                const code = document.getElementById('companyCodeInput').value;
                
                if (code === company.accessCode) {
                    companyVerified = true;
                    proceedToEmailVerification();
                } else {
                    alert('Invalid access code. Please check with your company administrator.');
                }
                
            } else if (selectedVerificationMethod === 'manager') {
                const managerEmail = document.getElementById('managerEmailInput').value;
                
                if (company.managers.includes(managerEmail)) {
                    companyVerified = true;
                    // In a real implementation, you'd send approval request to manager
                    alert('Manager approval request would be sent to ' + managerEmail + '. For this demo, approval is automatic.');
                    proceedToEmailVerification();
                } else {
                    alert('Manager email not recognized. Please enter a valid manager email address.');
                }
            }
        }

        function goBackToForm() {
            document.getElementById('companyVerificationScreen').style.display = 'none';
            document.getElementById('mainForm').style.display = 'block';
        }

        function proceedToEmailVerification() {
            // Generate verification token
            verificationToken = 'WO_' + Date.now() + '_' + Math.random().toString(36).substr(2, 9);
            
            // Show email verification screen
            showVerificationScreen();
        }

        function showVerificationScreen() {
            console.log('Showing verification screen'); // Debug log
            try {
                document.getElementById('mainForm').style.display = 'none';
                document.getElementById('companyVerificationScreen').style.display = 'none';
                document.getElementById('verificationScreen').style.display = 'block';
                document.getElementById('emailAddress').textContent = formData.technicianEmail;
                
                // Generate email content
                const emailContent = generateVerificationEmail();
                document.getElementById('emailContent').textContent = emailContent;
                console.log('Verification screen shown successfully'); // Debug log
            } catch (error) {
                console.error('Error in showVerificationScreen:', error);
            }
        }

        function generateVerificationEmail() {
            const verificationLink = `https://yourdomain.com/verify?token=${verificationToken}`;
            const companyStatus = companyVerified ? `✅ Company Verified via ${selectedVerificationMethod}` : '✅ No company verification required';
            
            return `Subject: Verify Your Work Order Submission

Dear ${formData.technicianName},

You recently submitted a work order through our system. Please click the link below to verify and confirm your submission:

${verificationLink}

Work Order Details:
- Work Order #: ${formData.workOrderNumber}
- Company: ${formData.companyName} (${companyStatus})
- Panel Account #: ${formData.panelAccount}
- Reference ID: ${formData.referenceId || 'None provided'}
- Location: ${formData.locationAddress}

If you did not submit this work order, please ignore this email.

Thank you,
Work Order Management System`;
        }

        function simulateVerification() {
            // Hide verification screen
            document.getElementById('verificationScreen').style.display = 'none';
            document.getElementById('companyVerificationScreen').style.display = 'none';
            
            // Show success screen with structured data
            showSuccessScreen();
        }

        function showSuccessScreen() {
            document.getElementById('successScreen').style.display = 'block';
            
            // Generate structured data for regex parsing
            const structuredData = generateStructuredData();
            document.getElementById('structuredData').textContent = structuredData;
        }

        function generateStructuredData() {
            const timestamp = new Date().toISOString();
            const companyVerificationStatus = companyVerified ? `VERIFIED_${selectedVerificationMethod.toUpperCase()}` : 'NOT_REQUIRED';
            
            return `SUBMISSION_START
TIMESTAMP:${timestamp}
VERIFICATION_TOKEN:${verificationToken}
COMPANY_VERIFICATION:${companyVerificationStatus}
FIELD:technician_name:${formData.technicianName}
FIELD:company_name:${formData.companyName}
FIELD:work_order_number:${formData.workOrderNumber}
FIELD:panel_account_number:${formData.panelAccount}
FIELD:reference_id:${formData.referenceId || 'N/A'}
FIELD:location_address:${formData.locationAddress}
FIELD:technician_email:${formData.technicianEmail}
FIELD:work_detail:${formData.workDetail.replace(/\n/g, '\\n')}
SUBMISSION_END

# Regex Pattern for Parsing:
# FIELD:([^:]+):(.+)
# COMPANY_VERIFICATION:([^\\n]+)
# 
# This will capture:
# Group 1: Field name (e.g., "technician_name")
# Group 2: Field value (e.g., "John Doe")
# Company verification status for security audit`;
        }

        function resetForm() {
            // Reset form
            document.getElementById('workOrderForm').reset();
            
            // Clear QR prefilled styling
            prefilledFields.forEach(fieldId => {
                const field = document.getElementById(fieldId);
                const label = document.querySelector(`label[for="${fieldId}"]`);
                if (field) field.classList.remove('prefilled-field');
                if (label) label.classList.remove('prefilled-label');
            });
            
            // Hide all screens except main form
            document.getElementById('qrInfo').style.display = 'none';
            document.getElementById('qrDataInfo').innerHTML = '';
            document.getElementById('companyVerificationScreen').style.display = 'none';
            document.getElementById('verificationScreen').style.display = 'none';
            document.getElementById('successScreen').style.display = 'none';
            document.getElementById('mainForm').style.display = 'block';
            
            // Clear all data and states
            formData = {};
            verificationToken = '';
            prefilledFields = [];
            selectedVerificationMethod = '';
            companyVerified = false;
            clearVerificationInputs();
            
            // Clear URL parameters
            window.history.replaceState({}, document.title, window.location.pathname);
        }
    </script>
</body>
</html>
