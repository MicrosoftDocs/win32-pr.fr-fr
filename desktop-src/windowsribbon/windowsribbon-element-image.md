---
title: élément Image (Windows Framework du ruban)
description: Représente une image.
ms.assetid: 2c71bb16-93ac-484f-b81b-1b95842472b3
keywords:
- élément Image Windows ruban
topic_type:
- apiref
api_name:
- Image
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b05f7c93ea1597d2dde4724ff0b24b53769cd9ea
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122631677"
---
# <a name="image-element"></a>Élément Image

Représente une image.

## <a name="usage"></a>Utilisation

``` syntax
<Image
  Source = "xs:anyURI"
  MinDPI = "xs:positiveInteger"
  Symbol = "xs:string"
  Id = "xs:positiveInteger union xs:string">
  child elements
</Image>
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
<td><strong>Id</strong><br/></td>
<td>XS : positiveInteger Union XS : String<br/></td>
<td>No<br/></td>
<td>ID de ressource unique. <br/> <br/>
<dt><span></span><span></span><strong></strong> (Union de XS : positiveInteger et XS : String)<br/> </dt> <dd> Valeur entière comprise entre 2 et 59999, inclusive, ou 0X2 et 0xea5f en hexadécimal, inclus. <br/> La longueur maximale est de 10 caractères, y compris des zéros non significatifs facultatifs. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>MinDPI</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>No<br/></td>
<td><dt><span></span><span></span><strong></strong> (XS : positiveInteger)<br/> </dt> <dd> Toute séquence de chiffres avec une valeur minimale de 96. <br/> Si MinDPI est omis, la valeur par défaut est 96. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Source</strong><br/></td>
<td>xs:anyURI<br/></td>
<td>No<br/></td>
<td><dt><span></span><span></span><strong></strong> (XS : anyURI)<br/> </dt> <dd> Séquence de caractères qui représente un URI. La valeur de l’URI est un chemin d’accès absolu ou relatif (au fichier de balisage du ruban) à une ressource image de type BMP. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Symbole</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Symbole de ressource pour l’image.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS : String)<br/> </dt> <dd> Chaîne composée d’une lettre ou d’un trait de soulignement suivi d’une séquence de lettres, de chiffres ou de traits de soulignement, avec un maximum de 100 caractères. <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Éléments enfants



| Élément                                                               | Description                                   |
|-----------------------------------------------------------------------|-----------------------------------------------|
| [**Image. source**](windowsribbon-element-image-source.md)<br/> | Peut se produire au plus une fois<br/> <br/> |



## <a name="parent-elements"></a>Éléments parents



| Élément                                                                                                     |
|-------------------------------------------------------------------------------------------------------------|
| [**Commande. LargeHighContrastImages**](windowsribbon-element-command-largehighcontrastimages.md)<br/> |
| [**Commande. LargeImages**](windowsribbon-element-command-largeimages.md)<br/>                         |
| [**Commande. SmallHighContrastImages**](windowsribbon-element-command-smallhighcontrastimages.md)<br/> |
| [**Commande. SmallImages**](windowsribbon-element-command-smallimages.md)<br/>                         |



## <a name="remarks"></a>Remarques

Optionnel.

Peut se produire une ou plusieurs fois pour chaque élément [**Command. SmallImages**](windowsribbon-element-command-smallimages.md), [**Command. SmallHighContrastImages**](windowsribbon-element-command-smallhighcontrastimages.md), [**Command. LargeImages**](windowsribbon-element-command-largeimages.md)ou [**Command. LargeHighContrastImages**](windowsribbon-element-command-largehighcontrastimages.md) .

Lorsqu’une collection de ressources d’image conçues pour prendre en charge des paramètres de points par pouce (dpi) spécifiques est fournie à l’infrastructure du ruban via un ensemble d’éléments d' **image** , l’infrastructure utilise l' **image** avec une valeur d’attribut *MinDPI* qui correspond au paramètre PPP d’écran actuel.

Si aucun élément **image** n’est déclaré avec une valeur *MinDPI* qui correspond au paramètre PPP d’écran actuel, l’infrastructure sélectionne l' **image** qui a la valeur *MinDPI* la plus proche inférieure au paramètre PPP d’écran actuel et met à l’échelle la ressource d’image. Sinon, si aucun élément **image** n’est déclaré avec une valeur d’attribut *MinDPI* inférieure au paramètre PPP d’écran actuel, le Framework choisit la valeur *MinDPI* la plus proche supérieure au paramètre PPP d’écran actuel et met à l’échelle la ressource d’image.

## <a name="examples"></a>Exemples

L’exemple de code suivant montre le balisage requis pour déclarer, via un ensemble d’éléments **image** , une collection de ressources d’image conçues pour prendre en charge quatre paramètres de résolution d’écran spécifiques.


```XML
<Command Name="cmdSizeAndColor" Symbol="IDR_CMD_SIZEANDCOLOR">
  <Command.LabelTitle>
    <String Id="250">Size and Color</String>
  </Command.LabelTitle>
  <Command.LargeImages>
    <Image Id="251" MinDPI="96">res/sizeAndColor_96.bmp</Image>
    <Image Id="252" MinDPI="120">res/sizeAndColor_120.bmp</Image>
    <Image Id="253" MinDPI="144">res/sizeAndColor_144.bmp</Image>
    <Image Id="254" MinDPI="192">res/sizeAndColor_192.bmp</Image>
  </Command.LargeImages>
</Command>
```



## <a name="element-information"></a>Informations sur les éléments

* **système minimal pris en charge**: Windows 7
* **Peut être vide**: non



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Spécification des ressources d’image du ruban](windowsribbon-imageformats.md)
</dt> </dl>

 

 





