---
title: Structure WINBIO_BDB_ANSI_381_RECORD ( \_ types WINBIO. h)
description: Contient des informations sur une empreinte digitale ou un exemple Palm d’un utilisateur final.
ms.assetid: e0b32d05-3e96-4b42-9e18-57d10513f224
keywords:
- API de Windows Biometric Framework de structure de WINBIO_BDB_ANSI_381_RECORD
topic_type:
- apiref
api_name:
- WINBIO_BDB_ANSI_381_RECORD
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15e30cd66348245aa3090fb21188d7d1cea347c1b28ee51243d2effd9b52609f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119480339"
---
# <a name="winbio_bdb_ansi_381_record-structure"></a>\_Structure d’enregistrement WINBIO BDB \_ ANSI \_ 381 \_

La structure d' **\_ enregistrement WINBIO BDB \_ ANSI \_ 381 \_** contient des informations sur une empreinte digitale ou un exemple Palm d’un utilisateur final. Une collection de ces structures est incluse dans chaque structure d' [**\_ \_ \_ \_ en-tête WINBIO BDB ANSI 381**](winbio-bdb-ansi-381-header.md) .

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _WINBIO_BDB_ANSI_381_RECORD {
  ULONG                    BlockLength;
  USHORT                   HorizontalLineLength;
  USHORT                   VerticalLineLength;
  WINBIO_BIOMETRIC_SUBTYPE Position;
  UCHAR                    CountOfViews;
  UCHAR                    ViewNumber;
  UCHAR                    ImageQuality;
  UCHAR                    ImpressionType;
  UCHAR                    Reserved;
} WINBIO_BDB_ANSI_381_RECORD;
```



## <a name="members"></a>Membres

<dl> <dt>

**BlockLength**
</dt> <dd>

Contient le nombre d’octets dans cette structure, plus le nombre d’octets d’exemples de données d’image.

</dd> <dt>

**HorizontalLineLength**
</dt> <dd>

Spécifie le nombre de pixels sur une ligne horizontale de l’échantillon.

</dd> <dt>

**VerticalLineLength**
</dt> <dd>

Spécifie le nombre de pixels dans une ligne verticale de l’échantillon.

</dd> <dt>

**Position**
</dt> <dd>

Valeur **de \_ sous- \_ type biométrique WINBIO** qui spécifie le doigt ou le Palm utilisé pour générer l’échantillon biométrique. Pour plus d'informations, consultez la section Notes.

</dd> <dt>

**CountOfViews**
</dt> <dd>

Doit être défini sur un (1);

</dd> <dt>

**ViewNumber**
</dt> <dd>

Doit être défini sur un (1);

</dd> <dt>

**ImageQuality**
</dt> <dd>

Réservé. Il doit s’agir de 254 (0xFE).

</dd> <dt>

**ImpressionType**
</dt> <dd>

Réservé.

</dd> <dt>

**Reserved**
</dt> <dd>

Réservé. Doit être défini sur zéro (0).

</dd> </dl>

## <a name="remarks"></a>Remarques

Le membre *position* spécifie la zone de la main ou le Palm utilisé pour créer l’échantillon biométrique. le Windows Biometric Framework (WBF) prend actuellement en charge uniquement la capture d’empreintes digitales et utilise les constantes suivantes pour représenter les informations de position.

-   WINBIO \_ ANSI \_ 381 \_ pos \_ inconnu
-   WINBIO \_ ANSI \_ 381 \_ pos \_ RH \_
-   WINBIO \_ ANSI \_ 381 \_ pos \_ RH \_ index \_ Finger
-   WINBIO \_ ANSI \_ 381 \_ pos \_ hr \_ \_ Finger Middle
-   WINBIO de l' \_ \_ \_ \_ anneau RH \_ du PDV ANSI 381 \_
-   WINBIO \_ ANSI \_ 381 \_ pos \_ RH \_ petit \_ Finger
-   WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_
-   WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ index \_ Finger
-   WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ - \_ Finger
-   \_ \_ Doigt Ring WINBIO ANSI 381 \_ pos \_ LH \_ \_
-   WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ petit \_ doigt
-   WINBIO \_ ANSI \_ 381 \_ pos \_ RH \_ quatre \_ doigts
-   WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ quatre \_ doigts
-   WINBIO \_ ANSI \_ 381 \_ pos \_ deux \_ pouces

> [!IMPORTANT]
>
> N’essayez pas de valider la valeur fournie pour la valeur de *position* . le Service de biométrie Windows validera la valeur fournie avant de la passer à votre implémentation. Si la valeur est **WINBIO \_ sous-type \_ aucune \_ information** ou **WINBIO sous- \_ type \_ any**, validez le cas échéant.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                                    |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                                       |
| En-tête<br/>                   | <dl> <dt>WinBio \_ types. h (include WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures d’application cliente](client-application-structures.md)
</dt> </dl>

 

 





