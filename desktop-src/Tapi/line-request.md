---
description: Le message de demande de ligne TAPI \_ est envoyé pour signaler l’arrivée d’une nouvelle demande à partir d’une autre application.
ms.assetid: d4dbba0d-8225-48d7-a66b-b189fdae70a8
title: Message LINE_REQUEST (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23987e370d5ae9c8eeb579780c5659f8075ac865
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539615"
---
# <a name="line_request-message"></a>Message de demande de ligne \_

Le message **de \_ demande de ligne** TAPI est envoyé pour signaler l’arrivée d’une nouvelle demande à partir d’une autre application.


```C++
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hDevice* 
</dt> <dd>

Non utilisé.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Instance d’inscription de l’application spécifiée sur [**lineRegisterRequestRecipient**](/windows/desktop/api/Tapi/nf-tapi-lineregisterrequestrecipient).

</dd> <dt>

*dwParam1* 
</dt> <dd>

Mode de requête de la demande nouvellement en attente. Ce paramètre utilise les [**\_ constantes LINEREQUESTMODE**](linerequestmode--constants.md).

</dd> <dt>

*dwParam2* 
</dt> <dd>

Les conditions de ce paramètre sont, si *dwParam1* est défini sur LINEREQUESTMODE \_ Drop, *dwParam2* contient le *HWND* de l’application qui demande la suppression. Dans le cas contraire, *dwParam2* n’est pas utilisé.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Si *dwParam1* a la valeur LINEREQUESTMODE \_ Drop, le mot de poids faible de *dwParam3* contient le *wRequestID* tel que spécifié par l’application qui a demandé la suppression. Dans le cas contraire, *dwParam3* n’est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Le message de **\_ demande de ligne** est envoyé à l’application dont la priorité est la plus élevée et qui est inscrite pour le mode de requête correspondant. Ce message indique l’arrivée d’une demande de téléphonie assistée du mode de demande spécifié. Si *dwParam1* est LINEREQUESTMODE \_ MAKECALL, l’application peut appeler [**lineGetRequest**](/windows/desktop/api/Tapi/nf-tapi-linegetrequest) en utilisant le mode de demande correspondant pour recevoir la demande. Si *dwParam1* est LINEREQUESTMODE \_ Drop, le message contient toutes les données requises par le destinataire de la demande pour effectuer la demande.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**lineGetRequest**](/windows/desktop/api/Tapi/nf-tapi-linegetrequest)
</dt> <dt>

[**lineRegisterRequestRecipient**](/windows/desktop/api/Tapi/nf-tapi-lineregisterrequestrecipient)
</dt> <dt>

[**tapiRequestMakeCall**](/windows/desktop/api/Tapi/nf-tapi-tapirequestmakecall)
</dt> </dl>

 

 




