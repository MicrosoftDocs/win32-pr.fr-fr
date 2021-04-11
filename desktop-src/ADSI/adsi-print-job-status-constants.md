---
title: Constantes d’État du travail d’impression ADSI (Adssts. h)
description: Les constantes suivantes sont utilisées avec la propriété IADsPrintJobOperations. Status pour indiquer l’état d’un travail d’impression.
ms.assetid: 44a981cc-1098-4b6d-8332-e678953c9112
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- ADS_JOB_PAUSED
- ADS_JOB_ERROR
- ADS_JOB_DELETING
- ADS_JOB_SPOOLING
- ADS_JOB_PRINTING
- ADS_JOB_OFFLINE
- ADS_JOB_PAPEROUT
- ADS_JOB_PRINTED
- ADS_JOB_DELETED
api_location:
- Adssts.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c51e83393aa0322ef142ee45b4a893f980293ded
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942574"
---
# <a name="adsi-print-job-status-constants"></a>Constantes d’État du travail d’impression ADSI

Les constantes suivantes sont utilisées avec la propriété [**IADsPrintJobOperations. Status**](iadsprintjoboperations-property-methods.md) pour indiquer l’état d’un travail d’impression.

<dl> <dt>

<span id="ADS_JOB_PAUSED"></span><span id="ads_job_paused"></span>**\_travail ADS \_ suspendu**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Le travail d'impression est suspendu.


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_ERROR"></span><span id="ads_job_error"></span>**\_erreur de tâche ADS \_**
</dt> <dd> <dl> <dt>

2 (0X2)
</dt> <dt>



Une erreur est survenue.


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_DELETING"></span><span id="ads_job_deleting"></span>**suppression d’un \_ travail ADS \_**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



Le travail d’impression est en cours de suppression.


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_SPOOLING"></span><span id="ads_job_spooling"></span>**mise en file d’attente des \_ travaux ADS \_**
</dt> <dd> <dl> <dt>

8 (0x8)
</dt> <dt>



Le travail d’impression est mis en attente.


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_PRINTING"></span><span id="ads_job_printing"></span>**\_impression des travaux ADS \_**
</dt> <dd> <dl> <dt>

16 (0x10)
</dt> <dt>



Le travail d’impression est en cours d’impression.


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_OFFLINE"></span><span id="ads_job_offline"></span>**\_travail ADS \_ hors connexion**
</dt> <dd> <dl> <dt>

32 (0x20)
</dt> <dt>



L'imprimante est hors connexion.


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_PAPEROUT"></span><span id="ads_job_paperout"></span>**\_PAPEROUT de travail ADS \_**
</dt> <dd> <dl> <dt>

64 (0x40)
</dt> <dt>



L’imprimante n’est plus imprimée.


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_PRINTED"></span><span id="ads_job_printed"></span>**\_travail ADS \_ imprimé**
</dt> <dd> <dl> <dt>

128 (0x80)
</dt> <dt>



Le travail d’impression a été imprimé.


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_DELETED"></span><span id="ads_job_deleted"></span>**\_travail ADS \_ supprimé**
</dt> <dd> <dl> <dt>

256 (0x100)
</dt> <dt>



Le travail d’impression a été supprimé.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Adssts. h</dt> </dl> |



 

 





