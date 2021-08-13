---
title: SplitButtonGallery. MenuGroups, propriété
description: Représente un conteneur pour un ensemble d’éléments de menu déroulant dans un contrôle SplitButtonGallery.
ms.assetid: e30fcf9a-488b-423a-8bc4-fccbc78f74de
keywords:
- SplitButtonGallery. MenuGroups, propriété Windows ruban
topic_type:
- apiref
api_name:
- SplitButtonGallery.MenuGroups
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 931a66ffca192a1655f3eeffc405c4c02c8e298c28fe9cb9d0d8c6612e29d793
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119441718"
---
# <a name="splitbuttongallerymenugroups-property"></a>SplitButtonGallery. MenuGroups, propriété

Représente un conteneur pour un ensemble d’éléments de menu déroulant dans un contrôle [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .

## <a name="usage"></a>Usage

``` syntax
<SplitButtonGallery.MenuGroups>
  child elements
</SplitButtonGallery.MenuGroups>
```

## <a name="attributes"></a>Attributs

Il n’y a pas d’attributs.

## <a name="child-elements"></a>Éléments enfants



| Élément                                                         | Description                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [**MenuGroup**](windowsribbon-element-menugroup.md)<br/> | Doit se produire au moins une fois<br/> <br/> |



## <a name="parent-elements"></a>Éléments parents



| Élément                                                                           |
|-----------------------------------------------------------------------------------|
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a>Remarques

Obligatoire.

Doit se produire une seule fois pour chaque élément [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .

## <a name="examples"></a>Exemples

L’exemple suivant illustre le balisage de base pour l’élément **SplitButtonGallery. MenuGroups** .

Cette section de code illustre la déclaration de contrôle **SplitButtonGallery. MenuGroups** .


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

 

 





