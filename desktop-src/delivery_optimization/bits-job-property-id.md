---
title: Énumération BITS_JOB_PROPERTY_ID (Deliveryoptimization. h)
description: L’énumération BITS_JOB_PROPERTY_ID spécifie l’ID de la propriété pour le travail DO. Cette énumération est utilisée dans l’Union BITS_JOB_PROPERTY_VALUE pour déterminer le type de valeur contenu dans l’Union.
ms.assetid: B0F3C6C2-474F-4FD8-990A-770FAA993550
keywords:
- Énumération BITS_JOB_PROPERTY_ID
topic_type:
- apiref
api_name:
- BITS_JOB_PROPERTY_ID
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 803e776bd635cd600bf664354dda8703d224dffcd63ea751919875a6ea69233d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047147"
---
# <a name="bits_job_property_id-enumeration"></a>Énumération BITS_JOB_PROPERTY_ID

L’énumération **BITS_JOB_PROPERTY_ID** spécifie l’ID de la propriété pour le travail do. Cette énumération est utilisée dans l’Union [**BITS_JOB_PROPERTY_VALUE**](bits-job-property-value-.md) pour déterminer le type de valeur contenu dans l’Union.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum  { 
  BITS_JOB_PROPERTY_ID_COST_FLAGS                     = 1,
  BITS_JOB_PROPERTY_NOTIFICATION_CLSID                = 2,
  BITS_JOB_PROPERTY_DYNAMIC_CONTENT                   = 3,
  BITS_JOB_PROPERTY_HIGH_PERFORMANCE                  = 4,
  BITS_JOB_PROPERTY_MAX_DOWNLOAD_SIZE                 = 5,
  BITS_JOB_PROPERTY_USE_STORED_CREDENTIALS            = 7,
  BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS  = 9,
  BITS_JOB_PROPERTY_ON_DEMAND_MODE                    = 10
} BITS_JOB_PROPERTY_ID;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="BITS_JOB_PROPERTY_ID_COST_FLAGS"></span><span id="bits_job_property_id_cost_flags"></span>**BITS_JOB_PROPERTY_ID_COST_FLAGS**
</dt> <dd>

ID utilisé pour [contrôler le comportement de transfert](https://www.bing.com/search?q=control+transfer+behavior) sur des réseaux cellulaires et/ou similaires. Cette propriété peut être modifiée lorsqu’un transfert est en cours, les nouveaux indicateurs de coût prennent effet immédiatement.

Cette propriété utilise le champ **Dword** **BITS_JOB_PROPERTY_VALUE** s.

</dd> <dt>

<span id="BITS_JOB_PROPERTY_NOTIFICATION_CLSID"></span><span id="bits_job_property_notification_clsid"></span>**BITS_JOB_PROPERTY_NOTIFICATION_CLSID**
</dt> <dd>

ID utilisé pour [inscrire un rappel com](https://www.bing.com/search?q=register+a+COM+callback) par CLSID pour recevoir des notifications sur la progression et l’achèvement d’un travail do. Le CLSID doit faire référence à une classe associée à un serveur COM hors processus inscrit. Elle peut également être définie sur **GUID_NULL** pour effacer un CLSID de notification précédemment défini.

Cette propriété utilise le champ **CLsID** **BITS_JOB_PROPERTY_VALUE** .

</dd> <dt>

<span id="BITS_JOB_PROPERTY_DYNAMIC_CONTENT"></span><span id="bits_job_property_dynamic_content"></span>**BITS_JOB_PROPERTY_DYNAMIC_CONTENT**
</dt> <dd>

Non pris en charge.

</dd> <dt>

<span id="BITS_JOB_PROPERTY_HIGH_PERFORMANCE"></span><span id="bits_job_property_high_performance"></span>**BITS_JOB_PROPERTY_HIGH_PERFORMANCE**
</dt> <dd>

Non pris en charge.

</dd> <dt>

<span id="BITS_JOB_PROPERTY_MAX_DOWNLOAD_SIZE"></span><span id="bits_job_property_max_download_size"></span>**BITS_JOB_PROPERTY_MAX_DOWNLOAD_SIZE**
</dt> <dd>

Non pris en charge.

</dd> <dt>

<span id="BITS_JOB_PROPERTY_USE_STORED_CREDENTIALS"></span><span id="bits_job_property_use_stored_credentials"></span>**BITS_JOB_PROPERTY_USE_STORED_CREDENTIALS**
</dt> <dd>

Non pris en charge.

</dd> <dt>

<span id="BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS"></span><span id="bits_job_property_minimum_notification_interval_ms"></span>**BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS**
</dt> <dd>

Non pris en charge.

</dd> <dt>

<span id="BITS_JOB_PROPERTY_ON_DEMAND_MODE"></span><span id="bits_job_property_on_demand_mode"></span>**BITS_JOB_PROPERTY_ON_DEMAND_MODE**
</dt> <dd>

Non pris en charge.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, les applications de bureau version 1709 \[ uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur, version 1709 \[ applications de bureau uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md)
</dt> <dt>

[**BITS_JOB_PROPERTY_VALUE**](bits-job-property-value-.md)
</dt> <dt>

[**BITS_JOB_TRANSFER_POLICY**](bits-job-transfer-policy-.md)
</dt> <dt>

[**IBackgroundCopyJob5 :: SetProperty**](ibackgroundcopyjob5-setproperty.md)
</dt> <dt>

[**IBackgroundCopyJob5 :: GetProperty**](ibackgroundcopyjob5-getproperty.md)
</dt> </dl>

 

 





