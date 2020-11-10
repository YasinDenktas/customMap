## **Pourquoi un custom map ?**

Webflow offre la possibilité d'[intégrer des maps](https://university.webflow.com/lesson/map) simplement mais on est vite limité. On ne peut pas intégrer plusieurs endroits, ni personnaliser les marqueurs ou ajouter des évènements DOM. Pour palier à cela, j'ai créé un EMBED HTML à intégrer dans le HEAD de la page Webflow.

## **Comment utiliser la customMap ?**

1. Créer une collection où on va stocker tous les points à afficher (dans mon exemple, des crèches)
2. Ajouter un champ "Lien Google Map" dans la collection et renseigner le lien de la page google. Exemple : [https://www.google.com/maps/place/Micro-Cr%C3%A8che+des+Anges+d'Illkirch/@48.5282431,7.7078054,17z/data=!3m1!4b1!4m5!3m4!1s0x4796ca11a42a2611:0xeaec77a351736b9!8m2!3d48.5282396!4d7.7099941](https://www.google.com/maps/place/Micro-Cr%C3%A8che+des+Anges+d'Illkirch/@48.5282431,7.7078054,17z/data=!3m1!4b1!4m5!3m4!1s0x4796ca11a42a2611:0xeaec77a351736b9!8m2!3d48.5282396!4d7.7099941)
3. Ajouter un élément COLLECTION LIST en reproduisant la structure du fichier "DOM.html"
4. Définir les classes suivantes :
    - crèches-ouverte
        - C'est l'élément qui rend chaque item unique. La Map va récupérer cet élément pour créer les marqueurs. C'est l'élément parent qu'on affichera au clic sur un marqueur
    - h3-cr-che
        - C'est le nom qui sera affiché dans le marqueur
    - h3-map-pin
        - C'est le format du marqueur
    - gmaplink
        - A configurer comme sur le fichier "champ-google-map.png" et à cacher à l'écran
5. Cacher la COLLECTION LIST nouvellement créé
    - Mettre en forme l'élément. Il sera affiché tel quel tant qu'aucun marqueur ne sera cliqué
6. Copier / coller le code du fichier head.html dans le de la page webflow concerné
7. Copier / coller le code du fichier map.html dans un élément EMBED HTML sur la page webflow concerné
    - Bien sûr, vous pouvez modifier le nom des classes. Pensez à les modifier dans le code <head.html>
8. Mettre en forme l'élément dont le id est "detailcreche"
    - Il sera affiché tel quel tant qu'aucun marqueur ne sera cliqué
9. Copier / coller le code du fichier head.html dans le "head" de la page webflow concerné

    Changer la clé API par votre clé d'API google MAP. Si vous n'en avez pas, suivez ce [tutoriel](https://developers.google.com/maps/documentation/javascript/get-api-key?hl=fr&utm_source=google&utm_medium=cpc&utm_campaign=FY18-Q2-global-demandgen-paidsearchonnetworkhouseads-cs-maps_contactsal_saf&utm_content=text-ad-none-none-DEV_c-CRE_321592199415-ADGP_Hybrid)

10. Copier / coller le code du fichier map.html dans un élément EMBED HTML sur la page webflow concerné Bien sûr, vous pouvez modifier le nom des classes. Pensez à les modifier dans le code <head.html>
