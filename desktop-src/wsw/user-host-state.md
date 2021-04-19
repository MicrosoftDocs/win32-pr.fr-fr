---
title: État utilisateur de l’hôte de service
description: L’hôte de service permet à une application d’associer des données d’État étendues au niveau de l’hôte du service.
ms.assetid: e18c6c0c-3205-4f88-9a9b-2515a7cfc462
keywords:
- Services Web de l’état de l’hôte utilisateur pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56f43942f7743d28534e0286a45203dc01e0e7b6
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "106509071"
---
# <a name="service-host-user-state"></a>État utilisateur de l’hôte de service

L' [hôte de service](service-host.md) permet à une application d’associer des données d’État étendues au niveau de l’hôte du service. Cet État est spécifié par une structure [**de \_ \_ propriété de service Web**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property) qui est passée à la fonction [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) lorsque l’application crée un [hôte de service](service-host.md), comme illustré dans l’exemple suivant.

``` syntax
void* quotePtr = (void*) quotes;
WS_SERVICE_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_PROPERTY_HOST_USER_STATE;
serviceProperties[0].value = &quotePtr; // assume this is some state that you want to associate with the service host
serviceProperties[0].valueSize = sizeof(quotePtr);
```


Les données d’État sont disponibles pour tous les rappels et [opérations de service](service-operation.md)de l’hôte de service. Les rappels et les opérations de service récupèrent les informations en appelant la fonction [**WsGetOperationContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty) et en spécifiant le contexte, référencé par la structure du contexte de l' [ \_ opération \_ WS](ws-operation-context.md) , et la propriété de contexte, comme l’une des valeurs de la propriété de contexte de l’opération WS eunumeration de l' [**\_ \_ \_ \_ \_ \_ état utilisateur**](/windows/desktop/api/WebServices/ne-webservices-ws_operation_context_property_id) , comme illustré dans l’exemple suivant.

``` syntax
QuoteTable* table = NULL;
HRESULT hr = NOERROR;
if (FAILED (WsGetOperationContextProperty (context, WS_OPERATION_CONTEXT_PROPERTY_HOST_USER_STATE, &table, sizeof(table), NULL, error)))
    return hr;
```

 

 




