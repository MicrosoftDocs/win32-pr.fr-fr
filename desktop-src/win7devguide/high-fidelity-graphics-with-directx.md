---
title: Graphiques haute fidélité avec DirectX
description: les développeurs d’applications Windows ont longtemps utilisé Microsoft DirectX pour fournir des graphiques 3d de haute qualité, à accélération matérielle.
ms.assetid: db555657-90b9-4db2-a0c2-bfaa526a8dd5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9ecb5d6403745162f19b16eea15c22ef7f9676b14bd291226af2f8321483b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086642"
---
# <a name="high-fidelity-graphics-with-directx"></a>Graphiques haute fidélité avec DirectX

les développeurs d’applications Windows ont longtemps utilisé Microsoft DirectX pour fournir des graphiques 3d de haute qualité, à accélération matérielle. Lorsque la technologie s’est lancée dans 1995, les développeurs peuvent fournir des graphiques 3D de haute qualité pour les jeux et les applications d’ingénierie pour les joueurs et les professionnels désireux de payer des suppléments pour une carte graphique 3D. Aujourd’hui, même les PC les plus peu coûteux incluent le matériel 3D-Graphics.

pour tirer parti de ces fonctionnalités graphiques, Windows Vista a introduit l’infrastructure WDDM (Windows Display Driver Model) pour DirectX qui permettait à plusieurs applications et services de partager les ressources de l’unité de traitement graphique (GPU). le Gestionnaire de fenêtrage (DWM) utilise cette technologie pour animer le changement de tâche en 3d, fournir des images miniatures dynamiques des fenêtres d’application et fournir des effets Windows Aero glass pour les applications de bureau.

Windows 7 met encore plus de fonctionnalités graphiques dans les mains des développeurs d’applications. Grâce à un nouvel ensemble de DirectXAPIs, les développeurs Microsoft Win32 peuvent tirer parti des innovations les plus récentes des GPU pour ajouter des graphiques, du texte et des images de haute qualité, extensibles, 2D et 3D à leurs applications. Sur les écrans *LCD* les plus récents, DirectXAPIs peut afficher le contenu du bureau et de la fenêtre en utilisant une profondeur de couleur supérieure à 8 bits par composant de couleur.

