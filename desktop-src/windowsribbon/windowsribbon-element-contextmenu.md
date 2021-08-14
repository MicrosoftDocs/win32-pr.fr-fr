---
title: ContextMenu, élément
description: Représente un contrôle de menu contextuel.
ms.assetid: 08cc0514-0795-4e6b-b80c-33d920783032
keywords:
- élément ContextMenu Windows ruban
topic_type:
- apiref
api_name:
- ContextMenu
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4fb061c08635cff46ca80d803089ebc01c48c19cdcc9136b1052c5a0ef2c3a1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118707432"
---
# <a name="contextmenu-element"></a>ContextMenu, élément

Représente un contrôle de menu contextuel.

## <a name="usage"></a>Usage

``` syntax
<ContextMenu
  Name = "xs:string">
  child elements
</ContextMenu>
```

## <a name="attributes"></a>Attributs



| Attribut           | Type                 | Obligatoire       | Description                                                                                                                                                                                                                |
|---------------------|----------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Nom**<br/> | xs:string<br/> | Oui<br/> | <dt> (XS : String)<br/> </dt> <dd> Chaîne composée de toute séquence de caractères, y compris les espaces blancs et les sauts de ligne.<br/> </dd> </dl> |



## <a name="child-elements"></a>Éléments enfants



| Élément                                                         | Description                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [**MenuGroup**](windowsribbon-element-menugroup.md)<br/> | Doit se produire au moins une fois<br/> <br/> |



## <a name="parent-elements"></a>Éléments parents



| Élément                                                                                         |
|-------------------------------------------------------------------------------------------------|
| [**ContextPopup.ContextMenus**](windowsribbon-element-contextpopup-contextmenus.md)<br/> |



## <a name="remarks"></a>Remarques

Facultatif.

Peut se produire une ou plusieurs fois pour chaque [**ContextPopup. ContextMenus**](windowsribbon-element-contextpopup-contextmenus.md).

> [!IMPORTANT]
> Un **ContextMenu** ne peut pas héberger des contrôles de [zone de liste déroulante](windowsribbon-controls-combobox.md) ou d' [Spinner](windowsribbon-controls-spinner.md) .

 

## <a name="examples"></a>Exemples

L’exemple suivant illustre le balisage de base pour une vue [**ContextPopup**](windowsribbon-element-contextpopup.md) .

Cette section de code illustre un ensemble de déclarations de contrôle **ContextMenu** .


```XML
    <ContextPopup>
      <!--
        The MiniToolbars and Context Menus are the basic ingredients for 
        the contextual UI popup. 
        Mix-and-match and associate each combination with a ContextMap Command 
        invoked in code.
      -->
      <ContextPopup.MiniToolbars>
        <MiniToolbar Name="MiniToolbar1">
          <MenuGroup Class="MajorItems">
            <Button CommandName="cmdCut" />
            <Button CommandName="cmdCopy" />
            <Button CommandName="cmdPaste" />
          </MenuGroup>
          <MenuGroup>
            <ToggleButton CommandName="cmdToggleButton" />
            <DropDownButton CommandName="cmdButtons">
              <MenuGroup>
                <Button CommandName="cmdButton1" />
                <Button CommandName="cmdButton2" />
                <Button CommandName="cmdButton3" />
              </MenuGroup>
            </DropDownButton>
          </MenuGroup>
        </MiniToolbar>
        <MiniToolbar Name="MiniToolbar2">
          <MenuGroup>
            <Button CommandName="cmdButton1" />
            <Button CommandName="cmdButton2" />
            <Button CommandName="cmdButton3" />
          </MenuGroup>
        </MiniToolbar>
      </ContextPopup.MiniToolbars>
      <ContextPopup.ContextMenus>
        <ContextMenu Name="ContextMenu1">
          <MenuGroup>
            <Button CommandName="cmdCut" />
            <Button CommandName="cmdCopy" />
            <Button CommandName="cmdPaste" />
          </MenuGroup>
        </ContextMenu>
        <ContextMenu Name="ContextMenu2">
          <MenuGroup>
            <ToggleButton CommandName="cmdToggleButton" />
          </MenuGroup>
          <MenuGroup>
            <Button CommandName="cmdButton1" />
            <Button CommandName="cmdButton2" />
            <Button CommandName="cmdButton3" />
          </MenuGroup>
        </ContextMenu>
        <ContextMenu Name="ContextMenu4">
          <MenuGroup>
            <Button CommandName="cmdCut" />
            <Button CommandName="cmdCopy" />
            <Button CommandName="cmdPaste" />
          </MenuGroup>
          <MenuGroup>
            <ToggleButton CommandName="cmdToggleButton" />
          </MenuGroup>
          <MenuGroup>
            <Button CommandName="cmdButton1" />
            <Button CommandName="cmdButton2" />
            <Button CommandName="cmdButton3" />
          </MenuGroup>
        </ContextMenu>
      </ContextPopup.ContextMenus>
      <ContextPopup.ContextMaps>
        <ContextMap CommandName="cmdContextMap1"
                    ContextMenu="ContextMenu1"/>
        <ContextMap CommandName="cmdContextMap2"
                    ContextMenu="ContextMenu2"
                    MiniToolbar="MiniToolbar1"/>
        <ContextMap CommandName="cmdContextMap3"
                    MiniToolbar="MiniToolbar2"/>
        <ContextMap CommandName="cmdContextMap4"
                    ContextMenu="ContextMenu4"/>
      </ContextPopup.ContextMaps>
    </ContextPopup>
```



## <a name="element-information"></a>Informations sur les éléments

* **système minimal pris en charge**: Windows 7
* **Peut être vide**: non



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Contrôle Popup du contexte](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 





