# ma démarche 
j'ai commencer par regarder l'indentation des element dans la maquette et les est reproduite en html en le fesant une section a la fois. puis je suis passer un css ou jai regarder toute les variable de couleur qui étais dans la maquette figma et les est reproduite dans le root, j'ai ensuite fait toute les autre variable qui me senblais utiles et réutilisable. j'ai ensuite reproduit section par section en fonction de se que je pouvait voir sur la maquette du mieux que je pouvais. Apres avoir terminer une je section je vérifiais quelle étais réactive au minimum d'un format paysage a un format portrais. j'ais ensuite fait un retour sur le css pour vérifier si il y avait un bug quelle que part.

# système de nomenclature CSS
j'ai honnetement tenter de suivre BEM mais je suis pas sur que tous suis exactement la rêgle.

# variable css
j'ai mis toute les variables de couleur qui étais dans la maquette avec exactement les meme nom apart certais qui n'apparaisais pas dans les variables de la maquette (j'ai suivie la logique et les est nommer en fonction de a quoi ils servais). Sinon j'ai fait des font size se qui est juste pratique pour changer la grosseur des textes. j'ais aussie mit des variable de border que j'ai sourtout utiliser pour faire du border-radius et les deux autres ses du padding et du margin qui sont tous simplement utiliser partout alors ils me semblais pratique a avoir.

# liste composant réutilisable
.btn
a
.rg_carte-mini
.carte_mini
.text_review
.btn
.card_lg
.carrer-card_lg
.text_card
ils ne sont pas placer au débuts mais ses réutilisable si ton compte refaire  le meme style de carte, boutton et autres.

# mes décisions pour layout dificile 
Je sais pas mais un layout est pas vraiment qu'un autre tant que l'indentation et que le placement de div est bien penmser elle sont pas tend compliquer a reproduire donc je dirais que j'ai juste utiliser de la logique (si le resultat finals est en colunm sarrager pour avoir un div placer qui nous permette de le mettre en colunm ses pas plus compliquer que cela même chose pour flex-wrap, shrink et autre)

# mes choix de fonctions css fluide
ex (dans la section card horraire): flex: 0 1 calc(33.33% - 50px); . J'ais utiliser calc car je voulais que mon flex basis soit d'une grandeur présise pour faire ne sorte qu'il que je garde en dans tout les cas seulement trois element sur la ligne sans prendre trop de place dans l'espace.
le reste du temps j'utilise majoritairement juste un flex avec des variable qui donne la réactiviter que je veux pour mes composant acompagner de min, max height et width. et j'utilise des uniter t'el que vh ou vw qui dépende du viewport.

# mes choix techniques
je suis pas sur de se que vous voulez dire par choix technique mais côter technique jai sourtout utiliser flexbox car je trouvais que c'étais l'outil logique pour produire cette maquette et j'ai utiliser des variable réutilisable pour la même raison.(en même temps ses se que vous aviez demander aussie alors j'avais pas trop le choix). Mais sinon sourtout du padding et du margin mais pour le reste ses juste les base imposibles a éviter comme les font-familie et les border radius et autres.

# les défis que j'ais rencontrer 
rendre tous réactif et faire en sorte que rien ne sois en dehors du viewport. Sinon c'étais tester un certain nombres de possibiliter quand je n'étais pas sur jusqu'a se soit la bonne réponse.(ou que sa lui ressemble tellement que je ne voit pas la diffrence).

# utilisation ai
elle a pas été utiliser pour la grande majoriter du travaille (elle a été utiliser 4 fois) j'ais malheureusement pas les prompt exact mais je sais environs se que j'ai demander
1: 
prompt: explique moi comment faire pour enpêcher de mettre un texte a la ligne
réponse: white-space: nowrap;
le model chagpt actuel: GPT-5.4 Mini (a se que jai pue voir mais je n'ais pas réussie a le trouver sur leur site)
date: 2026-03-22
je l'est utiliser a plusieur emplacement pour éviter quelle que probleme

2:
prompt: explique moi en détail chaque partie de flexbox
réponse: ils ma fait un texte très long pour mexpliquer les flex-direction, gap et autre.
le model chagpt actuel: GPT-5.4 Mini (a se que jai pue voir mais je n'ais pas réussie a le trouver sur leur site)
date: 2026-03-21
je l'est utiliser comme sorte d'aide mémoire (mais la réaliter ses quil a juste servie a me faire un rapel a chaque fois que je commencais a coder)

3:
prompt: explique moi en détail les ecriture possible de margin et padding
réponse: ils ma expliquer exactement se que je lui est demander.
le model chagpt actuel: GPT-5.4 Mini (a se que jai pue voir mais je n'ais pas réussie a le trouver sur leur site)
date: 2026-03-21
je l'est utiliser pour comprendre (je l'est demander plusieur fois en réaliter mais je le compte pour 1 vue que j'ai demander pour la meme chose plusieur fois)

4:
prompt: explique moi comment empcher que le ratio d'un element change 
réponse: aspect-ratio: 9 / 16;
le model chagpt actuel: GPT-5.4 Mini (a se que jai pue voir mais je n'ais pas réussie a le trouver sur leur site)
date: 2026-03-22
je l'est utiliser a plusieur reprise ses plutô pratique si on ne veux pas que sa change peut importe le viewport.

5: 
prompt: tu peux m'aider a comprendre comment mettre seulement trois element par lignes
.carte_horraire {
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: 12px;
}
réponse:
.carte_horraire {
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: 12px;
    flex: 0 1 calc(33.33% - 50px);
}
le model chagpt actuel: GPT-5.4 Mini (a se que jai pue voir mais je n'ais pas réussie a le trouver sur leur site)
date: 2026-03-21
je l'est utiliser pour exactement se que je lui est demander dans la section horraire.

le reste ses que moi et les notes de cours

# petit commentaire de fin 
je tien a dire que l'ont vien juste de me faire comprend que j'avait mals comprit se que vous vouliez vire par suivre la maquette (ils est présentement 22h16 le 22 mars) (j'ai respecter les couleur et la font) mais jai comment dire pas comprit que figma donnais le code a mettre dans chacunne des classes. Le fichier css qui est dans le projet est donc mon interpretation de la maquette que vous m'aver donner (elle presque identique et j'ais fait le code en le testand au fur et a mesure en format 9/16 et 16/9) elle est responsive mais bon je comprendrer que je vais perdres des point pour pas avoir exactement le même code que celuis qui étais dans l'auto layout.