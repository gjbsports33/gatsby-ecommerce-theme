<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>GJB Sports – Baseball & Softball Training</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <style>
    :root {
      --gjb-red: #c62828;
      --gjb-black: #111111;
      --gjb-light: #f7f7f7;
      --gjb-gray: #e0e0e0;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI",
        sans-serif;
      background: #ffffff;
      color: #111111;
      line-height: 1.6;
    }

    a {
      text-decoration: none;
      color: inherit;
    }

    /* HEADER & NAV */

    header {
      background: var(--gjb-black);
      color: #ffffff;
      position: sticky;
      top: 0;
      z-index: 1000;
    }

    .nav-wrapper {
      max-width: 1100px;
      margin: 0 auto;
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 0.4rem 1rem;
    }

    .logo-wrap {
      display: flex;
      align-items: center;
      gap: 0.6rem;
    }

    .logo-wrap img {
      height: 52px;
      width: 52px;
      object-fit: contain;
      border-radius: 50%;
      background: #ffffff;
      padding: 4px;
    }

    .logo-text {
      font-weight: 700;
      letter-spacing: 0.04em;
      font-size: 1.05rem;
    }

    nav ul {
      list-style: none;
      display: flex;
      gap: 1rem;
      font-size: 0.95rem;
    }

    nav a {
      padding: 0.35rem 0.6rem;
      border-radius: 999px;
      transition: background 0.2s ease, color 0.2s ease;
    }

    nav a:hover {
      background: #ffffff;
      color: var(--gjb-black);
    }

    /* HERO */

    .hero {
      background: linear-gradient(
          rgba(0, 0, 0, 0.6),
          rgba(0, 0, 0, 0.7)
        ),
        url("https://images.pexels.com/photos/1467181/pexels-photo-1467181.jpeg?auto=compress&cs=tinysrgb&w=1600")
          center/cover no-repeat;
      color: #ffffff;
      padding: 4.5rem 1.25rem;
      text-align: center;
    }

    .hero-inner {
      max-width: 850px;
      margin: 0 auto;
    }

    .hero h1 {
      font-size: 2.4rem;
      letter-spacing: 0.08em;
      margin-bottom: 0.75rem;
    }

    .hero p {
      font-size: 1.05rem;
      margin-bottom: 1.5rem;
    }

    .hero-buttons {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 0.75rem;
    }

    .btn {
      border-radius: 999px;
      padding: 0.7rem 1.4rem;
      border: none;
      cursor: pointer;
      font-weight: 600;
      font-size: 0.95rem;
      display: inline-block;
      transition: transform 0.1s ease, box-shadow 0.1s ease, background 0.2s;
      text-align: center;
    }

    .btn-primary {
      background: var(--gjb-red);
      color: #ffffff;
    }

    .btn-secondary {
      background: #ffffff;
      color: var(--gjb-black);
    }

    .btn-outline {
      background: transparent;
      border: 1px solid #ffffff;
      color: #ffffff;
    }

    .btn:hover {
      transform: translateY(-1px);
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.18);
    }

    /* LAYOUT */

    main {
      max-width: 1100px;
      margin: 0 auto;
      padding: 2.5rem 1.25rem 3.5rem;
    }

    section {
      margin-bottom: 3rem;
    }

    section h2 {
      font-size: 1.6rem;
      letter-spacing: 0.08em;
      text-transform: uppercase;
      margin-bottom: 1.25rem;
      position: relative;
      padding-bottom: 0.4rem;
    }

    section h2::after {
      content: "";
      position: absolute;
      left: 0;
      bottom: 0;
      width: 60px;
      height: 3px;
      background: var(--gjb-red);
    }

    .section-subtitle {
      color: #555;
      margin-bottom: 1.3rem;
      font-size: 0.95rem;
    }

    /* LESSONS */

    .lessons-grid {
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
      gap: 1.5rem;
    }

    .coach-card {
      background: var(--gjb-light);
      border-radius: 12px;
      padding: 1.25rem;
      display: flex;
      flex-direction: column;
      gap: 0.8rem;
    }

    .coach-header {
      display: flex;
      gap: 1rem;
      align-items: center;
    }

    .coach-photo {
      width: 80px;
      height: 80px;
      border-radius: 50%;
      background: #ccc;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 0.75rem;
      text-transform: uppercase;
      color: #555;
    }

    .coach-name {
      font-size: 1.1rem;
      font-weight: 700;
    }

    .coach-role {
      font-size: 0.9rem;
      color: #666;
    }

    .coach-details {
      font-size: 0.9rem;
      color: #444;
    }

    .lesson-meta {
      display: flex;
      flex-wrap: wrap;
      gap: 0.4rem 0.8rem;
      font-size: 0.85rem;
      color: #555;
    }

    .lesson-meta span {
      background: #ffffff;
      border-radius: 999px;
      padding: 0.2rem 0.6rem;
      border: 1px solid #ddd;
    }

    /* PARTIES & CAGES */

    .flex-two {
      display: grid;
      grid-template-columns: minmax(0, 1.3fr) minmax(0, 1fr);
      gap: 1.8rem;
    }

    .card {
      background: var(--gjb-light);
      border-radius: 12px;
      padding: 1.25rem 1.3rem;
    }

    .card h3 {
      margin-bottom: 0.75rem;
      font-size: 1.1rem;
    }

    .card p {
      font-size: 0.9rem;
      margin-bottom: 0.75rem;
    }

    .card-list {
      font-size: 0.9rem;
      margin-left: 1.1rem;
      margin-bottom: 0.75rem;
    }

    .card-list li {
      margin-bottom: 0.25rem;
    }

    .pricing-table {
      width: 100%;
      border-collapse: collapse;
      font-size: 0.9rem;
      margin-bottom: 0.85rem;
    }

    .pricing-table th,
    .pricing-table td {
      border: 1px solid var(--gjb-gray);
      padding: 0.45rem 0.6rem;
      text-align: left;
    }

    .pricing-table th {
      background: #ffffff;
    }

    /* SHOP */

    .shop-grid {
      display: grid;
      grid-template-columns: repeat(3, minmax(0, 1fr));
      gap: 1rem;
    }

    .shop-item {
      border-radius: 10px;
      border: 1px solid var(--gjb-gray);
      padding: 0.9rem;
      display: flex;
      flex-direction: column;
      gap: 0.35rem;
      font-size: 0.9rem;
    }

    .shop-item-img {
      background: var(--gjb-light);
      height: 120px;
      border-radius: 8px;
      margin-bottom: 0.4rem;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 0.75rem;
      color: #777;
      text-transform: uppercase;
    }

    .shop-price {
      font-weight: 700;
      margin-top: 0.25rem;
    }

    /* GALLERY */

    .gallery-grid {
      display: grid;
      grid-template-columns: repeat(4, minmax(0, 1fr));
      gap: 0.75rem;
    }

    .gallery-item {
      background: #ddd;
      height: 130px;
      border-radius: 8px;
      overflow: hidden;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 0.8rem;
      color: #555;
      text-transform: uppercase;
    }

    /* CONTACT */

    .contact-grid {
      display: grid;
      grid-template-columns: minmax(0, 1.1fr) minmax(0, 1fr);
      gap: 1.6rem;
    }

    form {
      display: grid;
      gap: 0.75rem;
    }

    label {
      font-size: 0.86rem;
      font-weight: 600;
    }

    input,
    textarea,
    select {
      width: 100%;
      padding: 0.55rem 0.6rem;
      border-radius: 6px;
      border: 1px solid #ccc;
      font: inherit;
    }

    textarea {
      min-height: 110px;
      resize: vertical;
    }

    .contact-info {
      font-size: 0.9rem;
    }

    .contact-info p {
      margin-bottom: 0.4rem;
    }

    .contact-info strong {
      display: inline-block;
      min-width: 80px;
    }

    footer {
      background: var(--gjb-black);
      color: #ffffff;
      font-size: 0.8rem;
      text-align: center;
      padding: 0.9rem 0.5rem;
    }

    /* RESPONSIVE */

    @media (max-width: 900px) {
      .lessons-grid,
      .flex-two,
      .shop-grid,
      .gallery-grid,
      .contact-grid {
        grid-template-columns: 1fr;
      }
      .gallery-grid {
        grid-template-columns: repeat(2, minmax(0, 1fr));
      }
    }

    @media (max-width: 720px) {
      .nav-wrapper {
        flex-direction: column;
        align-items: flex-start;
        gap: 0.35rem;
      }
      nav ul {
        flex-wrap: wrap;
        row-gap: 0.35rem;
      }
      .hero h1 {
        font-size: 2rem;
      }
    }

    @media (max-width: 480px) {
      .hero {
        padding: 3rem 1rem;
      }
      .hero-buttons {
        flex-direction: column;
        align-items: stretch;
      }
      .gallery-grid {
        grid-template-columns: 1fr;
      }
    }
  </style>
