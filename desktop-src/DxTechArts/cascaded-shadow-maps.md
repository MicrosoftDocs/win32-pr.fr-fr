---
title: Mappages d’ombres en cascade (CSM)
description: Les mappages d’ombre en cascade (CMS) constituent la meilleure façon de combattre l’une des erreurs les plus courantes avec l’utilisation d’un alias de perspective de masquage.
ms.assetid: d3570d0a-74e0-5b9c-6586-c933f630c4ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29498dc882133215c910f3bd6caa5966aa0e141aaf4f7a68051834d33f2a3b16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118649660"
---
# <a name="cascaded-shadow-maps"></a>Mappages d’ombres en cascade (CSM)

Les cartes d’ombre en cascade (CMS) constituent la meilleure façon de combattre l’une des erreurs les plus courantes avec l’occultation : l’utilisation des alias de perspective. Cet article technique, qui suppose que le lecteur est familiarisé avec le mappage des clichés instantanés, aborde le sujet de CMS. Plus précisément, il :

-   explique la complexité de CMS ;
-   donne des détails sur les variations possibles des algorithmes CSM.
-   décrit les deux techniques de filtrage les plus courantes : le filtrage en pourcentage plus proche (PCF) et le filtrage avec les mappages d’ombre de variance (VSMs);
-   identifie et traite certains des pièges courants associés à l’ajout du filtrage à CMS ; les
-   montre comment mapper des CMS à Direct3D 10 via le matériel Direct3D 11.

Vous trouverez le code utilisé dans cet article dans le kit de développement logiciel (SDK) DirectX dans les exemples CascadedShadowMaps11 et VarianceShadows11. cet article s’avère très utile après l’implémentation des techniques présentées dans l’article technique, ainsi que des [techniques courantes pour améliorer la profondeur de l’ombre Cartes](/windows/desktop/DxTechArts/common-techniques-to-improve-shadow-depth-maps), sont implémentées.

## <a name="cascaded-shadow-maps-and-perspective-aliasing"></a>Cartes d’ombre en cascade et alias de Perspective

L’alias de perspective dans une table fictive est l’un des problèmes les plus difficiles à surmonter. dans l’article technique, les techniques courantes d’amélioration de la profondeur de l’ombre Cartes, les alias de perspective sont décrits et certaines approches permettant d’atténuer le problème sont identifiées. En pratique, CMS a tendance à être la meilleure solution et est couramment utilisée dans les jeux modernes.

Le concept de base de CMS est facile à comprendre. Les différentes zones de l’appareil photo frustum nécessitent des cartes fictives avec des résolutions différentes. Les objets les plus proches de l’oeil requièrent une résolution supérieure à celle des objets distants. En fait, lorsque l’œil se déplace très près de la géométrie, les pixels les plus proches de l’œil peuvent nécessiter une résolution tellement importante que même un mappage d’ombre de 4096 × 4096 est insuffisant.

L’idée de base de CMS est de partitionner le frustum en plusieurs Frusta. Un mappage d’ombre est rendu pour chaque subfrustum ; le nuanceur de pixels est ensuite un échantillon de la carte qui correspond le mieux à la résolution requise (figure 2).

**Figure 1. Couverture des clichés instantanés**

![couverture des clichés instantanés](images/shadow-map-coverage.png)

Dans la figure 1, la qualité est indiquée (de gauche à droite) de la plus élevée à la plus faible. La série de grilles représentant des cartes fictives avec un affichage frustum (cône inversé en rouge) montre comment la couverture des pixels est affectée avec différentes cartes d’ombre de résolution. Les ombres sont de qualité supérieure (pixels blancs) lorsqu’il y a un rapport de 1:1 pixels de correspondance dans l’espace clair aux texels dans le mappage des ombres. L’alias de perspective se présente sous la forme de cartes de textures de grande taille (image de gauche) quand un trop grand nombre de pixels est mappé au même Texel d’ombre. Lorsque le mappage d’ombre est trop grand, il est sous échantillonné. Dans ce cas, les texels sont ignorés, les artefacts de scintillement sont introduits et les performances sont affectées.

**Figure 2. Qualité de l’ombre CSM**

![qualité de l’ombre CSM](images/csm-shadow-quality.png)

La figure 2 montre des découpages à partir de la section de qualité la plus élevée dans chaque carte fictive de la figure 1. Le mappage des ombres avec les pixels les plus rapprochés (au sommet) est le plus proche de l’œil. Techniquement, il s’agit de cartes de la même taille, avec le blanc et le gris utilisés pour illustrer la réussite du mappage des ombres en cascade. Le blanc est idéal, car il montre une couverture correcte, soit un ratio 1:1 pour les pixels d’espace œil et les texels de la carte fictive.

CMS requièrent les étapes suivantes par frame.

