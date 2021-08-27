---
title: État de l’appel asynchrone
description: Cette page décrit l’état d’appel asynchrone pour les appels RPC.
ms.assetid: 4a594dad-a8a1-44e9-8648-ddc2539c234c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db7ab00104b305ac87fa87883031d2425f229ce5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478625"
---
# <a name="asynchronous-call-state"></a>État de l’appel asynchrone

Cette page décrit l’état d’appel asynchrone pour les appels RPC.

## <a name="client-behavior"></a>Comportement du client




| State | Nom de l’état | Action | 
|-------|------------|--------|
| C | Effectuer l’appel | Rendre le RPC<ul><li>En cas de réussite, accédez à l’État WComp</li><li>En cas d’exception, aller à la fin</li></ul>Pour échec : atteindre peut<br /> | 
| Puissiez | Annuler l’appel | Appeler <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>accéder à WComp<br /> | 
| WComp | Attendre la fin de l’opération | Attendre la réception de la notification notificationCall-Complete<br /> Aller à la comp.<br /> | 
| Conformes | Completion | Problème <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>aller à la fin<br /> | 
| End | 




 

## <a name="server-behavior"></a>Comportement du serveur



| State | Nom de l’état     | Action                                                                                                                                                                                                              |
|-------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D     | Dispatch       | L’appel est distribué par le runtimeProcess RPC<br/> Aller à la comp.<br/> Pour échouer irrémédiablement (lors de l’exécution sur le thread RPC) : lever l’exception ; aller à la fin<br/> Pour échouer correctement : accédez à un<br/> |
| A     | Abandonner l’appel | Appeler [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall)aller à la fin<br/>                                                                                                                                             |
| Conformes  | Completion     | Problème [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall)aller à la fin<br/>                                                                                                                                      |
| End   |                |                                                                                                                                                                                                                     |



 

 

 





