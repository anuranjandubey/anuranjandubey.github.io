---
title: About
layout: page
---

<html>
<head>
    <style>
        :root {
            /* Color variables for dark mode */
            --indigo-50: #1c1b29;
            --indigo-100: #25233d;
            --indigo-200: #373352;
            --indigo-300: #4a4770;
            --indigo-400: #5e5c8e;
            --indigo-500: #7472aa;
            --indigo-600: #908bc0;
            --indigo-700: #b2a4db;
            --indigo-800: #cec3f1;
            --indigo-900: #e8e3ff;

            --text-color: #e0e0e0;
            --background-color: #121212;
            --card-background: #1f1f1f;
            --highlight-background: #282828;
            --border-color: #3a3a3a;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
            line-height: 1.6;
            color: var(--text-color);
            max-width: 1200px;
            margin: 0 auto;
            padding: 2rem;
            background-color: var(--background-color);
        }

        /* Hero section */
        .hero {
            text-align: center;
            margin-bottom: 4rem;
            padding: 2rem;
            background: var(--card-background);
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.5);
            border: 1px solid var(--border-color);
        }

        .hero img {
            border-radius: 50%;
            max-width: 200px;
            margin: 0 auto 1.5rem;
            display: block;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.7);
            border: 3px solid var(--indigo-200);
        }

        /* Section styling */
        h1 {
            color: var(--indigo-900);
            font-size: 2.5rem;
            margin-bottom: 1.5rem;
            border-bottom: 3px solid var(--indigo-500);
            padding-bottom: 0.5rem;
        }

        h2 {
            color: var(--indigo-700);
            font-size: 1.8rem;
            margin-top: 2.5rem;
        }

        h3 {
            color: var(--indigo-600);
            font-size: 1.4rem;
            margin-top: 0;
        }

        /* Experience cards */
        .experience-card {
            background: var(--card-background);
            border-radius: 8px;
            padding: 1.5rem;
            margin-bottom: 1.5rem;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.5);
            border: 1px solid var(--border-color);
            transition: transform 0.2s ease;
            display: flex;
            align-items: flex-start;
            gap: 1.5rem;
        }

        .experience-card:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.7);
        }

        .company-logo {
            width: 80px;
            height: 80px;
            object-fit: contain;
            margin-top: 0.5rem;
        }

        .experience-content {
            flex: 1;
        }

        /* Skills grid */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1.5rem;
            margin: 2rem 0;
        }

        .skill-category {
            background: var(--card-background);
            padding: 1.5rem;
            border-radius: 8px;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.5);
            border: 1px solid var(--border-color);
        }

        /* Badge styling */
        .badge {
            display: inline-block;
            padding: 0.25rem 0.75rem;
            background-color: var(--indigo-200);
            color: var(--indigo-900);
            border-radius: 9999px;
            font-size: 0.875rem;
            margin: 0.25rem;
        }

        /* Education cards */
        .education-card {
            background: var(--card-background);
            border-radius: 8px;
            padding: 1.5rem;
            margin-bottom: 1.5rem;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.5);
            border: 1px solid var(--border-color);
            border-left: 4px solid var(--indigo-500);
            transition: transform 0.2s ease;
        }

        .education-card:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.7);
        }

        .education-meta {
            color: var(--indigo-600);
            font-size: 0.9rem;
            margin-bottom: 0.5rem;
        }

        .gpa {
            display: inline-block;
            padding: 0.25rem 0.75rem;
            background-color: var(--indigo-200);
            color: var(--indigo-900);
            border-radius: 9999px;
            font-size: 0.875rem;
            margin: 0.5rem 0;
        }

        /* Interests section */
        .interests {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 1rem;
            margin: 2rem 0;
        }

        .interest-item {
            background: var(--card-background);
            padding: 1rem;
            border-radius: 8px;
            text-align: center;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.5);
            border: 1px solid var(--border-color);
            transition: transform 0.2s ease;
        }

        .interest-item:hover {
            transform: translateY(-2px);
            background-color: var(--highlight-background);
        }

        /* Highlight boxes */
        .highlight {
            background: var(--highlight-background);
            padding: 1.5rem;
            border-radius: 8px;
            margin: 1.5rem 0;
            border-left: 4px solid var(--indigo-500);
        }

        /* Links styling */
        a {
            color: var(--indigo-600);
            text-decoration: none;
            transition: color 0.3s ease;
        }

        a:hover {
            color: var(--indigo-400);
            text-decoration: underline;
        }

        .certificate-link {
            display: inline-flex;
            align-items: center;
            padding: 0.5rem 1rem;
            background-color: var(--highlight-background);
            color: var(--indigo-900);
            border-radius: 6px;
            margin-top: 1rem;
            transition: background-color 0.2s ease;
        }

        .certificate-link:hover {
            background-color: var(--indigo-100);
            text-decoration: none;
        }

        .course-logo {
        width: 80px;   /* Reduced from 60px */
        height: 80px;  /* Reduced from 60px */
        object-fit: contain; /* Maintains aspect ratio */
        }

        .course-header {
        display: flex;
        align-items: center;
        gap: 0.75rem;  /* Reduced spacing between logo and text */
        }

        img[src*="ucsan"], 
        img[src*="microicon"],
        img[src*="coursera"],
        img[src*="React-logo"],
        img[src*="forage"],
        img[src*="edx"] {
            width: 80px;
            height: 80px;
            object-fit: contain;
        }
        
        @media (max-width: 768px) {
        .course-logo {
            width: 80px;
            height: 80px;
        }
        }

        .section-divider {
        height: 1px;
        background: linear-gradient(
            to right,
            var(--border-dark),
            var(--indigo-400),
            var(--border-dark)
        );
        margin: 3rem 0;
        position: relative;
    }

    /* Fancy separator with icon or dot */
    .section-divider.fancy {
        height: 1px;
        background: linear-gradient(
            to right,
            var(--border-dark),
            var(--indigo-400),
            var(--border-dark)
        );
        margin: 3rem 0;
        position: relative;
    }

    .section-divider.fancy::before {
        content: "•";
        color: var(--indigo-400);
        background-color: var(--bg-dark);
        position: absolute;
        left: 50%;
        top: 50%;
        transform: translate(-50%, -50%);
        padding: 0 1rem;
        font-size: 1.5rem;
    }

    /* Alternative separator with multiple dots */
    .section-divider.dots {
        height: 1px;
        background: var(--border-dark);
        margin: 3rem 0;
        position: relative;
        text-align: center;
    }

    .section-divider.dots::before {
        content: "• • •";
        color: var(--indigo-400);
        background-color: var(--bg-dark);
        position: absolute;
        left: 50%;
        top: 50%;
        transform: translate(-50%, -50%);
        padding: 0 1rem;
        letter-spacing: 0.5rem;
    }

    /* Responsive adjustments */
    @media (max-width: 768px) {
        .section-divider {
            margin: 2rem 0;
        }
    }
    </style>
