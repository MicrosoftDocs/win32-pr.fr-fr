---
title: Utilisation de MSMQ en tant que transport RPC
description: Le sous-système RPC prend en charge l’utilisation de MSMQ en tant que transport en mode synchrone et asynchrone.
ms.assetid: c3f96a91-b7bb-4c2a-8699-2100324af165
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab18f4476815929e8a7e6fb4e4a1eef0a4e4e34754ac134f023c8551899e0138
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010677"
---
# <a name="using-msmq-as-an-rpc-transport"></a>Utilisation de MSMQ en tant que transport RPC

Le sous-système RPC prend en charge l’utilisation de MSMQ en tant que transport en mode synchrone et asynchrone.

Le mode synchrone utilise des appels de procédure distante conventionnels. Ces appels utilisent des points de terminaison connus et le transport de file d’attente de messages, [ncadg \_ MQ](/windows/desktop/Midl/ncadg-mq), comme protocole de transport. En mode synchrone, vos procédures distantes peuvent avoir des \[ paramètres [in](/windows/desktop/Midl/in) \] et \[ [out](/windows/desktop/Midl/out-idl) \] et peuvent utiliser les services de sécurité RPC standard. Le sous-système RPC crée une file d’attente de réponses pour les appels distants contenant des paramètres de **\[ sortie \]** . Le mode synchrone est utile pour les applications où le client a besoin de recevoir des données du serveur. La principale limitation de ce mode est que, comme pour les appels de procédure distante conventionnels, le client et le serveur doivent tous deux être en cours d’exécution et rester en cours d’exécution pendant la durée de l’appel.

Le mode asynchrone permet aux applications clientes d’effectuer des appels au serveur et de les retourner immédiatement, quel que soit l’état de l’application serveur ou de l’ordinateur serveur. Il fournit également un sous-ensemble de fonctionnalités MSMQ pour gérer les files d’attente de messages et le workflow d’informations. La fonction [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) vous permet de contrôler la qualité de service, la priorité d’appel, la journalisation, la sécurité et la durée de vie de la file d’attente de processus serveur. La fonction [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) vous permet de spécifier des attributs de la file d’attente des processus serveur, tels que la persistance de la file d’attente, l’authentification et le chiffrement.

Vous implémentez le MSMQ asynchrone comme vous le feriez avec MSMQ synchrone. Vous devez utiliser des points de terminaison connus et définir le protocole de transport [ncadg \_ MQ](/windows/desktop/Midl/ncadg-mq). Dans votre fichier IDL, appliquez l’attribut [message](/windows/desktop/Midl/message) aux fonctions qui utilisent Message Queuing asynchrone. Notez que les fonctions de message ne peuvent avoir que \[ des \] paramètres in.

 

 