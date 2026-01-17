<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mrs. Monica Geingos Initiative Investments Platform</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;600;700&family=Open+Sans:wght@300;400;600&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #0d4a82;
            --secondary: #1a7bca;
            --accent: #00c896;
            --light: #f8f9fa;
            --dark: #212529;
            --success: #28a745;
            --warning: #ffc107;
            --danger: #dc3545;
            --gray: #6c757d;
            --light-gray: #e9ecef;
            --border: #dee2e6;
            --shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
            --transition: all 0.3s ease;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Open Sans', sans-serif;
            background: linear-gradient(135deg, #f5f7fa 0%, #e4edf9 100%);
            color: var(--dark);
            line-height: 1.6;
        }
        
        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header Styles */
        header {
            background: white;
            box-shadow: var(--shadow);
            position: sticky;
            top: 0;
            z-index: 1000;
        }
        
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 0;
        }
        
        .logo {
            display: flex;
            align-items: center;
            gap: 12px;
        }
        
        .logo-icon {
            background: var(--primary);
            color: white;
            width: 48px;
            height: 48px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 24px;
            font-weight: bold;
        }
        
        .logo-text h1 {
            font-family: 'Montserrat', sans-serif;
            font-weight: 700;
            font-size: 22px;
            color: var(--primary);
            line-height: 1.2;
        }
        
        .logo-text p {
            font-size: 12px;
            color: var(--gray);
            margin-top: 4px;
        }
        
        nav ul {
            display: flex;
            list-style: none;
            gap: 25px;
        }
        
        nav a {
            text-decoration: none;
            color: var(--dark);
            font-weight: 600;
            font-size: 16px;
            transition: var(--transition);
            position: relative;
        }
        
        nav a:hover {
            color: var(--secondary);
        }
        
        nav a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--accent);
            transition: var(--transition);
        }
        
        nav a:hover::after {
            width: 100%;
        }
        
        .auth-buttons {
            display: flex;
            gap: 15px;
        }
        
        .btn {
            padding: 10px 20px;
            border-radius: 30px;
            font-weight: 600;
            cursor: pointer;
            transition: var(--transition);
            text-decoration: none;
            display: inline-block;
            text-align: center;
            border: none;
            font-size: 16px;
        }
        
        .btn-primary {
            background: var(--primary);
            color: white;
        }
        
        .btn-primary:hover {
            background: var(--secondary);
            transform: translateY(-2px);
        }
        
        .btn-outline {
            background: transparent;
            border: 2px solid var(--primary);
            color: var(--primary);
        }
        
        .btn-outline:hover {
            background: var(--primary);
            color: white;
            transform: translateY(-2px);
        }
        
        /* Hero Section */
        .hero {
            padding: 80px 0;
            background: linear-gradient(rgba(13, 74, 130, 0.85), rgba(13, 74, 130, 0.9)), url('https://images.unsplash.com/photo-1553877522-43269d4ea984?ixlib=rb-4.0.3&auto=format&fit=crop&w=1950&q=80');
            background-size: cover;
            background-position: center;
            color: white;
            text-align: center;
        }
        
        .hero-content {
            max-width: 800px;
            margin: 0 auto;
        }
        
        .hero h2 {
            font-family: 'Montserrat', sans-serif;
            font-size: 42px;
            font-weight: 700;
            margin-bottom: 20px;
            line-height: 1.2;
        }
        
        .hero p {
            font-size: 18px;
            margin-bottom: 30px;
            opacity: 0.9;
        }
        
        .bonus-badge {
            background: var(--accent);
            color: var(--dark);
            padding: 8px 20px;
            border-radius: 30px;
            font-weight: 700;
            display: inline-flex;
            align-items: center;
            gap: 8px;
            margin-top: 15px;
            font-size: 18px;
        }
        
        /* Features Section */
        .section {
            padding: 80px 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 50px;
        }
        
        .section-title h2 {
            font-family: 'Montserrat', sans-serif;
            font-size: 36px;
            color: var(--primary);
            margin-bottom: 15px;
        }
        
        .section-title p {
            color: var(--gray);
            max-width: 600px;
            margin: 0 auto;
        }
        
        /* Investment Plans */
        .plans-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .plan-card {
            background: white;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: var(--transition);
        }
        
        .plan-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 12px 20px rgba(0, 0, 0, 0.15);
        }
        
        .plan-header {
            background: var(--primary);
            color: white;
            padding: 25px;
            text-align: center;
        }
        
        .plan-header h3 {
            font-size: 24px;
            margin-bottom: 10px;
        }
        
        .plan-price {
            font-size: 32px;
            font-weight: 700;
            margin: 10px 0;
        }
        
        .plan-body {
            padding: 25px;
        }
        
        .plan-features {
            list-style: none;
            margin: 20px 0;
        }
        
        .plan-features li {
            padding: 8px 0;
            border-bottom: 1px dashed var(--border);
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .plan-features li:last-child {
            border-bottom: none;
        }
        
        .plan-features i {
            color: var(--accent);
        }
        
        /* Testimonials */
        .testimonials-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .testimonial-card {
            background: white;
            border-radius: 15px;
            padding: 30px;
            box-shadow: var(--shadow);
            position: relative;
        }
        
        .testimonial-card::before {
            content: """;
            position: absolute;
            top: 20px;
            left: 20px;
            font-size: 80px;
            color: var(--light-gray);
            font-family: Georgia, serif;
            line-height: 1;
        }
        
        .testimonial-content {
            margin-top: 20px;
            margin-bottom: 20px;
            font-style: italic;
            color: var(--gray);
        }
        
        .testimonial-author {
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .author-avatar {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background: var(--light-gray);
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            color: var(--primary);
        }
        
        .author-info h4 {
            font-weight: 600;
        }
        
        .author-info p {
            color: var(--gray);
            font-size: 14px;
        }
        
        /* Trading Signals */
        .trading-section {
            background: white;
            border-radius: 15px;
            padding: 30px;
            box-shadow: var(--shadow);
        }
        
        .signals-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 20px;
        }
        
        .signals-list {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
        }
        
        .signal-card {
            background: var(--light);
            border-radius: 10px;
            padding: 20px;
            border-left: 4px solid var(--accent);
        }
        
        .signal-pair {
            font-weight: 700;
            margin-bottom: 5px;
            color: var(--primary);
        }
        
        .signal-direction {
            display: inline-block;
            padding: 3px 10px;
            border-radius: 20px;
            font-size: 12px;
            font-weight: 600;
            margin-right: 10px;
        }
        
        .buy { background: #d4edda; color: #155724; }
        .sell { background: #f8d7da; color: #721c24; }
        
        .signal-time {
            color: var(--gray);
            font-size: 14px;
        }
        
        /* Payment Methods */
        .payment-methods {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 30px;
            margin-top: 30px;
        }
        
        .payment-method {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 10px;
            width: 120px;
        }
        
        .payment-icon {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            background: var(--light);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 24px;
            color: var(--primary);
        }
        
        /* Footer */
        footer {
            background: var(--dark);
            color: white;
            padding: 60px 0 30px;
        }
        
        .footer-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }
        
        .footer-col h3 {
            font-size: 20px;
            margin-bottom: 20px;
            position: relative;
            padding-bottom: 10px;
        }
        
        .footer-col h3::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 50px;
            height: 2px;
            background: var(--accent);
        }
        
        .footer-links {
            list-style: none;
        }
        
        .footer-links li {
            margin-bottom: 12px;
        }
        
        .footer-links a {
            color: #adb5bd;
            text-decoration: none;
            transition: var(--transition);
        }
        
        .footer-links a:hover {
            color: white;
            padding-left: 5px;
        }
        
        .copyright {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid #495057;
            color: #adb5bd;
            font-size: 14px;
        }
        
        /* Admin Dashboard Modal */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.7);
            z-index: 2000;
            justify-content: center;
            align-items: center;
        }
        
        .modal-content {
            background: white;
            border-radius: 15px;
            width: 90%;
            max-width: 800px;
            max-height: 90vh;
            overflow-y: auto;
            position: relative;
        }
        
        .modal-header {
            background: var(--primary);
            color: white;
            padding: 20px;
            border-radius: 15px 15px 0 0;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .close-modal {
            background: none;
            border: none;
            color: white;
            font-size: 24px;
            cursor: pointer;
        }
        
        .modal-body {
            padding: 30px;
        }
        
        .admin-tabs {
            display: flex;
            border-bottom: 1px solid var(--border);
            margin-bottom: 20px;
        }
        
        .tab {
            padding: 12px 24px;
            cursor: pointer;
            font-weight: 600;
            color: var(--gray);
            border-bottom: 3px solid transparent;
        }
        
        .tab.active {
            color: var(--primary);
            border-bottom-color: var(--accent);
        }
        
        .tab-content {
            display: none;
        }
        
        .tab-content.active {
            display: block;
        }
        
        .user-profile {
            display: flex;
            align-items: center;
            gap: 15px;
            padding: 15px 0;
            border-bottom: 1px solid var(--border);
        }
        
        .user-avatar {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background: var(--light-gray);
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            color: var(--primary);
        }
        
        .user-info h4 {
            font-weight: 600;
        }
        
        .user-info p {
            color: var(--gray);
            font-size: 14px;
        }
        
        .action-buttons {
            display: flex;
            gap: 10px;
        }
        
        .action-btn {
            padding: 5px 12px;
            border-radius: 5px;
            font-size: 12px;
            cursor: pointer;
        }
        
        .edit-btn {
            background: var(--warning);
            color: white;
        }
        
        .delete-btn {
            background: var(--danger);
            color: white;
        }
        
        /* Responsive Design */
        @media (max-width: 992px) {
            .hero h2 {
                font-size: 36px;
            }
        }
        
        @media (max-width: 768px) {
            .header-container {
                flex-direction: column;
                gap: 20px;
            }
            
            nav ul {
                gap: 15px;
                flex-wrap: wrap;
                justify-content: center;
            }
            
            .auth-buttons {
                width: 100%;
                justify-content: center;
            }
            
            .hero h2 {
                font-size: 32px;
            }
            
            .hero p {
                font-size: 16px;
            }
        }
        
        @media (max-width: 576px) {
            nav ul {
                gap: 10px;
            }
            
            .btn {
                padding: 8px 16px;
                font-size: 14px;
            }
            
            .section {
                padding: 60px 0;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container header-container">
            <div class="logo">
                <div class="logo-icon">MG</div>
                <div class="logo-text">
                    <h1>Mrs. Monica Geingos Initiative</h1>
                    <p>Investments Platform</p>
                </div>
            </div>
            <nav>
                <ul>
                    <li><a href="#home">Home</a></li>
                    <li><a href="#plans">Investment Plans</a></li>
                    <li><a href="#testimonials">Testimonials</a></li>
                    <li><a href="#trading">Trading Signals</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
            <div class="auth-buttons">
                <a href="#" class="btn btn-outline" id="loginBtn">Login</a>
                <a href="#" class="btn btn-primary" id="registerBtn">Register</a>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container hero-content">
            <h2>Secure Your Financial Future with Trusted Investment Solutions</h2>
            <p>Join thousands of investors who have already started their journey to financial freedom with our expertly managed investment portfolios.</p>
            <a href="#" class="btn btn-primary">Get Started Today</a>
            <div class="bonus-badge">
                <i class="fas fa-gift"></i> $10 Registration Bonus for New Users!
            </div>
        </div>
    </section>

    <!-- Investment Plans -->
    <section class="section" id="plans">
        <div class="container">
            <div class="section-title">
                <h2>Our Investment Plans</h2>
                <p>Choose the plan that best fits your investment goals and risk tolerance</p>
            </div>
            <div class="plans-container">
                <div class="plan-card">
                    <div class="plan-header">
                        <h3>Starter Plan</h3>
                        <div class="plan-price">5% Daily</div>
                        <p>For 30 days</p>
                    </div>
                    <div class="plan-body">
                        <ul class="plan-features">
                            <li><i class="fas fa-check-circle"></i> Minimum Deposit: $100</li>
                            <li><i class="fas fa-check-circle"></i> Maximum Deposit: $999</li>
                            <li><i class="fas fa-check-circle"></i> Principal Returned</li>
                            <li><i class="fas fa-check-circle"></i> Instant Withdrawals</li>
                            <li><i class="fas fa-check-circle"></i> 24/7 Support</li>
                        </ul>
                        <a href="#" class="btn btn-primary" style="width: 100%;">Select Plan</a>
                    </div>
                </div>
                
                <div class="plan-card">
                    <div class="plan-header">
                        <h3>Professional Plan</h3>
                        <div class="plan-price">8% Daily</div>
                        <p>For 45 days</p>
                    </div>
                    <div cla
