---
title: Énumération MPCALLBACK_TYPE (MpClient. h)
description: Types de rappel possibles.
ms.assetid: 8E4F50B7-0F02-434D-B91E-C9966C92CDC0
keywords:
- MPCALLBACK_TYPE énumération des fonctionnalités d’environnement Windows héritées
- PMPCALLBACK_TYPE des fonctionnalités d’environnement Windows héritées d’un pointeur d’énumération
topic_type:
- apiref
api_name:
- MPCALLBACK_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a3fd310f3733d36dd92ace1c7a5286bcf73a75f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464911"
---
# <a name="mpcallback_type-enumeration"></a>\_Énumération de type MPCALLBACK

Types de rappel possibles.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum tagMPCALLBACK_TYPE { 
  MPCALLBACK_UNKNOWN                     = 0,
  MPCALLBACK_STATUS                      = 1,
  MPCALLBACK_THREAT                      = 2,
  MPCALLBACK_SCAN                        = 3,
  MPCALLBACK_CLEAN                       = 4,
  MPCALLBACK_PRECHECK                    = 5,
  MPCALLBACK_SIGUPDATE                   = 6,
  MPCALLBACK_SAMPLE                      = 7,
  MPCALLBACK_RESERVED                    = 8,
  MPCALLBACK_CONFIGURATION_NOTIFICATION  = 9,
  MPCALLBACK_FASTPATH                    = 10,
  MPCALLBACK_PRODUCT_EXPIRATION          = 11,
  MPCALLBACK_NIS_PRIVATE                 = 12,
  MPCALLBACK_HEALTH                      = 13,
  MPCALLBACK_ENDOFLIFE                   = 14,
  MPCALLBACK_MALWARETOAST                = 15,
  MPCALLBACK_MAXVALUE                    = 15
} MPCALLBACK_TYPE, *PMPCALLBACK_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MPCALLBACK_UNKNOWN"></span><span id="mpcallback_unknown"></span>**MPCALLBACK \_ inconnu**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_STATUS"></span><span id="mpcallback_status"></span>**État de MPCALLBACK \_**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_THREAT"></span><span id="mpcallback_threat"></span>**\_menace MPCALLBACK**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_SCAN"></span><span id="mpcallback_scan"></span>**\_analyse MPCALLBACK**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_CLEAN"></span><span id="mpcallback_clean"></span>**MPCALLBACK \_ nettoyer**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_PRECHECK"></span><span id="mpcallback_precheck"></span>**prévérification MPCALLBACK \_**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_SIGUPDATE"></span><span id="mpcallback_sigupdate"></span>**MPCALLBACK \_ SIGUPDATE**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_SAMPLE"></span><span id="mpcallback_sample"></span>**\_exemple MPCALLBACK**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_RESERVED"></span><span id="mpcallback_reserved"></span>**MPCALLBACK \_ réservé**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_CONFIGURATION_NOTIFICATION"></span><span id="mpcallback_configuration_notification"></span>**\_notification de configuration MPCALLBACK \_**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_FASTPATH"></span><span id="mpcallback_fastpath"></span>**MPCALLBACK \_ FASTPATH**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_PRODUCT_EXPIRATION"></span><span id="mpcallback_product_expiration"></span>**\_expiration du produit MPCALLBACK \_**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_NIS_PRIVATE"></span><span id="mpcallback_nis_private"></span>**MPCALLBACK \_ NIS \_ privé**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_HEALTH"></span><span id="mpcallback_health"></span>**\_intégrité MPCALLBACK**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_ENDOFLIFE"></span><span id="mpcallback_endoflife"></span>**MPCALLBACK \_ ENDOFLIFE**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_MALWARETOAST"></span><span id="mpcallback_malwaretoast"></span>**MPCALLBACK \_ MALWARETOAST**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_MAXVALUE"></span><span id="mpcallback_maxvalue"></span>**MPCALLBACK \_ MaxValue**
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





