---
title: InRibbonGallery. MenuGroups, propriété
description: Représente un conteneur pour le jeu d’éléments de menu déroulant d’un contrôle In-Ribbon Gallery.
ms.assetid: 6b9ded25-4e8e-4e30-a349-f7c091dbfe7a
keywords:
- InRibbonGallery. MenuGroups, propriété Windows ruban
topic_type:
- apiref
api_name:
- InRibbonGallery.MenuGroups
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1722c8963b57256cf74f5911c8273539e10b5c6a6fef96dcfa1f0fec591bca04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710479"
---
# <a name="inribbongallerymenugroups-property"></a>InRibbonGallery. MenuGroups, propriété

Représente un conteneur pour le jeu d’éléments de menu déroulant d’un contrôle [de galerie dans le ruban](windowsribbon-controls-inribbongallery.md) .

## <a name="usage"></a>Usage

``` syntax
<InRibbonGallery.MenuGroups>
  child elements
</InRibbonGallery.MenuGroups>
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
| [**InRibbonGallery**](windowsribbon-element-inribbongallery.md)<br/> |



## <a name="remarks"></a>Remarques

Facultatif.

Peut se produire au plus une fois pour chaque élément [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) .

## <a name="examples"></a>Exemples

L’exemple suivant illustre le balisage de base pour un contrôle [de galerie dans le ruban](windowsribbon-controls-inribbongallery.md) .

Cette section de code illustre la déclaration de contrôle **InRibbonGallery. MenuGroups** .


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



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>              |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Contrôle de galerie dans le ruban](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[Utilisation des galeries](ribbon-controls-galleries.md)
</dt> <dt>

[Personnalisation d’un ruban à l’aide de définitions de taille et de stratégies de mise à l’échelle](windowsribbon-templates.md)
</dt> </dl>

 

 





