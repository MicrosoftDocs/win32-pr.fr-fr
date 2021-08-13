---
title: Énumération BITS_JOB_TRANSFER_POLICY (Deliveryoptimization. h)
description: L’énumération BITS_JOB_TRANSFER_POLICY définit les valeurs d’ID correspondant aux propriétés DO.
ms.assetid: 4811ADBF-F097-4340-BFF2-52CC9556ACF6
keywords:
- Énumération BITS_JOB_TRANSFER_POLICY
- Énumération BITS_JOB_TRANSFER_POLICY
topic_type:
- apiref
api_name:
- BITS_JOB_TRANSFER_POLICY
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 022d12b78416ce4ec84cf02ae8696f17bf5c315a207ae04f28a8980f6aaac073
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118544597"
---
# <a name="bits_job_transfer_policy-enumeration"></a>Énumération BITS_JOB_TRANSFER_POLICY

L’énumération **BITS_JOB_TRANSFER_POLICY** définit les valeurs d’ID correspondant aux propriétés do.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum _BITS_JOB_TRANSFER_POLICY { 
  BITS_JOB_TRANSFER_POLICY_ALWAYS        = 0x800000ff,
  BITS_JOB_TRANSFER_POLICY_NOT_ROAMING   = 0x8000007f,
  BITS_JOB_TRANSFER_POLICY_NO_SURCHARGE  = 0x8000006f,
  BITS_JOB_TRANSFER_POLICY_STANDARD      = 0x80000067,
  BITS_JOB_TRANSFER_POLICY_UNRESTRICTED  = 0x80000021
} BITS_JOB_TRANSFER_POLICY;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="BITS_JOB_TRANSFER_POLICY_ALWAYS"></span><span id="bits_job_transfer_policy_always"></span>**BITS_JOB_TRANSFER_POLICY_ALWAYS**
</dt> <dd>

Spécifie que le travail sera transféré lorsque la connectivité sera disponible, quel que soit le coût.

</dd> <dt>

<span id="BITS_JOB_TRANSFER_POLICY_NOT_ROAMING"></span><span id="bits_job_transfer_policy_not_roaming"></span>**BITS_JOB_TRANSFER_POLICY_NOT_ROAMING**
</dt> <dd>

Spécifie que le travail sera transféré lorsque la connectivité sera disponible, à moins que cette connectivité soit soumise à des surcharges d’itinérance.

</dd> <dt>

<span id="BITS_JOB_TRANSFER_POLICY_NO_SURCHARGE"></span><span id="bits_job_transfer_policy_no_surcharge"></span>**BITS_JOB_TRANSFER_POLICY_NO_SURCHARGE**
</dt> <dd>

Spécifie que le travail sera transféré uniquement lorsque la connectivité est disponible, ce qui n’est pas soumis à une surcharge.

</dd> <dt>

<span id="BITS_JOB_TRANSFER_POLICY_STANDARD"></span><span id="bits_job_transfer_policy_standard"></span>**BITS_JOB_TRANSFER_POLICY_STANDARD**
</dt> <dd>

Spécifie que le travail sera transféré uniquement lorsque la connectivité est disponible, ce qui n’est pas soumis à une surcharge ou à une épuisement proche.

</dd> <dt>

<span id="BITS_JOB_TRANSFER_POLICY_UNRESTRICTED"></span><span id="bits_job_transfer_policy_unrestricted"></span>**BITS_JOB_TRANSFER_POLICY_UNRESTRICTED**
</dt> <dd>

Spécifie que le travail sera transféré uniquement lorsque la connectivité est disponible, ce qui n’impose pas de coûts ou de limites de trafic.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, les applications de bureau version 1709 \[ uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur, version 1709 \[ applications de bureau uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



 

 





