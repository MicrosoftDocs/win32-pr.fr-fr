---
title: Propriété String.Id
description: Représente l’ID unique d’une ressource de type chaîne.
ms.assetid: 393da279-bdf6-4796-a546-1931cbe49113
keywords:
- String.Id, propriété Windows ruban
topic_type:
- apiref
api_name:
- String.Id
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15f9c1af4ba32982ce52ba470f6b3d1996abe11c81bdd520a4e50203adb56093
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119441649"
---
# <a name="stringid-property"></a>Propriété String.Id

Représente l’ID unique d’une ressource de type chaîne.

## <a name="usage"></a>Usage

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



## <a name="remarks"></a>Remarques

Facultatif.

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
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>              |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/> |



 

 





