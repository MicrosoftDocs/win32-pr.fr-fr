---
title: Algorithmes de création de transformation WCS
description: Algorithmes de création de transformation WCS
ms.assetid: 526bbbfc-fb60-415d-b4f0-6a44a5d11a55
keywords:
- Système de couleurs Windows (WCS), création de transformation
- WCS (système de couleurs Windows), création de transformation
- gestion des couleurs des images, création de transformations
- gestion des couleurs, création de transformations
- couleurs, création de transformation
- création de transformation
- Création de transformations WCS
- algorithmes, création de transformation
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 418596c0e57571f3e504727d4606921d36ff9461
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/03/2021
ms.locfileid: "104552946"
---
# <a name="wcs-transform-creation-algorithms"></a>Algorithmes de création de transformation WCS

[Création de transformations](#creation-of-transforms)

 

[Exécution de transformation séquentielle](#sequential-transform-execution)

 

[Création de transformations optimisées](#creation-of-optimized-transforms)

 

[ICCProfileFromWCSProfile](#iccprofilefromwcsprofile)

 

[Préservation du noir et génération de noir](#black-preservation-and-black-generation)

 

[Vérifier la gamme](#checkgamut)

## <a name="creation-of-transforms"></a>Création de transformations

Pour expliquer correctement le fonctionnement des transformations de couleurs, il est utile d’expliquer le chemin de traitement complet via ICM 2,0 et les éléments internes de la CTE. La fonction [**CREATECOLORTRANSFORMW**](/windows/win32/api/icm/nf-icm-createcolortransformw) ICM 2,0 crée une transformation de couleur que les applications peuvent utiliser pour effectuer la gestion des couleurs. Cette fonction crée un contexte de couleur à partir du [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) et des entrées d’intention. Les intentions sont mappées à la ligne de base des algorithmes de mappage de gamme ICC. La fonction appelle ensuite la fonction ICM 2,0 [**CreateMultiProfileTransform**](/windows/desktop/api/Wingdi/) pour le traitement cohérent des couleurs. La fonction **CreateColorTransform** copie généralement les données dans la structure de transformation optimisée interne.

La fonction CreateMultiProfileTransform ICM 2,0 accepte un tableau de profils et un tableau d’intentions ou un profil de lien d’appareil unique et crée une transformation de couleur que les applications peuvent utiliser pour effectuer le mappage des couleurs. Il traite ces profils et intentions d’entrée pour créer des modèles d’appareil, des modèles d’apparence de couleur, des descriptions de limites de gamme et des modèles de mappage de couleurs. Voici comment procéder :

-   Les modèles d’appareil sont initialisés directement à partir de profils DM. Un modèle d’appareil est créé pour chaque profil dans l’appel à [**CreateMultiProfileTransform**](/windows/desktop/api/Wingdi/).
-   Les modèles d’apparence de couleur sont initialisés directement à partir de profils CAM. Il existe un profil CAM pour chaque profil dans l’appel à [**CreateMultiProfileTransform**](/windows/desktop/api/Wingdi/). Toutefois, un même profil CAM peut être spécifié pour plusieurs profils.
-   Les descriptions de limites de gamme sont initialisées à partir d’un objet modèle d’appareil et d’un objet CAM. Il existe une description de la limite de la gamme pour chaque profil dans l’appel à [**CreateMultiProfileTransform**](/windows/desktop/api/Wingdi/).
-   Les modèles de mappage de gamme sont initialisés à partir de deux limites de gamme et d’une intention. Vous devez créer un modèle de mappage de gammes entre chaque paire de modèles d’appareil créés à partir de l’appel à [**CreateMultiProfileTransform**](/windows/desktop/api/Wingdi/). Notez que cela signifie que vous utilisez un modèle de mappage de couleurs moins important que le modèle de périphérique. Étant donné que le nombre d’intentions correspond au nombre de modèles d’appareil, il y a également une intention plus autre que nécessaire. La première intention de la liste est ignorée. Vous parcourez la liste des modèles d’appareil et des intentions, en créant des modèles de mappage de gamme. Sélectionnez le premier et le deuxième modèles d’appareil et le deuxième objectif, puis initialisez le premier modèle de mappage de gammes de couleurs. Sélectionnez le deuxième et le troisième modèles d’appareil et le troisième, puis initialisez le deuxième modèle de mappage de gammes de couleurs. Continuez de cette façon jusqu’à ce que vous ayez créé tous les modèles de mappage de gammes.

Lorsque les profils ont été correctement traités et que tous les objets intermédiaires ont été créés et initialisés, vous pouvez créer la transformation CITE avec l’appel suivant. *PDestCAM* et *pDestDM* sont ceux associés au dernier profil dans l’appel à [**CreateMultiProfileTransform**](/windows/desktop/api/Wingdi/).


```C++
HRESULT CreateCITEColorTransform(
 __inout     IDeviceModel          *pSourceDM,
 __inout     IColorAppearanceModel *pSourceCAM,
 __in        GamutMapArray         *pGamutMapArray,
 __inout     IColorAppearanceModel *pDestCAM,
 __inout     IDeviceModel          *pDestDM,
             EColorTransformMode    eTransformMode,
 __deref_out IColorTransform      **ppCTS
 );
```



## <a name="support-for-plug-ins"></a>Prise en charge des plug-ins

L’un des problèmes impliqués dans la configuration de la transformation consiste à vérifier si un plug-in requis est disponible. Le commutateur de modèle suivant fournit cette stratégie pour contrôler ce comportement. La gestion de cette liste de transformations est une méthode dans la structure de transformation optimisée interne, mais chaque méthode de modèle fournit le pointeur à lui-même et son propre ensemble de valeurs de paramètre.

Le mode doit être l’un des éléments suivants.

-   TfmRobust : si un profil de mesure spécifie un plug-in préféré et que le plug-in n’est pas disponible, le nouveau système CTE utilise le plug-in de ligne de base. Si aucun plug-in n’est disponible, la transformation signale une erreur.
-   TfmStrict : si le ColorContext spécifie un plug-in préféré, le plug-in doit être disponible. Si aucun plug-in préféré n’est trouvé, le plug-in de ligne de base est utilisé. Si aucun plug-in n’est disponible, la transformation signale une erreur.
-   TfmBaseline : seuls les plug-ins de ligne de base peuvent être utilisés dans AddMeasurementStep. Si le ColorContext spécifie un plug-in préféré, le plug-in sera ignoré. Si le plug-in de ligne de base n’est pas disponible, la transformation signale une erreur.

## <a name="transform-execution"></a>Transformation, exécution

La fonction [**TranslateColors**](/windows/win32/api/icm/nf-icm-translatecolors) de l’API ICM 2,0 convertit un tableau de couleurs de l' [espace de couleurs](c.md) source en espace de couleur de destination, comme défini par une transformation de couleur. Cette fonction effectue une vérification interne sur un tableau de couleurs mises en cache pour permettre une correspondance immédiate des couleurs couramment transformées. Cette transformation prend en charge des tableaux d’octets par canal à 8 bits et des tableaux flottants 32 bits par canal. Tous les autres formats seront convertis avant le passage à la nouvelle CTE.

La fonction [**TranslateBitmapBits**](/windows/win32/api/icm/nf-icm-translatebitmapbits) de l’API ICM 2,0 traduit les couleurs d’une image bitmap ayant un format défini pour produire une autre bitmap dans un format demandé. Cette fonction effectue une vérification interne sur un tableau de couleurs mises en cache pour permettre une correspondance immédiate des couleurs couramment transformées. Pour éviter un trop grand nombre de chemins de code, de prise en charge et de test de complexité, seul un nombre limité de formats bitmap est pris en charge dans le moteur de transformation et d’interpolation. Cette fonction doit traduire les formats bitmap entrants et sortants non natifs en formats pris en charge en mode natif pour le traitement. Cette transformation prend en charge uniquement les bitmaps de 8 bits par octet de canal et les bitmaps à virgule flottante 32 bits par canal. Tous les autres formats seront convertis avant le passage à la nouvelle CTE.

 

### <a name="sequential-transform-execution"></a>Exécution de transformation séquentielle

Si le  bit de transformation séquentiel est \_ défini pour le paramètre dwFlags lorsque les fonctions ICM [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransformw) ou **CreateMultiProfileTransform** sont appelées, les étapes de transformation sont exécutées de manière séquentielle. Cela signifie que le code parcourt séparément chaque modèle d’appareil, modèle d’apparence de couleur et modèle de mappage de couleurs, comme spécifié par l’appel de **CreateColorTransform** ou **CreateMultiProfileTransform** . Cela peut être utile pour déboguer des modules de plug-in, mais il est beaucoup plus lent que d’exécuter via une transformation optimisée. L’exécution en mode séquentiel n’est donc pas recommandée pour les logiciels de production. En outre, il peut y avoir de légères différences dans les résultats obtenus en mode séquentiel et en mode optimisé. Cela est dû à des variantes introduites lorsque les fonctions sont concaténées ensemble.

### <a name="creation-of-optimized-transforms"></a>Création de transformations optimisées

Une transformation optimisée est une table de recherche multidimensionnelle. La table peut être traitée par un moteur d’interpolation multidimensionnel, tel que l’interpolation tetrahedral, qui applique les couleurs d’entrée à la transformation. La section suivante décrit comment les tables de recherche optimisées sont créées. La section qui suit décrit comment interpoler dans les tables de recherche optimisées.

## <a name="sparse-lookup-tables"></a>Tables de recherche éparses

Les imprimantes conventionnelles comportent des encres CMJN. Pour étendre la gamme de couleurs, une approche consiste à ajouter de nouvelles encres au système. Les encres ajoutées sont généralement des couleurs que les encres CMJN ont des difficultés à reproduire. Les choix courants sont orange, vert, rouge, bleu, etc. Pour augmenter la résolution apparente, les encres avec des teintes différentes peuvent être utilisées, par exemple, cyan clair, magenta clair, et ainsi de suite. En effet, le périphérique d’impression possède plus de quatre canaux.

Bien que les imprimantes soient des périphériques de sortie, elles effectuent également la conversion des couleurs de l’espace de l’appareil vers un autre espace de couleurs. Dans le cas d’une imprimante CMYK, il s’agit d’une transformation de CMJN à XYZ, ou du « modèle de transfert » de l’imprimante. En associant le modèle de transfert à d’autres transformations, il est possible d’émuler une impression CMJN sur un autre appareil. Par exemple, une imprimante CMJN sur un moniteur RVB permet un mécanisme de vérification qui émule une impression de cette imprimante CMJN sur un moniteur. De même, il s’agit également d’une imprimante Hi-Fi. Une conversion CMYKOG à RGB permet la vérification de l’imprimante CMYKOG sur un moniteur.

L’approche conventionnelle pour implémenter une telle conversion de couleur consiste à utiliser un LUT uniforme. Par exemple, dans un profil ICC pour une imprimante CMYKOG, la spécification ICC impose une balise A2B1 qui stocke un LUT uniforme représentant un échantillonnage uniforme dans l’espace de l’appareil CMYKOG du modèle Forward, qui passe de CMYKOG à l’espace de connexion du profil ICC (CIELAB ou CIEXYZ). Le profil de lien d’appareil ICC permet une transformation directe de l’espace de l’appareil CMYKOG vers n’importe quel espace de couleurs, y compris un espace de l’appareil, également sous la forme d’un exemple de LUT échantillonné uniformément dans l’espace CMYKOG. L’échantillonnage n’est jamais effectué avec des niveaux 256 (profondeur de bit 8) en raison de l’énorme exemple de LUT qui résulte, sauf dans le cas des appareils monochromes (1 canal). Au lieu de cela, l’échantillonnage avec une profondeur de bit inférieure est utilisé ; Parmi les choix typiques, on retrouve 9 (bit Depth 3), 17 (bit profondeur 4), 33 (profondeur de bit 5). Avec le nombre de niveaux inférieurs à 256 dans chaque canal, le LUT est utilisé conjointement avec un algorithme d’interpolation pour produire le résultat si un niveau est compris entre deux niveaux échantillonnés.

Bien qu’un LUT uniforme soit simple à implémenter et l’interpolation sur un LUT uniforme est généralement efficace, la taille de LUT augmente de façon exponentielle avec la dimension d’entrée. En fait, si *d* est le nombre d’étapes utilisées dans le lut uniforme, et que *n* est le nombre de canaux dans l’espace de couleurs source, le nombre de nœuds dans lut ![ indique la variable pour le nombre de nœuds dans un lut. ](images/transformcreation-image002.gif) En clair, le nombre de nœuds exige rapidement autant de stockage en mémoire que même les systèmes informatiques de haut de gamme ont des difficultés à gérer la demande. Pour les appareils avec six ou huit canaux, une implémentation ICC du profil d’appareil requiert l’utilisation de quelques étapes dans LUT, parfois jusqu’à cinq étapes dans la table A2B1 pour conserver le profil en mégaoctets au lieu de gigaoctets. En clair, l’utilisation d’un plus petit nombre d’étapes augmente l’erreur d’interpolation, car il y a maintenant moins d’échantillons. Étant donné que le LUT doit être uniforme, la précision sur l’ensemble de l’espace colorimétrique est détériorée, même dans les régions de l’espace où une différence de couleur significative peut être due à une modification minime de la valeur de l’appareil.

Dans les appareils avec plus de quatre colorants, certains sous-espaces de l’ensemble de l’espace de l’appareil sont plus importants que d’autres. Par exemple, dans l’espace CMYKOG, les encres cyan et vertes sont rarement utilisées ensemble, car leurs teintes se chevauchent en grande partie. De même, les encres jaunes et orange se chevauchent en grande partie. Une réduction uniforme du nombre d’étapes peut être considérée comme une dégradation globale de la qualité sur l’ensemble de l’espace colorimétrique, ce qui est un élément que vous pouvez vous permettre de combiner les encres improbables, mais pas pour les combinaisons probables ou importantes.

Bien qu’une LUT échantillonnée de manière uniforme soit simple et efficace pour l’interpolation, elle impose des besoins de mémoire énormes en cas d’augmentation de la dimension. En réalité, bien qu’un appareil puisse avoir six ou huit canaux, il est rarement utilisé simultanément. Dans la plupart des cas, la couleur d’entrée pour la transformation de couleur n’a que quelques colorants « actifs » et réside donc dans un espace de couleurs de dimension inférieure. Cela signifie également que l’interpolation peut s’effectuer plus efficacement dans cet espace de dimension inférieure, car l’interpolation est plus rapide lorsque la dimension est inférieure.

Par conséquent, l’approche consiste à stratification l’ensemble de l’espace de l’appareil dans des sous-espaces de différentes dimensions. Et étant donné que les dimensions inférieures (qui combinent trois ou quatre colorants) sont plus importantes, en stratifying l’espace, vous pouvez également appliquer des taux d’échantillonnage différents. autrement dit, un nombre d’étapes différent pour les parties ; augmentation des taux d’échantillonnage pour les dimensions inférieures, en les réduisant pour les dimensions supérieures.

Pour corriger les notations, *n* est le nombre de canaux dans l’espace colorimétrique source de la transformation de couleur que vous souhaitez échantillonner. Vous pouvez également faire référence à *n* comme dimension d’entrée et ![ Afficher n supérieur ou égal à 5.](images/transformcreation-image004.gif) , sauf indication contraire.

Les blocs de construction de base sont des LUTs de différentes *dimensions* et tailles d’entrée, au lieu d’un lut uniforme avec la dimension d’entrée *n*. Pour être plus précis, un *lut* est un treillis rectangulaire imposé sur un cube d’unité. autrement dit, toutes les coordonnées de l’appareil sont normalisées à la plage \[ 0, 1 \] ). Si est la dimension d’entrée du lut (Notez qu’il ne doit pas être égal à *n*, bien que ![ affiche V inférieur ou égal à n.](images/transformcreation-image006.gif) est requis), il se compose de grilles d’échantillonnage unidimensionnelles ν :

SAMP *i*: ![ affiche une grille d’échantillonnage unidimensionnelle.](images/transformcreation-image008.gif)

où tous les *x <sub>j</sub>s* doivent se trouver dans la plage \[ 0, 1 \] , ![ affiche un exposant d (i).](images/transformcreation-image010.gif) nombre d’étapes pour l’échantillonnage de canal *i* qui doit être au moins égal à 1, et ![ indique un spuperscript de X (indice) d (i).](images/transformcreation-image012.gif) doit être 1. En revanche, ![ affiche un exposant X (indice 1).](images/transformcreation-image014.gif) ne doit pas être égal à 0.

Seuls les deux cas spéciaux suivants de LUT seront définis.

*Lut fermé*: il s’agit d’un lut avec la spécification supplémentaire que pour chaque SAMP *<sub>i</sub>*, ![ affiche un exposant X (indice 1) égal à 0.](images/transformcreation-image016.gif) , et ![ affiche un exposant d (i) supérieur ou égal à 2.](images/transformcreation-image018.gif) . Un LUT fermé de façon uniforme est un LUT fermé qui a le même ![ afficher un exposant d (i).](images/transformcreation-image010.gif) pour chaque canal, et les nœuds sont espacés uniformément entre 0 et 1.

*Open lut*: il s’agit d’un lut avec la spécification supplémentaire que pour chaque SAMP *i*, ![ affiche un exposant X (indice 1) supérieur à 0.](images/transformcreation-image020.gif) . Il est ![ possible d’afficher un exposant d (i) égal à 1.](images/transformcreation-image022.gif) .

L’objectif est de stratification le cube \[ d’unité 0, 1 \] *n* dans une collection de LUTs fermée et de Luts ouverts, de telle sorte que la collection entière couvre le cube d’unité. Il est conceptuellement plus simple d’organiser ces « strates de LUT » par leurs dimensions, de sorte que le niveau supérieur :

![Affiche le niveau supérieur pour organiser les strates de L U T par leurs dimensions.](images/transformcreation-image024.png)

où ![ représente Sigma indice k.](images/transformcreation-image026.gif) est la « collection de couches *k* ». Notez que la dimension de strates commence par 3 au lieu de 0 ; autrement dit, les points, car l’interpolation de combinaisons de trois couleurs peut être gérée sans nécessiter trop de mémoire.

## <a name="description-of-the-lut-strata"></a>Description des strates LUT

Dans cette implémentation :

1. ![Affiche l’indice Sigma 3.](images/transformcreation-image028.gif) se compose de LUTs fermées avec trois entrées, une de chaque combinaison possible de trois colorants choisis parmi les *n* colorants.

2. ![Affiche l’indice Sigma 4.](images/transformcreation-image030.gif) est constitué d’un LUT fermé pour la combinaison CMJN (ou les quatre premiers colorants), avec ![Affiche (n sur 4) moins 1.](images/transformcreation-image032.png) Ouvrez LUTs pour toutes les autres combinaisons de quatre couleurs. En Bachant la combinaison CMJN, vous reconnaissez qu’il s’agit d’une combinaison importante.

3. Pour ![ affiche k égal à 5,..., n.](images/transformcreation-image034.gif) , ![ Affiche un indice Sigma k.](images/transformcreation-image026.gif) comprend des ![ émissions (n sur k).](images/transformcreation-image037.gif) Ouvrez LUTs, un pour chaque combinaison possible de choix de *k* colorants à partir du total de *n* colorants.

Il reste à spécifier les tailles des LUTs. La principale différence entre les LUTs ouverts et fermés réside dans le fait que les LUTs ouverts ne se chevauchent pas et que les LUTs fermés peuvent se chevaucher aux faces limites. Le fait que l’échantillonnage unidimensionnel dans un LUT ouvert ne contienne pas 0 signifie essentiellement qu’un LUT ouvert ne contient pas la moitié des visages de limites, donc le nom « ouvert ». Si deux LUTs ne se chevauchent pas, vous pouvez utiliser un nombre différent d’étapes ou d’emplacements de nœuds dans chaque canal. Cela n’est pas vrai si deux LUTs se chevauchent. Dans ce cas, si le nombre d’étapes ou les emplacements de nœuds sont différents, un point situé dans l’intersection des deux LUTs recevra une valeur d’interpolation différente en fonction du LUT utilisé dans l’interpolation. Une solution simple à ce problème consiste à utiliser l’échantillonnage uniforme avec le même nombre d’étapes chaque fois que deux LUTs se chevauchent. En d’autres termes :

Toutes les LUTs fermées (toutes les LUTs de trois couleurs et la LUT CMYK dans cette implémentation) doivent être uniformes et comporter le même nombre d’étapes, qui sont indiquées *d*.

Les deux algorithmes suivants peuvent être utilisés pour déterminer le nombre d’étapes *d* pour les Luts fermés et le nombre d’étapes pour Open Luts.

## <a name="algorithm-1"></a>Algorithme \# 1

Cet algorithme ne nécessite pas d’entrée externe.

Toutes les LUTs fermées sont uniformes avec le nombre *d* d’étapes.

Toutes les LUTs ouvertes de la dimension *k* comporteront le même nombre d’étapes que ![ d (k).](images/transformcreation-image039.gif) dans chaque canal d’entrée, et les nœuds sont espacés de façon égale ; autrement dit, pour chaque ![ montre que j’ai égal à 1, 2,..., k.](images/transformcreation-image041.gif) .

SAMP *i*: ![ affiche l’algorithme SAMP i.](images/transformcreation-image043.png)

Enfin, spécifiez *d* et *d* (*k* ) dans le tableau suivant. Les trois modes « preuve », « normal » et « Best » sont les paramètres de qualité ICM 2,0. Dans cette implémentation, le mode de preuve a l’encombrement mémoire le plus faible et le meilleur mode a le plus grand encombrement mémoire.

Pour implémenter cet algorithme, vous devez appeler l’algorithme \# 2 suivant. Les utilisateurs peuvent spécifier leurs propres emplacements d’échantillonnage, en utilisant les tableaux comme guide.

## <a name="algorithm-2"></a>Algorithme \# 2

Cet algorithme nécessite une entrée externe sous la forme d’une liste d’emplacements d’échantillonnage « importants », mais il est plus adaptable et peut économiser de l’espace mémoire.

L’entrée requise est un tableau de valeurs d’appareil fournies par l’utilisateur. Ces valeurs d’appareil indiquent la région de l’espace de couleurs de l’appareil qui est importante. autrement dit, quelle région doit être échantillonnée en plus.

Toutes les LUTs fermées sont uniformes avec *d* nombre d’étapes, comme décrit dans algorithme \# 1. Les valeurs de *d* sont fournies dans le tableau 1.

*(a) LUT fermé de façon uniforme*



|         | Mode de vérification | Mode Normal | Meilleur mode |
|---------|------------|-------------|-----------|
| ***d*** | 9          | 17          | 33        |



 

*(b) ouvrir LUT*



| Dimension d’entrée | Mode de vérification | Mode Normal | Meilleur mode |
|-----------------|------------|-------------|-----------|
| 4               | 5          | 7           | 9         |
| 5               | 2          | 3           | 3         |
| 6               | 2          | 3           | 3         |
| 7               | 2          | 2           | 2         |
| au moins 8       | 2          | 2           | 2         |



 

**Tableau 1 :** Tailles de LUT utilisées dans l’algorithme

Chaque LUT ouvert peut avoir un nombre d’étapes différent dans chaque canal d’entrée, et les emplacements d’échantillonnage n’ont pas besoin d’être espacés de façon égale. Pour une strate LUT ouverte donnée, il y a une combinaison de couleurs associée, par exemple, ![ affiche l’indice c 1,..., c indice k.](images/transformcreation-image045.gif) , où le ![ affiche C indice i.](images/transformcreation-image047.gif) les s sont des entiers distincts compris entre 1 et *n*. Il s’agit des indices de canal correspondant aux colorants « actifs » dans cette strate.

ÉTAPE 1 : exclure le tableau entré des valeurs d’appareil qui ne sont pas contenues dans cette strate. Une valeur d’appareil ![ affiche x indice 1, x indice 2,..., x indice n.](images/transformcreation-image049.gif) est contenu dans les strates, si et seulement si ![ affiche un ensemble de valeurs pour un canal.](images/transformcreation-image051.gif) et tous les autres canaux sont 0. Si le jeu filtré comporte *N* entrées, laissez

![Affiche une équation à utiliser si l’ensemble filtré comporte N entrées.](images/transformcreation-image053.png)

Pour chaque ![Indique i égal à 1, 2,..., k.](images/transformcreation-image041.gif) , effectuez les étapes suivantes 2-5 :

ÉTAPE 2 : si ![ affiche l’indice d de tentative (k) égal à 1.](images/transformcreation-image055.gif) , SAMP *i* a uniquement 1 point, qui doit être 1,0. Passer à *l’étape suivante*. Sinon, passez à l’étape 3.

ÉTAPE 3 : trier les échantillons filtrés dans l’ordre croissant dans la ![Affiche l’indice C i.](images/transformcreation-image047.gif) canal.

ÉTAPE 4 : définir la grille d’échantillonnage « provisoire » à l’aide des nœuds

![Affiche les nœuds utilisés pour définir la grille d’échantillonnage « provisoire ».](images/transformcreation-image057.png)

where ![Affiche j égal à 1, 2,..., d indice provisoire (k).](images/transformcreation-image059.gif) .

ÉTAPE 5 : régulariser la grille provisoire pour s’assurer qu’elle est conforme à la monotonique stricte et qu’elle se termine par 1,0. Étant donné que le tableau est déjà trié, les nœuds de la grille provisoire sont déjà monotones nondecreasing. Toutefois, les nœuds adjacents peuvent être identiques. Vous pouvez résoudre ce problème en supprimant des nœuds identiques, si nécessaire. Enfin, après cette procédure, si le point de terminaison est inférieur à 1,0, remplacez-le par 1,0.

Notez que l’étape 5 est la raison pour laquelle les strates LUT peuvent avoir un nombre d’étapes différent dans chaque canal. Après le régularisation, le nombre d’étapes dans un canal peut être inférieur à ![Affiche la tentative d’indice d (k).](images/transformcreation-image061.gif) .

## <a name="interpolation"></a>Interpolation

Vous pouvez construire la stratification du cube d’unités en ouvrant des strates LUT et des strates de LUT fermées. Pour effectuer une interpolation à l’aide de cette « structure LUT éparse », procédez comme suit. Prendre une valeur donnée pour l’appareil d’entrée ![Affiche (X indice 1, X indice 2,..., X Indice n).](images/transformcreation-image049.gif) .

ÉTAPE 1 : déterminer le nombre de canaux « actifs ». Il s’agit du nombre de canaux non nuls. Cela détermine la dimension de strat *k* pour rechercher le stratum contenant. Plus précisément, la dimension de strate est 3 Si le nombre de canaux actifs est ![ inférieur ou égal à 3.](images/transformcreation-image063.gif) dans le cas contraire, la dimension de strates est la même que le nombre de canaux actifs.

ÉTAPE 2 : dans ![Affiche l’indice Sigma Sigma.](images/transformcreation-image026.gif) , recherchez le stratum contenant. Une valeur d’appareil est contenue dans une couche ouverte si tous les canaux correspondant à la couche ont une valeur différente de zéro et que tous les autres canaux sont nuls. Une valeur d’appareil est contenue dans une couche fermée si chaque canal non représenté par la couche est égal à zéro. Si aucun Stratum contenant n’est trouvé, il y a une condition d’erreur. Annuler et signaler une défaillance. Si un Stratum contenant est trouvé, passez à l’étape suivante.

ÉTAPE 3 : si le stratum contenant est fermé, l’interpolation au sein de la couche peut être effectuée à l’aide d’un algorithme d’interpolation connu. Dans cette implémentation, le choix de l’algorithme est l’interpolation tetrahedral. Si le stratum conteneur est ouvert et que la valeur de l’appareil se trouve strictement au sein de la couche, autrement dit,

![Affiche l’indice X i supérieur ou égal à... ](images/transformcreation-image065.gif) premier *nœud de la* chaîne

où *je suis* un index de canal pour la couche, l’algorithme d’interpolation standard, tel que l’interpolation tetrahedral, fonctionne.

Si ![ affiche l’indice X i inférieur à... ](images/transformcreation-image067.gif) premier nœud dans *ma* chaîne pour certains *i*, la valeur de l’appareil se trouve dans l’intervalle entre la couche et les sous-espaces à la dimension inférieure. Ce MOI n’est pas concerné par un algorithme d’interpolation par se, donc tout algorithme d’interpolation peut être utilisé pour interpoler dans ce « Gap », bien que l’algorithme préféré soit l’interpolation transfinie suivante.

L’architecture du module d’interpolation est illustrée dans les deux parties de la figure 1.

![Diagramme qui illustre la première partie de l’architecture du module d’interpolation.](images/transformcreation-image068.png)

![Diagramme qui affiche la partie deux de l’architecture du module d’interpolation.](images/transformcreation-image070.png)

**Figure 1 :** Architecture du module intepolation

Comme expliqué précédemment, cet algorithme est en mesure d’obtenir un échantillonnage très dense dans les régions de l’espace de l’appareil qui contiennent une combinaison importante de colorants, tout en minimisant la taille totale des LUTs nécessaires. Le tableau suivant présente une comparaison du nombre de nœuds nécessaires pour l’implémentation de LUT. épars (à l’aide de l’algorithme \# 1 et du mode normal) et de l’implémentation de lut uniforme correspondante.



| **Nombre de canaux d’entrée** | **LUT épars** | **LUT uniforme** |
|------------------------------|----------------|-----------------|
| 5                            | 142498         | 1419857         |
| 6                            | 217582         | 24137567        |
| 7                            | 347444         | 410338673       |
| 8                            | 559618         | 6975757441      |



 

## <a name="interpolation-within-a-unit-cube"></a>Interpolation au sein d’un cube d’unité

Une étape de base dans le cas d’une grille rectangulaire est l’interpolation dans une cellule englobante. Pour un point d’entrée, vous pouvez facilement déterminer la cellule englobante. Dans une grille rectangulaire, la valeur de sortie à chacun des sommets (points d’angle) de la cellule englobante est spécifiée. Il s’agit également des seules conditions limites (BCs) qu’un interpolateur doit respecter : l’interpolation doit traverser tous ces points. Notez que ces conditions limites se trouvent sur des points discrets, dans ce cas les deux points d’angle de la cellule, où n est la dimension de l’espace colorimétrique.

Il est utile de formaliser le concept des conditions limites avant de passer à. Pour tout sous-ensemble de la limite de la cellule englobante (le cube d’unité dans n dimensions), une condition de limite sur S est une spécification d’une fonction BC : S → RM, où m est la dimension de sortie. En d’autres termes, une interpolation, qui peut être dénotée interp : \[ 0, 1 \] n → RM, est requise pour satisfaire : interp (x) = BC (x) pour tous les x dans S.

Dans le scénario standard d’interpolation sur le cube d’unité, S est l’ensemble de points discrets qui représentent les 2n sommets du cube.

Vous pouvez désormais généraliser les conditions limites pour résoudre les problèmes décrits précédemment et fournir un nouvel algorithme d’interpolation au sein du cube d’unité. Au lieu d’autoriser uniquement des points de limite discrets, des conditions limites peuvent être imposées sur l’intégralité d’une face limite du cube. Les hypothèses précises sont les suivantes :

(a) le point VN = (1, 1,..., 1) est spécial et seule une condition de limite discrète est autorisée. En d’autres termes, aucune condition de limite continue ne peut être imposée sur les visages de limites n XI = 1 (i = 1,..., n).

(b) pour chacun des n points de limite restants XI = 0 (i = 1,..., n), la condition limite peut être imposée sur l’ensemble du visage, avec la condition de compatibilité qui, si deux visages se croisent, les conditions limites sur les faces doivent s’entendre sur l’intersection.

(c) tous les vertex qui ne sont pas contenus dans les faces avec la condition limite auront une condition de limite individuelle (discrète).

Vous pouvez faire référence à une condition de limite discrète comme données finies et une condition de limite continue en tant que données transfinies dans la discussion sur l’interpolation sur des données finies et transfinies.

Tout d’abord, passez en revue l’interpolation tetrahedral standard (telle que celle utilisée dans le brevet de Sakamoto) qui permet de définir les notations pour cette formulation particulière du problème. On sait que le cube d’unité \[ 0,1 \] n peut être subdivisé en n ! tetrahedra, paramétrable par le jeu de permutations sur n symboles. Plus spécifiquement, chacun de ces tétraèdres est défini par des inégalions

![Affiche la formule pour le inequalites des tétraèdres.](images/transformcreation-image073.gif)

où σ : {1, 2,.., n} → {1, 2,..., n} est une permutation de "Symbols" 1,2,..., n, autrement dit, il s’agit d’un mappage biject du jeu de n symboles. Par exemple, si n = 3 et σ = (3, 2, 1), ce qui signifie que σ (1) = 3, σ (2) = 2, σ (3) = 1, alors les tétraèdres correspondants sont définis par z ≥ y ≥ x, où la notation commune x, y, z est utilisée pour x1, x2, x3. Notez que ces tétraèdres ne sont pas dissociés les uns des autres. Dans le cadre de l’interpolation, les points situés sur une face commune de deux tétraèdres distincts auront la même valeur d’interpolation, quels que soient les tétraèdres utilisés dans l’interpolation. Toujours, dans le scénario standard de l’interpolation sur les points finis, pour un point d’entrée donné (x1,..., xn), déterminez d’abord les tétraèdres qu’il contient ou, de manière équivalente, la permutation σ correspondante, puis l’interpolation tetrahedral est définie comme

![Affiche l’équation qui définit l’interpolation tetrahedral.](images/transformcreation-image075.png)

where ![Affiche l’équation pour les vecteurs de base standard.](images/transformcreation-image077.png) pour i = 1,..., n et E1,..., en sont les vecteurs de base standard. Avant de passer à la généralisation, Notez que v0, v1,..., VN sont les vertex du tétraèdres, et ![Affiche les coordonnées Barycentric.](images/transformcreation-image079.png) sont les « coordonnées Barycentric ».

Pour le cas général de BCs sur les faces de frontière, vous pouvez utiliser le concept de projection Barycentric. Comme précédemment, pour un point d’entrée donné (x1,..., xn), déterminez d’abord dans quels tétraèdres il se trouve ou équivalent à la permutation σ correspondante. Effectuez ensuite une série de projections Barycentric, comme suit. La première projection ![Affiche l’indice BProj 1 (x).](images/transformcreation-image081.gif) envoie le point au plan ![Affiche le delta d’indice X (1) égal à 0.](images/transformcreation-image083.gif) s' ![Affiche X égal à V indice n.](images/transformcreation-image085.gif) dans ce cas, il n’est pas modifié. La définition précise du mappage BProj est définie comme suit :

![Affiche l’équation pour la définition précise du mappage BProj.](images/transformcreation-image087.png)

par ![Affiche l’équation pour P indice k.](images/transformcreation-image089.png) et k = 1, 2,..., n.

Dans le cas présent ![Affiche X est égal à V indice n.](images/transformcreation-image085.gif) , vous pouvez arrêter, car BC est défini à VN en supposant (a). Dans le cas présent ![Affiche X n’est pas égal à V indice n.](images/transformcreation-image091.gif) , il est clair que ![Affiche l’indice BProj 1 (X).](images/transformcreation-image081.gif) a le composant σ (1) th Annihilated. En d’autres termes, il se trouve sur l’un des visages de limites. Soit il se trouve sur un visage sur lequel BC est défini, auquel cas vous pouvez arrêter, ou effectuer une autre projection Barycentric ![Affiche l’indice BProj 2 (X').](images/transformcreation-image093.gif) where ![Affiche X’égal à BProj indice 1 (X).](images/transformcreation-image095.gif) . Et si ![Affiche X' ' = Bproj indice 1 (X').](images/transformcreation-image097.gif) est sur un visage sur lequel BC est défini, vous pouvez l’arrêter ; Sinon, effectuer une autre projection ![Affiche l’indice BProj 3 (X «»).](images/transformcreation-image099.gif) . Étant donné que chaque projection Annihilates un composant, la dimension effective diminue, de sorte que vous savez que le processus doit finalement être arrêté. Dans le pire des cas, vous effectuez n projections vers la dimension 0, c’est-à-dire, les sommets sur le cube, qui, selon l’hypothèse (c), vous savez que BC sera défini sur.

En supposant que K projections ont été effectuées, avec

![Affiche une équation à utiliser en supposant que la projection K a été effectuée.](images/transformcreation-image101.png)

x (0) = x, le point d’entrée et BC est défini sur x (k). Dérouler ensuite les projections en définissant une série de vecteurs de sortie :

![Affiche des équations pour une série de vecteurs de sortie.](images/transformcreation-image103.png)

where ![Affiche l’équation pour l’exposant Y (K).](images/transformcreation-image105.gif) et vous obtenez enfin la réponse

![Affiche interp (x) égal à l’exposant y (0).](images/transformcreation-image107.gif)

## <a name="worked-example"></a>Exemple pratique

![Diagramme qui montre un exemple travaillé d’interpolation avec un cube d’unité.](images/transformcreation-image108.png)

**Figure 2 :** Exemple de travail

Considérez la situation illustrée dans la figure 2, où n = 3, m = 1, et que vous disposez des BCs suivants :

(a) quatre BCs discrets sur les vertex

(0, 0, 1) : β001

(0, 1, 1) : β011

(1, 0, 1) : β 101

(1, 1, 1) : β 111

(b) un BC continu sur le visage x3 = 0 : F (x1, x2)

Calcul \# 1 : point d’entrée x = (0,8, 0,5, 0,2). Le tétraèdres englobant est associé à la permutation &lt; 1, 2, 3 &gt; .

1ère projection : ![Affiche l’équation de la première projection.](images/transformcreation-image110.png)

Il est déjà sur la face x3 = 0, ce qui vous permet de l’arrêter. La substitution vers l’arrière donne alors

![Affiche la réponse de la première projection.](images/transformcreation-image112.png) C’est la réponse.

Calcul \# 2 : point d’entrée x = (0,2, 0,5, 0,8). Le tétraèdres englobant est associé à la permutation &lt; 3, 2, 1 &gt; .

1ère projection : ![Affiche l’équation de la première projection du calcul 2.](images/transformcreation-image113.png)

2e projection : ![Affiche l’équation pour la deuxième projection du calcul 2.](images/transformcreation-image115.png)

3e projection : ![Affiche l’équation pour la troisième projection du calcul 2.](images/transformcreation-image117.png) , qui se trouve sur le visage x3 = 0. La substitution vers l’arrière donne alors

![Affiche les deux premières équations pour la substitution vers l’arrière.](images/transformcreation-image119.png)

![Affiche la troisième équation pour la substitution vers l’arrière.](images/transformcreation-image123.png), qui est la dernière réponse.

## <a name="applications"></a>Applications

*(a) interpolation tetrahedral séquentielle*

![Diagramme qui montre l’interpolation tetrahedral séquentielle.](images/transformcreation-image124.png)

**Figure 3 :** Interpolation tetrahedral séquentielle

Reportez-vous à la figure 3. Pour interpoler entre deux plans sur lesquels des grilles non compatibles ont été imposées, envisagez une cellule encadrant un point donné P illustrée dans la figure. Les sommets « supérieurs » de la cellule proviennent directement de la grille dans le plan supérieur. Les vertex de la face inférieure ne sont pas compatibles avec la grille dans le plan inférieur. la face entière est donc traitée comme ayant un BC avec des valeurs obtenues par interpolation sur la grille dans le plan inférieur. Il est alors évident que cette configuration satisfait les hypothèses (a), (b) et (c) ci-dessus, et vous pouvez appliquer l’algorithme d’interpolation.

Il est également clair que l’algorithme a réduit la dimension du problème d’interpolation de 1, car il en résulte une combinaison linéaire de valeurs aux sommets de la grille supérieure, et une interpolation dans le plan inférieur, qui a une dimension moins 1. Si une configuration de plan sandwich similaire existe dans le plan inférieur, vous pouvez appliquer la procédure dans ce plan, ce qui réduit davantage la dimension de 1. Cette procédure peut se poursuivre jusqu’à ce que vous atteigniez la dimension 0. Cette cascade de projections et d’interpolations peut être appelée « interpolation tetrahedral séquentielle ».

*(b) interpolation de l’intervalle*

![Diagramme qui montre l’interpolation de l’intervalle.](images/transformcreation-image126.jpg)

**Figure 4 :** Interpolation de l’intervalle

Il s’agit d’une grille imposée sur un cube se trouvant strictement à l’intérieur du quadrant positif. Le cube lui-même a une grille, et chaque plan de coordonnées a des grilles qui ne sont pas nécessairement compatibles. Le « GAP » entre le cube et les plans de coordonnées a une section transversale « L-Model » et n’est pas prise en compte pour les techniques standard. Toutefois, avec la technique introduite ici, vous pouvez facilement introduire des cellules qui couvrent ce fossé. La figure 4 illustre l’une d’entre elles. Les grilles sur les plans de coordonnées prennent en charge l’interpolation qui fournit le BCs nécessaire pour toutes les faces inférieures de la cellule, avec un vertex restant dont BC est fourni par l’angle inférieur du cube.

## <a name="final-note-on-implementation"></a>Dernière note sur l’implémentation

Dans l’application réelle, le « cube d’unité » qui est le paramètre de base de l’algorithme est extrait des plus grands treillis, et les valeurs des vertex peuvent nécessiter un calcul coûteux. D’un autre côté, il est également clair que l’interpolation tetrahedral nécessite uniquement les valeurs des sommets des tétraèdres, qui est un sous-ensemble de tous les vertex du cube d’unité. Par conséquent, il est plus efficace d’implémenter ce qui peut être appelé « évaluation différée ». Dans une implémentation logicielle de l’algorithme précédent, il est courant d’avoir une sous-routine qui prend le cube d’unité et les valeurs de ses vertex comme entrée. L’évaluation différée signifie qu’au lieu de passer les valeurs aux sommets, les informations nécessaires pour évaluer les valeurs des vertex sont passées, sans réellement effectuer l’évaluation. À l’intérieur de la sous-routine, l’évaluation réelle de ces valeurs est effectuée uniquement pour les vertex qui appartiennent au tétraèdres englobant, une fois le tétraèdres englobant déterminé.

## <a name="lookup-table-for-use-with-high-dynamic-range-virtual-rgb-source-devices"></a>Table de recherche à utiliser avec des appareils sources RGB virtuels à plage dynamique élevée

Dans le cas où une transformation est construite avec un appareil source modélisé comme appareil RVB virtuel, il est possible que les valeurs de couleur source soient négatives ou supérieures à Unity (1,0). Dans ce cas, l’appareil source est désigné comme ayant une plage dynamique élevée (HDR). Une attention particulière est apportée à ce cas.

Dans le cas des transformations HDR, les valeurs minimales et maximales de chaque canal colorant peuvent être déterminées à partir de la limite de la gamme de l’appareil. À l’aide de ces valeurs, une mise à l’échelle simple pour chaque canal en couleur est appliquée afin que les valeurs colorantes égales à la couleur minimale soient converties en 0,0 et que les valeurs de couleur égales à la couleur maximale soient converties en 1,0, avec une mise à l’échelle linéaire des valeurs entre pour correspondre de façon linéaire entre 0,0 et 1,0.

### <a name="iccprofilefromwcsprofile"></a>ICCProfileFromWCSProfile

Étant donné que l’objectif principal de cette fonctionnalité est de prendre en charge les versions antérieures à Vista de Windows, vous devez générer les profils ICC de la version 2,2 tels que définis dans la spécification ICC ICC. 1:1998-09. Dans certains cas (reportez-vous au tableau suivant « mappage de la classe de profil ICC »), vous pouvez créer un profil ICC basé sur une matrice ou un TRC à partir d’un profil WCS. Dans d’autres cas, le profil ICC est constitué de LUTs. Le processus suivant décrit comment créer les LUTs AToB et BToA. Bien entendu, les profils ICC comportent également d’autres champs. Certaines données peuvent être dérivées du profil WCS. Pour les autres données, vous devez développer des valeurs par défaut intelligentes. Les droits d’auteur seront attribués à Microsoft ; étant donné qu’il s’agit de la technologie Microsoft utilisée pour créer le LUTs.

Cette conception doit fonctionner pour tous les types de modèles d’appareil, y compris les plug-ins. Tant que le plug-in est associé à un modèle d’appareil de base, le type d’appareil sous-jacent peut être déterminé.

La partie difficile de la création d’un profil ICC consiste à créer les tables de recherche AToB et BToA. Ces tables sont mappées entre l’espace de l’appareil, par exemple, RVB ou CMJN, et l’espace de connexion du profil (PCS), qui est une variante de CIELAB. Cela est fondamentalement le même que le processus de gestion des couleurs utilisé dans la transformation CITE pour mapper l’espace de l’appareil à l’espace de l’appareil. Toutefois, vous devez disposer des informations suivantes pour effectuer la transformation.

1) Référencez les conditions d’affichage pour les PC.

2) Gamme de PC de référence.

3) Modèle d’appareil qui effectue une conversion entre les valeurs de PC et la colorimétrie.

Le profil WCS et le CAM qui lui est associé sont fournis en tant que paramètres. Il existe deux modèles d’appareil de base qui effectuent la conversion entre colorimétrie et l’encodage des PC. La raison pour laquelle vous avez besoin de deux est expliquée ci-dessous.

1) Vous pouvez obtenir les conditions d’affichage des références pour les PC à partir de la spécification de format de profil ICC. Les informations fournies dans la spécification de format de profil ICC sont suffisantes pour calculer toutes les données requises pour initialiser le CAM utilisé par le MCG. Pour des fins de cohérence et de flexibilité, ces informations sont stockées dans un profil de couleurs WCS.

2) Vous pouvez également utiliser un profil WCS pour stocker des exemples qui définissent la gamme de référence des PC. Le système de gestion des couleurs CITE (CMS) offre deux façons de créer des limites de gamme. L’une d’elles consiste à échantillonner la totalité de l’espace de l’appareil et à utiliser le modèle d’appareil pour créer des valeurs de mesure. La deuxième méthode consiste à utiliser des échantillons mesurés à partir du profil pour créer une limite de gammes de référence. Étant donné que la gamme de PC ICC est trop grande pour créer une gamme de référence utile, la première méthode n’est pas appropriée. Mais la deuxième méthode est une approche flexible basée sur les profils. Pour redéfinir la gamme de PC de référence, vous pouvez modifier les données de mesure dans le profil de périphérique PC.

3) Les PC ICC sont une modélisation d’un appareil idéal. En créant un modèle de PC en tant qu’appareil réel, vous pouvez tirer parti du processus de gestion des couleurs utilisé dans le Smart CMM. La création d’un modèle d’appareil à partir de colorimétrie sur l’encodage de PC est simple. Il vous suffit de mapper les valeurs colorimétriques vraies et les valeurs de PC encodées. Étant donné que l’interface CMS pour les modèles de périphérique prend en charge uniquement les valeurs XYZ, vous devrez peut-être également effectuer un mappage entre XYZ et LAB. Il s’agit d’une transformation bien connue. Ce modèle est décrit dans le document 2.2.02 « modèles d’appareil de base » dans les sections 7,9 et 7,10.

