---
description: Les \_ constantes d’indicateur de bit LINECALLSTATE décrivent les États d’appel dans lesquels un appel peut se trouver.
ms.assetid: 18d881ee-cf98-4dec-a561-333c2518935d
title: Constantes LINECALLSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d50301dfeca49513a919fba90cc960c7ccb572d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541148"
---
# <a name="linecallstate_-constants"></a>\_Constantes LINECALLSTATE

Les constantes d’indicateur de bit **LINECALLSTATE \_** décrivent les États d’appel dans lesquels un appel peut se trouver.

<dl> <dt>

<span id="LINECALLSTATE_ACCEPTED"></span><span id="linecallstate_accepted"></span>**LINECALLSTATE \_ accepté**
</dt> <dd> <dl> <dt>



L’appel était dans l’état d’offre et a été accepté. Cela indique à d’autres applications (de surveillance) que l’application propriétaire actuelle a déclaré responsable de la réponse à l’appel. Dans RNIS, l’état accepté est entré lorsque l’équipement de la partie appelée envoie un message au commutateur, indiquant qu’il est disposé à présenter l’appel à la personne appelée. Cela a pour effet secondaire d’alerter (sonnerie) les utilisateurs aux deux extrémités de l’appel. Un appel entrant peut toujours recevoir une réponse immédiatement sans avoir d’abord accepté séparément.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_BUSY"></span><span id="linecallstate_busy"></span>**LINECALLSTATE \_ occupé**
</dt> <dd> <dl> <dt>



L’appel reçoit un ton occupé. Une tonalité occupée indique que l’appel ne peut pas être effectué sur un circuit (Trunk) ou si la station distante est en cours d’utilisation. Consultez [**\_ constantes LINEBUSYMODE**](linebusymode--constants.md).


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_CONFERENCED"></span><span id="linecallstate_conferenced"></span>**LINECALLSTATE \_ Conférence**
</dt> <dd> <dl> <dt>



L’appel est membre d’un appel de conférence et est logiquement dans l’état connecté.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_CONNECTED"></span><span id="linecallstate_connected"></span>**LINECALLSTATE \_ connecté**
</dt> <dd> <dl> <dt>



L’appel a été établi et la connexion est établie. Les informations peuvent être transmises à l’appel entre l’adresse d’origine et l’adresse de destination.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_DIALING"></span><span id="linecallstate_dialing"></span>**\_numérotation LINECALLSTATE**
</dt> <dd> <dl> <dt>



L’expéditeur compose des chiffres sur l’appel. Les chiffres composés sont collectés par le commutateur. Notez que ni [**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits) ni [**TSPI \_ lineGenerateDigits**](/windows/win32/api/tspi/nf-tspi-tspi_linegeneratedigits) ne placent la ligne dans l’état de numérotation.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_DIALTONE"></span><span id="linecallstate_dialtone"></span>**LINECALLSTATE \_**
</dt> <dd> <dl> <dt>



L’appel reçoit une tonalité du commutateur, ce qui signifie que le commutateur est prêt à recevoir un numéro composé. Consultez [**LINEDIALTONEMODE \_ constantes**](linedialtonemode--constants.md) pour les identificateurs de tonalités spéciales, telles qu’une tonalité d’interruption de la messagerie vocale normale.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_DISCONNECTED"></span><span id="linecallstate_disconnected"></span>**LINECALLSTATE \_ déconnecté**
</dt> <dd> <dl> <dt>



Le tiers distant s’est déconnecté de l’appel.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_IDLE"></span><span id="linecallstate_idle"></span>**LINECALLSTATE \_ inactif**
</dt> <dd> <dl> <dt>



L’appel existe mais n’a pas été connecté. Aucune activité n’existe sur l’appel, ce qui signifie qu’aucun appel n’est actuellement actif. Un appel ne peut jamais passer de l’état inactif.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_OFFERING"></span><span id="linecallstate_offering"></span>**\_offre LINECALLSTATE**
</dt> <dd> <dl> <dt>



