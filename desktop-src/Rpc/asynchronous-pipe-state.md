---
title: État du canal asynchrone
description: Cette page décrit l’état du canal asynchrone pour les appels RPC.
ms.assetid: af937eba-6b70-447a-af76-a8e27f5754e3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8396b08c7ef7b8152457d9426883645fab39bdef
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104030813"
---
# <a name="asynchronous-pipe-state"></a>État du canal asynchrone

Cette page décrit l’état du canal asynchrone pour les appels RPC.

## <a name="in-pipe"></a>DANS le canal

Comportement du client

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>State</th>
<th>Nom d’état</th>
<th>Action</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>C</td>
<td>Effectuer l’appel</td>
<td>Rendre le RPC
<ul>
<li>En cas de réussite, accédez à l’État WS</li>
<li>En cas d’exception, aller à la fin</li>
</ul>
Pour échec : atteindre peut<br/></td>
</tr>
<tr class="even">
<td>P</td>
<td>Envoi de données (push)</td>
<td>Créer un push
<ul>
<li>En cas d’échec, aller à la fin</li>
<li>En cas de réussite, accédez à WS</li>
</ul>
Pour échec : atteindre peut<br/></td>
</tr>
<tr class="odd">
<td>WS</td>
<td>Attendre l’envoi</td>
<td>Attendre la notification
<ul>
<li>En cas d’échec d’une notification, accédez à CAN</li>
<li>Si un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> de réussite est reçu et que davantage de données doivent être envoyées, accédez à P</li>
<li>Si un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> de réussite est reçu et que davantage de données n’ont pas besoin d’être envoyées, accédez à NP</li>
<li>Si une erreur <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcCallComplete</strong></a> est reçue, Go COMP</li>
</ul>
Pour échec : atteindre peut<br/></td>
</tr>
<tr class="even">
<td>NP</td>
<td>Push null</td>
<td>Push 0 octets (push null)
<ul>
<li>En cas d’échec, aller à la fin</li>
<li>En cas de réussite, accédez à WComp</li>
</ul>
Pour échec : atteindre peut<br/></td>
</tr>
<tr class="odd">
<td>Puissiez</td>
<td>Annuler l’appel</td>
<td>Appeler <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>accéder à WComp<br/></td>
</tr>
<tr class="even">
<td>WComp</td>
<td>Attendre la fin de l’opération</td>
<td>L’attente de la notification de fin de notificationCall doit être reçue.<br/> Aller à la comp.<br/></td>
</tr>
<tr class="odd">
<td>Conformes</td>
<td>Completion</td>
<td>Problème <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>aller à la fin<br/></td>
</tr>
<tr class="even">
<td>End</td>


</tr>
</tbody>
</table>



 

Comportement du serveur

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>State</th>
<th>Nom d’état</th>
<th>Action</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D</td>
<td>Dispatch</td>
<td>L’appel est distribué par le runtime RPC accéder à P<br/> Pour échouer irrémédiablement (lors de l’exécution sur le thread RPC) : lever l’exception ; aller à la fin<br/> Pour échouer correctement : accédez à un<br/></td>
</tr>
<tr class="even">
<td>P</td>
<td>Extraction</td>
<td>Créer une extraction
<ul>
<li>En cas d’échec, aller à la fin</li>
<li>En cas de réussite et d’achèvement synchrone avec des octets non nuls lus, accéder à P</li>
<li>En cas de réussite et d’achèvement synchrone avec zéro octet de lecture (extraction null), atteindre la comp.</li>
<li>En cas de réussite et d’achèvement asynchrone (retournée ERROR_IO_PENDING), accédez à WP</li>
</ul>
Pour faire échouer : accédez à un<br/></td>
</tr>
<tr class="odd">
<td>WP</td>
<td>Attendre l’extraction</td>
<td>Attendre la notification
<ul>
<li>En cas d’échec de la saisie semi-automatique, accédez à</li>
<li>Si une erreur <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> est reçue, accédez à un</li>
<li>Si un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> de réussite est reçu avec des octets non nuls lus, aller à P</li>
<li>Si un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> de réussite est reçu avec zéro octet de lecture (extraction null), atteindre la comp.</li>
<li>Si une défaillance est reçue, accédez à un</li>
</ul>
Pour faire échouer : accédez à un<br/></td>
</tr>
<tr class="even">
<td>Un</td>
<td>Abandonner l’appel</td>
<td>Appeler <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>aller à la fin<br/></td>
</tr>
<tr class="odd">
<td>Conformes</td>
<td>Completion</td>
<td>Appeler <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>aller à la fin<br/></td>
</tr>
<tr class="even">
<td>End</td>


