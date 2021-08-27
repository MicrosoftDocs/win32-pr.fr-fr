---
title: Techniques courantes pour améliorer les mappages de profondeur d’ombre
description: Cet article technique fournit une vue d’ensemble de certains algorithmes de mappage de profondeur de tons foncés courants et des artefacts courants, et explique plusieurs techniques, allant des problèmes de base à intermédiaire, qui peuvent être utilisées pour augmenter la qualité des cartes fictives standard.
ms.assetid: bf994838-a261-0379-9301-eb9b250d216c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aafff1b537830ae0ee681ed32932cca2b6274a4d9da3e0471ef498e0bef2d483
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102469"
---
# <a name="common-techniques-to-improve-shadow-depth-maps"></a>Techniques courantes pour améliorer les mappages de profondeur d’ombre

Les mappages d’ombres, introduits dans 1978, sont une technique courante pour ajouter des ombres aux jeux. Trois décennies plus tard, malgré les avancées matérielles et logicielles, les artefacts occultants, à savoir la scintillement des bords, l’utilisation des alias de perspective et d’autres problèmes de précision, persistent.

Cet article technique fournit une vue d’ensemble de certains algorithmes de mappage de profondeur de tons foncés courants et des artefacts courants, et explique plusieurs techniques, allant des problèmes de base à intermédiaire, qui peuvent être utilisées pour augmenter la qualité des cartes fictives standard. L’ajout de mappages d’ombres de base à un titre est généralement simple, mais la compréhension des nuances des artefacts d’ombre peut être difficile. Cet article technique est destiné aux développeurs de graphiques intermédiaires qui ont implémenté des ombres, mais ne comprend pas entièrement pourquoi des artefacts spécifiques s’affichent et ne vous empêche pas de les contourner.

La sélection des techniques appropriées pour limiter les artefacts spécifiques n’est pas négligeable. En cas de défaillance de la carte fictive, la différence de qualité peut être impressionnante (figure 1). L’implémentation correcte de ces techniques améliore radicalement les ombres standard. Les techniques expliquées dans cet article sont implémentées dans l’exemple de CascadedShadowMaps11 dans le kit de développement logiciel (SDK) DirectX.

**Figure 1. Shadows avec des artefacts graves (à gauche) et des ombres après avoir implémenté les techniques décrites dans cet article (à droite)**

![Shadows avec des artefacts graves (à gauche) et des ombres après avoir implémenté les techniques décrites dans cet article (à droite)](images/shadows-before-and-after.jpg)

## <a name="shadow-depth-maps-review"></a>profondeur de l’ombre Cartes révision

L’algorithme de mappage de profondeur d’ombre est un algorithme à deux passes. La première passe génère une carte de profondeur dans l’espace clair. Dans la deuxième passe, cette carte est utilisée pour comparer la profondeur de chaque pixel dans l’espace clair par rapport à sa profondeur correspondante dans le mappage de profondeur d’espace clair.

**Figure 2. Éléments clés d’une scène fictive**

![éléments clés d’une scène fictive](images/key-parts-of-shadow-scene.jpg)

### <a name="pass-1"></a>Passe 1

La scène est illustrée à la figure 2. Dans la première passe (figure 3), la géométrie est rendue dans une mémoire tampon de profondeur à partir du point de vue de la lumière. Plus précisément, le nuanceur vertex transforme la géométrie en espace de vue claire.

Le résultat final de cette première passe est un tampon de profondeur contenant les informations de profondeur de la scène du point de vue de la lumière. Cela peut maintenant être utilisé dans la passe 2 pour déterminer les pixels bloqués à partir de la lumière.

**Figure 3. Première passe du mappage de clichés instantanés de base**

![première passe du mappage de clichés instantanés de base](images/first-pass-of-basic-hadow-mapping.png)

### <a name="pass-2"></a>Passe 2

Au cours de la deuxième passe (figure 4), le nuanceur vertex transforme chaque sommet à deux reprises. Chaque vertex est transformé en espace d’affichage de la caméra et passé au nuanceur de pixels comme position. Chaque vertex est également transformé par la matrice vue-projection-texture de la lumière et est passé au nuanceur de pixels comme une coordonnée de texture. La matrice vue-projection-texture est la même matrice que celle utilisée pour restituer la scène dans la passe 1 avec une transformation supplémentaire. Il s’agit d’une transformation qui met à l’échelle et traduit les points de l’espace d’affichage (– 1 à 1 dans X et Y) à l’espace de texture (de 0 à 1 dans X et de 1 à 0 dans Y).

