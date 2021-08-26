---
description: La \_ structure Job info \_ 3 permet de lier un ensemble de travaux d’impression.
ms.assetid: a110f555-dc33-450c-ae77-ea26f0f69448
title: Structure JOB_INFO_3 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JOB_INFO_3
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 111b292c5f355aceefa95fb01bafc2cb9220757618d39d4b3ca29bbf77ca4570
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119948679"
---
# <a name="job_info_3-structure"></a>\_Structure des informations sur le travail \_ 3

La structure **Job \_ info \_ 3** permet de lier un ensemble de travaux d’impression.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _JOB_INFO_3 {
  DWORD JobId;
  DWORD NextJobId;
  DWORD Reserved;
} JOB_INFO_3, *PJOB_INFO_3;
```



## <a name="members"></a>Membres

<dl> <dt>

**JobId**
</dt> <dd>

Identificateur du travail d’impression.

</dd> <dt>

**NextJobId**
</dt> <dd>

Identificateur du travail d’impression pour le travail d’impression suivant dans l’ensemble lié de travaux d’impression.

</dd> <dt>

**Reserved**
</dt> <dd>

Cette valeur est réservée à une utilisation ultérieure. Vous devez la définir sur zéro.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Structures de l’API du spouleur d’impression](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumJobs**](enumjobs.md)
</dt> <dt>

[**GetJob**](getjob.md)
</dt> <dt>

[**SetJob**](setjob.md)
</dt> </dl>

 

 