</tr>
</tbody>
</table>



 

## <a name="out-pipe"></a>Canal de sortie

Comportement du client

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>State</th>
<th>Nom d’état</th>
<th>Action</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>C</td>
<td>Effectuer l’appel</td>
<td>Rendre le RPC
<ul>
<li>En cas de réussite, accédez à P</li>
<li>En cas d’échec, accédez à COMP</li>
</ul>
Pour échec : atteindre peut<br/></td>
</tr>
<tr class="even">
<td>P</td>
<td>Extraction</td>
<td>Créer une extraction
<ul>
<li>En cas d’échec, aller à la fin</li>
<li>En cas de réussite et d’achèvement synchrone avec des octets non nuls lus, accéder à P</li>
<li>En cas de réussite et d’achèvement synchrone avec zéro octet de lecture (extraction null), accédez à WComp</li>
<li>En cas de réussite et d’achèvement asynchrone (retournée ERROR_IO_PENDING), accédez à WP</li>
</ul>
Pour échec : atteindre peut<br/></td>
</tr>
<tr class="odd">
<td>WP</td>
<td>Attendre l’extraction</td>
<td>Attendre la notification
<ul>
<li>En cas d’échec de la saisie semi-automatique, accédez à CAN</li>
<li>Si une erreur <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> est reçue, accéder à peut</li>
<li>Si un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> de réussite est reçu avec des octets non nuls lus, aller à P</li>
<li>Si un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> de réussite est reçu avec zéro octet de lecture (extraction null), atteindre la comp.</li>
<li>Si une défaillance est reçue, Go peut</li>
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
<td>Attendre la notification. La notification de fin d’appel doit être reçue.<br/> Aller à la comp.<br/></td>
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



 

Comportement du serveur

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>State</th>
<th>Nom d’état</th>
<th>Action</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D</td>
<td>Dispatch</td>
<td>L’appel est distribué par le runtime RPC accéder à P<br/> Pour échouer irrémédiablement (lors de l’exécution sur le thread RPC) : lever l’exception ; aller à la fin<br/> Pour échouer correctement : accédez à un<br/></td>
</tr>
<tr class="even">
<td>P</td>
<td>Envoi de données (push)</td>
<td>Créer un push
<ul>
<li>En cas de réussite, accédez à WP</li>
<li>En cas d’échec, aller à la fin</li>
</ul>
Pour faire échouer : accédez à un<br/></td>
</tr>
<tr class="odd">
<td>WP</td>
<td>Attendre la notification push</td>
<td>Attendre la notification
<ul>
<li>En cas d’échec de la saisie semi-automatique, accédez à</li>
<li>Si un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> de réussite est reçu et que davantage de données doivent être envoyées, accédez à P</li>
<li>Si un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> de réussite est reçu et que davantage de données n’ont pas besoin d’être envoyées, accédez à NP</li>
<li>Si une défaillance est reçue, cliquez sur COMP</li>
</ul>
Pour faire échouer : accédez à un<br/></td>
</tr>
<tr class="even">
<td>NP</td>
<td>Push null</td>
<td>Pousser 0 octets
<ul>
<li>en cas de réussite, accédez à WNP</li>
<li>en cas d’échec, accédez à COMP</li>
</ul>
Pour faire échouer : accédez à un<br/></td>
</tr>
<tr class="odd">
<td>WNP</td>
<td>Attendre une notification push null</td>
<td>Attendre la notification
<ul>
<li>En cas d’échec de la saisie semi-automatique, accédez à</li>
<li>Si une défaillance est reçue, cliquez sur COMP</li>
<li>Si une réussite est reçue, Go COMP</li>
</ul></td>
</tr>
<tr class="even">
<td>Un</td>
<td>Abandonner l’appel</td>
<td>Appelez <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>; aller à la fin</td>
</tr>
<tr class="odd">
<td>Conformes</td>
<td>Completion</td>
<td>Problème <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>; aller à la fin</td>
</tr>
<tr class="even">
<td>End</td>