Le nuanceur de pixels reçoit la position interpolée et les coordonnées de texture interpolées. Tout ce dont vous avez besoin pour effectuer le test de profondeur est maintenant dans cette coordonnée de texture. Le test de profondeur peut maintenant être effectué en indexant la mémoire tampon de profondeur à partir du premier passage avec les coordonnées de texture X et Y et en comparant la valeur de profondeur obtenue à la coordonnée de la texture Z.

**Figure 4. Deuxième passe du mappage de clichés instantanés de base**

![deuxième passe du mappage de clichés instantanés de base](images/second-pass-of-basic-shadow-mapping.png)

## <a name="shadow-map-artifacts"></a>Artifacts de la table de clichés instantanés

L’algorithme de mappage de profondeur d’ombre est l’algorithme d’occultation en temps réel le plus largement utilisé, mais produit toujours plusieurs artefacts nécessitant une atténuation. Les types d’artefacts qui peuvent se produire sont résumés ci-après.

### <a name="perspective-aliasing"></a>Alias de perspective

L’alias de perspective, un artefact courant, est illustré à la figure 5. Cela se produit lorsque le mappage de pixels dans l’espace d’affichage aux texels dans le mappage des ombres n’est pas un ratio un-à-un. Cela est dû au fait que les pixels proches du plan proche sont plus proches et nécessitent une résolution de plus en plus grande de la carte fictive.

La figure 6 illustre un mappage d’ombre et un frustum d’affichage. Près de l’œil, les pixels sont plus proches et de nombreux pixels correspondent aux mêmes texels d’ombre. Les pixels du plan Far sont répartis, réduisant ainsi les alias de perspective.

**Figure 5. Alias haute perspective (à gauche) et alias à faible perspective (à droite)**

![alias haute perspective (à gauche) et alias à faible perspective (à droite)](images/high-perspective-aliasing-vs-low-perspective-aliasing.jpg)

Pour l’image à gauche, l’alias de perspective est plus élevé ; un trop grand nombre de pixels d’espace œil est mappé aux mêmes texels de mappages instantanés. Dans l’image à droite, l’alias de perspective est faible, car il y a un mappage de 1:1 entre les pixels d’espace œil et les texels de la carte ombrée.

**Figure 6. Afficher les frustum avec le mappage d’ombre**

![afficher les frustum avec le mappage d’ombre](images/view-frustum-with-shadow-map.jpg)

Les pixels clairs dans le plan Far représentent les alias de faible perspective, tandis que les pixels foncés dans le plan near représentent les alias de perspective haute.

La résolution de la carte fictive peut également être trop élevée. Bien qu’une résolution plus élevée soit moins perceptible, elle peut néanmoins entraîner des petits objets, tels que des câbles téléphoniques, et non des ombres. En outre, une résolution trop élevée peut entraîner de graves problèmes de performances en raison des modèles d’accès à la texture.

Les mappages d’ombre de perspective (PSMs) et les mappages d’ombres en perspective d’espace clair (LSPSMs) tentent d’adresser des alias de perspective en inclinant la matrice de projection de la lumière afin de placer plus de texels à proximité de l’œil où elles sont nécessaires. Malheureusement, aucune technique ne peut résoudre l’alias de perspective. Le paramétrage de la transformation nécessaire pour mapper les pixels de l’espace œil aux texels dans le mappage des ombres ne peut pas être lié par un décalage linéaire. Un paramétrage logarithmique est requis. Les PSMs placent trop de détails près de l’oeil, ce qui amène les ombres éloignées à être de faible qualité ou à disparaître. Les LSPSMs permettent de mieux trouver un fond central entre une résolution plus importante et une plus grande partie de l’oeil et de laisser suffisamment de détails pour les objets. Les deux techniques dégénèrent les ombres orthographiques dans certaines configurations de scène. Cette dégénération peut être contrecarrée par le rendu d’un mappage d’ombre distinct pour chaque face de la vue frustum, bien que cela soit onéreux. Les cartes fictives de perspective logarithmique (LogPSMs) affichent également une carte séparée par face de la vue frustum. Cette technique utilise la pixellisation non linéaire pour placer plus de texels près de l’œil. Le matériel de classe D3D10 et D3D11 ne prend pas en charge la pixellisation non linéaire. Pour plus d’informations sur ces techniques et algorithmes, consultez la section Références.

