---
title: État du canal asynchrone
description: Cette page décrit l’état du canal asynchrone pour les appels RPC.
ms.assetid: af937eba-6b70-447a-af76-a8e27f5754e3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a35e54d9f86228cb4c957f53411c105e20e2109
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468166"
---
# <a name="asynchronous-pipe-state"></a>État du canal asynchrone

Cette page décrit l’état du canal asynchrone pour les appels RPC.

## <a name="in-pipe"></a>DANS le canal

Comportement du client


| State | Nom d’état | Action | 
|-------|------------|--------|
| C | Effectuer l’appel | Rendre le RPC<ul><li>En cas de réussite, accédez à l’État WS</li><li>En cas d’exception, aller à la fin</li></ul>Pour échec : atteindre peut<br /> | 
| P | Envoi (push) | Créer un push<ul><li>En cas d’échec, aller à la fin</li><li>En cas de réussite, accédez à WS</li></ul>Pour échec : atteindre peut<br /> | 
| WS | Attendre l’envoi | Attendre la notification<ul><li>En cas d’échec d’une notification, accédez à CAN</li><li>Si un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> de réussite est reçu et que davantage de données doivent être envoyées, accédez à P</li><li>Si un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> de réussite est reçu et que davantage de données n’ont pas besoin d’être envoyées, accédez à NP</li><li>Si une erreur <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcCallComplete</strong></a> est reçue, Go COMP</li></ul>Pour échec : atteindre peut<br /> | 
| NP | Push null | Push 0 octets (push null)<ul><li>En cas d’échec, aller à la fin</li><li>En cas de réussite, accédez à WComp</li></ul>Pour échec : atteindre peut<br /> | 
| Puissiez | Annuler l’appel | Appeler <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>accéder à WComp<br /> | 
| WComp | Attendre la fin de l’opération | L’attente de la notification de fin de notificationCall doit être reçue.<br /> Aller à la comp.<br /> | 
| Conformes | Completion | Problème <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>aller à la fin<br /> | 
| End | 




 

Comportement du serveur


| State | Nom d’état | Action | 
|-------|------------|--------|
| D | Dispatch | L’appel est distribué par le runtime RPC accéder à P<br /> Pour échouer irrémédiablement (lors de l’exécution sur le thread RPC) : lever l’exception ; aller à la fin<br /> Pour échouer correctement : accédez à un<br /> | 
| P | Extraction | Créer une extraction<ul><li>En cas d’échec, aller à la fin</li><li>En cas de réussite et d’achèvement synchrone avec des octets non nuls lus, accéder à P</li><li>En cas de réussite et d’achèvement synchrone avec zéro octet de lecture (extraction null), atteindre la comp.</li><li>En cas de réussite et d’achèvement asynchrone (retournée ERROR_IO_PENDING), accédez à WP</li></ul>Pour faire échouer : accédez à un<br /> | 
| WP | Attendre l’extraction | Attendre la notification<ul><li>En cas d’échec de la saisie semi-automatique, accédez à</li><li>Si une erreur <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> est reçue, accédez à un</li><li>Si un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> de réussite est reçu avec des octets non nuls lus, aller à P</li><li>Si un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> de réussite est reçu avec zéro octet de lecture (extraction null), atteindre la comp.</li><li>Si une défaillance est reçue, accédez à un</li></ul>Pour faire échouer : accédez à un<br /> | 
| A | Abandonner l’appel | Appeler <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>aller à la fin<br /> | 
| Conformes | Completion | Appeler <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>aller à la fin<br /> | 
| End | 




 

## <a name="out-pipe"></a>Canal de sortie

Comportement du client


