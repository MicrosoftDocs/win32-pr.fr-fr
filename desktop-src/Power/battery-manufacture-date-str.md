---
description: Contient la date de fabrication d’une batterie.
ms.assetid: 0cda66fc-bf4a-4a38-b43c-6eecde46c414
title: Structure BATTERY_MANUFACTURE_DATE (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_MANUFACTURE_DATE
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: 30a70fed151304d189fa91b20106e1154ca0e9f4ea5225c52bf1023dbd218346
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032969"
---
# <a name="battery_manufacture_date-structure"></a>Structure de date de la fabrication de la batterie \_ \_

Contient la date de fabrication d’une batterie. Cette structure est utilisée par la structure d' [**\_ \_ informations sur les requêtes de batterie**](battery-query-information-str.md) lorsque le niveau d’information BatteryManufactureDate est demandé.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _BATTERY_MANUFACTURE_DATE {
  UCHAR  Day;
  UCHAR  Month;
  USHORT Year;
} BATTERY_MANUFACTURE_DATE, *PBATTERY_MANUFACTURE_DATE;
```



## <a name="members"></a>Membres

<dl> <dt>

**Jour**
</dt> <dd>

Jour du mois de fabrication, compris entre 1 et 31. En dépit du type de données, il ne s’agit pas d’une valeur encodée en ASCII. Il s’agit d’un octet non signé.

</dd> <dt>

**Month**
</dt> <dd>

Mois de fabrication, dans la plage comprise entre 1 (janvier) et 12 (décembre). En dépit du type de données, il ne s’agit pas d’une valeur encodée en ASCII. Il s’agit d’un octet non signé.

</dd> <dt>

**Year**
</dt> <dd>

Année de fabrication. Il se trouve généralement dans la plage 1900-2100.

</dd> </dl>

## <a name="remarks"></a>Remarques

La date est encodée au format grégorien ou occidental.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                                                                                                                                                                                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                                                                                                                                                                                |
| En-tête<br/>                   | <dl> <dt>Poclass. h ;</dt> <dt>Batclass. h sur Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 et Windows XP</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_informations sur la requête de batterie \_**](battery-query-information-str.md)
</dt> <dt>

[**\_ \_ informations sur les requêtes de batterie IOCTL \_**](ioctl-battery-query-information.md)
</dt> </dl>

 

 




