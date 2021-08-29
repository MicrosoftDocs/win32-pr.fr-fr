---
title: Propriété Ribbon. ContextualTabs
description: Représente un conteneur pour les onglets contextuels.
ms.assetid: 1f57a8d7-97ac-4007-8a36-c6aec5b85e6c
keywords:
- ruban. ContextualTabs, propriété Windows ruban
topic_type:
- apiref
api_name:
- Ribbon.ContextualTabs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6853952574d955a04246b6fa02cbdd92e361ab65049560e402ae0728dc9ac09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710459"
---
# <a name="ribboncontextualtabs-property"></a>Propriété Ribbon. ContextualTabs

Représente un conteneur pour les onglets contextuels.

## <a name="usage"></a>Usage

``` syntax
<Ribbon.ContextualTabs>
  child elements
</Ribbon.ContextualTabs>
```

## <a name="attributes"></a>Attributs

Il n’y a pas d’attributs.

## <a name="child-elements"></a>Éléments enfants



| Élément                                                       | Description                                     |
|---------------------------------------------------------------|-------------------------------------------------|
| [**TabGroup**](windowsribbon-element-tabgroup.md)<br/> | Doit se produire au moins une fois<br/> <br/> |



## <a name="parent-elements"></a>Éléments parents



| Élément                                                   |
|-----------------------------------------------------------|
| [**Ruban**](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a>Remarques

Facultatif.

Peut se produire au plus une fois pour chaque [**ruban**](windowsribbon-element-ribbon.md).

Les onglets contextuels sont utiles pour afficher des fonctionnalités qui s’appliquent uniquement à un contexte d’application spécifique, tel qu’un onglet de mise en forme d’image dans un éditeur de texte qui s’affiche uniquement quand une image est mise en surbrillance. En général, les onglets contextuels ne sont pas visibles tant qu’un contexte d’application spécifique n’a pas été spécifié et que l’application notifie l’infrastructure du ruban.

Quand ils sont affichés, les onglets contextuels sont codés par couleur pour les différencier des onglets normaux.

## <a name="examples"></a>Exemples

L’exemple suivant illustre le balisage de base pour l’élément **Ribbon. ContextualTabs** .

Cette section de code illustre une déclaration de commande [**TabGroup**](windowsribbon-element-tabgroup.md) et deux déclarations de commande d' [**onglet**](windowsribbon-element-tab.md) contextuelles.


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



Cette section de code illustre la déclaration de contrôle **Ribbon. ContextualTabs** avec un [**TabGroup**](windowsribbon-element-tabgroup.md) et deux contrôles d' [**onglet**](windowsribbon-element-tab.md) contextuels.


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



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>              |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Ruban. tabulations**](windowsribbon-element-ribbon-tabs.md)
</dt> </dl>

 

 