1.  Partitionnez le frustum dans subfrusta.
2.  Calcule une projection orthographique pour chaque subfrustum.
3.  Affichez un mappage d’ombre pour chaque subfrustum.
4.  Affiche la scène.

    1.  Liez les mappages d’ombre et le rendu.
    2.  Le nuanceur vertex effectue les opérations suivantes :

        -   Calcule des coordonnées de texture pour chaque subfrustum de lumière (sauf si la coordonnée de texture nécessaire est calculée dans le nuanceur de pixels).
        -   Transforme et illumine le vertex, et ainsi de suite.

    3.  Le nuanceur de pixels effectue les opérations suivantes :

        -   Détermine le mappage des ombres approprié.
        -   Transforme les coordonnées de texture si nécessaire.
        -   Échantillonne l’en cascade.
        -   Illumine le pixel.

## <a name="partitioning-the-frustum"></a>Partitionnement du frustum

Le partitionnement du frustum est l’acte de création de subfrusta. L’une des techniques permettant de fractionner le frustum consiste à calculer les intervalles de 0 à 100% sur l’axe Z. Chaque intervalle représente ensuite un plan proche et un plan Far sous la forme d’un pourcentage de l’axe Z.

**Figure 3. Afficher les frustums partitionnés arbitrairement**

![afficher les frustums partitionnés arbitrairement](images/view-frustums-partitioned-arbitrarily.png)

Dans la pratique, le recalcul des fractionnements de frustum par image entraîne un scintillement des bords de l’ombre. La pratique généralement acceptée consiste à utiliser un ensemble statique d’intervalles en cascade par scénario. Dans ce scénario, l’intervalle le long de l’axe Z est utilisé pour décrire un subfrustum qui se produit lors du partitionnement du frustum. La détermination des intervalles de taille corrects pour une scène donnée dépend de plusieurs facteurs.

### <a name="orientation-of-the-scene-geometry"></a>Orientation de la géométrie de la scène

En ce qui concerne la géométrie de scène, l’orientation de l’appareil photo affecte la sélection de l’intervalle en cascade. Par exemple, un appareil photo très proche du sol, tel qu’un appareil photo terrestre dans un jeu de football, a un ensemble statique différent d’intervalles en cascade qu’un appareil photo du ciel.

La figure 4 montre des caméras différentes et leurs partitions respectives. Lorsque la plage Z de la scène est très volumineuse, davantage de plans de fractionnement sont nécessaires. Par exemple, lorsque l’œil est très proche du plan de masse, mais que les objets distants sont toujours visibles, plusieurs cascades peuvent être nécessaires. En divisant le frustum afin que davantage de fractionnements soient proches de l’œil (où les alias de perspective changent le plus rapide) est également utile. Lorsque la plus grande partie de la géométrie est divisée en une petite section (telle qu’une vue de traitement ou un simulateur de vol) de la vue frustum, moins de cascades sont nécessaires.

**Figure 4. Différentes configurations nécessitent des fractionnements de frustum différents**

![différentes configurations nécessitent des fractionnements de frustum différents](images/different-configurations-require-different-frustum-splits.png)

Gauche Lorsque Geometry a une plage dynamique élevée en Z, un grand nombre de cascades sont nécessaires. Gestionnaire Lorsque la géométrie a une plage dynamique faible dans Z, il y a peu d’avantages par rapport à plusieurs frustums. Approprié Seules trois partitions sont nécessaires lorsque la plage dynamique est moyenne.

### <a name="orientation-of-the-light-and-the-camera"></a>Orientation de la lumière et de l’appareil photo

La matrice de projection de chaque cascade est adaptée à son subfrustum correspondant. Dans les configurations où l’appareil photo de vue et les directions de lumière sont orthogonaux, les cascades peuvent s’ajuster étroitement avec peu de chevauchement. Le chevauchement est plus grand que la lumière et la caméra de vue passent à l’alignement parallèle (figure 5). Lorsque la lumière et l’appareil photo de la vue sont presque parallèles, on parle de « Dueling Frusta » et est un scénario très dur pour la plupart des algorithmes d’occultation. Il n’est pas rare de contraindre la lumière et l’appareil photo afin que ce scénario ne se produise pas. CMS, cependant, fonctionnent beaucoup mieux que de nombreux autres algorithmes dans ce scénario.

**Figure 5. Le chevauchement en cascade augmente, car la direction de la lumière est parallèle à la direction de la caméra**

![le chevauchement en cascade augmente, car la direction de la lumière est parallèle à la direction de la caméra](images/cascade-overlap-increases-as-light-direction-becomes.jpg)

De nombreuses implémentations de CSM utilisent des Frusta de taille fixe. Le nuanceur de pixels peut utiliser la profondeur Z pour indexer dans le tableau des cascades lorsque le frustum est fractionné dans des intervalles de taille fixe.

## <a name="calculating-a-view-frustum-bound"></a>Calcul d’un View-Frustum lié

Une fois les intervalles de frustum sélectionnés, les subfrusta sont créés à l’aide d’un des deux : ajuster à la scène et ajuster à la cascade.

