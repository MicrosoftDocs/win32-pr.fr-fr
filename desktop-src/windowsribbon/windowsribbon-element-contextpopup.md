---
title: Élément ContextPopup
description: Représente le contrôle contextuel de contexte dans la vue ContextPopup.
ms.assetid: b955be16-803e-47b5-a72d-f993180fbf14
keywords:
- Ruban des fenêtres d’élément ContextPopup
topic_type:
- apiref
api_name:
- ContextPopup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f779b0196d14fb42246c2a10d476352d835b6cf8
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443461"
---
# <a name="contextpopup-element"></a>Élément ContextPopup

Représente le contrôle [contextuel de contexte](windowsribbon-controls-contextpopup.md) dans la vue ContextPopup.

## <a name="usage"></a>Utilisation

``` syntax
<ContextPopup>
  child elements
</ContextPopup>
```

## <a name="attributes"></a>Attributs

Il n’y a pas d’attributs.

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                                         | Description                                   |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [**ContextPopup.ContextMaps**](windowsribbon-element-contextpopup-contextmaps.md)<br/>   | Peut se produire au plus une fois<br/> <br/> |
| [**ContextPopup.ContextMenus**](windowsribbon-element-contextpopup-contextmenus.md)<br/> | Peut se produire au plus une fois<br/> <br/> |
| [**ContextPopup.MiniToolbars**](windowsribbon-element-contextpopup-minitoolbars.md)<br/> | Peut se produire au plus une fois<br/> <br/> |



## <a name="parent-elements"></a>Éléments parents



| Élément                                                                         |
|---------------------------------------------------------------------------------|
| [**Application. views**](windowsribbon-element-application-views.md)<br/> |



## <a name="remarks"></a>Remarques

facultatif.

Peut se produire au plus une fois pour chaque [**application. views**](windowsribbon-element-application-views.md).

## <a name="examples"></a>Exemples

L’exemple suivant illustre le balisage de base pour une vue **ContextPopup** .


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

* **Système minimal pris en charge**: Windows 7
* **Peut être vide**: non



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Contrôle Popup du contexte](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 





