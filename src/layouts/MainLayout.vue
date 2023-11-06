<template class="back">
  <div>
    <q-splitter v-model="splitterModel" style="height: 400px">
      <template v-slot:before>
        <q-tabs v-model="tab" vertical class="text-teal">
          <q-tab name="profile" icon="person" label="Profile" />
          <q-tab name="interest" icon="sports" label="Interest" />
          <q-tab name="education" icon="book" label="Education" />
          <q-tab name="contact" icon="phone" label="Contact" />
        </q-tabs>
      </template>

      <template v-slot:after>
        <q-tab-panels
          v-model="tab"
          animated
          swipeable
          vertical
          transition-prev="jump-up"
          transition-next="jump-up"
        >
          <q-tab-panel name="profile">
            <div class="text-h4 q-mb-md">Shruti Sunil Upadhyay</div>
            <q-img
              src="../assets/Shruti.jpg"
              style="max-width: 200px; height: 200px; align-items: center"
              :fit="scale - down"
              img-class="my-custom-image"
            >
            </q-img>
            <div>
              <p class="text-h6 text-weight-medium my-name" style="text-align: right;">Hi I'm ShrutiSunil, a Software Engineer at LTIMindtree.</p>
              <p style="text-align: right;">PS NO : 10725923</p>
              <!-- <p style="text-align: right;">Email : Shruti.10725923@ltimindtree.com</p> -->
            </div>
          </q-tab-panel>

          <q-tab-panel name="interest">
            <div class="text-h4 q-mb-md">Interest</div>
    <p> Here are some of interest and hobbies that I like about.</p>
    <p >
      <ul>
        <li>Sports</li>
        <li> Social Service</li>
        <li> Arts</li>
      </ul>
    </p>
    <p> Coming to technical my interests are HTML, CSS, Frontend, Networks.</p>
          </q-tab-panel>

          <q-tab-panel name="education">
            <div class="text-h4 q-mb-md">Education</div>
            <p>Schooling done from J.N Tata Parsi</p>
    <p>Graduation completed from RCOEM, Nagpur in Electronics Engineering</p>
    <p> Batch : 2019-2023</p>
          </q-tab-panel>

          <q-tab-panel name="contact">
            <div class="text-h4 q-mb-md">Contacts</div>
            <p>Phone No: 8830031503</p>
    <p>Email : Shruti.10725923@ltimindtree.com</p>
    <p>Address: LTIMindtree, Coimbatore</p>
          </q-tab-panel>


        </q-tab-panels>
      </template>
    </q-splitter>
  </div>
</template>

<script>
import { ref } from 'vue'

export default {
  setup() {
    return {
      tab: ref('profile'),
      splitterModel: ref(20)
    }
  }
}
</script>

