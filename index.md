<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8" />
  <title>Hariharan Ragothaman</title>
  <!-- Link your CSS file if you prefer separate styling -->
  <style>
    /* Just for quick demonstration; move to a separate .css file if desired */
    body {
      margin: 0; 
      padding: 2rem;
      font-family: sans-serif;
      line-height: 1.6;
    }

    .profile-container {
      display: flex;
      justify-content: space-between;
      align-items: flex-start;
      gap: 2rem;
      max-width: 1000px;
      margin: 0 auto;
    }

    /* Left text column */
    .profile-left {
      flex: 1;  /* Expand to fill space */
    }
    .profile-left h1 {
      margin-bottom: 0.2rem;
      font-size: 2.5rem;
    }
    .subtitle {
      color: #888;
      font-size: 1.1rem;
      margin-bottom: 1.5rem;
    }

    /* Right column (photo + contact card + CV button) */
    .profile-right {
      width: 300px;  /* or use flex-basis, etc. */
      flex-shrink: 0;
    }
    .profile-right img {
      width: 100%;
      height: auto;
      border-radius: 8px; /* Slightly rounded corners */
      display: block;
    }
    .contact-card {
      margin-top: 1rem;
      border: 1px solid #ddd;
      border-radius: 8px;
      padding: 1rem;
      font-size: 0.95rem;
    }
    .contact-card p {
      margin: 0.4rem 0;
      display: flex;
      align-items: center;
    }
    .contact-card p::before {
      /* Minimal icon/emoji for demonstration */
      content: "• ";
      margin-right: 0.4rem;
    }
    .cv-button {
      display: inline-block;
      margin-top: 1rem;
      padding: 0.6rem 1rem;
      background-color: #f9f9f9;
      border-radius: 4px;
      text-decoration: none;
      border: 1px solid #ccc;
      color: #333;
      font-weight: 500;
    }
    .cv-button:hover {
      background-color: #eee;
    }

  </style>
</head>
<body>
  <div class="profile-container">

    <!-- Left side -->
    <div class="profile-left">
      <h1>Saloni Potdar</h1>
      <div class="subtitle">Senior AI/ML Manager @ Apple</div>

      <p>
        I work on Natural Language Processing and machine learning research specifically in generative AI, question answering, 
        and conversational AI. I am a Senior AI/ML Manager in the Siri and Search team at Apple leading the query understanding 
        and knowledge graph machine learning initiatives. I have 30+ patents and 20+ papers accepted at top conferences 
        like ACL, EMNLP, NAACL, AAAI, and KDD with over 1000+ citations.
      </p>

      <p>
        Prior to this, I was a Senior Staff Applied Scientist and Engineering Manager at IBM Watson where I designed and developed 
        algorithms for IBM's conversational AI product &mdash; Watson Assistant. I got my Master's degree at the Language 
        Technologies Institute at Carnegie Mellon University in 2014. I was awarded the Women in AI Award &mdash; North America 
        (Special Jury Recognition) in 2023 for my work in AI.
      </p>
    </div>

    <!-- Right side -->
    <div class="profile-right">
      <!-- Profile image -->
      <img src="images/saloni.jpg" alt="Saloni Potdar profile photo">

      <!-- Contact info card -->
      <div class="contact-card">
        <p>saloni.potdar@gmail.com</p>
        <p>s_potdar@apple.com</p>
        <p>Google Scholar</p>
        <p>@saloni_p</p>
      </div>

      <!-- CV button -->
      <a class="cv-button" href="#">CV</a>
    </div>

  </div>
</body>
</html>
