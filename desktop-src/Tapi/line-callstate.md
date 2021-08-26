---
description: Le \_ message CALLSTATE de ligne TAPI est envoyé lorsque l’état de l’appel spécifié a changé.
ms.assetid: 7b24e3c3-bc69-488b-a698-cf17875bc3c5
title: Message LINE_CALLSTATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90d82dfb5f0d5e306085ecd2d7f29270d19c2c9c101e30ac547fe246b7e6fddb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012569"
---
# <a name="line_callstate-message"></a>\_Message CALLSTATE de ligne

Le message **\_ CALLSTATE de ligne** TAPI est envoyé lorsque l’état de l’appel spécifié a changé. En règle générale, plusieurs de ces messages sont reçus pendant la durée de vie d’un appel. Les applications sont averties des nouveaux appels entrants avec ce message ; le nouvel appel est dans l’état de l' *offre* . L’application peut utiliser [**lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus) pour récupérer des informations plus détaillées sur l’état actuel de l’appel.


```C++
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hDevice* 
</dt> <dd>

Handle de l’appel.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Instance de rappel fournie lors de l’ouverture de la ligne de l’appel.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Nouvel état de l’appel. Ce paramètre doit être une et une seule des [**\_ constantes LINECALLSTATE**](linecallstate--constants.md)suivantes.



| dwParam1                                                                                                                                                                                             | Signification                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LINECALLSTATE_BUSY"></span><span id="linecallstate_busy"></span><dl> <dt>**LINECALLSTATE \_ occupé**</dt> </dl>                         | *dwParam2* contient des détails sur le mode Busy. Ce paramètre utilise l’une des [**\_ constantes LINEBUSYMODE**](linebusymode--constants.md).<br/>                          |
| <span id="LINECALLSTATE_CONNECTED"></span><span id="linecallstate_connected"></span><dl> <dt>**LINECALLSTATE \_ connecté**</dt> </dl>          | *dwParam2* contient des détails sur le mode connecté. Ce paramètre utilise l’une des [**\_ constantes LINECONNECTEDMODE**](lineconnectedmode--constants.md).<br/>           |
| <span id="LINECALLSTATE_DIALTONE"></span><span id="linecallstate_dialtone"></span><dl> <dt>**LINECALLSTATE \_**</dt> </dl>             | *dwParam2* contient des détails sur le mode de tonalité. Ce paramètre utilise l’une des [**\_ constantes LINEDIALTONEMODE**](linedialtonemode--constants.md).<br/>             |
| <span id="LINECALLSTATE_OFFERING"></span><span id="linecallstate_offering"></span><dl> <dt>**\_offre LINECALLSTATE**</dt> </dl>             | *dwParam2* contient des détails sur le mode connecté. Ce paramètre utilise l’une des [**\_ constantes LINEOFFERINGMODE**](lineofferingmode--constants.md).<br/>             |
| <span id="LINECALLSTATE_SPECIALINFO"></span><span id="linecallstate_specialinfo"></span><dl> <dt>**LINECALLSTATE \_ SPECIALINFO**</dt> </dl>    | *dwParam2* contient les détails sur le mode d’information spécial. Ce paramètre utilise l’une des [**\_ constantes LINESPECIALINFO**](linespecialinfo--constants.md).<br/> |
| <span id="LINECALLSTATE_DISCONNECTED"></span><span id="linecallstate_disconnected"></span><dl> <dt>**LINECALLSTATE \_ déconnecté**</dt> </dl> | *dwParam2* contient des détails sur le mode de déconnexion. Ce paramètre utilise l’une des [**\_ constantes LINEDISCONNECTMODE**](linedisconnectmode--constants.md).<br/>        |



 

</dd> <dt>

*dwParam2* 
</dt> <dd>

Informations dépendantes de l’état d’appel. Consultez *dwParam1*.

> [!Note]  
> Dans les cas où une réponse *différée* est appropriée, utilisez LINEDISCONNECTMODE \_ TEMPFAILURE. Quand une réponse *mis en liste* est appropriée, utilisez LINEDISCONNECT \_ bloqué. Pour plus d’informations, [**consultez \_ constantes LINEDISCONNECTMODE**](linedisconnectmode--constants.md).

 

Si *dwParam1* est LINECALLSTATE \_ conferenced, *DwParam2* contient le paramètre *hConfCall* de l’appel parent de la conférence dont l’objet *hCall* est membre. Si l’appel spécifié dans *dwParam2* n’a pas été précédemment pris en compte par l’application pour être un appel de conférence parent (*hConfCall*, l’application doit le faire à la suite de ce message. Si l’application n’a pas de handle vers l’appel parent de la Conférence (car elle a précédemment appelé [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) sur ce handle) *dwParam2* a la valeur **null**.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Si la valeur est zéro, ce paramètre indique qu’il n’y a eu aucune modification du privilège de l’application pour l’appel.

Si la valeur est différente de zéro, elle spécifie le privilège de l’application pour l’appel. Cela se produit dans les situations suivantes : (1) la première fois que l’application reçoit un handle pour cet appel ; (2) lorsque l’application est la cible d’un transfert d’appel (même si l’application était déjà propriétaire de l’appel). Ce paramètre utilise l’une des [**\_ constantes LINECALLPRIVILEGE**](linecallprivilege--constants.md)suivantes.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Remarques

Ce message est envoyé à toute application qui a un handle pour l’appel. Le message de **ligne \_ CALLSTATE** avertit également les applications qui surveillent les appels sur une ligne de l’existence et de l’état des appels sortants établis par d’autres applications ou manuellement par l’utilisateur (par exemple, sur un appareil téléphonique attaché). L’état d’appel de ces appels reflète l’état réel de l’appel, qui n' *offre* pas. En examinant l’état de l’appel, l’application peut déterminer si l’appel est un appel entrant qui doit être traité ou non.

Un **message \_ CALLSTATE de ligne** avec un état d’appel inconnu peut être envoyé à une application de surveillance suite à une réussite de [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall), [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward), [**LineUnpark**](/windows/desktop/api/Tapi/nf-tapi-lineunpark), [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer), [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup), [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)ou [**linePrepareAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference) qui a été demandée par une autre application. En même temps que l’application à l’origine de la demande reçoit une [**\_ réponse de ligne**](line-reply.md) (succès) pour l’opération demandée, les applications de surveillance de la ligne reçoivent le message de **ligne \_ CALLSTATE** (inconnu). Un message de **\_ CALLSTATE de ligne** indiquant l’état d’appel « réel » de l’appel récemment généré est envoyé (à l’aide des informations fournies par le fournisseur de services) aux applications de demande et de surveillance, peu de temps après.

Un message **line \_ CALLSTATE** (Unknown) est envoyé aux applications de surveillance uniquement si [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) entraîne la résolution des appels en conférence triple.

Pour la compatibilité descendante, les applications plus anciennes n’attendent aucune valeur particulière dans *dwParam2* d’un \_ message LINECALLSTATE conferencinged. TAPI transmet donc l’appel parent *hConfCall* dans *dwParam2* , quelle que soit la version d’API de l’application qui reçoit le message. Dans le cas d’un appel de conférence initié par le fournisseur de services, l’ancienne application ne sait pas que l’appel parent est devenu un appel de conférence, à moins qu’il n’examine spontanément d’autres informations (par exemple, appelez [**lineGetConfRelatedCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls)).

Ce message ne peut pas être désactivé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**réponse de ligne \_**](line-reply.md)
</dt> <dt>

[**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer)
</dt> <dt>

[**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall)
</dt> <dt>

[**LINEDIALPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linedialparams)
</dt> <dt>

[**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward)
</dt> <dt>

[**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits)
</dt> <dt>

[**lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus)
</dt> <dt>

[**lineGetConfRelatedCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls)
</dt> <dt>

[**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup)
</dt> <dt>

[**linePrepareAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference)
</dt> <dt>

[**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)
</dt> <dt>

[**lineUnpark**](/windows/desktop/api/Tapi/nf-tapi-lineunpark)
</dt> </dl>

 

 