### <a name="fit-to-scene"></a>Ajuster à la scène

Toutes les Frusta peuvent être créées avec le même proche plan. Cela force le chevauchement des cascades. L’exemple CascadedShadowMaps11 appelle cette technique pour s’adapter à la scène.

### <a name="fit-to-cascade"></a>Ajuster à la cascade

Vous pouvez également créer Frusta avec l’intervalle de partition réel utilisé comme plans near et Far. Cela entraîne un ajustement plus étroit, mais dégénère pour ajuster à la scène dans le cas de Dueling Frusta. Les exemples CascadedShadowMaps11 appellent cette technique s’adaptent à cascade.

Ces deux méthodes sont illustrées à la figure 6. Ajuster à cascade gaspille moins de résolution. Le problème avec fit to cascade est que la projection orthographique augmente et diminue en fonction de l’orientation de la vue frustum. La technique adapter à la scène remplit la projection orthographique de la taille maximale de la vue frustum en supprimant les artefacts qui s’affichent lorsque l’appareil photo est déplacé. [Techniques courantes pour améliorer la profondeur de l’ombre Cartes](/windows/desktop/DxTechArts/common-techniques-to-improve-shadow-depth-maps) résout les artefacts qui apparaissent lorsque la lumière se déplace dans la section « déplacement de la lumière dans des incréments de taille de texel ».

**Figure 6. Ajuster à la scène et ajuster à la cascade**

![ajuster à la scène et ajuster à la cascade](images/fit-to-scene-vs-fit-to-cascade.png)

## <a name="render-the-shadow-map"></a>Rendre le mappage des ombres

L’exemple CascadedShadowMaps11 restitue les mappages d’ombres dans une mémoire tampon de grande taille. Cela est dû au fait que PCF sur des tableaux de texture est une fonctionnalité Direct3D 10,1. Pour chaque cascade, une fenêtre d’affichage qui couvre la section de la mémoire tampon de profondeur correspondant à cette cascade est créée. Un nuanceur de pixels null est lié, car seule la profondeur est nécessaire. Enfin, la fenêtre d’affichage et la matrice fictive appropriées sont définies pour chaque cascade à mesure que les mappages de profondeur sont restitués l’un après l’autre dans le tampon d’ombre principal.

## <a name="render-the-scene"></a>Rendu de la scène

La mémoire tampon contenant les ombres est maintenant liée au nuanceur de pixels. Il existe deux méthodes pour sélectionner la cascade implémentée dans l’exemple CascadedShadowMaps11. Ces deux méthodes sont expliquées avec le code du nuanceur.

### <a name="interval-based-cascade-selection"></a>Interval-Based la sélection en cascade

**Figure 7. Sélection de cascade basée sur des intervalles**

![sélection de cascade basée sur des intervalles](images/interval-based-cascade-selection.jpg)

Dans une sélection basée sur des intervalles (figure 7), le nuanceur de sommets calcule la position dans l’espace universel du vertex.


```C++
Output.vDepth = mul( Input.vPosition, m_mWorldView ).z;
```



Le nuanceur de pixels reçoit la profondeur interpolée.


```C++
fCurrentPixelDepth = Input.vDepth;
```



La sélection en cascade basée sur des intervalles utilise une comparaison vectorielle et un produit scalaire pour déterminer le cacade correct. L' \_ \_ indicateur de nombre de cascades spécifie le nombre de cascades. Les données de m \_ fCascadeFrustumsEyeSpaceDepths \_ limitent la vue des partitions frustum. Après la comparaison, fComparison contient la valeur 1, où le pixel actuel est plus grand que le cloisonnement, et la valeur 0 lorsque la cascade actuelle est plus petite. Un produit scalaire additionne ces valeurs dans un index de tableau.


```C++
        float4 vCurrentPixelDepth = Input.vDepth;
        float4 fComparison = ( vCurrentPixelDepth > m_fCascadeFrustumsEyeSpaceDepths_data[0]);
        float fIndex = dot(
        float4( CASCADE_COUNT_FLAG > 0,
        CASCADE_COUNT_FLAG > 1,
        CASCADE_COUNT_FLAG > 2,
        CASCADE_COUNT_FLAG > 3)
        , fComparison );

        fIndex = min( fIndex, CASCADE_COUNT_FLAG );
        iCurrentCascadeIndex = (int)fIndex;
```



Une fois la cascade sélectionnée, la coordonnée de texture doit être transformée en cascade correcte.


```C++
vShadowTexCoord = mul( InterpolatedPosition, m_mShadow[iCascadeIndex] );
```



Cette coordonnée de texture est ensuite utilisée pour échantillonner la texture avec la coordonnée X et la coordonnée Y. La coordonnée Z est utilisée pour effectuer la comparaison de profondeur finale.

### <a name="map-based-cascade-selection"></a>Map-Based la sélection en cascade

