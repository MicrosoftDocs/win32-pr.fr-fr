---
title: Tab (élément)
description: Représente un onglet principal ou contextuel.
ms.assetid: 2e73a89c-4d31-4075-93c8-e43213a20791
keywords:
- Ruban fenêtres d’élément d’onglet
topic_type:
- apiref
api_name:
- Tab
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 410326961df84f6ae62d3c43bee3e651c9533066
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443880"
---
# <a name="tab-element"></a>Tab (élément)

Représente un onglet [principal](windowsribbon-controls-tab.md) ou [contextuel](windowsribbon-controls-tabgroup.md) .

## <a name="usage"></a>Utilisation

``` syntax
<Tab
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</Tab>
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
<td><strong>ApplicationModes</strong><br/></td>
<td>xs:string<br/></td>
<td>Non<br/></td>
<td>Valide uniquement si <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> est l’élément parent.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS : String)<br/> </dt> <dd> Chaîne qui contient une liste d’entiers séparés par des virgules, comprise entre 0 et 31.<br/> L’espace blanc est valide et ignoré.<br/> Longueur maximale : 250 caractères. <br/> </dd> </dl></td>
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



| Élément                                                                         | Description                                        |
|---------------------------------------------------------------------------------|----------------------------------------------------|
| [**Groupe**](windowsribbon-element-group.md)<br/>                         | Peut se produire une ou plusieurs fois<br/> <br/> |
| [**Tab. ScalingPolicy**](windowsribbon-element-tab-scalingpolicy.md)<br/> | Peut se produire au plus une fois<br/> <br/>      |



## <a name="parent-elements"></a>Éléments parents



| Élément                                                             |
|---------------------------------------------------------------------|
| [**Ruban. tabulations**](windowsribbon-element-ribbon-tabs.md)<br/> |
| [**TabGroup**](windowsribbon-element-tabgroup.md)<br/>       |



## <a name="remarks"></a>Remarques

Obligatoire.

Doit se produire au moins une fois pour chaque élément [**ruban. Tabs**](windowsribbon-element-ribbon-tabs.md) ou [**TabGroup**](windowsribbon-element-tabgroup.md) .

L' **onglet** prend en charge les [modes d’application](ribbon-applicationmodes.md).

Si [**ScalingPolicy. IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) est présent pour l’élément **Tab** , une entrée pour chaque élément de [**groupe**](windowsribbon-element-group.md) et sa taille idéale est requise sous **ScalingPolicy. IdealSizes**.

## <a name="examples"></a>Exemples

L’exemple suivant illustre le balisage de base pour l’élément **Tab** .

Cette section de code montre les déclarations de commande d' **onglet** pour un onglet de **démarrage** .


```XML
<Command Name="cmdHomeTab"
         LabelTitle="Home"
         Keytip="H" />
<Command Name="cmdClipboardGroup"
         Symbol="IDR_CMD_CLIPBOARD"
         Id="10000"
         Comment="Command definition for clipboard group"
         LabelTitle="Clipboard"
         Keytip="CB" />
<Command Name="cmdCopy"
         Symbol="IDR_CMD_COPY"
         LabelTitle="Copy"
         LabelDescription="Copy"
         Keytip="C"
         TooltipTitle="Copy"
         TooltipDescription="Click to copy">
  <Command.SmallImages>
    <Image>res/copyS_16.bmp</Image>
  </Command.SmallImages>
  <Command.LargeImages>
    <Image>res/copyL_32.bmp</Image>
  </Command.LargeImages>
</Command>
<Command Name="cmdPaste"
         Symbol="IDR_CMD_PASTE" >
  <Command.LabelTitle>Paste</Command.LabelTitle>
  <Command.LabelDescription>
    <String Content="Paste contents of clipboard"
            Id="10001"
            Symbol="IDR_RES_LABELDESC_PASTE" />
  </Command.LabelDescription>
  <Command.Keytip>P</Command.Keytip>
  <Command.TooltipTitle>
    <String Content="Paste contents of clipboard"
            Id="10002"
            Symbol="IDR_RES_TOOLTIP_PASTE"/>
  </Command.TooltipTitle>
  <Command.TooltipDescription>
    <String Content="Click to paste contents of clipboard"/>
  </Command.TooltipDescription>
  <Command.SmallImages>
    <Image
      Id="10010"
      MinDPI="96"
      Symbol="IDR_RES_SMALL_IMAGE96">
      <Image.Source>res/pasteS_96bpp.bmp</Image.Source>
    </Image>
    <Image Source="res/pasteS_120bpp.bmp"
           Id="10011"
           MinDPI="120"
           Symbol="IDR_RES_SMALL_IMAGE120" />
  </Command.SmallImages>
  <Command.LargeImages>
    <Image>res/pasteL_32.bmp</Image>
  </Command.LargeImages>
</Command>
<Command Name="cmdMinimize"
         Symbol="IDR_CMD_MINIMIZE"
         Id="10001"
         LabelTitle="Minimize" />
```



Cette section de code montre les déclarations de contrôle d' **onglet** .


```XML
<Tab CommandName="cmdHomeTab">
  <Group CommandName="cmdClipboardGroup" 
         SizeDefinition="ThreeButtons">
    <Button CommandName="cmdCopy"/>
    <Button CommandName="cmdPaste"/>
    <ToggleButton CommandName="cmdMinimize"/>
  </Group>
</Tab>
```



## <a name="element-information"></a>Informations sur les éléments

- **Système minimal pris en charge**: Windows 7 
- **Peut être vide**: non



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Contrôle Tab](windowsribbon-controls-tab.md)
</dt> <dt>

[Contrôle de groupe d’onglets](windowsribbon-controls-tabgroup.md)
</dt> <dt>

[**SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

