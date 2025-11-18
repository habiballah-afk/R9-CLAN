<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>The R9 - أبطال تونس غير المهزومين</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css">
    <style>
        :root {
            --black: #000000;
            --purple: #9d4edd;
            --white: #ffffff;
            --dark-purple: #7b2cbf;
            --light-purple: #c77dff;
            --gradient: linear-gradient(135deg, var(--purple) 0%, var(--dark-purple) 100%);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background: var(--black);
            color: var(--white);
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* تأثيرات التصميم */
        .glass-effect {
            background: rgba(0, 0, 0, 0.7);
            backdrop-filter: blur(20px);
            border: 1px solid rgba(157, 78, 221, 0.3);
        }

        .purple-glow {
            box-shadow: 0 0 20px rgba(157, 78, 221, 0.4);
        }

        .pulse {
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0% { box-shadow: 0 0 0 0 rgba(157, 78, 221, 0.7); }
            70% { box-shadow: 0 0 0 15px rgba(157, 78, 221, 0); }
            100% { box-shadow: 0 0 0 0 rgba(157, 78, 221, 0); }
        }

        /* شريط التقدم */
        .progress-container {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 4px;
            background: transparent;
            z-index: 1001;
        }

        .progress-bar {
            height: 4px;
            background: var(--gradient);
            width: 0%;
            transition: width 0.3s ease;
        }

        /* التصميم العام */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* الهيدر */
        header {
            background: rgba(0, 0, 0, 0.95);
            padding: 1.2rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            border-bottom: 2px solid var(--purple);
            transition: all 0.3s ease;
        }

        header.scrolled {
            padding: 0.8rem 0;
            background: rgba(0, 0, 0, 0.98);
            backdrop-filter: blur(10px);
        }

        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .logo-text {
            font-size: 2.2rem;
            font-weight: bold;
            color: var(--purple);
            text-shadow: 0 0 15px var(--purple);
        }

        .logo-badge {
            background: var(--purple);
            color: var(--white);
            padding: 8px 15px;
            border-radius: 25px;
            font-size: 0.9rem;
            font-weight: bold;
            animation: pulse 2s infinite;
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 2.5rem;
        }

        nav a {
            color: var(--white);
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s;
            padding: 8px 16px;
            border-radius: 8px;
            position: relative;
            font-size: 1.1rem;
        }

        nav a::before {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--purple);
            transition: width 0.3s;
        }

        nav a:hover {
            color: var(--purple);
        }

        nav a:hover::before {
            width: 100%;
        }

        /* قائمة الجوال */
        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            color: var(--white);
            font-size: 1.8rem;
            cursor: pointer;
            padding: 5px;
            z-index: 1002;
        }

        .mobile-menu {
            display: none;
            position: fixed;
            top: 0;
            right: 0;
            width: 80%;
            height: 100vh;
            background: rgba(0, 0, 0, 0.98);
            z-index: 2000;
            padding: 2rem;
            transform: translateX(100%);
            transition: transform 0.3s ease;
            overflow-y: auto;
            backdrop-filter: blur(10px);
        }

        .mobile-menu.active {
            transform: translateX(0);
        }

        .mobile-menu-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 2rem;
            padding-bottom: 1rem;
            border-bottom: 1px solid var(--purple);
        }

        .mobile-menu-close {
            background: none;
            border: none;
            color: var(--white);
            font-size: 1.8rem;
            cursor: pointer;
        }

        .mobile-nav ul {
            list-style: none;
        }

        .mobile-nav li {
            margin-bottom: 1.5rem;
        }

        .mobile-nav a {
            color: var(--white);
            text-decoration: none;
            font-size: 1.3rem;
            font-weight: 600;
            display: block;
            padding: 10px 0;
            border-bottom: 1px solid rgba(157, 78, 221, 0.2);
            transition: all 0.3s;
        }

        .mobile-nav a:hover {
            color: var(--purple);
            padding-right: 10px;
        }

        /* البانر الرئيسي */
        .hero {
            background: 
                radial-gradient(circle at 20% 50%, rgba(157, 78, 221, 0.1) 0%, transparent 50%),
                radial-gradient(circle at 80% 20%, rgba(157, 78, 221, 0.05) 0%, transparent 50%),
                var(--black);
            height: 100vh;
            display: flex;
            align-items: center;
            text-align: center;
            margin-top: 80px;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: 
                linear-gradient(45deg, transparent 65%, rgba(157, 78, 221, 0.03) 75%, transparent 85%),
                linear-gradient(-45deg, transparent 65%, rgba(157, 78, 221, 0.03) 75%, transparent 85%);
        }

        .clan-slogan {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            font-size: 9rem;
            font-weight: 900;
            color: transparent;
            -webkit-text-stroke: 2px rgba(157, 78, 221, 0.15);
            z-index: 1;
            opacity: 0.4;
            white-space: nowrap;
            letter-spacing: 15px;
            font-family: 'Arial Black', sans-serif;
        }

        .hero-content {
            position: relative;
            z-index: 2;
            width: 100%;
        }

        .hero-content h1 {
            font-size: 4.5rem;
            margin-bottom: 1.5rem;
            color: var(--purple);
            text-shadow: 0 0 20px var(--purple);
            letter-spacing: 3px;
            font-weight: 800;
        }

        .hero-content .subtitle {
            font-size: 1.6rem;
            margin-bottom: 3rem;
            color: var(--white);
            max-width: 700px;
            margin-left: auto;
            margin-right: auto;
            line-height: 1.8;
            font-weight: 300;
        }

        .stats {
            display: flex;
            justify-content: center;
            gap: 4rem;
            margin: 3rem 0;
        }

        .stat-item {
            text-align: center;
            background: rgba(0, 0, 0, 0.8);
            padding: 2rem;
            border-radius: 20px;
            border: 2px solid var(--purple);
            transition: all 0.3s;
            min-width: 180px;
            backdrop-filter: blur(10px);
        }

        .stat-item:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(157, 78, 221, 0.3);
        }

        .stat-number {
            font-size: 3rem;
            font-weight: 800;
            color: var(--purple);
            display: block;
            text-shadow: 0 0 15px var(--purple);
            margin-bottom: 0.5rem;
        }

        .stat-label {
            font-size: 1.1rem;
            color: var(--white);
            font-weight: 500;
        }

        /* زر العودة للأعلى */
        .back-to-top {
            position: fixed;
            bottom: 30px;
            left: 30px;
            width: 50px;
            height: 50px;
            background: var(--gradient);
            color: white;
            border: none;
            border-radius: 50%;
            font-size: 1.5rem;
            cursor: pointer;
            z-index: 999;
            opacity: 0;
            visibility: hidden;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(157, 78, 221, 0.4);
        }

        .back-to-top.visible {
            opacity: 1;
            visibility: visible;
        }

        .back-to-top:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(157, 78, 221, 0.6);
        }

        /* الأقسام العامة */
        .section {
            padding: 6rem 0;
            position: relative;
        }

        .section::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 1px;
            background: linear-gradient(90deg, transparent, var(--purple), transparent);
        }

        .section-title {
            text-align: center;
            font-size: 3.2rem;
            margin-bottom: 4rem;
            color: var(--purple);
            position: relative;
            text-shadow: 0 0 20px var(--purple);
            letter-spacing: 2px;
            font-weight: 800;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: -20px;
            left: 50%;
            transform: translateX(-50%);
            width: 200px;
            height: 4px;
            background: var(--purple);
            box-shadow: 0 0 20px var(--purple);
        }

        /* قسم عن الكلان */
        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: center;
        }

        .about-text {
            font-size: 1.2rem;
            background: rgba(0, 0, 0, 0.8);
            padding: 3rem;
            border-radius: 25px;
            border: 2px solid var(--purple);
            line-height: 1.8;
            backdrop-filter: blur(15px);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.5);
        }

        .philosophy-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2.5rem;
            margin-top: 3rem;
        }

        .philosophy-item {
            background: rgba(0, 0, 0, 0.8);
            padding: 3rem 2rem;
            border-radius: 20px;
            text-align: center;
            border: 2px solid var(--purple);
            transition: all 0.3s;
            backdrop-filter: blur(15px);
            position: relative;
            overflow: hidden;
        }

            });
        });