Les CMS sont la technique la plus populaire pour traiter les alias de perspective. Bien que CMS puisse être combiné avec PSMs et LSPSMs, il est inutile. l’utilisation de cms pour corriger les erreurs d’alias de perspective est traitée dans l’article compagnon, [Cartes Shadow en cascade](/windows/desktop/DxTechArts/cascaded-shadow-maps).

### <a name="projective-aliasing"></a>Alias projective

L’alias projective est plus difficile à afficher que les alias de perspective. Les ombres dissimulées mises en surbrillance dans la figure 7 illustrent les erreurs d’alias projective. L’alias projective se produit lorsque le mappage entre les texels de l’espace de l’appareil photo et les texels dans l’espace clair n’est pas un ratio un-à-un. Cela est dû à l’orientation de la géométrie par rapport à la caméra légère. L’alias projective se produit lorsque le plan tangent de la géométrie devient parallèle aux rayons légers.

**Figure 7. Crénelage (High-projection alias) et alias à faible projection**

![crénelage (High-projection alias) et alias à faible projection](images/high-projective-aliasing-vs-low%20projective-aliasing.jpg)

Les techniques utilisées pour atténuer les erreurs d’alias de perspective atténuent également l’utilisation des alias projective. L’alias projective se produit lorsque la surface normale est orthogonale à la lumière ; ces surfaces doivent recevoir moins de lumière en fonction des équations d’éclairage diffus.

### <a name="shadow-acne-and-erroneous-self-shadowing"></a>Shadow-acné et Self-Shadowing erronées

Shadow acné (figure 8), un terme synonyme de l’auto-occultation erronée, se produit lorsque la table fictive quantifie la profondeur sur une Texel entière. Lorsque le nuanceur compare une profondeur réelle à cette valeur, il est très probable qu’il soit auto-ombré, car il doit être masqué.

Une autre raison pour l’acné de l’acné est que le Texel dans l’espace clair est tellement proche de la profondeur du Texel correspondant dans le mappage de profondeur que les erreurs de précision entraînent un échec erroné du test de profondeur. L’une des raisons de cette différence de précision est que la carte de profondeur a été calculée par le matériel de pixellisation à fonction fixe, tandis que la profondeur comparée a été calculée par le nuanceur. L’inversion de l’acné peut également entraîner une ombre.

**Figure 8. Artefact d’acné Shadow**

![artefact d’acné Shadow](images/shadow-acne-artifact.jpg)

Comme indiqué dans l’image de gauche, certains pixels n’ont pas réussi le test de profondeur et créé des artefacts et des motifs de moiré. Pour réduire l’auto-occultation erronée, les limites sur le plan proche et le plan lointain pour la vue de l’espace clair frustum doivent être calculées aussi étroitement que possible. L’écart de profondeur basé sur l’échelle de la pente et les autres types de biais sont les autres solutions utilisées pour atténuer l’acné des ombres.

### <a name="peter-panning"></a>Panorama Peter

Le terme « *Peter panoramisation* » dérive son nom du livre d’enfants dont l’ombre a été détachée et qui peut voler. Cet artefact permet de détacher des objets avec des ombres manquantes et de les faire flotter au-dessus de la surface (figure 9).

**Figure 9. Objet panoramique Peter**

![objet panoramique Peter](images/peter-panning-artifact.jpg)

Dans l’image de gauche, l’ombre est détachée de l’objet, ce qui crée un effet flottant.

Une technique pour la suppression de l’acné de surface consiste à ajouter une valeur à la position de pixel dans l’espace clair ; C’est ce que l’on appelle ajouter un décalage de profondeur. Peter panoramique des résultats lorsque le décalage de profondeur utilisé est trop grand. Dans ce cas, le décalage de profondeur force le test de profondeur à passer à tort. À l’instar de l’acné Shadow, Peter panoramisation est aggravé lorsque la précision est insuffisante dans le tampon de profondeur. Le calcul des plans étroits et des plans lointains permet également d’éviter Peter panoramisation.

## <a name="techniques-to-improve-shadow-maps"></a>Techniques pour améliorer le Cartes Shadow

