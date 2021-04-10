---
title: Structure BITS_JOB_PROPERTY_VALUE (Deliveryoptimization. h)
description: L’BITS_JOB_PROPERTY_VALUE Union fournit la valeur de propriété du travail DO en fonction de la valeur de l’énumération BITS_JOB_PROPERTY_ID.
ms.assetid: C24D9EA1-2E72-4403-939A-7B01D7133FE7
keywords:
- Structure BITS_JOB_PROPERTY_VALUE
- Structure BITS_JOB_PROPERTY_VALUE
topic_type:
- apiref
api_name:
- BITS_JOB_PROPERTY_VALUE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c48c1fe550db51b6b838379d44df21c95fa95e41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103663"
---
# <a name="bits_job_property_value-structure"></a>Structure BITS_JOB_PROPERTY_VALUE

L' **BITS_JOB_PROPERTY_VALUE** Union fournit la valeur de propriété du travail do en fonction de la valeur de l’énumération [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) .

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  DWORD          Dword;
  GUID           ClsID;
  BOOL           Enable;
  UINT64         Uint64;
  BG_AUTH_TARGET Target;
} BITS_JOB_PROPERTY_VALUE;
```



## <a name="members"></a>Membres

<dl> <dt>

**Grande**
</dt> <dd>

Cette valeur est retournée en cas d’utilisation de l’ID de propriété d’énumération **BITS_JOB_PROPERTY_ID_COST_FLAGS** et est appliquée comme [stratégie de transfert](https://www.bing.com/search?q=transfer+policy) sur le travail do.

</dd> <dt>

**Identificateur**
</dt> <dd>

Cette valeur est retournée en cas d’utilisation de l’ID de propriété enum **BITS_JOB_PROPERTY_NOTIFICATION_CLSID** et représente le CLSID de l’objet de rappel à inscrire avec le travail do.

</dd> <dt>

**Activer**
</dt> <dd>

Non pris en charge.

</dd> <dt>

**Uint64**
</dt> <dd>

Non pris en charge.

</dd> <dt>

**Cible**
</dt> <dd>

Non pris en charge.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 10, version 1709 \[ uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Server, version 1709, \[ applications de bureau uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md)
</dt> <dt>

[**BITS_JOB_TRANSFER_POLICY**](bits-job-transfer-policy-.md)
</dt> </dl>

 

 