Vous devrez peut-être effectuer un mappage de gamme, si la gamme de l’appareil est plus grande que la gamme de PC. Les MGM de base peuvent être utilisés à cette fin. Notez qu’un profil ICC correctement créé possède des tables de recherche pour les intentions de colorimétrie, de perception et de saturation relatives, même si celles-ci peuvent tous pointer vers le même LUT en interne.

![Diagramme qui montre la création d’un T o B L U T.](images/transformcreation-image128.png)

**Figure 5 :** Création d’un LUT AToB

Ce processus est illustré à la figure 5. Tout d’abord, le modèle d’appareil est initialisé à partir des données du profil DM. Ensuite, construisez une limite de gamme d’appareils comme suit. Un échantillonnage des données à partir du modèle d’appareil est exécuté via le modèle d’appareil pour obtenir des données colorimétriques. Les données colorimétriques sont exécutées via le CAM pour créer des données d’apparence. Les données d’apparence sont utilisées pour créer la limite de la gamme d’appareils.

Ensuite, utilisez les données du profil de mesure PC de référence pour créer une limite de gamme pour les PC.

Utilisez les deux limites de gamme que vous venez de créer pour initialiser un MGM. Utilisez ensuite le modèle d’appareil, le MGM et le modèle d’appareil PCS pour créer une transformation. Exécutez un échantillonnage de l’espace de l’appareil via la transformation pour créer un LUT AToB.

