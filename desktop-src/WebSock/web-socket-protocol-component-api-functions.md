---
title: Fonctions de l’API du composant de protocole WebSocket
description: L’API du composant de protocole WebSocket définit ces fonctions.
ms.assetid: B833D18D-286C-4D32-A9C7-D5D5806EC306
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d778fef6680112007b0f4a459787a51eb20bfe0d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127517721"
---
# <a name="websocket-protocol-component-api-functions"></a>Fonctions de l’API du composant de protocole WebSocket

L’API du composant de protocole WebSocket définit ces fonctions.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                             | Description                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WebSocketAbortHandle**](/windows/desktop/api/Websocket/nf-websocket-websocketaborthandle)<br/>                   | abandonne un handle de session WebSocket créé par [**WebSocketCreateClientHandle**](/windows/desktop/api/websocket/nf-websocket-websocketcreateclienthandle) ou [**WebSocketCreateServerHandle**](/windows/desktop/api/websocket/nf-websocket-websocketcreateserverhandle).<br/>   |
| [**WebSocketBeginClientHandshake**](/windows/desktop/api/Websocket/nf-websocket-websocketbeginclienthandshake)<br/> | commence le protocole de transfert côté client.<br/>                                                                                                                                                                |
| [**WebSocketBeginServerHandshake**](/windows/desktop/api/Websocket/nf-websocket-websocketbeginserverhandshake)<br/> | commence le protocole de transfert côté serveur.<br/>                                                                                                                                                                |
| [**WebSocketCompleteAction**](/windows/desktop/api/Websocket/nf-websocket-websocketcompleteaction)<br/>             | termine une action démarrée par [**WebSocketGetAction**](/windows/desktop/api/websocket/nf-websocket-websocketgetaction).<br/>                                                                                                             |
| [**WebSocketCreateClientHandle**](/windows/desktop/api/Websocket/nf-websocket-websocketcreateclienthandle)<br/>     | crée un handle de session WebSocket côté client.<br/>                                                                                                                                                  |
| [**WebSocketCreateServerHandle**](/windows/desktop/api/Websocket/nf-websocket-websocketcreateserverhandle)<br/>     | crée un handle de session WebSocket côté serveur.<br/>                                                                                                                                                  |
| [**WebSocketDeleteHandle**](/windows/desktop/api/Websocket/nf-websocket-websocketdeletehandle)<br/>                 | supprime un handle de session WebSocket créé par [**WebSocketCreateClientHandle**](/windows/desktop/api/websocket/nf-websocket-websocketcreateclienthandle) ou [**WebSocketCreateServerHandle**](/windows/desktop/api/websocket/nf-websocket-websocketcreateserverhandle).<br/>  |
| [**WebSocketEndClientHandshake**](/windows/desktop/api/Websocket/nf-websocket-websocketendclienthandshake)<br/>     | termine le protocole de transfert côté client.<br/>                                                                                                                                                             |
| [**WebSocketEndServerHandshake**](/windows/desktop/api/Websocket/nf-websocket-websocketendserverhandshake)<br/>     | termine le protocole de transfert côté serveur.<br/>                                                                                                                                                             |
| [**WebSocketGetAction**](/windows/desktop/api/Websocket/nf-websocket-websocketgetaction)<br/>                       | retourne une action à partir d’un appel à [**WebSocketSend**](/windows/desktop/api/websocket/nf-websocket-websocketsend), [**WebSocketReceive**](/windows/desktop/api/websocket/nf-websocket-websocketreceive) ou [**WebSocketCompleteAction**](/windows/desktop/api/websocket/nf-websocket-websocketcompleteaction).<br/> |
| [**WebSocketGetGlobalProperty**](/windows/desktop/api/Websocket/nf-websocket-websocketgetglobalproperty)<br/>       | Obtient une propriété WebSocket unique.<br/>                                                                                                                                                                |
| [**WebSocketReceive**](/windows/desktop/api/Websocket/nf-websocket-websocketreceive)<br/>                           | Ajoute une opération Receive à la file d’attente des opérations du composant de protocole.<br/>                                                                                                                              |
| [**WebSocketSend**](/windows/desktop/api/Websocket/nf-websocket-websocketsend)<br/>                                 | Ajoute une opération d’envoi à la file d’attente des opérations du composant de protocole.<br/>                                                                                                                                 |



 

 

