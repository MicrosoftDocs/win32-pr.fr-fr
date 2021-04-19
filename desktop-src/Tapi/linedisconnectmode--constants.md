---
description: Les \_ constantes d’indicateur de bit LINEDISCONNECTMODE décrivent les différentes raisons d’une demande de déconnexion distante. Un mode de déconnexion est disponible en tant qu’État d’appel à l’application une fois que l’état d’appel passe à déconnecté.
ms.assetid: 1b26f13c-b0bf-4d2c-8514-f0c376e36bcd
title: Constantes LINEDISCONNECTMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c70ba70175685e2c264343f9345227ee64c206f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540026"
---
# <a name="linedisconnectmode_-constants"></a>\_Constantes LINEDISCONNECTMODE

Les constantes d’indicateur de bit **LINEDISCONNECTMODE \_** décrivent les différentes raisons d’une demande de déconnexion distante. Un mode de déconnexion est disponible en tant qu’État d’appel à l’application une fois que l’état d’appel passe à déconnecté.

<dl> <dt>

<span id="LINEDISCONNECTMODE_BADADDRESS"></span><span id="linedisconnectmode_badaddress"></span>**LINEDISCONNECTMODE \_ BADADDRESS**
</dt> <dd> <dl> <dt>



L’adresse de destination n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_BLOCKED"></span><span id="linedisconnectmode_blocked"></span>**LINEDISCONNECTMODE \_ bloqué**
</dt> <dd> <dl> <dt>



L’appel n’a pas pu être connecté, car les appels à partir de l’adresse d’origine ne sont pas acceptés à l’adresse de destination. Cela diffère de LINEDISCONNECTMODE \_ Reject dans ce blocage qui est implémenté dans le réseau (un rejet passif), tandis qu’un rejet est implémenté dans l’équipement de destination (un rejet actif). Le blocage peut être dû à une exclusion spécifique de l’adresse d’origine, ou parce que la destination accepte uniquement les appels d’un ensemble d’adresses d’origine sélectionné (groupe d’utilisateurs fermés). (TAPI versions 2,0 et ultérieures)

LINEDISCONNECTMODE \_ bloqué est approprié en tant que réponse mis en liste. Par exemple, un modem a reçu une réponse plus de six secondes sans détecter les rappels, échec de la connexion d’un nombre défini de fois, détermine que le numéro de téléphone n’est pas valide pour appeler et émet une réponse « mis en liste ».


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_BUSY"></span><span id="linedisconnectmode_busy"></span>**LINEDISCONNECTMODE \_ occupé**
</dt> <dd> <dl> <dt>



La station de l’utilisateur distant est occupée.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_CANCELLED"></span><span id="linedisconnectmode_cancelled"></span>**LINEDISCONNECTMODE \_ annulé**
</dt> <dd> <dl> <dt>



L’appel a été annulé. (TAPI versions 2,0 et ultérieures)


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_CONGESTION"></span><span id="linedisconnectmode_congestion"></span>**\_congestion LINEDISCONNECTMODE**
</dt> <dd> <dl> <dt>



Le réseau est encombré.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_DONOTDISTURB"></span><span id="linedisconnectmode_donotdisturb"></span>**LINEDISCONNECTMODE \_ DONOTDISTURB**
</dt> <dd> <dl> <dt>



L’appel n’a pas pu être connecté, car la destination a appelé la fonctionnalité ne pas déranger. (TAPI versions 2,0 et ultérieures)


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_FORWARDED"></span><span id="linedisconnectmode_forwarded"></span>**LINEDISCONNECTMODE \_ transféré**
</dt> <dd> <dl> <dt>



L’appel a été transféré par le commutateur.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_INCOMPATIBLE"></span><span id="linedisconnectmode_incompatible"></span>**LINEDISCONNECTMODE \_ INcompatible**
</dt> <dd> <dl> <dt>



L’équipement de la station de l’utilisateur distant n’est pas compatible avec le type d’appel demandé.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_NOANSWER"></span><span id="linedisconnectmode_noanswer"></span>**LINEDISCONNECTMODE \_ NOanswer**
</dt> <dd> <dl> <dt>



La station de l’utilisateur distant ne répond pas.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_NODIALTONE"></span><span id="linedisconnectmode_nodialtone"></span>**LINEDISCONNECTMODE \_ NODIALTONE**
</dt> <dd> <dl> <dt>



Une tonalité n’a pas été détectée dans un délai d’attente défini par le fournisseur de services, à un moment donné pendant la numérotation (par exemple, « W » dans la chaîne de numérotation). Cela peut également se produire sans délai d’attente défini par le fournisseur de services ou sans valeur spécifiée dans le membre **dwWaitForDialTone** de la structure [**LINEDIALPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linedialparams) . (TAPI versions 1,4 et ultérieures)


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_NORMAL"></span><span id="linedisconnectmode_normal"></span>**LINEDISCONNECTMODE \_ normal**
</dt> <dd> <dl> <dt>



