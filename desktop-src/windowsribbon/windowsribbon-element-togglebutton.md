---
title: ToggleButton, élément
description: Représente un contrôle bouton bascule.
ms.assetid: f26a90e6-9e9a-4fde-8753-50b8b1d09f80
keywords:
- élément ToggleButton Windows ruban
topic_type:
- apiref
api_name:
- ToggleButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c92a5985b560738d7119a6c5de354ad703f58894
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404225"
---
# <a name="togglebutton-element"></a>ToggleButton, élément

Représente un contrôle [bouton bascule](windowsribbon-controls-togglebutton.md) .

## <a name="usage"></a>Usage

``` syntax
<ToggleButton
  CommandName = "xs:positiveInteger or xs:string"
  ApplicationDefaults.IsChecked = "Boolean"/>
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
<td><strong>ApplicationDefaults. IsChecked</strong><br/></td>
<td>Boolean<br/></td>
<td>Non<br/></td>
<td>Cet attribut est valide uniquement lorsque l’élément <strong>ToggleButton</strong> est un enfant de <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar. ApplicationDefaults</strong></a>. <br/> Limité à l’une des valeurs suivantes :<br/> <br/>
<dt><span></span><span></span><strong></strong> :<br/> </dt> <dd> Par défaut. <br/> </dd> <dt><span></span><span></span><strong></strong> fausses<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
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



| Élément                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------|
| [**ControlGroup**](windowsribbon-element-controlgroup.md)<br/>                                                     |
| [**DropDownButton**](windowsribbon-element-dropdownbutton.md)<br/>                                                 |
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/>                                               |
| [**Groupe**](windowsribbon-element-group.md)<br/>                                                                   |
| [**MenuGroup**](windowsribbon-element-menugroup.md)<br/>                                                           |
| [**QuickAccessToolbar.ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)<br/> |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>                                                       |
| [**SplitButton. ButtonItem**](windowsribbon-element-splitbutton-buttonitem.md)<br/>                                 |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/>                                         |



## <a name="remarks"></a>Notes

Facultatif ou obligatoire, en fonction de l’élément parent.

Peut se produire au plus une fois pour chaque élément [**SplitButton. ButtonItem**](windowsribbon-element-splitbutton-buttonitem.md) .

Peut se produire une ou plusieurs fois pour chaque élément [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**Group**](windowsribbon-element-group.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**QuickAccessToolbar. ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md), [**SplitButton**](windowsribbon-element-splitbutton.md)ou [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .

## <a name="examples"></a>Exemples

L’exemple suivant illustre le balisage de base pour l’élément **ToggleButton** .

Cette section de code illustre une déclaration d’élément **ToggleButton** au sein de l’élément [**QuickAccessToolbar. ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) .


```XML
      <Ribbon.QuickAccessToolbar>
        <QuickAccessToolbar CommandName="cmdQAT"
                            CustomizeCommandName="cmdCustomizeQAT">
          <QuickAccessToolbar.ApplicationDefaults>
            <Button CommandName="cmdButton1"/>
            <ToggleButton CommandName="cmdMinimize"
                          ApplicationDefaults.IsChecked="false"/>
          </QuickAccessToolbar.ApplicationDefaults>
        </QuickAccessToolbar>
      </Ribbon.QuickAccessToolbar>
```



## <a name="element-information"></a>Informations sur les éléments



|                                     |           |
|-------------------------------------|-----------|
| Système minimal pris en charge<br/> | Windows 7 |
| Peut être vide                        | Oui       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Bouton bascule](windowsribbon-controls-togglebutton.md)
</dt> </dl>

 

 





