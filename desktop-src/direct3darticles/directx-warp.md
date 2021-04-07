---
title: Guide de la plateforme de rastérisation avancée Windows (WARP)
description: Cet article décrit la plateforme Windows Advanced rastérisation (WARP) et les aspects suivants de WARP.
ms.assetid: C40A96EB-64AA-46EB-85A9-7C996ABC8BFE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1c09c29dd7b935542f0238cde0a71cbc97fce23
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729244"
---
# <a name="windows-advanced-rasterization-platform-warp-guide"></a>Guide de la plateforme de rastérisation avancée Windows (WARP)

Cet article décrit la plateforme Windows Advanced rastérisation (WARP) et les aspects suivants de WARP.

-   [Qu’est-ce que la distorsion ?](#what-is-warp)
-   [Avantages de la déformation](#warp-benefits)
    -   [Suppression du besoin de Rastériseurs logiciels personnalisés](#removing-the-need-for-custom-software-rasterizers)
    -   [Activation des performances maximales à partir du matériel graphique](#enabling-maximum-performance-from-graphics-hardware)
    -   [Activation du rendu lorsque le matériel Direct3D n’est pas disponible](#enabling-rendering-when-direct3d-hardware-is-not-available)
    -   [Exploitation des ressources existantes pour le rendu logiciel](#leveraging-existing-resources-for-software-rendering)
    -   [Activation de scénarios qui ne nécessitent pas de matériel graphique](#enabling-scenarios-that-do-not-require-graphics-hardware)
    -   [Finalisation de la plateforme graphique DirectX](#completing-the-directx-graphics-platform)
-   [Fonctionnalités et exigences de distorsion](#warp-capabilities-and-requirements)
-   [Utilisation de WARP](#how-to-use-warp)
-   [Types d’application recommandés pour WARP](#recommended-application-types-for-warp)
    -   [Jeux informels](#casual-games)
    -   [Applications sans jeu existantes](#existing-non-gaming-applications)
    -   [Jeux de rendu avancés](#advanced-rendering-games)
    -   [Autres applications](#other-applications)
-   [Architecture et performances de la distorsion](#warp-architecture-and-performance)
-   [Conformité de la distorsion](#warp-conformance)

## <a name="what-is-warp"></a>Qu’est-ce que la distorsion ?

WARP est un rastériseur logiciel à grande vitesse et entièrement conforme. Il s’agit d’un composant de la technologie graphique DirectX introduit par le runtime Direct3D 11. Le runtime Direct3D 11 est installé sur Windows 7, Windows Server 2008 R2 et Windows Vista avec la \[ \] mise à jour KB971644. Windows 8, Windows 10, Windows Server 2012 & versions ultérieures et Windows RT incluent le runtime Direct3D 11,1, qui dispose d’une version mise à jour de WARP. Windows 10 automne Creators Update (1709) comprend une version de WARP qui prend en charge les runtimes Direct3D 11 et Direct3D 12.

## <a name="warp-benefits"></a>Avantages de la déformation

WARP offre les avantages suivants :

-   [Suppression du besoin de Rastériseurs logiciels personnalisés](#removing-the-need-for-custom-software-rasterizers)
-   [Activation des performances maximales à partir du matériel graphique](#enabling-maximum-performance-from-graphics-hardware)
-   [Activation du rendu lorsque le matériel Direct3D n’est pas disponible](#enabling-rendering-when-direct3d-hardware-is-not-available)
-   [Exploitation des ressources existantes pour le rendu logiciel](#leveraging-existing-resources-for-software-rendering)
-   [Activation de scénarios qui ne nécessitent pas de matériel graphique](#enabling-scenarios-that-do-not-require-graphics-hardware)
-   [Finalisation de la plateforme graphique DirectX](#completing-the-directx-graphics-platform)

### <a name="removing-the-need-for-custom-software-rasterizers"></a>Suppression du besoin de Rastériseurs logiciels personnalisés

La distorsion simplifie le développement en éliminant le besoin de créer un rastériseur logiciel personnalisé et de l’adapter à votre application au lieu de paramétrer votre application pour le matériel. En fournissant un rastériseur logiciel unique et à usage général, vous n’avez plus besoin d’écrire des algorithmes de rendu d’image de plusieurs façons pour s’exécuter sur du matériel ou des logiciels avec des fonctionnalités et des fonctionnalités différentes. Vous pouvez toujours implémenter des algorithmes de plusieurs façons pour améliorer les performances ou la mise à l’échelle ; Toutefois, vous n’avez pas besoin de modifier l’architecture d’API ou de rendu utilisée pour implémenter ces algorithmes. Au lieu de cela, vous pouvez vous concentrer sur la création d’une application Direct3D 10 ou version ultérieure qui se présente de la même façon et s’exécute correctement sur le matériel ou les logiciels.

### <a name="enabling-maximum-performance-from-graphics-hardware"></a>Activation des performances maximales à partir du matériel graphique

Quand une application est configurée pour s’exécuter efficacement sur du matériel, elle s’exécute également efficacement sur la distorsion. L’inverse est également vrai ; toutes les applications réglées pour s’exécuter correctement sur WARP s’exécutent correctement sur le matériel. Les applications qui utilisent Direct3D 10 et versions ultérieures peuvent ne pas être mises à l’échelle de manière efficace sur un matériel différent. WARP possède des profils de performances similaires à ceux du matériel. ainsi, si vous paramétrez une application pour des lots volumineux, en minimisant les changements d’État, la suppression des points de synchronisation ou des verrous tirera parti du matériel et de la distorsion

### <a name="enabling-rendering-when-direct3d-hardware-is-not-available"></a>Activation du rendu lorsque le matériel Direct3D n’est pas disponible

WARP permet un rendu rapide dans différentes situations où les implémentations matérielles sont indésirables ou indisponibles, notamment :

-   Quand l’utilisateur ne dispose d’aucun matériel de compatibilité Direct3D
-   Quand une application s’exécute en tant que service ou dans un environnement serveur
-   Quand une application souhaite réserver les ressources matérielles Direct3D pour d’autres utilisations
-   Quand une carte vidéo n’est pas installée
-   Lorsqu’un pilote vidéo n’est pas disponible ou ne fonctionne pas correctement
-   Quand la mémoire d’une carte vidéo est insuffisante, se bloque ou nécessite un trop grand nombre de ressources système pour s’initialiser

### <a name="leveraging-existing-resources-for-software-rendering"></a>Exploitation des ressources existantes pour le rendu logiciel

Il existe une vaste communauté, de nombreux livres, des sites Web, des kits de développement logiciel (SDK), des exemples, des livres blancs, des listes de diffusion et d’autres ressources qui peuvent vous aider à tirer parti du rendu d’image basé sur le nuanceur Direct3D 10 et versions ultérieures. Avec WARP comme solution de secours logicielle, vous pouvez utiliser les connaissances existantes sur le matériel pour améliorer les performances de votre application lorsqu’elle s’exécute avec du matériel ou des logiciels. En outre, de nombreux excellents outils des fournisseurs de cartes graphiques et du kit de développement logiciel (SDK) DirectX peuvent vous aider à concevoir, générer, développer, déboguer et analyser les problèmes de performances des applications graphiques. Ces outils et connaissances peuvent désormais tirer parti du développement d’applications qui ciblent le matériel et les logiciels lorsque vous utilisez la distorsion.

### <a name="enabling-scenarios-that-do-not-require-graphics-hardware"></a>Activation de scénarios qui ne nécessitent pas de matériel graphique

Les différents algorithmes et applications (algorithmes de traitement des images, impression, communication à distance, PC virtuels et autres émulateurs, rendu des polices de haute qualité, graphiques, graphiques, etc.) ont généralement été optimisés pour le processeur, car ils ne dépendent pas du matériel. Avec WARP, vous pouvez utiliser une architecture unique qui exécute ces algorithmes et applications, et qui peut s’exécuter entièrement dans le logiciel. Pourtant, si l’accélération matérielle est disponible, vous pouvez en tirer parti.

### <a name="completing-the-directx-graphics-platform"></a>Finalisation de la plateforme graphique DirectX

WARP vous permet d’accéder à toutes les fonctionnalités graphiques Direct3D 10 et versions ultérieures, même sur des ordinateurs sans matériel graphique Direct3D 10 et versions ultérieures. Les bits des fonctionnalités de Direct3D 10 ont été supprimés (Cap); autrement dit, vous n’avez plus besoin de vérifier si les fonctionnalités graphiques sont disponibles à partir du matériel graphique, car Direct3D 10 et versions ultérieures garantissent cette disponibilité. Vous pouvez désormais utiliser toutes les fonctionnalités d’un large éventail de cartes vidéo en sachant que leur application se comportera et aura le même aspect partout. Vous pouvez mettre à l’échelle les performances de ces applications en désactivant simplement les fonctionnalités graphiques onéreuses sur les cartes vidéo de bas niveau ou le rendu sur des cibles plus petites.

## <a name="warp-capabilities-and-requirements"></a>Fonctionnalités et exigences de distorsion

WARP prend entièrement en charge toutes les fonctionnalités Direct3D 10 et 10,1. Par exemple, WARP prend en charge les fonctionnalités les plus importantes suivantes :

-   Toutes les exigences de précision de la spécification Direct3D 10 et 10,1
-   Direct3D 11 lorsqu’il est utilisé avec les niveaux de fonctionnalité 9 \_ 1, 9 \_ 2, 9 \_ 3, 10 \_ 0 et 10 \_ 1 (pour plus d’informations sur les niveaux de fonctionnalité, consultez [**\_ \_ niveau de fonctionnalité D3D**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level)).
-   Tous les formats de texture facultatifs, tels que les exemples de cibles de rendu et d’échantillonnage à partir de surfaces flottantes
-   Rendu avec anticrénelage et haute qualité jusqu’à 8x (multiéchantillonner l’anticrénelage)
-   Filtrage anisotrope
-   applications 32 bits et 64 bits et applications 32 bits prenant en charge les adresses volumineuses

Quand vous installez la [mise à jour de la plateforme pour Windows 7](https://support.microsoft.com/kb/2670838) sur Windows 7 SP1 ou windows Server 2008 R2 SP1, ce système d’exploitation comprend le runtime Direct3D 11,1 et une version de Warp qui prend en charge Direct3D 11. x lorsqu’il est utilisé avec les [niveaux de fonctionnalité](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ 1, 9, 9 \_ \_ 3, 10 \_ \_ 1 et 11 \_ 0.

Windows 8, Windows 10, Windows Server 2012 & versions ultérieures et Windows RT incluent le runtime Direct3D 11,1 et une nouvelle version de WARP. Cette version prend en charge Direct3D 11. x lorsqu’elle est utilisée avec les [niveaux de fonctionnalité](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ 1, 9 \_ 2, 9 \_ 3, 10 \_ 0, 10 \_ 1, 11 \_ 0 et 11 \_ 1.

Windows 10 automne Creators Update (1709) comprend une nouvelle version de WARP qui prend en charge les niveaux de fonctionnalité [Direct3D 12](../direct3d12/direct3d-12-graphics.md) 12 \_ 0 et 12 \_ 1. 

La configuration minimale requise pour la déformation est la même que pour Windows Vista, en particulier :

-   UC minimum 800 MHz
-   MMX, SSE ou SSE2 ne sont pas requis
-   Minimum 512 Mo de RAM

## <a name="how-to-use-warp"></a>Utilisation de WARP

Les composants Direct3D 10, 10,1, 11 et 12 peuvent utiliser un type de pilote supplémentaire que vous pouvez spécifier lors de la création de l’appareil (par exemple, lorsque vous appelez la fonction [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) ). Ce type de pilote est D3D10 type de pilote [**\_ \_ \_ Warp**](/windows/desktop/api/d3d10misc/ne-d3d10misc-d3d10_driver_type) ou [**D3D. \_ \_ type \_ Warp**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_driver_type). Lorsque vous spécifiez ce type de pilote, le runtime crée un appareil de distorsion et n’initialise pas de périphérique matériel.

Étant donné que WARP utilise la même interface logicielle pour Direct3D que le rastériseur de référence, toute application Direct3D pouvant prendre en charge l’exécution avec le rastériseur de référence peut être testée à l’aide de WARP. Pour utiliser la distorsion, renommez D3d10warp.dll en D3d10ref.dll et placez-le dans le même dossier que l’exemple ou l’application. Ensuite, lorsque vous basculez vers REF, vous verrez le rendu de la distorsion.

Si vous renommez WARP en D3d10ref.dll et que vous le placez dans C : \\ Program Files (x86) \\ SDK Microsoft DirectX (juin 2010) \\ Samples \\ C++ \\ Direct3D \\ bin \\ x86, vous pouvez exécuter tous les exemples DirectX sur Warp, soit en cliquant sur le bouton « Toggle REF » dans l’exemple, soit en exécutant l’exemple avec/ref spécifié sur la ligne de commande.

## <a name="recommended-application-types-for-warp"></a>Types d’application recommandés pour WARP

Toutes les applications qui peuvent utiliser Direct3D peuvent utiliser WARP. Cela comprend les types d’applications suivants :

-   [Jeux informels](#casual-games)
-   [Applications sans jeu existantes](#existing-non-gaming-applications)
-   [Jeux de rendu avancés](#advanced-rendering-games)
-   [Autres applications](#other-applications)

### <a name="casual-games"></a>Jeux informels

Les jeux ont généralement des exigences de rendu simples. Toutefois, ils nécessitent également l’utilisation d’effets visuels impressionnants, qui peuvent nécessiter une accélération matérielle. La majorité des titres de jeux les plus vendus pour Windows sont les simulations ou les jeux informels, qui ne nécessitent pas de graphiques à hautes performances. Toutefois, les deux styles de jeux tirent parti des graphiques basés sur un nuanceur moderne et de la capacité de mise à l’échelle du matériel.

### <a name="existing-non-gaming-applications"></a>Applications sans jeu existantes

Une grande quantité d’applications graphiques requièrent un nombre minimal de chemins de code dans leur couche de rendu. WARP permet à ces applications d’implémenter un chemin de code Direct3D unique qui peut cibler un grand nombre de configurations d’ordinateur.

### <a name="advanced-rendering-games"></a>Jeux de rendu avancés

Les développeurs de jeux peuvent souhaiter isoler les erreurs de rendu propres aux cartes graphiques ou aux pilotes. Par conséquent, tous les jeux, même les jeux extrêmement exigeants, peuvent tirer parti de la possibilité d’afficher leur contenu à l’aide de WARP. Vous pouvez utiliser WARP pour vérifier si des artefacts visuels que vous trouvez présentent des erreurs ou des problèmes liés au matériel ou aux pilotes.

### <a name="other-applications"></a>les autres applications ;

Les applications cibles pour WARP incluent également celles qui peuvent ne pas utiliser Direct3D 10 ou Direct3D 10,1. Ces applications cibles incluent des applications qui doivent toujours fonctionner sur tous les ordinateurs, les applications de traitement d’images qui n’écrivent pas les versions d’UC et de GPU des algorithmes de traitement d’image, les algorithmes de traitement d’image où la vitesse ou l’utilisation du GPU n’est pas critique, comme l’impression, les émulateurs et les environnements virtuels qui affichent des graphiques 3D avancés

## <a name="warp-architecture-and-performance"></a>Architecture et performances de la distorsion

WARP est basé sur le code base du rastériseur de référence. Par conséquent, WARP utilise la même interface logicielle pour Direct3D 10 et versions ultérieures et DXGI. WARP est inclus dans Windows 7 dans le D3d10warp.dll, situé dans dossiers systèmes Windows. Deux versions de WARP sont installées sur les ordinateurs 64 bits, une version x86 et x64. La version x64 peut s’exécuter plus rapidement dans certaines circonstances, car le générateur de code contenu dans WARP peut tirer parti des registres supplémentaires disponibles quand les utilisateurs exécutent des applications 64 bits.

WARP contient les deux compilateurs haute vitesse et en temps réel suivants :

-   Le compilateur de langage intermédiaire de haut niveau qui convertit le bytecode HLSL et l’état de rendu actuel en un flux optimisé de commandes vectorielles pour les étapes de nuanceur de géométrie (GS), de nuanceur de sommets (VS) et de nuanceur de pixels (PS) du pipeline.
-   Le générateur de code juste-à-temps hautes performances qui peut prendre ces commandes et générer le code d’assembly SSE2, SSE 4.1, x86, x64, ARM et arm64 optimisé.

WARP utilise le pool de threads et la gestion des tâches complexes et le suivi des dépendances introduits dans Windows Vista pour permettre la distribution efficace de toutes les parties du pipeline de rendu sur les cœurs de processeur disponibles.

WARP utilise le rendu différé. Autrement dit, la distorsion peut afficher par lot des commandes afin que la pixellisation se produise uniquement lorsque des données suffisantes sont disponibles pour utiliser efficacement toutes les ressources du processeur. Le travail sur le thread d’application principal est réduit pour permettre à l’application d’envoyer des commandes aussi rapidement que possible. Si une application est également multithread et qu’elle utilise le pool de threads, le travail est réparti uniformément entre la WARP et l’application.

Le générateur de code WARP a été réglé pour tirer le meilleur parti de l’architecture d’UC moderne. WARP s’exécute sur tous les ordinateurs qui peuvent exécuter Windows Vista et les systèmes d’exploitation ultérieurs, même si l’ordinateur ne prend pas en charge SSE. Toutefois, la déformation a été optimisée pour les ordinateurs qui prennent en charge SSE2. Il contient également des optimisations pour des architectures spécifiques de processeurs AMD et Intel, ainsi que la prise en charge des extensions SSE 4,1.

WARP ne nécessite pas l’exécution de matériel graphique. Il peut s’exécuter même dans des situations où le matériel n’est pas disponible ou ne peut pas être initialisé.

Les applications et les exemples qui ont été conçus et générés pour s’exécuter sur un matériel Direct3D 10 et ultérieur sans aucune connaissance de la distorsion s’exécuteront probablement correctement à l’aide de WARP. Toutefois, nous vous recommandons de réduire autant que possible les paramètres et la résolution de qualité pour atteindre des fréquences d’images utilisables. Vous pouvez utiliser WARP pour développer et paramétrer des applications qui s’exécutent correctement sur le matériel et les logiciels.

Étant donné que WARP utilise plusieurs cœurs de processeur, il fonctionne mieux sur les processeurs quadruple cœur modernes. WARP s’exécute également beaucoup plus rapidement sur les ordinateurs sur lesquels sont installés des extensions SSE 4.1. Microsoft a effectué des tests et un réglage des performances significatifs sur les ordinateurs dotés de huit cœurs ou plus et de SSE 4.1, car ces ordinateurs de haut niveau sont plus courants pendant la durée de vie des systèmes d’exploitation Windows 7 et versions ultérieures.

Lorsque la déformation est exécutée sur l’UC, elle est limitée par rapport à une carte graphique de plusieurs façons. La vitesse du bus frontal d’un processeur est généralement d’environ 10 Go/s. En revanche, une carte graphique a souvent une mémoire dédiée qui utilise 20 à 100 Go/s ou plus de bande passante graphique. Le matériel graphique comporte également des unités à fonction fixe qui peuvent exécuter des tâches complexes et coûteuses, telles que le filtrage de texture, la décompression de format ou les conversions, de manière asynchrone, avec peu de surcharge ou un coût d’électricité. L’exécution de ces opérations sur un processeur standard est coûteuse en termes de consommation d’énergie et de cycles de performances.

Les numéros de performances typiques d’une machine à quatre cœurs Intel Penryn 3,0 GHz montrent que la distorsion peut parfois surpasser les GPU graphiques de type Direct3D 10 et versions ultérieures intégrés de bas niveau sur un certain nombre de tests d’évaluation. Le matériel graphique discret de bas de gamme est généralement 4 à 5 fois plus rapide que la déformation lors de l’exécution de ces tests. Ces GPU intégrées ou discrètes bas de gamme ont une utilisation minimale des ressources du processeur. Les cartes graphiques de milieu ou haut de gamme sont beaucoup plus rapides que la déformation pour de nombreuses applications, en particulier lorsqu’une application peut tirer parti du parallélisme et de la bande passante de mémoire que ces cartes graphiques fournissent.

La déformation ne remplace pas le matériel graphique, en particulier par l’exécution raisonnable de Direct3D 10 de bas de gamme et des matériels discrets ultérieurs. L’objectif de la distorsion est de permettre aux applications de cibler le matériel de niveau Direct3D 10 sans avoir des chemins de code ou des conditions de test très différents, qu’ils s’exécutent sur du matériel ou dans des logiciels.

Les deux tableaux suivants présentent des exemples de données WARP avec différents processeurs et cartes graphiques.

Le premier tableau montre des exemples de données de déviation avec Direct3D 10 Crysis s’exécutant à 800x600 avec tous les paramètres de qualité sur leurs niveaux les plus bas :

| Processeur                         | Temps   | Moy. FPS | FPS min. | Frame min. | Nbre max. d’images | Trame max. |
|-----------------------------|--------|---------|---------|-----------|---------|-----------|
| Core i7 8 Core @ 3,0 GHz     | 271,57 | 7,36    | 3.46    | 1966      | 15,01   | 995       |
| Penryn 4 cœurs @ 3,0 GHz      | 351,35 | 5,69    | 2.49    | 1967      | 10,95   | 980       |
| Penryn 2 cœurs @ 3,0 GHz      | 573,98 | 3.48    | 1,35    | 1964      | 6,61    | 988       |
| Core 2 Duo à 2,6 GHz         | 707,19 | 2.83    | 0.81    | 1959      | 5.18    | 982       |
| Core 2 Duo à 2,4 GHz         | 763,25 | 2.62    | 0.76    | 1964      | 4.70    | 984       |
| Core 2 Duo @ 2,1 GHz         | 908,87 | 2.20    | 0,64    | 1965      | 3.72    | 986       |
| Xeon 8 cœur @ 2.0 GHz        | 424,04 | 4.72    | 1.84    | 1967      | 9,56    | 988       |
| AMD FX74 4 cœurs @ 3,0 GHz    | 583,12 | 3.43    | 1,41    | 1967      | 5,78    | 986       |
| Phenom 9550 4 cœur @ 2,2 GHz | 664,69 | 3.01    | 0,53    | 1959      | 5.46    | 987       |

Le deuxième tableau montre des exemples de données exécutant le même test sur une variété de cartes graphiques :

| Carte graphique         | Temps   | Moy. FPS | FPS min. | Frame min. | Nbre max. d’images | Trame max. |
|-----------------------|--------|---------|---------|-----------|---------|-----------|
| NVIDIA 8800 GTS       | 23,58  | 84,80   | 60,78   | 1957      | 130,83  | 1022      |
| NVIDIA 8500 GT        | 47,63  | 41,99   | 25,67   | 1986      | 72,57   | 991       |
| NVIDIA Quadro 290     | 67,16  | 29,78   | 18,19   | 1969      | 49,87   | 1017      |
| NVIDIA 8400 GS        | 59,01  | 33,89   | 21,22   | 1962      | 51,82   | 1021      |
| ATI 3400              | 53,79  | 37,18   | 22,97   | 618       | 59,77   | 1021      |
| ATI 3200              | 67,19  | 29,77   | 18,91   | 1963      | 45,74   | 980       |
| ATI 2400 PRO          | 67,04  | 29,83   | 17,97   | 606       | 45,91   | 987       |
| Intel facilement intégré | 386,94 | 5.17    | 1,74    | 1974      | 16,22   | 995       |

## <a name="warp-conformance"></a>Conformité de la distorsion

WARP réussit tous les tests de conformité WHQL (Windows Hardware Quality Labs) standard pour la validation des périphériques matériels Direct3D.

WARP a été testé par rapport à une suite d’applications et d’évaluation Direct3D 10 et Direct3D 10,1, ainsi qu’à des exemples du kit de développement logiciel (SDK) de DirectX, NVIDIA et AMD.

WARP a utilisé l’outil de débogage et d’analyse [pix](https://msdn.microsoft.com/library/ee417062(v=VS.85).aspx) pour Windows dans son test. Microsoft dispose d’une grande bibliothèque de captures de frames uniques d’applications qui sont utilisées pour effectuer une comparaison entre le matériel et la distorsion. La majorité des images s’affichent presque identiques entre le matériel et la déformation ; Si de petites différences se produisent parfois, elles se trouvent dans les tolérances définies par la spécification Direct3D 10.