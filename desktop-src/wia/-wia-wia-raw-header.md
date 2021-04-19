---
description: La \_ \_ structure d’en-tête brut WIA définit une image au format de données brutes d’un appareil et permet aux applications d’utiliser le format RAW dans les transferts WIA (Windows Image Acquisition).
ms.assetid: c7b50816-d596-4c62-a00e-cd8d6e303e42
title: Structure WIA_RAW_HEADER (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_RAW_HEADER
api_type:
- HeaderDef
api_location:
- Wiadef.h
ms.openlocfilehash: 8da33f0b257168712f1b16fb7f940df5db862d3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515037"
---
# <a name="wia_raw_header-structure"></a>\_Structure d' \_ en-tête brut WIA

La structure d' **\_ \_ en-tête brut WIA** définit une image au format de données brutes d’un appareil et permet aux applications d’utiliser le format RAW dans les transferts WIA (Windows Image Acquisition).

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _WIA_RAW_HEADER {
  DWORD Tag;
  DWORD Version;
  DWORD HeaderSize;
  DWORD XRes;
  DWORD YRes;
  DWORD XExtent;
  DWORD YExtent;
  DWORD BytesPerLine;
  DWORD BitsPerPixel;
  DWORD ChannelsPerPixel;
  DWORD DataType;
  BYTE  BitsPerChannel[8];
  DWORD Compression;
  DWORD PhotometricInterp;
  DWORD LineOrder;
  DWORD RawDataOffset;
  DWORD RawDataSize;
  DWORD PaletteOffset;
  DWORD PaletteSize;
} WIA_RAW_HEADER;
```



## <a name="members"></a>Membres

<dl> <dt>

**Tag**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Nom du format. Il doit s’agir du littéral « WRAW » (quatre caractères ASCII sur un seul octet).

</dd> <dt>

**Version**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Version du format brut. Utilisez toujours 0x00010000.

</dd> <dt>

**HeaderSize**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Nombre total d’octets valides dans l’en-tête.

</dd> <dt>

**XRes**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

La résolution horizontale en points par pouce.

</dd> <dt>

**YRes**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

La résolution verticale en points par pouce.

</dd> <dt>

**XExtent**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Largeur de l’image en pixels.

</dd> <dt>

**YExtent**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Hauteur de l’image en pixels.

</dd> <dt>

**BytesPerLine**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Nombre d’octets dans une ligne d’une image non compressée. Utilisez 0 lorsque les données sont compressées pour signaler que le nombre d’octets par ligne est inconnu.

</dd> <dt>

**BitsPerPixel**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Nombre total de bits par pixel pour tous les canaux du pixel.

</dd> <dt>

**ChannelsPerPixel**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Nombre de canaux de couleur dans un pixel.

</dd> <dt>

**DataType**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

\_ \_ Type de données WIA de la loi WIA de l’image. Étant donné \_ que \_ le format WIA WIA est défini sur WiaImgFmt \_ RAW, il s’agit d’une liste de valeurs autorisées que l’application choisit.

</dd> <dt>

**BitsPerChannel \[ 8\]**
</dt> <dd>

Type : **Byte**

</dd> <dd>

Nombre de bits dans un canal, jusqu’à un maximum de 8.

</dd> <dt>

**Compression**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

\_ \_ Valeur de compression WIA de la Loi d’images qui spécifie le type de compression utilisé, le cas échéant.

</dd> <dt>

**PhotometricInterp**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

\_ \_ Valeur interp photométrique WIA \_ de la loi WIA spécifiant l’interprétation photométrique de l’image.

</dd> <dt>

**LineOrder**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Valeur représentant l’ordre des lignes de l’image. Il s’agit toujours de l' \_ ordre des lignes WIA \_ \_ \_ de haut en bas ou de l’ordre des \_ \_ lignes WIA \_ \_ \_ de bas en \_ haut.

</dd> <dt>

**RawDataOffset**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Position des données d’image brutes en octets, à partir de la position à laquelle l’en-tête se termine ou de la position à laquelle la palette se termine.

</dd> <dt>

**RawDataSize**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Taille, en octets, des données d’image brutes.

</dd> <dt>

**PaletteOffset**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Position de la palette en octets, à partir de la position à laquelle l’en-tête se termine ou de la position à laquelle les données se terminent. (Cette valeur est 0, s’il n’y a aucune palette.)

</dd> <dt>

**PaletteSize**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Taille, en octets, de la table de palettes. (Il s’agit de 0, s’il n’y a aucune palette.)

</dd> </dl>

## <a name="remarks"></a>Notes

Étant donné qu’il ne s’agit pas d’un format de fichier, utilisez une chaîne vide pour la propriété d’extension de fichier WIA de la \_ Loi \_ \_ .

La palette et les données peuvent être dans l’ordre.

**RawDataSize** n’inclut ni l’en-tête ni la palette. Utilisez ce champ pour vérifier que le transfert de l’image a réussi.

**PaletteSize** est le nombre d’octets, et non le nombre d’entrées dans la palette.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 