Il s’agit d’une demande de déconnexion normale de la partie distante. L’appel a été arrêté normalement.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_NUMBERCHANGED"></span><span id="linedisconnectmode_numberchanged"></span>**LINEDISCONNECTMODE \_ NUMBERCHANGED**
</dt> <dd> <dl> <dt>



L’appel n’a pas pu être connecté car le numéro de destination a été modifié, mais la redirection automatique vers le nouveau numéro n’est pas fournie. (TAPI versions 2,0 et ultérieures)


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_OUTOFORDER"></span><span id="linedisconnectmode_outoforder"></span>**LINEDISCONNECTMODE \_ OUTOFORDER**
</dt> <dd> <dl> <dt>



L’appel n’a pas pu être connecté ou a été déconnecté car l’appareil de destination est dans le désordre (défaillance matérielle). (TAPI versions 2,0 et ultérieures)


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_PICKUP"></span><span id="linedisconnectmode_pickup"></span>**\_collecte LINEDISCONNECTMODE**
</dt> <dd> <dl> <dt>



L’appel a été récupéré à partir d’un autre emplacement.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_QOSUNAVAIL"></span><span id="linedisconnectmode_qosunavail"></span>**LINEDISCONNECTMODE \_ QOSUNAVAIL**
</dt> <dd> <dl> <dt>



L’appel n’a pas pu être connecté ou a été déconnecté, car la qualité minimale du service n’a pas pu être obtenue ou maintenue. Cela diffère de LINEDISCONNECTMODE \_ incompatible dans le fait que le manque de ressources peut être une condition temporaire au niveau de la destination. (TAPI versions 2,0 et ultérieures)


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_REJECT"></span><span id="linedisconnectmode_reject"></span>**LINEDISCONNECTMODE \_ rejeter**
</dt> <dd> <dl> <dt>



L’utilisateur distant a rejeté l’appel.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_TEMPFAILURE"></span><span id="linedisconnectmode_tempfailure"></span>**LINEDISCONNECTMODE \_ TEMPFAILURE**
</dt> <dd> <dl> <dt>



L’appel n’a pas pu être connecté ou a été déconnecté en raison d’une défaillance temporaire du réseau. l’appel peut être retenté ultérieurement et devrait finir. (TAPI versions 2,0 et ultérieures)

LINEDISCONNECTMODE \_ TEMPFAILURE est approprié en tant que réponse différée. Par exemple, un modem obtenant un signal occupé ou un équivalent trop fréquent dans une période donnée conclut que le nombre ne doit pas être rappelé tant qu’une heure définie n’est pas écoulée et qu’il émet une réponse « retardée ».


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_UNAVAIL"></span><span id="linedisconnectmode_unavail"></span>**LINEDISCONNECTMODE \_ INdispo**
</dt> <dd> <dl> <dt>



La raison de la déconnexion n’est pas disponible et ne sera pas connue ultérieurement.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_UNKNOWN"></span><span id="linedisconnectmode_unknown"></span>**LINEDISCONNECTMODE \_ inconnu**
</dt> <dd> <dl> <dt>



La raison de la demande de déconnexion est inconnue, mais peut devenir connue ultérieurement.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_UNREACHABLE"></span><span id="linedisconnectmode_unreachable"></span>**LINEDISCONNECTMODE \_ INaccessible**
</dt> <dd> <dl> <dt>



L’utilisateur distant n’a pas pu être atteint.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Les 16 bits de poids fort peuvent être affectés pour les extensions spécifiques à l’appareil. Les 16 bits de poids faible sont réservés.

Une demande de déconnexion distante pour un appel donné entraîne la transition de l’état de l’appel à l’État Disconnected et un message de [**ligne \_ CALLSTATE**](line-callstate.md) est envoyé à l’application. Les informations de LINEDISCONNECTMODE \_ fournissent des détails sur la demande de déconnexion distante. Elle est disponible dans la structure [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) de l’appel lorsque l’appel est à l’État Disconnected. Lorsqu’un appel est dans cet État, l’application est toujours autorisée à interroger les informations et l’état de l’appel. Par exemple, les informations utilisateur utilisateur reçues dans le cadre de la déconnexion distante sont disponibles. L’application peut effacer un appel déconnecté en supprimant l’appel.

Pour la compatibilité descendante, il incombe au fournisseur de services d’examiner la version de l’API négociée sur la ligne et de ne pas utiliser cette \_ valeur LINEDISCONNECTMODE si elle n’est pas prise en charge sur la version négociée (LINEDISCONNECTMODE \_ normal ou \_ Unknown peut être utilisé à la place).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CALLSTATE de ligne \_**](line-callstate.md)
</dt> <dt>

[**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus)
</dt> <dt>

[**LINEDIALPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linedialparams)
</dt> </dl>

 

 




