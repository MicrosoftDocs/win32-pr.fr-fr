---
title: Vue d’ensemble des styles visuels
description: cette rubrique décrit les styles visuels et identifie les composants Windows qui les prennent en charge. Elle explique également les étapes à suivre pour utiliser les styles visuels dans vos applications.
ms.assetid: 5B5D7BB6-684F-478D-BF5F-B8D18BBCFF2E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 237ac858e1a60e615a6af177728102fb7e6ea1737a3a2d94d93091264b02121a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077721"
---
# <a name="visual-styles-overview"></a>Vue d’ensemble des styles visuels

cette rubrique décrit les styles visuels et identifie les composants Windows qui les prennent en charge. Elle explique également les étapes à suivre pour utiliser les styles visuels dans vos applications. Cette rubrique comporte les sections suivantes :

-   [Thèmes et styles visuels](#themes-and-visual-styles)
-   [Composants de styles visuels](#visual-styles-components)
-   [Spécifications de l’application pour la prise en charge des styles visuels](#application-requirements-for-supporting-visual-styles)
-   [Rubriques connexes](#related-topics)

## <a name="themes-and-visual-styles"></a>Thèmes et styles visuels

Windows propose plusieurs fonctionnalités qui permettent aux utilisateurs d’adapter l’interface utilisateur en fonction de leurs besoins individuels et de leurs préférences. Ces fonctionnalités incluent des thèmes, qui ont été introduits dans Microsoft plus ! pour Windows 95. Un thème est une collection de paramètres sélectionnables par l’utilisateur, qui comprend le papier peint, les curseurs, les polices, les sons et les icônes. Voici quelques caractéristiques des thèmes.

-   Les paramètres de thème sont spécifiés dans les fichiers. Theme qui ont un format similaire à win.ini fichiers.
-   Un éditeur de logiciels indépendant (ISV) peut créer et distribuer un fichier. Theme avec un produit.
-   dans les versions antérieures à Windows Vista, les fichiers de thème s’affichent sous l’onglet thème du panneau de configuration d’affichage. dans Windows Vista et versions ultérieures, les thèmes s’affichent dans le panneau de configuration personnalisation.

Pour plus d’informations sur les fichiers. Theme, consultez [format de fichier de thème](themesfileformat-overview.md).

un style visuel est une spécification qui définit l’apparence du Windows contrôles communs. Les styles visuels sont associés à des thèmes ; autrement dit, un fichier. Theme contient une section qui spécifie le style visuel à appliquer lorsque le thème particulier est actif. Voici quelques caractéristiques des styles visuels.

-   Les utilisateurs peuvent modifier le style visuel à tout moment en sélectionnant un autre thème.
-   Vous devez utiliser l’API des styles visuels pour appliquer le style visuel actuellement actif aux contrôles personnalisés ou owner-drawn de votre application, le cas échéant.
-   Les informations qui définissent un style visuel sont stockées dans un fichier. msstyles. Microsoft ne prend pas en charge la création de fichiers. msstyles.


l’illustration suivante montre une boîte de dialogue simple avec une barre des tâches, sur un bureau Windows 7 qui utilise le thème Windows Aero sans transparence. Étant donné que l’application n’est pas configurée pour utiliser les styles visuels, les boutons sont les mêmes, quels que soient les paramètres de thème.

![capture d’écran d’une boîte de dialogue avec des boutons qui n’utilisent pas la transparence](images/tb-wostyles.png)

En revanche, l’illustration suivante montre la même boîte de dialogue sur le même bureau, mais cette fois, l’application a été configurée pour fonctionner avec les styles visuels. Notez l’apparence différente des boutons dans la zone cliente. Les boutons s’affichent différemment, car le système a appliqué les styles visuels définis dans le thème Aero.

![capture d’écran d’une boîte de dialogue avec des boutons qui utilisent la transparence](images/tb-withstyles.png)

l’exemple suivant montre une boîte de dialogue similaire sur un bureau Windows 8. dans Windows 8, les styles visuels sont toujours activés, afin que les applications Windows 8 les obtiennent « gratuitement ».

![capture d’écran d’une boîte de dialogue simple sur le bureau Windows 8](images/tb-win8.png)

## <a name="visual-styles-components"></a>Composants de styles visuels

Les styles visuels sont pris en charge par les composants suivants :

-   Version 6 ou ultérieure de la bibliothèque de contrôles communs (ComCtl32.dll)
-   API des styles visuels implémentée dans UxTheme.dll
-   Service thèmes
-   Un ou plusieurs fichiers de définition de style visuel (. msstyles)

L’API des styles visuels dépend d’un service système appelé themes. la bibliothèque de contrôles communs interroge le service themes pour obtenir des informations relatives au style et, jusqu’à Windows 7, utilise le service pour restituer les contrôles dans le style visuel actuel.

dans Windows 8 et versions ultérieures, l’API des styles visuels fonctionne toujours si le service thèmes est désactivé. Cela signifie que les contrôles communs et la zone non cliente de Windows auront toujours des styles visuels lorsque le service thèmes est désactivé. les fonctionnalités Windows 8 qui requièrent toujours le service themes sont les suivantes :

-   modification du style visuel, en général via la page de **personnalisation** des **Paramètres de PC**.
-   Optimisations des performances impliquées dans le changement des utilisateurs, la déconnexion, l’arrêt et le partage entre les sessions utilisateur.

L’API des styles visuels obtient des informations de style à partir du fichier. msstyles associé au thème actuellement sélectionné. Le fichier. msstyles contient un ensemble de métriques, de polices, de couleurs et de bitmaps qui définissent un style visuel

## <a name="application-requirements-for-supporting-visual-styles"></a>Spécifications de l’application pour la prise en charge des styles visuels

Pour utiliser les styles visuels, votre application doit s’exécuter sur un système d’exploitation qui contient ComCtl32.dll version 6 ou ultérieure. Si vous souhaitez que votre application utilise ComCtl32.dll version 6, vous devez ajouter un manifeste d’application ou une directive de compilateur pour spécifier que la version 6 doit être utilisée si elle est disponible. Pour plus d’informations sur la création d’un manifeste d’application qui permet à votre application d’utiliser des styles visuels, consultez [activation de styles visuels](cookbook-overview.md).

Pour les contrôles communs, aucune action supplémentaire n’est nécessaire pour s’assurer que les contrôles sont affichés dans le style visuel préféré de l’utilisateur.

Si votre application contient des contrôles personnalisés ou owner-drawn, vous devez utiliser l’API des styles visuels pour récupérer des informations sur le style visuel actuellement actif et dessiner les contrôles dans ce style.

pour les versions Windows antérieures à Windows 8, les applications doivent généralement fournir deux chemins de code distincts pour dessiner des contrôles personnalisés et owner-drawn. un chemin d’accès de code dessine les contrôles lorsqu’un thème qui utilise des styles visuels est actif, et un autre chemin d’accès de code dessine les contrôles lorsque le thème Windows classique ou un thème à contraste élevé est actif. dans Windows 8, toutefois, les styles visuels sont toujours activés, donc les chemins de code séparés ne sont pas nécessaires. les Applications qui sont manifestes pour Windows 8 obtiennent un contraste élevé « gratuit ». Pour plus d’informations, consultez [prise en charge des thèmes de contraste élevé](supporting-high-contrast-themes.md).

Pour plus d’informations sur, consultez [utilisation de styles visuels avec des contrôles personnalisés et Owner-Drawn](using-visual-styles.md) et [référence des styles visuels](uxctl-ref.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Styles visuels](themes-overview.md)
</dt> </dl>

 

 




