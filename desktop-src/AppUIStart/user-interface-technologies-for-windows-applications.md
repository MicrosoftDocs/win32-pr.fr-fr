---
title: Technologies de l’interface utilisateur
description: Cette rubrique fournit une brève enquête sur les technologies Microsoft pour le développement d’interfaces utilisateur pour les applications Windows.
ms.assetid: 5ecbaaf0-704e-4c27-b3ce-b5436e577d62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7d9343672d064cf073ea8018758b90083f440bd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941280"
---
# <a name="user-interface-technologies"></a>Technologies de l’interface utilisateur

Cette rubrique fournit une brève enquête sur les technologies Microsoft pour le développement d’interfaces utilisateur pour les applications Windows. Il fournit les informations requises pour vous aider à déterminer s’il est nécessaire d’utiliser une technologie particulière et vous indique où trouver des informations supplémentaires à son sujet.

Cette rubrique décrit les technologies suivantes :

-   [Technologies d’interface utilisateur pour les applications non gérées](#user-interface-technologies-for-unmanaged-applications)
    -   [Contrôles Windows](#windows-controls)
    -   [Styles visuels](#visual-styles)
    -   [Infrastructure de ruban Windows](#windows-ribbon-framework)
    -   [Gestionnaire d’animations Windows](#windows-animation-manager)
    -   [Gestionnaire de fenêtres du Bureau](#desktop-window-manager)
    -   [API Windows Automation](#windows-automation-api)
    -   [API Microsoft Speech](#speech-api)
    -   [API de grossissement](#magnification-api)
    -   [Compilateur de ressources](#resource-compiler)
-   [Technologies d’interface utilisateur pour les applications managées](#user-interface-technologies-for-managed-applications)
    -   [Windows Forms](#windows-forms)
    -   [Windows Presentation Foundation](#windows-presentation-foundation)
    -   [Silverlight](#silverlight)
    -   [Expression Blend 3 + SketchFlow](/windows)
    -   [UI Automation pour les applications managées](#ui-automation-for-managed-applications)

## <a name="user-interface-technologies-for-unmanaged-applications"></a>Technologies d’interface utilisateur pour les applications non gérées

Cette section décrit les technologies Microsoft pour le développement d’interfaces utilisateur pour les applications Windows non managées. Ces technologies sont destinées aux développeurs C/C++ expérimentés qui connaissent bien les concepts de programmation WindowsAPI et qui utilisent le kit de développement logiciel (SDK) Microsoft Windows. Certaines technologies ont des conditions préalables supplémentaires, telles que la connaissance des problèmes de programmation de graphiques ou la connaissance des concepts de base de la programmation COM (Component Object Model).

### <a name="windows-controls"></a>Contrôles Windows

Les contrôles Windows sont des éléments d’interface utilisateur qui sont utilisés conjointement à une autre fenêtre (généralement une fenêtre cliente ou une boîte de dialogue) pour permettre à l’utilisateur d’interagir avec une application. La plupart des éléments qui composent l’interface utilisateur d’une application Windows traditionnelle sont des contrôles Windows, y compris des éléments tels que des menus, des barres de défilement, des boutons, des zones de liste, des arborescences, etc.

Les contrôles Windows sont pris en charge par toutes les versions de Windows. Toutefois, étant donné que les composants d’exécution qui prennent en charge les contrôles ont évolué au fil du temps, certains contrôles et fonctionnalités introduits dans les versions ultérieures ne sont pas pris en charge dans les versions antérieures. Les applications doivent détecter les versions et utiliser uniquement les fonctionnalités disponibles.

Vous devez utiliser des contrôles Windows si vous souhaitez créer une interface utilisateur traditionnelle pour une application Windows non gérée qui s’exécute sur un large éventail de versions de Windows.

Pour plus d’informations, consultez [contrôles Windows](../controls/window-controls.md).

### <a name="visual-styles"></a>Styles visuels

Les styles visuels sont des spécifications pour l’apparence des contrôles. Par exemple, un style visuel peut définir l’apparence générale des contrôles et permettre aux développeurs de logiciels de configurer l’interface visuelle de ces contrôles pour coordonner l’apparence d’une application. En outre, les styles visuels offrent un mécanisme permettant à toutes les applications Windows de normaliser l’apparence d’une application.

Les styles visuels sont pris en charge sur Windows XP et versions ultérieures, et n’affectent que l’apparence des contrôles Windows standard et des contrôles communs Microsoft Win32.

Vous devez utiliser des styles visuels si vous devez modifier l’apparence des contrôles Windows standard et des contrôles communs pour qu’ils correspondent à l’apparence de l’interface utilisateur de votre application.

Pour plus d’informations, consultez [styles visuels](../controls/themes-overview.md).

### <a name="windows-ribbon-framework"></a>Infrastructure de ruban Windows

L’infrastructure de ruban Windows est un système de présentation de commande riche pour les applications basées sur Windows. Il se compose d’une barre de commandes de ruban qui expose les principales fonctionnalités d’une application via une série d’onglets en haut d’une fenêtre d’application, et un système de menu contextuel. L’infrastructure de ruban Windows est prise en charge sur les versions suivantes de Windows :

-   Windows Vista avec Service Pack 2 (SP2) et mise à jour de plateforme pour Windows Vista
-   Windows 7 et ultérieur
-   Windows Server 2008 R2
-   Windows Server 2008 avec Service Pack 2 (SP2) et mise à jour de plateforme pour Windows Server 2008

Vous devez utiliser Windows Ribbon Framework si vous souhaitez implémenter une interface utilisateur de commande qui est une alternative aux menus superposés, aux barres d’outils et aux volets de tâches des applications Windows traditionnelles.

L’infrastructure de ruban Windows est destinée aux développeurs qui maîtrisent la programmation COM.

Pour plus d’informations, consultez [Windows Ribbon Framework](../windowsribbon/-uiplat-windowsribbon-entry.md).

### <a name="windows-animation-manager"></a>Gestionnaire d’animations Windows

Le gestionnaire d’animations Windows prend en charge l’animation des éléments d’interface utilisateur en fournissant un moteur d’animation puissant et une interface de programmation standardisée. La plateforme simplifie le développement et la maintenance des séquences d’animation de l’interface utilisateur et permet aux développeurs d’implémenter des animations d’interface utilisateur cohérentes et intuitives. L’animation Windows peut être utilisée avec n’importe quelle plateforme graphique, notamment Direct2D, Microsoft Direct3D ou Windows GDI+.

Windows animation Framework est pris en charge sur Windows Vista avec la mise à jour de la plateforme pour Windows VistaWindows Vista avec SP2 et la mise à jour de la plateforme pour Windows Vista et Windows 7 et versions ultérieures.

Vous devez utiliser le gestionnaire d’animations Windows si vous souhaitez ajouter des séquences d’animation à l’interface utilisateur d’une application Windows non gérée.

Pour plus d’informations, consultez [Windows animation Manager](../uianimation/-main-portal.md).

### <a name="desktop-window-manager"></a>Gestionnaire de fenêtres du Bureau

Gestionnaire de fenêtrage (DWM) est un composant d’exécution Windows qui prend en charge la composition du bureau, une fonctionnalité introduite dans Windows Vista. Grâce à la composition du bureau, DWM active les effets visuels dans l’interface utilisateur, tels que les cadres de fenêtres en verre, les animations de transition de fenêtre 3D, Windows Flip et Windows Flip3D, ainsi que la prise en charge de la haute résolution.

DWM expose une API pour contrôler un grand nombre des effets visuels associés à la composition du bureau. Par exemple, une application peut afficher des miniatures, appliquer un effet translucide et flou à la zone cliente des fenêtres de niveau supérieur, contrôler les effets de transparence et de transition utilisés dans la région non cliente de Windows, et ainsi de suite.

DWM est pris en charge sur Windows Vista et Windows Server 2008.

Vous devez utiliser DWM si votre application a besoin d’accéder aux effets visuels associés à la composition du bureau et de les contrôler.

Pour plus d’informations, consultez [Gestionnaire de fenêtrage](../dwm/dwm-overview.md).

### <a name="windows-automation-api"></a>API Windows Automation

L’API d’automatisation Windows aide les développeurs à créer des applications qui sont accessibles au public le plus vaste possible, y compris les personnes souffrant de troubles de la vision, de l’audition ou du mouvement. L’API fonctionne en exposant des informations sur les éléments qui composent une interface utilisateur d’application. Les applications de technologie d’assistance, telles que les lecteurs d’écran, peuvent utiliser les informations pour présenter l’interface utilisateur d’une manière qui peut être utilisée par des personnes handicapées.

L’API Windows Automation se compose de deux infrastructures d’API distinctes : Microsoft Active Accessibility et Microsoft UI Automation. Microsoft Active Accessibility est une API héritée qui a été introduite dans Windows 95 en tant que complément de plateforme. UI Automation est le successeur de Microsoft Active Accessibility et est une implémentation Windows de la spécification UI Automation.

La prise en charge complète de Microsoft Active Accessibility est intégrée à Windows XP et Windows Server 2003. Microsoft Active Accessibility est également pris en charge sur Windows NT 4,0 avec Service Pack 6 (SP6) et versions ultérieures, et sur Windows 98. UI Automation est pris en charge sur les systèmes d’exploitation suivants : Windows XP, Windows Server 2003, Windows Server 2003 R2, Windows Vista, Windows 7, Windows Server 2008 et Windows Server 2008 R2.

Si votre application contient des contrôles personnalisés ou d’autres fonctionnalités personnalisées de l’interface utilisateur, vous devez utiliser l’API d’automatisation Windows pour vous assurer que les contrôles et les fonctionnalités personnalisés sont entièrement accessibles. En général, les développeurs ont besoin d’un niveau modéré de compréhension des objets COM et des interfaces, d’Unicode et de la programmation de l’API Windows.

Pour plus d’informations, consultez [API Windows Automation](../winauto/windows-automation-api-portal.md).

### <a name="speech-api"></a>API Microsoft Speech

L’API Microsoft Speech (SAPI) fournit une interface de haut niveau entre une application et des moteurs de reconnaissance vocale. SAPI implémente tous les détails de bas niveau nécessaires pour contrôler et gérer les opérations en temps réel de divers moteurs de reconnaissance vocale.

Les deux principaux types de moteurs SAPI sont les systèmes TTS (Text-to-Speech) et les modules de reconnaissance vocale. Les systèmes TTS synthétisent les chaînes de texte et les fichiers en audio parlé à l’aide de voix synthétiques. Les reconnaissance vocale convertissent le contenu audio oral en chaînes et fichiers lisibles.

Vous devez utiliser SAPI si vous souhaitez implémenter une interface utilisateur qui permet à l’utilisateur d’interagir avec votre application par le biais de la reconnaissance vocale et TTS en plus des périphériques d’entrée standard tels que le clavier, la souris et l’affichage.

Pour plus d’informations, consultez [Microsoft Speech API (SAPI) 5,4](/previous-versions/windows/desktop/ee125663(v=vs.85)).

### <a name="magnification-api"></a>API de grossissement

L’API d’agrandissement (MAPI) est utilisée pour agrandir des parties de l’écran et pour appliquer des effets de couleur et d’autres transformations. Cette API est principalement conçue pour les applications de technologie d’assistance qui agrandissent les parties de l’écran afin de les rendre plus visibles.

MAPI est pris en charge sur Windows Vista, Windows 7, Windows Server 2008 et Windows Server 2008 R2. Elle est destinée aux développeurs qui connaissent bien les concepts de la programmation graphique.

Pour plus d’informations, consultez l' [API zoom](/previous-versions/windows/desktop/magapi/entry-magapi-sdk).

### <a name="resource-compiler"></a>compilateur de ressources

Le compilateur de ressources Microsoft Windows est un outil de développement d’applications utilisé pour ajouter une interface utilisateur et d’autres ressources à une application Windows. Une ressource est une donnée non exécutable utilisée par une application et qui comprend des boîtes de dialogue, des menus, des chaînes, des curseurs, des icônes, des bitmaps, etc. Le compilateur de ressources est inclus dans Microsoft Visual Studio et le SDK Windows.

Pour plus d’informations, consultez [Compilateur de ressources](../menurc/resource-compiler.md).

## <a name="user-interface-technologies-for-managed-applications"></a>Technologies d’interface utilisateur pour les applications managées

Cette section décrit les technologies Microsoft pour le développement d’interfaces utilisateur pour les applications Windows managées qui s’exécutent dans le contexte de la .NET Framework. Pour plus d’informations, consultez [développement .net](/previous-versions/ff361664(v=vs.100)).

### <a name="windows-forms"></a>Windows Forms

Windows Forms est une interface de programmation d’applications graphique permettant de créer des applications Windows managées basées sur le .NET Framework. Dans Windows Forms, un formulaire est une surface visuelle sur laquelle vous affichez des informations pour l’utilisateur, et par le biais duquel vous recevez une entrée de l’utilisateur.

Vous générez des applications Windows Forms en ajoutant des contrôles aux formulaires et en développant des réponses aux actions de l’utilisateur, telles que des clics de souris ou des frappes de touches. Un contrôle est un élément d’interface utilisateur discret qui affiche des données ou accepte l’entrée de données. Windows Forms contient divers contrôles que vous pouvez ajouter aux formulaires : des contrôles qui affichent des zones de texte, des boutons, des listes déroulantes, des cases d’option et même des pages web. Windows Forms prend également en charge la création de contrôles personnalisés.

Pour plus d’informations, consultez [Windows Forms](/previous-versions/dotnet/netframework-4.0/cc656767(v=vs.100)).

### <a name="windows-presentation-foundation"></a>Windows Presentation Foundation

Windows Presentation Foundation (WPF) est le successeur de [Windows Forms](/previous-versions/dotnet/netframework-4.0/cc656767(v=vs.100)). WPF est un système de présentation permettant de générer et de restituer des interfaces utilisateur dans des applications clientes Windows et des applications hébergées sur un navigateur. Le cœur de WPF est un moteur de rendu vectoriel et indépendant de toute résolution, créé pour tirer parti du matériel graphique moderne. WPF étend le cœur avec un ensemble complet de fonctionnalités de développement d’applications qui incluent XAML (Extensible Application Markup Language), des contrôles, la liaison de données, la disposition, les graphiques 2D et 3D, l’animation, les styles, les modèles, les documents, les médias, le texte et la typographie.

WPF étant inclus dans le .NET Framework, vous pouvez développer des applications qui incorporent d’autres éléments de la bibliothèque de classes .NET Framework. WPF est pris en charge sur Windows Vista, Windows 7, Windows Server 2008, Windows Server 2008 R2 et est également disponible pour Windows XP avec Service Pack 2 (SP2) et Windows Server 2003.

Pour plus d’informations, consultez [Windows Presentation Foundation](/dotnet/framework/wpf/).

### <a name="silverlight"></a>Silverlight

Microsoft Silverlight est une plate-forme de développement puissante permettant de créer des applications multimédias et des applications métier riches pour le Web, les ordinateurs de bureau et les appareils mobiles.

Sur la base du .NET Framework, le plug-in Silverlight gratuit fonctionne sur plusieurs navigateurs, appareils et systèmes d’exploitation pour apporter une nouvelle interactivité au Web. Avec de nombreuses options de mise en page et de style, des protocoles de communication puissants, un accès aux données fiable et une prise en charge de l’interaction utilisateur et des médias haute définition, Silverlight permet de créer des expériences client rapides, lisses et visuellement riches. Les applications Silverlight peuvent être développées rapidement avec la plateforme Web Microsoft, Visual Studio et expression Studio.

Pour plus d’informations, consultez [Microsoft Silverlight](/previous-versions/windows/silverlight/dotnet-windows-silverlight/cc838158(v=vs.95)).

### <a name="expression-blend-3--sketchflow"></a>Expression Blend 3 + SketchFlow

Expression Blend 3 + SketchFlow est un outil visuel permettant de concevoir, de créer des prototypes et de créer des interfaces utilisateur sophistiquées pour les applications de bureau et Web WPF et Silverlight. Vous générez une application en dessinant des formes, en dessinant des contrôles tels que des boutons et des zones de liste, en faisant en sorte que les parties de votre application répondent à des clics de souris et à d’autres entrées utilisateur, et tout en apportant un style à votre propre utilisateur.

Pour plus d’informations, consultez [prototypage avec SketchFlow](/previous-versions/visualstudio/design-tools/expression-studio-3/ee341458(v=expression.30)).

### <a name="ui-automation-for-managed-applications"></a>UI Automation pour les applications managées

UI Automation est une infrastructure d’accessibilité pour Windows, disponible sur tous les systèmes d’exploitation qui prennent en charge WPF.

UI Automation fournit un accès par programme à la plupart des éléments de l’interface utilisateur sur le bureau, ce qui permet aux produits de technologie d’assistance tels que les lecteurs d’écran de fournir aux utilisateurs finaux des informations sur l’interface utilisateur et de manipuler l’interface utilisateur par d’autres moyens que l’entrée standard. UI Automation permet également aux scripts de test automatisés d’interagir avec l’interface utilisateur.

Pour plus d’informations, consultez [UI Automation pour les applications managées](/dotnet/framework/ui-automation/).

 

 