</head>
<body>

# About Me

<div class="hero">
    <img src="/assets/images/profilefull.jpeg" alt="Profile Picture">
    <h1>I'm Always Up to Learn New Things</h1>
    <p class="highlight">Software Developer | Machine Learning Enthusiast | Graduate Student at ASU</p>
</div>

<div class="highlight">
I'm a software developer pursuing my Master's in Computer Science at Arizona State University. Throughout my academic journey, I've worked with cutting-edge technologies including AWS, Git, MSSQL, Apache Kafka, MongoDB, and OpenCV. My passion lies in creating innovative solutions and exploring the frontiers of technology.
</div>

<div class="highlight">
I worked on a research paper on classifying defects in glass bangles, published at CVIP 2022 Conference and featured in Springer's CCIS Series. This project combined traditional feature-based approaches with deep learning techniques, showcasing my ability to bridge classical and modern methodologies.
</div>

<div class="highlight">
I've recently embarked on a fitness journey, recognizing that a healthy body and mind pave the way for success. Beyond coding, I'm an enthusiast of food, coffee, and a budding bibliophile. A recent read, "Atomic Habits" by James Clear, has significantly impacted my daily productivity.
</div>

<div class="section-divider"></div>

<h1>Work Experience</h1>

<div class="experience-card">
    <img class="company-logo" src="/assets/images/intuit.png" alt="Intuit Logo">
    <div class="experience-content">
        <h3>Intuit</h3>
        <p><strong>Software Engineering Intern</strong></p>
        <p class="education-meta">May 2024 - Aug 2024</p>
    </div>
