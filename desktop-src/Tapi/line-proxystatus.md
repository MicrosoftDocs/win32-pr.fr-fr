---
description: La ligne \_ PROXYSTATUS le message est envoyé lorsque les proxies disponibles changent sur une ligne ouverte par l’application.
ms.assetid: e20d4b48-a72a-4a83-ae04-a608791a1a3a
title: Message LINE_PROXYSTATUS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 585feda6194a13ecfbe17292aadb9036784d244c9ee5b7df4361981ab7401f65
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682349"
---
# <a name="line_proxystatus-message"></a>\_Message PROXYSTATUS de ligne

La **ligne \_ PROXYSTATUS** le message est envoyé lorsque les proxies disponibles changent sur une ligne ouverte par l’application.

TAPISRV génère ce message pendant une fonction [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) à l’aide de LINEPROXYSTATUS \_ Open et LINEPROXYSTATUS \_ ALLOPENFORACD ou d’une fonction [**LINECLOSE**](/windows/desktop/api/Tapi/nf-tapi-lineclose) à l’aide de LINEPROXYSTATUS \_ Close (toutes les [**\_ constantes LINEPROXYSTATUS**](lineproxystatus--constants.md)).


```C++
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwDevice* 
</dt> <dd>

Handle de l’application sur le périphérique de ligne. Cela est relatif au gestionnaire de l’agent.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Instance de rappel fournie lors de l’ouverture de la ligne.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Spécifie l’état de la file d’attente qui a changé. Il peut s’agir d’une ou plusieurs des [**\_ constantes LINEPROXYSTATUS**](lineproxystatus--constants.md).

</dd> <dt>

*dwParam2* 
</dt> <dd>

Si *dwParam1* a la valeur LINEPROXYSTATUS \_ Open ou LINEPROXYSTATUS \_ Close, *dwParam2* indique le type de requête proxy associé, qui est l’un des éléments suivants :

-   LINEPROXYREQUEST \_ SETAGENTGROUP
-   LINEPROXYREQUEST \_ SETAGENTSTATE
-   LINEPROXYREQUEST \_ SETAGENTACTIVITY
-   LINEPROXYREQUEST \_ GETAGENTCAPS
-   LINEPROXYREQUEST \_ GETAGENTSTATUS
-   LINEPROXYREQUEST \_ AGENTSPECIFIC
-   LINEPROXYREQUEST \_ GETAGENTACTIVITYLIST
-   LINEPROXYREQUEST \_ GETAGENTGROUPLIST
-   LINEPROXYREQUEST \_ CREATEAGENT
-   LINEPROXYREQUEST \_ SETAGENTMEASUREMENTPERIOD
-   LINEPROXYREQUEST \_ GETAGENTINFO
-   LINEPROXYREQUEST \_ CREATEAGENTSESSION
-   LINEPROXYREQUEST \_ GETAGENTSESSIONLIST
-   LINEPROXYREQUEST \_ SETAGENTSESSIONSTATE
-   LINEPROXYREQUEST \_ GETAGENTSESSIONINFO
-   LINEPROXYREQUEST \_ GETQUEUELIST
-   LINEPROXYREQUEST \_ SETQUEUEMEASUREMENTPERIOD
-   LINEPROXYREQUEST \_ GETQUEUEINFO
-   LINEPROXYREQUEST \_ GETGROUPLIST
-   LINEPROXYREQUEST \_ SETAGENTSTATEEX

Sinon, *dwParam2* a la valeur zéro.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Réservé. Définit la valeur zéro.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,2<br/>                                                      |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose)
</dt> <dt>

[**PROXYREQUEST de ligne \_**](line-proxyrequest.md)
</dt> <dt>

[**\_Constantes LINEPROXYREQUEST**](lineproxyrequest--constants.md)
</dt> </dl>

 

 