L’ajout d’ombres à un titre est un processus. La première étape consiste à faire fonctionner les cartes fictives de base. La seconde consiste à s’assurer que tous les calculs de base sont effectués de façon optimale : Frusta s’adaptent aussi étroitement que possible, les plans proches/Far s’ajustent fortement, l’écart à l’échelle de la pente est utilisé, et ainsi de suite. Une fois que les ombres de base sont activées et qu’elles s’affichent aussi bien que possible, le développeur a une meilleure idée des algorithmes nécessaires pour obtenir les ombres pour une fidélité suffisante. Les conseils de base qui peuvent être nécessaires pour obtenir des cartes fictives de base en examinant les meilleurs résultats sont fournis dans cette section.

### <a name="slope-scale-depth-bias"></a>Slope-Scale décalage de profondeur

Comme mentionné précédemment, l’auto-occultation peut entraîner une ombre de l’acné. L’ajout d’un décalage trop grand peut entraîner la panoramisation de Peter. En outre, les polygones avec des pentes abruptes (par rapport à la lumière) sont plus retirés de l’alias projective que les polygones avec des pentes superficielles (par rapport à la lumière). Pour cette raison, chaque valeur de mappage de profondeur peut avoir besoin d’un décalage différent selon la pente du polygone par rapport à la lumière.

Le matériel Direct3D 10 a la possibilité de biaiser un polygone en fonction de sa pente par rapport à la direction de la vue. Cela a pour effet d’appliquer un grand décalage à un polygone qui est visualisé sur la direction de la lumière, mais qui n’applique pas de biais à un polygone situé directement à l’extrémité de la lumière. La figure 10 illustre la manière dont deux pixels voisins peuvent alterner entre les clichés instantanés et non ombrés lorsqu’ils sont testés par rapport à la même pente non biaisée.

**Figure 10. Décalage de profondeur de pente décalée par rapport à la profondeur non biaisée**

![décalage de profondeur de pente décalée par rapport à la profondeur non biaisée](images/slope-scaled-depth-bias-compared-to-unbiased-depth.png)

### <a name="calculating-a-tight-projection"></a>Calcul d’une projection étroite

L’ajustement étroit de la projection de la lumière sur la vue frustum augmente la couverture de la carte fictive. La figure 11 illustre que l’utilisation d’une projection arbitraire, ou l’ajustement de la projection aux limites de la scène, produit des alias de perspective plus élevée.

**Figure 11. Cliché instantané arbitraire frustum et Shadow frustum ajuster à la scène**

![cliché instantané arbitraire frustum et Shadow frustum ajuster à la scène](images/arbitrary-shadow-frustum-and-shadow-frustum-fit-to-scene.jpg)

La vue est à partir du point de vue de la lumière. La trapèze représente le frustum de l’appareil photo de la vue. La grille dessinée sur l’image représente le mappage des ombres. L’image à droite montre que le même mappage de cliché instantané de résolution crée une couverture plus Texel lorsqu’elle s’ajuste plus étroitement à la scène.

La figure 12 illustre les frustums qui s’adaptent correctement. Pour calculer la projection, les huit points qui composent la vue frustum sont transformés en espace clair. Ensuite, les valeurs minimale et maximale dans X et Y sont trouvées. Ces valeurs composent les limites d’une projection orthographique.

**Figure 12. Projection de l’ombre ajuster pour afficher frustum**

![projection de l’ombre ajuster pour afficher frustum](images/shadow-projection-fit-to-view-frustum.jpg)

Il est également possible de détourer le frustum en AABB de scène pour obtenir une liaison plus étroite. Cela n’est pas recommandé dans tous les cas, car cela peut modifier la taille de la projection de la caméra légère du cadre en Frame. De nombreuses techniques, telles que celles décrites dans la section déplacement de la lumière Texel-Sized incréments, donnent de meilleurs résultats lorsque la taille de la projection de la lumière reste constante dans chaque cadre.

### <a name="calculating-the-near-plane-and-far-plane"></a>Calcul du plan proche et du plan lointain

Le plan proche et le plan Far sont les éléments finaux requis pour calculer la matrice de projection. Plus les plans sont rapprochés, plus les valeurs de la mémoire tampon de profondeur sont précises.

