---
title: Utilisation des galeries
description: l’infrastructure du ruban Windows offre aux développeurs un modèle robuste et cohérent pour gérer le contenu dynamique sur divers contrôles basés sur des collections.
ms.assetid: 447039f3-1428-4b6f-94cf-78cf81974041
keywords:
- Windows Ruban, galeries
- Ruban, galeries
- Windows Ruban, contrôle DropDownGallery
- Ruban, contrôle DropDownGallery
- Windows Ruban, contrôle SplitButtonGallery
- Ruban, contrôle SplitButtonGallery
- Contrôle DropDownGallery
- Contrôle SplitButtonGallery
- galeries pour Windows ruban
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce142c1159d7a7c4129f402716ed7e394ebb4829f043d7c58dd23221b1479720
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119933443"
---
# <a name="working-with-galleries"></a>Utilisation des galeries

l’infrastructure du ruban Windows offre aux développeurs un modèle robuste et cohérent pour gérer le contenu dynamique sur divers contrôles basés sur des collections. En adaptant et en reconfigurant l’interface ruban, ces contrôles dynamiques permettent à l’infrastructure de répondre à l’interaction de l’utilisateur dans l’application hôte et le ruban lui-même, et offrent la flexibilité nécessaire pour gérer différents environnements d’exécution.

