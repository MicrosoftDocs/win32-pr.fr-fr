---
title: Élément String
description: Représente une ressource de type chaîne.
ms.assetid: 83e5bdbb-ef86-4942-af40-2e327360ee67
keywords:
- élément String Windows ruban
topic_type:
- apiref
api_name:
- String
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a34a417b6ad4d57bea83fcae13d810b22114271
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122630955"
---
# <a name="string-element"></a>Élément String

Représente une ressource de type chaîne.

## <a name="usage"></a>Utilisation

``` syntax
<String
  Content = "xs:string"
  Id = "xs:positiveInteger or xs:string"
  Symbol = "xs:string">
  child elements
</String>
```

## <a name="attributes"></a>Attributs



<table>
<colgroup>
<col  />
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Attribut</th>
<th>Type</th>
<th>Obligatoire</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Contenu</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td><dt><span></span><span></span><strong></strong> (XS : String)<br/> </dt> <dd> Chaîne composée de toute séquence de caractères, y compris les espaces blancs et les sauts de ligne.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Id</strong><br/></td>
<td>XS : positiveInteger ou XS : String<br/></td>
<td>No<br/></td>
<td>ID de ressource unique. <br/> <br/>
<dt><span></span><span></span><strong></strong> (XS : positiveInteger ou XS : String)<br/> </dt> <dd> Valeur entière comprise entre 2 et 59999, inclusive, ou 0X2 et 0xea5f en hexadécimal, inclus. <br/> La longueur maximale est de 10 caractères, y compris des zéros non significatifs facultatifs. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Symbole</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Symbole de ressource pour la chaîne.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS : String)<br/> </dt> <dd> Une lettre ou un trait de soulignement suivi d’une séquence de lettres, de chiffres ou de traits de soulignement.<br/> La longueur maximale est de 100 caractères.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Éléments enfants



| Élément                                                                   | Description                                   |
|---------------------------------------------------------------------------|-----------------------------------------------|
| [**String. Content**](windowsribbon-element-string-content.md)<br/> | Peut se produire au plus une fois<br/> <br/> |
| [**String.Id**](windowsribbon-element-string-id.md)<br/>           | Peut se produire au plus une fois<br/> <br/> |
| [**String. Symbol**](windowsribbon-element-string-symbol.md)<br/>   | Peut se produire au plus une fois<br/> <br/> |



## <a name="parent-elements"></a>Éléments parents



| Élément                                                                                           |
|---------------------------------------------------------------------------------------------------|
| [**Commande. KeyTip**](windowsribbon-element-command-keytip.md)<br/>                         |
| [**Commande. LabelDescription**](windowsribbon-element-command-labeldescription.md)<br/>     |
| [**Commande. LabelTitle**](windowsribbon-element-command-labeltitle.md)<br/>                 |
| [**Commande. TooltipDescription**](windowsribbon-element-command-tooltipdescription.md)<br/> |
| [**Commande. TooltipTitle**](windowsribbon-element-command-tooltiptitle.md)<br/>             |



## <a name="remarks"></a>Remarques

Optionnel.

Peut se produire au plus une fois pour chaque élément [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md), [**Command. LabelDescription**](windowsribbon-element-command-labeldescription.md), [**Command. KeyTip**](windowsribbon-element-command-keytip.md), [**Command. TooltipTitle**](windowsribbon-element-command-tooltiptitle.md)ou [**Command. TooltipDescription**](windowsribbon-element-command-tooltipdescription.md) .

La définition de chaîne est ajoutée au fichier d’en-tête du ruban, par exemple `#define strSave 59999` .

La chaîne est ajoutée à une table de chaînes dans le fichier de ressources du ruban où un nom et un ID sont générés par l’infrastructure du ruban si aucun n’est déclaré.

## <a name="examples"></a>Exemples

L’exemple suivant illustre le balisage pour un élément [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) avec une déclaration de **chaîne** .


```XML
<Command.LabelTitle>
  <String>
    <String.Content>Label for Save</String.Content>
    <String.Id>59999</String.Id>
    <String.Symbol>strSave</String.Symbol>
  </String>
</Command.LabelTitle>
```



## <a name="element-information"></a>Informations sur les éléments

- **système minimal pris en charge**: Windows 7 
- **Peut être vide**: non



 

 





