<template>
  <q-page>
    <q-card flat >

      <q-tab-panels v-model="tab" animated>
        <q-tab-panel name="sura" class="q-pa-none">
          <q-card flat>
            <q-img
              style="height: 250px;"
              src="statics/image.jpg"
              basic
            >
              <div class="absolute-bottom text-center" style="text-align: center;">
                SURA INSHIRAH
              </div>
            </q-img>

            <q-card-section class="text-center q-py-md" style="text-align: center;">
              <span class="text-bold" style="font-size: 24px">
                {{starting}}
              </span>
            </q-card-section>

            <q-card-section>
              <span
                v-for="(line,index) in suraInshirah" :key="index"
                class="text-bold"
                style="font-size: 24px"
              >
                {{line + ' O '}}
              </span>
            </q-card-section>
          </q-card>
        </q-tab-panel>

        <q-tab-panel name="tasbeeh" class="q-pa-none">
          <q-card flat>
            <q-img
              src="statics/tasbeeh.png"
              basic
              style="height: 250px;"
            >
              <div class="absolute-bottom text-center" style="text-align: center;">
                TASBEEH
              </div>
            </q-img>

            <q-card-section class="text-bold text-center" style="text-align: center;font-size: 14px">
              Will Be Available in next version
            </q-card-section>
          </q-card>
        </q-tab-panel>

        <q-tab-panel name="aboutUs" class="q-pa-none">
          <q-card flat>
            <q-img
              src="statics/quran.jpg"
              basic
              style="height: 250px;"
            >
              <div class="absolute-bottom text-center" style="text-align: center;">
                ABOUT US
              </div>
            </q-img>

            <q-card-section class="text-bold text-center" style="text-align: center;font-size: 14px">
              Developed By: Rimel
            </q-card-section>
          </q-card>
        </q-tab-panel>
      </q-tab-panels>

      <q-tabs
        v-model="tab"
        class="bg-grey-3 fixed-bottom"
        align="justify"
        narrow-indicator
      >
        <q-tab name="aboutUs" label="About us" />
        <q-tab name="tasbeeh" label="Tasbeeh" />
        <q-tab name="sura" label="Sura" />
      </q-tabs>
    </q-card>
  </q-page>
</template>

<script>
export default {
  name: 'PageIndex',
  data () {
    return {
      tab: 'sura',
      starting: ' بِسْمِ ٱللَّهِ ٱلرَّحْمَٰنِ ٱلرَّحِيمِ',
      suraInshirah: [' أَلَمْ نَشْرَحْ لَكَ صَدْرَكَ', 'وَوَضَعْنَا عَنكَ وِزْرَك', ' ٱلَّذِىٓ أَنقَضَ ظَهْرَكَ', ' وَرَفَعْنَا لَكَ ذِكْرَكَ', ' فَإِنَّ مَعَ ٱلْعُسْرِ يُسْرًا', ' إِنَّ مَعَ ٱلْعُسْرِ يُسْرً', ' فَإِذَا فَرَغْتَ فَٱنصَبْ', 'وَإِلَىٰ رَبِّكَ فَٱرْغَب']
    }
  }
}
</script>
