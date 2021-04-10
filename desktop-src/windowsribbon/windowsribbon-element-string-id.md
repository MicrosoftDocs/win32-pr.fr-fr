---
title: Propriété String.Id
description: Représente l’ID unique d’une ressource de type chaîne.
ms.assetid: 393da279-bdf6-4796-a546-1931cbe49113
keywords:
- Ruban Windows de la propriété String.Id
topic_type:
- apiref
api_name:
- String.Id
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c3ab87327ed4f11a901fb8a201e72137ab62c7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105622"
---
# <a name="stringid-property"></a>Propriété String.Id

Représente l’ID unique d’une ressource de type chaîne.

## <a name="usage"></a>Utilisation

``` syntax
<String.Id/>
```

## <a name="attributes"></a>Attributs

Il n’y a pas d’attributs.

## <a name="child-elements"></a>Éléments enfants

Il n’y a pas d’éléments enfants.

## <a name="parent-elements"></a>Éléments parents



| Élément                                                   |
|-----------------------------------------------------------|
| [**String**](windowsribbon-element-string.md)<br/> |



## <a name="remarks"></a>Notes

Optionnel.

Peut se produire au plus une fois pour chaque élément de [**chaîne**](windowsribbon-element-string.md) .

La valeur de **String.ID** doit être unique.

L’ID est associé à une définition de chaîne dans le fichier d’en-tête du ruban, par exemple `#define strSave 59999` .

Cet élément contient une valeur de l’Union de types *XS : positiveInteger* et *XS : String*. La valeur est restreinte à une valeur entière comprise entre 2 et 59999, inclusive, ou 0X2 et 0xea5f en hexadécimal, inclus.

La longueur maximale est de 10 caractères avec des zéros non significatifs facultatifs.

## <a name="examples"></a>Exemples

L’exemple suivant illustre le balisage pour un élément [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) avec une déclaration **String.ID** .


```XML
<Command.LabelTitle>
  <String>
    <String.Content>Label for Save</String.Content>
    <String.Id>59999</String.Id>
    <String.Symbol>strSave</String.Symbol>
  </String>
</Command.LabelTitle>
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/> |



 

 





