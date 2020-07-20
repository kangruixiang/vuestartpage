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
    BlockContainer
  },

  data: () => ({
    links: [
      {
        name: "Wake",
        sites: [
          { name: "Medhub", url: "https://wfbmc.medhub.com" },
          {
            name: "Citrix",
            url: "https://portal2.wakehealth.edu/"
          },
          {
            name: "Intranet",
            url: "https://intranet.wakehealth.edu/index.htm"
          },
          { name: "Outlook", url: "https://owa.wakehealth.edu" },
          {
            name: "ACP Journal",
            url: "https://annals-org.go.libproxy.wakehealth.edu/aim"
          },
          {
            name: "UWorld",
            url:
              "https://www.uworld.com/ClientApp/V2/apps/Qbank/index.html#/test/welcome/5618757"
          },
          {
            name: "MKSAP",
            url: "https://mksap18.acponline.org/"
          }
        ]
      },
      {
        name: "Personal",
        sites: [
          { name: "Wiki", url: "http://thisispiggy.gitlab.io/my-wiki/" },
          { name: "Calendar", url: "https://www.google.com/calendar/" },
          { name: "Todoist", url: "https://todoist.com/app#start" },
          { name: "Gmail", url: "https://gmail.com" },
          { name: "Drive", url: "https://drive.google.com" },
          { name: "Keep", url: "https://keep.google.com/u/0/" },
          { name: "Notion", url: "https://www.notion.so" },
          { name: "Roam", url: "https://roamresearch.com/#/app/kangruixiang" }
        ]
      },
      {
        name: "Social",
        sites: [
          { name: "Reddit", url: "http://old.reddit.com" },
          { name: "Youtube", url: "https://youtube.com" },
          { name: "Messages", url: "https://messages.google.com/web/" },
          { name: "Telegram", url: "https://web.telegram.org/" },
          { name: "Gmail", url: "https://gmail.com" },
          { name: "Drive", url: "https://drive.google.com" }
        ]
      },
      {
        name: "Finance",
        sites: [
          { name: "Dicover", url: "https://card.discover.com" },
          {
            name: "Truliant",
            url:
              "https://www.truliantfcuonline.org/tob/live/usp-core/app/login/consumer"
          },
          { name: "Ally", url: "https://secure.ally.com/" },
          { name: "Vanguard", url: "https://personal.vanguard.com/us/MyHome" },
          {
            name: "Fedloan",
            url:
              "https://accountaccess.myfedloan.org/accountAccess/index.cfm?event=common.home"
          },
          {
            name: "AMSbilling",
            url: "https://ams-ubs.com/dvara/"
          },
          {
            name: "YNAB",
            url: "https://app.youneedabudget.com/"
          }
        ]
      }
    ]
  })
};
</script>

<style>
:root {
  --gradient: linear-gradient(45deg, #1c6a66, #1c546a, #264371, #312671);
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
