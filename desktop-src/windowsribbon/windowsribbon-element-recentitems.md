---
title: Élément RecentItems
description: Représente le contrôle éléments récents dans le menu de l’application.
ms.assetid: a3df0bb0-e0f8-413a-879d-8e39164535d0
keywords:
- élément RecentItems Windows ruban
topic_type:
- apiref
api_name:
- RecentItems
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6ae49864fea057aa942b121f21813acfd0f26c6cc4411d4f1b3c59cda12014c3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119881559"
---
# <a name="recentitems-element"></a>Élément RecentItems

Représente le contrôle [éléments récents](windowsribbon-controls-recentitems.md) dans le [menu](windowsribbon-controls-applicationmenu.md)de l’application.

## <a name="usage"></a>Usage

``` syntax
<RecentItems
  CommandName = "xs:positiveInteger or xs:string"
  MaxCount = "xs:nonNegativeInteger"
  EnablePinning = "Boolean"/>
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
<tr class="even">
<td><strong>EnablePinning</strong><br/></td>
<td>Boolean<br/></td>
<td>Non<br/></td>
<td>Limité à l’une des valeurs suivantes (0 et 1 ne sont pas valides) :<br/> <br/>
<dt><span></span><span></span><strong></strong> :<br/> </dt> <dd> Par défaut. <br/> </dd> <dt><span></span><span></span><strong></strong> fausses<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>MaxCount</strong><br/></td>
<td>xs:nonNegativeInteger<br/></td>
<td>Non<br/></td>
<td>Nombre d’éléments récents à afficher.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS : nonNegativeInteger)<br/> </dt> <dd> Valeur entière égale ou supérieure à 0.<br/> La valeur par défaut est <strong>10</strong>.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Éléments enfants

Il n’y a pas d’éléments enfants.

## <a name="parent-elements"></a>Éléments parents



| Élément                                                                                             |
|-----------------------------------------------------------------------------------------------------|
| [**ApplicationMenu.RecentItems**](windowsribbon-element-applicationmenu-recentitems.md)<br/> |



## <a name="remarks"></a>Remarques

Obligatoire.

Doit se produire une seule fois pour chaque élément [**ApplicationMenu. RecentItems**](windowsribbon-element-applicationmenu-recentitems.md) .

Le contrôle [éléments récents](windowsribbon-controls-recentitems.md) affiche la liste des éléments utilisés le plus récemment (MRU) de l’application ruban.

## <a name="examples"></a>Exemples

L’exemple suivant illustre le balisage de base pour le contrôle d' [éléments récents](windowsribbon-controls-recentitems.md) .

L’exemple suivant illustre une déclaration de commande **RecentItems** .


```XML
<!-- Command declaration for most recently used items. -->
<Command Name="cmdMRUItems"
         Symbol="ID_FILE_MRUITEMS"
         Id="25050"/>
```



L’exemple suivant illustre la déclaration de contrôles **RecentItems** associée.


```XML
<!-- Most recently used items collection. -->
<ApplicationMenu.RecentItems>
  <RecentItems CommandName="cmdMRUItems"/>
</ApplicationMenu.RecentItems>
```



## <a name="element-information"></a>Informations sur les éléments

* **système minimal pris en charge**: Windows 7
* **Peut être vide**: Oui


## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Contrôle de menu de l’application](windowsribbon-controls-applicationmenu.md)
</dt> <dt>

[Contrôle des éléments récents](windowsribbon-controls-recentitems.md)
</dt> </dl>

 

 





