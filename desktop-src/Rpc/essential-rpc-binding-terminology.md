---
title: Terminologie des liaisons RPC essentielles
description: Pour mieux vous aider dans une discussion sur le processus de connexion client/serveur, il est utile de connaître les termes suivants.
ms.assetid: 05aca325-87ee-4581-9152-a8a2ff7fb490
keywords:
- Appel de procédure distante RPC, description, liaison
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a08b0741b27360fe81c2ed713ee39189ef043073c03bc7e12d53165f8a09146c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021438"
---
# <a name="essential-rpc-binding-terminology"></a>Terminologie des liaisons RPC essentielles

Pour mieux vous aider dans une discussion sur le processus de connexion client/serveur, il est utile de connaître les termes suivants.

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="Protocol_Sequence"></span><span id="protocol_sequence"></span><span id="PROTOCOL_SEQUENCE"></span>Séquence de protocole
</dt> <dd>

Lorsque les systèmes d’exploitation réseau communiquent entre eux, ils doivent écouter et prononcer la même langue. Ces langages sont appelés *séquences de protocole*. Les programmes client et serveur doivent utiliser des séquences de protocole que le réseau qui les connecte prend en charge. Microsoft RPC prend en charge différentes séquences de protocole. Pour plus d’informations, consultez [sélection d’une séquence de protocole](selecting-a-protocol-sequence.md), [spécification de séquences de protocole](specifying-protocol-sequences.md)et [**point de terminaison**](/windows/desktop/Midl/endpoint).

</dd> <dt>

<span id="Server_Host_Computer_or_Server_Host_System"></span><span id="server_host_computer_or_server_host_system"></span><span id="SERVER_HOST_COMPUTER_OR_SERVER_HOST_SYSTEM"></span>Ordinateur hôte serveur ou système hôte serveur
</dt> <dd>

Le programme serveur s’exécute sur l’ordinateur hôte du serveur. Toutefois, une grande partie de la documentation sur l’informatique client/serveur fait référence au programme serveur et à l’ordinateur hôte du serveur en tant que « serveur ». Le résultat est qu’il n’est pas toujours évident de savoir ce qui est abordé.

</dd> <dt>

<span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Poste
</dt> <dd>

Les programmes serveur écoutent un port ou un groupe de ports sur l’ordinateur hôte du serveur pour les demandes des clients. Les systèmes hôtes de serveur maintiennent une base de données de ces ports, appelés points de terminaison dans RPC. La base de données est appelée mappage de point de terminaison.

</dd> <dt>

<span id="Binding"></span><span id="binding"></span><span id="BINDING"></span>Liant
</dt> <dd>

Les programmes clients créent une liaison avec le serveur pour établir une session de communication. Une liaison contient toutes les informations dont l’application cliente a besoin pour créer la session.

</dd> </dl>

 

 