| State | Nom d’état | Action | 
|-------|------------|--------|
| C | Effectuer l’appel | Rendre le RPC<ul><li>En cas de réussite, accédez à P</li><li>En cas d’échec, accédez à COMP</li></ul>Pour échec : atteindre peut<br /> | 
| P | Extraction | Créer une extraction<ul><li>En cas d’échec, aller à la fin</li><li>En cas de réussite et d’achèvement synchrone avec des octets non nuls lus, accéder à P</li><li>En cas de réussite et d’achèvement synchrone avec zéro octet de lecture (extraction null), accédez à WComp</li><li>En cas de réussite et d’achèvement asynchrone (retournée ERROR_IO_PENDING), accédez à WP</li></ul>Pour échec : atteindre peut<br /> | 
| WP | Attendre l’extraction | Attendre la notification<ul><li>En cas d’échec de la saisie semi-automatique, accédez à CAN</li><li>Si une erreur <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> est reçue, accéder à peut</li><li>Si un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> de réussite est reçu avec des octets non nuls lus, aller à P</li><li>Si un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> de réussite est reçu avec zéro octet de lecture (extraction null), atteindre la comp.</li><li>Si une défaillance est reçue, Go peut</li></ul>Pour échec : atteindre peut<br /> | 
| Puissiez | Annuler l’appel | Appeler <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>accéder à WComp<br /> | 
| WComp | Attendre la fin de l’opération | Attendre la notification. La notification de fin d’appel doit être reçue.<br /> Aller à la comp.<br /> | 
| Conformes | Completion | Problème <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>aller à la fin<br /> | 
| End | 




 

Comportement du serveur


| State | Nom d’état | Action | 
|-------|------------|--------|
| D | Dispatch | L’appel est distribué par le runtime RPC accéder à P<br /> Pour échouer irrémédiablement (lors de l’exécution sur le thread RPC) : lever l’exception ; aller à la fin<br /> Pour échouer correctement : accédez à un<br /> | 
| P | Envoi (push) | Créer un push<ul><li>En cas de réussite, accédez à WP</li><li>En cas d’échec, aller à la fin</li></ul>Pour faire échouer : accédez à un<br /> | 
| WP | Attendre la notification push | Attendre la notification<ul><li>En cas d’échec de la saisie semi-automatique, accédez à</li><li>Si un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> de réussite est reçu et que davantage de données doivent être envoyées, accédez à P</li><li>Si un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> de réussite est reçu et que davantage de données n’ont pas besoin d’être envoyées, accédez à NP</li><li>Si une défaillance est reçue, cliquez sur COMP</li></ul>Pour faire échouer : accédez à un<br /> | 
| NP | Push null | Pousser 0 octets<ul><li>en cas de réussite, accédez à WNP</li><li>en cas d’échec, accédez à COMP</li></ul>Pour faire échouer : accédez à un<br /> | 
| WNP | Attendre une notification push null | Attendre la notification<ul><li>En cas d’échec de la saisie semi-automatique, accédez à</li><li>Si une défaillance est reçue, cliquez sur COMP</li><li>Si une réussite est reçue, Go COMP</li></ul> | 
| A | Abandonner l’appel | Appelez <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>; aller à la fin | 
| Conformes | Completion | Problème <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>; aller à la fin | 
| End | 




 

## <a name="in-out-pipe"></a>Canal de sortie

Comportement du client


