---
description: Les \_ constantes LINEAGENTSTATE décrivent l’état d’un agent sur une adresse.
ms.assetid: 1dbc33e7-05cc-4cb9-8904-f495b884b8db
title: Constantes LINEAGENTSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 001b760a5b566089814195b11fc39dc356a3444f5c5dc6ee26e71a471e26e338
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140112"
---
# <a name="lineagentstate_-constants"></a>\_Constantes LINEAGENTSTATE

Les **\_ constantes LINEAGENTSTATE** décrivent l’état d’un agent sur une adresse.

<dl> <dt>

<span id="LINEAGENTSTATE_BUSYACD"></span><span id="lineagentstate_busyacd"></span>**LINEAGENTSTATE \_ BUSYACD**
</dt> <dd> <dl> <dt>



L’agent est occupé à gérer un appel acheminé à partir d’une file d’attente ACD.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_BUSYINCOMING"></span><span id="lineagentstate_busyincoming"></span>**LINEAGENTSTATE \_ BUSYINCOMING**
</dt> <dd> <dl> <dt>



L’agent est occupé à gérer un appel entrant qui n’a pas été transféré à l’agent à partir d’une file d’attente ACD dans laquelle l’agent est connecté.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_BUSYOTHER"></span><span id="lineagentstate_busyother"></span>**LINEAGENTSTATE \_ BUSYOTHER**
</dt> <dd> <dl> <dt>



L’agent est occupé à gérer un autre type d’appel, tel qu’un appel personnel sortant non transféré à l’agent par un numéroteur prédictif. Cette valeur peut également être utilisée lorsque l’agent est connu pour être occupé sur un appel, mais que le type d’appel est inconnu.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_BUSYOUTBOUND"></span><span id="lineagentstate_busyoutbound"></span>**LINEAGENTSTATE \_ BUSYOUTBOUND**
</dt> <dd> <dl> <dt>



L’agent est occupé à gérer un appel sortant, tel qu’un itinéraire à partir d’une file d’attente de numérotation prédictive.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_LOGGEDOFF"></span><span id="lineagentstate_loggedoff"></span>**LINEAGENTSTATE \_ LOGGEDOFF**
</dt> <dd> <dl> <dt>



Aucun agent n’est connecté à l’adresse.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_NOTREADY"></span><span id="lineagentstate_notready"></span>**LINEAGENTSTATE \_ NOchapy**
</dt> <dd> <dl> <dt>



L’agent est connecté, mais il est occupé par une tâche autre que le traitement d’un appel (par exemple, en cas d’arrêt). Aucun appel supplémentaire ne doit être acheminé vers l’agent.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_READY"></span><span id="lineagentstate_ready"></span>**LINEAGENTSTATE \_ prêt**
</dt> <dd> <dl> <dt>



L’agent est prêt à accepter les appels.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_UNAVAIL"></span><span id="lineagentstate_unavail"></span>**LINEAGENTSTATE \_ INdispo**
</dt> <dd> <dl> <dt>



L’état de l’agent est inconnu et ne devient jamais connu. Dans [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus), cette condition peut également être représentée par le membre **dwAgentState** qui a la valeur 0.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_UNKNOWN"></span><span id="lineagentstate_unknown"></span>**LINEAGENTSTATE \_ inconnu**
</dt> <dd> <dl> <dt>



L’état de l’agent est actuellement inconnu, mais peut devenir connu ultérieurement. Il peut s’agir d’un état de transition lors de la première ouverture d’une ligne ou d’une adresse.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_WORKINGAFTERCALL"></span><span id="lineagentstate_workingaftercall"></span>**LINEAGENTSTATE \_ WORKINGAFTERCALL**
</dt> <dd> <dl> <dt>



L’agent a terminé l’appel précédent, mais il est toujours occupé par le travail associé à cet appel. L’agent ne doit pas recevoir d’appels supplémentaires.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Remarques

Les 16 bits supérieurs de cet ensemble de constantes sont réservés aux extensions spécifiques à l’appareil.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




