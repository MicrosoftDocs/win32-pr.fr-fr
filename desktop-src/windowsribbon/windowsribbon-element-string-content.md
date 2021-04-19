---
title: Propriété String. Content
description: Représente le contenu d’une ressource de type chaîne.
ms.assetid: 86f34cdc-1311-4f52-979f-201d71bbb9e9
keywords:
- Propriété String. Content du ruban Windows
topic_type:
- apiref
api_name:
- String.Content
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8912264e4f55568c190212227d2e305f9d676a1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511140"
---
# <a name="stringcontent-property"></a>Propriété String. Content

Représente le contenu d’une ressource de type chaîne.

## <a name="usage"></a>Utilisation

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
| [**String**](windowsribbon-element-string.md)<br/> |



## <a name="remarks"></a>Notes

Optionnel.

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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/> |



 

 





