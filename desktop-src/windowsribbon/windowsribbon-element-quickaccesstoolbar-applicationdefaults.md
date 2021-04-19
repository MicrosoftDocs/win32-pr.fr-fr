---
title: QuickAccessToolbar. ApplicationDefaults, propriété
description: Représente un conteneur pour les commandes par défaut dans la barre d’outils accès rapide (QAT).
ms.assetid: 8f44d7c0-1a39-4a88-ae01-7d7d1bb6bf7e
keywords:
- Ruban Windows de la propriété QuickAccessToolbar. ApplicationDefaults
topic_type:
- apiref
api_name:
- QuickAccessToolbar.ApplicationDefaults
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 084ea334441cb0cf545adaa3d1016f7d02da1b88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106518066"
---
# <a name="quickaccesstoolbarapplicationdefaults-property"></a>QuickAccessToolbar. ApplicationDefaults, propriété

Représente un conteneur pour les commandes par défaut dans la [barre d’outils accès rapide (qat)](windowsribbon-controls-quickaccesstoolbar.md).

## <a name="usage"></a>Utilisation

``` syntax
<QuickAccessToolbar.ApplicationDefaults>
  child elements
</QuickAccessToolbar.ApplicationDefaults>
```

## <a name="attributes"></a>Attributs

Il n’y a pas d’attributs.

## <a name="child-elements"></a>Éléments enfants



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Élément</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="windowsribbon-element-button.md"><strong>Button</strong></a><br/></td>
<td>Doit être présent au moins une fois.<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-element-checkbox.md"><strong>CheckBox</strong></a><br/></td>
<td>Doit être présent au moins une fois.<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-element-combobox.md"><strong>ComboBox</strong></a><br/></td>
<td>Doit être présent au moins une fois.<br/>
<blockquote>
[!Note]<br />
Windows 8 et versions ultérieures.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-element-dropdowngallery.md"><strong>DropDownGallery</strong></a><br/></td>
<td>Doit être présent au moins une fois.<br/>
<blockquote>
[!Note]<br />
Windows 8 et versions ultérieures.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-element-inribbongallery.md"><strong>InRibbonGallery</strong></a><br/></td>
<td>Doit être présent au moins une fois.<br/>
<blockquote>
[!Note]<br />
Windows 8 et versions ultérieures.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-element-splitbuttongallery.md"><strong>SplitButtonGallery</strong></a><br/></td>
<td>Doit être présent au moins une fois.<br/>
<blockquote>
[!Note]<br />
Windows 8 et versions ultérieures.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-element-togglebutton.md"><strong>ToggleButton</strong></a><br/></td>
<td>Doit être présent au moins une fois.<br/> <br/></td>
</tr>
</tbody>
</table>



## <a name="parent-elements"></a>Éléments parents



| Élément                                                                           |
|-----------------------------------------------------------------------------------|
| [**QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar.md)<br/> |



## <a name="remarks"></a>Notes

Optionnel.

Peut se produire au plus une fois pour chaque [**QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar.md).

Au moins un élément enfant doit être spécifié.

Vous pouvez spécifier un maximum de 20 éléments enfants.

## <a name="examples"></a>Exemples

L’exemple suivant illustre le balisage de base pour [**QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar.md).

Cette section de code illustre la déclaration de contrôle **QuickAccessToolbar. ApplicationDefaults** .


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



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Contrôle de barre d’outils accès rapide](windowsribbon-controls-quickaccesstoolbar.md)
</dt> </dl>

 

 