</tr>
</tbody>
</table>



 

## <a name="in-out-pipe"></a>Canal de sortie

Comportement du client

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>State</th>
<th>Nom d’état</th>
<th>Action</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>C</td>
<td>Effectuer l’appel</td>
<td>Rendre le RPC
<ul>
<li>En cas de réussite, accédez à WS</li>
<li>En cas d’exception, aller à la fin</li>
</ul>
Pour échec : atteindre peut<br/></td>
</tr>
<tr class="even">
<td>PS</td>
<td>Envoi de données (push)</td>
<td>Créer un push
<ul>
<li>En cas d’échec, aller à la fin</li>
<li>En cas de réussite, accédez à WS</li>
</ul>
Pour échec : atteindre peut<br/></td>
</tr>
<tr class="odd">
<td>WS</td>
<td>Attendre l’envoi</td>
<td>Attendre la notification
<ul>
<li>En cas d’échec d’une notification, accédez à CAN</li>
<li>Si un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> de réussite est reçu et que davantage de données doivent être envoyées, accédez à PS</li>
<li>Si un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> de réussite est reçu et que davantage de données n’ont pas besoin d’être envoyées, accédez à NP</li>
<li>Si une erreur <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcCallComplete</strong></a> est reçue, Go COMP</li>
</ul>
Pour échec : atteindre peut<br/></td>
</tr>
<tr class="even">
<td>NP</td>
<td>Push null</td>
<td>Push 0 octets (push null)
<ul>
<li>En cas d’échec, aller à la fin</li>
<li>En cas de réussite, accédez à PL</li>
</ul>
Pour échec : atteindre peut<br/></td>
</tr>
<tr class="odd">
<td>PL</td>
<td>Extraction</td>
<td>Créer une extraction
<ul>
<li>En cas d’échec, aller à la fin</li>
<li>En cas de réussite et d’achèvement synchrone avec des octets non nuls lus, accédez à PL</li>
<li>En cas de réussite et d’achèvement synchrone avec zéro octet de lecture (extraction null), accédez à WComp</li>
<li>En cas de réussite et d’achèvement asynchrone (ERROR_IO_PENDING est retourné), accédez à WPL</li>
</ul>
Pour échec : atteindre peut<br/></td>
</tr>
<tr class="even">
<td>WPL</td>
<td>Attendre l’extraction</td>
<td>Attendre la notification
<ul>
<li>En cas d’échec de la saisie semi-automatique, accédez à CAN</li>
<li>Si une erreur <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> est reçue, accéder à peut</li>
<li>Si un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> de réussite est reçu avec des octets non nuls lus, accédez à pl</li>
<li>Si un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> de réussite est reçu avec zéro octet lu atteindre la comp.</li>
<li>Si une défaillance est reçue, Go peut</li>
</ul>
Pour échec : atteindre peut<br/></td>
</tr>
<tr class="odd">
<td>Puissiez</td>
<td>Annuler l’appel</td>
<td>Appeler <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>accéder à WComp<br/></td>
</tr>
<tr class="even">
<td>WComp</td>
<td>Attendre la fin de l’opération</td>
<td>Attendre la notification. La notification CallComplete doit être reçue.<br/> Aller à la comp.<br/></td>
</tr>
<tr class="odd">
<td>Conformes</td>
<td>Completion</td>
<td>Problème <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>aller à la fin<br/></td>
</tr>
<tr class="even">
<td>End</td>