Sélection basée sur une carte (figure 8) tests effectués sur les quatre côtés des cascades pour trouver le mappage le plus étroit qui couvre le pixel spécifique. Au lieu de calculer la position dans l’espace universel, le nuanceur de sommets calcule la position de l’espace d’affichage pour chaque cascade. Le nuanceur de pixels itère sur les cascades afin de mettre à l’échelle et de déplacer les coordonnées de texture afin qu’elles indexent la cascade actuelle. La coordonnée de texture est ensuite testée par rapport aux limites de texture. Lorsque les valeurs X et Y de la coordonnée de texture se trouvent dans une cascade, elles sont utilisées pour échantillonner la texture. La coordonnée Z est utilisée pour effectuer la comparaison de profondeur finale.

**Figure 8. Sélection de cascade basée sur une carte**

![sélection de cascade basée sur une carte](images/map-based-cascade-selection.jpg)

### <a name="interval-based-selection-vs-map-based-selection"></a>Sélection Interval-Based et Map-Based sélection

La sélection basée sur un intervalle est légèrement plus rapide que la sélection basée sur les mappages, car la sélection en cascade peut être effectuée directement. La sélection basée sur une carte doit croiser la coordonnée de texture avec les limites de la cascade.

La sélection basée sur une carte utilise la cascade de manière plus efficace lorsque les cartes fictives ne s’alignent pas parfaitement (voir figure 8).

## <a name="blend-between-cascades"></a>Fusion entre les cascades

VSMs (abordé plus loin dans cet article) et des techniques de filtrage telles que PCF peuvent être utilisées avec des CMS basse résolution pour produire des ombres douces. Malheureusement, cela se traduit par une jointure visible (figure 9) entre les couches de cascade, car la résolution ne correspond pas. La solution consiste à créer une bande entre les cartes fictives où le test de cliché instantané est effectué pour les deux cascades. Ensuite, le nuanceur interpole de manière linéaire entre les deux valeurs en fonction de l’emplacement du pixel dans la bande de fusion. Les exemples CascadedShadowMaps11 et VarianceShadows11 fournissent un curseur d’interface graphique qui peut être utilisé pour augmenter et diminuer cette bande floue. Le nuanceur effectue une branche dynamique afin que la grande majorité des pixels lisent uniquement la cascade actuelle.

**Figure 9. Coutures en cascade**

![coutures en cascade](images/cascade-seams.jpg)

Gauche Une jointure visible peut être affichée là où se chevauchent les cascades. Approprié Quand les cascades sont fusionnées entre, aucune jointure n’est effectuée.

## <a name="filtering-shadow-maps"></a>filtrage des Cartes Shadow

### <a name="pcf"></a>PCF

Le filtrage des mappages d’ombres ordinaires ne produit pas d’ombres floues et floues. Le matériel de filtrage brouille les valeurs de profondeur, puis compare ces valeurs floues au Texel de l’espace clair. Le bord dur résultant du test de réussite/d’échec existe toujours. Le flou des mappages d’ombres sert uniquement à déplacer le bord dur de manière erronée. PCF active le filtrage sur les cartes fictives. L’idée générale de PCF est de calculer un pourcentage du pixel dans l’ombre en fonction du nombre de sous-échantillons qui réussissent le test de profondeur sur le nombre total de sous-échantillons.

Le matériel Direct3D 10 et Direct3D 11 peut exécuter PCF. L’entrée d’un échantillonneur PCF se compose de la coordonnée de texture et d’une valeur de profondeur de comparaison. Par souci de simplicité, PCF est expliqué avec un filtre à quatre clics. L’échantillon de texture lit la texture quatre fois, de la même manière qu’un filtre standard. Toutefois, le résultat retourné est un pourcentage des pixels qui ont passé le test de profondeur. La figure 10 montre comment un pixel qui passe l’un des quatre tests de profondeur est de 25% dans une ombre. La valeur réelle retournée est une interpolation linéaire basée sur les coordonnées de sous-Texel des lectures de texture pour produire un dégradé lisse. Sans cette interpolation linéaire, le PCF à quatre clics ne peut retourner que cinq valeurs : {0,0, 0,25, 0,5, 0,75, 1,0}.

**Figure 10. Image filtrée PCF, avec 25% du pixel sélectionné couverts**

![image filtrée PCF, avec 25% du pixel sélectionné couverts](images/pcf-filtered-image.png)

Il est également possible d’effectuer PCF sans prise en charge matérielle ou d’étendre PCF à des noyaux plus importants. Certaines techniques encodent même des exemples avec un noyau pondéré. Pour ce faire, créez un noyau (tel qu’un gaussien) pour une grille N × N. Les poids doivent être additionnés à 1. La texture est ensuite échantillonnée des occurrences N2. Chaque échantillon est mis à l’échelle en fonction des pondérations correspondantes dans le noyau. L’exemple CascadedShadowMaps11 utilise cette approche.

