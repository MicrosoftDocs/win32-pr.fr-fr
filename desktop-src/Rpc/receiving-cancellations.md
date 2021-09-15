---
title: Réception des annulations
description: L’application serveur peut appeler RpcServerTestCancel avec le handle de liaison de l’appel en question pour déterminer si le client a demandé l’annulation de l’appel asynchrone. Elle retourne RPC \_ S \_ OK si le client a annulé l’appel.
ms.assetid: ac7d7a50-a788-40a9-b57d-1f528bdbd7df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50b8b48ef2796dab071ac705edf0ffca5156e235
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311458"
---
# <a name="receiving-cancellations"></a>Réception des annulations

L’application serveur peut appeler [**RpcServerTestCancel**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcservertestcancel) avec le handle de liaison de l’appel en question pour déterminer si le client a demandé l’annulation de l’appel asynchrone. Elle retourne RPC \_ S \_ OK si le client a annulé l’appel.

 

 




