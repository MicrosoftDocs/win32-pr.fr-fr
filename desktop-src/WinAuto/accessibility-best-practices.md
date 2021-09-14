---
title: Meilleures pratiques d'accessibilité
description: L’implémentation des meilleures pratiques décrites dans cette section permet de s’assurer que votre application est accessible aux personnes qui utilisent des produits de technologie d’assistance.
ms.assetid: ef694361-49b7-424c-a583-1eadc2519db7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38d9f70828610d04255b61ad3ee533d23c514867
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010731"
---
# <a name="accessibility-best-practices"></a>Meilleures pratiques d'accessibilité

L’implémentation des meilleures pratiques décrites dans cette section permet de s’assurer que votre application est accessible aux personnes qui utilisent des produits de technologie d’assistance. La plupart de ces meilleures pratiques se concentrent sur une bonne conception de l’interface utilisateur. Chaque meilleure pratique comprend des informations d’implémentation pour les contrôles ou les applications. Dans de nombreux cas, une grande partie du travail pour répondre à ces meilleures pratiques est déjà incluse dans les contrôles.

Cette rubrique contient les sections suivantes.

-   [Accès par programme](#programmatic-access)
    -   [Activer l'accès par programmation à tous les éléments de l'interface utilisateur et le texte](#enable-programmatic-access-to-all-ui-elements-and-text)
    -   [Placer des noms, titres et descriptions sur les objets, les cadres et les pages de l'interface utilisateur](#place-names-titles-and-descriptions-on-ui-objects-frames-and-pages)
    -   [Vérifier que les événements par programmation sont déclenchés par toutes les activités de l'interface utilisateur](#ensure-programmatic-events-are-triggered-by-all-ui-activities)
-   [Paramètres utilisateur](#user-settings)
    -   [Respecter tous les paramètres au niveau du système et ne pas interférer avec les fonctions d'accessibilité](#respect-all-system-wide-settings-and-do-not-interfere-with-accessibility-functions)
-   [Conception de l'interface utilisateur visuelle](#visual-ui-design)
    -   [Ne pas Hard-Code les couleurs](#do-not-hard-code-colors)
    -   [Prendre en charge le contraste élevé et tous les attributs de l'affichage du système](#support-high-contrast-and-all-system-display-attributes)
    -   [Vérifier que toute l'interface utilisateur est correctement mise à l'échelle par tous les paramètres PPP](#ensure-all-ui-correctly-scales-by-any-dpi-setting)
-   [Navigation au clavier](#keyboard-navigation)
    -   [Fournir une interface de clavier pour tous les éléments de l'interface utilisateur](#provide-keyboard-interface-for-all-ui-elements)
    -   [Afficher le focus clavier](#show-the-keyboard-focus)
    -   [Prendre en charge les standards de navigation et les schémas de navigation puissants](#support-navigation-standards-and-powerful-navigation-schemes)
    -   [Ne pas laisser l'emplacement de la souris interférer avec la navigation au clavier](#do-not-let-mouse-location-interfere-with-keyboard-navigation)
-   [Interface multimodale](#multi-modal-interface)
    -   [Fournir des équivalents sélectionnables par l'utilisateur pour les éléments non-texte](#provide-user-selectable-equivalents-for-non-text-elements)
    -   [Utiliser la couleur mais fournir également des alternatives à la couleur](#use-color-but-also-provide-alternatives-to-color)
    -   [Utiliser les API d'entrée standard avec des appels indépendants de l’appareil](#use-standard-input-apis-with-device-independent-calls)
-   [Rubriques connexes](#related-topics)

## <a name="programmatic-access"></a>Accès par programme

Les meilleures pratiques décrites dans cette section Enure que les produits de technologie d’assistance disposent d’un accès par programmation adéquat aux informations et aux fonctionnalités de l’interface utilisateur.

### <a name="enable-programmatic-access-to-all-ui-elements-and-text"></a>Activer l'accès par programmation à tous les éléments de l'interface utilisateur et le texte

Les éléments d’interface utilisateur de votre application doivent être accessibles par programmation aux produits de technologie d’assistance. Tous les éléments d’interface utilisateur doivent avoir des étiquettes, ils doivent exposer toutes les valeurs de propriété et doivent déclencher tous les événements appropriés. pour les contrôles de Windows standard, la majeure partie de ce travail est déjà effectuée par le biais des objets de proxy microsoft UI Automation et microsoft Active Accessibility. Toutefois, les contrôles personnalisés nécessitent un travail supplémentaire pour s’assurer qu’ils sont entièrement exposés afin que les fournisseurs de technologie d’assistance puissent identifier et manipuler les éléments de l’interface utilisateur de votre application.

Suivre cette meilleure pratique permet aux fournisseurs de technologies d’assistance d’identifier et de manipuler les éléments de l’interface utilisateur de votre produit.

### <a name="place-names-titles-and-descriptions-on-ui-objects-frames-and-pages"></a>Placer des noms, titres et descriptions sur les objets, les cadres et les pages de l'interface utilisateur

Étant donné que les produits de technologie d’assistance, en particulier les lecteurs d’écran, utilisent des titres pour comprendre l’emplacement d’un cadre, d’un objet ou d’une page dans le schéma de navigation, les titres doivent être très descriptifs. De bons titres descriptifs permettent aux produits de technologie d’assistance d’identifier et de manipuler les éléments d’interface utilisateur dans les contrôles et les applications. Par exemple, le titre de la page Web « Microsoft Web page » est inutile si l’utilisateur a navigué profondément dans une zone particulière. Un titre descriptif est essentiel pour les utilisateurs aveugles et en fonction des lecteurs d’écran.

L’application de cette meilleure pratique permet aux produits de technologie d’assistance d’identifier et de manipuler l’interface utilisateur dans des exemples de contrôles et d’applications.

### <a name="ensure-programmatic-events-are-triggered-by-all-ui-activities"></a>Vérifier que les événements par programmation sont déclenchés par toutes les activités de l'interface utilisateur

Votre application doit déclencher des événements chaque fois que des modifications se produisent dans l’État ou l’apparence d’un élément d’interface utilisateur.

Suivre cette meilleure pratique permet aux produits de technologie d’assistance d’écouter les modifications apportées à l’interface utilisateur et d’informer l’utilisateur de ces modifications.

## <a name="user-settings"></a>Paramètres utilisateur

La meilleure pratique décrite dans cette section permet de vérifier que les contrôles et les applications n'écrasent pas les paramètres utilisateur.

### <a name="respect-all-system-wide-settings-and-do-not-interfere-with-accessibility-functions"></a>Respecter tous les paramètres au niveau du système et ne pas interférer avec les fonctions d'accessibilité

Les utilisateurs peuvent utiliser le panneau de configuration pour définir certains indicateurs à l’ensemble du système. d’autres indicateurs peuvent être définis par programmation. Ces paramètres ne doivent pas être modifiés par des contrôles ou des applications. Les applications doivent aussi prendre en charge les paramètres d'accessibilité du système d'exploitation hôte.

L'application de cette meilleure pratique permet aux utilisateurs de définir des paramètres d'accessibilité et de savoir que ceux-ci ne seront pas modifiés par les applications.

## <a name="visual-ui-design"></a>Conception de l'interface utilisateur visuelle

Les meilleures pratiques décrites dans cette section garantissent que les contrôles ou les applications utilisent la couleur et les images de manière efficace et peuvent être utilisés par les produits de technologie d’assistance.

### <a name="do-not-hard-code-colors"></a>Ne pas Hard-Code les couleurs

Les personnes qui ne perçoivent pas les couleurs, qui ont une acuité visuelle réduite ou qui utilisent un écran noir et blanc risquent de ne pas pouvoir utiliser les applications dont les couleurs sont codées en dur.

L'application de cette meilleure pratique permet aux utilisateurs d'ajuster les combinaisons de couleurs en fonction de leurs besoins.

### <a name="support-high-contrast-and-all-system-display-attributes"></a>Prendre en charge le contraste élevé et tous les attributs de l'affichage du système

Les applications ne doivent pas perturber ou désactiver les paramètres sélectionnés par l'utilisateur et définis au niveau du système, ni les sélections des couleurs ou d'autres paramètres et attributs au niveau du système. Les paramètres au niveau du système qui sont adoptés par un utilisateur améliorent l'accessibilité des applications, ils ne doivent donc pas être désactivés ou ignorés par les applications. Les couleurs doivent être utilisées dans leur combinaison correcte du premier plan sur l'arrière-plan afin de fournir un contraste approprié. Les couleurs qui ne se marient pas bien ne doivent pas être mélangées, et les couleurs ne doivent pas être inversées.

De nombreux utilisateurs requièrent des combinaisons de contraste élevé spécifiques, telles que du texte blanc sur un arrière-plan noir. Les afficher de façon inversée, comme du texte noir sur un arrière-plan blanc, provoque la bavure de l'arrière-plan sur le premier plan et peut entraîner des difficultés de lecture pour certains utilisateurs.

### <a name="ensure-all-ui-correctly-scales-by-any-dpi-setting"></a>Vérifier que toute l'interface utilisateur est correctement mise à l'échelle par tous les paramètres PPP

Assurez-vous que tous les éléments d’interface utilisateur peuvent être mis à l’échelle correctement en fonction du paramètre de points par pouce (dpi). Assurez-vous également que les éléments d’interface utilisateur s’ajustent à un écran de 1024 x 768 avec 120 points par pouce (dpi).

## <a name="keyboard-navigation"></a>Navigation au clavier

Les meilleures pratiques décrites dans cette section garantissent que toutes les fonctionnalités de l’application sont accessibles aux utilisateurs qui reposent sur le clavier.

### <a name="provide-keyboard-interface-for-all-ui-elements"></a>Fournir une interface de clavier pour tous les éléments de l'interface utilisateur

Les taquets de tabulation, en particulier lorsqu’ils sont soigneusement planifiés, offrent aux utilisateurs une autre façon de naviguer dans l’interface utilisateur.

Les applications doivent fournir les interfaces de clavier suivantes :

-   Les taquets de tabulation pour tous les contrôles avec lesquels l’utilisateur peut interagir, comme les boutons, les liens ou les zones de liste.
-   Ordre de tabulation logique.

### <a name="show-the-keyboard-focus"></a>Afficher le focus clavier

Les utilisateurs ont besoin de savoir quel est l'objet qui a le focus clavier afin de pouvoir anticiper l'effet de leurs séquences de touches. Pour mettre en surbrillance le focus clavier, utilisez des couleurs, des fontes ou des graphiques tels que les rectangles ou l'agrandissement. Pour mettre en évidence de façon audible le focus clavier, modifiez le volume, la fréquence du son ou la qualité de la tonalité.

Pour éviter toute confusion, les applications doivent cacher tous les indicateurs de focus visuels et estomper les sélections situées sur les fenêtres ou les panneaux inactifs.

Les applications doivent procéder comme suit en ce qui concerne le focus clavier :

-   Un élément doit toujours avoir le focus clavier.
-   Le focus clavier doit être visible et évident.
-   Les sélections et/ou les éléments ayant le focus doivent être visuellement mis en surbrillance.

### <a name="support-navigation-standards-and-powerful-navigation-schemes"></a>Prendre en charge les standards de navigation et les schémas de navigation puissants

Différents aspects de la navigation au clavier offrent aux utilisateurs différents moyens de naviguer dans l’interface utilisateur.

Les applications doivent fournir les interfaces de clavier suivantes :

-   Touches de raccourci et touches d’accès soulignées pour l’ensemble des commandes, menus et contrôles.
-   Raccourcis clavier vers des liens importants.
-   Tous les éléments de menu ont une touche d’accès ; tous les boutons ont des touches accélérateur ; toutes les commandes ont une touche accélérateur.

### <a name="do-not-let-mouse-location-interfere-with-keyboard-navigation"></a>Ne pas laisser l'emplacement de la souris interférer avec la navigation au clavier

L'emplacement de la souris ne doit pas interférer avec la navigation au clavier. Par exemple, si la souris est positionnée quelque part et que l'utilisateur est en train de naviguer avec le clavier, il ne doit pas se produire de clic de souris, à moins qu'il soit initié par l'utilisateur.

## <a name="multi-modal-interface"></a>Interface multimodale

La meilleure pratique dans cette section s’assure que l’interface utilisateur de l’application comprend des alternatives pour les éléments visuels.

### <a name="provide-user-selectable-equivalents-for-non-text-elements"></a>Fournir des équivalents sélectionnables par l'utilisateur pour les éléments non-texte

Pour chaque élément non-texte, fournissez un équivalent sélectionnable par l'utilisateur pour le texte, les transcriptions ou les descriptions audio, comme du texte alternatif, des légendes ou une rétroaction visuelle.

Les éléments non-texte couvrent un large éventail d’éléments d’interface utilisateur, notamment : les images, les régions d’images interactives, les animations, les applets, les cadres, les scripts, les boutons graphiques, les sons, les fichiers audio autonomes et la vidéo. Les éléments non-texte sont importants lorsqu’ils contiennent des informations visuelles, de la parole ou des informations audio générales auxquelles l’utilisateur a besoin d’accéder pour comprendre le contenu de l’interface utilisateur.

### <a name="use-color-but-also-provide-alternatives-to-color"></a>Utiliser la couleur mais fournir également des alternatives à la couleur

Utilisez la couleur pour améliorer, accentuer ou réitérer des informations déjà affichées par d'autres moyens, mais ne communiquez pas des informations uniquement à l'aide des couleurs. Les utilisateurs qui ne perçoivent pas les couleurs ou qui ont un écran monochrome ont besoin d'alternatives à la couleur.

### <a name="use-standard-input-apis-with-device-independent-calls"></a>Utiliser les API d'entrée standard avec des appels indépendants de l’appareil

Les appels indépendants du périphérique garantissent que tous les périphériques d’entrée sont traités de la même manière, tout en fournissant des produits de technologie d’assistance avec les informations nécessaires sur l’interface utilisateur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows Vue d’ensemble de l’API Automation](windows-automation-api-overview.md)
</dt> </dl>

 

 