![Diagramme illustrant la création d’un T o B L U T à l’aide d’un échantillonnage de l’espace P C S.](images/transformcreation-image130.png)

**Figure 6 :** Création d’un LUT BToA

La figure 6 illustre la création du LUT BToA. Cela est presque identique à la création d’un LUT AToB, avec les rôles de source et de destination échangés. En outre, vous devez échantillonner la gamme complète de PC pour créer le LUT.

Notez que, étant donné que la came (CIECAM02 dans le WCS) est impliquée dans le processus, une adaptation chromatique entre le point blanc du média et le point blanc du PC (exigé par ICC pour être celle de D50) est appliquée de manière transparente par le CAM.

## <a name="hdr-virtual-rgb-devices"></a>Périphériques HDR virtuels HDR

Une attention particulière doit être fournie lors de la génération de profils pour les périphériques RGB virtuels HDR ; autrement dit, les appareils pour lesquels les valeurs de couleur peuvent être inférieures à 0,0 ou supérieures à 1,0. Dans la génération de la ATOB LUT, un plus grand ensemble de LUTs d’entrée 1D est généré. Les valeurs de couleur sont mises à l’échelle et décalées vers la plage 0. 1 à l’aide des valeurs de couleur minimale et maximale dans le profil WCS.

Étant donné que l’espace colorimétrique pour les appareils HDR n’est pas susceptible d’être complètement rempli, une prise en charge spéciale est fournie dans le LUT 3D pour la balise également. Pour gérer les couleurs dans la région peu peuplée, les colorants sont recodés afin que l’extrapolation au-delà de 0,0 et 1,0 puisse être obtenue. La plage utilisée est-1.. + 4.

