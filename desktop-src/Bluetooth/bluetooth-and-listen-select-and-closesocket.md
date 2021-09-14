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
ms.openlocfilehash: e442cfc0593ab5be297902487c7c3ccdf056b4e0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127296958"
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

 

 