---
title: API du composant de protocole WebSocket
description: .
ms.assetid: ae73fd5e-9715-448c-b7ca-898f2705e228
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24edd74fe87185db498e6309a7fda5fa091c7d60
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101961"
---
# <a name="websocket-protocol-component-api"></a>API du composant de protocole WebSocket

## <a name="purpose"></a>Objectif

L’API du composant de protocole WebSocket active des canaux de communication bidirectionnels asynchrones sur HTTP qui fonctionnent sur les intermédiaires réseau existants. Avec l’API du composant de protocole WebSocket, un client utilise le protocole HTTP pour communiquer avec un serveur, puis les deux côtés basculent vers à l’aide du protocole sous-jacent sur lequel HTTP a été superposé (par exemple, TCP ou SSL). L’objectif est d’utiliser tout d’abord le protocole HTTP pour traverser les intermédiaires réseau, puis d’utiliser le canal TCP/SSL sous-jacent de bout en bout pour la communication des applications bidirectionnelles. Le protocole WebSocket \[ [WSPROTO](https://tools.ietf.org/html/rfc6455) \] est défini au niveau de l’IETF, tandis qu’un W3CAPI d’API JavaScript associé \[ [](https://dev.w3.org/html5/websockets/) \] est défini au W3C.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                                          | Description                                                                 |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [**Types de données de l’API du composant de protocole WebSocket**](web-socket-protocol-component-api-data-types.md)<br/> | L’API du composant de protocole WebSocket définit ces types de données.<br/>   |
| [Énumérations de l’API du composant de protocole WebSocket](web-socket-protocol-component-api-enumerations.md)<br/> | L’API du composant de protocole WebSocket définit ces énumérations.<br/> |
| [Fonctions de l’API du composant de protocole WebSocket](web-socket-protocol-component-api-functions.md)<br/>       | L’API du composant de protocole WebSocket définit ces fonctions.<br/>    |
| [Structures de l’API du composant de protocole WebSocket](web-socket-protocol-component-api-structures.md)<br/>     | L’API du composant de protocole WebSocket définit ces structures.<br/>   |



 

## <a name="developer-audience"></a>Développeurs concernés

L’API du composant de protocole WebSocket est conçue pour être utilisée par les programmeurs C/C++. Vous devez être familiarisé avec la mise en réseau HTTP et Windows.

> [!Note]  
> La meilleure façon d’utiliser le protocole WebSocket sur Windows consiste à utiliser l' [API Windows http services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page) ou l' [espace de noms Windows. Networking. Sockets](/uwp/api/Windows.Networking.Sockets).

 

## <a name="run-time-requirements"></a>Conditions d’exécution

L’API du composant de protocole WebSocket requiert Windows 8 et les versions ultérieures du système d’exploitation Windows. Les API peuvent être liées de manière dynamique via websocket.dll.

> [!Note]  
> websocket.dll assure la prise en charge des en-têtes HTTP liés aux protocoles client et serveur, vérifie les données de négociation reçues et analyse le flux de données WebSocket. Elle ne gère pas les opérations HTTP spécifiques (redirection, authentification, prise en charge du proxy) et n’effectue aucune opération d’e/s (envoi ou réception d’octets de flux WebSocket).

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[HTTP](/windows/desktop/Http/http-api-start-page)
</dt> <dt>

[Services HTTP Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page)
</dt> </dl>

 