avec DirectX, les développeurs Win32 peuvent également utiliser le parallélisme du GPU pour le calcul à usage général, comme le traitement de l’image, et peuvent effectuer un rendu sur le matériel directx 10, le matériel directx 9, l’uc ou sur un ordinateur distant Windows. ces technologies ont été conçues pour interagir avec Windows Graphics Device Interface (GDI) et Windows GDI+, garantissant que les développeurs peuvent facilement conserver leurs investissements existants dans du code Win32. (Voir [Nouveautés du kit de développement logiciel (SDK) DirectX du 2009 mars](/previous-versions//bb173043(v=vs.85)).)

Ces fonctionnalités graphiques améliorées sont fournies par les API *com* suivantes :

-   [Direct2D](../direct2d/direct2d-portal.md) pour le dessin de graphiques 2D.
-   [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) pour organiser et afficher le texte.
-   [Windows composant de création](/windows/desktop/wic/-wic-lh) d’images pour le traitement et l’affichage d’images.
-   [Direct3D 10](/windows/desktop/direct3d10/d3d10-graphics) pour le dessin de graphiques 3D.
-   [Direct3D 11](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) permet de dessiner des graphiques 3D et de fournir un accès à des technologies GPU de nouvelle génération, telles que la polygonalisation, la prise en charge limitée de la diffusion en continu des textures et l’informatique à usage général.
-   [DirectX Graphics infrastructure (dxgi)](/windows/desktop/direct3ddxgi/dx-graphics-dxgi) pour la gestion des périphériques d’affichage locaux et distants et des ressources GPU, ainsi que l’interopérabilité entre DirectX et GDI.

## <a name="direct2d"></a>Direct2D

reposant sur Microsoft Direct3D 10, [Direct2D](../direct2d/direct2d-portal.md) offre aux développeurs Win32 des api 2d indépendantes du mode de résolution, qui utilisent la puissance du matériel graphique de nouvelle génération, mais interagissent bien avec les applications GDI/GDI+ actuelles et les applications Direct3D 10. Direct2D fournit un rendu 2D de haute qualité avec des performances supérieures à GDI et GDI+. Il permet aux développeurs Win32 de contrôler plus précisément les ressources et leur gestion. (Consultez [Direct2D](../direct2d/direct2d-portal.md).)

## <a name="directwrite"></a>DirectWrite

La plupart des applications d’aujourd’hui doivent prendre en charge le rendu de texte de haute qualité, les polices de contour indépendantes de la résolution et la prise en charge complète du texte et de la disposition Unicode. [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal), un nouveau composant DirectX, offre les fonctionnalités suivantes :

-   Système de disposition de texte indépendant du périphérique qui améliore la lisibilité du texte dans les documents et dans l’interface utilisateur.
-   Rendu de texte *ClearType* de haute qualité, sous-pixel, qui peut utiliser GDI, [Direct2D](../direct2d/direct2d-portal.md)ou la technologie de rendu propre à l’application.
-   Texte avec accélération matérielle, lorsqu’il est utilisé avec [Direct2D](../direct2d/direct2d-portal.md).
-   Prise en charge du texte à plusieurs formats.
-   Prise en charge des fonctionnalités typographiques avancées des polices *OpenType* .
-   Prise en charge de la disposition et du rendu du texte dans toutes les langues prises en charge.
-   Mise en page et rendu compatibles GDI.

le système de police [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) active l’utilisation des polices « n’importe quelle police », où les utilisateurs n’ont pas à effectuer une étape d’installation distincte simplement pour utiliser une police, et une hiérarchie structurelle améliorée de regroupement de polices pour faciliter la découverte de polices manuelle ou par programmation. Les API prennent en charge la mesure, le dessin et le test d’atteinte du texte à plusieurs formats. DirectWrite gère le texte dans toutes les langues prises en charge pour les applications globales et localisées, en se basant sur l’infrastructure de langage clé qui se trouve dans Windows 7. DirectWrite fournit également des api de rendu de glyphes de bas niveau pour les développeurs qui souhaitent effectuer leur propre disposition et un traitement Unicode-à-glyphe. (Voir [DirectWrite](../directwrite/direct-write-portal.md).)

## <a name="windows-imaging-component"></a>Composant Windows Imaging

dans Windows Vista, le [composant Windows Imaging](/windows/desktop/wic/-wic-lh) a introduit une infrastructure extensible pour l’utilisation des images et des métadonnées d’image. les formats d’image pris en charge par Windows composant de création d’images incluent *JPEG*, *PNG* et *TIFF*, et les formats de métadonnées pris en charge incluent *XMP* et *EXIF*. avec Windows 7, Windows composant d’imagerie élargit sa conformité aux normes en fournissant une prise en charge du décodage d’image progressive, des fonctionnalités *PNG* étendues, des métadonnées *GIF* et des métadonnées qui s’étendent sur les segments *APPn* . (voir [nouveautés de WIC dans Windows 7](/previous-versions//ee720061(v=vs.85)).)

## <a name="direct3d-11"></a>Direct3D 11

Microsoft direct3d 11 étend les fonctionnalités du pipeline direct3d 10 et fournit Windows 7 jeux et des applications 3d haut de gamme avec un accès efficace, robuste et évolutif à la prochaine génération de gpu et d’uc à plusieurs cœurs. En plus des fonctionnalités disponibles dans Direct3D 10, Direct3D 11 introduit plusieurs nouvelles fonctionnalités.

Les surfaces Geometry et de poids fort peuvent maintenant être fractionnées pour prendre en charge le contenu dynamique évolutif dans les représentations de la surface de la sous-division et des patchs.

Pour tirer le meilleur parti de la puissance de traitement parallèle disponible à partir de plusieurs cœurs de processeur, le multithreading augmente le nombre d’appels de rendu potentiels par trame en répartissant l’application, le runtime et les appels de pilote sur plusieurs cœurs. En outre, la création et la gestion des ressources ont été optimisées pour une utilisation multithread, ce qui permet une meilleure gestion de la texture dynamique pour la diffusion en continu.

De nouveaux nuanceurs de calcul à usage général ont été créés pour Direct3D 11. Contrairement aux nuanceurs existants, il s’agit des extensions du pipeline programmable qui permettent à votre application d’effectuer davantage de travail sur le GPU, indépendamment de l’UC. [**DrawAuto**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-drawauto), qui a été introduit dans Direct3D 10, a été étendu pour interagir avec un nuanceur de calcul.

Plusieurs améliorations ont été apportées au langage[HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl)(large-Level Shading Language), telles qu’une forme limitée de liaison dynamique dans les nuanceurs pour améliorer la complexité de la spécialisation, et les constructions de programmation orientée objet comme les classes et les interfaces. (Voir [Nouveautés du kit de développement logiciel (SDK) DirectX du 2009 mars](/previous-versions//bb173043(v=vs.85)).)

## <a name="direct3d-10-improvements"></a>Améliorations de Direct3D 10

Direct3D 10 comprend un pipeline graphique remanié avec des étapes de nuanceur programmable et des objets d’État immuables pour initialiser les étapes à fonction fixe. Les objets d’État simplifient le pipeline et améliorent les performances en minimisant le nombre de modifications d’État requises. La programmabilité des étapes du nuanceur offre désormais des extensions de langage d’ombrage de haut niveau pour prendre en charge des instructions de nuanceur illimitées, des ressources de nuanceur généralisées et des calculs d’entiers et de bits.

Le pipeline présente également l’étape de nuanceur Geometry, qui décharge entièrement le travail du processeur vers le GPU. Cette nouvelle phase vous permet de créer une géométrie, de transmettre les données en mémoire et de rendre la géométrie sans interaction de l’UC.

Plusieurs autres améliorations sont conçues spécifiquement pour accélérer les performances. Le rendu prédicat effectue une élimination d’occlusion pour réduire la quantité de géométrie rendue. Les API d’instanciation peuvent réduire considérablement la quantité de géométrie qui doit être transférée vers le GPU en dessinant plusieurs instances d’objets similaires. Les tableaux de texture permettent au GPU d’effectuer un échange de texture sans intervention de l’UC.

Plusieurs ajouts ont été apportés à Direct3D 10 et Direct3D 11 pour étendre la gamme de configurations pouvant être ciblées avec ces API. la [plateforme de rastérisation avancée (WARP) de Windows](/windows/desktop/direct3darticles/directx-warp) met en œuvre un rendu rapide et évolutif multicœur pour Direct3D 10, ce qui permet un rendu graphique complet sur les systèmes ne disposant pas de matériel graphique. L’ajout de nouveaux « niveaux de fonctionnalité », spécifiquement appelés [Direct3D 10 Level 9](/windows/desktop/direct3d11/d3d11-graphics-reference-10level9), permet aux 11APIs Direct3D 10 et Direct3D de piloter le matériel Microsoft Direct3D 9, en étendant le nombre de configurations qu’une application Direct3D 10 ou Direct3D 11 peut cibler sur presque tous les systèmes informatiques du marché. (Voir [graphiques Direct3D 10](../direct3d10/d3d10-graphics.md).)

## <a name="directxgdi-interoperability"></a>Interopérabilité DirectX/GDI

dans Windows Vista, le comportement d’une application qui utilise à la fois DirectX et GDI pour effectuer un rendu sur une surface partagée est différent selon que le DWM est activé ou désactivé. en outre, lorsque DWM est activé, les applications qui utilisent à la fois DirectX et GDI se comportent différemment sur Windows Vista que sur Windows XP. de nombreux éditeurs de logiciels indépendants ont ainsi désactivé DWM lors de l’exécution de leurs applications sur Windows Vista pour garantir un comportement cohérent. grâce aux améliorations apportées à directx dans Windows 7, une application peut désormais librement mélanger directx et GDI sans désactiver DWM. Windows 7 offre également des performances améliorées pour les scénarios qui requièrent l’interopérabilité entre DirectX et GDI en utilisant les api Direct3D 10 plus efficaces. (Consultez [vue d’ensemble de l’interopérabilité de Direct2D et GDI](../direct2d/direct2d-and-gdi-interoperation-overview.md).)

 

 