---
title: Structure MPCALLBACK_DATA (MpClient. h)
description: Données passées à la fonction de rappel.
ms.assetid: EA8E6C1E-F80B-4247-B073-C78D49A354CF
keywords:
- fonctionnalités d’environnement Windows héritées de la structure MPCALLBACK_DATA
- PMPCALLBACK_DATA des fonctionnalités d’environnement du pointeur de structure Windows hérité
topic_type:
- apiref
api_name:
- MPCALLBACK_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d1eb129101c341485a1e6b5763a0325cbf586a6e51e5e2875b4465696c39df8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117883651"
---
# <a name="mpcallback_data-structure"></a>\_Structure de données MPCALLBACK

Données passées à la fonction de rappel.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagMPCALLBACK_DATA {
  MPNOTIFY        Notify;
  HRESULT         hResult;
  ULARGE_INTEGER  TimeStamp;
  MPCALLBACK_TYPE Type;
  union {
    PMPSTATUS_DATA         pStatusData;
    PMPSCAN_DATA           pScanData;
    PMPCLEAN_DATA          pCleanData;
    PMPCLEAN_PRECHECK_DATA pPrecheckData;
    PMPTHREAT_DATA         pThreatData;
    PMPSIGUPDATE_DATA      pSigUpdateData;
    PMPSAMPLE_DATA         pSampleData;
    PMPRESERVED_DATA       pReservedData;
    PMPCONFIGURATION_DATA  pConfigurationData;
    PMPFASTPATH_DATA       pFastPathData;
    PMPEXPIRATION_DATA     pExpirationData;
    PMPNIS_PRIVATE_DATA    pNISPrivateData;
    PMPHEALTH_DATA         pHealthData;
    PMPENDOFLIFE_DATA      pEndOfLifeData;
    PMPMALWARETOAST_DATA   pMalwareToastData;
  } Data;
} MPCALLBACK_DATA, *PMPCALLBACK_DATA;
```



## <a name="members"></a>Membres

<dl> <dt>

**Notifier**
</dt> <dd>

Type : **[ **MPNOTIFY**](mpnotify.md)**

</dd> <dd>

Notification de modification au rapport.

</dd> <dt>

**Signé**
</dt> <dd>

Type : **HRESULT**

</dd> <dd>

Code d’erreur, en cas de défaillance interne.

</dd> <dt>

**Confirmé**
</dt> <dd>

Type : **\_ entier ULARGE**

</dd> <dd>

Horodatage actuel.

</dd> <dt>

**Type**
</dt> <dd>

Type : **[ **MPCALLBACK \_**](mpcallback-type.md)**

</dd> <dd>

Type de données spécial de rappel.

</dd> <dt>

**Données**
</dt> <dd>

Données spéciales de rappel. Le pointeur vers la structure appropriée dépend de la valeur de **type**.

<dl> <dt>

**pStatusData**
</dt> <dd>

Type : **\_ données PMPSTATUS**

</dd> <dd>

Lorsque le **type**  ==  **MPCALLBACK est \_ Status**. Consultez [**\_ données MPSTATUS**](mpstatus-data.md).

</dd> <dt>

**pScanData**
</dt> <dd>

Type : **\_ données PMPSCAN**

</dd> <dd>

Lorsque le **type**  ==  **MPCALLBACK \_ Scan**. Consultez [**\_ données MPSCAN**](mpscan-data.md).

</dd> <dt>

**pCleanData**
</dt> <dd>

Type : **\_ données PMPCLEAN**

</dd> <dd>

Lorsque le **type**  ==  **MPCALLBACK \_ Clean**. Consultez [**\_ données MPCLEAN**](mpclean-data.md).

</dd> <dt>

**pPrecheckData**
</dt> <dd>

Type : **PMPCLEAN \_ prévérifier les \_ données**

</dd> <dd>

Quand le **type** est  ==  **MPCALLBACK \_ précheck**. Consultez [**MPCLEAN \_ prévérifier les \_ données**](mpclean-precheck-data.md).

</dd> <dt>

**pThreatData**
</dt> <dd>

Type : **\_ données PMPTHREAT**

</dd> <dd>

Lorsque le **type**  ==  **MPCALLBACK \_ menace**. Consultez [**\_ données MPTHREAT**](mpthreat-data.md).

</dd> <dt>

**pSigUpdateData**
</dt> <dd>

Type : **\_ données PMPSIGUPDATE**

</dd> <dd>

Lorsque le **type** est  ==  **MPCALLBACK \_ SIGUPDATE**. Consultez [**\_ données MPSIGUPDATE**](mpsigupdate-data.md).

</dd> <dt>

**pSampleData**
</dt> <dd>

Type : **\_ données PMPSAMPLE**

</dd> <dd>

Lorsque **type**  ==  **MPCALLBACK \_ Sample**. Consultez [**\_ données MPSAMPLE**](mpsample-data.md).

</dd> <dt>

**pReservedData**
</dt> <dd>

Type : **\_ données PMPRESERVED**

</dd> <dd>

Lorsque le **type**  ==  **MPCALLBACK est \_ réservé**. Consultez [**\_ données MPRESERVED**](mpreserved-data.md).

</dd> <dt>

**pConfigurationData**
</dt> <dd>

Type : **\_ données PMPCONFIGURATION**

</dd> <dd>

Lorsque le **type** est  ==  **\_ \_ notification de configuration MPCALLBACK**. Consultez [**\_ données MPCONFIGURATION**](mpconfiguration-data.md).

</dd> <dt>

**pFastPathData**
</dt> <dd>

Type : **\_ données PMPFASTPATH**

</dd> <dd>

Lorsque le **type** est  ==  **MPCALLBACK \_ FASTPATH**. Consultez [**\_ données MPFASTPATH**](mpfastpath-data.md).

</dd> <dt>

**pExpirationData**
</dt> <dd>

Type : **\_ données PMPEXPIRATION**

</dd> <dd>

Lorsque **tapez**  ==  **MPCALLBACK \_ \_ expiration du produit**. Consultez [**\_ données MPEXPIRATION**](mpexpiration-data.md).

</dd> <dt>

**pNISPrivateData**
</dt> <dd>

Type : **PMPNIS \_ Private \_ Data**

</dd> <dd>

Lorsque **tapez**  ==  **MPCALLBACK \_ NIS \_ Private**. Consultez [**MPNIS \_ Private \_ Data**](mpnis-private-data.md).

</dd> <dt>

**pHealthData**
</dt> <dd>

Type : **\_ données PMPHEALTH**

</dd> <dd>

Lorsque le **type**  ==  **MPCALLBACK \_ Health**. Consultez [**\_ données MPHEALTH**](mphealth-data.md).

</dd> <dt>

**pEndOfLifeData**
</dt> <dd>

Type : **\_ données PMPENDOFLIFE**

</dd> <dd>

Lorsque le **type** est  ==  **MPCALLBACK \_ ENDOFLIFE**. Consultez [**\_ données MPENDOFLIFE**](mpendoflife-data.md).

</dd> <dt>

**pMalwareToastData**
</dt> <dd>

Type : **\_ données PMPMALWARETOAST**

</dd> <dd>

Lorsque le **type** est  ==  **MPCALLBACK \_ MALWARETOAST**. Consultez [**\_ données MPMALWARETOAST**](mpmalwaretoast-data.md).

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_type MPCALLBACK**](mpcallback-type.md)
</dt> <dt>

[**\_données MPCLEAN**](mpclean-data.md)
</dt> <dt>

[**MPCLEAN les données de la \_ PRÉvérification \_**](mpclean-precheck-data.md)
</dt> <dt>

[**\_données MPCONFIGURATION**](mpconfiguration-data.md)
</dt> <dt>

[**\_données MPENDOFLIFE**](mpendoflife-data.md)
</dt> <dt>

[**\_données MPEXPIRATION**](mpexpiration-data.md)
</dt> <dt>

[**\_données MPFASTPATH**](mpfastpath-data.md)
</dt> <dt>

[**\_données MPHEALTH**](mphealth-data.md)
</dt> <dt>

[**\_données MPMALWARETOAST**](mpmalwaretoast-data.md)
</dt> <dt>

[**\_données privées \_ MPNIS**](mpnis-private-data.md)
</dt> <dt>

[**MPNOTIFY**](mpnotify.md)
</dt> <dt>

[**\_données MPRESERVED**](mpreserved-data.md)
</dt> <dt>

[**\_données MPSAMPLE**](mpsample-data.md)
</dt> <dt>

[**\_données MPSCAN**](mpscan-data.md)
</dt> <dt>

[**\_données MPSIGUPDATE**](mpsigupdate-data.md)
</dt> <dt>

[**\_données MPSTATUS**](mpstatus-data.md)
</dt> <dt>

[**\_données MPTHREAT**](mpthreat-data.md)
</dt> </dl>

 

 





