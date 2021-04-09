---
title: Mode de contraste élevé
description: Mode de contraste élevé
ms.assetid: 817F2BBD-3744-4D34-927F-EBF9F7894CC0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae8c53d3e92bb97dd9e2f5fa34bad9f901920cc7
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "103730741"
---
# <a name="high-contrast-mode"></a>Mode de contraste élevé

## <a name="platforms"></a>Plateformes

 **Clients** -Windows 8  
**Serveurs** -Windows Server 2012  



## <a name="description"></a>Description

Dans les systèmes d’exploitation Windows précédents, le mode de contraste élevé était limité aux thèmes s’exécutant sous les thèmes classiques, qui n’étaient pas visuellement stylisés. Dans Windows 8 et Windows Server 2012, le mode classique a été supprimé et remplacé par des thèmes visuellement à contraste élevé. L’un des principaux avantages de ce changement est la suppression d’un chemin de code distinct pour les applications qui s’exécutent en mode classique.

Les développeurs doivent toujours être sensibilisés à la façon dont le mode de contraste élevé peut affecter leur application et comment développer une application qui est véritablement indépendante du style. Cela est important, car bien que l’utilisation incorrecte ou la supposition des couleurs de thème puisse entraîner un comportement correct des applications sous un style visuel tel que Aero, ces mêmes applications répondent de manière incorrecte sous un contraste élevé. Par exemple, dans Aero, le texte est toujours noir et la couleur de surbrillance est un bleu clair. Toutefois, dans le contraste noir élevé, la couleur de surbrillance est noire. Si vous partez du texte noir, comme c’était le cas dans de nombreuses applications de la zone antérieures à Windows 8 et que vous utilisez la valeur système par défaut pour la mise en surbrillance, l’utilisateur verra du texte noir sur un arrière-plan noir. Dans ces situations, il est nécessaire de comprendre comment utiliser correctement les thèmes et les métriques du système pour que l’application semble correcte entre les styles.

## <a name="manifestations"></a>Manifestations

-   Ils ne sont pas activés dans la zone cliente des applications qui ne contiennent pas de <supportedOS> balise Windows 8 dans leur manifeste d’application. Par conséquent, les applications doivent restituer la zone cliente à l’aide du chemin de code requis pour le rendu en mode de contraste élevé du thème classique.
-   Ils ne sont pas activés dans les zones non clientes et clientes des applications dans des thèmes à contraste élevé. Elle n’est pas non plus activée dans les applications qui ne contiennent pas de <supportedOS> balise Windows 8 dans leur manifeste d’application et qui dessinent dans la zone non cliente d’une fenêtre à l’aide de l’API DwnIsCompositionEnabled (). L’application entière effectue le rendu dans le mode de contraste élevé du thème classique.
-   Les applications qui ajoutent la prise en charge de Windows 8 dans leur manifeste, mais n’utilisent pas de styles visuels pour le rendu, autrement dit, ils encodés en dur des couleurs ou des images dans leurs applications, risquent de ne pas s’afficher correctement dans les thèmes à contraste élevé. Le texte peut être difficile à lire ou les images ne s’affichent pas comme elles le devraient en mode de contraste élevé.

## <a name="mitigation"></a>Limitation des risques

Les couleurs de texte dans les thèmes à contraste élevé ont été créées pour être conformes aux instructions d’accessibilité de Microsoft. Nous maintenons un ratio de contraste élevé de 14:1 entre le premier plan et l’arrière-plan. Si les couleurs qui sont activées par défaut ne conviennent pas à un utilisateur final particulier, elles peuvent être facilement personnalisées par le biais des paramètres du panneau de configuration pour « couleur de la fenêtre » dans ces thèmes à contraste élevé.

Ces composants de l’interface utilisateur sont personnalisables dans les thèmes à contraste élevé :

-   Couleur d’arrière-plan de la fenêtre
-   Couleur du texte
-   Couleur des liens hypertexte
-   Texte désactivé
-   Couleurs de premier plan et d’arrière-plan du texte sélectionné
-   Couleurs de premier plan et d’arrière-plan du titre de la fenêtre active
-   Couleurs de premier plan et d’arrière-plan des titres de fenêtre inactives
-   Couleurs de premier plan et d’arrière-plan du bouton

## <a name="solution"></a>Solution

Si un comportement inattendu est observé dans les applications dans les thèmes à contraste élevé, l’une de ces solutions peut vous aider à :

-   **Manifeste d’une application pour Windows 8 :**

    Les zones clientes des applications qui ne contiennent pas la <supportedOS> balise Windows 8 dans le manifeste de l’application sont rendues sans thème. Les applications intégrées doivent toutes contenir cette entrée dans le manifeste de l’application. Ajoutez la valeur GUID 4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38 pour Windows 8.

-   **Utilisation de styles visuels avec des interfaces utilisateur owner-drawn :**

    Les contrôles owner-drawn doivent suivre les instructions sur [MSDN](/windows/desktop/Controls/using-visual-styles) pour restituer correctement les parties et les États de contrôle, y compris le texte. Les développeurs ne doivent pas compter sur la couleur de texte ou d’arrière-plan spécifiée dans un contexte de périphérique afin d’utiliser des méthodes non UxTheme pour le rendu. Dans le cas où il n’y a pas de partie de thème pour le contrôle en question, utilisez GetThemeSysColor avec la [mesure appropriée](/windows/desktop/api/winuser/nf-winuser-getsyscolor) et dessinez le texte à l’aide de méthodes GDI standard. Si aucun des appels UxTheme n’est approprié, utilisez la méthode GetSysColor pour accéder à la mesure appropriée.

