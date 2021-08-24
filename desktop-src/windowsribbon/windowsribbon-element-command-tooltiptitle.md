---
title: Command. TooltipTitle, propriété
description: Représente un titre d’info-bulle.
ms.assetid: b06a7a6a-fbdd-464b-b804-e62912d6e176
keywords:
- propriété Command. TooltipTitle Windows ruban
topic_type:
- apiref
api_name:
- Command.TooltipTitle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f9050c97980b0ffa2c2c4828a8ac1d85dfbd1a40ed8330d144db2c0d3802524
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710549"
---
# <a name="commandtooltiptitle-property"></a>Command. TooltipTitle, propriété

Représente un titre d’info-bulle.

## <a name="usage"></a>Usage

``` syntax
<Command.TooltipTitle>
  child elements
</Command.TooltipTitle>
```

## <a name="attributes"></a>Attributs

Il n’y a pas d’attributs.

## <a name="child-elements"></a>Éléments enfants



| Élément                                                   | Description                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| [**String**](windowsribbon-element-string.md)<br/> | Peut se produire au plus une fois<br/> <br/> |



## <a name="parent-elements"></a>Éléments parents



| Élément                                                     |
|-------------------------------------------------------------|
| [**Commande**](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a>Remarques

Facultatif.

Peut se produire au plus une fois pour chaque [**commande**](windowsribbon-element-command.md).

**Command. TooltipTitle** peut contenir une valeur de type *XS : String* limitée à toute séquence de caractères, y compris les espaces blancs et les sauts de ligne.

> [!Note]  
> Utilisez la référence de caractère XML UCS (Universal Character Set) `&#xA;` pour spécifier un saut de ligne.

 

La longueur maximale est illimitée.

Si aucune valeur n’est fournie pour **Command. TooltipTitle**, l’élément enfant [**String**](windowsribbon-element-string.md) est requis.

> [!Note]  
> Si **Command. TooltipTitle** contient à la fois une valeur et un élément enfant de [**chaîne**](windowsribbon-element-string.md) , la **chaîne** est prioritaire.

 

**Command. TooltipTitle** prend uniquement en charge l’alignement à gauche.

## <a name="examples"></a>Exemples

L’exemple suivant illustre le balisage pour un élément [**Command**](windowsribbon-element-command.md) avec une déclaration **Command. TooltipTitle** .


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



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>              |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[IU \_ \_ TooltipTitle](windowsribbon-reference-properties-uipkey-tooltiptitle.md)
</dt> </dl>

 

 