En raison de la remise à l’échelle appliquée pour le LUT 3D, un ensemble de LUTs de sortie 1D est créé pour mapper le résultat à la plage 0. 1.

## <a name="more-than-one-pcs"></a>Plusieurs PC

La ICC a découvert qu’un ordinateur n’était pas suffisamment flexible pour répondre à toutes les utilisations prévues d’un MCG. Dans la version 4 de la spécification de profil, la ICC a clarifié qu’il y a en fait deux encodages de PC. L’un est utilisé pour les intentions de colorimétrie ; un autre est utilisé pour l’intention de perception. (Aucun PC n’est spécifié pour l’objectif de saturation. La CCI a laissé cette partie ambiguë.) Les PC colorimétriques ont une luminosité minimale et maximale spécifiée, mais les valeurs de chrominance et de teinte sont comprises entre + 127 environ. Ce PC ressemble à un prisme rectangulaire. Comme mentionné précédemment, le volume des PC de perception ressemble à la gamme d’une imprimante à jet d’encre.

Les deux PCSs ICC ont également deux encodages numériques différents. Dans les PC percepteurs, la valeur zéro représente une luminosité de zéro. Dans les PC colorimétriques, la valeur zéro représente la luminosité minimale des PC, qui est supérieure à zéro. Vous pouvez résoudre ce problème en utilisant un modèle d’appareil différent pour chacun des encodages de PC.

