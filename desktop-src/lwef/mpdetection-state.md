---
title: Énumération MPDETECTION_STATE (MpClient. h)
description: État de la menace actuellement détectée.
ms.assetid: 293771FF-A210-41D0-88A5-3B52ACAA9295
keywords:
- MPDETECTION_STATE énumération des fonctionnalités d’environnement Windows héritées
- PMPDETECTION_STATE de l’héritage des Windows fonctionnalités d’environnement du pointeur d’énumération
topic_type:
- apiref
api_name:
- MPDETECTION_STATE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0443e0c47eef4d4943d39bd671c28c19db0ff5e1fbe79e5af8d034603b1ab78d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117883516"
---
# <a name="mpdetection_state-enumeration"></a>\_Énumération de l’État MPDETECTION

État de la menace actuellement détectée.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum tagMPDETECTION_STATE { 
  MPDETECTION_STATE_UNKNOWN             = 0,
  MPDETECTION_STATE_ACTIVE              = 1,
  MPDETECTION_STATE_FINISHED            = 2,
  MPDETECTION_STATE_ADDITIONAL_ACTIONS  = 3,
  MPDETECTION_STATE_FAILED              = 4,
  MPDETECTION_STATE_CRITICALLY_FAILED   = 5,
  MPDETECTION_STATE_CLEARED             = 6
} MPDETECTION_STATE, *PMPDETECTION_STATE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MPDETECTION_STATE_UNKNOWN"></span><span id="mpdetection_state_unknown"></span>**État de MPDETECTION \_ \_ inconnu**
</dt> <dd>

Dans un état d’erreur.

</dd> <dt>

<span id="MPDETECTION_STATE_ACTIVE"></span><span id="mpdetection_state_active"></span>**État de MPDETECTION \_ \_ actif**
</dt> <dd>

Menace active.

</dd> <dt>

<span id="MPDETECTION_STATE_FINISHED"></span><span id="mpdetection_state_finished"></span>**État de MPDETECTION \_ \_ terminé**
</dt> <dd>

En attente de 24 heures jusqu’au déplacement jusqu’à la suppression.

</dd> <dt>

<span id="MPDETECTION_STATE_ADDITIONAL_ACTIONS"></span><span id="mpdetection_state_additional_actions"></span>**\_ \_ actions supplémentaires de l’État MPDETECTION \_**
</dt> <dd>

Actions supplémentaires requises.

</dd> <dt>

<span id="MPDETECTION_STATE_FAILED"></span><span id="mpdetection_state_failed"></span>**échec de l’état de MPDETECTION \_ \_**
</dt> <dd>

Échec de la mise à jour non critique.

</dd> <dt>

<span id="MPDETECTION_STATE_CRITICALLY_FAILED"></span><span id="mpdetection_state_critically_failed"></span>**\_ \_ échec critique de l’État MPDETECTION \_**
</dt> <dd>

Échec de la correction critique.

</dd> <dt>

<span id="MPDETECTION_STATE_CLEARED"></span><span id="mpdetection_state_cleared"></span>**\_État MPDETECTION \_ effacé**
</dt> <dd>

La menace n’apparaît pas dans la requête d’État, uniquement dans l’historique.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





