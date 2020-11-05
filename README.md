# CustomMap
## Pourquoi un custom map ?
Webflow offre la possibilité d'[intégrer des maps](https://university.webflow.com/lesson/map) simplement
Mais on est vite limité. On ne peut pas intégrer plusieurs endroits, ni personnaliser les marqueurs ou afficher quelque chose au clic.
Pour palier à cela, j'ai créé un EMBED HTML à intégrer dans le HEAD de la page Webflow.

## Comment utiliser la customMap ?
<ol>
<li>Créer une collection où on va stocker tous les points à afficher (dans mon exemple, des crèches)</li>
<li>Ajouter un champ "Lien Google Map" dans la collection et renseigner le lien de la page google. Exemple : https://www.google.com/maps/place/Micro-Cr%C3%A8che+des+Anges+d'Illkirch/@48.5282431,7.7078054,17z/data=!3m1!4b1!4m5!3m4!1s0x4796ca11a42a2611:0xeaec77a351736b9!8m2!3d48.5282396!4d7.7099941</li>
<li>Ajouter un élément COLLECTION LIST en reproduisant la structure du fichier "DOM.html"</li>
<li>Définir les classes suivantes :</li>
<ul>
<li>crèches-ouverte<ul>C'est l'élément qui rend chaque item unique. La Map va récupérer cet élément pour créer les marqueurs. C'est l'élément parent qu'on affichera au clic sur un marqueur</ul></li>
<li>h3-cr-che<ul>C'est le nom qui sera affiché dans le marqueur</ul></li>
<li>h3-map-pin<ul>C'est le format du marqueur</ul></li>
<li>gmaplink<ul>A configurer comme sur le fichier "champ-google-map.png" et à cacher à l'écran</ul></li>
</ul>
<li>Cacher la COLLECTION LIST nouvellement créé</li>
<li>Mettre en forme l'élément <div id="detailcrech" ...> <ul>Il sera affiché tel quel tant qu'aucun marqueur ne sera cliqué</ul></li>
<li>copier / coller le code du fichier head.html dans le <head> de la page webflow concerné</li>
<li>copier / coller le code du fichier map.html dans un élément EMBED HTML sur la page webflow concerné</li>
</ol>

Bien sûr, vous pouvez modifier le nom des classes. Pensez à les modifier dans le code <head.html>