-   [Introduction](#introduction)
-   [Galeries](#working-with-galleries)
    -   [Galeries d’éléments](#item-galleries)
    -   [Galeries de commandes](#command-galleries)
    -   [Contrôles de la Galerie](#working-with-galleries)
-   [Comment implémenter une galerie](#how-to-implement-a-gallery)
    -   [Composants de base](#the-basic-components)
    -   [Déclarer les contrôles dans le balisage](#declare-the-controls-in-markup)
    -   [Créer un gestionnaire de commandes](#create-a-command-handler)
    -   [Lier le gestionnaire de commandes](#bind-the-command-handler)
    -   [Initialiser une collection](#initialize-a-collection)
    -   [Gérer les événements de collection](#handle-collection-events)
-   [Rubriques connexes](#related-topics)

## <a name="introduction"></a>Introduction

Cette capacité de l’infrastructure du ruban à s’adapter de manière dynamique aux conditions d’exécution, aux exigences de l’application et aux entrées de l’utilisateur final met en évidence les fonctionnalités enrichies de l’interface utilisateur de l’infrastructure et offre aux développeurs la flexibilité nécessaire pour répondre à un large éventail de besoins des clients.

L’objectif de ce guide est de décrire les contrôles de Galerie dynamiques pris en charge par l’infrastructure, d’expliquer leurs différences, de discuter du moment et de l’endroit où ils peuvent être utilisés, et de montrer comment ils peuvent être incorporés dans une application de ruban.

## <a name="galleries"></a>Galeries

Les galeries sont des contrôles de zone de liste riches en fonctionnalités et graphiques. La collection d’éléments d’une galerie peut être organisée par catégories, affichées dans des colonnes flexibles et des dispositions basées sur des lignes, représentées par des images et du texte, et selon le type de Galerie, prend en charge l’aperçu instantané.

Les galeries sont fonctionnellement distinctes des autres contrôles de ruban dynamique pour les raisons suivantes :

-   Les galeries implémentent l’interface [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) qui définit les différentes méthodes de manipulation des collections d’éléments de la Galerie.
-   Les galeries peuvent être mises à jour au moment de l’exécution, en fonction de l’activité qui se produit directement dans le ruban, par exemple lorsqu’un utilisateur ajoute une commande à la barre d’outils accès rapide (QAT).
-   Les galeries peuvent être mises à jour au moment de l’exécution, en fonction de l’activité qui se produit indirectement de l’environnement d’exécution, par exemple lorsqu’un pilote d’imprimante prend uniquement en charge les mises en page en mode portrait.
-   Les galeries peuvent être mises à jour au moment de l’exécution, en fonction de l’activité qui se produit indirectement dans l’application hôte, par exemple lorsqu’un utilisateur sélectionne un élément dans un document.

L’infrastructure du ruban expose deux types de galeries : les galeries d’éléments et les galeries de commandes.

### <a name="item-galleries"></a>Galeries d’éléments

Les galeries d’éléments contiennent une collection d’éléments associés basée sur les index, où chaque élément est représenté par une image, une chaîne, ou les deux. Le contrôle est lié à un gestionnaire de commandes unique qui s’appuie sur la valeur d’index qui est identifiée par la propriété de l’interface utilisateur de la valeur [ \_ \_ SelectedItem](windowsribbon-reference-properties-uipkey-selecteditem.md) .

Les galeries d’éléments prennent en charge l’aperçu instantané, ce qui signifie que vous pouvez afficher un résultat de commande, basé sur mouseover ou Focus, sans valider ou appeler réellement la commande.

> [!IMPORTANT]
> L’infrastructure ne prend pas en charge l’hébergement de galeries d’éléments dans le menu de l’application.

 

### <a name="command-galleries"></a>Galeries de commandes

Les galeries de commandes contiennent une collection d’éléments distincts non indexés. Chaque élément est représenté par un contrôle unique lié à un gestionnaire de commandes via un ID de commande. Comme les contrôles autonomes, chaque élément d’une bibliothèque de commandes achemine les événements d’entrée vers un gestionnaire de commandes associé, la Galerie de commandes elle-même n’écoute pas les événements.

Les galeries de commandes ne prennent pas en charge l’aperçu instantané.

### <a name="gallery-controls"></a>Contrôles de la Galerie

L’infrastructure du ruban contient quatre contrôles de Galerie : [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md), [**InRibbonGallery**](windowsribbon-element-inribbongallery.md)et [**ComboBox**](windowsribbon-element-combobox.md). Tout sauf le **contrôle ComboBox** peut être implémenté comme une galerie d’éléments ou une bibliothèque de commandes.

### <a name="dropdowngallery"></a>DropDownGallery

Un [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) est un bouton qui affiche une liste déroulante contenant une collection d’éléments ou de commandes s’excluant mutuellement.

la capture d’écran suivante illustre le contrôle de galerie de la [liste](windowsribbon-controls-dropdowngallery.md) déroulante du ruban dans Microsoft Paint pour Windows 7.

![capture d’écran d’un contrôle de la Galerie déroulante dans Microsoft Paint pour Windows 7.](images/controls/dropdowngallery.png)

### <a name="splitbuttongallery"></a>SplitButtonGallery

Un [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) est un contrôle composite qui expose un élément ou une commande par défaut unique à partir de sa collection sur un bouton principal, et qui affiche d’autres éléments ou commandes dans une liste déroulante mutuellement exclusive qui s’affiche lorsqu’un utilisateur clique sur un bouton secondaire.

la capture d’écran suivante illustre le contrôle de [galerie du bouton partagé](windowsribbon-controls-splitbuttongallery.md) du ruban dans Microsoft Paint pour Windows 7.

![capture d’écran d’un contrôle de Galerie de boutons partagés dans Microsoft Paint pour Windows 7.](images/controls/splitbuttongallery.png)

### <a name="inribbongallery"></a>InRibbonGallery

Un [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) est une galerie qui affiche une collection d’éléments ou de commandes connexes dans le ruban. S’il y a trop d’éléments dans la Galerie, une flèche de développement est fournie pour afficher le reste de la collection dans un volet développé.

la capture d’écran suivante illustre le contrôle de [galerie ruban dans le ruban](windowsribbon-controls-inribbongallery.md) dans Microsoft Paint pour Windows 7.

![capture d’écran d’un contrôle de galerie dans le ruban dans le ruban Microsoft Paint.](images/controls/inribbongallery.png)

### <a name="combobox"></a>Liste déroulante

Une zone de liste [**modifiable**](windowsribbon-element-combobox.md) est une zone de liste à une seule colonne qui contient une collection d’éléments avec un contrôle statique ou un contrôle d’édition et une flèche déroulante. La partie zone de liste du contrôle s’affiche lorsque l’utilisateur clique sur la flèche déroulante.

La capture d’écran suivante illustre un contrôle de [zone de liste déroulante](windowsribbon-controls-combobox.md) du ruban à partir de Windows Live Movie Maker.

![capture d’écran d’un contrôle de zone de liste déroulante dans le ruban Microsoft Paint.](images/controls/combobox.png)

Étant donné que la [**zone de liste déroulante**](windowsribbon-element-combobox.md) est exclusivement une galerie d’éléments, elle ne prend pas en charge les éléments de commande. C’est également le seul contrôle de galerie qui ne prend pas en charge un espace de commande. (Un espace de commande est une collection de commandes qui sont déclarées dans le balisage et répertoriées en bas d’une galerie d’éléments ou d’une bibliothèque de commandes.)

L’exemple de code suivant montre le balisage requis pour déclarer un espace de commande à trois boutons dans un [**DropDownGallery**](windowsribbon-element-dropdowngallery.md).


```C++
<DropDownGallery 
  CommandName="cmdSizeAndColor" 
  TextPosition="Hide" 
  Type="Commands"
  ItemHeight="32"
  ItemWidth="32">
  <DropDownGallery.MenuLayout>
    <FlowMenuLayout Rows="2" Columns="3" Gripper="None"/>
  </DropDownGallery.MenuLayout>
  <Button CommandName="cmdCommandSpace1"/>
  <Button CommandName="cmdCommandSpace2"/>
  <Button CommandName="cmdCommandSpace3"/>
</DropDownGallery>
```



La capture d’écran suivante illustre l’espace de commande à trois boutons de l’exemple de code précédent.

![capture d’écran d’un espace de commande à trois boutons dans un dropdowngallery.](images/markup/gallerysample-commandspace.png)

## <a name="how-to-implement-a-gallery"></a>Comment implémenter une galerie

Cette section décrit les détails d’implémentation des galeries de ruban et explique comment les incorporer dans une application de ruban.

### <a name="the-basic-components"></a>Composants de base

Cette section décrit l’ensemble des propriétés et des méthodes qui forment la structure fondamentale du contenu dynamique dans l’infrastructure du ruban et prennent en charge l’ajout, la suppression, la mise à jour et la manipulation du contenu et de la disposition visuelle des galeries de ruban au moment de l’exécution.

### <a name="iuicollection"></a>IUICollection

Les galeries requièrent un ensemble de méthodes de base pour accéder aux éléments individuels de leurs collections et les manipuler.

L’interface [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) définit ces méthodes, et l’infrastructure complète leurs fonctionnalités à l’aide de méthodes supplémentaires définies dans l’interface [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) . **IUICollection** est implémenté par l’infrastructure pour chaque déclaration de galerie dans le balisage du ruban.

Si vous avez besoin de fonctionnalités supplémentaires qui ne sont pas fournies par l’interface [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) , un objet de collection personnalisé qui est implémenté par l’application hôte et dérivé de [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) peut être substitué à la collection de frameworks.

### <a name="iuicollectionchangedevent"></a>IUICollectionChangedEvent

Pour qu’une application réponde aux modifications apportées à une collection de la Galerie, elle doit implémenter l’interface [**IUICollectionChangedEvent**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollectionchangedevent) . Les applications peuvent s’abonner à des notifications à partir d’un objet [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) par le biais de l’écouteur d’événements [**IUICollectionChangedEvent :: OnChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicollectionchangedevent-onchanged) .

Lorsque l’application remplace la collection de galeries fournie par le Framework par une collection personnalisée, l’application doit implémenter l’interface [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) . Si [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) n’est pas implémenté, l’application ne peut pas notifier l’infrastructure des modifications apportées à la collection personnalisée qui requièrent des mises à jour dynamiques du contrôle Gallery.

Dans les cas où [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) n’est pas implémenté, le contrôle Gallery peut être mis à jour uniquement par invalidation via [**IUIFramework :: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) et [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty), ou en appelant [**IUIFramework :: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).

### <a name="iuisimplepropertyset"></a>IUISimplePropertySet

Les applications doivent implémenter IUISimplePropertySet pour chaque élément ou commande d’une collection de la Galerie. Toutefois, les propriétés qui peuvent être demandées avec [**IUISimplePropertySet :: GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) varient.

Les éléments sont définis et liés à une galerie via la clé de propriété [ \_ \_ ItemsSource de l’interface utilisateur](windowsribbon-reference-properties-uipkey-itemssource.md) et exposent les propriétés avec un objet [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) .

Les propriétés valides pour les éléments dans les galeries d’éléments ([**\_ \_ collection UI COMMANDTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype)) sont décrites dans le tableau suivant.

> [!Note]  
> Certaines propriétés d’élément, telles [que \_ l' \_ étiquette de l’interface utilisateur](windowsribbon-reference-properties-uipkey-label.md), peuvent être définies dans le balisage. Pour plus d’informations, consultez la documentation de référence sur les [clés de propriété](windowsribbon-reference-properties.md) .

 



Contrôler

Propriétés

[**ComboBox**](windowsribbon-element-combobox.md)

[Interface utilisateur \_ \_Étiquette de nom](windowsribbon-reference-properties-uipkey-label.md)du code de [l’interface utilisateur, code de \_ \_ catégorie](windowsribbon-reference-properties-uipkey-categoryid.md)

[**DropDownGallery**](windowsribbon-element-dropdowngallery.md)

[Interface utilisateur \_ \_Étiquette de nom](windowsribbon-reference-properties-uipkey-label.md)de la partie, [ \_ \_ ItemImage d’interface utilisateur](windowsribbon-reference-properties-uipkey-itemimage.md) , nom de la [ \_ \_ catégorie d’interface utilisateur](windowsribbon-reference-properties-uipkey-categoryid.md)

[**InRibbonGallery**](windowsribbon-element-inribbongallery.md)

[Interface utilisateur \_ \_Étiquette de nom](windowsribbon-reference-properties-uipkey-label.md)de la partie, [ \_ \_ ItemImage d’interface utilisateur](windowsribbon-reference-properties-uipkey-itemimage.md) , nom de la [ \_ \_ catégorie d’interface utilisateur](windowsribbon-reference-properties-uipkey-categoryid.md)

[**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)

[Interface utilisateur \_ \_Étiquette de nom](windowsribbon-reference-properties-uipkey-label.md)de la partie, [ \_ \_ ItemImage d’interface utilisateur](windowsribbon-reference-properties-uipkey-itemimage.md), nom de la [ \_ \_ catégorie d’interface utilisateur](windowsribbon-reference-properties-uipkey-categoryid.md)

[Interface utilisateur \_ La \_ ](windowsribbon-reference-properties-uipkey-selecteditem.md) propriété de la bibliothèque de propriétés est une propriété de la Galerie d’éléments.



 

Les propriétés d’élément valides pour les galeries de commandes ([**UI \_ COMMANDTYPE \_ COMMANDCOLLECTION**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype)) sont décrites dans le tableau suivant.



| Contrôler                                                                | Propriétés                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)       | [Interface utilisateur \_ Hypergraphique de la \_ ](windowsribbon-reference-properties-uipkey-commandid.md)présente, interface de [l’interface utilisateur \_ \_ CommandType](windowsribbon-reference-properties-uipkey-commandtype.md) , code de la [ \_ \_ catégorie](windowsribbon-reference-properties-uipkey-categoryid.md) d’interface utilisateur |
| [**InRibbonGallery**](windowsribbon-element-inribbongallery.md)       | [Interface utilisateur \_ Hypergraphique de la \_ ](windowsribbon-reference-properties-uipkey-commandid.md)présente, interface de [l’interface utilisateur \_ \_ CommandType](windowsribbon-reference-properties-uipkey-commandtype.md) , code de la [ \_ \_ catégorie](windowsribbon-reference-properties-uipkey-categoryid.md) d’interface utilisateur |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) | [Interface utilisateur \_ Hypergraphique de la \_ ](windowsribbon-reference-properties-uipkey-commandid.md)présente, interface de [l’interface utilisateur \_ \_ CommandType](windowsribbon-reference-properties-uipkey-commandtype.md), code de la [ \_ \_ catégorie](windowsribbon-reference-properties-uipkey-categoryid.md) d’interface utilisateur  |



 

Les catégories sont utilisées pour organiser les éléments et les commandes dans les galeries. Les catégories sont définies et liées à une galerie via la clé de propriété des [ \_ \_ catégories de l’interface utilisateur](windowsribbon-reference-properties-uipkey-categories.md) et exposent les propriétés avec un objet [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) spécifique à la catégorie.

Les catégories n’ont pas de CommandType et ne prennent pas en charge l’interaction de l’utilisateur. Par exemple, les catégories ne peuvent pas devenir SelectedItem dans une galerie d’éléments, et elles ne sont pas liées à une commande dans une galerie de commandes. À l’instar des autres propriétés d’élément de la Galerie, les propriétés de catégorie telles que [l’étiquette de nom d’utilisateur et le \_ \_ nom](windowsribbon-reference-properties-uipkey-label.md) du code [](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue)de [ \_ \_ ](windowsribbon-reference-properties-uipkey-categoryid.md) catégorie

> [!IMPORTANT]
> [**IUISimplePropertySet :: GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) doit retourner la [**collection d’interface utilisateur \_ \_ INVALIDINDEX**](/windows/desktop/windowsribbon/windowsribbon-ui-collection-invalidindex) lorsque [l’interface utilisateur du groupe de catégories d’utilisateur \_ \_](windowsribbon-reference-properties-uipkey-categoryid.md) est demandée pour un élément qui n’a pas de catégorie associée.

 

### <a name="declare-the-controls-in-markup"></a>Déclarer les contrôles dans le balisage

Les galeries, comme tous les contrôles de ruban, doivent être déclarées dans le balisage. Une galerie est identifiée dans le balisage comme une galerie d’éléments ou une bibliothèque de commandes, et divers détails de présentation sont déclarés. Contrairement à d’autres contrôles, les galeries ne requièrent que le contrôle de base, ou conteneur de collection, soient déclarés dans le balisage. Les regroupements réels sont remplis au moment de l’exécution. Quand une galerie est déclarée dans le balisage, l’attribut de *type* est utilisé pour spécifier si la Galerie est une galerie d’éléments d’une bibliothèque de commandes.

Un certain nombre d’attributs de disposition facultatifs sont disponibles pour chacun des contrôles présentés ici. Ces attributs fournissent des préférences de développeur pour l’infrastructure à suivre qui affectent directement la manière dont un contrôle est rempli et affiché dans un ruban. Les préférences applicables dans le balisage sont liées aux modèles d’affichage et de disposition et aux comportements décrits dans [Personnalisation d’un ruban à l’aide des définitions de taille et des stratégies de mise à l’échelle](windowsribbon-templates.md).

Si un contrôle particulier n’autorise pas les préférences de disposition directement dans le balisage ou si les préférences de disposition ne sont pas spécifiées, l’infrastructure définit les conventions d’affichage spécifiques au contrôle en fonction de la quantité d’espace d’écran disponible.

Les exemples suivants montrent comment incorporer un ensemble de galeries dans un ruban.

### <a name="command-declarations"></a>Déclarations de commande

Les commandes doivent être déclarées avec un attribut *CommandName* utilisé pour associer un contrôle, ou un ensemble de contrôles, à la commande.

Un attribut *CommandID* utilisé pour lier une commande à un gestionnaire de commandes lors de la compilation du balisage peut également être spécifié ici. Si aucun ID n’est fourni, l’infrastructure est générée.


```XML
<!-- ComboBox -->
<Command Name="cmdComboBoxGroup"
         Symbol="cmdComboBoxGroup"
         Comment="ComboBox Group"
         LabelTitle="ComboBox"/>
<Command Name="cmdComboBox"
         Symbol="cmdComboBox"
         Comment="ComboBox"
         LabelTitle="ComboBox"/>
```


```XML

<!-- DropDownGallery -->
<Command Name="cmdDropDownGalleryGroup"
         Symbol="cmdDropDownGalleryGroup"
         Comment="DropDownGallery Group"
         LabelTitle="DropDownGallery"/>
<Command Name="cmdDropDownGallery"
         Symbol="cmdDropDownGallery"
         Comment="DropDownGallery"
         LabelTitle="DropDownGallery"/>
```




```XML

<!-- InRibbonGallery -->
<Command Name="cmdInRibbonGalleryGroup"
         Symbol="cmdInRibbonGalleryGroup"
         Comment="InRibbonGallery Group"
         LabelTitle="InRibbonGallery"/>
<Command Name="cmdInRibbonGallery"
         Symbol="cmdInRibbonGallery"
         Comment="InRibbonGallery"
         LabelTitle="InRibbonGallery"
```



```XML

<!-- SplitButtonGallery -->
<Command Name="cmdSplitButtonGalleryGroup"
         Symbol="cmdSplitButtonGalleryGroup"
         Comment="SplitButtonGallery Group"
         LabelTitle="SplitButtonGallery"/>
<Command Name="cmdSplitButtonGallery"
         Symbol="cmdSplitButtonGallery"
         Comment="SplitButtonGallery"
         LabelTitle="SplitButtonGallery"
```



### <a name="control-declarations"></a>Déclarations de contrôle

Cette section contient des exemples qui illustrent le balisage de contrôle de base requis pour les différents types de Galerie. Elles montrent comment déclarer les contrôles de la Galerie et les associer à une commande via l’attribut *CommandName* .

L’exemple suivant montre une déclaration de contrôle pour le [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) où l’attribut de *type* est utilisé pour spécifier qu’il s’agit d’une bibliothèque de commandes.


```XML
<!-- DropDownGallery -->
<Group CommandName="cmdDropDownGalleryGroup">
  <DropDownGallery CommandName="cmdDropDownGallery"
                   TextPosition="Hide"
                   Type="Commands"
                   ItemHeight="32"
                   ItemWidth="32">
    <DropDownGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </DropDownGallery.MenuLayout>
    <DropDownGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
       </MenuGroup>
       <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </DropDownGallery.MenuGroups>
  </DropDownGallery>
</Group>
```



L’exemple suivant montre une déclaration de contrôle pour [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md).


```XML
<!-- SplitButtonGallery -->
<Group CommandName="cmdSplitButtonGalleryGroup">
  <SplitButtonGallery CommandName="cmdSplitButtonGallery">
    <SplitButtonGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </SplitButtonGallery.MenuLayout>
    <SplitButtonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </SplitButtonGallery.MenuGroups>
  </SplitButtonGallery>
</Group>
```



L’exemple suivant montre une déclaration de contrôle pour [**InRibbonGallery**](windowsribbon-element-inribbongallery.md).

> [!Note]  
> Étant donné que [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) est conçu pour afficher un sous-ensemble de sa collection d’éléments dans le ruban sans activer un menu déroulant, il fournit un certain nombre d’attributs facultatifs qui régissent la taille et la disposition des éléments sur l’initialisation du ruban. Ces attributs sont uniques à **InRibbonGallery** et ne sont pas disponibles dans les autres contrôles dynamiques.

 


```XML
<!-- InRibbonGallery -->
<Group CommandName="cmdInRibbonGalleryGroup" SizeDefinition="OneInRibbonGallery">
  <InRibbonGallery CommandName="cmdInRibbonGallery"
                   MaxColumns="10"
                   MaxColumnsMedium="5"
                   MinColumnsLarge="5"
                   MinColumnsMedium="3"
                   Type="Items">
    <InRibbonGallery.MenuLayout>
      <VerticalMenuLayout Rows="2"
                          Gripper="Vertical"/>
    </InRibbonGallery.MenuLayout>
    <InRibbonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </InRibbonGallery.MenuGroups>            
  </InRibbonGallery>
</Group>
```



L’exemple suivant montre une déclaration de contrôle pour la [**zone de liste déroulante**](windowsribbon-element-combobox.md).


```XML
<!-- ComboBox -->
<Group CommandName="cmdComboBoxGroup">
  <ComboBox CommandName="cmdComboBox">              
  </ComboBox>
</Group>
```



### <a name="create-a-command-handler"></a>Créer un gestionnaire de commandes

Pour chaque commande, l’infrastructure du ruban requiert un gestionnaire de commandes correspondant dans l’application hôte. Les gestionnaires de commandes sont implémentés par l’application hôte du ruban et sont dérivés de l’interface [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) .

> [!Note]  
> Plusieurs commandes peuvent être liées à un gestionnaire de commandes unique.

 

Un gestionnaire de commandes remplit deux fonctions :

-   [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) répond aux demandes de mise à jour de propriété. Les valeurs des propriétés de commande, telles que [l’interface utilisateur de l’interface utilisateur \_ \_ activée](windowsribbon-reference-properties-uipkey-enabled.md) ou [l' \_ \_ étiquette de l’interface utilisateur](windowsribbon-reference-properties-uipkey-label.md), sont définies par le biais d’appels à [**IUIFramework :: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) ou [**IUIFramework :: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand).
-   [**IUICommandHandler :: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) répond aux événements d’exécution. Cette méthode prend en charge les trois États d’exécution suivants qui sont spécifiés par le paramètre [**\_ EXECUTIONVERB de l’interface utilisateur**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_executionverb) .
    -   L’état d’exécution exécute, ou valide, toutes les commandes auxquelles le gestionnaire est lié.
    -   L’état d’aperçu affiche un aperçu des commandes auxquelles le gestionnaire est lié. Cela permet essentiellement d’exécuter les commandes sans valider le résultat.
    -   L’État CancelPreview annule toutes les commandes prévisualisées. Cela est nécessaire pour prendre en charge le parcours via un menu ou une liste, et pour afficher un aperçu séquentiel et annuler les résultats en fonction des besoins.

L’exemple suivant illustre un gestionnaire de commandes de la Galerie.


```C++
/*
 * GALLERY COMMAND HANDLER IMPLEMENTATION
 */
class CGalleryCommandHandler
      : public CComObjectRootEx<CComMultiThreadModel>
      , public IUICommandHandler
{
public:
  BEGIN_COM_MAP(CGalleryCommandHandler)
    COM_INTERFACE_ENTRY(IUICommandHandler)
  END_COM_MAP()

  // Gallery command handler's Execute method
  STDMETHODIMP Execute(UINT nCmdID,
                       UI_EXECUTIONVERB verb, 
                       const PROPERTYKEY* key,
                       const PROPVARIANT* ppropvarValue,
                       IUISimplePropertySet* pCommandExecutionProperties)
  {
    HRESULT hr = S_OK;
        
    // Switch on manner of execution (Execute/Preview/CancelPreview)
    switch (verb)
    {
      case UI_EXECUTIONVERB_EXECUTE:
        if(nCmdID == cmdTextSizeGallery || 
           nCmdID == cmdTextSizeGallery2 || 
           nCmdID == cmdTextSizeGallery3)
        {
          if (pCommandExecutionProperties != NULL)
          {
            CItemProperties *pItem = 
              static_cast<CItemProperties *>(pCommandExecutionProperties);
            g_prevSelection = g_index = pItem->GetIndex();
            UpdateGallerySelectedItems();
            ::InvalidateRect(g_hWindowFrame, NULL, TRUE);
          }
          else
          {
            g_prevSelection = g_index = 0;
            UpdateGallerySelectedItems();
            ::InvalidateRect(g_hWindowFrame, NULL, TRUE);
          }
        }           
        break;
      case UI_EXECUTIONVERB_PREVIEW:
        CItemProperties *pItem = 
          static_cast<CItemProperties *>(pCommandExecutionProperties);
        g_index = pItem->GetIndex();
        ::InvalidateRect(g_hWindowFrame, NULL, TRUE);
        break;
      case UI_EXECUTIONVERB_CANCELPREVIEW:
        g_index = g_prevSelection;
        ::InvalidateRect(g_hWindowFrame, NULL, TRUE);
        break;
    }   
    return hr;
  }

  // Gallery command handler's UpdateProperty method
  STDMETHODIMP UpdateProperty(UINT nCmdID,
                              REFPROPERTYKEY key,
                              const PROPVARIANT* ppropvarCurrentValue,
                              PROPVARIANT* ppropvarNewValue)
  {
    UNREFERENCED_PARAMETER(ppropvarCurrentValue);

    HRESULT hr = E_NOTIMPL;         

    if (key == UI_PKEY_ItemsSource) // Gallery items requested
    {
      if (nCmdID == cmdTextSizeGallery || 
          nCmdID == cmdTextSizeGallery2 || 
          nCmdID == cmdTextSizeGallery3)
      {
        CComQIPtr<IUICollection> spCollection(ppropvarCurrentValue->punkVal);

        int count = _countof(g_labels);

        for (int i = 0; i < count; i++)
        {
          CComObject<CItemProperties> * pItem;
          CComObject<CItemProperties>::CreateInstance(&pItem);
                    
          pItem->AddRef();
          pItem->Initialize(i);

          spCollection->Add(pItem);
        }
        return S_OK;
      }
      if (nCmdID == cmdCommandGallery1)
      {
        CComQIPtr<IUICollection> spCollection(ppropvarCurrentValue->punkVal);

        int count = 12;
        int commands[] = {cmdButton1, 
                          cmdButton2, 
                          cmdBoolean1, 
                          cmdBoolean2, 
                          cmdButton1, 
                          cmdButton2, 
                          cmdBoolean1, 
                          cmdBoolean2, 
                          cmdButton1, 
                          cmdButton2, 
                          cmdBoolean1, 
                          cmdBoolean2};

        for (int i = 0; i < count; i++)
        {
          CComObject<CItemProperties> * pItem;
          CComObject<CItemProperties>::CreateInstance(&pItem);
                    
          pItem->AddRef();
          pItem->InitializeAsCommand(commands[i]);

          spCollection->Add(pItem);
        }
        return S_OK;
      }
    }        
    else if (key == UI_PKEY_SelectedItem) // Selected item requested
    {           
      hr = UIInitPropertyFromUInt32(UI_PKEY_SelectedItem, g_index, ppropvarNewValue);           
    }
    return hr;
  }
};

```



### <a name="bind-the-command-handler"></a>Lier le gestionnaire de commandes

Une fois que vous avez défini un gestionnaire de commandes, la commande doit être liée au gestionnaire.

L’exemple suivant montre comment lier une commande de la galerie à un gestionnaire de commandes spécifique. Dans ce cas, les contrôles [**ComboBox**](windowsribbon-element-combobox.md) et Gallery sont liés à leurs gestionnaires de commandes respectifs.


```C++
// Called for each Command in markup. 
// Application will return a Command handler for each Command.
STDMETHOD(OnCreateUICommand)(UINT32 nCmdID,
                             UI_COMMANDTYPE typeID,
                             IUICommandHandler** ppCommandHandler) 
{   
  // CommandType for ComboBox and galleries
  if (typeID == UI_COMMANDTYPE_COLLECTION || typeID == UI_COMMANDTYPE_COMMANDCOLLECTION) 
  {
    switch (nCmdID)
    {
      case cmdComboBox:
        CComObject<CComboBoxCommandHandler> * pComboBoxCommandHandler;
        CComObject<CComboBoxCommandHandler>::CreateInstance(&pComboBoxCommandHandler);
        return pComboBoxCommandHandler->QueryInterface(IID_PPV_ARGS(ppCommandHandler));
      default:
        CComObject<CGalleryCommandHandler> * pGalleryCommandHandler;
        CComObject<CGalleryCommandHandler>::CreateInstance(&pGalleryCommandHandler);
        return pGalleryCommandHandler->QueryInterface(IID_PPV_ARGS(ppCommandHandler));
    }
    return E_NOTIMPL; // Command is not implemented, so do not pass a handler back.
  }
}
```



### <a name="initialize-a-collection"></a>Initialiser une collection

L’exemple suivant illustre une implémentation personnalisée de [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) pour les galeries d’éléments et de commandes.

La classe CItemProperties dans cet exemple est dérivée de [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset). En plus de la méthode [**IUISimplePropertySet :: GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue)requise, la classe CItemProperties implémente un ensemble de fonctions d’assistance pour l’initialisation et le suivi d’index.


```C++
//
//  PURPOSE:    Implementation of IUISimplePropertySet.
//
//  COMMENTS:
//              Three gallery-specific helper functions included. 
//

class CItemProperties
  : public CComObjectRootEx<CComMultiThreadModel>
  , public IUISimplePropertySet
{
  public:

  // COM map for QueryInterface of IUISimplePropertySet.
  BEGIN_COM_MAP(CItemProperties)
    COM_INTERFACE_ENTRY(IUISimplePropertySet)
  END_COM_MAP()

  // Required method that enables property key values to be 
  // retrieved on gallery collection items.
  STDMETHOD(GetValue)(REFPROPERTYKEY key, PROPVARIANT *ppropvar)
  {
    HRESULT hr;

    // No category is associated with this item.
    if (key == UI_PKEY_CategoryId)
    {
      return UIInitiPropertyFromUInt32(UI_PKEY_CategoryId, 
                                       UI_COLLECTION_INVALIDINDEX, 
                                       pprovar);
    }

    // A Command gallery.
    // _isCommandGallery is set on initialization.
    if (_isCommandGallery)
    {           
      if(key == UI_PKEY_CommandId && _isCommandGallery)
      {
        // Return a pointer to the CommandId of the item.
        return InitPropVariantFromUInt32(_cmdID, ppropvar);
      }         
    }
    // An item gallery.
    else
    {
      if (key == UI_PKEY_Label)
      {
        // Return a pointer to the item label string.
        return UIInitPropertyFromString(UI_PKEY_Label, ppropvar);
      }
      else if(key == UI_PKEY_ItemImage)
      {
        // Return a pointer to the item image.
        return UIInitPropertyFromImage(UI_PKEY_ItemImage, ppropvar);
      }         
    }
    return E_NOTIMPL;
  }

  // Initialize an item in an item gallery collection at the specified index.
  void Initialize(int index)
  {
    _index = index;
    _cmdID = 0;
    _isCommandGallery = false;
  }

  // Initialize a Command in a Command gallery.
  void InitializeAsCommand(__in UINT cmdID)
  {
    _index = 0;
    _cmdID = cmdID;
    _isCommandGallery = true;
  }

  // Gets the index of the selected item in an item gallery.
  int GetIndex()
  {
    return _index;
  }

private:
  int _index;
  int _cmdID;
  bool _isCommandGallery;   
};
```



### <a name="handle-collection-events"></a>Gérer les événements de collection

L’exemple suivant illustre une implémentation de IUICollectionChangedEvent.


```C++
class CQATChangedEvent
  : public CComObjectRootEx<CComSingleThreadModel>
  , public IUICollectionChangedEvent
{
  public:

  HRESULT FinalConstruct()
  {
    _pSite = NULL;
    return S_OK;
  }

  void Initialize(__in CQATSite* pSite)
  {
    if (pSite != NULL)
    {
      _pSite = pSite;
    }
  }

  void Uninitialize()
  {
    _pSite = NULL;
  }

  BEGIN_COM_MAP(CQATChangedEvent)
    COM_INTERFACE_ENTRY(IUICollectionChangedEvent)
  END_COM_MAP()

  // IUICollectionChangedEvent interface
  STDMETHOD(OnChanged)(UI_COLLECTIONCHANGE action, 
                       UINT32 oldIndex, 
                       IUnknown *pOldItem, 
                       UINT32 newIndex, 
                       IUnknown *pNewItem)
  {
    if (_pSite)
    {
      _pSite->OnCollectionChanged(action, oldIndex, pOldItem, newIndex, pNewItem);
    }
    return S_OK;
  }

  protected:
  virtual ~CQATChangedEvent(){}

  private:
  CQATSite* _pSite; // Weak ref to avoid circular refcounts
};

HRESULT CQATHandler::EnsureCollectionEventListener(__in IUICollection* pUICollection)
{
  // Check if listener already exists.
  if (_spQATChangedEvent)
  {
    return S_OK;
  }

  HRESULT hr = E_FAIL;

  // Create an IUICollectionChangedEvent listener.
  hr = CreateInstanceWithRefCountOne(&_spQATChangedEvent);
    
  if (SUCCEEDED(hr))
  {
    CComPtr<IUnknown> spUnknown;
    _spQATChangedEvent->QueryInterface(IID_PPV_ARGS(&spUnknown));

    // Create a connection between the collection connection point and the sink.
    AtlAdvise(pUICollection, spUnknown, __uuidof(IUICollectionChangedEvent), &_dwCookie);
    _spQATChangedEvent->Initialize(this);
  }
  return hr;
}

HRESULT CQATHandler::OnCollectionChanged(
             UI_COLLECTIONCHANGE action, 
          UINT32 oldIndex, 
             IUnknown *pOldItem, 
          UINT32 newIndex, 
          IUnknown *pNewItem)
{
    UNREFERENCED_PARAMETER(oldIndex);
    UNREFERENCED_PARAMETER(newIndex);

    switch (action)
    {
      case UI_COLLECTIONCHANGE_INSERT:
      {
        CComQIPtr<IUISimplePropertySet> spProperties(pNewItem);
                
        PROPVARIANT var;
        if (SUCCEEDED(spProperties->GetValue(UI_PKEY_CommandId, &var)))
        {
          UINT tcid;
          if (SUCCEEDED(UIPropertyToUInt32(UI_PKEY_CommandId, var, &tcid)))
          {
            FireETWEvent(tcid, L"Added to QAT");
            PropVariantClear(&var);
          }
        }
      }
      break;
      case UI_COLLECTIONCHANGE_REMOVE:
      {
        CComQIPtr<IUISimplePropertySet> spProperties(pOldItem);
                
        PROPVARIANT var;
        if (SUCCEEDED(spProperties->GetValue(UI_PKEY_CommandId, &var)))
        {
          UINT tcid;
          if (SUCCEEDED(UIPropertyToUInt32(UI_PKEY_CommandId, var, &tcid)))
          {
            FireETWEvent(tcid, L"Removed from QAT");
            PropVariantClear(&var);
          }
        }
      }
      break;
    default:
  }
  return S_OK;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Propriétés de la collection](windowsribbon-reference-properties-collection.md)
</dt> <dt>

[Création d’une application de ruban](windowsribbon-stepbystep.md)
</dt> <dt>

[Fonctionnement des commandes et des contrôles](windowsribbon-commandscontrols.md)
</dt> <dt>

[Instructions relatives à l’expérience utilisateur du ruban](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[Processus de conception du ruban](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> <dt>

[Exemple de Galerie](windowsribbon-gallerysample.md)
</dt> </dl>

 

 