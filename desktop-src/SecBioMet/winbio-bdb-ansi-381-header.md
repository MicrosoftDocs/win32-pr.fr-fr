---
title: Structure WINBIO_BDB_ANSI_381_HEADER ( \_ types WINBIO. h)
description: Spécifie des informations sur une série d’exemples d’empreintes digitales ou Palm.
ms.assetid: 8b0caa50-9bba-45c4-b4bf-514540894793
keywords:
- API de Windows Biometric Framework de structure de WINBIO_BDB_ANSI_381_HEADER
topic_type:
- apiref
api_name:
- WINBIO_BDB_ANSI_381_HEADER
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9da04643bbdff273a2594394011ba46c16bfa29d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512575"
---
# <a name="winbio_bdb_ansi_381_header-structure"></a>\_Structure d' \_ \_ \_ en-tête WINBIO BDB ANSI 381

La structure d' **\_ \_ \_ \_ en-tête WINBIO BDB ANSI 381** spécifie des informations sur une série d’exemples d’empreintes digitales ou Palm.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _WINBIO_BDB_ANSI_381_HEADER {
  ULONG64                  RecordLength;
  ULONG                    FormatIdentifier;
  ULONG                    VersionNumber;
  WINBIO_REGISTERED_FORMAT ProductId;
  USHORT                   CaptureDeviceId;
  USHORT                   ImageAcquisitionLevel;
  USHORT                   HorizontalScanResolution;
  USHORT                   VerticalScanResolution;
  USHORT                   HorizontalImageResolution;
  USHORT                   VerticalImageResolution;
  UCHAR                    ElementCount;
  UCHAR                    ScaleUnits;
  UCHAR                    PixelDepth;
  UCHAR                    ImageCompressionAlg;
  USHORT                   Reserved;
} WINBIO_BDB_ANSI_381_HEADER;
```



## <a name="members"></a>Membres

<dl> <dt>

**RecordLength**
</dt> <dd>

Taille, en octets, de cette structure plus la taille de toutes les structures d' [**\_ enregistrement WINBIO BDB \_ ANSI \_ 381 \_**](winbio-bdb-ansi-381-record.md) pour les exemples d’empreintes digitales ou Palm capturés par un utilisateur final. Seuls les six octets de poids faible sont valides.

</dd> <dt>

**FormatIdentifier**
</dt> <dd>

Spécifie le format. Actuellement, il doit s’agir de 0x46495200.

</dd> <dt>

**NuméroVersion**
</dt> <dd>

Spécifie le numéro de version. À l’heure actuelle, ce doit être 0x30313000 qui correspond en interne à 0.1.0.0.

</dd> <dt>

**ProductId**
</dt> <dd>

Structure [**de \_ \_ format inscrite WINBIO**](winbio-registered-format.md) qui contient le format de données inscrit sous la forme d’une paire propriétaire/type.

</dd> <dt>

**CaptureDeviceId**
</dt> <dd>

Contient l’ID d’unité de l’appareil utilisé pour capturer l’exemple.

</dd> <dt>

**ImageAcquisitionLevel**
</dt> <dd>

Spécifie le niveau de résolution à partir duquel l’échantillon est capturé.

</dd> <dt>

**HorizontalScanResolution**
</dt> <dd>

Spécifie la résolution horizontale de l’analyse.

</dd> <dt>

**VerticalScanResolution**
</dt> <dd>

Spécifie la résolution verticale de l’analyse.

</dd> <dt>

**HorizontalImageResolution**
</dt> <dd>

Spécifie la résolution horizontale de l’empreinte digitale ou de l’image Palm capturée.

</dd> <dt>

**VerticalImageResolution**
</dt> <dd>

Spécifie la résolution verticale de l’empreinte digitale ou de l’image Palm capturée.

</dd> <dt>

**ElementCount**
</dt> <dd>

Nombre d’enregistrements Finger ou Palm dans cette structure.

</dd> <dt>

**ScaleUnits**
</dt> <dd>

Contient l’unité de mesure, 1 pour les pouces et 2 pour les centimètres.

</dd> <dt>

**PixelDepth**
</dt> <dd>

Spécifie le nombre de bits dans un pixel. Il peut s’agir de 1 à 16 bits par pixel pour la couleur.

</dd> <dt>

**ImageCompressionAlg**
</dt> <dd>

Spécifie l’algorithme utilisé pour compresser l’image de doigt ou Palm.

</dd> <dt>

**Reserved**
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                                    |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                                                       |
| En-tête<br/>                   | <dl> <dt>WinBio \_ types. h (include WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures d’application cliente](client-application-structures.md)
</dt> </dl>

 

 