| State | Nom d’état | Action | 
|-------|------------|--------|
| C | Effectuer l’appel | Rendre le RPC<ul><li>En cas de réussite, accédez à WS</li><li>En cas d’exception, aller à la fin</li></ul>Pour échec : atteindre peut<br /> | 
| PS | Envoi (push) | Créer un push<ul><li>En cas d’échec, aller à la fin</li><li>En cas de réussite, accédez à WS</li></ul>Pour échec : atteindre peut<br /> | 
| WS | Attendre l’envoi | Attendre la notification<ul><li>En cas d’échec d’une notification, accédez à CAN</li><li>Si un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> de réussite est reçu et que davantage de données doivent être envoyées, accédez à PS</li><li>Si un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> de réussite est reçu et que davantage de données n’ont pas besoin d’être envoyées, accédez à NP</li><li>Si une erreur <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcCallComplete</strong></a> est reçue, Go COMP</li></ul>Pour échec : atteindre peut<br /> | 
| NP | Push null | Push 0 octets (push null)<ul><li>En cas d’échec, aller à la fin</li><li>En cas de réussite, accédez à PL</li></ul>Pour échec : atteindre peut<br /> | 
| PL | Extraction | Créer une extraction<ul><li>En cas d’échec, aller à la fin</li><li>En cas de réussite et d’achèvement synchrone avec des octets non nuls lus, accédez à PL</li><li>En cas de réussite et d’achèvement synchrone avec zéro octet de lecture (extraction null), accédez à WComp</li><li>En cas de réussite et d’achèvement asynchrone (ERROR_IO_PENDING est retourné), accédez à WPL</li></ul>Pour échec : atteindre peut<br /> | 
| WPL | Attendre l’extraction | Attendre la notification<ul><li>En cas d’échec de la saisie semi-automatique, accédez à CAN</li><li>Si une erreur <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> est reçue, accéder à peut</li><li>Si un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> de réussite est reçu avec des octets non nuls lus, accédez à pl</li><li>Si un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> de réussite est reçu avec zéro octet lu atteindre la comp.</li><li>Si une défaillance est reçue, Go peut</li></ul>Pour échec : atteindre peut<br /> | 
| Puissiez | Annuler l’appel | Appeler <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>accéder à WComp<br /> | 
| WComp | Attendre la fin de l’opération | Attendre la notification. La notification CallComplete doit être reçue.<br /> Aller à la comp.<br /> | 
| Conformes | Completion | Problème <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>aller à la fin<br /> | 
| End | 




 

Comportement du serveur


| State | Nom d’état | Action | 
|-------|------------|--------|
| D | Dispatch | L’appel est distribué par le runtimeGo RPC à PL<br /> Pour échouer irrémédiablement (lors de l’exécution sur le thread RPC) : lever l’exception ; aller à la fin<br /> Pour échouer correctement : accédez à un<br /> | 
| PL | Extraction | Créer une extraction<ul><li>En cas d’échec, aller à la fin</li><li>En cas de réussite et d’achèvement synchrone avec des octets non nuls lus, accédez à PL</li><li>En cas de réussite et d’achèvement synchrone avec zéro octet de lecture (extraction null), accédez à PS</li><li>En cas de réussite et d’achèvement asynchrone (ERROR_IO_PENDING est retourné), accédez à WPL</li></ul>Pour faire échouer : accédez à un<br /> | 
| WPL | Attendre l’extraction | Attendre la notification<ul><li>En cas d’échec de la saisie semi-automatique, accédez à</li><li>Si une erreur <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> est reçue, accédez à un</li><li>Si un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> de réussite est reçu avec des octets non nuls lus, accédez à pl</li><li>Si un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> de réussite est reçu avec zéro octet lu, accédez à PS</li><li>Si une défaillance est reçue, accédez à</li></ul>Pour faire échouer : accédez à un<br /> | 
| PS | Envoi (push) | Créer un push<ul><li>En cas de réussite, accédez à WPS</li><li>En cas d’échec, aller à la fin</li></ul>Pour faire échouer : accédez à un<br /> | 
| WP | Attendre la notification push | Attendre la notification<ul><li>En cas d’échec de la saisie semi-automatique, accédez à</li><li>Si un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> de réussite est reçu et que davantage de données doivent être envoyées, accédez à PS</li><li>Si un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> de réussite est reçu et que davantage de données n’ont pas besoin d’être envoyées, accédez à NP</li><li>Si une défaillance est reçue, cliquez sur COMP</li></ul>Pour faire échouer : accédez à un<br /> | 
| NP | Push null | Pousser 0 octets<ul><li>en cas de réussite, accédez à WNP</li><li>en cas d’échec, accédez à COMP</li></ul>Pour faire échouer : accédez à un<br /> | 
| WNP | Attendre une notification push null | Attendre la notification<ul><li>En cas d’échec de la saisie semi-automatique, accédez à</li><li>Si une défaillance est reçue, cliquez sur COMP</li><li>Si une réussite est reçue, Go COMP</li></ul><br /> | 
| A | Abandonner l’appel | Appelez <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>; aller à la fin | 
| Conformes | Completion | Problème <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>; aller à la fin | 
| End | 




 

 

 





