<template>
  <v-app>
    <v-content class="background">
      <BlockContainer class="block" v-bind:categories="links" />
    </v-content>
    <router-view />
  </v-app>
</template>

<script>
import BlockContainer from "./components/BlockContainer";

export default {
  name: "App",

  components: {
    BlockContainer,
  },

  data: () => ({
    links: [
      {
        name: "Wake",
        sites: [
          { name: "Medhub", url: "https://wfbmc.medhub.com" },
          {
            name: "Citrix",
            url: "https://portal2.wakehealth.edu/",
          },
          {
            name: "Intranet",
            url: "https://intranet.wakehealth.edu/index.htm",
          },
          { name: "Outlook", url: "http://outlook.com/owa/wakehealth.edu" },
          {
            name: "ACP Journal",
            url: "https://annals-org.go.libproxy.wakehealth.edu/aim",
          },
          {
            name: "MKSAP",
            url: "https://mksap18.acponline.org/",
          },
        ],
      },
      {
        name: "Personal",
        sites: [
          { name: "Wiki", url: "http://thisispiggy.gitlab.io/my-wiki/" },
          { name: "Calendar", url: "https://www.google.com/calendar/" },
          { name: "Todoist", url: "https://todoist.com/app/" },
          { name: "Drafts", url: "https://draftin.com/documents" },
          { name: "Drive", url: "https://drive.google.com" },
          {
            name: "Random Evernote",
            url: "https://evernote-random.glitch.me/",
          },
          { name: "Notion", url: "https://www.notion.so" },
        ],
      },
      {
        name: "Social",
        sites: [
          { name: "Reddit", url: "http://old.reddit.com" },
          { name: "Youtube", url: "https://youtube.com" },
          { name: "Messages", url: "https://messages.google.com/web/" },
          { name: "Telegram", url: "https://web.telegram.org/" },
          { name: "Gmail", url: "https://gmail.com" },
          { name: "Inoreader", url: "https://www.inoreader.com/" },
        ],
      },
      {
        name: "Finance",
        sites: [
          { name: "Dicover", url: "https://card.discover.com" },
          {
            name: "Truliant",
            url:
              "https://www.truliantfcuonline.org/tob/live/usp-core/app/login/consumer",
          },
          { name: "Ally", url: "https://secure.ally.com/" },
          { name: "Vanguard", url: "https://personal.vanguard.com/us/MyHome" },
          {
            name: "Fedloan",
            url:
              "https://accountaccess.myfedloan.org/accountAccess/index.cfm?event=common.home",
          },
          {
            name: "YNAB",
            url: "https://app.youneedabudget.com/",
          },
        ],
      },
    ],
  }),
};
</script>

<style>
:root {
  --gradient: linear-gradient(45deg, #416b69, #3f5f6b, #435570, #504a70);
}

.block {
  height: 100%;
}

.background {
  background-image: var(--gradient);
  background-size: 400%;
  animation: bg-animation 10s infinite alternate;
}

@keyframes bg-animation {
  0% {
    background-position: left;
  }
  100% {
    background-position: right;
  }
}
</style>
