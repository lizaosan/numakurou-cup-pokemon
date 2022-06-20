<template>
  <v-app class="transparent">
    <v-main>
      <h1>Numakurou Cup</h1>
      <bracket :rounds="rounds">
        <template #player="{ player }">
            <div :class="[player.type]" class="type">{{ player.name }} <span class="score">{{ player.score }}</span></div>
        </template>
      </bracket>
    </v-main>
  </v-app>
</template>

<script>
import HelloWorld from "./components/HelloWorld";
import Bracket from "vue-tournament-bracket";

    const rounds = [
        //Quarter
        {
            games: [
                {
                    player1: { id: "1", name: "大頭", type:"dragon", winner: false, score:1},
                    player2: { id: "2", name: "阿德", type:"dragon", winner: true, score:2}
                },
                {
                    player1: { id: "3", name: "恐龍道長", type:"electric", winner: false, score:0},
                    player2: { id: "4", name: "鮭魚", type:"ground", winner: true, score:2}
                },
                {
                    player1: { id: "5", name: "芒果提姆", type:"fire", winner: null, score:1},
                    player2: { id: "6", name: "星宇", type:"ghost", winner: null, score:2}
                },
                {
                    player1: { id: "7", name: "沼喰髏", type:"rock", winner: false, score:0},
                    player2: { id: "8", name: "黑玥", type:"dark", winner: true, score:2}
                },
                {
                    player1: { id: "9", name: "瀧", type:"electric", winner: true, score:2},
                    player2: { id: "10", name: "崩龍斬光", type:"fairy", winner: false, score:1}
                },
                {
                    player1: { id: "11", name: "冰子", type:"bug", winner: null, score:0},
                    player2: { id: "12", name: "小哥", type:"psychic", winner: null, score:0}
                },
                {
                    player1: { id: "13", name: "魚狗", type:"flying", winner: null, score:0},
                    player2: { id: "14", name: "殘夢", type:"bug", winner: null, score:0}
                },
                {
                    player1: { id: "15", name: "漢克", type:"normal", winner: false, score:0},
                    player2: { id: "16", name: "立早三", type:"poison", winner: true, score:2}
                }
            ]
        },
        //Semi
        {
            games: [
                {
                    player1: { id: "2", name: "阿德", type:"dragon", winner: null, score:0},
                    player2: { id: "4", name: "鮭魚", type:"ground", winner: null, score:0}
                },
                {
                    player1: { id: "6", name: "星宇", type:"ghost", winner: null, score:0},
                    player2: { id: "8", name: "黑玥", type:"dark", winner: null, score:0}
                },
                {
                    player1: { id: "9", name: "瀧", type:"electric", winner: true, score:0},
                    player2: { id: "6", name: "", type:"", winner: null, score:0}
                },
                {
                    player1: { id: "7", name: "", type:"", winner: null, score:0},
                    player2: { id: "8", name: "立早三", type:"poison", winner: null, score:0}
                }
            ]
        },
        //Final
        {
            games: [
                {
                    player1: { id: "1", name: "", type:"", winner: null, score:0},
                    player2: { id: "2", name: "", type:"", winner: null, score:0}
                },
                {
                    player1: { id: "3", name: "", type:"", winner: null, score:0},
                    player2: { id: "4", name: "", type:"", winner: null, score:0}
                }
            ]
        },
        {
            games: [
                {
                    player1: { id: "1", name: "", type:"", winner: null, score:0},
                    player2: { id: "2", name: "", type:"", winner: null, score:0}
                }
            ]
        },
        {
            games: [
                {
                    player1: { id: "1", name: "", type:"", winner: null, score:0},
                    player2: { id: "2", name: "", type:"", winner: null, score:0}
                }
            ]
        }
    ];

export default {
  name: "App",

  components: {
    HelloWorld, Bracket
  },

  data: () => ({
    rounds: rounds
  }),

  
};
</script>

<style>
    @import "./assets/css/style.css";
</style>