</div>

<div class="experience-card">
    <img class="company-logo" src="/assets/images/genpacticon.png" alt="Genpact Logo">
    <div class="experience-content">
        <h3>Genpact</h3>
        <p><strong>Senior Associate (Data Engineering)</strong></p>
        <p class="education-meta">June 2021 - May 2023</p>
    </div>
</div>

<div class="experience-card">
    <img class="company-logo" src="/assets/images/filedicon.png" alt="Filed Logo">
    <div class="experience-content">
        <h3>Filed</h3>
        <p><strong>Software Developer</strong></p>
        <p class="education-meta">April 2021 - June 2021</p>
        <p>Delivered 3 Integration for Ecommerce platforms for Product Catalogue Import.</p>
    </div>
</div>

<div class="experience-card">
    <img class="company-logo" src="/assets/images/tsficon.png" alt="The Sparks Foundation Logo">
    <div class="experience-content">
        <h3>The Sparks Foundation</h3>
        <p><strong>Data Analyst (GRIP)</strong></p>
        <p class="education-meta">August 2020</p>
        <p>Worked on a Data Analysis Project using seaborn and matplotlib.</p>
    </div>
</div>


<div class="section-divider dots"></div>

<h1>Education</h1>

<div class="education-card">
    <h3>Arizona State University</h3>
    <div class="education-meta">Aug 2023 - Aug 2025</div>
    <p><strong>Master of Science in Computer Science</strong></p>
    <div class="gpa">GPA: 4.22/4</div>
</div>

<div class="education-card">
    <h3>Jaypee Institute of Information Technology</h3>
    <div class="education-meta">July 2017 - July 2021</div>
    <p><strong>Bachelor of Technology, Computer Science and Engineering</strong></p>
    <div class="gpa">GPA: 7.3/10</div>
    <p><strong>Activities:</strong> Table Tennis Captain</p>
</div>

<div class="education-card">
    <h3>Kendriya Vidyalaya, Aligarh</h3>
    <div class="education-meta">May 2015 - May 2016</div>
    <p><strong>Intermediate (12th)</strong></p>
    <p>Science Stream with 80% Overall</p>
    <p>Second Topper, Highest Marks in Computer Science and Chemistry</p>
    <p><strong>Activities:</strong> School Captain, House Captain</p>
</div>

<div class="education-card">
    <h3>Kendriya Vidyalaya, Aligarh</h3>
    <div class="education-meta">May 2013 - May 2014</div>
    <p><strong>High School (10th)</strong></p>
    <div class="gpa">CGPA: 10/10</div>
    <p>All India Topper with Merit Certificate in All Subjects</p>
</div>



<div class="section-divider dots"></div>
<h1>Technical Knowledge</h1>

