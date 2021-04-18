---
title: Élément ApplicationMenu
description: Représente le menu de l’application. | Élément ApplicationMenu
ms.assetid: 815e0462-ea45-44b1-81bf-f5797b22e920
keywords:
- Ruban des fenêtres d’élément ApplicationMenu
topic_type:
- apiref
api_name:
- ApplicationMenu
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a02193b4c3e61b4b8cf2f129619969f6a82a84ac
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104211526"
---
# <a name="applicationmenu-element"></a>Élément ApplicationMenu

Représente le [menu](windowsribbon-controls-applicationmenu.md)de l’application.

## <a name="usage"></a>Utilisation

``` syntax
<ApplicationMenu
  CommandName = "xs:positiveInteger or xs:string"
>
  child elements
</ApplicationMenu>
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



| Élément                                                                                             | Description                                        |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [**ApplicationMenu.RecentItems**](windowsribbon-element-applicationmenu-recentitems.md)<br/> | Peut se produire au plus une fois<br/> <br/>      |
| [**MenuGroup**](windowsribbon-element-menugroup.md)<br/>                                     | Peut se produire une ou plusieurs fois<br/> <br/> |



## <a name="parent-elements"></a>Éléments parents



| Élément                                                                                   |
|-------------------------------------------------------------------------------------------|
| [**Ruban. ApplicationMenu**](windowsribbon-element-ribbon-applicationmenu.md)<br/> |



## <a name="remarks"></a>Notes

Obligatoire.

Doit se produire une seule fois pour chaque [**ruban. ApplicationMenu**](windowsribbon-element-ribbon-applicationmenu.md).

Les éléments enfants de l’élément **ApplicationMenu** doivent se produire dans l’ordre spécifié :

1.  [**ApplicationMenu.RecentItems**](windowsribbon-element-applicationmenu-recentitems.md)
2.  [**MenuGroup**](windowsribbon-element-menugroup.md)

## <a name="examples"></a>Exemples

L’exemple suivant illustre le balisage de base pour le menu de l' [application](windowsribbon-controls-applicationmenu.md).

Cette section de code montre les déclarations de commande **ApplicationMenu** .


```XML
<!-- Command declarations for the Application Menu. -->
<Command Name="cmdFileMenu"
         Symbol="ID_FILE_MENU"
         Id="25000" />
<!-- Command declaration for most recently used items. -->
<Command Name="cmdMRUItems"
         Symbol="ID_FILE_MRUITEMS"
         Id="25050"/>
<!-- Command declarations for Application Menu items. -->
<Command Name="cmdNew"
         Symbol="ID_FILE_NEW"
         Comment="New"
         Id="25001"
         LabelTitle="&amp;New"/>
<Command Name="cmdOpen"
         Symbol="ID_FILE_OPEN"
         Comment="Open"
         Id="25002"
         LabelTitle="&amp;&amp;Open"/>
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
<Command Name="cmdPrint"
         Symbol="ID_FILE_PRINT"
         Comment="Save"
         Id="25004"
         LabelTitle="Print" />
<Command Name="cmdExit"
         Symbol="ID_FILE_EXIT"
         Comment="Exit"
         Id="25005"
         LabelTitle="Exit" />
```



Cette section de code montre les déclarations de contrôle **ApplicationMenu** .


```XML
<!-- Control declarations for Application Menu items. -->
<Ribbon.ApplicationMenu>
  <ApplicationMenu CommandName="cmdFileMenu">
    <!-- Most recently used items collection. -->
    <ApplicationMenu.RecentItems>
      <RecentItems CommandName="cmdMRUItems"/>
    </ApplicationMenu.RecentItems>
    <!-- Menu items collection. -->
    <MenuGroup>
      <Button CommandName="cmdNew" />
      <Button CommandName="cmdOpen" />
      <Button CommandName="cmdSave" />
    </MenuGroup>
    <MenuGroup>
      <Button CommandName="cmdPrint" />
      <Button CommandName="cmdExit" />
    </MenuGroup>
  </ApplicationMenu>
</Ribbon.ApplicationMenu>
```



## <a name="element-information"></a>Informations sur les éléments



|                                     |           |
|-------------------------------------|-----------|
| Système minimal pris en charge<br/> | Windows 7 |
| Peut être vide                        | Non        |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Contrôle de menu de l’application](windowsribbon-controls-applicationmenu.md)
</dt> </dl>

 

 





