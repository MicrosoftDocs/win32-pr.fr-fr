---
title: Proxy de service et sessions
description: Le proxy de service a des comportements spéciaux pour les liaisons de canal de session et non basées sur une session.
ms.assetid: 6dc9de95-b97c-4acc-9d45-d5e6ebb6bd77
keywords:
- Services Web proxy de service et sessions pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc8477a8cd03579e1d8cbfe4509f89890af8482
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104032111"
---
# <a name="service-proxy-and-sessions"></a>Proxy de service et sessions

Le [proxy de service](service-proxy.md) a des comportements spéciaux pour les liaisons de canal de session et non basées sur une session. Le proxy de service fournit une sémantique basée sur une session si la liaison de canal sous-jacente est basée sur une session. Dans ce cas, un canal unique est utilisé pour traiter les appels. Toutefois, si la liaison de canal n’est pas basée sur une session, le proxy de service crée un canal distinct pour chaque appel. Notez, cependant, que les canaux non basés sur une session sont regroupés et peuvent être réutilisés. Dans la réutilisation d’un canal, le proxy de service maintient le canal ouvert si le canal sous-jacent n’a pas généré d’erreur ou si l’appel sur un canal a entraîné une erreur du proxy de service. Notez que. sauf en cas d’erreur, une fois qu’un canal est ouvert, il est maintenu ouvert tant que le proxy de service est ouvert et qu’il est fermé uniquement lorsque le proxy de service est fermé.


Si la liaison de canal est basée sur une session et si le canal sous-jacent est défaillant, l’ordinateur d’État du proxy de service passera à l’état d’erreur de l' [**\_ État du \_ proxy \_ \_ WS service**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) . Dans le cas d’une liaison de canal non basée sur une session, une erreur dans le canal sous-jacent n’entraîne pas la transition du proxy vers l’état d’erreur de l' **\_ État du \_ proxy \_ \_ WS service** .

Pour plus d’informations sur le proxy de service et sa relation avec l’État, consultez la rubrique [service proxy](service-proxy.md) . Pour obtenir des exemples de liaisons de canal différentes, consultez les exemples suivants :

-   liaison de canal non-session, [HttpCalculatorClientExample](httpcalculatorclientexample.md)
-   liaison de canal basée sur une session, [SessionfullCalculatorClientExample](sessionfullcalculatorclientexample.md)

 

 