</head>
<body>
  <!-- HEADER / NAV -->
  <header>
    <div class="nav-wrapper">
      <div class="logo-wrap">
        <!-- Replace src with your logo path -->
        <img src="images/gjb-logo.png" alt="GJB Sports logo" />
        <div class="logo-text">GJB SPORTS</div>
      </div>
      <nav>
        <ul>
          <li><a href="#home">Home</a></li>
          <li><a href="#lessons">Lessons</a></li>
          <li><a href="#parties">Parties &amp; Events</a></li>
          <li><a href="#cages">Cage Rentals</a></li>
          <li><a href="#shop">Shop</a></li>
          <li><a href="#gallery">Gallery</a></li>
          <li><a href="#contact">Contact</a></li>
        </ul>
      </nav>
    </div>
  </header>

  <!-- HERO -->
  <section id="home" class="hero">
    <div class="hero-inner">
      <h1>BASEBALL &amp; SOFTBALL TRAINING</h1>
      <p>
        High-energy, fundamentals-first instruction for athletes of all ages in
        a positive, competitive environment.
      </p>
      <div class="hero-buttons">
        <a href="#lessons" class="btn btn-primary">Book a Lesson</a>
        <a href="#cages" class="btn btn-secondary">Rent a Cage</a>
        <a href="#parties" class="btn btn-outline">Parties &amp; Events</a>
      </div>
    </div>
  </section>

  <main>
    <!-- LESSONS -->
    <section id="lessons">
      <h2>Lessons</h2>
      <p class="section-subtitle">
        One-on-one and small-group training with experienced coaches focused on
        hitting, pitching, fielding, catching and overall confidence.
      </p>

      <div class="lessons-grid">
        <!-- COACH JOSE -->
        <article class="coach-card">
          <div class="coach-header">
            <div class="coach-photo">Coach Photo</div>
            <!-- Replace with real photo later -->
            <div>
              <div class="coach-name">Coach Jose</div>
              <div class="coach-role">Baseball &amp; Softball Instructor</div>
            </div>
          </div>
          <p class="coach-details">
            Specializes in hitting, infield/outfield defense, and game IQ.
            Focus on mechanics, approach at the plate, and position-specific
            work tailored to each athlete.
          </p>
          <div class="lesson-meta">
            <span>Private &amp; Small Group</span>
            <span>Baseball &amp; Softball</span>
            <span>All Ages</span>
          </div>
          <!-- TODO: Link this button to your booking system (Calendly, etc.) -->
          <a href="#contact" class="btn btn-primary"
            >Book Lesson with Coach Jose</a
          >
        </article>

        <!-- COACH AMANDA -->
        <article class="coach-card">
          <div class="coach-header">
            <div class="coach-photo">Coach Photo</div>
            <!-- Replace with real photo later -->
            <div>
              <div class="coach-name">Coach Amanda</div>
              <div class="coach-role">Softball &amp; Baseball Instructor</div>
            </div>
          </div>
          <p class="coach-details">
            Specializes in softball hitting, slapping, pitching and catching.
            Emphasis on confidence, leadership, and competitive game
            preparation.
          </p>
          <div class="lesson-meta">
            <span>Softball Specialist</span>
            <span>Hitting &amp; Pitching</span>
            <span>Youth–High School</span>
          </div>
          <!-- TODO: Link this button to your booking system -->
          <a href="#contact" class="btn btn-primary"
            >Book Lesson with Coach Amanda</a
          >
        </article>
      </div>
    </section>

    <!-- PARTIES & CAGE RENTALS -->
    <section id="parties">
      <h2>Parties &amp; Events</h2>
      <p class="section-subtitle">
        Host your next birthday, team party, or special event at GJB Sports.
      </p>

      <div class="flex-two">
        <!-- PARTIES CARD -->
        <article class="card">
          <h3>Baseball &amp; Softball Parties</h3>
          <p>
            Celebrate with games, contests, and cage time run by our coaches.
            Perfect for birthdays, team celebrations, and group outings.
          </p>
          <ul class="card-list">
            <li>90–120 minute party packages</li>
            <li>Guided drills, games &amp; competitions</li>
            <li>Use of cages &amp; turf space</li>
            <li>Bring your own food, cake &amp; decorations</li>
          </ul>
          <!-- TODO: Set your real email in the mailto below -->
          <a
            href="mailto:info@gjbsports.com?subject=Party%20Request"
            class="btn btn-primary"
            >Contact Us About a Party</a
          >
        </article>

        <!-- CAGE RENTAL PREVIEW -->
        <article id="cages" class="card">
          <h3>Cage Rentals</h3>
          <p>
            Reserve a batting cage for individual work, small groups, or full
            team practices.
          </p>
          <table class="pricing-table">
            <thead>
              <tr>
                <th>Duration</th>
                <th>Price</th>
                <th>Notes</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td>30 Minutes</td>
                <td>$XX</td>
                <td>Individual / Small Group</td>
              </tr>
              <tr>
                <td>60 Minutes</td>
                <td>$XX</td>
                <td>Great for 1–4 athletes</td>
              </tr>
              <tr>
                <td>Team Practice (90+ min)</td>
                <td>$XX</td>
                <td>Contact for team rates</td>
              </tr>
            </tbody>
          </table>
          <!-- TODO: Link to actual cage booking OR email -->
          <a
            href="mailto:info@gjbsports.com?subject=Cage%20Rental%20Request"
            class="btn btn-secondary"
            >Request Cage Time</a
          >
        </article>
      </div>
    </section>

    <!-- SHOP -->
    <section id="shop">
      <h2>Shop</h2>
      <p class="section-subtitle">
        Gear coming soon! Use this section to list bats, gloves, apparel and
        other items for sale.
      </p>

      <div class="shop-grid">
        <!-- SAMPLE ITEMS – replace with real ones later -->
        <article class="shop-item">
          <div class="shop-item-img">Product Image</div>
          <strong>GJB Sports T-Shirt</strong>
          <p>Comfortable, athletic-fit tee available in youth &amp; adult sizes.</p>
          <div class="shop-price">$XX.XX</div>
          <button class="btn btn-primary" type="button">Add to Cart (coming soon)</button>
        </article>

        <article class="shop-item">
          <div class="shop-item-img">Product Image</div>
          <strong>GJB Sports Hat</strong>
          <p>Structured cap perfect for practice, games, and everyday wear.</p>
          <div class="shop-price">$XX.XX</div>
          <button class="btn btn-primary" type="button">Add to Cart (coming soon)</button>
        </article>

        <article class="shop-item">
          <div class="shop-item-img">Product Image</div>
          <strong>Batting Gloves</strong>
          <p>High-grip gloves designed for comfort and durability.</p>
          <div class="shop-price">$XX.XX</div>
          <button class="btn btn-primary" type="button">Add to Cart (coming soon)</button>
        </article>
      </div>

      <p style="font-size: 0.85rem; margin-top: 0.75rem; color: #555;">
        <!-- Instruction for you -->
        When you're ready, you can replace these sample items with your real products,
        prices, and links to an online checkout (Square, Stripe, etc.).
      </p>
    </section>

    <!-- GALLERY -->
    <section id="gallery">
      <h2>Gallery</h2>
      <p class="section-subtitle">
        Add photos from lessons, clinics, tournaments, and team events.
      </p>

      <div class="gallery-grid">
        <div class="gallery-item">Photo 1</div>
        <div class="gallery-item">Photo 2</div>
        <div class="gallery-item">Photo 3</div>
        <div class="gallery-item">Photo 4</div>
      </div>

      <p style="font-size: 0.85rem; margin-top: 0.75rem; color: #555;">
        Replace each “Photo” box with actual images once you have them.
      </p>
    </section>

    <!-- CONTACT -->
    <section id="contact">
      <h2>Contact</h2>
      <p class="section-subtitle">
        Have questions about lessons, parties, or cage rentals? Reach out and
        we’ll get back to you as soon as possible.
      </p>

      <div class="contact-grid">
        <!-- CONTACT FORM -->
        <form
          action="mailto:info@gjbsports.com"
          method="post"
          enctype="text/plain"
        >
          <!-- Replace info@gjbsports.com with your actual email -->
          <div>
            <label for="name">Athlete / Parent Name</label>
            <input type="text" id="name" name="Name" required />
          </div>

          <div>
            <label for="email">Email</label>
            <input type="email" id="email" name="Email" required />
          </div>

          <div>
            <label for="phone">Phone</label>
            <input type="tel" id="phone" name="Phone" />
          </div>

          <div>
            <label for="interest">I’m Interested In</label>
            <select id="interest" name="Interest">
              <option value="lessons-jose">Lessons with Coach Jose</option>
              <option value="lessons-amanda">Lessons with Coach Amanda</option>
              <option value="party">Party / Event</option>
              <option value="cage-rental">Cage Rental</option>
              <option value="shop">Shop / Merchandise</option>
              <option value="other">Other</option>
            </select>
          </div>

          <div>
            <label for="message">Message / Preferred Days &amp; Times</label>
            <textarea id="message" name="Message"></textarea>
          </div>

          <button type="submit" class="btn btn-primary">Send Message</button>
        </form>

        <!-- CONTACT INFO -->
        <div class="contact-info">
          <p><strong>Email:</strong> info@gjbsports.com</p>
          <p><strong>Phone:</strong> (XXX) XXX-XXXX</p>
          <p><strong>Location:</strong> Your Facility Address Here</p>
          <p style="margin-top: 0.8rem;">
            Follow GJB Sports on social media for updates on clinics, camps,
            and special events.
          </p>
        </div>
      </div>
    </section>
  </main>

  <footer>
    &copy; <span id="year"></span> GJB Sports. All rights reserved.
  </footer>

  <script>
    // Set current year automatically
    document.getElementById("year").textContent = new Date().getFullYear();
  </script>
</body>
</html>