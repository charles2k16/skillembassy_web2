<template>
  <div class="section">
    <el-row :gutter="20">
      <el-col :xs="24" :sm="24" :md="2"> .</el-col>
      <el-col :xs="24" :sm="24" :md="10">
        <div>
          <img
            src="https://skillembassy-website-images.s3.us-east-2.amazonaws.com/untitled+folder/live-classes.png"
            alt="gif"
            width="100%"
          />
        </div>
      </el-col>

      <el-col :xs="24" :sm="24" :md="10" class="mob_mt">
        <div>
          <el-collapse v-model="activeQuestion" accordion class="course_faq">
            <el-collapse-item name="1">
              <template slot="title">
                <img
                  src="../assets/images/liveIcons/presentation.png"
                  alt="ic"
                  width="20px"
                  class="mr-1"
                />
                Live Classes
              </template>
              <div>
                <p>
                  This is an active learning classroom program in which you will
                  have two live lessons of two hours each on Saturdays and
                  Sundays for ten weeks (20 live classes in total). This will be
                  followed by mentor support sessions in which you will be able
                  to ask your burning questions and gain insights from
                  professionals with real-world experience.
                </p>
              </div>
            </el-collapse-item>
            <el-collapse-item name="2">
              <template slot="title">
                <img
                  src="../assets/images/liveIcons/education.png"
                  alt="ic"
                  width="17px"
                  class="mr-1"
                />
                Hands-on Training
              </template>
              <div>
                <p>
                  All of the courses will be hands-on, and they will be
                  complemented with projects. During the workshop, instructors
                  will use less PowerPoint and more real-world and practical
                  materials.
                </p>
              </div>
              <div></div>
            </el-collapse-item>
            <el-collapse-item name="3">
              <template slot="title">
                <img
                  src="../assets/images/liveIcons/problem.png"
                  alt="ic"
                  width="17px"
                  class="mr-1"
                />
                Solve Real World Problems
              </template>
              <div>
                <p>
                  You will collaborate with your team to solve real-world
                  problems that will be used as part of your project portfolio.
                  You will be supervised by our instructors, who have worked
                  with some of the leading product firms and will present many
                  valuable examples from their own experiences.
                </p>
              </div>
            </el-collapse-item>
            <el-collapse-item name="4">
              <template slot="title">
                <img
                  src="../assets/images/liveIcons/question.png"
                  alt="ic"
                  width="17px"
                  class="mr-1"
                />
                Mock Interviews
              </template>
              <div>
                <p>
                  You will get access to two peer-to-peer mock interviews as
                  well as instructor-led mock interviews to help you feel
                  confident about your next interview. All simulated interviews
                  will provide actionable feedback.
                </p>
              </div>
            </el-collapse-item>
            <el-collapse-item name="5">
              <template slot="title">
                <img
                  src="../assets/images/liveIcons/open-book.png"
                  alt="ic"
                  width="17px"
                  class="mr-1"
                />
                Extensive Curriculum
              </template>
              <div>
                <p>
                  With an extensive curriculum, we provide exclusive learning
                  contents that focus on the significant growth of your
                  remarkable engineering, design, and management career.
                </p>
              </div>
            </el-collapse-item>
          </el-collapse>
        </div>
      </el-col>

      <el-col :xs="24" :sm="24" :md="2"> </el-col>
    </el-row>
  </div>
</template>

<script>
export default {
  name: 'LiveClasses',
  data() {
    return {
      activeQuestion: ['1'],
    };
  },
};
</script>
