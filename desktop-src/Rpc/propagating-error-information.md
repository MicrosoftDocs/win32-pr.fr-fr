---
title: Propagation des informations d’erreur
description: La propagation des informations d’erreur étendues autorise les serveurs qui reçoivent une \_ erreur RPC S \_ \, ou tout autre code d’erreur, à permettre au runtime RPC de propager les informations qu’il a reçues à ses appelants.
ms.assetid: f0395f19-ceb1-4249-892e-9b688464d0d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd20575cee304c0a1693ae4bc6442de4837caa0d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311481"
---
# <a name="propagating-error-information"></a>Propagation des informations d’erreur

La propagation des informations d’erreur étendues autorise les serveurs qui reçoivent une \_ erreur RPC S \_ \* ou tout autre code d’erreur à permettre au runtime RPC de propager les informations qu’il a reçues à ses appelants. Tout le serveur doit faire appel à [**RpcRaiseException**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) ou [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall) lors de la rencontre d’une erreur irrécupérable. Le temps d’exécution RPC prend en charge le chaînage des informations d’erreur étendues, le cas échéant, provoquant l’erreur irrécupérable pour signaler l’erreur irrécupérable, tant que le code d’erreur donné à **RpcRaiseException** ou **RpcAsyncAbortCall** est le même que le code d’erreur à l’origine de l’erreur irrécupérable.

 

 




