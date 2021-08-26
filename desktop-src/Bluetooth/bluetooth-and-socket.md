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
ms.openlocfilehash: 5afaf61e307ce8d5001c2ba5402607b63b1ad6d19317aee044d7a2cac31259b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004299"
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

 

 