## <a name="gamut-mapping"></a>Mappage de la gamme

Pour créer le LUTs AToB dans un profil ICC, vous mappez de la gamme d’appareils à l’espace de PC approprié. Pour créer le LUTs BToA, vous mappez de l’espace PC à la gamme de périphériques. Le mappage du LUTs AToB est assez similaire à celui utilisé dans un CMS basé sur des mesures. Pour les PC percepteurs, mappez la gamme de l’appareil plausible à la limite de la gamme des PC perception, en utilisant le découpage ou la compression pour toutes les couleurs hors de la gamme. Pour les intentions de colorimétrie, vous devrez peut-être détourer la lumière, mais les valeurs de chrominance et de teinte sont toutes adaptées à la gamme de PC colorimétriques.

Le mappage du LUTs BToA est un peu différent. Les intentions de colorimétrie sont toujours faciles ; il vous suffit de découper les valeurs des PC pour la gamme des appareils. Toutefois, la ICC exige que toutes les valeurs de PC possibles correspondent à une valeur de périphérique, et pas simplement à celles de la gamme de référence des PC percepteurs. Vous devez donc vous assurer que les MGM peuvent gérer les couleurs sources qui se trouvent en dehors de la gamme de référence. Cela peut être géré en découpant ces couleurs vers la limite de gamme d’appareils.

