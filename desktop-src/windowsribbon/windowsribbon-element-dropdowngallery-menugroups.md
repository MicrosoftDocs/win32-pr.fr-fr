---
title: DropDownGallery. MenuGroups, propriété
description: Représente un conteneur pour un ensemble d’éléments de menu déroulants dans un contrôle de Galerie de Drop-Down.
ms.assetid: 594f6ae5-760e-456d-98cd-04ecae0bae99
keywords:
- DropDownGallery. MenuGroups, propriété Windows ruban
topic_type:
- apiref
api_name:
- DropDownGallery.MenuGroups
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67fcaeb81020cf4c317bf065c25a770d2a77e21f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127521156"
---
# <a name="dropdowngallerymenugroups-property"></a>DropDownGallery. MenuGroups, propriété

Représente un conteneur pour un ensemble d’éléments de menu déroulants dans un contrôle de [Galerie](windowsribbon-controls-dropdowngallery.md) déroulante.

## <a name="usage"></a>Usage

``` syntax
<DropDownGallery.MenuGroups>
  child elements
</DropDownGallery.MenuGroups>
```

## <a name="attributes"></a>Attributs

Il n’y a pas d’attributs.

## <a name="child-elements"></a>Éléments enfants



| Élément                                                         | Description                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [**MenuGroup**](windowsribbon-element-menugroup.md)<br/> | Doit se produire au moins une fois<br/> <br/> |



## <a name="parent-elements"></a>Éléments parents



| Élément                                                                     |
|-----------------------------------------------------------------------------|
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/> |



## <a name="remarks"></a>Notes

Obligatoire.

Doit se produire une seule fois pour chaque élément [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) .

## <a name="examples"></a>Exemples

L’exemple suivant illustre le balisage de base pour l’élément **DropDownGallery. MenuGroups** .

Cette section de code illustre la déclaration de contrôle **DropDownGallery. MenuGroups** dans un espace de commandes de [la Galerie déroulante](windowsribbon-controls-dropdowngallery.md) .


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



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>              |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Contrôle de la Galerie déroulante**](windowsribbon-element-dropdowngallery.md)
</dt> <dt>

[Utilisation des galeries](ribbon-controls-galleries.md)
</dt> </dl>

 

 





