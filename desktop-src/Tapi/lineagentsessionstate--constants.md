---
description: Les \_ constantes LINEAGENTSESSIONSTATE décrivent les différents États de session de l’agent.
ms.assetid: 8a0d06bb-51ba-4eaf-8719-120aed817f63
title: Constantes LINEAGENTSESSIONSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdfd1be8cf846d0e23828f0a3540960a86a83ef1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525463"
---
# <a name="lineagentsessionstate_-constants"></a>\_Constantes LINEAGENTSESSIONSTATE

Les **\_ constantes LINEAGENTSESSIONSTATE** décrivent les différents États de session de l’agent.

<dl> <dt>

<span id="LINEAGENTSESSIONSTATE_BUSYONCALL"></span><span id="lineagentsessionstate_busyoncall"></span>**LINEAGENTSESSIONSTATE \_ BUSYONCALL**
</dt> <dd> <dl> <dt>



L’agent est occupé à gérer un appel.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSESSIONSTATE_BUSYWRAPUP"></span><span id="lineagentsessionstate_busywrapup"></span>**LINEAGENTSESSIONSTATE \_ BUSYWRAPUP**
</dt> <dd> <dl> <dt>



L’agent est occupé à gérer l’encapsulation de l’appel.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSESSIONSTATE_ENDED"></span><span id="lineagentsessionstate_ended"></span>**LINEAGENTSESSIONSTATE \_ terminé**
</dt> <dd> <dl> <dt>



La session de l’agent s’est terminée.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSESSIONSTATE_NOTREADY"></span><span id="lineagentsessionstate_notready"></span>**LINEAGENTSESSIONSTATE \_ NOchapy**
</dt> <dd> <dl> <dt>



L’agent est connecté, mais il est occupé par une tâche autre que le traitement d’un appel (par exemple, en cas d’arrêt). Aucun appel supplémentaire ne doit être acheminé vers l’agent.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSESSIONSTATE_READY"></span><span id="lineagentsessionstate_ready"></span>**LINEAGENTSESSIONSTATE \_ prêt**
</dt> <dd> <dl> <dt>



L’agent est prêt à accepter les appels.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSESSIONSTATE_RELEASED"></span><span id="lineagentsessionstate_released"></span>**LINEAGENTSESSIONSTATE \_ libéré**
</dt> <dd> <dl> <dt>



La session de l’agent a été libérée.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,2<br/>                                                      |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