La mémoire tampon de profondeur peut être 16 bits, 24 bits ou 32 bits, avec des valeurs comprises entre 0 et 1. En règle générale, les mémoires tampons de profondeur sont des points fixes, les valeurs proches du plan proche étant regroupées plus étroitement que les valeurs proches du plan Far. Le degré de précision disponible pour la mémoire tampon de profondeur est déterminé par le rapport entre le plan near et le plan Far. L’utilisation du plan proche/Far le plus étroit pourrait permettre l’utilisation d’une mémoire tampon de profondeur 16 bits. Une mémoire tampon de profondeur de 16 bits peut réduire l’utilisation de la mémoire tout en renforçant la vitesse de traitement.

### <a name="aabb-based-near-plane-and-far-plane"></a>AABB-Based près du plan et du plan lointain

Un moyen simple et naïve de calculer le plan proche et le plan lointain consiste à transformer le volume englobant de la scène en espace clair. La plus petite valeur de la coordonnée Z est le plan near et la plus grande valeur de la coordonnée Z est le plan Far. Pour de nombreuses configurations de la scène et de la lumière, cette approche est suffisante. Toutefois, le pire scénario peut entraîner une perte significative de précision dans le tampon de profondeur ; La figure 13 illustre un tel scénario. Ici, la plage du plan near vers le plan FAR est quatre fois supérieure à celle nécessaire.

La vue frustum de la figure 13 a été intentionnellement choisie comme petite. Une petite vue frustum est affichée dans une très grande scène composée de piliers s’étendant à partir de l’appareil photo de la vue. L’utilisation de la scène AABB pour les plans near et Far n’est pas optimale. l’algorithme CSM décrit dans l’article technique de l' [ombre en cascade Cartes](/windows/desktop/DxTechArts/cascaded-shadow-maps) doit calculer des plans proches et éloignés pour les frustums de très petite taille.

**Figure 13. Plans near et Far basés sur la scène AABB**

![plans near et Far basés sur la scène AABB](images/near-far-%20planes-based-on-scene-aabb.jpg)

### <a name="frustum-based-near-plane-and-far-plane"></a>Frustum-Based près du plan et du plan lointain

Une autre technique pour calculer les plans near et Far consiste à transformer le frustum en espace clair et à utiliser les valeurs minimales et maximales en Z comme les plans near et Far, respectivement. La figure 14 illustre les deux problèmes de cette approche. Tout d’abord, le calcul est trop prudent, comme indiqué lorsque le frustum s’étend au-delà de la géométrie de la scène. Deuxièmement, le plan proche peut être trop étroit, provoquant le rognage des conversions de clichés instantanés.

**Figure 14. Plans near et Far basés uniquement sur la vue frustum**

![plans near et Far basés uniquement sur la vue frustum](images/near-far-planes-based-solely-on-view-frustum.jpg)

### <a name="light-frustum-intersected-with-scene-to-calculate-near-and-far-planes"></a>Frustum clair avec intersection avec la scène pour calculer des plans proches et éloignés

La méthode appropriée pour calculer les plans near et FAR est illustrée à la figure 15. Quatre des plans de la lumière orthographique frustum ont été calculés en utilisant la valeur minimale et la valeur maximale des coordonnées X et Y de la vue frustum dans l’espace clair. Les deux derniers plans de la vue orthogonale frustum sont les plans near et Far. Pour rechercher ces plans, les limites de la scène sont découpées par rapport aux quatre plans frustum de lumière connus. Les plus petites et les plus grandes valeurs Z de la limite nouvellement coupée représentent respectivement le plan proche et le plan Far.

Le code qui effectue cette opération se trouve dans l’exemple CascadedShadowMaps11. Les huit points qui composent les AABB du monde sont transformés en espace clair. La transformation des points en espace clair simplifie les tests de découpage. Les quatre plans connus du frustum clair peuvent maintenant être représentés sous forme de lignes. Le volume englobant des scènes dans l’espace clair peut être représenté sous la forme de six quadrilatères. Ces 6 quadrilatères peuvent ensuite être convertis en 12 triangles pour le découpage en triangle. Les triangles sont découpés par rapport aux plans connus de la vue frustum (il s’agit de lignes horizontales et verticales dans X et Y dans un espace clair). Quand un point d’intersection est trouvé dans X et Y, le triangle 3D est coupé à ce stade. Les valeurs Z minimale et maximale de tous les triangles découpés sont le plan proche et le plan lointain. L’exemple CascadedShadowMaps11 montre comment effectuer ce découpage dans la fonction **ComputeNearAndFar** .

Il existe deux autres techniques qui peuvent être utilisées pour calculer les plans near et Far les plus étroits. Ces techniques ne sont pas affichées dans l’exemple CascadedShadowMaps.

