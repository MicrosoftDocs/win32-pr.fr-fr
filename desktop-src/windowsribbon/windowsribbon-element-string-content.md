---
title: Propriété String. Content
description: Représente le contenu d’une ressource de type chaîne.
ms.assetid: 86f34cdc-1311-4f52-979f-201d71bbb9e9
keywords:
- propriété String. Content Windows ruban
topic_type:
- apiref
api_name:
- String.Content
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 526062956c6ab7498caac8712ba932d6e7ac1f2dd6307359183d2529e35fc8a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118439504"
---
# <a name="stringcontent-property"></a>Propriété String. Content

Représente le contenu d’une ressource de type chaîne.

## <a name="usage"></a>Usage

``` syntax
<String.Content/>
```

## <a name="attributes"></a>Attributs

Il n’y a pas d’attributs.

## <a name="child-elements"></a>Éléments enfants

Il n’y a pas d’éléments enfants.

## <a name="parent-elements"></a>Éléments parents



| Élément                                                   |
|-----------------------------------------------------------|
| [**Chaîne**](windowsribbon-element-string.md)<br/> |



## <a name="remarks"></a>Remarques

Facultatif.

Peut se produire au plus une fois pour chaque élément de [**chaîne**](windowsribbon-element-string.md) .

Cet élément contient une valeur de type *XS : String*. La valeur est limitée à une chaîne composée d’une séquence de caractères, y compris des espaces blancs et des sauts de ligne.

La longueur maximale est illimitée.

## <a name="examples"></a>Exemples

L’exemple suivant illustre le balisage pour un élément [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) avec une déclaration **String. Content** .


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



 

 





