---
title: Windows Bibliothèque de contrôles de Framework du ruban
description: les rubriques contenues dans cette section décrivent l’ensemble des contrôles inclus avec l’infrastructure de ruban Windows. Les contrôles répertoriés ici sont les objets d’interface utilisateur d’un ruban qui exposent les fonctionnalités de commande.
ms.assetid: bda13e51-7e5f-4600-a6bd-9388bffd6ce2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 065d69e52cee2300041eedd2d440d292a73e1dc46f5084545effc5e470bceee4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119933349"
---
# <a name="windows-ribbon-framework-control-library"></a>Windows Bibliothèque de contrôles de Framework du ruban

les rubriques contenues dans cette section décrivent l’ensemble des contrôles inclus avec l’infrastructure de ruban Windows. Les contrôles répertoriés ici sont les objets d’interface utilisateur d’un ruban qui exposent les fonctionnalités de commande.

-   [Introduction](#introduction)
-   [Les contrôles](#windows-ribbon-framework-control-library)
    -   [Contrôles de base](#basic-controls)
    -   [Contrôles de conteneur](#container-controls)
    -   [Contrôles spécialisés](#specialized-controls)
-   [Rubriques connexes](#related-topics)

## <a name="introduction"></a>Introduction

L’infrastructure du ruban est composée de composants tels que les [onglets](windowsribbon-controls-tab.md) et la [barre d’outils accès rapide](windowsribbon-controls-quickaccesstoolbar.md), qui fonctionnent ensemble pour offrir une expérience d’interface utilisateur riche. Individuellement, ces composants exposent différents types de commandes pour offrir aux clients une expérience organisée et prévisible sur les applications du ruban. Par exemple, chaque onglet expose des commandes relatives à la création et à l’action sur des parties spécifiques du contenu dans l’espace de travail de l’application, tandis que le menu de l' [application](windowsribbon-controls-applicationmenu.md) expose les fonctionnalités associées à un projet complet, tel qu’un document, une image ou un film entier.

Cette rubrique fournit une liste complète des contrôles du ruban et inclut une brève description de chaque contrôle, avec des liens vers une documentation plus détaillée, le cas échéant.

## <a name="the-controls"></a>Les contrôles

L’infrastructure du ruban est composée de deux [vues](windowsribbon-reference-elements-view.md): la vue du [**ruban**](windowsribbon-element-ribbon.md) et la vue [**ContextPopup**](windowsribbon-element-contextpopup.md) . Chaque vue peut héberger plusieurs composants qui jouent le rôle de conteneurs de présentation pour tous les contrôles rendus et gérés par l’infrastructure.

La vue [**du ruban**](windowsribbon-element-ribbon.md) héberge l’élément [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) , l’élément [**QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar.md) et la barre de commandes du ruban tandis que la vue [**ContextPopup**](windowsribbon-element-contextpopup.md) héberge un élément [**ContextMenu**](windowsribbon-element-contextmenu.md) , un élément [**MiniToolbar**](windowsribbon-element-minitoolbar.md) , ou les deux.

Chaque contrôle d’infrastructure est distingué par la fonctionnalité associée à son [**type de commande**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype).

### <a name="basic-controls"></a>Contrôles de base

Les contrôles de base se composent d’un ou de plusieurs boutons qui peuvent être appelés par un clic de souris unique pour effectuer une action simple.

> [!Note]  
> Le [**compteur**](windowsribbon-element-spinner.md) est une exception, car il contient un contrôle d’édition.

 

Le tableau suivant répertorie les contrôles de base dans l’infrastructure du ruban.



| Contrôler                                                  | Élément de balisage                                             |
|----------------------------------------------------------|------------------------------------------------------------|
| [Button](windowsribbon-controls-button.md)              | [**Bouton**](windowsribbon-element-button.md)             |
| [Case à cocher](windowsribbon-controls-checkbox.md)         | [**Activé**](windowsribbon-element-checkbox.md)         |
| [Bouton aide](windowsribbon-controls-helpbutton.md)     | [**HelpButton**](windowsribbon-element-helpbutton.md)     |
| [Spinner](windowsribbon-controls-spinner.md)            | [**Spinner**](windowsribbon-element-spinner.md)           |
| [Bouton bascule](windowsribbon-controls-togglebutton.md) | [**ToggleButton**](windowsribbon-element-togglebutton.md) |



 

### <a name="container-controls"></a>Contrôles de conteneur

Les contrôles conteneurs sont composés de groupes de contrôles, de menus, de listes ou d’éléments et de collections de commandes.

Le Framework distingue deux types de conteneurs, statiques et dynamiques.

### <a name="static-containers"></a>Conteneurs statiques

Les conteneurs statiques sont déclarés et remplis, ainsi que toutes les ressources associées, dans le fichier de balisage du ruban. Ces contrôles ne peuvent pas être modifiés au moment de l’exécution.

Les avantages des contrôles statiques sont les suivants :

-   Prototypage rapide. Les contrôles statiques permettent de créer rapidement un simulacre de ruban ressemblant à une conception de ruban finale qui ne requiert pas de code compliqué.
-   Modifications simples. La plupart des éléments, des attributs, des ressources et des mises en page de contrôles statiques peuvent être modifiés dans le balisage.
-   Interface utilisateur cohérente. Les applications bien conçues fournissent une interface utilisateur cohérente et stable qui évite les modifications des menus et des listes au moment de l’exécution.

Le tableau suivant décrit les contrôles de conteneur statiques dans l’infrastructure du ruban.



| Contrôler                                                        | Élément de balisage                                                   |
|----------------------------------------------------------------|------------------------------------------------------------------|
| [Menu de l’application](windowsribbon-controls-applicationmenu.md) | [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) |
| [Menu contextuel contexte](windowsribbon-controls-contextpopup.md)       | [**ContextPopup**](windowsribbon-element-contextpopup.md)       |
| [Bouton déroulant](windowsribbon-controls-dropdownbutton.md)  | [**DropDownButton**](windowsribbon-element-dropdownbutton.md)   |
| [Groupe](windowsribbon-controls-group.md)                      | [**Groupe**](windowsribbon-element-group.md)                     |
| [Groupe de menus](windowsribbon-controls-menugroup.md)             | [**MenuGroup**](windowsribbon-element-menugroup.md)             |
| [Bouton partagé](windowsribbon-controls-splitbutton.md)         | [**SplitButton**](windowsribbon-element-splitbutton.md)         |
| [Tab](windowsribbon-controls-tab.md)                          | [**Onglet**](windowsribbon-element-tab.md)                         |
| [Groupe d’onglets](windowsribbon-controls-tabgroup.md)               | [**TabGroup**](windowsribbon-element-tabgroup.md)               |



 

### <a name="dynamic-containers"></a>Conteneurs dynamiques

Les conteneurs dynamiques sont déclarés dans le fichier de balisage du ruban. Ils présentent un groupe d’éléments ou de commandes qui sont créés ou modifiés au moment de l’exécution.

Une sous-classe de conteneurs dynamiques, appelée galeries, se distingue par leur implémentation de l’interface [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) . Cette interface permet à un contrôle d’exposer son élément ou sa liste de commandes sous la forme d’une collection, et de prendre en charge les mises à jour en fonction des conditions d’interaction et d’exécution de l’utilisateur. Pour plus d’informations, consultez [utilisation des galeries](ribbon-controls-galleries.md).

Le tableau suivant répertorie les contrôles de conteneur dynamiques dans l’infrastructure du ruban.



| Contrôler                                                               | Élément de balisage                                                         |
|-----------------------------------------------------------------------|------------------------------------------------------------------------|
| [Zone de liste déroulante](windowsribbon-controls-combobox.md)                      | [**ComboBox**](windowsribbon-element-combobox.md)                     |
| [Galerie déroulante](windowsribbon-controls-dropdowngallery.md)       | [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)       |
| [Galerie dans le ruban](windowsribbon-controls-inribbongallery.md)       | [**InRibbonGallery**](windowsribbon-element-inribbongallery.md)       |
| [Barre d’outils accès rapide](windowsribbon-controls-quickaccesstoolbar.md) | [**QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar.md) |
| [Éléments récents](windowsribbon-controls-recentitems.md)                | [**RecentItems**](windowsribbon-element-recentitems.md)               |
| [Galerie de boutons partagés](windowsribbon-controls-splitbuttongallery.md) | [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) |



 

### <a name="specialized-controls"></a>Contrôles spécialisés

L’infrastructure du ruban contient un certain nombre de contrôles spécialisés pour des fonctionnalités d’interface utilisateur spécifiques.

Le tableau suivant répertorie les contrôles spécialisés dans l’infrastructure du ruban.



| Contrôler                                                                  | Élément de balisage                                                           |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Sélecteur de couleurs déroulantes](windowsribbon-controls-dropdowncolorpicker.md) | [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) |
| [Contrôle de police](windowsribbon-controls-fontcontrol.md)                   | [**FontControl**](windowsribbon-element-fontcontrol.md)                 |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fonctionnement des commandes et des contrôles](windowsribbon-commandscontrols.md)
</dt> </dl>

 

 