---
title: Annulation d’appel
description: La notification d’annulation d’appel annule l’opération d’opérations de service côté serveur et de rappels de modèle de service.
ms.assetid: dc371921-869f-4775-98d3-80a1006358ba
keywords:
- Appeler des services Web d’annulation pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dda4ec4227403bed5239b68cfa05d2064976517a7473fa7926c8de5f56227645
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026697"
---
# <a name="call-cancellation"></a>Annulation d’appel

La notification d’annulation d’appel annule l’opération d' [opérations de service côté serveur](server-side-service-operations.md) et de rappels de modèle de service. Cette annulation peut être pour l’une des deux raisons suivantes :

-   L’hôte de service a arrêté les opérations en raison d’un appel à la fonction [**WsAbortServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsabortservicehost) .
-   Le canal sous-jacent a généré une erreur.


Pour recevoir une notification d’annulation, le rappel de l’opération de service ou du modèle de service doit inscrire un rappel d' [**annulation de \_ \_ \_ rappel de l’opération WS**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback) en appelant la fonction [**WsRegisterOperationForCancel**](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel) .

Si vous le souhaitez, dans le cadre de la notification d’annulation, le rappel de l’opération de service ou du modèle de service peut également enregistrer les données d’État spécifiques à l’application et le rappel de rappel de l' [**\_ \_ \_ état \_ libre de l’opération WS**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback) .

Les données d’État sont mises à la disposition du rappel de rappel d’annulation de l' [**\_ opération \_ \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback) . À la fin de l’appel, le rappel de rappel de l' [**\_ \_ \_ état \_ libre de l’opération WS**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback) est appelé pour permettre à l’application de libérer les données d’État.

Pour obtenir un exemple de code, consultez [BlockingServiceExample](blockingserviceexample.md).

Le rappel d’annulation est appelé une seule fois pendant la durée de vie des [opérations de service côté serveur](server-side-service-operations.md) ou de la fonction de rappel.

L’annulation d’appel est disponible dans pour tous les rappels d’hôte de service qui prennent le [ \_ \_ contexte WS Operation](ws-operation-context.md) comme paramètre.

Les éléments d’API suivants sont liés à l’annulation d’appel.

| Rappel                                                                         | Description                                                                                                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**rappel d’annulation de l' \_ opération WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback)          | Appelée par le modèle de service pour notifier l’annulation d’une opération de service asynchrone à la suite d’un arrêt abandonné de l’hôte de service. |
| [**\_rappel de \_ l' \_ état \_ libre de l’opération WS**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback) | Appelée par le modèle de service pour permettre à une application de nettoyer les données d’État qui ont été inscrites avec le rappel d’annulation.                |



 



| Fonction                                                             | Description                                                                                       |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**WsRegisterOperationForCancel**](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel) | Permet à une opération de service ou à un rappel de modèle de service de s’inscrire pour une notification d’annulation. |



 

 

 




