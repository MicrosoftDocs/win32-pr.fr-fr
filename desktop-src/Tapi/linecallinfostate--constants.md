---
description: Les \_ constantes d’indicateur de bit LINECALLINFOSTATE décrivent les différents éléments d’informations sur les appels sur lesquels une application peut être notifiée dans le message de ligne \_ CALLINFO.
ms.assetid: c216d9b7-8e2f-4604-ba93-1d9e1a5d23fc
title: Constantes LINECALLINFOSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f560cfd6ba65929a9f6cf5c9aa6cd8bc2f48b24
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532521"
---
# <a name="linecallinfostate_-constants"></a>\_Constantes LINECALLINFOSTATE

Les constantes d’indicateur de bit **LINECALLINFOSTATE \_** décrivent les différents éléments d’informations sur les appels sur lesquels une application peut être notifiée dans le message de [**ligne \_ CALLINFO**](line-callinfo.md) .

<dl> <dt>

<span id="LINECALLINFOSTATE_APPSPECIFIC"></span><span id="linecallinfostate_appspecific"></span>**LINECALLINFOSTATE \_ APPSPECIFIC**
</dt> <dd> <dl> <dt>



Champ propre à l’application de l’enregistrement d’informations d’appel.


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_BEARERMODE"></span><span id="linecallinfostate_bearermode"></span>**LINECALLINFOSTATE \_ BEARERMODE**
</dt> <dd> <dl> <dt>



Champ du mode porteur de l’enregistrement d’informations d’appel.


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_CALLDATA"></span><span id="linecallinfostate_calldata"></span>**LINECALLINFOSTATE \_ CALLDATA**
</dt> <dd> <dl> <dt>



Le membre **CallData** dans [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) a été mis à jour.


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_CALLEDID"></span><span id="linecallinfostate_calledid"></span>**LINECALLINFOSTATE \_ CALLEDID**
</dt> <dd> <dl> <dt>



Un des champs liés à calledID de l’enregistrement d’informations d’appel.


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_CALLERID"></span><span id="linecallinfostate_callerid"></span>**LINECALLINFOSTATE \_ CALLERID**
</dt> <dd> <dl> <dt>



Un des champs liés à callerID de l’enregistrement d’informations d’appel.


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_CALLID"></span><span id="linecallinfostate_callid"></span>**LINECALLINFOSTATE \_ CALLID**
</dt> <dd> <dl> <dt>



Champ ID d’appel de l’enregistrement d’informations d’appel.


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_CHARGINGINFO"></span><span id="linecallinfostate_charginginfo"></span>**LINECALLINFOSTATE \_ CHARGINGINFO**
</dt> <dd> <dl> <dt>



Informations de facturation de l’enregistrement d’informations d’appel.


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_COMPLETIONID"></span><span id="linecallinfostate_completionid"></span>**LINECALLINFOSTATE \_ COMPLETIONID**
</dt> <dd> <dl> <dt>



Champ d’identificateur de saisie semi-automatique de l’enregistrement d’informations d’appel.


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_CONNECTEDID"></span><span id="linecallinfostate_connectedid"></span>**LINECALLINFOSTATE \_ CONNECTEDID**
</dt> <dd> <dl> <dt>



Un des champs liés à connectedID de l’enregistrement d’informations d’appel.


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_DEVSPECIFIC"></span><span id="linecallinfostate_devspecific"></span>**LINECALLINFOSTATE \_ DEVSPECIFIC**
</dt> <dd> <dl> <dt>



Champ spécifique à l’appareil de l’enregistrement d’informations d’appel.


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_DIALPARAMS"></span><span id="linecallinfostate_dialparams"></span>**LINECALLINFOSTATE \_ DIALPARAMS**
</dt> <dd> <dl> <dt>



Paramètres de numérotation de l’enregistrement d’informations d’appel.


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_DISPLAY"></span><span id="linecallinfostate_display"></span>**\_affichage LINECALLINFOSTATE**
</dt> <dd> <dl> <dt>



Champ d’affichage de l’enregistrement d’informations d’appel.


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_HIGHLEVELCOMP"></span><span id="linecallinfostate_highlevelcomp"></span>**LINECALLINFOSTATE \_ HIGHLEVELCOMP**
</dt> <dd> <dl> <dt>



Champ de compatibilité de haut niveau de l’enregistrement d’informations d’appel.


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_LOWLEVELCOMP"></span><span id="linecallinfostate_lowlevelcomp"></span>**LINECALLINFOSTATE \_ LOWLEVELCOMP**
</dt> <dd> <dl> <dt>



Champ de compatibilité de bas niveau de l’enregistrement d’informations d’appel.


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_MEDIAMODE"></span><span id="linecallinfostate_mediamode"></span>**LINECALLINFOSTATE \_ MEDIAMODE**
</dt> <dd> <dl> <dt>



Champ type de média de l’enregistrement Call-information.


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_MONITORMODES"></span><span id="linecallinfostate_monitormodes"></span>**LINECALLINFOSTATE \_ MONITORMODES**
</dt> <dd> <dl> <dt>



