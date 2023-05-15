<template>
  <div>
    <!-- Start Resume 
      ============================================= -->
    <div id="resume" class="resume-area default-padding-top">
      <div class="shape-right-top-extra">
        <img src="../assets/img/shape/14.png" alt="Shape" />
      </div>
      <div class="container">
        <div class="experience-content-box">
          <div class="row">
            <div class="col-xl-10 offset-xl-1">
              <div
                class="nav nav-tabs text-center resume-tab-navs"
                id="nav-tab"
                role="tablist"
              >
                <button
                  class="nav-link active"
                  id="nav-id-1"
                  data-bs-toggle="tab"
                  data-bs-target="#tab1"
                  type="button"
                  role="tab"
                  aria-controls="tab1"
                  aria-selected="true"
                >
                  Biography <strong>01</strong>
                </button>
                <button
                  class="nav-link"
                  id="nav-id-2"
                  data-bs-toggle="tab"
                  data-bs-target="#tab2"
                  type="button"
                  role="tab"
                  aria-controls="tab2"
                  aria-selected="false"
                >
                  Skills <strong>02</strong>
                </button>
                <button
                  class="nav-link"
                  id="nav-id-3"
                  data-bs-toggle="tab"
                  data-bs-target="#tab3"
                  type="button"
                  role="tab"
                  aria-controls="tab3"
                  aria-selected="false"
                >
                  Education <strong>03</strong>
                </button>
              </div>

              <div class="tab-content resume-tab-content" id="nav-tabContent">
                <!-- Single Item -->
                <div
                  class="tab-pane fade show active"
                  id="tab1"
                  role="tabpanel"
                  aria-labelledby="nav-id-1"
                >
                  <div class="row">
                    <div class="col-lg-12">
                      <ul class="biography-table">
                        <li>
                          <h5>Name</h5>
                          <p>Joaquim Crous Mayné</p>
                        </li>
                        <li>
                          <h5>Birthday</h5>
                          <p>04 May, 1987</p>
                        </li>
                        <li>
                          <h5>Age</h5>
                          <p>35</p>
                        </li>
                        <li>
                          <h5>Address</h5>
                          <p>Sant Feliu de Llobregat, Cat, SP</p>
                        </li>
                        <li>
                          <h5>Email</h5>
                          <p>joaquimcrous@gmail.com</p>
                        </li>
                        <li>
                          <h5>Phone</h5>
                          <p>+(34)686542727</p>
                        </li>
                        <li>
                          <h5>LinkedIn</h5>
                          <p>
                            <a
                              href="https://www.linkedin.com/in/joaquim-crous-mayné/"
                              target="_blank"
                              >Joaquim Crous</a
                            >
                          </p>
                        </li>
                        <li>
                          <h5>GitHub</h5>
                          <p>
                            <a
                              href="https://github.com/QuimCrous"
                              target="_blank"
                              >GitHub Link</a
                            >
                          </p>
                        </li>
                      </ul>
                    </div>
                  </div>
                </div>
                <!-- End Single Item -->

                <!-- Single Item -->
                <div
                  class="tab-pane fade"
                  id="tab2"
                  role="tabpanel"
                  aria-labelledby="nav-id-2"
                >
                  <div class="row align-center">
                    <div class="col-lg-12">
                      <ul class="skill-table">
                        <li>
                          <div class="row align-center">
                            <div class="col-lg-2">
                              <div class="icon">
                                <!-- <i class="mb-5">
                                    <img
                                      src="../assets/img/icon/java.svg"
                                      alt=""
                                    />
                                  </i> -->
                                <i class="fab fa-java bg-black"></i>
                              </div>
                            </div>
                            <div class="col-lg-5">
                              <h4>Object oriented programming</h4>
                            </div>
                            <div class="col-lg-5">
                              <div class="progress-box">
                                <h5>75%</h5>
                                <div class="progress">
                                  <div
                                    class="progress-bar"
                                    role="progressbar"
                                    data-width="75"
                                  ></div>
                                </div>
                              </div>
                            </div>
                          </div>
                        </li>

                        <li>
                          <div class="row align-center">
                            <div class="col-lg-2">
                              <div class="icon">
                                <!-- <i class="mb-5"
                                    ><img
                                      src="../assets/img/icon/square-js.svg"
                                      alt=""
                                  /></i> -->
                                <i class="fab fa-js bg-black"></i>
                              </div>
                            </div>
                            <div class="col-lg-5">
                              <h4>Advance frontend development</h4>
                            </div>
                            <div class="col-lg-5">
                              <div class="progress-box">
                                <h5>84%</h5>
                                <div class="progress">
                                  <div
                                    class="progress-bar"
                                    role="progressbar"
                                    data-width="84"
                                  ></div>
                                </div>
                              </div>
                            </div>
                          </div>
                        </li>

                        <li>
                          <div class="row align-center">
                            <div class="col-lg-2">
                              <div class="icon">
                                <!-- <i>
                                    <img
                                      src="../assets/img/icon/vuejs.svg"
                                      alt=""
                                    />
                                  </i> -->
                                <i class="fab fa-vuejs bg-black"></i>
                              </div>
                            </div>
                            <div class="col-lg-5">
                              <h4>Front-End with VUE</h4>
                            </div>
                            <div class="col-lg-5">
                              <div class="progress-box">
                                <h5>92%</h5>
                                <div class="progress">
                                  <div
                                    class="progress-bar"
                                    role="progressbar"
                                    data-width="92"
                                  ></div>
                                </div>
                              </div>
                            </div>
                          </div>
                        </li>
                      </ul>
                    </div>
                  </div>
                </div>
                <!-- End Single Item -->

                <!-- Single Item -->
                <div
                  class="tab-pane fade"
                  id="tab3"
                  role="tabpanel"
                  aria-labelledby="nav-id-3"
                >
                  <div class="row">
                    <div class="col-lg-12">
                      <ul class="education-table">
                        <li>
                          <h4>Frontend Web Development</h4>
                          <h5>Ironhack</h5>
                          <span>2023</span>
                          <p>
                            Bootcamp in which I was taught web development using
                            HTML, CSS, and JavaScript. It also delved into the
                            design of SPAs using the VUE.js framework.
                          </p>
                        </li>
                        <li>
                          <h4>Master Course Python</h4>
                          <h5>Udemy</h5>
                          <span>2022</span>
                          <p>
                            Online course where I learned basic programming
                            skills in Python.
                          </p>
                        </li>
                        <li>
                          <h4>Backend Web Development - Java</h4>
                          <h5>Ironhack Barcelona</h5>
                          <span>2022</span>
                          <p>
                            Bootcamp in which I was taught object-oriented
                            programming in Java. It delved into creating REST
                            APIs using the Spring framework. We were also taught
                            how to manage relational databases (MySQL).
                          </p>
                        </li>
                        <li>
                          <h4>Physics grade</h4>
                          <h5>Universitat de Barcelona</h5>
                          <span>2006 - 2008 (unfinished)</span>
                          <p>
                            University degree where Physics and Mathematics, and
                            their related fields, are taught.
                          </p>
                        </li>
                      </ul>
                    </div>
                  </div>
                </div>
                <!-- End Single Item -->
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- End Resume -->
  </div>
</template>

<script setup></script>

<style lang="scss" scoped></style>