L’appel est offert à la station, signalant l’arrivée d’un nouvel appel. L’état de l’offre n’est pas le même que celui d’un téléphone ou d’un ordinateur. Dans certains environnements, un appel dans l’état de l’offre ne sonne pas l’utilisateur tant que le commutateur ne demande pas à la ligne de sonner. Un exemple d’utilisation peut être l’endroit où un appel entrant s’affiche sur plusieurs ensembles de stations, mais uniquement les sonneries d’adresse principales. L’instruction à Ring n’affecte pas les États d’appel.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_ONHOLD"></span><span id="linecallstate_onhold"></span>**LINECALLSTATE \_ ONHOLD**
</dt> <dd> <dl> <dt>



L’appel est en attente par le commutateur. Cela libère la ligne physique, ce qui permet à un autre appel d’utiliser la ligne.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_ONHOLDPENDCONF"></span><span id="linecallstate_onholdpendconf"></span>**LINECALLSTATE \_ ONHOLDPENDCONF**
</dt> <dd> <dl> <dt>



L’appel est actuellement en attente pendant son ajout à une conférence.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_ONHOLDPENDTRANSFER"></span><span id="linecallstate_onholdpendtransfer"></span>**LINECALLSTATE \_ ONHOLDPENDTRANSFER**
</dt> <dd> <dl> <dt>



L’appel est actuellement en attente de transfert vers un autre nombre.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_PROCEEDING"></span><span id="linecallstate_proceeding"></span>**LINECALLSTATE \_**
</dt> <dd> <dl> <dt>



La numérotation est terminée et l’appel se poursuit via le commutateur ou le réseau téléphonique. Cela se produit une fois que la numérotation est terminée et que l’appel atteint le tiers composé, comme indiqué par le rappel, le occupé ou la réponse.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_RINGBACK"></span><span id="linecallstate_ringback"></span>**\_rappel LINECALLSTATE**
</dt> <dd> <dl> <dt>



La station à appeler a été atteinte et le commutateur de la destination génère une tonalité de retour à l’expéditeur. Un *rappel* signifie que l’adresse de destination est avertie de l’appel.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_SPECIALINFO"></span><span id="linecallstate_specialinfo"></span>**LINECALLSTATE \_ SPECIALINFO**
</dt> <dd> <dl> <dt>



L’appel reçoit un signal d’information spécial, qui précède une annonce préenregistrée indiquant la raison pour laquelle un appel ne peut pas être effectué. Consultez [**\_ constantes LINESPECIALINFO**](linespecialinfo--constants.md).


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_UNKNOWN"></span><span id="linecallstate_unknown"></span>**LINECALLSTATE \_ inconnu**
</dt> <dd> <dl> <dt>



L’appel existe, mais son état est actuellement inconnu. Cela peut être dû à une mauvaise détection de la progression de l’appel par le fournisseur de services. Un message d’état d’appel avec l’état d’appel défini sur inconnu peut également être généré pour informer la DLL TAPI à propos d’un nouvel appel à la fois lorsque l’état d’appel réel de l’appel n’est pas exactement connu.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Les 8 bits de poids fort peuvent définir un sous-état spécifique à l’appareil de l’un des États prédéfinis, à condition que l’un des \_ bits LINECALLSTATE définis ci-dessus soit également défini. Les 24 bits de poids faible sont réservés aux États prédéfinis.

Les **\_ constantes LINECALLSTATE** sont utilisées comme paramètres par le message de [**ligne \_ CALLSTATE**](line-callstate.md) envoyé à l’application. Le message transporte le nouvel état d’appel vers lequel l’appel a été transféré. Ces constantes sont également utilisées comme membres dans la structure [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) retournée par la fonction [**lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus) .

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

[**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits)
</dt> <dt>

[**lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus)
</dt> </dl>

 

