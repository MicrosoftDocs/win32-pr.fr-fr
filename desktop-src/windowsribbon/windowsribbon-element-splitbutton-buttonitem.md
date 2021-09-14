---
title: Propriété SplitButton. ButtonItem
description: Représente un conteneur pour un bouton ou un bouton bascule qui expose la commande par défaut d’un bouton partagé.
ms.assetid: 3d46d606-238d-46d4-b92e-dfd759951770
keywords:
- propriété SplitButton. ButtonItem Windows ruban
topic_type:
- apiref
api_name:
- SplitButton.ButtonItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bf1e1cb908ce9a86f23f75d17bf2e76797997db
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127293938"
---
# <a name="splitbuttonbuttonitem-property"></a>Propriété SplitButton. ButtonItem

Représente un conteneur pour un [bouton ou un](windowsribbon-controls-button.md) [bouton bascule](windowsribbon-controls-togglebutton.md) qui expose la commande par défaut d’un [bouton partagé](windowsribbon-controls-splitbutton.md).

## <a name="usage"></a>Usage

``` syntax
<SplitButton.ButtonItem>
  child elements
</SplitButton.ButtonItem>
```

## <a name="attributes"></a>Attributs

Il n’y a pas d’attributs.

## <a name="child-elements"></a>Éléments enfants



| Élément                                                               | Description                                   |
|-----------------------------------------------------------------------|-----------------------------------------------|
| [**Button**](windowsribbon-element-button.md)<br/>             | Peut se produire au plus une fois<br/> <br/> |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/> | Peut se produire au plus une fois<br/> <br/> |



## <a name="parent-elements"></a>Éléments parents



| Élément                                                             |
|---------------------------------------------------------------------|
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/> |



## <a name="remarks"></a>Notes

Optionnel.

Peut se produire au plus une fois pour chaque [**SplitButton**](windowsribbon-element-splitbutton.md).

Chaque **SplitButton. ButtonItem** ne peut contenir qu’un seul élément enfant [**Button**](windowsribbon-element-button.md) ou [**ToggleButton**](windowsribbon-element-togglebutton.md) .

## <a name="examples"></a>Exemples

L’exemple suivant illustre le balisage de base pour le [bouton partagé](windowsribbon-controls-splitbutton.md).

Cette section de code montre les déclarations de commande [**SplitButton**](windowsribbon-element-splitbutton.md) et **SplitButton. ButtonItem** , avec un [**groupe**](windowsribbon-element-group.md) associé qui fonctionne comme conteneur parent de l’élément **SplitButton** .


```XML
<!-- SplitButton -->
<Command Name="cmdSplitButtonGroup"
         Symbol="cmdSplitButtonGroup"
         Comment="SplitButton Group"
         LabelTitle="SplitButton"/>
<Command Name="cmdSplitButton"
         Symbol="cmdSplitButton"
         Comment="SplitButton"
         LabelTitle="SplitButton"/>
<Command Name="cmdSBButtonItem"
         Symbol="cmdSBButtonItem"
         Comment="SBButtonItem"
         LabelTitle="SB ButtonItem"/>
<Command Name="cmdSBButton1"
         Symbol="cmdSBButton1"
         Comment="SBButton1"
         LabelTitle="SB Button">
  <Command.LargeImages>
    <Image Source="res/copyL_32.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/copyS_16.bmp"/>
  </Command.SmallImages>
  <Command.LargeHighContrastImages>
    <Image Source="res/copyLHC_32.bmp"/>
  </Command.LargeHighContrastImages>
  <Command.SmallHighContrastImages>
    <Image Source="res/copySHC_16.bmp"/>
  </Command.SmallHighContrastImages>
</Command>
<Command Name="cmdSBMajorItems"
         Comment="Major Items Category"
         LabelTitle="Major Items"/>
<Command Name="cmdSBStandardItems"
         Comment="Standard Items Category"
         LabelTitle="Standard Items"/>
```



Cette section de code montre les déclarations de contrôle [**SplitButton**](windowsribbon-element-splitbutton.md) et **SplitButton. ButtonItem** .


```XML
<Group CommandName="cmdSplitButtonGroup">
  <SplitButton CommandName="cmdSplitButton">
    <SplitButton.ButtonItem>
      <Button CommandName="cmdSBButtonItem"/>
    </SplitButton.ButtonItem>
    <SplitButton.MenuGroups>
      <MenuGroup CommandName="cmdSBMajorItems" 
                 Class="MajorItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup CommandName="cmdSBStandardItems"
                 Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
    </SplitButton.MenuGroups>
  </SplitButton>
</Group>
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>              |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Contrôle de bouton partagé](windowsribbon-controls-splitbutton.md)
</dt> </dl>

 

 