-   Même des plans proches et Far plus étroits pourraient être calculés en croisant une hiérarchie d’une scène ou d’objets individuels dans une scène par rapport au frustum clair. Il s’agit d’un calcul plus complexe. Bien que cela ne soit pas illustré dans l’exemple CascadedShadowMaps11, il peut s’agir d’une technique valide pour certaines vignettes.
-   Le plan Far peut être calculé en utilisant la valeur minimale suivante :

    -   Profondeur la plus grande de la vue frustum dans l’espace clair.
    -   Profondeur la plus grande de l’intersection de la vue frustum et de la scène AABB.

Cette approche peut être problématique lorsqu’elle est utilisée avec des cartes fictives en cascade où il est possible d’indexer en dehors d’une vue frustum. Dans ce cas, il se peut que la géométrie du mappage d’ombre soit manquante.

**Figure 15. Plans near et Far basés sur l’intersection des quatre plans calculés de la lumière frustum et de la géométrie englobante de la scène**

![plans near et Far basés sur l’intersection des quatre plans calculés de la lumière frustum et de la géométrie englobante de la scène](images/near-far-plane-based-on-intersection-of-four.jpg)

### <a name="moving-the-light-in-texel-sized-increments"></a>Déplacement de la lumière dans les incréments de Texel-Sized

Un artefact courant dans les clichés instantanés est l’effet de contour de scintillement. Lors du déplacement de l’appareil photo, les pixels situés le long des bords de l’ombre se illuminent et assombrissent. Cela ne peut pas être observé dans les images fixes, mais il est très perceptible et gênant en temps réel. La figure 16 met en évidence ce problème et la figure 17 montre l’aspect des bords de l’ombre.

L’erreur de bord de scintillement se produit car la matrice de projection légère est recalculée à chaque déplacement de l’appareil photo. Cela crée des différences subtiles dans les cartes fictives générées. Tous les facteurs suivants peuvent influencer la matrice créée pour lier la scène.

-   Taille de la vue frustum
-   Orientation de la vue frustum
-   Emplacement de la lumière
-   Emplacement de l’appareil photo

Chaque fois que cette matrice change, les bords des ombres peuvent changer.

**Figure 16. Scintillement des bords de l’ombre**

![scintillement des bords de l’ombre](images/shimmering-shadow-edges.jpg)

Les pixels situés le long de la bordure de l’ombre entrent et sortent de l’ombre lorsque l’appareil photo se déplace de gauche à droite.

**Figure 17. Ombres sans scintillement des bords**

![ombres sans scintillement des bords](images/shadows-without-shimmering-edges.jpg)

Les bords de l’ombre restent constants lorsque l’appareil photo se déplace de gauche à droite.

Pour les lumières directionnelles, la solution à ce problème consiste à arrondir la valeur minimale/maximale dans X et Y (qui composent les limites de projection orthographique) aux incréments de taille de pixel. Cela peut être fait avec une opération de division, une opération Floor et une multiplication.


```C++
        vLightCameraOrthographicMin /= vWorldUnitsPerTexel;
        vLightCameraOrthographicMin = XMVectorFloor( vLightCameraOrthographicMin );
        vLightCameraOrthographicMin *= vWorldUnitsPerTexel;
        vLightCameraOrthographicMax /= vWorldUnitsPerTexel;
        vLightCameraOrthographicMax = XMVectorFloor( vLightCameraOrthographicMax );
        vLightCameraOrthographicMax *= vWorldUnitsPerTexel;
```



La valeur vWorldUnitsPerTexel est calculée en acceptant une limite de la vue frustum et en la divisant par la taille de la mémoire tampon.


```C++
        FLOAT fWorldUnitsPerTexel = fCascadeBound /
        (float)m_CopyOfCascadeConfig.m_iBufferSize;
        vWorldUnitsPerTexel = XMVectorSet( fWorldUnitsPerTexel, fWorldUnitsPerTexel,                            0.0f, 0.0f );
```



Le délimitation de la taille maximale de la vue frustum produit un ajustement plus faible pour la projection orthographique.

Il est important de noter que la texture a une largeur et une hauteur de 1 pixel supérieures lors de l’utilisation de cette technique. Cela permet de conserver les coordonnées fantômes de l’indexation en dehors du mappage des ombres.

### <a name="back-face-and-front-face"></a>Face arrière et face avant

