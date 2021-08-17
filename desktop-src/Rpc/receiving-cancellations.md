---
title: Réception des annulations
description: L’application serveur peut appeler RpcServerTestCancel avec le handle de liaison de l’appel en question pour déterminer si le client a demandé l’annulation de l’appel asynchrone. Elle retourne RPC \_ S \_ OK si le client a annulé l’appel.
ms.assetid: ac7d7a50-a788-40a9-b57d-1f528bdbd7df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1757c2cac82b672504fc5aed5fe55a06d973a247c76d42e6f2a9debf1837d598
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927117"
---
# <a name="receiving-cancellations"></a>Réception des annulations

L’application serveur peut appeler [**RpcServerTestCancel**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcservertestcancel) avec le handle de liaison de l’appel en question pour déterminer si le client a demandé l’annulation de l’appel asynchrone. Elle retourne RPC \_ S \_ OK si le client a annulé l’appel.

 

 