### <a name="depth-bias"></a>Décalage de profondeur

Le décalage de profondeur devient encore plus important lorsque de gros noyaux PCF sont utilisés. Elle est uniquement valide pour comparer la profondeur d’espace clair d’un pixel au pixel auquel elle est mappée dans le mappage de profondeur. Les voisins de la représentation de la correspondance de profondeur font référence à une autre position. Cette profondeur est susceptible d’être similaire, mais elle peut être très différente en fonction de la scène. La figure 11 met en surbrillance les artefacts qui se produisent. Une seule profondeur est comparée à trois texels voisins dans le mappage des ombres. L’un des tests de profondeur échoue de manière erronée, car sa profondeur n’est pas corrélée à la profondeur de l’espace clair calculé de la géométrie actuelle. Pour résoudre ce problème, il est recommandé d’utiliser un décalage plus grand. Un décalage trop important peut toutefois entraîner Peter panoramisation. Le calcul d’un plan étroit et du plan Far permet de réduire les effets de l’utilisation d’un décalage.

**Figure 11. Auto-occultation erronée**

![Auto-occultation erronée](images/erroneous-self-shadowing.png)

Les résultats de l’auto-occultation erronés proviennent de la comparaison des pixels de la profondeur d’espace clair aux texels du mappage d’ombre qui ne sont pas corrélés. La profondeur dans l’espace clair est corrélée avec l’ombre 2 dans le mappage de profondeur. Texel 1 est supérieur à la profondeur de l’espace clair, tandis que 2 est égal à et 3 à moins. Les texels 2 et 3 réussissent le test de profondeur, tandis que Texel 1 échoue.

### <a name="calculating-a-per-texel-depth-bias-with-ddx-and-ddy-for-large-pcfs"></a>Calcul d’un écart de profondeur de Per-Texel avec DDX et DDY pour les grands PCFs

Le calcul d’un décalage de profondeur par Texel avec **ddx** et **ddy** pour des PCFs de grande taille est une technique qui calcule le décalage de profondeur correct (en supposant que la surface est planaire) pour le Texel de la carte fictive adjacente.

Cette technique correspond à la profondeur de comparaison d’un plan à l’aide des informations dérivées. Étant donné que cette technique est complexe en termes de calcul, elle doit être utilisée uniquement quand un GPU a des cycles de calcul à Spare. En cas d’utilisation de noyaux très volumineux, il peut s’agir de la seule technique qui consiste à supprimer les artefacts d’auto-occultation sans provoquer de panoramique Peter.

La figure 12 met en évidence le problème. La profondeur dans l’espace clair est connue pour le Texel qui est comparé. Les profondeurs clairs qui correspondent aux texels voisins dans le mappage de profondeur sont inconnus.

**Figure 12. Plan de scène et de profondeur**

![plan de scène et de profondeur](images/scene-and-depth-map.png)

La scène rendue est affichée à gauche et la carte de profondeur avec un exemple de bloc Texel est affichée à droite. Le Texel de l’espace œil correspond au pixel étiqueté D au centre du bloc. Cette comparaison est exacte. La profondeur de l’espace œil est correcte en corrélation avec les pixels que le voisin D est inconnu. Le mappage des texels voisins à l’espace œil est possible uniquement si nous supposons que le pixel se rapporte au même triangle que D.

La profondeur est connue pour le Texel qui se met en corrélation avec la position de l’espace clair. La profondeur est inconnue pour les texels voisins dans la carte de profondeur.

À un niveau élevé, cette technique utilise les opérations HLSL **ddx** et **ddy** pour rechercher la dérivée de la position de l’espace clair. Cela n’est pas insignifiant, car les opérations dérivées retournent le dégradé de la profondeur d’espace clair par rapport à l’espace à l’écran. Pour convertir cela en un dégradé de la profondeur d’espace clair par rapport à l’espace clair, une matrice de conversion doit être calculée.

### <a name="explanation-with-shader-code"></a>Explication du code du nuanceur

Les détails du reste de l’algorithme sont fournis comme une explication du code du nuanceur qui effectue cette opération. Ce code se trouve dans l’exemple CascadedShadowMaps11. La figure 13 montre comment les coordonnées de la texture de l’espace lumineux sont mappées à la carte de profondeur et comment les dérivés dans X et Y peuvent être utilisés pour créer une matrice de transformation.

**Figure 13. Screen-espace sur la matrice de l’espace clair**

![Screen-espace sur la matrice de l’espace clair](images/screen-space-to-light-space-matrix.png)

Les dérivés de la position de l’espace clair dans X et Y sont utilisés pour créer cette matrice.

La première étape consiste à calculer la dérivée de la position de l’espace d’affichage clair.


```C++
          float3 vShadowTexDDX = ddx (vShadowMapTextureCoordViewSpace);
          float3 vShadowTexDDY = ddy (vShadowMapTextureCoordViewSpace);
```



