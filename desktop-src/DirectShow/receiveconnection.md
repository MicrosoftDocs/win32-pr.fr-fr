---
description: ReceiveConnection
ms.assetid: 90a6a09a-95e1-4adf-8e0b-269f971aaa67
title: ReceiveConnection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55a8a91cbf9870d6c53592ff823f710eb5875fa939592309425df0a0bca6f0e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072763"
---
# <a name="receiveconnection"></a>ReceiveConnection

Ce mécanisme permet à une broche de sortie de proposer une modification de format à son homologue en aval, lorsque le nouveau format requiert une mémoire tampon plus grande. La broche de sortie effectue les opérations suivantes :

1.  Appelle [**IPIN :: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) sur la broche d’entrée en aval.
2.  Si `ReceiveConnection` elle est réussie, appelle [**IMemInputPin :: NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) sur la broche d’entrée.

En outre, la broche de sortie devra peut-être appeler [**IMemAllocator :: SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) , puis dévalider et revalider l’allocateur afin de modifier les tailles de mémoire tampon. Veillez à remettre tous les échantillons en attente dans l’ancien format avant de modifier la taille de la mémoire tampon.

Certains décodeurs MPEG-2 utilisent ce mécanisme pour basculer entre la sortie MPEG-1 et MPEG-2, ou si la taille de la vidéo change.

 

 