## <a name="baseline-device-to-icc-profile-class-mapping"></a>Mappage de la classe de profil d’appareil à ICC



| Type de périphérique de base              | Classe de profil ICC       | Remarque                                                                      |
|-----------------------------------|-------------------------|-----------------------------------------------------------------------------|
| Appareil de capture RVB                | Périphérique d’entrée (« SCNR »)   | PC est CIELAB. AToB0Tag est un appareil à PC avec une intention de Colorimétrie relative. |
| CRT, moniteur LCD                  | Périphérique d’affichage (« MNTR ») | PC est CIEXYZ. Consultez les éléments suivants pour la conversion de modèle.                      |
| Projecteur RGB                     | Espace colorimétrique (« SPAC »)    | PC est CIELAB.                                                              |
| Imprimante RVB et CMJN              | Périphérique de sortie (« PRTR »)  | PC est CIELAB.                                                              |
| Appareil virtuel RVB (cas non HDR) | Périphérique d’affichage (« MNTR ») | PC est CIEXYZ.                                                              |
| Appareil virtuel RVB (cas HDR)     | Espace colorimétrique (« SPAC »)    | PC est CIELAB.                                                              |



 

La conversion des profils Monitor n’implique pas la création de LUTs, mais consiste plutôt en la création d’un modèle Matrix ou TRC. Le modèle utilisé dans ICC est légèrement différent de celui utilisé dans le CRT WCS ou la modélisation LCD en ce que le terme « correction noire » est manquant. Plus précisément :