Les clichés instantanés doivent être rendus avec l’élimination des faces arrière standard, un processus qui ignore la pixellisation des objets que la visionneuse ne peut pas voir et accélère le rendu de la scène. Une autre option courante consiste à restituer des cartes fictives avec l’élimination de face avant activée, ce qui signifie que les objets qui sont confrontés à la visionneuse sont éliminés. L’argument pour cela est qu’il aide à l’auto-ombrage lorsque la géométrie qui compose l’arrière des objets est légèrement décalée. Cette idée présente deux problèmes.

-   Tout objet avec une géométrie frontale ou face arrière incorrecte provoque des artefacts dans le mappage des ombres. Toutefois, si la géométrie frontale ou la face arrière est incorrecte, d’autres problèmes peuvent survenir. par conséquent, il peut être prudent de supposer que la géométrie frontale et la géométrie de face arrière sont correctement effectuées. Il peut être difficile de créer des faces arrière pour une géométrie basée sur des sprites telles que des feuillages.
-   Peter panoramiques et clichés instantanés proches de la base d’objets tels que les murs sont plus susceptibles de se produire car la disparité de la profondeur de l’ombre est trop petite.

### <a name="shadow-mapfriendly-geometry"></a>Mappage des ombres-géométrie conviviale

La création d’une géométrie qui fonctionne correctement dans les clichés instantanés offre davantage de souplesse lors de la lutte contre les artefacts tels que Peter panoramique et Shadow-acné.

Les bords fixes sont problématiques pour l’auto-ombrage. La disparité de profondeur près de la pointe de la périphérie est très petite. Même un décalage réduit peut entraîner la perte des ombres des objets (figure 18).

**Figure 18. Des arêtes nettes entraînent des artefacts à partir de la disparité de faible profondeur avec des décalages**

![des arêtes nettes entraînent des artefacts à partir de la disparité de faible profondeur avec des décalages](images/sharp-edges-cause%20artifacts.jpg)

Les objets étroits tels que les murs doivent avoir des arrières, même s’ils ne sont jamais visibles. Cela augmentera la disparité de profondeur.

Il est également important de s’assurer que la direction vers laquelle la géométrie est dirigée est correcte. autrement dit, l’extérieur d’un objet doit être orienté vers l’arrière et l’intérieur d’un objet doit être frontal. Cela est important pour le rendu avec l’élimination de face arrière activée, ainsi que pour la lutte contre les effets d’un décalage de profondeur.

## <a name="summary"></a>Résumé

Les techniques décrites dans cet article peuvent être utilisées pour augmenter la qualité des cartes fictives standard. L’étape suivante consiste à examiner les techniques qui peuvent fonctionner correctement avec les mappages d’ombres standard. Les CMS sont recommandés comme une technique supérieure pour combattre les alias de perspective. Vous pouvez utiliser des mappages de filtrage ou de variance de pourcentage plus rapprochés pour adoucir les bords de l’ombre. pour plus d’informations, consultez l’article technique de l' [ombre en cascade Cartes](/windows/desktop/DxTechArts/cascaded-shadow-maps) .

Donnelly, W. et Lauritzen, A. [Variance Cartes](https://portal.acm.org/citation.cfm?doid=1111411.1111440). Congrès sur les graphiques 3D interactifs, les procédures du congrès 2006 sur les jeux et les graphiques 3D interactifs. 2006, pp. 161 – 165.

Engel, Woflgang F. section 4. Cartes d’ombre en cascade. ShaderX5, *techniques de rendu avancées*, Wolfgang F. Engel, Ed. Charles River un support, Boston, Massachusetts. 2006. pp. 197 – 206.

Stamminger, Marc et Drettakis, George. [Cartes d’ombre de Perspective](https://portal.acm.org/citation.cfm?id=566616). Conférence internationale sur les graphiques informatiques et les techniques interactives, *les procédures du 29 Conférence annuelle sur les graphiques informatiques et les techniques interactives*. 2002, pp 557-562.

Wimmer, M., Scherzer, D., and Purgathofer, W. [lighting Space Perspective Cartes](https://www.cg.tuwien.ac.at/research/vr/lispsm/shadows_egsr2004_revised.pdf). Congrès Eurographics sur le rendu. 2004. Révision le 10 juin 2005. [Technische Universität Wien](https://www.cg.tuwien.ac.at/research/vr/lispsm/).

 

 
