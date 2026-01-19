<template>
  <div>
    <!-- Navbar -->
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
      <div class="container px-lg-5">
        <a class="navbar-brand" href="#">A Site on the Web</a>
        <button
          class="navbar-toggler"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#navbarSupportedContent"
          aria-controls="navbarSupportedContent"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>

        <div class="collapse navbar-collapse" id="navbarSupportedContent">
          <ul class="navbar-nav ms-auto mb-2 mb-lg-0">
            <li class="nav-item">
              <a class="nav-link active" href="#">Home</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">About</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">Contact</a>
            </li>
          </ul>
        </div>
      </div>
    </nav>

    <!-- Header -->
    <header class="py-5">
      <div class="container px-lg-5">
        <div class="p-4 p-lg-5 bg-light rounded-3 text-center">
          <div class="m-4 m-lg-5">
            <h1 class="display-5 fw-bold">Buenos Dias!</h1>
            <p class="fs-4">
              This is my first attempt in creating a personal portfolio website
            </p>
            <button class="btn btn-primary btn-lg">
              Let's get to work!
            </button>
          </div>
        </div>
      </div>
    </header>

    <!-- Page Content -->
    <section class="pt-4">
      <div class="container px-lg-5">
        <div class="row gx-lg-5">
          <div
            v-for="(feature, index) in features"
            :key="index"
            class="col-lg-6 col-xxl-4 mb-5"
          >
            <div class="card bg-light border-0 h-100">
              <div class="card-body text-center p-4 p-lg-5 pt-0 pt-lg-0">
                <div
                  class="feature bg-primary bg-gradient text-white rounded-3 mb-4 mt-n4"
                >
                  <i :class="feature.icon"></i>
                </div>
                <h2 class="fs-4 fw-bold">{{ feature.title }}</h2>
                <p class="mb-0">{{ feature.description }}</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Footer -->
    <footer class="py-5 bg-dark">
      <div class="container">
        <p class="m-0 text-center text-white">
          Copyright © Your Website 2023
        </p>
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  name: "Home",
  data() {
    return {
      features: [
        {
          title: "A Sophomore Student",
          description:
            "Bachelor of Science in Computer Science - Specialization in Cybersecurity and Forensics",
          icon: "bi bi-collection",
        },
        {
          title: "A Frustrated Engineer",
          description:
            "I took up Bachelor of Science in Mechanical Engineering at the University of Santo Tomas from 2023 to 2024.",
          icon: "bi bi-cloud-download",
        },
        {
          title: "BS Org",
          description:
            "I serve as a relations officer in JISSA-APC, APC Chorale, and The RamPage!",
          icon: "bi bi-card-heading",
        },
        {
          title: "A Tinkerer",
          description:
            "From troubleshooting to home repairs, I'm your guy!",
          icon: "bi bi-bootstrap",
        },
        {
          title: "A Certified Gearhead",
          description:
            "As long as it has wheels and engines, I'm into it!",
          icon: "bi bi-code",
        },
        {
          title: "Old-School is the Future",
          description:
            "Country music, blues, and soul. If it's vintage, I dig it!",
          icon: "bi bi-patch-check",
        },
      ],
    };
  },
};
</script>

<style scoped>
/* Optional: component-specific styles */
/* Your existing styles.css can remain global */
</style>