Modèle WCS : ![Affiche un modèle W C S.](images/transformcreation-image132.png)

Modèle ICC : ![Montre un modèle I c c.](images/transformcreation-image134.png)

La conversion du modèle WCS au modèle ICC s’effectue comme suit.

Définir de nouvelles courbes :

![Affiche une matrice pour définir de nouvelles courbes.](images/transformcreation-image136.png)

Ce ne sont pas des courbes de reproduction de ton car elles ne correspondent pas à 1 à 1. Une normalisation permet d’y parvenir. Les définitions finales du modèle ICC sont les suivantes :

![Affiche les définitions finales du modèle C c.](images/transformcreation-image138.png)

![Affiche la matrice finale pour le modèle C I c.](images/transformcreation-image140.png)

Pour les appareils virtuels RVB non HDR, vous générez également un profil d’affichage ICC pour l’efficacité de l’espace. Dans ce cas, la matrice tristimulus *M ICC* peut être obtenue directement à partir des primaires du profil WCS sans la conversion du modèle ci-dessus. L’une des dernières, mais importantes, est que cette matrice tristimulus doit être adaptée de façon chromatique à D50 pour se conformer à la spécification ICC des PC. En d’autres termes, les entrées de chaque ligne de la matrice à encoder dans le profil ICC doivent être additionnées respectivement à 96,42, 100 et 82,49. Dans l’implémentation actuelle, l’adaptation chromatique est effectuée par CAT02, qui est également la transformation d’adaptation chromatique utilisée dans CAM02.

## <a name="black-preservation-and-black-generation"></a>Préservation du noir et génération de noir

L’implémentation de la préservation du noir est liée à la génération du canal noir dans les appareils qui prennent en charge un canal noir. Pour ce faire, des informations sur chaque couleur source sont collectées pour permettre aux modèles d’appareil qui prennent en charge un canal noir de déterminer la meilleure façon de définir le canal noir sur la sortie. Bien que la préservation du noir soit pertinente pour les transformations de couleur qui effectuent une conversion entre un périphérique de canal noir et un autre, la génération noire est implémentée pour toutes les transformations impliquant un appareil de destination de canal noir.

