---
title: Élément Ribbon
description: Représente le contrôle de ruban dans la vue du ruban.
ms.assetid: 51083180-4e86-4c90-9fd1-a58c12bcc756
keywords:
- ruban Windows élément de ruban
topic_type:
- apiref
api_name:
- Ribbon
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 70841866ec656dc840fb467d598cc42bf919283b
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122630915"
---
# <a name="ribbon-element"></a>Élément Ribbon

Représente le contrôle de ruban dans la vue du ruban.

## <a name="usage"></a>Utilisation

``` syntax
<Ribbon
  Name = "xs:string"
  GroupSpacing = "xs:string">
  child elements
</Ribbon>
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
<td><strong>GroupSpacing</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td><dt><span></span><span></span><strong></strong> Small<br/> </dt> <dd> Par défaut. <br/> </dd> <dt><span></span><span></span><strong></strong> Médias<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Conséquent<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Nom</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Utilisé pour annoter l’élément Command.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS : String)<br/> </dt> <dd> Toute séquence de zéro ou plusieurs caractères.<br/> La longueur maximale est illimitée.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Éléments enfants



| Élément                                                                                         | Description                                   |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [**Ruban. ApplicationMenu**](windowsribbon-element-ribbon-applicationmenu.md)<br/>       | Peut se produire au plus une fois<br/> <br/> |
| [**Ruban. ContextualTabs**](windowsribbon-element-ribbon-contextualtabs.md)<br/>         | Peut se produire au plus une fois<br/> <br/> |
| [**Ruban. HelpButton**](windowsribbon-element-ribbon-helpbutton.md)<br/>                 | Peut se produire au plus une fois<br/> <br/> |
| [**Ruban. QuickAccessToolbar**](windowsribbon-element-ribbon-quickaccesstoolbar.md)<br/> | Peut se produire au plus une fois<br/> <br/> |
| [**Ruban. SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md)<br/>       | Peut se produire au plus une fois<br/> <br/> |
| [**Ruban. tabulations**](windowsribbon-element-ribbon-tabs.md)<br/>                             | Peut se produire au plus une fois<br/> <br/> |



## <a name="parent-elements"></a>Éléments parents



| Élément                                                                         |
|---------------------------------------------------------------------------------|
| [**Application. views**](windowsribbon-element-application-views.md)<br/> |



## <a name="remarks"></a>Remarques

Obligatoire.

Doit se produire exactement une fois pour chaque élément [**application. views**](windowsribbon-element-application-views.md) .

## <a name="examples"></a>Exemples

L’exemple suivant illustre le balisage de base pour une vue de **ruban** .


```XML
<Ribbon Name="ScenicRibbonSampleApp">
  <Ribbon.QuickAccessToolbar>
  ...
  </Ribbon.QuickAccessToolbar>
  <Ribbon.ApplicationMenu>
  ...
  </Ribbon.ApplicationMenu>
  <Ribbon.SizeDefinitions>
  ...
  </Ribbon.SizeDefinitions>
  <Ribbon.Tabs>
  ...
  </Ribbon.Tabs>
  <Ribbon.ContextualTabs>
  ...
  </Ribbon.ContextualTabs>
  <Ribbon.HelpButton>
  ...
  </Ribbon.HelpButton>
</Ribbon>
```



## <a name="element-information"></a>Informations sur les éléments




* **système minimal pris en charge**: Windows 7
* **Peut être vide**: non



 

 





