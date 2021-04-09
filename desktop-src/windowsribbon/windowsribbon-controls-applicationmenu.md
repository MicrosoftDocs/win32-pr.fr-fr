---
title: Menu de l’application
description: Le menu application est le menu principal d’une application qui implémente l’infrastructure de ruban Windows.
ms.assetid: 5be93a5b-277b-44c1-be24-a0598a140bfc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e99f57045daa35149e5fa074cb59e2f538c589b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842309"
---
# <a name="application-menu"></a>Menu de l’application

Le menu application est le menu principal d’une application qui implémente l’infrastructure de ruban Windows.

-   [Introduction](#introduction)
-   [Composants du menu de l’application](#components-of-the-application-menu)
    -   [Menu de l’application MenuGroup](#application-menu-menugroup)
-   [Dimensionnement du menu de l’application](#sizing-the-application-menu)
-   [Propriétés du menu de l’application](#application-menu-properties)
-   [Rubriques connexes](#related-topics)

## <a name="introduction"></a>Introduction

Le menu application se compose d’un contrôle de bouton déroulant qui affiche un menu contenant les commandes qui exposent les fonctionnalités liées à un projet complet, telles que l’intégralité d’un document, d’une image ou d’un film. Les exemples incluent les commandes **nouveau**, **ouvrir**, **Enregistrer** et **quitter** .

La capture d’écran suivante illustre le menu de l’application.

![capture d’écran du menu de l’application et de la liste des éléments récents du ruban Paint pour Windows 7.](images/controls/recentitems.png)

## <a name="components-of-the-application-menu"></a>Composants du menu de l’application

Le menu application est un élément obligatoire dans une application de ruban. Le point d’entrée dans le menu de l’application est un bouton distinctif qui apparaît en tant que premier élément de la ligne d' [onglet](windowsribbon-controls-tab.md) , comme illustré dans la capture d’écran suivante.

> [!Note]  
> Windows 8 et versions ultérieures : l’image du bouton de menu de l’application a été changée en étiquette : **fichier**. Nous vous recommandons de ne pas utiliser de fichier comme étiquette pour vos propres onglets.

 

![capture d’écran du bouton de menu de l’application de WordPad pour Windows 7.](images/overviews/applicationmenu-button.png)

Lorsque vous cliquez dessus, ce bouton affiche le menu détaillé qui s’affiche dans la capture d’écran suivante (le menu de l’application de WordPad pour Windows 7).

![capture d’écran du menu de l’application dans WordPad pour Windows 7.](images/overviews/applicationmenu-menu.png)

> [!Note]  
> Il n’y a aucun impact sur le jeu d’onglets lorsque l’utilisateur clique sur le bouton de menu de l’application ; au lieu de cela, le focus entre dans le menu.

 

Le menu application contient deux volets : une liste de commandes représentées par un ou plusieurs éléments [**MenuGroup**](windowsribbon-element-menugroup.md) et une liste d' [éléments récents](windowsribbon-controls-recentitems.md) représentée par un élément [**ApplicationMenu. RecentItems**](windowsribbon-element-applicationmenu-recentitems.md) .

### <a name="application-menu-menugroup"></a>Menu de l’application MenuGroup

L’élément [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) doit contenir au moins un élément enfant [**MenuGroup**](windowsribbon-element-menugroup.md) qui expose une liste de commandes au niveau de l’application. Si plusieurs éléments **MenuGroup** sont déclarés, une ligne de séparation est dessinée entre les groupes, comme illustré dans la capture d’écran suivante.

![capture d’écran d’un menu d’application MenuGroup.](images/overviews/applicationmenu-menugroup.png)

Voici une liste de contraintes pour un élément [**MenuGroup**](windowsribbon-element-menugroup.md) d’un menu d’application :

-   Tous les éléments [**MenuGroup**](windowsribbon-element-menugroup.md) doivent être déclarés avec une valeur d’attribut de *classe* de `MajorItems` .
-   Un menu d’application  [**MenuGroup**](windowsribbon-element-menugroup.md) prend uniquement en charge le [bouton](windowsribbon-controls-button.md), le [bouton bascule](windowsribbon-controls-togglebutton.md), le [bouton déroulant](windowsribbon-controls-dropdownbutton.md), le bouton [partagé](windowsribbon-controls-splitbutton.md), [la Galerie](windowsribbon-controls-dropdowngallery.md)déroulante et les contrôles de la [Galerie de boutons partagés](windowsribbon-controls-splitbuttongallery.md) .
    > \[! Précieuse\]  
    > Les galeries de commandes sont le seul type de Galerie pris en charge dans le menu de l’application. Pour plus d’informations sur les contrôles de la Galerie, consultez [utilisation des galeries](./ribbon-controls-galleries.md).

     

Quand un [bouton](windowsribbon-controls-button.md) ou un [bouton bascule](windowsribbon-controls-togglebutton.md) est utilisé dans un [**MenuGroup**](windowsribbon-element-menugroup.md), la valeur de [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) est affichée dans le menu et les valeurs de [**Command. TooltipTitle**](windowsribbon-element-command-tooltiptitle.md) et [**Command. TooltipDescription**](windowsribbon-element-command-tooltipdescription.md) sont affichées comme info-bulle, comme illustré dans la capture d’écran suivante.

![capture d’écran d’un contrôle bouton dans un menu d’application.](images/overviews/applicationmenu-menubutton.png)

Quand un [bouton](windowsribbon-controls-dropdownbutton.md)déroulant, un [bouton partagé](windowsribbon-controls-splitbutton.md), [une galerie](windowsribbon-controls-dropdowngallery.md)déroulante ou une [bibliothèque de boutons partagés](windowsribbon-controls-splitbuttongallery.md) est utilisé dans le menu de l’application, la partie de menu s’affiche sous la forme d’un menu volant qui couvre et masque le volet **éléments récents** .

Pour les contrôles bouton [partagé](windowsribbon-controls-splitbutton.md) et [bouton déroulant](windowsribbon-controls-dropdownbutton.md) , la valeur de [**Command. LabelDescription**](windowsribbon-element-command-labeldescription.md) est présentée en ligne dans le menu contextuel pour aider les utilisateurs à découvrir la fonctionnalité de commande. La valeur affichée de **Command. LabelDescription** est divisée par programmation sur une étendue de deux lignes, et une tentative est effectuée pour ajuster la valeur exactement au volet des **éléments récents** sous. Si la valeur **Command. LabelDescription** n’est pas adaptée, le menu volant se développe pour s’adapter à la valeur [**Command. Comment**](windowsribbon-element-command-comment.md) la plus longue dans le [**MenuGroup**](windowsribbon-element-menugroup.md).

La capture d’écran suivante illustre ces comportements dans un menu volant de [bouton partagé](windowsribbon-controls-splitbutton.md) .

![capture d’écran d’un menu volant de contrôle de liste dans un menu d’application.](images/overviews/applicationmenu-menuflyout.png)

Avec une [Galerie déroulante](windowsribbon-controls-dropdowngallery.md) et une [Galerie de boutons partagés](windowsribbon-controls-splitbuttongallery.md), seule une étiquette et une image sont affichées.

## <a name="sizing-the-application-menu"></a>Dimensionnement du menu de l’application

Le dimensionnement du menu de l’application est géré par l’infrastructure du ruban. Si des chaînes très longues sont fournies pour la valeur de [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) ou [**Command. LabelDescription**](windowsribbon-element-command-labeldescription.md), ou si une longue liste de commandes est utilisée, le menu ajuste sa taille pour s’adapter au contenu. Certaines formes d’ajustement incluent l’augmentation de la taille des menus volants ou des volets de menu, ainsi que l’ajout de visionneuses panoramiques lorsque le défilement est requis.

## <a name="application-menu-properties"></a>Propriétés du menu de l’application

L’infrastructure du ruban définit une collection de [clés de propriété](windowsribbon-reference-properties.md) pour le contrôle de menu de l’application.

En général, une propriété de menu de l’application est mise à jour dans l’interface ruban en invalidant la commande associée au contrôle via un appel à la méthode [**IUIFramework :: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . L’événement d’invalidation est géré et les mises à jour de propriété sont définies par la méthode de rappel [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

La méthode de rappel [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) n’est pas exécutée et l’application n’est pas interrogée pour obtenir une valeur de propriété mise à jour tant que la propriété n’est pas requise par le Framework. Par exemple, l’infrastructure requiert la propriété lorsqu’un onglet est activé et qu’un contrôle est affiché dans l’interface ruban, ou lorsqu’une info-bulle est affichée.



| Clé de propriété                                                                                     | Notes                                     |
|--------------------------------------------------------------------------------------------------|-------------------------------------------|
| [IU \_ \_ TooltipDescription](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | Peut uniquement être mis à jour par le biais d’une invalidation. |
| [IU \_ \_ TooltipTitle](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | Peut uniquement être mis à jour par le biais d’une invalidation. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Bibliothèque de contrôles de l’infrastructure du ruban Windows](windowsribbon-controls-entry.md)
</dt> <dt>

[**Élément de balisage ApplicationMenu**](windowsribbon-element-applicationmenu.md)
</dt> </dl>

 

 