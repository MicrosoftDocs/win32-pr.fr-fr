---
description: Les \_ constantes d’indicateur de bit LINECALLREASON décrivent la raison d’un appel.
ms.assetid: 16278146-886f-433a-afe5-64f4894b1428
title: Constantes LINECALLREASON_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab6d2411c652c13add1620ca6029cabbf2b878e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523889"
---
# <a name="linecallreason_-constants"></a>\_Constantes LINECALLREASON

Les constantes d’indicateur de bit **LINECALLREASON \_** décrivent la raison d’un appel.

<dl> <dt>

<span id="LINECALLREASON_CALLCOMPLETION"></span><span id="linecallreason_callcompletion"></span>**LINECALLREASON \_ CALLCOMPLETION**
</dt> <dd> <dl> <dt>



L’appel était le résultat d’une demande d’achèvement d’appel.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_CAMPEDON"></span><span id="linecallreason_campedon"></span>**LINECALLREASON \_ CAMPEDON**
</dt> <dd> <dl> <dt>



L’appel a été campé sur l’adresse. En règle générale, il apparaît initialement dans l’État onHold et peut être remplacé par [**lineSwapHold**](/windows/desktop/api/Tapi/nf-tapi-lineswaphold). Si un appel actif devient inactif, l’appel d’activation peut passer à l’état de l’offre et à la sonnerie de démarrage de l’appareil.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_DIRECT"></span><span id="linecallreason_direct"></span>**LINECALLREASON \_ direct**
</dt> <dd> <dl> <dt>



Il s’agit d’un appel direct entrant ou sortant.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_FWDBUSY"></span><span id="linecallreason_fwdbusy"></span>**LINECALLREASON \_ FWDBUSY**
</dt> <dd> <dl> <dt>



Cet appel a été transféré à partir d’une autre extension qui était occupée au moment de l’appel.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_FWDNOANSWER"></span><span id="linecallreason_fwdnoanswer"></span>**LINECALLREASON \_ FWDNOANSWER**
</dt> <dd> <dl> <dt>



L’appel a été transféré à partir d’une autre extension qui n’a pas répondu à l’appel après un certain nombre d’anneaux.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_FWDUNCOND"></span><span id="linecallreason_fwduncond"></span>**LINECALLREASON \_ FWDUNCOND**
</dt> <dd> <dl> <dt>



L’appel a été transféré sans condition à partir d’un autre nombre.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_INTRUDE"></span><span id="linecallreason_intrude"></span>**LINECALLREASON \_ intrus**
</dt> <dd> <dl> <dt>



L’appel a été effectué sur la ligne, soit par une action d’achèvement d’appel appelée par une autre station, soit par une action de l’opérateur. Selon l’implémentation du commutateur, l’appel peut apparaître dans l’état connecté ou être associé à un appel actif existant sur la ligne.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_PARKED"></span><span id="linecallreason_parked"></span>**LINECALLREASON \_ parqué**
</dt> <dd> <dl> <dt>



L’appel a été parqué sur l’adresse. En règle générale, il apparaît initialement dans l’État onHold.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_PICKUP"></span><span id="linecallreason_pickup"></span>**\_collecte LINECALLREASON**
</dt> <dd> <dl> <dt>



L’appel a été récupéré à partir d’une autre extension.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_REDIRECT"></span><span id="linecallreason_redirect"></span>**redirection LINECALLREASON \_**
</dt> <dd> <dl> <dt>



L’appel a été redirigé vers cette station.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_REMINDER"></span><span id="linecallreason_reminder"></span>**\_rappel LINECALLREASON**
</dt> <dd> <dl> <dt>



L’appel est un rappel (ou « rappel ») que l’utilisateur a un appel parqué ou bloqué pendant (potentiellement) un long moment.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_ROUTEREQUEST"></span><span id="linecallreason_routerequest"></span>**LINECALLREASON \_ ROUTEREQUEST**
</dt> <dd> <dl> <dt>



L’appel apparaît sur l’adresse, car le commutateur a besoin d’instructions de routage de l’application. L’application doit examiner le membre **CalledID** dans [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)et utiliser la fonction [**lineRedirect**](/windows/desktop/api/Tapi/nf-tapi-lineredirect) pour fournir une nouvelle adresse de numérotation pour l’appel. Si l’appel doit être bloqué à la place, l’application peut appeler [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop). Si l’application ne parvient pas à effectuer d’action dans un délai défini par le commutateur, une action par défaut est effectuée. Un fournisseur de services peut utiliser cette constante uniquement si la version négociée sur la ligne est 2,0 ou supérieure. Dans le cas contraire, le fournisseur de services doit substituer LINECALLREASON \_ .


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_TRANSFER"></span><span id="linecallreason_transfer"></span>**\_transfert LINECALLREASON**
</dt> <dd> <dl> <dt>



L’appel a été transféré à partir d’un autre nombre.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_UNAVAIL"></span><span id="linecallreason_unavail"></span>**LINECALLREASON \_ INdispo**
</dt> <dd> <dl> <dt>



La raison de l’appel n’est pas disponible et ne sera pas connue ultérieurement.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_UNKNOWN"></span><span id="linecallreason_unknown"></span>**LINECALLREASON \_ inconnu**
</dt> <dd> <dl> <dt>



La raison de l’appel est actuellement inconnue, mais peut devenir connue ultérieurement.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_UNPARK"></span><span id="linecallreason_unpark"></span>**déspark LINECALLREASON \_**
</dt> <dd> <dl> <dt>



L’appel a été récupéré en tant qu’appel parqué.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Aucune extensibilité. Tous les 32 bits sont réservés.

Les \_ constantes LINECALLREASON sont utilisées dans le membre **dwReason** de la structure de données [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)
</dt> <dt>

[**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop)
</dt> <dt>

[**lineRedirect**](/windows/desktop/api/Tapi/nf-tapi-lineredirect)
</dt> <dt>

[**lineSwapHold**](/windows/desktop/api/Tapi/nf-tapi-lineswaphold)
</dt> </dl>

 

 




