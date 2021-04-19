---
description: Le \_ \_ \_ type d’énumération types d’analyses vidéo wpd décrit la façon dont les champs d’un fichier vidéo sont encodés.
ms.assetid: ea0dab57-6783-4d02-a43c-414e313f1e80
title: Énumération WPD_VIDEO_SCAN_TYPES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_VIDEO_SCAN_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: a636bc95fd3d25de20c2df413576a504c4fa1b96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545355"
---
# <a name="wpd_video_scan_types-enumeration"></a>\_ \_ Énumération des types d’analyses vidéo wpd \_

Le type d’énumération **\_ \_ \_ types d’analyses vidéo wpd** décrit la façon dont les champs d’un fichier vidéo sont encodés.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum WPD_VIDEO_SCAN_TYPES { 
  WPD_VIDEO_SCAN_TYPE_UNUSED                           = 0,
  WPD_VIDEO_SCAN_TYPE_PROGRESSIVE                      = 1,
  WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_UPPER_FIRST    = 2,
  WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_LOWER_FIRST    = 3,
  WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_UPPER_FIRST         = 4,
  WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_LOWER_FIRST         = 5,
  WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE                  = 6,
  WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE_AND_PROGRESSIVE  = 7
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_UNUSED"></span><span id="wpd_video_scan_type_unused"></span>**\_type d' \_ analyse vidéo wpd \_ \_ inutilisé**
</dt> <dd>

Le type d’analyse n’a pas été défini pour ce fichier vidéo ou n’est pas applicable.

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_PROGRESSIVE"></span><span id="wpd_video_scan_type_progressive"></span>**\_type d' \_ analyse vidéo wpd \_ \_ progressif**
</dt> <dd>

Fichier vidéo d’analyse progressive.

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_UPPER_FIRST"></span><span id="wpd_video_scan_type_field_interleaved_upper_first"></span>**\_champ de \_ type d’analyse vidéo wpd entrelacé en \_ \_ \_ \_ \_ premier**
</dt> <dd>

Fichier vidéo entrelacé dans lequel les champs alternatifs et le champ supérieur (avec la ligne 1) sont dessinés en premier. Pour plus d'informations, consultez la section Notes.

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_LOWER_FIRST"></span><span id="wpd_video_scan_type_field_interleaved_lower_first"></span>**\_champ de \_ type d’analyse vidéo wpd entrelacé en \_ \_ \_ \_ \_ premier**
</dt> <dd>

Fichier vidéo entrelacé dans lequel les champs alternatifs et le champ inférieur (avec la ligne 2) sont dessinés en premier. Pour plus d’informations, consultez la section Notes, à la suite de cette section.

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_UPPER_FIRST"></span><span id="wpd_video_scan_type_field_single_upper_first"></span>**\_champ de \_ type d’analyse vidéo wpd unique en \_ \_ \_ \_ \_ premier**
</dt> <dd>

Fichier vidéo entrelacé dans lequel les champs sont envoyés en tant qu’échantillons contigus et le champ supérieur (avec la ligne 1) est dessiné en premier. Pour plus d’informations, consultez la section Notes, à la suite de cette section.

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_LOWER_FIRST"></span><span id="wpd_video_scan_type_field_single_lower_first"></span>**\_champ de \_ type d’analyse vidéo wpd simple en \_ \_ \_ \_ \_ premier**
</dt> <dd>

Fichier vidéo entrelacé dans lequel les champs sont envoyés en tant qu’échantillons contigus et le champ inférieur (avec la ligne 2) est envoyé en premier.

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE"></span><span id="wpd_video_scan_type_mixed_interlace"></span>**\_balayage vidéo \_ de \_ type \_ wpd \_ entrelacé mixte**
</dt> <dd>

Fichier vidéo avec un mélange de modes d’entrelacement.

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE_AND_PROGRESSIVE"></span><span id="wpd_video_scan_type_mixed_interlace_and_progressive"></span>**\_balayage vidéo wpd- \_ \_ type \_ mixte \_ entrelacé \_ et \_ progressif**
</dt> <dd>

Fichier vidéo avec un mélange de modes entrelacés et progressifs.

</dd> </dl>

## <a name="remarks"></a>Notes

Cette énumération est utilisée par la propriété de [ \_ \_ \_ type d’analyse vidéo wpd](properties-and-attributes.md) .

Il existe deux types de formats de fichier entrelacés qui sont spécifiés par cette énumération. **Wpd \_ \_Champ de type d’analyse vidéo \_ \_ \_ entrelacée** fait référence à un format de fichier dans lequel les trames sont remises au fur et à mesure qu’elles ont été analysées. les champs alternatifs et les données sont placés ligne par ligne, comme illustré ici :

**Trame 1**

Champ 1 : ligne 1

Champ 2 : ligne 1

Champ 1 : ligne 2

Champ 2 : ligne 2

Champ 1 : ligne 3

Champ 2 : ligne 3

...

**Wpd \_ Le \_ champ de type d’analyse vidéo \_ \_ \_ unique** fait référence à un format de fichier où chaque champ est stocké dans un bloc unique de lignes de numérisation, et les champs sont stockés de manière séquentielle, comme illustré ici :

**Trame 1**

Champ 1 : ligne 1

Champ 1 : ligne 2

Champ 1 : ligne 3

...

Suivi de

Champ 2 : ligne 1

Champ 2 : ligne 2

Champ 2 : ligne 3

...

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Structures et types énumération**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




