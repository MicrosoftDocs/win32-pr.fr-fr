---
title: Déclaration des commandes et des contrôles avec le balisage du ruban
description: l’infrastructure de ruban Windows utilise un langage de balisage basé sur Extensible Application Markup Language (XAML) pour implémenter de manière déclarative l’apparence d’une Application de ruban.
ms.assetid: 76bacfb3-ecaf-47b3-be97-afa5e7e52330
keywords:
- Windows Ruban, structure de balisage
- Ruban, structure de balisage
- Windows Ruban, séparation de la présentation de la logique de commande
- Ruban, séparation de la présentation de la logique de commande
- Windows Ruban, composants
- Ruban, composants
- système de commandes pour Windows ruban
- contrôles pour Windows ruban
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20ae6c8d62012fac240c6d044c688295d89d8d5899e3673a3b914d8d142111d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118201321"
---
# <a name="declaring-commands-and-controls-with-ribbon-markup"></a>Déclaration des commandes et des contrôles avec le balisage du ruban

l’infrastructure de ruban Windows utilise un langage de balisage basé sur Extensible Application Markup Language (XAML) pour implémenter de manière déclarative l’apparence d’une Application de ruban.

-   [Séparation de la présentation de la logique de commande](#separating-presentation-from-command-logic)
-   [Structure de balisage](#markup-structure)
-   [Composants du ruban](#ribbon-components)
-   [Rubriques connexes](#related-topics)

## <a name="separating-presentation-from-command-logic"></a>Séparation de la présentation de la logique de commande

La séparation des attributs de présentation et visuels de la logique de commande dans l’infrastructure du ruban s’effectue via deux plateformes de développement distinctes, mais dépendantes. Les dispositions de contrôle, les comportements de mise à l’échelle, les déclarations de commande et les spécifications de ressources sont le domaine au moment de la conception d’une syntaxe de balisage déclarative basée sur la spécification [Extensible Application Markup Language (XAML)](/dotnet/framework/wpf/advanced/xaml-in-wpf) . Les fonctionnalités de bas niveau, les crochets d’application et les gestionnaires de commandes sont définis dans les implémentations d’interface basées sur le modèle COM (Component Object Model).

Cette séparation de la présentation et de la logique offre les avantages suivants :

-   Un cycle de développement d’applications plus efficace qui permet aux développeurs d’interface utilisateur et aux concepteurs d’implémenter l’interface graphique utilisateur de l’application ruban indépendamment de la fonctionnalité d’application principale. Cette fonctionnalité principale peut être laissée aux développeurs de logiciels dédiés.
-   Maintenance moins coûteuse, car les modifications apportées à l’interface graphique sont possibles sans modification des fonctionnalités principales (et inversement).
-   Spécification simple de ressources de type chaîne et image par le biais du balisage.
-   Facilité de prototypage.

## <a name="markup-structure"></a>Structure de balisage

Deux branches distinctes existent dans la structure du balisage de l’infrastructure du ruban.

La première branche contient un manifeste de déclarations de commande et de ressource (chaînes et images). Chaque entrée de commande est utilisée par l’infrastructure pour lier un contrôle de ruban, via un ID de commande, à un gestionnaire de commandes défini dans le code de l’application.

La deuxième branche contient les déclarations de contrôle réelles. Chaque contrôle est associé à une commande via un attribut *CommandName* qui correspond à un attribut *Name* spécifié dans chaque déclaration de commande.

## <a name="ribbon-components"></a>Composants du ruban

Les fonctionnalités de l’interface utilisateur de l’infrastructure du ruban sont exposées par le biais de [vues](windowsribbon-reference-elements-view.md). Une vue est essentiellement un conteneur, tel que le [**ruban**](windowsribbon-element-ribbon.md) et [**ContextPopup**](windowsribbon-element-contextpopup.md), qui est utilisé pour présenter des contrôles d’infrastructure et les commandes auxquelles elles sont liées.

La vue du [**ruban**](windowsribbon-element-ribbon.md) est composée de plusieurs composants qui incluent un [menu d’application](windowsribbon-controls-applicationmenu.md), la [barre d’outils accès rapide (qat)](windowsribbon-controls-quickaccesstoolbar.md) pour l’affichage des commandes couramment utilisées à partir de l’interface ruban, des [onglets](windowsribbon-controls-tab.md) principaux et contextuels qui contiennent des [groupes](windowsribbon-controls-group.md) de contrôles et le riche système de menu contextuel du [**ContextPopup**](windowsribbon-element-contextpopup.md).

Tous les composants de ruban sont déclarés dans un fichier de balisage autonome qui :

-   Spécifie les propriétés de base pour chaque élément.
-   Affiche clairement les relations hiérarchiques.
-   Fournit des préférences de disposition et des indicateurs de mise à l’échelle. Pour plus d’informations sur les modèles de disposition de l’infrastructure du ruban, consultez [Personnalisation d’un ruban à l’aide de définitions de taille et de stratégies de mise à l’échelle](windowsribbon-templates.md).
-   Fournit un moyen de définir des ressources telles que des images et des étiquettes. Pour plus d’informations sur les ressources d’image, consultez [spécification des ressources d’image de ruban](windowsribbon-imageformats.md).

Les deux exemples de balisage de ruban suivants montrent comment un ensemble d’éléments de menu d’application de ruban est associé à un nom de commande et à un ID.

1.  Cette section présente les déclarations de commande requises pour un menu d’application avec des commandes de base telles que nouveau, ouvrir et enregistrer.
    ```XML
    <!-- Command declarations for the Application Menu. -->
    <Command Name="cmdFileMenu"
             Symbol="ID_FILE_MENU"
             Id="25000" />
    <!-- Command declaration for most recently used items. -->
    <Command Name="cmdMRUItems"
             Symbol="ID_FILE_MRUITEMS"
             Id="25050"/>
    <!-- Command declarations for Application Menu items. -->
    <Command Name="cmdNew"
             Symbol="ID_FILE_NEW"
             Comment="New"
             Id="25001"
             LabelTitle="&amp;New"/>
    <Command Name="cmdOpen"
             Symbol="ID_FILE_OPEN"
             Comment="Open"
             Id="25002"
             LabelTitle="&amp;&amp;Open"/>
    <Command>
      <Command.Name>cmdSave</Command.Name>
      <Command.Symbol>ID_FILE_SAVE</Command.Symbol>
      <Command.Comment>Save</Command.Comment>
      <Command.Id>25003</Command.Id>
      <Command.LabelTitle>
        <String>
          <String.Content>Label for Save</String.Content>
          <String.Id>59999</String.Id>
          <String.Symbol>strSave</String.Symbol>
        </String>
      </Command.LabelTitle>
      <Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
      <Command.TooltipDescription>Tooltip description for Save Command.</Command.TooltipDescription>
      <Command.Keytip>s1</Command.Keytip>
    </Command>
    <Command Name="cmdPrint"
             Symbol="ID_FILE_PRINT"
             Comment="Save"
             Id="25004"
             LabelTitle="Print" />
    <Command Name="cmdExit"
             Symbol="ID_FILE_EXIT"
             Comment="Exit"
             Id="25005"
             LabelTitle="Exit" />
    ```

    

2.  Cette section présente les déclarations de contrôle associées.
    ```XML
    <!-- Control declarations for Application Menu items. -->
    <Ribbon.ApplicationMenu>
      <ApplicationMenu CommandName="cmdFileMenu">
        <!-- Most recently used items collection. -->
        <ApplicationMenu.RecentItems>
          <RecentItems CommandName="cmdMRUItems"/>
        </ApplicationMenu.RecentItems>
        <!-- Menu items collection. -->
        <MenuGroup>
          <Button CommandName="cmdNew" />
          <Button CommandName="cmdOpen" />
          <Button CommandName="cmdSave" />
        </MenuGroup>
        <MenuGroup>
          <Button CommandName="cmdPrint" />
          <Button CommandName="cmdExit" />
        </MenuGroup>
      </ApplicationMenu>
    </Ribbon.ApplicationMenu>
    ```

    

Lorsque le balisage est compilé avec l’outil compilateur de commande d’interface utilisateur (UICC), les noms et les ID de commande sont placés dans un fichier d’en-tête utilisé par l’application hôte du ruban.

Voici un exemple de fichier d’en-tête généré par UICC.


```
// *****************************************************************************
// * This is an automatically generated header file for UI Element definition  *
// * resource symbols and values. Please do not modify manually.               *
// *****************************************************************************

#pragma once

#define cmdFileMenu 25000 
#define cmdNew 22001  /* New */ 
#define cmdNew_LabelTitle_RESID 60005
#define cmdOpen 22002  /* Open */ 
#define cmdOpen_LabelTitle_RESID 60006
#define cmdSave 22003  /* Save */ 
#define cmdSave_LabelTitle_RESID 60007
#define cmdSave_TooltipTitle_RESID 60008
#define cmdSave_TooltipDescription_RESID 60009
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Extensible Application Markup Language (XAML)](/dotnet/framework/wpf/advanced/xaml-in-wpf)
</dt> <dt>

[Compilation du balisage du ruban](windowsribbon-intentcl.md)
</dt> </dl>

 

 