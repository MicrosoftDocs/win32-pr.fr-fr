---
title: élément Command
description: Représente une définition de commande.
ms.assetid: f332423d-d258-488d-9233-71687288b462
keywords:
- élément de commande Windows ruban
topic_type:
- apiref
api_name:
- Command
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0c29539c9c76342b8b88603ea3dd2926554228ac
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404745"
---
# <a name="command-element"></a>élément Command

Représente une définition de commande.

## <a name="usage"></a>Usage

``` syntax
<Command
  Name = "xs:string"
  Symbol = "xs:string"
  Id = "xs:positiveInteger union xs:string"
  Comment = "xs:string"
  LabelTitle = "xs:string"
  LabelDescription = "xs:string"
  TooltipTitle = "xs:string"
  TooltipDescription = "xs:string"
  Keytip = "xs:string">
  child elements
</Command>
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
<td><strong>Commentaire</strong><br/></td>
<td>xs:string<br/></td>
<td>Non<br/></td>
<td>Utilisé pour annoter l’élément Command.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS : String)<br/> </dt> <dd> Chaîne composée de toute séquence de caractères, y compris les espaces blancs et les sauts de ligne.<br/> Longueur maximale : 250 caractères.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Id</strong><br/></td>
<td>XS : positiveInteger Union XS : String<br/></td>
<td>Non<br/></td>
<td>ID de ressource unique. <br/> <br/>
<dt><span></span><span></span><strong></strong> (Union de XS : positiveInteger et XS : String)<br/> </dt> <dd> Valeur entière comprise entre 2 et 59999, inclusive, ou 0X2 et 0xea5f en hexadécimal, inclus. <br/> La longueur maximale est de 10 caractères, y compris des zéros non significatifs facultatifs. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>KeyTip</strong><br/></td>
<td>xs:string<br/></td>
<td>Non<br/></td>
<td>Chaîne qui représente le raccourci clavier d’un élément de commande.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS : String)<br/> </dt> <dd> Chaîne composée d’une séquence de caractères, y compris un espace blanc.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>LabelDescription</strong><br/></td>
<td>xs:string<br/></td>
<td>Non<br/></td>
<td>Chaîne qui représente le texte affiché sur un élément Command.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS : String)<br/> </dt> <dd> Chaîne composée de toute séquence de caractères, y compris les espaces blancs et les sauts de ligne.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>LabelTitle</strong><br/></td>
<td>xs:string<br/></td>
<td>Non<br/></td>
<td>Chaîne qui représente le texte affiché sur un élément Command.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS : String)<br/> </dt> <dd> Chaîne composée de toute séquence de caractères, y compris les espaces blancs et les sauts de ligne.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Nom</strong><br/></td>
<td>xs:string<br/></td>
<td>Non<br/></td>
<td><dt><span></span><span></span><strong></strong> (XS : String)<br/> </dt> <dd> Chaîne qui se compose d’une lettre ou d’un trait de soulignement suivi d’une séquence de chiffres, de lettres ou de traits de soulignement.<br/> Longueur maximale : 100 caractères.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Symbole</strong><br/></td>
<td>xs:string<br/></td>
<td>Non<br/></td>
<td><dt><span></span><span></span><strong></strong> (XS : String)<br/> </dt> <dd> Chaîne qui se compose d’une lettre ou d’un trait de soulignement suivi d’une séquence de chiffres, de lettres ou de traits de soulignement.<br/> Longueur maximale : 100 caractères.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>TooltipDescription</strong><br/></td>
<td>xs:string<br/></td>
<td>Non<br/></td>
<td>Chaîne qui représente le texte affiché sur un élément Command.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS : String)<br/> </dt> <dd> Chaîne composée de toute séquence de caractères, y compris les espaces blancs et les sauts de ligne.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>TooltipTitle</strong><br/></td>
<td>xs:string<br/></td>
<td>Non<br/></td>
<td>Chaîne qui représente le texte affiché sur un élément Command.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS : String)<br/> </dt> <dd> Chaîne composée de toute séquence de caractères, y compris les espaces blancs et les sauts de ligne.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Éléments enfants



| Élément                                                                                                     | Description                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [**Commande. Comment.**](windowsribbon-element-command-comment.md)<br/>                                 | Peut se produire au plus une fois<br/> <br/> |
| [**Command.Id**](windowsribbon-element-command-id.md)<br/>                                           | Peut se produire au plus une fois<br/> <br/> |
| [**Commande. KeyTip**](windowsribbon-element-command-keytip.md)<br/>                                   | Peut se produire au plus une fois<br/> <br/> |
| [**Commande. LabelDescription**](windowsribbon-element-command-labeldescription.md)<br/>               | Peut se produire au plus une fois<br/> <br/> |
| [**Commande. LabelTitle**](windowsribbon-element-command-labeltitle.md)<br/>                           | Peut se produire au plus une fois<br/> <br/> |
| [**Commande. LargeHighContrastImages**](windowsribbon-element-command-largehighcontrastimages.md)<br/> | Peut se produire au plus une fois<br/> <br/> |
| [**Commande. LargeImages**](windowsribbon-element-command-largeimages.md)<br/>                         | Peut se produire au plus une fois<br/> <br/> |
| [**Command.Name**](windowsribbon-element-command-name.md)<br/>                                       | Peut se produire au plus une fois<br/> <br/> |
| [**Commande. SmallHighContrastImages**](windowsribbon-element-command-smallhighcontrastimages.md)<br/> | Peut se produire au plus une fois<br/> <br/> |
| [**Commande. SmallImages**](windowsribbon-element-command-smallimages.md)<br/>                         | Peut se produire au plus une fois<br/> <br/> |
| [**Command. Symbol**](windowsribbon-element-command-symbol.md)<br/>                                   | Peut se produire au plus une fois<br/> <br/> |
| [**Commande. TooltipDescription**](windowsribbon-element-command-tooltipdescription.md)<br/>           | Peut se produire au plus une fois<br/> <br/> |
| [**Commande. TooltipTitle**](windowsribbon-element-command-tooltiptitle.md)<br/>                       | Peut se produire au plus une fois<br/> <br/> |



## <a name="parent-elements"></a>Éléments parents



| Élément                                                                               |
|---------------------------------------------------------------------------------------|
| [**Application. commandes**](windowsribbon-element-application-commands.md)<br/> |



## <a name="remarks"></a>Notes

Obligatoire.

Peut se produire une ou plusieurs fois pour chaque élément [**application. Commands**](windowsribbon-element-application-commands.md) .

Les éléments enfants de l’élément de **commande** peuvent se produire dans n’importe quel ordre.

En général, les ressources de commande sont déclarées dans le balisage du ruban, mais elles peuvent également être définies au moment de l’exécution avec un appel à [**SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty). Par exemple, il est possible de définir la propriété de [ \_ \_ KeyTip KeyTip de l’interface utilisateur](windowsribbon-reference-properties-uipkey-keytip.md) pour une commande au lieu de déclarer une valeur dans le balisage avec l’élément [**Command. KeyTip**](windowsribbon-element-command-keytip.md) .

Dans les cas où les propriétés de commande, telles que les étiquettes et les images, ne peuvent pas être définies avec des [**SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) , elles peuvent être invalidées avec un appel à [**InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand). Après l’invalidation, l’infrastructure interroge l’application hôte pour obtenir les détails des ressources.

> [!Note]  
> Une ressource ne peut pas être rétablie à partir de la table de ressources de balisage une fois qu’elle a été invalidée.

 

Une définition de commande est ajoutée au fichier d’en-tête de balisage du ruban pour chaque **commande** déclarée dans le balisage.

La valeur de *KeyTip* agit comme touche d’accès rapide pour une commande, sauf si cette commande est exposée par le biais d’un élément de menu. Dans ce cas, le Framework ignore la valeur *KeyTip* et utilise à la place un caractère précédé d’un signe & comme spécifié par *LabelTitle* ou [l' \_ \_ étiquette de l’interface utilisateur](windowsribbon-reference-properties-uipkey-label.md). Si aucune esperluette n’est spécifiée par *LabelTitle* ou par l’étiquette de l’interface utilisateur, aucune touche d’accès ou touche d’accès \_ \_ rapide n’est exposée.

## <a name="examples"></a>Exemples

L’exemple suivant montre un manifeste d’éléments de **commande** pour un onglet de **démarrage** .


```XML
<Application.Commands>
```




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




```XML
</Application.Commands>
```



## <a name="element-information"></a>Informations sur les éléments

* **système minimal pris en charge**: Windows 7
* **Peut être vide**: non



 

