---
title: Command. Symbol, propriété
description: Représente le nom d’une commande qui peut être référencée en externe.
ms.assetid: affa5f3f-f641-4bec-9165-6102509cf355
keywords:
- propriété Command. Symbol Windows ruban
topic_type:
- apiref
api_name:
- Command.Symbol
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b88dccb71a90feca7348ca9731ca5966b012c9c0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404746"
---
# <a name="commandsymbol-property"></a>Command. Symbol, propriété

Représente le nom d’une [**commande**](windowsribbon-element-command.md) qui peut être référencée en externe.

## <a name="usage"></a>Usage

``` syntax
<Command.Symbol/>
```

## <a name="attributes"></a>Attributs

Il n’y a pas d’attributs.

## <a name="child-elements"></a>Éléments enfants

Il n’y a pas d’éléments enfants.

## <a name="parent-elements"></a>Éléments parents



| Élément                                                     |
|-------------------------------------------------------------|
| [**Commande**](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a>Notes

facultatif.

Peut se produire au plus une fois pour chaque [**commande**](windowsribbon-element-command.md).

Le symbole est associé à une définition de commande dans le fichier d’en-tête du ruban, par exemple `#define cmdSave 25003 /* Save */` .

Cet élément contient une valeur de type *XS : String*.

La valeur est conformée en une chaîne qui se compose d’une lettre ou d’un trait de soulignement suivi d’une séquence de lettres, de chiffres et de traits de soulignement.

La longueur maximale est de 100 caractères.

## <a name="examples"></a>Exemples

L’exemple suivant illustre le balisage pour un élément [**Command**](windowsribbon-element-command.md) avec une déclaration **Command. Symbol** .


```XML
<Command>
  <Command.Name>cmdSave</Command.Name>
  <Command.Symbol>ID_FILE_SAVE</Command.Symbol>
  <Command.Comment>Save</Command.Comment>
  <Command.Id>25003</Command.Id>
  <Command.LabelTitle>
    <String>
      <String.Content>Label for Save</String.Content>
      <String.Id>59999</String.Id>
      <String.Symbol>strSave</String.Symbol>
    </String>
  </Command.LabelTitle>
  <Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
  <Command.TooltipDescription>Tooltip description for Save Command.</Command.TooltipDescription>
  <Command.Keytip>s1</Command.Keytip>
</Command>
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>              |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/> |



 

 





