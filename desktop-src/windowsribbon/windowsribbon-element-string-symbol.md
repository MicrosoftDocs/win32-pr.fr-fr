---
title: String. Symbol, propriété
description: Représente le nom d’une ressource de type chaîne.
ms.assetid: 7c1d0197-2c9b-4f42-afba-73fd1c366deb
keywords:
- propriété String. Symbol Windows ruban
topic_type:
- apiref
api_name:
- String.Symbol
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe6c071461fcdeb5f2bbbdbb15fce0f3f6e6031edddf4bd18e034416ba8c49e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118706860"
---
# <a name="stringsymbol-property"></a>String. Symbol, propriété

Représente le nom d’une ressource de type chaîne.

## <a name="usage"></a>Usage

``` syntax
<String.Symbol/>
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

Le symbole est associé à une définition de chaîne dans le fichier d’en-tête du ruban, par exemple `#define strSave 59999` .

Cet élément contient une valeur de type *XS : String*. La valeur est conformée en une chaîne composée d’une lettre ou d’un trait de soulignement suivi d’une séquence de lettres, de chiffres ou de traits de soulignement.

La longueur maximale est de 100 caractères.

## <a name="examples"></a>Exemples

L’exemple suivant illustre le balisage pour un élément [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) avec une déclaration **String. Symbol** .


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



 

 