Les GPU de classe Direct3D 11 calculent ces dérivés en exécutant 2 × 2 Quad de pixels en parallèle et en soustrayant les coordonnées de texture du voisin dans X pour **ddx** et du voisin dans Y pour **ddy**. Ces deux dérivées composent les lignes d’une matrice 2 × 2. Dans sa forme actuelle, cette matrice peut être utilisée pour convertir les pixels voisins de l’espace à l’écran en pentes d’espaces clairs. Toutefois, l’inverse de cette matrice est nécessaire. Matrice qui transforme les pixels voisins de l’espace lumineux en pentes d’espace à l’écran.


```C++
          float2x2 matScreentoShadow = float2x2( vShadowTexDDX.xy, vShadowTexDDY.xy );
          float fInvDeterminant = 1.0f / fDeterminant;

          float2x2 matShadowToScreen = float2x2 (
          matScreentoShadow._22 * fInvDeterminant,
          matScreentoShadow._12 * -fInvDeterminant,
          matScreentoShadow._21 * -fInvDeterminant,
          matScreentoShadow._11 * fInvDeterminant );
```



**Figure 14. Espace clair vers l’espace à l’écran**

![espace clair vers l’espace à l’écran](images/light-space-to-screen-space.png)

Cette matrice est ensuite utilisée pour transformer les deux texels au-dessus et à droite du Texel actuel. Ces voisins sont représentés comme un décalage par rapport au Texel actuel.


```C++
          float2 vRightShadowTexelLocation = float2( m_fTexelSize, 0.0f );
          float2 vUpShadowTexelLocation = float2( 0.0f, m_fTexelSize );
          float2 vRightTexelDepthRatio = mul( vRightShadowTexelLocation,
          matShadowToScreen );
          float2 vUpTexelDepthRatio = mul( vUpShadowTexelLocation,
          matShadowToScreen );
```



Le rapport créé par la matrice est enfin multiplié par les dérivés de profondeur pour calculer les décalages de profondeur pour les pixels voisins.


```C++
            float fUpTexelDepthDelta =
            vUpTexelDepthRatio.x * vShadowTexDDX.z
            + vUpTexelDepthRatio.y * vShadowTexDDY.z;
            float fRightTexelDepthDelta =
            vRightTexelDepthRatio.x * vShadowTexDDX.z
            + vRightTexelDepthRatio.y * vShadowTexDDY.z;
```



Ces pondérations peuvent désormais être utilisées dans une boucle PCF pour ajouter un décalage à la position.


```C++
    for( int x = m_iPCFBlurForLoopStart; x < m_iPCFBlurForLoopEnd; ++x ) 
    {
        for( int y = m_iPCFBlurForLoopStart; y < m_iPCFBlurForLoopEnd; ++y )
            {
            if ( USE_DERIVATIVES_FOR_DEPTH_OFFSET_FLAG )
            {
            depthcompare += fRightTexelDepthDelta * ( (float) x ) +
            fUpTexelDepthDelta * ( (float) y );
            }
            // Compare the transformed pixel depth to the depth read
            // from the map.
            fPercentLit += g_txShadow.SampleCmpLevelZero( g_samShadow,
            float2(
            vShadowTexCoord.x + ( ( (float) x ) * m_fNativeTexelSizeInX ) ,
            vShadowTexCoord.y + ( ( (float) y ) * m_fTexelSize )
            ),
            depthcompare
            );
            }
     }
```



## <a name="pcf-and-csms"></a>PCF et CMS

PCF ne fonctionne pas sur les tableaux de texture dans Direct3D 10. Pour utiliser PCF, toutes les cascades sont stockées dans un grand Atlas de textures.

### <a name="derivative-based-offset"></a>Décalage de Derivative-Based

L’ajout des décalages basés sur les dérivés pour CMS présente des défis. Cela est dû à un calcul de dérivé dans un contrôle de fluide divergent. Le problème se produit en raison d’un fonctionnement fondamental des GPU. Les GPU Direct3D11 fonctionnent sur 2 × 2 Quad de pixels. Pour effectuer une dérivée, les GPU soustraient généralement la copie du pixel actuel d’une variable à partir de la copie du pixel voisin de la même variable. La façon dont cela se produit varie d’un GPU au GPU. Les coordonnées de la texture sont déterminées par une sélection en cascade basée sur une carte ou sur un intervalle. Certains pixels d’un quadruple pixel choisissent une cascade différente de celle du reste des pixels. Il en résulte des jointures visibles entre les clichés instantanés, car les décalages basés sur les dérivés sont maintenant complètement erronés. La solution consiste à exécuter la dérivée sur les coordonnées de texture d’espace de l’affichage clair. Ces coordonnées sont identiques pour chaque cascade.

### <a name="padding-for-pcf-kernels"></a>Remplissage pour les noyaux PCF

