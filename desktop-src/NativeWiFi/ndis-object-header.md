---
description: Empaquette les informations relatives au type d’objet, à la version et à la taille requises dans de nombreuses structures NDIS 6,0.
ms.assetid: 0dfb6022-1d8d-4bd9-bde3-2ee6d683f223
title: Structure NDIS_OBJECT_HEADER (Ntddndis. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDIS_OBJECT_HEADER
api_type:
- HeaderDef
api_location:
- ntddndis.h
ms.openlocfilehash: fe28a87eeb1457bace0b72a386bcb07667b24a64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544836"
---
# <a name="ndis_object_header-structure"></a>\_Structure d' \_ en-tête d’objet NDIS

La structure d' **\_ \_ en-tête d’objet NDIS** conditionne le type d’objet, la version et les informations de taille requis dans de nombreuses structures NDIS 6,0.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _NDIS_OBJECT_HEADER {
  UCHAR  Type;
  UCHAR  Revision;
  USHORT Size;
} NDIS_OBJECT_HEADER, *PNDIS_OBJECT_HEADER;
```



## <a name="members"></a>Membres

<dl> <dt>

**Type**
</dt> <dd>

Spécifie le type d’objet NDIS décrit par une structure.

</dd> <dt>

**Faisant**
</dt> <dd>

Spécifie le numéro de révision de cette structure.

</dd> <dt>

**Taille**
</dt> <dd>

Spécifie la taille totale, en octets, de la structure NDIS qui contient **l' \_ \_ en-tête d’objet NDIS**. Cette taille comprend la taille du membre **d' \_ \_ en-tête d’objet NDIS** et de tous les autres membres de la structure.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista, Windows XP avec les \[ applications de bureau SP3 uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                                       |
| Composant redistribuable<br/>          | API de réseau local sans fil pour Windows XP avec SP2<br/>                                                        |
| En-tête<br/>                   | <dl> <dt>Ntddndis. h (inclure Windot11. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Liste des BSSID DOT11 \_**](dot11-bssid-list.md)
</dt> </dl>

 

 




