<script lang="ts">
import { ContainerGroupInfoTypeUI, ContainerInfoUI } from './ContainerInfoUI';
import PodIcon from './PodIcon.svelte';

export let type = '';
export let containers: ContainerInfoUI[] = [];

let isRunning = false;
$: isRunning = containers.every(c => c.state === 'RUNNING') ? true : false;
$: isExited = containers.some(c => c.state === 'EXITED') ? true : false;
</script>

<div
  class:border-green-600="{isRunning}"
  class:border-orange-500="{isExited}"
  class="border flex flex-col justify-center align-middle m-3 p-1 w-10 text-center items-center rounded">
  {#if type === ContainerGroupInfoTypeUI.COMPOSE}
    <svg
      class:text-green-600="{isRunning}"
      class:text-orange-500="{isExited}"
      version="1.0"
      width="14px"
      height="14px"
      viewBox="0 0 1280.000000 1165.000000"
      preserveAspectRatio="xMidYMid meet">
      <g transform="translate(0.000000,1165.000000) scale(0.100000,-0.100000)" fill="currentColor" stroke="none">
        <path
          d="M6675 11644 c-314 -29 -553 -75 -790 -151 -553 -176 -1026 -470
-1442 -896 -383 -392 -657 -843 -832 -1365 -117 -349 -171 -635 -190 -1005 -9
-183 -1 -451 19 -617 30 -248 103 -574 185 -825 25 -76 44 -139 42 -140 -154
-102 -356 -179 -564 -215 -210 -37 -369 -42 -888 -29 -506 13 -682 8 -885 -27
-576 -97 -1131 -469 -1281 -858 -152 -394 80 -853 535 -1061 170 -77 400 -132
646 -155 551 -49 1299 99 1785 353 222 117 310 192 593 507 386 429 500 528
678 591 74 26 221 29 309 6 273 -73 513 -275 651 -549 144 -287 159 -561 44
-803 -67 -140 -124 -192 -640 -585 -377 -288 -558 -439 -740 -621 -355 -355
-562 -684 -673 -1076 -243 -851 40 -1654 688 -1950 148 -68 311 -114 545 -155
101 -17 535 -17 655 0 369 54 767 164 996 276 532 259 949 777 1093 1358 50
201 59 291 58 588 -1 151 -6 358 -11 460 -48 841 -27 1194 93 1566 72 221 171
316 344 331 249 21 586 -171 797 -452 62 -83 99 -154 150 -290 301 -807 568
-1274 928 -1622 171 -165 306 -260 502 -354 451 -215 1011 -265 1545 -139 345
82 544 227 712 520 150 261 204 675 133 1025 -137 678 -678 1206 -1316 1284
-235 29 -244 31 -314 66 -160 78 -266 221 -294 394 -20 126 27 250 124 323 94
71 126 79 715 174 193 31 343 60 440 85 455 118 763 331 910 628 45 90 60 144
66 241 20 294 -200 554 -551 650 -99 28 -297 38 -388 21 -103 -20 -210 -59
-284 -105 -39 -24 -151 -108 -249 -187 -200 -162 -324 -254 -431 -323 -255
-162 -518 -236 -740 -208 -116 15 -157 35 -161 79 -4 39 14 75 88 178 65 90
109 174 145 273 110 311 168 715 169 1177 0 272 -8 382 -45 610 -201 1250
-1037 2308 -2184 2763 -278 110 -519 173 -840 217 -104 15 -558 28 -650 19z"></path>
      </g>
    </svg>
  {:else}
    <PodIcon colorClasses="{isRunning ? 'text-green-600' : ''} isExited ? 'text-orange-500' : ''}" />
  {/if}
</div>
