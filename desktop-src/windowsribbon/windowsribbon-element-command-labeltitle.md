---
title: Command. LabelTitle, propriété
description: Représente le titre d’une étiquette.
ms.assetid: 97378ec3-7988-4e39-9cf5-c382b246c5c9
keywords:
- Ruban Windows de la propriété Command. LabelTitle
topic_type:
- apiref
api_name:
- Command.LabelTitle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed6d6c72ddd60cca63834fdcf21cf8f8b726ad22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509182"
---
# <a name="commandlabeltitle-property"></a>Command. LabelTitle, propriété

Représente le titre d’une étiquette.

## <a name="usage"></a>Utilisation

``` syntax
<Command.LabelTitle>
  child elements
</Command.LabelTitle>
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



## <a name="remarks"></a>Notes

Optionnel.

Peut se produire au plus une fois pour chaque [**commande**](windowsribbon-element-command.md).

**Command. LabelTitle** peut contenir une valeur de type *XS : String* limitée à toute séquence de caractères, y compris les espaces blancs et les sauts de ligne.

> [!Note]  
> Utilisez la référence de caractère XML UCS (Universal Character Set) `&#xA;` pour spécifier un saut de ligne.

 

La longueur maximale est illimitée.

Si aucune valeur n’est fournie pour **Command. LabelTitle**, l’élément enfant [**String**](windowsribbon-element-string.md) est requis.

> [!Note]  
> Si **Command. LabelTitle** contient à la fois une valeur et un élément enfant de [**chaîne**](windowsribbon-element-string.md) , la **chaîne** est prioritaire.

 

**Command. LabelTitle** prend uniquement en charge l’alignement à gauche.

Si une commande est exposée à l’aide d’un élément de menu et que la valeur de **Command. LabelTitle** ou de l' [ \_ \_ étiquette de l’interface utilisateur](windowsribbon-reference-properties-uipkey-label.md) contient une lettre précédée d’une esperluette, comme indiqué dans l’exemple suivant, cette lettre est traitée comme une touche d’accès et une touche d’accès rapide pour cette commande par l’infrastructure du ruban.


```XML
<Command Name="cmdNew"
         Symbol="ID_FILE_NEW"
         Comment="New"
         Id="25001"
         LabelTitle="&amp;New"/>
```



Pour afficher une esperluette dans une étiquette, échappez la désignation de caractères spéciaux par une double esperluette ( `&&` ), comme illustré dans l’exemple suivant.


```XML
<Command Name="cmdOpen"
         Symbol="ID_FILE_OPEN"
         Comment="Open"
         Id="25002"
         LabelTitle="&amp;&amp;Open"/>
```



## <a name="examples"></a>Exemples

L’exemple suivant illustre le balisage pour un élément [**Command**](windowsribbon-element-command.md) avec une déclaration **Command. LabelTitle** .


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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[\_Étiquette de nom de l’interface utilisateur \_](windowsribbon-reference-properties-uipkey-label.md)
</dt> </dl>

 

 





