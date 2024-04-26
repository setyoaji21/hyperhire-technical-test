<template>
  <q-layout view="lHh Lpr lFf" class="desktop">
    <q-header elevated>
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
          @click="toggleLeftDrawer"
        />

        <q-toolbar-title> Quasar App </q-toolbar-title>

        <div>Quasar v{{ $q.version }}</div>
      </q-toolbar>
    </q-header>

    <!-- <q-drawer v-model="leftDrawerOpen" show-if-above bordered>
      <q-list>
        <q-item-label header> Essential Links </q-item-label>

        <EssentialLink
          v-for="link in linksList"
          :key="link.title"
          v-bind="link"
        />
      </q-list>
    </q-drawer> -->

    <q-page-container>
      <router-view />
    </q-page-container>

    <q-footer class="overlap-group-wrapper">
      <div class="overlap-group-2">
        <div class="rectangle"></div>
        <img class="element-2" src="img/1.svg" />
        <p class="text-wrapper-21">
          우리는 국가의 장벽을 넘어 최고의 인재를 매칭해드립니다.
        </p>
        <div class="text-wrapper-22">010-0000-0000</div>
        <div class="text-wrapper-23">aaaaa@naver.com</div>
        <p class="text-wrapper-24">서울특별시 강남대로 479, 지하 1층 238호</p>
        <div class="text-wrapper-25">427-86-01187</div>
        <div class="text-wrapper-26">하이퍼하이어</div>
        <div class="text-wrapper-27">김주현</div>
        <div class="text-wrapper-28">사업자등록번호 CIN</div>
        <div class="text-wrapper-29">대표 CEO</div>
        <div class="text-wrapper-30">상호명</div>
        <div class="text-wrapper-31">U74110DL2016PTC290812</div>
        <div class="text-wrapper-32">주소 ADDRESS</div>
        <p class="d-street-number">
          D-138, Street number 11, Jagjeet Nagar, North East Delhi, New Delhi,
          <br />110053 India
        </p>
        <div class="text-wrapper-33">Hyperhire India Private Limited</div>
        <div class="text-wrapper-34">Juhyun Kim</div>
        <div class="text-wrapper-35">ⓒ 2023 Hyperhire</div>
        <div class="frame-25">
          <div class="frame-26">
            <img class="frame-20" src="img/frame-5042.svg" />
            <div class="frame-27">
              <div class="text-wrapper-36">해외 개발자 원격 채용</div>
            </div>
          </div>
          <div class="frame-28">
            <div class="text-wrapper-37">바로가기</div>
            <div class="iconly-light-outline"></div>
          </div>
        </div>
        <div class="frame-29">
          <div class="frame-30">
            <img class="frame-20" src="img/frame-5042-3.svg" />
            <div class="frame-27">
              <div class="text-wrapper-36">외국인 원격 채용 (비개발)</div>
            </div>
          </div>
          <div class="frame-28">
            <div class="text-wrapper-37">바로가기</div>
            <div class="iconly-light-outline-2"></div>
          </div>
        </div>
        <div class="frame-31">
          <div class="frame-26">
            <img class="frame-20" src="img/frame-5042-2.svg" />
            <div class="frame-27">
              <div class="text-wrapper-36">한국어 가능 외국인 채용</div>
            </div>
          </div>
          <div class="frame-28">
            <div class="text-wrapper-37">바로가기</div>
            <div class="iconly-light-outline-3"></div>
          </div>
        </div>
        <div class="frame-32">
          <div class="frame-26">
            <img class="frame-20" src="img/frame-5043.svg" />
            <div class="frame-27">
              <div class="text-wrapper-36">해외 개발자 활용 서비스</div>
            </div>
          </div>
          <div class="frame-28">
            <div class="text-wrapper-37">바로가기</div>
            <div class="iconly-light-outline-4"></div>
          </div>
        </div>
      </div>
    </q-footer>
  </q-layout>
</template>

<script setup>
import { ref } from "vue";
import EssentialLink from "components/EssentialLink.vue";

defineOptions({
  name: "MainLayout",
});

const linksList = [
  {
    title: "Docs",
    caption: "quasar.dev",
    icon: "school",
    link: "https://quasar.dev",
  },
  {
    title: "Github",
    caption: "github.com/quasarframework",
    icon: "code",
    link: "https://github.com/quasarframework",
  },
  {
    title: "Discord Chat Channel",
    caption: "chat.quasar.dev",
    icon: "chat",
    link: "https://chat.quasar.dev",
  },
  {
    title: "Forum",
    caption: "forum.quasar.dev",
    icon: "record_voice_over",
    link: "https://forum.quasar.dev",
  },
  {
    title: "Twitter",
    caption: "@quasarframework",
    icon: "rss_feed",
    link: "https://twitter.quasar.dev",
  },
  {
    title: "Facebook",
    caption: "@QuasarFramework",
    icon: "public",
    link: "https://facebook.quasar.dev",
  },
  {
    title: "Quasar Awesome",
    caption: "Community Quasar projects",
    icon: "favorite",
    link: "https://awesome.quasar.dev",
  },
];

const leftDrawerOpen = ref(false);

function toggleLeftDrawer() {
  leftDrawerOpen.value = !leftDrawerOpen.value;
}
</script>
