---
description: Les \_ constantes LINEAGENTSTATEEX décrivent l’état d’un agent sur une adresse.
ms.assetid: d49025c5-f1db-4b71-a2d5-1cf3df66f3e5
title: Constantes LINEAGENTSTATEEX_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3f46c00b337a9106165616fe2eaf86bd2b2634b0c113369558953203313d59f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140092"
---
# <a name="lineagentstateex_-constants"></a>\_Constantes LINEAGENTSTATEEX

Les **\_ constantes LINEAGENTSTATEEX** décrivent l’état d’un agent sur une adresse.

<dl> <dt>

<span id="LINEAGENTSTATEEX_BUSYACD"></span><span id="lineagentstateex_busyacd"></span>**LINEAGENTSTATEEX \_ BUSYACD**
</dt> <dd> <dl> <dt>



L’agent est occupé à gérer un appel acheminé à partir d’une file d’attente ACD.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_BUSYINCOMING"></span><span id="lineagentstateex_busyincoming"></span>**LINEAGENTSTATEEX \_ BUSYINCOMING**
</dt> <dd> <dl> <dt>



L’agent est occupé à gérer un appel entrant qui n’a pas été transféré à l’agent à partir d’une file d’attente ACD dans laquelle l’agent est connecté.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_BUSYOUTGOING"></span><span id="lineagentstateex_busyoutgoing"></span>**LINEAGENTSTATEEX \_ BUSYOUTGOING**
</dt> <dd> <dl> <dt>



L’agent est occupé à gérer un appel sortant, tel qu’un itinéraire à partir d’une file d’attente de numérotation prédictive.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_NOTREADY"></span><span id="lineagentstateex_notready"></span>**LINEAGENTSTATEEX \_ NOchapy**
</dt> <dd> <dl> <dt>



L’agent est connecté, mais il est occupé par une tâche autre que le traitement d’un appel (par exemple, en cas d’arrêt). Aucun appel supplémentaire ne doit être acheminé vers l’agent.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_READY"></span><span id="lineagentstateex_ready"></span>**LINEAGENTSTATEEX \_ prêt**
</dt> <dd> <dl> <dt>



L’agent est prêt à accepter les appels.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_RELEASED"></span><span id="lineagentstateex_released"></span>**LINEAGENTSTATEEX \_ libéré**
</dt> <dd> <dl> <dt>



L’agent a été libéré, probablement parce qu’il a été déconnecté.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_UNKNOWN"></span><span id="lineagentstateex_unknown"></span>**LINEAGENTSTATEEX \_ inconnu**
</dt> <dd> <dl> <dt>



L’état de l’agent est actuellement inconnu, mais peut devenir connu ultérieurement. Il peut s’agir d’un état de transition lors de la première ouverture d’une ligne ou d’une adresse.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,2<br/>                                                      |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




