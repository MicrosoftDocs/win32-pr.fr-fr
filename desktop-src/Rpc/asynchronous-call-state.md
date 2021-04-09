---
title: État de l’appel asynchrone
description: Cette page décrit l’état d’appel asynchrone pour les appels RPC.
ms.assetid: 4a594dad-a8a1-44e9-8648-ddc2539c234c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96331a18b267b2e44072840727c8fd06afd11d6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840854"
---
# <a name="asynchronous-call-state"></a>État de l’appel asynchrone

Cette page décrit l’état d’appel asynchrone pour les appels RPC.

## <a name="client-behavior"></a>Comportement du client



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>State</th>
<th>Nom de l’état</th>
<th>Action</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>C</td>
<td>Effectuer l’appel</td>
<td>Rendre le RPC
<ul>
<li>En cas de réussite, accédez à l’État WComp</li>
<li>En cas d’exception, aller à la fin</li>
</ul>
Pour échec : atteindre peut<br/></td>
</tr>
<tr class="even">
<td>Puissiez</td>
<td>Annuler l’appel</td>
<td>Appeler <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>accéder à WComp<br/></td>
</tr>
<tr class="odd">
<td>WComp</td>
<td>Attendre la fin de l’opération</td>
<td>Attendre la réception de la notification notificationCall-Complete<br/> Aller à la comp.<br/></td>
</tr>
<tr class="even">
<td>Conformes</td>
<td>Completion</td>
<td>Problème <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>aller à la fin<br/></td>
</tr>
<tr class="odd">
<td>End</td>


</tr>
</tbody>
</table>



 

## <a name="server-behavior"></a>Comportement du serveur



| State | Nom de l’état     | Action                                                                                                                                                                                                              |
|-------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D     | Dispatch       | L’appel est distribué par le runtimeProcess RPC<br/> Aller à la comp.<br/> Pour échouer irrémédiablement (lors de l’exécution sur le thread RPC) : lever l’exception ; aller à la fin<br/> Pour échouer correctement : accédez à un<br/> |
| Un     | Abandonner l’appel | Appeler [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall)aller à la fin<br/>                                                                                                                                             |
| Conformes  | Completion     | Problème [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall)aller à la fin<br/>                                                                                                                                      |
| End   |                |                                                                                                                                                                                                                     |



 

 

 





