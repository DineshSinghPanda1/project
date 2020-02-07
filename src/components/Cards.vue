<template>
  <v-container grid-list-md>
    <div>
      <v-btn color="purple ml-5">CLASS1</v-btn>
    </div>
    <v-alert outlined color="purple">
      <v-layout row wrap class="border-color:red">
        <v-flex md3 v-for="card in cards" :key="card">
          <v-card>
            <v-card-title v-bind:style="{ color: dynamic }">
              {{ card.title }}
            </v-card-title>
            <v-divider></v-divider>
            <v-row justify="space-between ">
              <v-col>
                <v-responsive>
                  <v-avatar color="teal" size="120">
                    <v-img :src="card"></v-img> </v-avatar
                ></v-responsive>
              </v-col>
              <v-col cols="auto" class=" ">
                <v-row justify="center">
                  <v-col class="px-0">
                    <h5 v-bind:style="{ color: dynamic }">{{ card.name }}</h5>
                    <h5 v-bind:style="{ color: dynamic }">
                      {{ card.subject }}
                    </h5>
                    <h5 v-bind:style="{ color: dynamic }">
                      {{ card.strenght }}
                    </h5>
                    <h5 v-bind:style="{ color: dynamic }">
                      {{ card.present }}
                    </h5>
                    <h5 v-bind:style="{ color: dynamic }">
                      {{ card.abscent }}
                    </h5>
                  </v-col>
                </v-row>
              </v-col>
            </v-row>
          </v-card>
        </v-flex>
      </v-layout>
    </v-alert>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      dynamic: "purple",
      cards: [
        {
          title: "SECTION A",
          src: require("../assets/student.jpg"),
          name: "Raj",
          subject: "Math",
          strenght: "Strenght of class",
          present: "Student Present",
          abscent: "Student Abscent"
        },
        {
          title: "SECTION B",
          src: require("../assets/boy.jpg"),
          name: "Dinesh",
          subject: "English",
          strenght: "Strenght of class",
          present: "Student Present",
          abscent: "Student Abscent"
        },
        {
          title: "SECTION C",
          src: require("../assets/student.jpg"),
          name: "Kamal",
          subject: "C++",
          strenght: "Strenght of class",
          present: "Student Present",
          abscent: "Student Abscent"
        },
        {
          title: "SECTION D",
          src: require("../assets/boy.jpg"),
          name: "Suraj",
          subject: "English",
          strenght: "Strenght of class",
          present: "Student Present",
          abscent: "Student Abscent"
        }
      ]
    };
  }
};
</script>
<style lang="scss" scoped></style>
