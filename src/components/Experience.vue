<template>
  <section id="experience" class="row">

    <div class="col-12 col-lg-3 experience-left">
      <mdc-icon class="accent" icon="work"></mdc-icon>
      <h2 class="accent">Experience</h2>

      <div class="description">
        <!--Love is the only mind, the only guarantee of attitude.Place the sauerkraut in a pan, and flavor thoroughly with sour triple sec.All of those processors evacuate strange, modern vogons.Love is the only mind, the only guarantee of attitude.Place the sauerkraut in a pan, and flavor thoroughly with sour triple sec.All of those processors evacuate strange, modern vogons.-->
      </div>
    </div>

    <div class="col-12 col-lg-9 experience-right">

      <div class="steps-wrapper" v-for="(step, index) in steps">
        <div :id="step.id" :class="step.yearEnd? '': 'current'">
          <div class="step-header">
          <span>
            <svg class="accent" focusable="false" viewBox="0 0 48 48" aria-hidden="true">
              <circle cx="50%" cy="50%" r="24"></circle>
              <text class="" x="24" y="24" alignment-baseline="central" text-anchor="middle">{{step.yearStart}}</text>
            </svg>
          </span>
            <h3 class="step-title">{{step.title}}</h3>
          </div>
          <div class="row step-detail">
            <p v-html="step.details"></p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>

    export default {
        name: 'Experience',


        data() {
            return {
                steps: [
                    {
                        id: 'internship-11f',
                        yearStart: 2014,
                        yearEnd: 2015,
                        company: {
                            name: "11Freunde",
                            website: "https://www.11freunde.de/"
                        },
                        title: 'Practical semester / internship - Web Development',
                        details: "As part of my bachelor's program, I worked as an intern for 6 months at <a href=\"https://www.11freunde.de/\" target=\"_blank\">11Freunde Verlag</a> in Berlin. My scope of responsibility included developing new web applications (front- and backend), maintaining existing applications and databases as well as various IT-related tasks",
                    },
                    {
                        id: 'workingstudent-11f',
                        yearStart: 2015,
                        yearEnd: 2018,
                        company: {
                            name: "11Freunde",
                            website: "https://www.11freunde.de/"
                        },
                        title: 'Working student - Full Stack Development',
                        details: 'I very much liked the kind of work and freedom I had during my internship at 11Freunde. Therefore I was genuinely happy about the offer to continue as a working student being able to work completely remotely. Since I already gained some experience in Android development during my studies, I also assumed responsibility for maintenance of the <a href="https://play.google.com/store/apps/details?id=de.android.elffreunde" target="_blank">11Freunde App</a>  with its more than 100.000 accumulated downloads.',
                    },
                    {
                        id: 'master',
                        yearStart: 2017,
                        yearEnd: 2017,
                        company: {
                            name: "Daimler AG",
                            website: "https://www.daimler.com/"
                        },
                        title: "Master's candidate - Software Development Artificial Intelligence",
                        details: "After writing my bachelor's thesis at the university, I decided to approach my master's thesis in collaboration with industry. I started my work at the <a href='https://www.daimler.com/' target='_blank'>Daimler AG</a> as member of the #teamPactris, which again belongs to the <a href='https://www.daimler.com/company/strategy/digitallife/' target='_blank'>DigitalLife@Daimler</a> department.",
                    },
                    {
                        id: 'job-daimler',
                        yearStart: 2018,
                        yearEnd: null,
                        company: {
                            name: "Daimler AG",
                            website: "https://www.daimler.com/"
                        },
                        title: 'Software Developer Artificial Intelligence',
                        details: "With all the theoretical and practical experience I gained in the last years, I was perfectly prepared for my first fulltime job. And because I loved the work during my master's thesis, I am happy to still be part of this amazing team and to contribute my knowledge and expertise about AI and ML",
                    },
                    {
                        id: 'dhbw',
                        yearStart: 2019,
                        yearEnd: null,
                        company: {
                            name: "DHBW Stuttgart",
                            website: "https://www.dhbw-stuttgart.de/home/"
                        },
                        title: 'Lecturer at DHBW Stuttgart for Computer Science',
                        details: "Besides my primary job I started a position as Lecturer at <a href='https://www.dhbw-stuttgart.de/home/'>DHBW (Cooperative State University) Stuttgart</a>, Campus Horb. I'm teaching computer science and programming to industrial engineering students, 1st and 2nd semester. I love to share my knowledge and passion about coding with the students and it also gives me a lot in return.",
                    },
                ],
            }
        }
    }
</script>

<style scoped>

  #experience {
    border-collapse: collapse;
    border: 1px solid #f2f2f2;
    box-shadow: 0 0 10px 0 rgba(0, 0, 0, .05);
  }

  .experience-left {
    text-align: left;
    padding: 20px;
  }

  .experience-left h2 {
    display: inline-block;
    padding-left: 10px;
  }


  .current .step-detail {
    border-left: 1px dashed gray;
  }

</style>