Index des noyaux PCF en dehors d’une partition en cascade si le tampon d’ombre n’est pas rempli. La solution consiste à remplir le bord extérieur de la cascade d’une moitié de la taille du noyau PCF. Elle doit être implémentée dans le nuanceur qui sélectionne la cascade et dans la matrice de projection qui doit rendre le en cascade suffisamment grand pour que la bordure soit conservée.

## <a name="variance-shadow-maps"></a>Cartes d’ombre de Variance

VSMs (consultez [écarts des clichés instantanés](https://portal.acm.org/citation.cfm?doid=1111411.1111440) par Donnelly et Lauritzen pour plus d’informations) activer le filtrage de carte d’ombre directe. Lorsque vous utilisez VSMs, toute la puissance du matériel de filtrage de texture peut être utilisée. Le filtrage trilinéaire et anisotrope (figure 15) peut être utilisé. En outre, les VSMs peuvent être flous directement par convolution. VSMs présentent certains inconvénients ; deux canaux de données de profondeur doivent être stockés (profondeur et profondeur au carré). Lorsque les ombres se chevauchent, la saignée est courante. Ils fonctionnent bien, toutefois, avec des résolutions inférieures et peuvent être combinés avec CMS.

**Figure 15. Filtrage anisotrope**

![filtrage anisotrope](images/anisotropic-filtering.png)

### <a name="algorithm-details"></a>Détails des algorithmes

Les VSMs fonctionnent en affichant la profondeur et la profondeur au carré d’un mappage de clichés instantanés sur deux canaux. Ce mappage de clichés instantanés à deux canaux peut ensuite être flou et filtré comme une texture normale. L’algorithme utilise ensuite l’inégalité de Chebychev dans le nuanceur de pixels pour estimer la fraction de la zone de pixels qui passerait le test de profondeur.

Le nuanceur de pixels récupère les valeurs de profondeur et de carré de profondeur.


```C++
        float  fAvgZ  = mapDepth.x; // Filtered z
        float  fAvgZ2 = mapDepth.y; // Filtered z-squared
```



La comparaison de profondeur est effectuée.


```C++
        if ( fDepth <= fAvgZ )
        {
        fPercentLit = 1;
        }
```



Si la comparaison de profondeur échoue, le pourcentage du pixel allumé est estimé. La variance est calculée en tant que moyenne des carrés moins la moyenne des carrés.


```C++
        float variance = ( fAvgZ2 ) − ( fAvgZ * fAvgZ );
        variance = min( 1.0f, max( 0.0f, variance + 0.00001f ) );
```



La valeur fPercentLit est estimée avec l’inégalité de Chebychev.


```C++
        float mean           = fAvgZ;
        float d              = fDepth - mean;
        float fPercentLit    = variance / ( variance + d*d );
```



## <a name="light-bleeding"></a>Saignement léger

Le plus grand inconvénient de VSMs est le saignement léger (figure 16). Un saignement lumineux se produit lorsque plusieurs conversions de clichés instantanés se occultaitnt le long des bords. VSMs ombrer les bords des ombres en fonction des disparités de profondeur. Lorsque les ombres se chevauchent, une disparité de profondeur existe au centre d’une région qui doit être masquée. Il s’agit d’un problème lié à l’utilisation de l’algorithme VSM.

**Figure 16. Saignements de la lumière VSM**

![saignements de la lumière VSM](images/vsm-light-bleeding.png)

Une solution partielle au problème consiste à élever le fPercentLit à une puissance. Cela a pour effet de amortir le flou, ce qui peut entraîner des artefacts où la disparité de profondeur est faible. Il existe parfois une valeur magique qui atténue le problème.


```C++
fPercentLit = pow( p_max, MAGIC_NUMBER );
```



Une alternative à l’augmentation du pourcentage d’éclairage sur une puissance consiste à éviter les configurations où les ombres se chevauchent. Même les configurations fictives fortement réglées présentent plusieurs contraintes sur la lumière, l’appareil photo et la géométrie. Le saignement léger est également réduit en utilisant des textures de résolution plus élevée.

Les cartes fictives de variances en couche (LVSMs) résolvent le problème au détriment de la Division des frustum en couches perpendiculaires à la lumière. Le nombre de mappages requis serait assez important quand les CMS sont également utilisés.

En outre, Andrew Lauritzen, co-auteur du document sur VSMs et auteur d’un document sur LVSMs, a abordé la combinaison de cartes fictives exponentielles (ESMs) et de VSMs pour contrecarrer la fusion d’éclairage dans un [Forum Beyond3D](https://forum.beyond3d.com/showthread.php?t=47427).

## <a name="vsms-with-csms"></a>VSMs avec CMS

L’exemple VarianceShadow11 combine VSMs et CMS. La combinaison est relativement simple. L’exemple suit les mêmes étapes que l’exemple CascadedShadowMaps11. PCF n’étant pas utilisé, les ombres sont floues dans une convolution séparable à deux passes. Le fait de ne pas utiliser PCF permet également à l’exemple d’utiliser des tableaux de texture au lieu d’un Atlas de textures. PCF sur les tableaux de texture est une fonctionnalité Direct3D 10,1.

### <a name="gradients-with-csms"></a>Dégradés avec CMS

L’utilisation de dégradés avec CMS peut produire une couture le long de la bordure entre deux cascades, comme illustré dans la figure 17. L’exemple d’instruction utilise des dérivées entre les pixels pour calculer des informations, telles que le niveau de mipmap, nécessaires au filtre. Cela pose un problème en particulier pour la sélection mipmap ou le filtrage anisotrope. Lorsque les pixels d’un quadruple prennent différentes branches dans le nuanceur, les dérivés calculés par le matériel GPU ne sont pas valides. Cela aboutit à une jointure en escalier le long du mappage d’ombre.

**Figure 17. Jointures sur les bordures en cascade en raison d’un filtrage anisotrope avec un contrôle de Flow divergent**

![jointures sur les bordures en cascade en raison d’un filtrage anisotrope avec un contrôle de Flow divergent](images/seams-on-cascade-borders-due-to-anisotropic.jpg)

Ce problème est résolu en calculant les dérivés à la position dans l’espace d’affichage clair. la coordonnée de l’espace d’affichage clair n’est pas spécifique à la cascade sélectionnée. Les dérivés calculés peuvent être mis à l’échelle en fonction de la partie de l’échelle de la matrice de texture de projection au niveau de mipmap correct.


```C++
        float3 vShadowTexCoordDDX = ddx( vShadowMapTextureCoordViewSpace );
        vShadowTexCoordDDX *= m_vCascadeScale[iCascade].xyz;
        float3 vShadowTexCoordDDY = ddy( vShadowMapTextureCoordViewSpace );
        vShadowTexCoordDDY *= m_vCascadeScale[iCascade].xyz;

        mapDepth += g_txShadow.SampleGrad( g_samShadow, vShadowTexCoord.xyz,
        vShadowTexCoordDDX, vShadowTexCoordDDY );
```



## <a name="vsms-compared-to-standard-shadows-with-pcf"></a>VSMs comparaison avec les ombres standard avec PCF

VSMs et PCF tentent tous les deux de se rapprocher de la zone de pixels qui passerait le test de profondeur. Les VSMs fonctionnent avec le matériel de filtrage et peuvent être flous avec les noyaux séparable. Les noyaux de convolution séparable sont beaucoup moins chers à implémenter qu’un noyau complet. En outre, VSMs compare une profondeur d’espace clair à une valeur de la carte de profondeur d’espace clair. Cela signifie que les VSMs n’ont pas les mêmes problèmes de décalage que PCF. Techniquement, VSMs est une profondeur d’échantillonnage sur une plus grande surface, ainsi qu’une analyse statistique. Cela est moins précis que PCF. En pratique, les VSMs effectuent un bon travail de fusion, ce qui se traduit par un décalage moins important. Comme décrit ci-dessus, le nombre un inconvénients pour VSMs est le saignement léger.

VSMs et PCF représentent un compromis entre la puissance de calcul GPU et la bande passante de texture GPU. Les VSMs requièrent plus d’opérations mathématiques pour calculer la variance. PCF requiert plus de bande passante de mémoire de texture. Les gros noyaux PCF peuvent rapidement devenir goulots d’étranglement en matière de bande passante. Avec la croissance de la puissance de calcul GPU plus rapidement que la bande passante GPU, les VSMs deviennent plus pratiques des deux algorithmes. Les VSMs sont également mieux adaptés aux mappages d’ombres de résolution inférieure en raison de la fusion et du filtrage.

## <a name="summary"></a>Récapitulatif

CMS offre une solution au problème d’alias de perspective. Il existe plusieurs configurations possibles pour obtenir la fidélité visuelle nécessaire pour un titre. PCF et VSMs sont largement utilisés et doivent être combinés avec CMS pour réduire les alias.

## <a name="references"></a>Références

Donnelly, W. et Lauritzen, A. [variance les cartes Shadow](https://portal.acm.org/citation.cfm?doid=1111411.1111440). Dans SI3D' 06 : procédure du congrès 2006 sur les jeux et les graphiques 3D interactifs. 2006. pp. 161 – 165. New York, NY, USA : ACM Press.

Lauritzen, Andrew et McCool, Michael. [Cartes fictives de variance en couches](https://portal.acm.org/citation.cfm?id=1375714.1375739&coll=GUIDE&dl=GUIDE&CFID=45360327&CFTOKEN=34578992). Procédure de l’interface graphique 2008, du 28 au 30 mai, 2008, Windsor, Ontario, Canada.

Engel, Woflgang F. section 4. Cartes d’ombre en cascade. ShaderX5, techniques de rendu avancées, Wolfgang F. Engel, Ed. Charles River un support, Boston, Massachusetts. 2006. pp. 197 – 206.

 

 