Les informations de canal noir sont enregistrées dans une structure de données appelée [**BlackInformation**](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_blackinformation). La structure **BlackInformation** contient une valeur booléenne indiquant si la couleur contient uniquement un colorant noir et une valeur numérique indiquant le degré de « noir » appelé poids noir. Pour les appareils source qui prennent en charge un canal noir, la pondération noire est le pourcentage de couleur noire dans la couleur source. Pour les appareils source qui ne contiennent pas de canal noir, le poids noir est calculé à l’aide des autres colorants et de la valeur d’apparence. Une valeur appelée « pureté de la couleur » est calculée en tenant la différence entre la valeur de couleur maximale et la valeur de couleur minimale divisée par la valeur de couleur maximale. Une valeur appelée « Lighting relative » est calculée en tenant compte de la différence entre la luminosité de la couleur et la luminosité minimale du périphérique de destination, divisée par la différence entre la luminosité minimale et la luminosité maximale du périphérique de destination. Si l’appareil source est un appareil additif (moniteur ou projecteur), le poids noir est déterminé comme étant le 1,0 moins la pureté de couleur multiplié par la clarté relative. Par exemple, si l’appareil source est une analyse RVB, la valeur maximale et la valeur minimale de R, G et B pour chaque couleur sont calculées et le poids noir est déterminé par la formule :

BW = (1,0 – (Max (R, G, B) – min (R, G, B))/max (R, G, B)) \* luminosité relative

Si l’appareil source prend en charge la coloration contre la soustraction, par exemple, une imprimante CMJ, les colorants individuels doivent être « ceux qui sont complétés » (soustrait de 1,0) avant d’être utilisés dans la formule précédente. Par conséquent, pour une imprimante CMJ, R = 1,0 – C, G = 1,0 – M et B = 1,0 – Y.

Les informations noires de chaque couleur traitée par la transformation de couleur sont déterminées au cours du processus de traduction des couleurs. Les informations en noir uniquement sont déterminées uniquement si la préservation du noir est spécifiée. Le poids noir est toujours déterminé si le modèle d’appareil de destination prend en charge une couleur noire. Les informations noires sont transmises au modèle d’appareil de destination via la méthode [**ColorimetricToDeviceColorsWithBlack**](/previous-versions/windows/desktop/api/WcsPlugIn/nf-wcsplugin-idevicemodelplugin-colorimetrictodevicecolorswithblack) , qui utilise le lut résultant.

Notez que, en raison de l’optimisation de la transformation des couleurs, le processus ci-dessus se produit uniquement lors de la création du LUT de transformation optimisé, et non lors de l’exécution de la méthode TranslateColors.

## <a name="optimization-for-transforms-with-more-than-three-source-channels"></a>Optimisation des transformations avec plus de trois canaux sources

La taille de la transformation optimisée est déterminée par plusieurs facteurs : le nombre de canaux de couleur dans l’appareil source, le nombre d’étapes dans le tableau pour chaque canal de couleur source et le nombre de canaux de couleur dans le périphérique de sortie. La formule permettant de déterminer la taille de la table de transformation est la suivante :

Size = nombre d’étapes par canal <sub>source \ Device (Number \ of \ Channels \ in \ source \ Device)</sub> x Number of Channels in output Device

Comme vous pouvez le voir, la taille de la table augmente de façon exponentielle en fonction du nombre de canaux de l’appareil source. De nombreux appareils sources prennent en charge trois canaux de couleurs, par exemple, rouge, vert et bleu. Toutefois, si un appareil source prend en charge quatre canaux, tels que CMJN, la taille de la table et le temps nécessaire à la construction de la table augmentent d’un facteur du nombre d’étapes. Dans un CMS basé sur des mesures où les transformations sont construites « à la volée », cette durée peut être inacceptable.

Pour réduire le temps nécessaire à la construction de la table de conversion des couleurs, il est possible de tirer parti de deux faits. Tout d’abord, tandis que l’appareil source peut prendre en charge plus de trois canaux de couleurs, l’espace de couleurs indépendant du périphérique intermédiaire (CIECAM02 ja <sub>c</sub> b <sub>c</sub> ) n’a que trois canaux de couleur. Deuxièmement, la partie la plus longue du traitement n’est pas la modélisation de l’appareil (conversion des coordonnées de couleur de l’appareil aux valeurs tristimuluss), mais le mappage de la gamme. À l’aide de ces faits, vous pouvez construire une table de conversion des couleurs préliminaire qui convertit les couleurs dans l’espace de couleurs indépendant du périphérique, par le biais des étapes de mappage de la gamme, et enfin, via le modèle de couleur du périphérique de sortie. La construction de cette table est de la dimension 3. Ensuite, nous créons la dimension 4 de la table de conversion des couleurs finales en convertissant les combinaisons de couleurs sources en espace indépendant du périphérique, puis en utilisant la table de conversion des couleurs préliminaires, vous terminez la conversion dans l’espace de couleurs de l’appareil de sortie. Ainsi, vous réduisez le calcul (nombre d’étapes dans le tableau de recherche) <sub>Number \ of \ chaînes</sub> gammes de correspondances calculées au nombre d’étapes dans les calculs de mappage de gamme ₃ de la table intermédiaire. Même si vous devez effectuer un certain nombre d’étapes dans le (table de recherche) <sub>Number \ of \ Channels</sub> calcule la modélisation de l’appareil et les recherches dans la table en trois dimensions, cette opération est encore beaucoup plus rapide que le calcul original.

Le processus précédent fonctionne bien, à condition qu’il n’est pas nécessaire de passer des informations entre le modèle d’appareil source et tout autre composant dans la transformation de couleur. Toutefois, si le périphérique de sortie et l’appareil source prennent tous deux en charge une couleur noire et que la couleur noire source est utilisée pour déterminer la couleur noire de sortie, le processus ne parvient pas à communiquer correctement les informations noires de la source. Un autre processus consiste à construire une table de conversion de couleurs préliminaire qui convertit les couleurs dans l’espace de couleurs indépendant du périphérique par le biais des étapes de mappage de la gamme. Ensuite, construisez la dimension 4 table de conversion des couleurs finales en procédant comme suit : a) convertir les combinaisons de couleurs source en espace indépendant du périphérique, b) effectuer les étapes de mappage de la gamme de couleurs en interpolant dans la table des couleurs préliminaires au lieu d’appliquer les processus de mappage de gamme réels, et c) utiliser les valeurs obtenues à partir des étapes de mappage de gamme et les informations de canal noir source pour calculer les couleurs de périphérique de sortie à l' Ce processus peut également être utilisé lorsque des informations sont transférées entre les modèles d’appareil source et de sortie, même s’il n’y a pas de canal noir. par exemple, si les deux modules sont implémentés avec une architecture de plug-in qui autorise l’échange de données entre les modules.

Les deux processus précédents peuvent être utilisés pour améliorer efficacement le temps nécessaire à la construction de la table de transformation des couleurs à quatre dimensions.

### <a name="checkgamut"></a>CheckGamut

L’ICM appelle CreateTransform et **CreateMultiProfileTransform** prend un mot de valeurs d’indicateur, dont l’une est active la vérification de la \_ gamme \_ . Lorsque cet indicateur est défini, CITE doit créer la transformation différemment. Les étapes initiales sont les mêmes : les CAM source et de destination doivent être initialisées, puis les descripteurs de la limite de la gamme source et de destination doivent être initialisés. Quelle que soit l’intention spécifiée, le MGM CheckGamut doit être utilisé. Le MGM CheckGamut doit être initialisé à l’aide des modèles d’appareil source et de destination et des descripteurs de limites de gamme. Toutefois, la transformation doit ensuite créer une transformation tronquée comprenant le modèle d’appareil source, le CAM source, tous les MGM intermédiaires et le MGM CheckGamut. Cela garantit que les valeurs Delta J, Delta C et Delta h générées par l’CheckGamut CMM deviennent les valeurs finales obtenues.

La signification de CheckGamut est claire quand il n’y a que deux profils d’appareil dans la transformation. Lorsqu’il existe plus de deux profils d’appareil et plus de deux MGM, CheckGamut signale si les couleurs qui ont été transformées par le premier modèle d’appareil et tous les MGM sauf le dernier se trouvent dans la gamme du périphérique de destination.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Concepts de base de la gestion des couleurs](basic-color-management-concepts.md)
</dt> <dt>

[Schémas et algorithmes du système de couleurs Windows](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 




