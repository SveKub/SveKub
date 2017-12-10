---
layout: page
title: Testar AnimCubeJS
permalink: /Losningar/Test
activeMenu: Losningar
---

<div class="container margin-top">
    <div class="row">
        <div class="col-md-6">
            <h2>Korset</h2>
            Första steget i att lösa Rubiks kub är att göra ett vitt kors. För det behövs det ingen algoritm. Försök vrida de fyra vita kantbitarna så de matchar med den vita centerbiten och var av en av de andra fyra färgerna. 
        </div>
        <div class="col-md-4">
          <iframe src="/AnimCubeJS/cube.html?config=AnimCube.cfg&edit=0&buttonbar=2&facelets=lWlWWWlWlllllllllllllgglllllllBBlllllollolllllllRRllll" frameborder="0" height="100%" width="100%"></iframe>
        </div>
    </div>
    <div class="row">
        <div class="col-md-4">
            <h2>Första lagret</h2>
            <p>För att lösa första lagret är det efter korsets fyra kantbitar, fyra hörnbitar som ska sättas på rätt plats vända åt rätt håll. För att göra det används en algoritm som är 4 drag lång. </p>
            <p>Algoritmen som ska användas är: R' D' R D</p>
            <p>
            Börja med att leta efter en vit hörnbit i det undre lagret. När du hittar en titta du vilka två andra färger samma hörnbit har. De andra två färgerna ska matchas med två andra centerbitar. Vrid det undre lagret tills hörnbiten sitter mellan de två andra färgernas centerbitar. </p>
        </div>
        <div class="col-md-4">
          <iframe src="/AnimCubeJS/cube.html?config=AnimCube.cfg&edit=0&buttonbar=1&colorscheme=wygbor&initmove=L D L' B D B' R D R' F D F' D2&move=D" frameborder="0" height="100%" width="100%"></iframe>
        </div>
        <div class="col-md-4">
          <iframe src="/AnimCubeJS/cube.html?config=AnimCube.cfg&edit=0&buttonbar=1&colorscheme=wygbor&initmove=L D L' B D B' R D R' F D F' D'2&move=R' D' R D" frameborder="0" height="100%" width="100%"></iframe>
        </div>
    </div>
    <div class="row">
        <div class="col-md-8"> 
            <p>För att hörnbiten ska hamna på rätt plats och vara vänd åt rätt håll kan du behöva göra algoritmen fem gånger. </p>
            <p>Gör detta steg en gång för alla fyra hörnbitar som ska sitta i det första lagret. </p>
        </div>
        <div class="col-md-4">
          <iframe src="/AnimCubeJS/cube.html?config=AnimCube.cfg&edit=0&buttonbar=1&colorscheme=wygbor&initmove=L D L' B D B' R D R' F D F' D' R' D' R D D' R' D' R D&move=R' D' R D R' D' R D R' D' R D R' D' R D R' D' R D" frameborder="0" height="100%" width="100%"></iframe>
        </div>
    </div>
    <div class="row">
        <div class="col-md-12">
            <h2>Andra lagret</h2>
            <p>När första lagret är löst ska vi lösa andra lagret utan att förstöra något i det första lagret. Börja med att vänd kuben upp och ner så den vita lösta sidan är på kubens undersida. </p>
            <p>
            Andra lagret löser vi med två algoritmer som flyttar ner kantbitar från det översta lagret till det mittersta lagret. Kantbitarna kan flyttas ner till höger eller vänster om en centrumbit. 
            </p>
            <p>Till höger: U R U' R' - U' F' U F</p>
            <p>Till vänster: U' L' U L - U F U' F'</p>
            <p>Vrid det översta lagret tills en kantbit som ska sitta i andra lagret matchar med en centrumbit i det andra lagret. Håll kuben så kantbiten matchar med färgen på centrumbiten på framsidan av kuben. Om kantbitens färg som inte matchar med centrumbiten är på vänster sida av kuben ska algoritmen för vänster göras. Sitter centrumbiten istället på kubens högra sidan ska algoritmen för höger göras. </p>
        </div>
    </div>
    <div class="row">
        <div class="col-md-8">
            Vrid först det övre lagret tills en kantbit matchar med en centrumbit i andra lagret och rotera kuben så kantbiten finns på framsidan. 
        </div>
        <div class="col-md-4">
            <iframe src="/AnimCubeJS/cube.html?config=AnimCube.cfg&edit=0&buttonbar=1&colorscheme=ywgbor&initmove=F U R U' R' F' U R U' R' U' F' U F&move=U Z" frameborder="0" height="100%" width="100%"></iframe>
        </div>
    </div>
    <div class="row">
        <div class="col-md-8">
            Om kantbiten ska sättas ner till vänster gör vi algoritmen för vänster. U' L' U L - U F U' F'
        </div>
        <div class="col-md-4">
            <iframe src="/AnimCubeJS/cube.html?config=AnimCube.cfg&edit=0&buttonbar=1&colorscheme=ywgbor&initmove=F U R U' R' F' U R U' R' U' F' U F U Z&move=U' L' U L U F U' F'" frameborder="0" height="100%" width="100%"></iframe>
        </div>
    </div>
    <div class="row">
        <div class="col-md-8">
            Om kantbiten ska sättas ner till höger gör vi algoritmen för höger:  U R U' R' - U' F' U F
        </div>
        <div class="col-md-4">
            <iframe src="/AnimCubeJS/cube.html?config=AnimCube.cfg&edit=0&buttonbar=1&colorscheme=ywgbor&initmove=F U R U' R' F' U' L' U L U F U' F' U' Z'&move=U R U' R' U' F' U F" frameborder="0" height="100%" width="100%"></iframe>
        </div>
    </div>
    <div class="row">
        <div class="col-md-8">
            <h2>Övre korset</h2>
            <p>Med två lösta lager är det dags att göra kors nummer två. Till det använder vi en ytterligare en algoritm, den här är sex drag lång och ser ut så här: </p>
            <p>F R U – R' U' F'</p>
            <p>De fyra gula kantbitarna ska bilda ett kors, har man tur är det redan ett kors när man kommer hit och då är det bara att gå vidare till nästa steg. Är det gula korset inte löst finns det tre olika lägen och för att lösa dem gör man algoritmen en, två eller tre gånger. </p>
        </div>
        <div class="col-md-4">
            <iframe src="/AnimCubeJS/cube.html?config=AnimCube.cfg&edit=0&buttonbar=1&colorscheme=ylllll&move=F R U R' U' F'" frameborder="0" height="100%" width="100%"></iframe>
        </div>
    </div>
    <div class="row">
        <div class="col-md-12">
            <p>För att algoritmen ska skapa ett kors ska man utföra den med två gula kantbitar mitt emot varandra på varsin sida om centrumbiten. Om ingen gul kantbit förutom centrumbiten finns på ovansidan görs algoritmen först en gång. Då kommer två kantbitar bredvid varandra att vändas rätt. Vrid det över lagret så de gula kantbitarna pekar till vänster och uppåt och utför algoritmen en gång till. Nu kommer det tredje fallet med två gula kantbitar på varsin sida om centrumbiten. Vrid det övre lagret så två gula bitarna pekar till vänster och höger och utför algoritmen en sista gång. 
            De tre olika fallen visas nedan. </p>
        </div>
    </div>
    <div class="row">
        <div class="col-md-4">
            <iframe src="/AnimCubeJS/cube.html?config=AnimCube.cfg&edit=0&buttonbar=1&colorscheme=ywgbor&initmove=L2 U' F' B L2 F B' U' L2 R' F R' B2 R F' R' B2 R2 F R U R' U' F' U2 F R U R' U' F' F R U R' U' F'&move=F R U R' U' F' U2 F R U R' U' F' F R U R' U' F'" frameborder="0" height="100%" width="100%"></iframe>
        </div>
        <div class="col-md-4">
            <iframe src="/AnimCubeJS/cube.html?config=AnimCube.cfg&edit=0&buttonbar=1&colorscheme=ywgbor&initmove=L2 U' F' B L2 F B' U' L2 R' F R' B2 R F' R' B2 R2 F R U R' U' F'&move=F R U R' U' F' F R U R' U' F'" frameborder="0" height="100%" width="100%"></iframe>
        </div>
        <div class="col-md-4">
            <iframe src="/AnimCubeJS/cube.html?config=AnimCube.cfg&edit=0&buttonbar=1&colorscheme=ywgbor&initmove=L2 U' F' B L2 F B' U' L2 R' F R' B2 R F' R' B2 R2 F R U R' U' F' U2 F R U R' U' F'&move=U F R U R' U' F'" frameborder="0" height="100%" width="100%"></iframe>
        </div>
    </div>
    <div class="row">
        <div class="col-md-8">
            <h2>Fixa korset</h2>
            <p>När det övre korset är löst måste de fyra kanterna matchas med de fyra centrarna i andra lagret. Det görs med att utföra en algoritm en eller två gånger. Algoritmen som används kallas Sune och ser ut så här</p>
            <p>R U' R' U' - R U2 R'</p>
        </div>
        <div class="col-md-4">
            <iframe src="/AnimCubeJS/cube.html?config=AnimCube.cfg&edit=0&buttonbar=1&colorscheme=ylllll&move=R U R' U R U2 R'" frameborder="0" height="100%" width="100%"></iframe>
        </div>
    </div>
    <div class="row">
        <div class="col-md-8">
            <p>Vrid det övre lagret så två kantbitar matchar med centrumbitarna i andra lagret. Om de två bitarna sitter bredvid varandra vrider vi på hela kuben så de två bitar som matchar pekar uppåt och till höger. Sedan utför vi algoritmen och avslutar med att vrida det över lagret tills alla fyra kantbitar matchar med centrumbitarna i andra lagret. </p>
        </div>
        <div class="col-md-4">
            <iframe src="/AnimCubeJS/cube.html?config=AnimCube.cfg&edit=0&buttonbar=1&colorscheme=ywgbor&initmove=L2 U' F' B L2 F B' U' L2 R' F' L F R F' L' F&move=U z R U R' U R U2 R' U" frameborder="0" height="100%" width="100%"></iframe>
        </div>
    </div>
    <div class="row">
        <div class="col-md-8">
            <p>Om de två kantbitaran som matchar centrumbitarna ligger på motsatt sida måste algoritmen utföras två gånger. Vrid kuben så det två bitarna pekar mot dig och ifrån dig och utför algoritmen. Efter det kommer du kunna vrida det övre lagret så två kantbitar bredvid varandra matchar med centumbitarna i andra lagret och du kan utföra algoritmen en gång till som i första fallet. </p>
        </div>
        <div class="col-md-4">
            <iframe src="/AnimCubeJS/cube.html?config=AnimCube.cfg&edit=0&buttonbar=1&colorscheme=ywgbor&initmove=L2 U' F' B L2 F B' U' L2 U' L2 U' F' B L2 F B' U' L2  R' F' L F R F' L' F z U&move=U z2 R U R' U R U2 R' z' R U R' U R U2 R' U" frameborder="0" height="100%" width="100%"></iframe>
        </div>
    </div>
    <div class="row">
        <div class="col-md-8">
            <h2>Hörnbitarna</h2>
            <p>För att sätta de fyra sist hörnbitarna på rätt plats ska vi använda den sista algoritmen vi behöver lära oss. Den ser ut så här</p>
            <p>U R U' L' - U R' U' L</p>
            För att den ska fungera ska ett hörn vara på rätt plats. Vrid på kuben (hela kuben, om vi bara vrider på det övre lagret nu kommer vi sätta kantbitarna på fel plats och det vill vi inte eftersom vi i steget innan satte dem på sina rätta platser) och leta efter ett hörn som sitter mellan sina tre centrumbitar. Om inget av de fyra hörnen sitter på rätt plats utför vi algoritmen en gång. Därefter kommer ett hörn sitta på sin rätta plats och vi kan leta efter det. Rotera kuben så det hörn som sitter på rätt plats ligger närmast dig på höger sida och utför algoritmen. 
        </div>
        <div class="col-md-4">
            <iframe src="/AnimCubeJS/cube.html?config=AnimCube.cfg&edit=0&buttonbar=1&colorscheme=ylllll&move=U R U' L' U R' U' L" frameborder="0" height="100%" width="100%"></iframe>
        </div>
    </div>
    <div class="row">
        <div class="col-md-8">
        Vrid hela kuben så en hörnbit sitter på rätt plats när den är på höger sidan närmast dig och utför algoritmen. Titta på alla fyra hörn och se om de sitter på rätt plats. Om de inte gör det letar du efter ett som sitter på rätt plats, vrider på kuben så det sitter närmast dig på höger sida och utför algoritmen igen. 
        </div>
        <div class="col-md-4">
            <iframe src="/AnimCubeJS/cube.html?config=AnimCube.cfg&edit=0&buttonbar=1&colorscheme=ywgbor&initmove=R' F' L F R F' L' F U R U' L' U R' U' L&move=z2 U R U' L' U R' U' L" frameborder="0" height="100%" width="100%"></iframe>
        </div>
    </div>
    <div class="row">
        <div class="col-md-8">
        <h2>Sista steget</h2>
            <p>I sista steget ska vi vända hörnbitarna så de sitter rättvända. Det gör vi med den första algoritmen du lärde dig. </p>
            <p>R' D' R D</p>
            Vrid på kuben så det hörn du vill vända på sitter till närmast dig till höger. Utför algoritmen tills hörnet hamnar med den gula sidan uppåt. Nu kan det se ut som att mycket annat på kuben blivit förstört men så är det inte. Så länge som du fortsätter att utföra algorimen rätt kommer det rätta till sig när du vänt på alla hörn. När det första hörnet är vänt rätt vrider vi det översta lagret så ett annat hörn som är felvänt hamnar närmast dig till höger. Sedan utför vi algoritmen igen tills det hörnet vänds rätt. Fortsätt så med alla hörn som är felvridna. </p>
        </div>
        <div class="col-md-4">
            <iframe src="/AnimCubeJS/cube.html?config=AnimCube.cfg&edit=0&buttonbar=1&colorscheme=ywgbor&initmove=R' D' R D2 F D' F' U F D F' D2 R' D R U'&move=R' D' R D R' D' R D R' D' R D R' D' R D U R' D' R D R' D' R D U'" frameborder="0" height="100%" width="100%"></iframe>
        </div>
    </div>
    
</div>