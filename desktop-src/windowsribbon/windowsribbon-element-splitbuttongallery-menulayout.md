---
title: SplitButtonGallery. MenuLayout, propriété
description: Représente un conteneur pour les dispositions des menus déroulants de la Galerie de boutons partagés.
ms.assetid: 4bebdff6-16ea-4cf3-adc7-9b86ea200e81
keywords:
- SplitButtonGallery. MenuLayout, propriété Windows ruban
topic_type:
- apiref
api_name:
- SplitButtonGallery.MenuLayout
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f40cf184d6122fc40041cfb77953bba2b7950d9d1a957d99aae659633ee5c194
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118706897"
---
# <a name="splitbuttongallerymenulayout-property"></a>SplitButtonGallery. MenuLayout, propriété

Représente un conteneur pour les dispositions des menus déroulants de la [Galerie de boutons partagés](windowsribbon-controls-splitbuttongallery.md) .

## <a name="usage"></a>Usage

``` syntax
<SplitButtonGallery.MenuLayout>
  child elements
</SplitButtonGallery.MenuLayout>
```

## <a name="attributes"></a>Attributs

Il n’y a pas d’attributs.

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                           | Description                                    |
|-----------------------------------------------------------------------------------|------------------------------------------------|
| [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md)<br/>         | Doit se produire exactement une fois<br/> <br/> |
| [**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md)<br/> | Doit se produire exactement une fois<br/> <br/> |



## <a name="parent-elements"></a>Éléments parents



| Élément                                                                           |
|-----------------------------------------------------------------------------------|
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a>Remarques

Facultatif.

Peut se produire au plus une fois pour chaque élément [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .

> [!Note]  
> Un seul élément enfant ([**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) ou [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md)) est autorisé.

 

## <a name="examples"></a>Exemples

L’exemple suivant illustre le balisage de base pour la [bibliothèque de boutons partagés](windowsribbon-controls-splitbuttongallery.md).

Cette section de code illustre la déclaration de contrôle **SplitButtonGallery. MenuLayout** .


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



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>              |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Contrôle de la Galerie des boutons partagés](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[Utilisation des galeries](ribbon-controls-galleries.md)
</dt> </dl>

 

 





