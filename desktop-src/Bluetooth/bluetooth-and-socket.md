---
title: Bluetooth et socket
description: Crée un socket pour les connexions entrantes ou sortantes.
ms.assetid: 21b9cf1f-1a85-4a4b-9557-faa4f32c3696
keywords:
- Bluetooth Bluetooth
- Bluetooth de socket
- Bluetooth et socket Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c2c2085ee0c61941bab93ed25dd86f5c102d0d0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127122046"
---
# <a name="bluetooth-and-socket"></a>Bluetooth et socket

La fonction [**Socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) crée un socket pour les connexions entrantes ou sortantes. :

pour créer un socket à l’aide de Bluetooth, utilisez les paramètres suivants :

-   le paramètre *af* de la fonction [**socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) est toujours défini sur **af \_ BTH** pour Bluetooth sockets.
-   Le paramètre de *type* de la fonction de [**Socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) est toujours un **\_ flux de chaussette**; **Chaussette \_** Les sockets DGRAM ne sont pas pris en charge par Bluetooth.
-   Pour le paramètre de *protocole* , **BTHPROTO \_ RFCOMM** est le protocole pris en charge.

pour plus d’informations, consultez [Windows sockets](/windows/desktop/WinSock/windows-sockets-start-page-2).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**socle**](/windows/desktop/api/winsock2/nf-winsock2-socket)
</dt> </dl>

 

 