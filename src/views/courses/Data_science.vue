<template>
  <div>
    <div class="course_page_header">
      <div class="section py-100">
        <el-row :gutter="50">
          <el-col :xs="24" :sm="24" :md="12" class="mob_mt">
            <h3 class="white course_hd">
              Start Your Career As A Data Scientist
            </h3>
            <p class="mt-40 text_highlight">
              Do you want to enjoy the experience of developing and launching a
              social or human problem from idea to completion with your own
              designer, product manager, and software developer?
            </p>
            <el-button
              type="primary"
              class="mt-20"
              @click="applyCourse('data_science')"
              >Apply Now</el-button
            >
          </el-col>

          <el-col :xs="24" :sm="24" :md="12" class="mob_mt">
            <div class="d-flex-align-center justify-right">
              <img
                src="../../assets/images/gifs/data-science.gif"
                alt="gif"
                class="course_head_img"
              />
            </div>
          </el-col>
        </el-row>
      </div>
    </div>

    <div class="section py-100 mob_mt">
      <div class="course_detail">
        <h2>The program is best suited for</h2>
        <el-row :gutter="20">
          <el-col :xs="24" :sm="24" :md="8">
            <div class="program_div">
              <div class="program">Professionals</div>
              <p class="px-0 mt-10">
                Seeking to move into product management jobs from backgrounds in
                engineering, marketing, sales, design, operations, and finance
              </p>
            </div>
          </el-col>
          <el-col :xs="24" :sm="24" :md="8">
            <div class="program_div">
              <div class="program">Entrepreneurs</div>
              <p class="px-0 mt-10">
                Seeking to establish a product mentality for their own endeavors
                in order to generate great products faster while avoiding
                potentially fatal mistakes
              </p>
            </div>
          </el-col>
          <el-col :xs="24" :sm="24" :md="8">
            <div class="program_div">
              <div class="program">"Senior" Freshers</div>
              <p class="px-0 mt-10">
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Quis
                natus soluta tempore.
              </p>
            </div>
          </el-col>
        </el-row>
        <br />
      </div>
    </div>

    <div class="bg_white py-100">
      <LiveClasses />
    </div>

    <div class="py-70 curr_bg">
      <h3 class="center h_title">Curriculum</h3>
      <br />
      <p class="text_highlight curr_p">
        With an extensive curriculum, we provide exclusive learning contents
        that focus on the significant growth of your remarkable engineering,
        design, and management career.
      </p>
      <div class="section mt-20 d-flex-center">
        <el-collapse
          v-model="activeCurr"
          accordion
          class="curriculum mt-20 mb-40"
        >
          <el-collapse-item
            v-for="(curr, index) in curriculum"
            :key="index"
            :name="`${index.toString()}`"
          >
            <template slot="title">
              <span class="step_num mr-1">Week {{ index + 1 }}</span
              >{{ curr.name }}
            </template>
            <div>
              <p v-html="curr.description"></p>
            </div>
          </el-collapse-item>
        </el-collapse>
      </div>

      <div class="center mt-20">
        <el-button
          type="primary"
          icon="el-icon-edit-outline"
          @click="applyCourse('data_science')"
        >
          <b>APPLY NOW</b></el-button
        >
      </div>
    </div>

    <div class="full_width bg_business py-70">
      <HowItWorks />
      <div class="d-flex justify_center">
        <div class="advisor_div">
          <p>
            Would you like to know more? Our admission consultants can help you
            schedule a conversation with a learning advisor.
          </p>
          <el-button class="mt-20" type="primary"
            >Talk to a Learning Advisor
          </el-button>
        </div>
      </div>
    </div>
    <div class="full_width bg_white py-70">
      <Faqs />
    </div>

    <div class="full_width bg_callUs py-70">
      <div class="center">
        <p class="callUs_p">Ready to change your your life?</p>
        <h3 class="callUs_h3 mt-20">
          Take the next step & apply to Skill Embassy.
        </h3>
      </div>

      <div class="mt-40 d-flex justify_center">
        <el-button
          icon="el-icon-edit-outline"
          @click="applyCourse('data_science')"
        >
          <b>APPLY NOW</b></el-button
        >
      </div>
    </div>
    <div class="full-width bg_footer">
      <Footer />
    </div>
  </div>
</template>

<script>
import Faqs from '../../components/Faqs.vue';
import Footer from '../../components/Footer.vue';
import HowItWorks from '../../components/HowItWorks.vue';
import LiveClasses from '../../components/LiveClasses.vue';

export default {
  name: 'Data_science',
  components: {
    Faqs,
    HowItWorks,
    Footer,
    LiveClasses,
  },
  created() {
    window.scrollTo({ top: 0, behavior: 'smooth' });
  },
  data() {
    return {
      activeCurr: ['1'],
      // activeCurr: ['1'],
      curriculum: [
        {
          name: 'Understanding the product management & marketing tools',
          description:
            ' - Devops BootCamp Overview <br /> - What is DEvOps <br /> - Roles and Responsibilities of DevOps Engineer <br /> - How DevOps fit in the whole Software Development lifecycle.',
        },
        {
          name: 'User Reasearch, Market Research & Product Types',
          description:
            ' - Devops BootCamp Overview <br /> - What is DEvOps <br /> - Roles and Responsibilities of DevOps Engineer <br /> - How DevOps fit in the whole Software Development lifecycle.',
        },
      ],
    };
  },
};
</script>
