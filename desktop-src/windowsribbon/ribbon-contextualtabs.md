---
title: Affichage des onglets contextuels
description: Dans une application de l’infrastructure de ruban Windows, un onglet contextuel est un contrôle onglet masqué qui est affiché dans la ligne d’onglet lorsqu’un objet dans l’espace de travail d’application, tel qu’une image, est sélectionné ou mis en surbrillance.
ms.assetid: 2059ca42-6a99-43a2-b1f5-ce5554156993
keywords:
- Ruban Windows, onglets contextuels
- Ruban, onglets contextuels
- affichage des onglets contextuels du ruban Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8a1e81ac6587e39a04114fa2f938a6da0e9a4d1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727365"
---
# <a name="displaying-contextual-tabs"></a>Affichage des onglets contextuels

Dans une application de l’infrastructure de ruban Windows, un onglet contextuel est un contrôle [onglet](windowsribbon-controls-tab.md) masqué qui est affiché dans la ligne d’onglet lorsqu’un objet dans l’espace de travail d’application, tel qu’une image, est sélectionné ou mis en surbrillance.

-   [Introduction](#introduction)
-   [Implémentation des onglets contextuels](#implementing-contextual-tabs)
    -   [balisage](#markup)
    -   [Code](#code)
-   [Rubriques connexes](#related-topics)

## <a name="introduction"></a>Introduction

Contrairement aux onglets principaux, qui contiennent différentes commandes courantes qui sont pertinentes quel que soit le contexte de l’espace de travail, les onglets contextuels contiennent généralement une ou plusieurs commandes applicables à un objet sélectionné ou en surbrillance uniquement.

Lorsqu’un objet est sélectionné ou mis en surbrillance dans l’espace de travail de l’application, le type et le contexte de l’objet peuvent nécessiter des commandes disparates qui n’effectuent pas d’organisation ou de sens fonctionnel sur un onglet contextuel. Dans ce cas, plusieurs onglets contextuels, qui sont contenus dans un [groupe d’onglets](windowsribbon-controls-tabgroup.md), peuvent être nécessaires. Par exemple, la sélection d’une image contenue dans une cellule de tableau peut nécessiter deux onglets contextuels qui exposent les fonctionnalités de table et d’image.

> [!Note]  
> Outre plusieurs onglets contextuels, l’infrastructure du ruban prend également en charge plusieurs contrôles de [groupe d’onglets](windowsribbon-controls-tabgroup.md) dans un ruban.

 

Lorsque vous affichez des onglets contextuels, l’infrastructure du ruban applique un ensemble de comportements de base qui incluent :

-   Les onglets contextuels sont positionnés dans l’ordre dans lequel ils sont déclarés et à droite des onglets centraux dans la ligne de l’onglet du ruban.
-   Lorsque le ruban est redimensionné, les onglets sont mis à l’échelle et les étiquettes d’onglet sont tronquées en fonction de l’espace requis. Toutefois, les onglets contextuels visibles reçoivent une priorité d’affichage plus élevée dans laquelle ils sont mis à l’échelle et tronqués en dernier.
-   L’étiquette d’un [groupe d’onglets](windowsribbon-controls-tabgroup.md) s’affiche dans la barre de titre de l’application et s’étend sur tous les onglets contextuels associés.
-   Lorsque plusieurs contrôles de [groupe d’onglets](windowsribbon-controls-tabgroup.md) sont affichés en même temps, l’une des cinq couleurs uniques est assignée à l’arrière-plan de chaque groupe d’onglets dans la barre de titre de l’application. Cette couleur est également utilisée comme couleur de surbrillance pour les onglets contextuels dans le groupe d’onglets.
-   L’affectation de couleur au [groupe d’onglets](windowsribbon-controls-tabgroup.md) est basée sur l’ordre dans lequel les éléments du groupe d’onglets sont déclarés dans le balisage. Les couleurs sont définies par l’infrastructure et ne peuvent pas être spécifiées par l’application.
-   Les couleurs des [groupes d’onglets](windowsribbon-controls-tabgroup.md) définies par l’infrastructure peuvent être modifiées indirectement via les clés de propriété des [Propriétés du Framework](windowsribbon-reference-properties-framework.md) . Pour plus d’informations, consultez [Personnalisation des couleurs du ruban](ribbon-color.md).
-   Lorsque plus de cinq contrôles de [groupe d’onglets](windowsribbon-controls-tabgroup.md) sont affichés à un moment donné, le Framework effectue le cycle des couleurs associées.
-   Le nombre maximal de contrôles [onglet](windowsribbon-controls-tab.md) dans un ruban est limité à 100. Cela comprend les onglets contextuels, visibles ou non.

La capture d’écran suivante montre un onglet contextuel de Windows 7 Paint.

![capture d’écran qui montre un contrôle d’onglet contextuel.](images/controls/contextualtab.png)

## <a name="implementing-contextual-tabs"></a>Implémentation des onglets contextuels

Cette section présente les détails de l’implémentation des onglets contextuels du ruban et explique comment les incorporer dans une application de ruban.

### <a name="markup"></a>balisage

Les exemples suivants illustrent le balisage de base pour un élément [**TabGroup**](windowsribbon-element-tabgroup.md) qui contient deux onglets contextuels.

Cette section de code montre les déclarations de commande [**TabGroup**](windowsribbon-element-tabgroup.md) et [Tab](windowsribbon-controls-tab.md) .


```XML
<!-- Contextual Tabs -->
<Command Name='cmdContextualTab1'
         LabelTitle='Contextual Tab 1'
         Symbol='ID_CONTEXTUALTAB1'/>
<Command Name='cmdContextualTab2'
         LabelTitle='Contextual Tab 2'
         Symbol='ID_CONTEXTUALTAB2'/>
<Command Name='cmdContextualTabGroup'
         LabelTitle='Contextual Tabs'
         Symbol='ID_CONTEXTUALTAB_GROUP'/>
```



Cette section de code montre les déclarations de contrôle requises pour afficher deux onglets contextuels dans un [**TabGroup**](windowsribbon-element-tabgroup.md).


```XML
      <Ribbon.ContextualTabs>
        <TabGroup CommandName='cmdContextualTabGroup'>
          <Tab CommandName='cmdContextualTab1'>
            <!--InRibbonGallery Group-->
            <Group CommandName='cmdInRibbonGalleryGroup'
                   SizeDefinition='OneInRibbonGallery'>
              <InRibbonGallery CommandName='cmdTextSizeGallery3'
                               HasLargeItems='true'
                               ItemHeight='32'
                               ItemWidth='32'
                               MaxColumns='3' >
                <InRibbonGallery.MenuLayout>
                  <FlowMenuLayout Columns='3'
                                  Gripper ='Corner'/>
                </InRibbonGallery.MenuLayout>
              </InRibbonGallery>
            </Group>
            <!--Command Galleries Group-->
            <Group CommandName='cmdCommandGalleriesGroup'
                   SizeDefinition='OneInRibbonGallery'>
              <InRibbonGallery CommandName='cmdCommandGallery1'
                               Type='Commands'
                               MaxRows='3'
                               MaxColumns='3'>
                <InRibbonGallery.MenuLayout>
                  <FlowMenuLayout Columns='3'
                                  Gripper ='Corner'/>
                </InRibbonGallery.MenuLayout>
              </InRibbonGallery>
            </Group>
          </Tab>
          <Tab CommandName='cmdContextualTab2'></Tab>
        </TabGroup>
      </Ribbon.ContextualTabs> 
```



### <a name="code"></a>Code

[Interface utilisateur \_ Le \_ ContextAvailable](windowsribbon-reference-properties-uipkey-contextavailable.md) de la clé de serveur est la clé de propriété unique définie par l’infrastructure pour la spécification de la visibilité et de l’état des onglets contextuels. Lorsqu’un objet est sélectionné dans l’espace de travail d’application, l’une des trois valeurs de l’énumération [**\_ CONTEXTAVAILABILITY de l’interface utilisateur**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_contextavailability) peut être affectée à cette propriété, qui définit si un onglet contextuel existe et, le cas échéant, s’il est affiché sous la forme de l’onglet actif.

Une application demande une mise à jour du [groupe d’onglets](windowsribbon-controls-tabgroup.md) en invalidant et en mettant à jour la propriété [ \_ \_ ContextAvailable de l’interface utilisateur](windowsribbon-reference-properties-uipkey-contextavailable.md) , lorsque le contexte de l’espace de travail change.

Les sections suivantes du code montrent comment afficher un onglet contextuel quand une image est sélectionnée dans un espace de travail d’application.


```C++
// Initialize the image tools contextual tab visibility setting.
UI_CONTEXTAVAILABILITY g_ImageTools = UI_CONTEXTAVAILABILITY_NOTAVAILABLE;

// Called when an image is selected in the application.
void SelectImage()
{
  ...
  g_ImageTools = UI_CONTEXTAVAILABILITY_ACTIVE;

  // Invalidate the UI_PKEY_ContextAvailable property of the image tools  
  // contextual tab Command and trigger the UpdatePropery callback function.
  pUIFramework->InvalidateUICommand(
                  cmdImageTabSet, 
                  UI_INVALIDATIONS_PROPERTY, 
                  UI_PKEY_ContextAvailable);
  ...
}

// Update Tab Group properties.
HRESULT MyTabGroupCommandHandler::UpdateProperty(
                                  UINT nCmdID,
                                  REFPROPERTYKEY key,
                                  const PROPVARIANT* ppropvarCurrentValue,
                                  PROPVARIANT* ppropvarNewValue)
{
  HRESULT hr = E_FAIL;

  if (key == UI_PKEY_ContextAvailable)
  {
    hr = UIInitPropertyFromUInt32(key, g_ImageTools, ppropvarNewValue);
  }
  ...
  return hr;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions relatives à l’expérience utilisateur du ruban](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[Processus de conception du ruban](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

 

 