Un ou plusieurs champs de surveillance de chiffre, de tonalité ou de média dans l’enregistrement d’informations d’appel.


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_NUMMONITORS"></span><span id="linecallinfostate_nummonitors"></span>**LINECALLINFOSTATE \_ NUMMONITORS**
</dt> <dd> <dl> <dt>



Le champ nombre de moniteurs dans l’enregistrement d’informations d’appel a changé.


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_NUMOWNERDECR"></span><span id="linecallinfostate_numownerdecr"></span>**LINECALLINFOSTATE \_ NUMOWNERDECR**
</dt> <dd> <dl> <dt>



Le nombre de champs de propriétaire dans l’enregistrement d’informations d’appel a été réduit.


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_NUMOWNERINCR"></span><span id="linecallinfostate_numownerincr"></span>**LINECALLINFOSTATE \_ NUMOWNERINCR**
</dt> <dd> <dl> <dt>



Le nombre de champs de propriétaire dans l’enregistrement d’informations d’appel a été augmenté.


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_ORIGIN"></span><span id="linecallinfostate_origin"></span>**LINECALLINFOSTATE \_ origine**
</dt> <dd> <dl> <dt>



Champ Origin de l’enregistrement d’informations d’appel.


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_OTHER"></span><span id="linecallinfostate_other"></span>**LINECALLINFOSTATE \_ autre**
</dt> <dd> <dl> <dt>



Les éléments d’informations d’appel autres que ceux listés ci-dessous ont été modifiés. L’application doit vérifier les informations d’appel actuelles pour déterminer les éléments qui ont été modifiés.


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_QOS"></span><span id="linecallinfostate_qos"></span>**\_QoS LINECALLINFOSTATE**
</dt> <dd> <dl> <dt>



Un ou plusieurs des membres **QoS** dans [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) ont été mis à jour.


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_RATE"></span><span id="linecallinfostate_rate"></span>**taux de LINECALLINFOSTATE \_**
</dt> <dd> <dl> <dt>



Le champ rate de l’enregistrement Call-information.


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_REASON"></span><span id="linecallinfostate_reason"></span>**\_raison LINECALLINFOSTATE**
</dt> <dd> <dl> <dt>



Champ raison de l’enregistrement d’informations d’appel.


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_REDIRECTINGID"></span><span id="linecallinfostate_redirectingid"></span>**LINECALLINFOSTATE \_ REDIRECTINGID**
</dt> <dd> <dl> <dt>



Identificateur d’adresse de l’emplacement qui a redirigé un appel.


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_REDIRECTIONID"></span><span id="linecallinfostate_redirectionid"></span>**LINECALLINFOSTATE \_ REDIRECTIONID**
</dt> <dd> <dl> <dt>



Identificateur d’adresse de l’emplacement vers lequel un appel a été redirigé.


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_RELATEDCALLID"></span><span id="linecallinfostate_relatedcallid"></span>**LINECALLINFOSTATE \_ RELATEDCALLID**
</dt> <dd> <dl> <dt>



Champ ID d’appel associé de l’enregistrement d’informations d’appel.


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_TERMINAL"></span><span id="linecallinfostate_terminal"></span>**\_Terminal LINECALLINFOSTATE**
</dt> <dd> <dl> <dt>



Informations relatives au mode terminal de l’enregistrement d’informations d’appel.


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_TREATMENT"></span><span id="linecallinfostate_treatment"></span>**\_traitement LINECALLINFOSTATE**
</dt> <dd> <dl> <dt>



Le membre **CallTreatment** dans [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) a été mis à jour. Cela peut se produire en réponse à une fonction [**lineSetCallTreatment**](/windows/desktop/api/Tapi/nf-tapi-linesetcalltreatment) , à un changement d’état d’appel, à un appel « Vector » ou à un autre script contrôlant l’appel, ou à la fin de la lecture d’un message enregistré (en général, en indiquant une modification de « silence » ou de « musique »).


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_TRUNK"></span><span id="linecallinfostate_trunk"></span>**LINECALLINFOSTATE \_ Trunk**
</dt> <dd> <dl> <dt>



Champ Trunk de l’enregistrement d’informations d’appel.


</dt> </dl> </dd> <dt>

<span id="LINECALLINFOSTATE_USERUSERINFO"></span><span id="linecallinfostate_useruserinfo"></span>**LINECALLINFOSTATE \_ USERUSERINFO**
</dt> <dd> <dl> <dt>



Informations utilisateur utilisateur de l’enregistrement d’informations d’appel.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Aucune extensibilité. Tous les 32 bits sont réservés.

Lorsque des modifications se produisent dans cette structure de données, un message [**\_ CALLINFO de ligne**](line-callinfo.md) est envoyé à l’application. Les paramètres de ce message sont un descripteur de l’appel et une indication de l’élément d’information qui a changé. La structure de données [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) indique également les éléments d’informations d’appel qui sont valides pour chaque appel sur l’adresse.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CALLINFO de ligne \_**](line-callinfo.md)
</dt> <dt>

[**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)
</dt> <dt>

[**lineSetCallTreatment**](/windows/desktop/api/Tapi/nf-tapi-linesetcalltreatment)
</dt> </dl>

 

 




