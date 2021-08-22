---
title: Déchargement d’un serveur avec des handles de contexte en attente
description: Traditionnellement, le déchargement d’une DLL qui traite les appels RPC à l’aide de handles de contexte, sans arrêter au préalable le processus d’hébergement, a été problématique.
ms.assetid: d3880578-e542-418c-803a-fd00d0bfde7f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e581ff142c7453f4a9e9f1e40a5ab9991257a350a84b2fcb2ea08a0e157288cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010947"
---
# <a name="unloading-a-server-with-outstanding-context-handles"></a>Déchargement d’un serveur avec des handles de contexte en attente

Traditionnellement, le déchargement d’une DLL qui traite les appels RPC à l’aide de handles de contexte, sans arrêter au préalable le processus d’hébergement, a été problématique. Cela est dû au fait que la routine d’exécution n’est plus valide lorsque la DLL est déchargée. Lorsqu’un client avec un handle de contexte précédemment ouvert échoue et que l’exécution de l’appel de procédure distante tente de fermer le descripteur de contexte, sa tentative d’appeler l’accès à la routine d’exécution ne respecte pas et le serveur tombe en panne.

à partir de Windows XP, une nouvelle API appelée [**RpcServerUnregisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterifex) a été ajoutée. **RpcServerUnregisterIfEx** ferme les descripteurs de contexte ouverts par l’interface en cours d’annulation d’inscription ; la fonction [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) ne le fait pas. L’utilisation de **RpcServerUnregisterIfEx** n’est pas nécessaire lorsque l’ensemble du processus s’arrête, mais il est nécessaire si une ou plusieurs dll hébergeant les routines d’exécution sont déchargées alors que des handles de contexte en attente existent.

 

 