<div class="skills-container">
    <div class="skills-section">
        <h3>Applications & Platforms</h3>
        <div class="skills-badges">
            <span class="badge">Docker</span>
            <span class="badge">POSTMAN</span>
            <span class="badge">GraphQL</span>
            <span class="badge">Fast-API</span>
            <span class="badge">AWS (EC2)</span>
            <span class="badge">Git</span>
            <span class="badge">MSSQL</span>
            <span class="badge">CyberArk</span>
        </div>
    </div>

    <div class="skills-section">
        <h3>Languages</h3>
        <div class="skills-badges">
            <span class="badge">Python</span>
            <span class="badge">C/C++</span>
            <span class="badge">JavaScript</span>
            <span class="badge">SQL</span>
            <span class="badge">PL/SQL</span>
            <span class="badge">HTML</span>
            <span class="badge">LaTeX</span>
            <span class="badge">Assembly</span>
        </div>
    </div>

    <div class="skills-section">
        <h3>Machine Learning</h3>
        <div class="skills-badges">
            <span class="badge">NLP</span>
            <span class="badge">OpenCV</span>
            <span class="badge">Image Processing</span>
            <span class="badge">TensorFlow</span>
            <span class="badge">Regex</span>
            <span class="badge">Classification</span>
            <span class="badge">Regression</span>
        </div>
    </div>

    <div class="skills-section">
        <h3>Web & App Development</h3>
        <div class="skills-badges">
            <span class="badge">HTML</span>
            <span class="badge">CSS</span>
            <span class="badge">JavaScript</span>
            <span class="badge">PHP</span>
            <span class="badge">React-Native</span>
            <span class="badge">Flutter</span>
        </div>
    </div>

    <div class="skills-section">
        <h3>Operating Systems</h3>
        <div class="skills-badges">
            <span class="badge">Mac-OSX</span>
            <span class="badge">Linux</span>
            <span class="badge">Windows</span>
            <span class="badge">Android</span>
        </div>
    </div>
</div>

<div class="section-divider dots"></div>

<h1>Courses and Certifications</h1>

<div class="course-grid">
    <div class="course-card">
        <div class="course-header">
            <img src="/assets/images/ucsan.png" alt="UC San Diego" class="course-logo">
            <div class="course-meta">
                <div class="course-date">Sep 2022 - July 2023</div>
                <h3>Data Science MicroMasters® Program</h3>
            </div>
        </div>
        <p>Python for Data Science, Probability and Statistics, Machine Learning Fundamentals, Big Data Analytics Using Spark</p>
    </div>

    <div class="course-card">
        <div class="course-header">
            <img src="/assets/images/microicon.png" alt="Microsoft" class="course-logo">
            <div class="course-meta">
                <div class="course-date">July 2020</div>
                <h3>Engineering Virtual Internship</h3>
            </div>
        </div>
        <p>Business Foundation Skills, Work Ready Skills, Technical Engineer Skills</p>
        <a href="https://insidesherpa.s3.amazonaws.com/completion-certificates/Microsoft/ms2CK9b2SCWGXwPMS_Microsoft_sbFYPrpDyhAkFiFii_completion_certificate.pdf" class="certificate-link">View Certificate →</a>
    </div>

    <div class="course-card">
        <div class="course-header">
            <img src="/assets/images/React-logo.png" alt="React" class="course-logo">
            <div class="course-meta">
                <div class="course-date">June 2020</div>
                <h3>React Native The Practical Guide</h3>
            </div>
        </div>
        <p>Comprehensive course on React Native development</p>
        <a href="https://www.udemy.com/certificate/UC-6ad58f28-3b90-4700-8831-cf06c9bd71fb/" class="certificate-link">View Certificate →</a>
    </div>

    <div class="course-card">
        <div class="course-header">
            <img src="/assets/images/coursera-logo-square.png" alt="Coursera" class="course-logo">
            <div class="course-meta">
                <div class="course-date">July 2019</div>
                <h3>Machine Learning by Andrew Ng</h3>
            </div>
        </div>
        <p>Stanford University Course on Machine Learning Fundamentals</p>
        <a href="https://www.coursera.org/account/accomplishments/verify/TME8CTEUJK5E" class="certificate-link">View Certificate →</a>
    </div>
</div>

<div class="section-divider dots"></div>

<h1>Interests</h1>

<div class="interests">
    <div class="interest-item">Competitive Programming</div>
    <div class="interest-item">Automobiles</div>
    <div class="interest-item">Music and Art</div>
    <div class="interest-item">Genetic Technologies</div>
    <div class="interest-item">Brain Interface Technologies</div>
    <div class="interest-item">Machine Learning</div>
</div>

[Back to Top ↑](#top)

</body>
</html>