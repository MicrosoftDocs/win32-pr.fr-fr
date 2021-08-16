---
title: Propagation des informations d’erreur
description: La propagation des informations d’erreur étendues autorise les serveurs qui reçoivent une \_ erreur RPC S \_ \, ou tout autre code d’erreur, à permettre au runtime RPC de propager les informations qu’il a reçues à ses appelants.
ms.assetid: f0395f19-ceb1-4249-892e-9b688464d0d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 510ecf011dbac01d2b4c931a463bebb3739a92322059eb3a7a342160c42a9e4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927157"
---
# <a name="propagating-error-information"></a>Propagation des informations d’erreur

La propagation des informations d’erreur étendues autorise les serveurs qui reçoivent une \_ erreur RPC S \_ \* ou tout autre code d’erreur à permettre au runtime RPC de propager les informations qu’il a reçues à ses appelants. Tout le serveur doit faire appel à [**RpcRaiseException**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) ou [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall) lors de la rencontre d’une erreur irrécupérable. Le temps d’exécution RPC prend en charge le chaînage des informations d’erreur étendues, le cas échéant, provoquant l’erreur irrécupérable pour signaler l’erreur irrécupérable, tant que le code d’erreur donné à **RpcRaiseException** ou **RpcAsyncAbortCall** est le même que le code d’erreur à l’origine de l’erreur irrécupérable.

 

 




