---
title: Contexte (services Web Windows)
description: Un contexte est utilisé dans les opérations de service de modèle de service et les rappels pour passer les données d’État pertinentes à l’opération de service ou au rappel lorsqu’il est appelé.
ms.assetid: 44283854-96df-4e6b-8464-3df685896f07
keywords:
- Services Web de contexte pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f7edd1f8c93bbf4fd4b4d5feea5b2219bc522ea
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/23/2019
ms.locfileid: "103940583"
---
# <a name="context-windows-web-services"></a>Contexte (services Web Windows)

Un contexte est utilisé dans les [opérations de service](service-operation.md) de modèle de service et les rappels pour passer les données d’État pertinentes à l’opération de service ou au rappel lorsqu’il est appelé. Un contexte est référencé par une structure [de \_ \_ contexte d’opération WS](ws-operation-context.md) . Les propriétés d’un contexte peuvent être récupérées avec la fonction [**WsGetOperationContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty) , comme illustré dans le code suivant.

``` syntax
WS_MESSAGE* requestMessage = NULL;
HRESULT hr = WsGetOperationContextProperty (
                context, 
                WS_OPERATION_CONTEXT_PROPERTY_INPUT_MESSAGE, 
                &requestMessage, 
                sizeof(requestMessage),
                error);
```

Toutes les propriétés de contexte ne sont pas disponibles à un moment donné. Consultez la documentation de la propriété de contexte relative à la disponibilité d’une propriété spécifique dans un rappel ou une [opération de service](service-operation.md).

Pour plus d’informations sur la gestion de la durée de vie du contexte de l’opération et le Threading, consultez la rubrique relative à la [durée de vie du contexte de l’opération](operation-context-lifetime-and-threading.md) .

L’énumération suivante fait partie du contexte :

-   [**\_ID de \_ propriété de contexte \_ \_ de l’opération WS**](/windows/desktop/api/WebServices/ne-webservices-ws_operation_context_property_id)

La fonction suivante fait partie du contexte :

-   [**WsGetOperationContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty)

Le handle suivant fait partie du contexte :

-   [contexte de l' \_ opération WS \_](ws-operation-context.md)

 

 