-   **Sélection de la couleur du texte :**

    N’utilisez pas de couleur de texte codée en dur, même s’il est supposé s’adapter à tous les scénarios courants. Les thèmes d’expédition sont créés de façon à prendre en charge la haute visibilité avec les mesures associées. Par exemple, \_ la couleur HIGHLIGHTTEXT est destinée à être utilisée avec \_ la mise en surbrillance des couleurs comme un arrière-plan et un WINDOWTEXT de couleur \_ est destiné à être utilisé avec \_ la fenêtre de couleur comme arrière-plan. S’il existe des exceptions à ces associations, utilisez-les dans les parties de thème et les définitions d’État elles-mêmes et non dans le code. Lors de la conception d’interfaces utilisateur à contraste élevé, il est essentiel que l’interface utilisateur soit indépendante du thème à contraste élevé actuellement appliqué, car les utilisateurs à contraste élevé peuvent personnaliser leurs couleurs.

-   **Réponse à l' \_ événement WM ThemeChange :**

    Si votre application met en cache les couleurs récupérées à partir du thème ou applique des couleurs de manière non standard, ajoutez un gestionnaire de messages pour WM \_ THEMECHANGE qui recalcule les valeurs de couleur stockées et repeint l’interface utilisateur.

-   **Écriture d’une application WWA à contraste élevé :**

    Les applications Web n’ont pas accès aux API UxTheme, mais doivent toujours être écrites avec les métriques système actuelles comme base pour l’interface utilisateur. Les développeurs WWA peuvent tirer parti de quelques ressources pour garantir une application conforme à un contraste élevé :

    -   La [spécification de couleur CSS du W3C](https://www.w3.org/TR/css3-color/) spécifie la syntaxe d’utilisation des métriques système plutôt que des couleurs spécifiques
    -   La prise en charge des requêtes de média à contraste élevé est ajoutée à Internet Explorer 10
    -   WWAs peut tirer parti de la méthode IAccessibilityCapabilities :: d'-obtient le \_ contraste () pour vérifier l’état du contraste élevé

    Les applications du Windows Store n’ont pas beaucoup de problèmes avec les parties de thème présentes dans les applications Windows classiques, mais vous devez toujours garantir une conformité à contraste élevé. Par défaut, Internet Explorer ignore certains styles définis par l’utilisateur et les remplace par des valeurs conformes à un contraste élevé. Par exemple, les propriétés CSS d’image d’arrière-plan, d’arrière-plan et de couleur sont ignorées.

    Si vous ne souhaitez pas qu’Internet Explorer ignore les propriétés que vous avez définies et que vous vous êtes assuré que l’interface utilisateur est conforme à un contraste élevé, vous pouvez définir la nouvelle propriété CSS m3 – MS-contraste élevé : OFF sur un élément parent.

-   **Écriture d’une application du Windows Store à contraste élevé :**

    L’application du Windows Store doit utiliser la classe [SystemColors](/dotnet/api/system.windows.systemcolors) pour déterminer les couleurs appropriées des éléments d’interface utilisateur, en gardant à l’esprit que certaines couleurs de mesure système sont conçues pour être utilisées conjointement, par exemple SystemColors. WindowColor et SystemColors. WindowTextColor. Vous bénéficiez ainsi d’une expérience de contraste élevée supérieure.

-   **Détection correcte du contraste élevé dans les versions précédentes de Windows :**

    Les applications qui s’exécutent sur des versions antérieures de Windows n’ont pas accès aux nouveaux thèmes à contraste élevé, même si le manifeste spécifie la compatibilité avec la version de Windows en question. Par conséquent, il peut être nécessaire d’insérer des chemins de code supplémentaires pour gérer le rendu dans l’environnement classique utilisé dans les versions précédentes de Windows. Dans ce cas, la présence d’un contraste élevé doit être vérifiée en appelant la fonction [SystemParametersInfo](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) avec l' \_ indicateur SPI GETHIGHCONTRAST. Il s’agit de la seule méthode prise en charge pour vérifier la présence d’un contraste élevé.

## <a name="tests"></a>Tests

Lors du test d’une application, assurez-vous qu’elle s’affiche correctement dans tous les thèmes fournis par Windows 8 : Aero, Basic, contraste élevé 1, contraste élevé 2, contraste élevé Black et contraste élevé White. Assurez-vous que le texte est clairement visible et facile à lire dans les thèmes à contraste élevé.

## <a name="resources"></a>Ressources

-   [Classes de style Aero, parties et États](../controls/aero-style-classes-parts-and-states.md) (le nouveau thème de base et les thèmes à contraste élevé utilisent également ces États)
-   [Parties et États communs à tous les styles visuels](../controls/parts-and-states.md)
-   [Utilisation de styles visuels avec des contrôles personnalisés et Owner-Drawn](../controls/using-visual-styles.md)
-   [GetSysColor, fonction](/windows/win32/api/winuser/nf-winuser-getsyscolor)
-   [W3C-module de couleur CSS-niveau 3](https://www.w3.org/TR/css3-color/)
-   [SystemColors (classe)](/dotnet/api/system.windows.systemcolors?view=netcore-3.1)
-   [SystemParametersInfo, fonction](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
-   [Accessibilité Microsoft](https://www.microsoft.com/enable/)

 

 