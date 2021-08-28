---
title: Bluetooth et écouter, sélectionner et opération closesocket
description: Bluetooth utilise les fonctions listen, select et opération closesocket sans aucune modification de la programmation standard Windows sockets.
ms.assetid: b64440de-bc63-4e3b-bfd9-5cf783f36c23
keywords:
- Bluetooth
- opération closesocket
- listen
- select
- Bluetooth et écouter
- Bluetooth et écouter, sélectionnez
- Bluetooth et écouter, sélectionner et opération closesocket
- listen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01fa3fc1285a9035173da80cc7a9821535409b872b171f7822708c379ff01543
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004479"
---
# <a name="bluetooth-and-listen-select-and-closesocket"></a>Bluetooth et écouter, sélectionner et opération closesocket

Bluetooth utilise les fonctions [**listen**](/windows/desktop/api/winsock2/nf-winsock2-listen), [**select**](/windows/desktop/api/winsock2/nf-winsock2-select)et [**opération closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) sans aucune modification de la programmation standard Windows sockets.

comme avec Windows sockets, la fonction [**opération closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) libère les ressources associées au socket.

Lors de l’appel de la fonction [**Listen**](/windows/desktop/api/winsock2/nf-winsock2-listen) , il est fortement recommandé d’utiliser une valeur basse pour le paramètre *backlog* (généralement 2 à 4), car seules quelques connexions client sont acceptées. Cela réduit les ressources système allouées pour une utilisation par le socket d’écoute.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**opération closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket)
</dt> <dt>

[**listen**](/windows/desktop/api/winsock2/nf-winsock2-listen)
</dt> <dt>

[**sélectionné**](/windows/desktop/api/winsock2/nf-winsock2-select)
</dt> </dl>

 

 