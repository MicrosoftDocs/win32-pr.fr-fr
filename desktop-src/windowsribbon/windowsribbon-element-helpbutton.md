---
title: Élément HelpButton
description: Représente le contrôle de bouton d’aide.
ms.assetid: 24c709da-539e-4ea0-bd3e-d3fbd72dfb97
keywords:
- Ruban des fenêtres d’élément HelpButton
topic_type:
- apiref
api_name:
- HelpButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5be084ff6fc92d4eac4bbaffb3c507142f91eba8
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2020
ms.locfileid: "106511270"
---
# <a name="helpbutton-element"></a>Élément HelpButton

Représente le contrôle de [bouton d’aide](windowsribbon-controls-helpbutton.md) .

## <a name="usage"></a>Utilisation

``` syntax
<HelpButton
  CommandName = "xs:positiveInteger or xs:string"/>
```

## <a name="attributes"></a>Attributs



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
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
<td><strong>CommandName</strong><br/></td>
<td>XS : positiveInteger ou XS : String<br/></td>
<td>Non<br/></td>
<td>Associe l’élément à une <a href="windowsribbon-element-command.md"><strong>commande</strong></a>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS : positiveInteger ou XS : String)<br/> </dt> <dd> Chaîne, valeur entière comprise entre 2 et 59999, inclusive, ou valeur hexadécimale comprise entre 0X2 et 0xea5f inclus. <br/> La valeur doit être unique dans le document XML du ruban. <br/> Longueur maximale : 100 caractères. <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Éléments enfants

Il n’y a pas d’éléments enfants.

## <a name="parent-elements"></a>Éléments parents



| Élément                                                                         |
|---------------------------------------------------------------------------------|
| [**Ruban. HelpButton**](windowsribbon-element-ribbon-helpbutton.md)<br/> |



## <a name="remarks"></a>Notes

Optionnel.

Peut se produire au plus une fois pour chaque [**ruban. HelpButton**](windowsribbon-element-ribbon-helpbutton.md).

Ouvre une boîte de dialogue d’aide sur l’application lorsque vous cliquez dessus.

## <a name="examples"></a>Exemples

L’exemple suivant illustre le balisage de base requis pour implémenter un contrôle de [bouton d’aide](windowsribbon-controls-helpbutton.md) du ruban.

Cette section de code affiche la déclaration de commande **HelpButton** .


```XML
<Command Name="cmdHelp"
         Symbol="IDR_CMD_HELP">      
</Command>
```



Cette section de code illustre la déclaration de contrôle **HelpButton** .


```XML
<Ribbon.HelpButton>
  <HelpButton CommandName="cmdHelp"/>
</Ribbon.HelpButton>
```



## <a name="element-information"></a>Informations sur les éléments



|                                     |           |
|-------------------------------------|-----------|
| Système minimal pris en charge<br/> | Windows 7 |
| Peut être vide                        | Oui       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Contrôle de bouton d’aide](windowsribbon-controls-helpbutton.md)
</dt> </dl>

 

 