</tr>
</tbody>
</table>



 

Comportement du serveur

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>State</th>
<th>Nom d’état</th>
<th>Action</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D</td>
<td>Dispatch</td>
<td>L’appel est distribué par le runtimeGo RPC à PL<br/> Pour échouer irrémédiablement (lors de l’exécution sur le thread RPC) : lever l’exception ; aller à la fin<br/> Pour échouer correctement : accédez à un<br/></td>
</tr>
<tr class="even">
<td>PL</td>
<td>Extraction</td>
<td>Créer une extraction
<ul>
<li>En cas d’échec, aller à la fin</li>
<li>En cas de réussite et d’achèvement synchrone avec des octets non nuls lus, accédez à PL</li>
<li>En cas de réussite et d’achèvement synchrone avec zéro octet de lecture (extraction null), accédez à PS</li>
<li>En cas de réussite et d’achèvement asynchrone (ERROR_IO_PENDING est retourné), accédez à WPL</li>
</ul>
Pour faire échouer : accédez à un<br/></td>
</tr>
<tr class="odd">
<td>WPL</td>
<td>Attendre l’extraction</td>
<td>Attendre la notification
<ul>
<li>En cas d’échec de la saisie semi-automatique, accédez à</li>
<li>Si une erreur <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> est reçue, accédez à un</li>
<li>Si un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> de réussite est reçu avec des octets non nuls lus, accédez à pl</li>
<li>Si un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> de réussite est reçu avec zéro octet lu, accédez à PS</li>
<li>Si une défaillance est reçue, accédez à</li>
</ul>
Pour faire échouer : accédez à un<br/></td>
</tr>
<tr class="even">
<td>PS</td>
<td>Envoi de données (push)</td>
<td>Créer un push
<ul>
<li>En cas de réussite, accédez à WPS</li>
<li>En cas d’échec, aller à la fin</li>
</ul>
Pour faire échouer : accédez à un<br/></td>
</tr>
<tr class="odd">
<td>WP</td>
<td>Attendre la notification push</td>
<td>Attendre la notification
<ul>
<li>En cas d’échec de la saisie semi-automatique, accédez à</li>
<li>Si un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> de réussite est reçu et que davantage de données doivent être envoyées, accédez à PS</li>
<li>Si un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> de réussite est reçu et que davantage de données n’ont pas besoin d’être envoyées, accédez à NP</li>
<li>Si une défaillance est reçue, cliquez sur COMP</li>
</ul>
Pour faire échouer : accédez à un<br/></td>
</tr>
<tr class="even">
<td>NP</td>
<td>Push null</td>
<td>Pousser 0 octets
<ul>
<li>en cas de réussite, accédez à WNP</li>
<li>en cas d’échec, accédez à COMP</li>
</ul>
Pour faire échouer : accédez à un<br/></td>
</tr>
<tr class="odd">
<td>WNP</td>
<td>Attendre une notification push null</td>
<td>Attendre la notification
<ul>
<li>En cas d’échec de la saisie semi-automatique, accédez à</li>
<li>Si une défaillance est reçue, cliquez sur COMP</li>
<li>Si une réussite est reçue, Go COMP</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td>Un</td>
<td>Abandonner l’appel</td>
<td>Appelez <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>; aller à la fin</td>
</tr>
<tr class="odd">
<td>Conformes</td>
<td>Completion</td>
<td>Problème <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>; aller à la fin</td>
</tr>
<tr class="even">
<td>End</td>


</tr>
</tbody>
</table>



 

 

 





