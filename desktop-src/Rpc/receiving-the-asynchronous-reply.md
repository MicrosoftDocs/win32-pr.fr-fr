---
title: Réception de la réponse asynchrone
description: Une fois que le serveur a envoyé une réponse, le client appelle RpcAsyncCompleteCall avec le handle asynchrone afin qu’il puisse recevoir la réponse.
ms.assetid: 48fb3777-d90a-474b-a1fa-9d034b5791e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9143daaf1f276f784086e2ec17efb47dfd1fb6e4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311454"
---
# <a name="receiving-the-asynchronous-reply"></a>Réception de la réponse asynchrone

Une fois que le serveur a envoyé une réponse, le client appelle [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) avec le handle asynchrone afin qu’il puisse recevoir la réponse. Lorsque **RpcAsyncCompleteCall** s’est terminé avec succès, le paramètre *reply* pointe vers une mémoire tampon qui contient la valeur de retour de la fonction distante. Toutes les mémoires tampons fournies par le programme client comme des \[ [](/windows/desktop/Midl/out-idl) \] paramètres out ou \[ [**in**](/windows/desktop/Midl/in), **out** \] à la fonction distante asynchrone contiennent des données valides. Si le client appelle **RpcAsyncCompleteCall** avant que le serveur n’ait envoyé la réponse, cet appel échoue et retourne la valeur RPC \_ S \_ Async \_ Call \_ en attente.

Si votre programme client utilise des ports de terminaison d’e/s ou des événements pour la notification, il doit appeler [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) pour libérer le port ou le descripteur lorsqu’il n’en a plus besoin.

 

 