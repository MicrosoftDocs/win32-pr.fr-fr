---
title: API graphiques dans Windows
description: Cet article traite des API et des fonctionnalités graphiques de Windows.
ms.assetid: 54cd5027-cdcf-fc4a-40a9-beacfaa08681
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7543ee7c5e3cdbfb022cc9299dd5ddd3cdd36981
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382564"
---
# <a name="graphics-apis-in-windows"></a>API graphiques dans Windows

Windows Vista prend en charge un modèle de pilote d’affichage entièrement nouveau qui représente une révision majeure de la conception des pilotes vidéo depuis l’introduction du Windows Driver Model (WDM) pour Windows 98. Ce modèle repensé reflète l’évolution du matériel vidéo du monde des opérations 2D raster et des applications GDI à celles des jeux 3D avec un matériel graphique à fonction fixe, et enfin à celle de l’unité de traitement graphique (GPU) programmable moderne qui prend en charge une large gamme d’applications graphiques hautes performances. Windows 7 et Windows 8 sont générés sur l’infrastructure graphique de Windows Vista en fournissant des fonctionnalités graphiques et des API supplémentaires. Cet article traite des API et des fonctionnalités graphiques de Windows.

-   [Contexte](#background)
-   [Direct3D 9](#direct3d-9)
-   [Direct3D 9Ex](#direct3d-9ex)
-   [Direct3D 10](#direct3d-10)
-   [Direct3D 10,1](#direct3d-101)
-   [Direct3D 11](#direct3d-11)
-   [Direct3D 11,1](#direct3d-111)
-   [Technologie](#opengl)
-   [Compatibilité des applications, GDI et versions antérieures de Direct3D](#application-compatibility-gdi-and-older-versions-of-direct3d)
-   [Recommandations](#recommendations)

## <a name="background"></a>Arrière-plan

L’API principale pour la programmation de graphiques depuis les premiers jours de Windows est l’interface GDI (Graphical Device Interface). Cette API a été conçue pour gérer de nombreux périphériques de sortie 2D et est basée sur la base de l’interface utilisateur Windows. DirectDraw et Direct3D ont été introduits en tant qu’autres API pour prendre en charge les jeux en plein écran et le rendu 3D en tant qu’extensions du matériel existant du moment. Les interactions avec GDI étaient compliquées. L’intermélange efficace des éléments GDI traditionnels avec les éléments Direct3D a été limité par cette conception. La version Windows XP de WDM, appelée XPDM, reflète la nature côte à côte de GDI et Direct3D (voir figure 1).

**Figure 1. API graphiques dans Windows XP**

![XPDM](images/graphics-apis-in-windows-xp.gif)

Au fil des années, la puissance des cartes vidéo en 3D a considérablement augmenté jusqu’au point où la grande majorité du matériel est dédiée à cette fonction. Un nouveau modèle de pilote, WDDM (Windows Display Driver Model), fait passer le GPU et Direct3D au Forefront, ce qui permet la création d’une expérience entièrement nouvelle, le bureau 3D, qui fusionne en toute transparence le monde 2D de GDI avec la puissance des GPU programmables modernes. Avec WDDM, le matériel vidéo est entièrement piloté par Direct3D, et toutes les autres interfaces graphiques communiquent avec le matériel vidéo via le nouveau modèle de pilote orienté Direct3D (voir la figure 2).

**Figure 2. API graphiques dans Windows Vista**

![WDDM](images/graphics-apis-in-windows-vista.gif)

Pour plus d’informations sur le WDDM, consultez le [Guide de conception de Windows Vista Display Driver Model (WDDM)](/windows-hardware/drivers/display/windows-vista-display-driver-model-design-guide) sur MSDN.

## <a name="direct3d-9"></a>Direct3D 9

La version 9 de DirectX était d’abord publiée pour Windows dans 2002, avec les mises à jour suivantes dans 2003 et 2004. Cette API représente une décennie d’évolution des technologies DirectX, l’introduction de modèles de programmation de nuanceur plus puissants pour Direct3D, ainsi qu’une maturité avec des milliers de titres d’expédition. Direct3D 9 est l’interface graphique principale de Windows Vista. Il reste l’API idéale pour l’écriture de jeux et d’applications 3D qui doivent s’exécuter sur un large éventail de versions matérielles et Windows existantes. Les détails du nouveau modèle de pilote sont masqués dans les applications qui utilisent les interfaces Direct3D 9, mais en coulisses, le système d’exploitation tire pleinement parti des nouvelles fonctionnalités pour offrir une véritable multitâche du GPU, une gestion des ressources plus efficace et des performances robustes.

Pour garantir une compatibilité complète avec les versions antérieures de Windows, certains excentriques de l’ancien modèle de pilote doivent être émulées, même avec le nouveau modèle de pilote d’affichage de Windows Vista. Par exemple, lorsqu’une application en plein écran perd le focus, elle doit supposer qu’elle a perdu toutes les ressources de la mémoire vidéo (VRAM) et recharger celles qu’elle a créées en tant que ressources non managées, même si le nouveau modèle de pilote gère les ressources de manière transparente sans les supprimer du contexte de périphérique. Même le concept de type de ressource géré et par défaut est spécifique à l’ancien modèle de pilote. Un autre exemple est l’attente d’une défaillance lors de l’allocation de ressources non gérées (pool par défaut) dépassant la quantité de mémoire vive disponible, même si le nouveau modèle de pilote peut fournir une quantité quasiment illimitée de mémoire vidéo virtuelle. En raison de ces exigences, les applications Direct3D s’exécutant sous Windows Vista recevront toujours ces conditions d’erreur. Par conséquent, ils sont limités à leur capacité à utiliser les interfaces Direct3D 9 de base pour utiliser pleinement certaines fonctionnalités du nouveau modèle de pilote.

Alors que les nouveaux systèmes commercialisés avec Windows Vista incluent des cartes vidéo avec des pilotes WDDM et que de nouveaux pilotes pour plusieurs cartes vidéo populaires sont inclus dans la zone, Windows Vista continue de prendre en charge la possibilité d’utiliser des pilotes XPDM plus anciens pour les mises à niveau et les éditions de l’entreprise. Sur les systèmes utilisant l’ancien modèle de pilote, vous devez utiliser Direct3D 9 et des interfaces plus anciennes, et le fonctionnement du système graphique est très similaire à celui de Windows XP (figure 1). WDDM est requis pour que les applications utilisent Direct3D 9Ex, Direct3D 10 et les versions ultérieures.

## <a name="direct3d-9ex"></a>Direct3D 9Ex

L’interface Direct3D 9Ex fournit un accès à une légère extension de l’API standard Direct3D 9 qui expose l’allocation de ressources virtualisée, une nouvelle sémantique de périphérique perdue et d’autres nouvelles fonctionnalités disponibles lors de l’exécution sur Windows Vista. En créant cet objet étendu, l’API Direct3D 9 utilise la nouvelle sémantique. par conséquent, l’application doit utiliser une logique différente (et donc des chemins de code différents) pour la création de ressources, la gestion et la gestion des erreurs pour de nouveaux types de conditions. Cette API est disponible uniquement sur Windows Vista et requiert des pilotes WDDM. Étant donné que Direct3D 9Ex utilise une API et un chemin de code de pilote distincts de Direct3D 9, la prise en charge de cette API nécessite des cas de test supplémentaires pour votre application.

La principale raison de la création de la nouvelle API de Direct3D 9Ex consistait à permettre un accès complet aux nouvelles fonctionnalités du WDDM tout en conservant la compatibilité pour les applications Direct3D existantes. Le nouveau bureau 3D et de nombreuses applications spécifiques à Windows Vista utilisent cette version de Direct3D 9, mais elles ne sont pas fonctionnelles quand elles s’exécutent sur des pilotes XPDM plus anciens. Étant donné que l’API de Direct3D 9Ex n’apparaît jamais sur les versions antérieures de Windows en raison d’un manque de prise en charge du WDDM, les interfaces standard Direct3D 9 couvrent un ensemble de systèmes bien plus large. Pour les applications à hautes performances qui peuvent tirer parti de la nouvelle génération de matériel vidéo, la version 10 complète de Direct3D offre de nombreuses nouvelles fonctionnalités qui ne sont pas exposées par Direct3D 9Ex. Par conséquent, pour les jeux et la plupart des autres applications, Direct3D 9 ou Direct3D 10 est l’API recommandée.

> [!Note]  
> Le kit de développement logiciel (SDK) DirectX ne fournit pas d’exemples, d’en-têtes ou de bibliothèques pour l’interface Direct3D 9Ex. MSDN Library et SDK Windows (anciennement appelé Platform SDK) contiennent la documentation, les en-têtes et les bibliothèques disponibles.

 

Pour plus d’informations sur Direct3D 9Ex, consultez [DirectX pour Windows Vista](/previous-versions//ms681824(v=vs.85)) sur MSDN.

## <a name="direct3d-10"></a>Direct3D 10

Pour tirer pleinement parti du potentiel du nouveau modèle de pilote Windows Vista et du matériel de nouvelle génération, une version entièrement nouvelle de l’API Direct3D a été créée. Bien que WDDM élimine certaines des limitations des performances dans le système graphique existant, Direct3D 10 va plus loin en supprimant les goulots d’étranglement de conception dans l’API Direct3D existante, et simplifie grandement la programmation du GPU.

La nouvelle API élimine complètement tous les aspects de fonction fixe, à l’exception de quelques-unes, en les remplaçant par des constructions programmables et en rationalisant considérablement l’implémentation interne. Les centaines de bits de capacité des versions précédentes de Direct3D ont été complètement supprimés et remplacés par un ensemble de fonctionnalités bien défini et limité qui n’a que quelques scénarios d’utilisation facultatifs pour des formats de ressources spécifiques. La création et la validation de ressources nécessitant une utilisation intensive du processeur ont désormais une sémantique explicite dans la nouvelle API. Cela permet un comportement de performances beaucoup plus prévisible et une surcharge par dessin fortement réduite. Les ressources peuvent être reconfigurées en plusieurs formes pour permettre une utilisation efficace à différentes étapes, et l’ensemble de fonctionnalités impose des restrictions beaucoup moins nombreuses sur les scénarios d’utilisation pour les formats. Il existe également de nouveaux formats de texture de la carte normale compressés par bloc.

Dans la nouvelle API, les constantes de nuanceur et l’état de l’appareil sont des ressources explicites, ce qui permet une mise en cache beaucoup plus efficace sur le matériel et simplifie considérablement la validation des pilotes. Le modèle de nuanceur programmable a été unifié sur les nuanceurs vertex et de pixels, et rendu plus expressif avec un modèle de calcul et un ensemble d’opérateurs bien définis. En outre, une nouvelle étape de nuanceur Geometry a été ajoutée pour fonctionner sur les primitives après l’étape du nuanceur de sommets. Les résultats du travail du GPU dans les étapes vertex et Geometry Shader du pipeline peuvent être transmis à la RAM vidéo en vue de leur réutilisation, ce qui permet d’effectuer des opérations GPU à plusieurs passes extrêmement complexes avec une interaction minimale du processeur.

Toutes ces améliorations permettent la technologie graphique de nouvelle génération et étendent la capacité des applications à décharger le travail sur le GPU. Le déchargement permet d’obtenir des pelures de caractères basés sur le GPU plus complexes. techniques de morphage accélérées, génération et extrusion de volume de clichés instantanés, systèmes de particule et physique qui sont entièrement des matériaux basés sur GPU, plus complexes, combinés en lots à grande échelle efficaces, en décrivant des procédures, en temps réel de mappage de déplacement par Ray, en création de mappage de cube à passage unique et de nombreuses autres techniques, tout en libérant des ressources

Pour fournir ce niveau d’innovation dans Direct3D 10, le matériel plus ancien ne peut pas être exprimé comme une implémentation partielle d’une nouvelle interface. Une carte vidéo peut prendre en charge toutes les nouvelles fonctionnalités ou il ne s’agit pas d’une carte compatible Direct3D 10. Par conséquent, bien que Direct3D 9 puisse piloter le matériel DirectX7-Era avec de nombreuses fonctionnalités manquantes et des limitations d’utilisation, Direct3D 10 fonctionne uniquement sur une nouvelle génération de cartes vidéo. Pour qu’une application prenne en charge un matériel vidéo plus ancien, elle doit également prendre en charge les interfaces Direct3D 9. Les futures versions de Direct3D s’appuieront sur la version 10, en l’étendant aux nouvelles versions de l’API tout en garantissant un sur-ensemble strict de fonctionnalités Direct3D 10.

Pour plus d’informations sur Direct3D 10, consultez [Direct3D 10](/windows/desktop/direct3d10/d3d10-graphics).

## <a name="direct3d-101"></a>Direct3D 10,1

Windows Vista Service Pack 1 étend l’API Direct3D 10 avec Direct3D 10,1, qui ajoute des interfaces facultatives et un modèle de nuanceur supplémentaire pour prendre en charge les nouvelles fonctionnalités matérielles des cartes vidéo qui prennent en charge Direct3D 10,1. Tout le matériel capable de prendre en charge Direct3D 10,1 prend également entièrement en charge toutes les fonctionnalités de Direct3D 10, et les développeurs de jeux peuvent utiliser les fonctionnalités supplémentaires de Direct3D 10,1, le cas échéant.

> [!Note]  
> Direct3D 10,1 est l’API Graphics utilisée par le bureau Windows 7.

 

> [!Note]  
> Windows 7 et la mise à jour de Windows Vista ([KB 971644](https://support.microsoft.com/kb/971644)) ajoutent la prise en charge des DXGI 1,1, 10level9 Feature levels et WARP10 Device à l’API Direct3D 10,1 existante.

 

## <a name="direct3d-11"></a>Direct3D 11

Windows 7 prend en charge une nouvelle révision de Direct3D, Direct3D 11, basée sur la conception de l’API Direct3D 10,1. Les nouvelles fonctionnalités de l’API incluent le rendu multithread et la création de ressources, le nuanceur de calcul, la prise en charge des niveaux de fonctionnalités 10level9 et l’appareil de rendu logiciel WARP10, ainsi que de nouvelles fonctionnalités matérielles de classe Direct3D 11 telles que la pavage à l’aide des nuanceurs de domaine de la coque &, des formats de compression de texture BC6H et BC7, du 5,0 modèle de La nouvelle API peut utiliser des cartes vidéo Direct3D 10 et 10,1 Class existantes, certaines cartes Direct3D 9 via les niveaux de fonctionnalité 10level9 avec une prise en charge limitée des fonctionnalités et la dernière génération de cartes vidéo de la classe Direct3D 11.

En plus de l’API Direct3D 11, Windows 7 comprend DXGI 1,1, Direct2D, DirectWrite et la prise en charge des pilotes WDDM 1,1.

> [!Note]  
> Direct3D 11 et les API associées sont également disponibles en tant que mise à jour de Windows Vista (voir la [base de connaissances 971644](https://support.microsoft.com/kb/971644)).

 

## <a name="direct3d-111"></a>Direct3D 11,1

Windows 8 étend l' [API Direct3D 11](#direct3d-11) avec Direct3D 11,1. Direct3D 11,1 prend en charge tous les matériels existants qui [disposent](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) de \_ la prise en charge des niveaux 11, 10 x et 9 \_ x, ainsi qu’un nouveau \_ niveau de fonctionnalité 11 1.

En plus de l' [API Direct3D 11,1](/windows/desktop/direct3d11/direct3d-11-1-features), Windows 8 comprend [DXGI 1,2](/windows/desktop/direct3ddxgi/dxgi-1-2-improvements), les [contextes de périphérique Direct2D](/windows/desktop/Direct2D/devices-and-device-contexts)et la prise en charge des pilotes WDDM 1,2.

> [!Note]  
> Si vous souhaitez que vos applications du Windows Store programment des graphiques 3D avec DirectX, vous pouvez utiliser l’API Direct3D 11,1. Pour plus d’informations sur la programmation de graphiques 3D avec DirectX, consultez [Introduction aux graphiques 3D avec DirectX](/previous-versions/windows/apps/hh465137(v=win.10)).

 

**Mise à jour de plateforme pour Windows 7 :** La prise en charge partielle est disponible pour l' [API Direct3D 11,1](/windows/desktop/direct3d11/direct3d-11-1-features) sur Windows 7 ou windows Server 2008 R2 avec la [mise à jour de plateforme pour Windows 7](https://support.microsoft.com/kb/2670838) installée. Pour plus d’informations sur la mise à jour de plateforme pour Windows 7, consultez [mise à jour de la plateforme pour Windows 7](platform-update-for-windows-7.md).

## <a name="opengl"></a>Technologie

Windows Vista, Windows 7 et Windows 8 offrent la même prise en charge que Windows XP pour OpenGL, qui permet aux fabricants de cartes vidéo de fournir un pilote client installable (ICD) pour OpenGL qui fournit un support accéléré par le matériel. Notez que les versions plus récentes de ces ICDs sont requises pour prendre entièrement en charge Windows Vista, Windows 7 ou Windows 8. Si aucun ICD n’est installé, le système revient à la couche logicielle OpenGL v 1.1 dans la plupart des cas.

## <a name="application-compatibility-gdi-and-older-versions-of-direct3d"></a>Compatibilité des applications, GDI et versions antérieures de Direct3D

Les systèmes graphiques Windows Vista, Windows 7 et Windows 8 sont conçus pour prendre en charge un large éventail de scénarios de matériel et d’utilisation pour permettre de nouvelles technologies tout en continuant à prendre en charge les systèmes existants. Les interfaces graphiques existantes, telles que GDI, GDI+ et les versions antérieures de Direct3D, continuent de fonctionner sur Windows Vista et Windows 7, mais sont remappées en interne dans la mesure du possible. Cela signifie que la majorité des applications Windows existantes continueront à fonctionner.

Windows Vista, Windows 7 et Windows 8 continuent de prendre en charge les mêmes interfaces Direct3D et DirectDraw que Windows XP, jusqu’à la version 3 de DirectX (à l’exception du mode Retained Direct3D’s, qui a été supprimé). À l’instar de Windows XP Professionnel Édition x64, les applications natives 64 bits sur les versions plus récentes de Windows sont limitées à des interfaces Direct3D9, DirectDraw7 ou plus récentes. Les applications à hautes performances doivent utiliser Direct3D 9 ou une version ultérieure pour s’assurer qu’elles ont la correspondance la plus proche possible avec les fonctionnalités matérielles.

## <a name="recommendations"></a>Recommandations

Tenez compte des recommandations suivantes lors de la sélection d’une API pour votre application graphique :

-   Utilisez Direct3D 9 Si votre application doit prendre en charge Windows XP ou une version antérieure de Windows.
-   Utilisez Direct3D 9 Si vous souhaitez prendre en charge Windows Vista ou Windows 7 s’exécutant avec des pilotes XPDM. Pour les systèmes Windows Vista ou Windows 7 qui n’ont pas Direct3D 10 ou un matériel vidéo plus performant, vous pouvez choisir d’utiliser le chemin de code Windows XP Direct3D 9 existant ou utiliser les niveaux de fonctionnalité 10level9 via l’API Direct3D 10,1 ou Direct3D 11.
-   Utilisez Direct3D 11 pour tirer parti de la nouvelle génération de matériel vidéo sur Windows Vista, Windows 7 et Windows 8. Les applications du Windows Store doivent utiliser Direct3D 11 ou une version ultérieure.

 

 