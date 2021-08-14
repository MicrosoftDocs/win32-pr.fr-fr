---
title: Propriété Ribbon. SizeDefinitions
description: Représente un conteneur pour les modèles de disposition personnalisés des contrôles du ruban.
ms.assetid: 1f5fcffc-7f2e-4763-b0a7-4e8f46534da8
keywords:
- ruban. SizeDefinitions, propriété Windows ruban
topic_type:
- apiref
api_name:
- Ribbon.SizeDefinitions
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24f3109c7e9f709267310415b48238b24050c7531bc0f784290876ab47706d6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118202255"
---
# <a name="ribbonsizedefinitions-property"></a>Propriété Ribbon. SizeDefinitions

Représente un conteneur pour les modèles de disposition personnalisés des contrôles du ruban.

## <a name="usage"></a>Usage

``` syntax
<Ribbon.SizeDefinitions>
  child elements
</Ribbon.SizeDefinitions>
```

## <a name="attributes"></a>Attributs

Il n’y a pas d’attributs.

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                   | Description                                        |
|---------------------------------------------------------------------------|----------------------------------------------------|
| [**SizeDefinition**](windowsribbon-element-sizedefinition.md)<br/> | Peut se produire une ou plusieurs fois<br/> <br/> |



## <a name="parent-elements"></a>Éléments parents



| Élément                                                   |
|-----------------------------------------------------------|
| [**Ruban**](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a>Remarques

Facultatif.

Peut se produire au plus une fois pour chaque [**ruban**](windowsribbon-element-ribbon.md).

## <a name="examples"></a>Exemples

L’exemple de code suivant illustre un modèle personnalisé de base.


```
<Ribbon.SizeDefinitions>
  <SizeDefinition Name="CustomTemplate">
    <GroupSizeDefinition Size="Large">
      <ControlSizeDefinition ImageSize="Large" IsLabelVisible="true" />
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Medium">
      <ControlSizeDefinition ImageSize="Small" IsLabelVisible="false" />
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Small">
      <ControlSizeDefinition ImageSize="Small" IsLabelVisible="false" />
    </GroupSizeDefinition>
  </SizeDefinition>
</Ribbon.SizeDefinitions>
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>              |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Personnalisation d’un ruban à l’aide de définitions de taille et de stratégies de mise à l’échelle](windowsribbon-templates.md)
</dt> </dl>

 

 





