---
description: Ces constantes sont utilisées dans deux contextes.
ms.assetid: 5c05a567-cc65-411e-b049-919a442c5c57
title: Constantes LINEPROXYREQUEST_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eba34a3a7f7b1f41f0c32783c4132afcfafef1aa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013468"
---
# <a name="lineproxyrequest_-constants"></a>\_Constantes LINEPROXYREQUEST

Ces constantes sont utilisées dans deux contextes. Tout d’abord, elles peuvent être utilisées dans un tableau de valeurs **DWORD** dans la structure [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) passée avec [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) lorsque l' \_ option de proxy LINEOPENOPTION est spécifiée, pour indiquer les fonctions que l’application est prête à gérer. Deuxièmement, elles sont utilisées dans la [**ligne \_ PROXYREQUEST**](line-proxyrequest.md) transmise à l’application de gestionnaire par un message de **ligne \_ PROXYREQUEST** pour indiquer le type de demande à traiter et le format des données dans la mémoire tampon.

<dl> <dt>

<span id="LINEPROXYREQUEST_AGENTSPECIFIC"></span><span id="lineproxyrequest_agentspecific"></span>**LINEPROXYREQUEST \_ AGENTSPECIFIC**
</dt> <dd> <dl> <dt>



Associé à [**lineAgentSpecific**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_CREATEAGENT"></span><span id="lineproxyrequest_createagent"></span>**LINEPROXYREQUEST \_ CREATEAGENT**
</dt> <dd> <dl> <dt>



Associé à [**lineCreateAgent**](/windows/desktop/api/Tapi/nf-tapi-linecreateagenta).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_CREATEAGENTSESSION"></span><span id="lineproxyrequest_createagentsession"></span>**LINEPROXYREQUEST \_ CREATEAGENTSESSION**
</dt> <dd> <dl> <dt>



Associé à [**lineCreateAgentSession**](/windows/desktop/api/Tapi/nf-tapi-linecreateagentsessiona).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_GETAGENTACTIVITYLIST"></span><span id="lineproxyrequest_getagentactivitylist"></span>**LINEPROXYREQUEST \_ GETAGENTACTIVITYLIST**
</dt> <dd> <dl> <dt>



Associé à [**lineGetAgentActivityList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentactivitylista).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_GETAGENTCAPS"></span><span id="lineproxyrequest_getagentcaps"></span>**LINEPROXYREQUEST \_ GETAGENTCAPS**
</dt> <dd> <dl> <dt>



Associé à [**lineGetAgentCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetagentcapsa).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_GETAGENTGROUPLIST"></span><span id="lineproxyrequest_getagentgrouplist"></span>**LINEPROXYREQUEST \_ GETAGENTGROUPLIST**
</dt> <dd> <dl> <dt>



Associé à [**lineGetAgentGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentgrouplista).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_GETAGENTINFO"></span><span id="lineproxyrequest_getagentinfo"></span>**LINEPROXYREQUEST \_ GETAGENTINFO**
</dt> <dd> <dl> <dt>



Associé à [**lineGetAgentInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetagentinfo).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_GETAGENTSESSIONINFO"></span><span id="lineproxyrequest_getagentsessioninfo"></span>**LINEPROXYREQUEST \_ GETAGENTSESSIONINFO**
</dt> <dd> <dl> <dt>



Associé à [**lineGetAgentSessionInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetagentsessioninfo).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_GETAGENTSESSIONLIST"></span><span id="lineproxyrequest_getagentsessionlist"></span>**LINEPROXYREQUEST \_ GETAGENTSESSIONLIST**
</dt> <dd> <dl> <dt>



Associé à [**lineGetAgentSessionList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentsessionlist).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_GETAGENTSTATUS"></span><span id="lineproxyrequest_getagentstatus"></span>**LINEPROXYREQUEST \_ GETAGENTSTATUS**
</dt> <dd> <dl> <dt>



Associé à [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_GETGROUPLIST"></span><span id="lineproxyrequest_getgrouplist"></span>**LINEPROXYREQUEST \_ GETGROUPLIST**
</dt> <dd> <dl> <dt>



Associé à [**lineGetGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetgrouplista).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_GETQUEUEINFO"></span><span id="lineproxyrequest_getqueueinfo"></span>**LINEPROXYREQUEST \_ GETQUEUEINFO**
</dt> <dd> <dl> <dt>



Associé à [**lineGetQueueInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetqueueinfo).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_GETQUEUELIST"></span><span id="lineproxyrequest_getqueuelist"></span>**LINEPROXYREQUEST \_ GETQUEUELIST**
</dt> <dd> <dl> <dt>



Associé à [**lineGetQueueList**](/windows/desktop/api/Tapi/nf-tapi-linegetqueuelista).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_SETAGENTACTIVITY"></span><span id="lineproxyrequest_setagentactivity"></span>**LINEPROXYREQUEST \_ SETAGENTACTIVITY**
</dt> <dd> <dl> <dt>



Associé à [**lineSetAgentActivity**](/windows/desktop/api/Tapi/nf-tapi-linesetagentactivity).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_SETAGENTGROUP"></span><span id="lineproxyrequest_setagentgroup"></span>**LINEPROXYREQUEST \_ SETAGENTGROUP**
</dt> <dd> <dl> <dt>



Associé à [**lineSetAgentGroup**](/windows/desktop/api/Tapi/nf-tapi-linesetagentgroup).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_SETAGENTMEASUREMENTPERIOD"></span><span id="lineproxyrequest_setagentmeasurementperiod"></span>**LINEPROXYREQUEST \_ SETAGENTMEASUREMENTPERIOD**
</dt> <dd> <dl> <dt>



Associé à [**lineSetAgentMeasurementPeriod**](/windows/desktop/api/Tapi/nf-tapi-linesetagentmeasurementperiod).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_SETAGENTSESSIONSTATE"></span><span id="lineproxyrequest_setagentsessionstate"></span>**LINEPROXYREQUEST \_ SETAGENTSESSIONSTATE**
</dt> <dd> <dl> <dt>



Associé à [**lineSetAgentSessionState**](/windows/desktop/api/Tapi/nf-tapi-linesetagentsessionstate).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_SETAGENTSTATE"></span><span id="lineproxyrequest_setagentstate"></span>**LINEPROXYREQUEST \_ SETAGENTSTATE**
</dt> <dd> <dl> <dt>



Associé à [**lineSetAgentState**](/windows/desktop/api/Tapi/nf-tapi-linesetagentstate).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_SETAGENTSTATEEX"></span><span id="lineproxyrequest_setagentstateex"></span>**LINEPROXYREQUEST \_ SETAGENTSTATEEX**
</dt> <dd> <dl> <dt>



Associé à [**lineSetAgentStateEx**](/windows/desktop/api/Tapi/nf-tapi-linesetagentstateex).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_SETQUEUEMEASUREMENTPERIOD"></span><span id="lineproxyrequest_setqueuemeasurementperiod"></span>**LINEPROXYREQUEST \_ SETQUEUEMEASUREMENTPERIOD**
</dt> <dd> <dl> <dt>



Associé à [**lineSetQueueMeasurementPeriod**](/windows/desktop/api/Tapi/nf-tapi-linesetqueuemeasurementperiod).


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes de centre d’appels](call-center-constants.md)
</dt> <dt>

[Fonctions du centre d’appels](call-center-functions.md)
</dt> </dl>

 

 




