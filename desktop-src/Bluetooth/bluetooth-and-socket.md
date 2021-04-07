---
title: Bluetooth et Socket
description: Crée un socket pour les connexions entrantes ou sortantes.
ms.assetid: 21b9cf1f-1a85-4a4b-9557-faa4f32c3696
keywords:
- Bluetooth Bluetooth
- Bluetooth Socket
- Bluetooth et Bluetooth Socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c2c2085ee0c61941bab93ed25dd86f5c102d0d0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727652"
---
# <a name="bluetooth-and-socket"></a>Bluetooth et Socket

La fonction [**Socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) crée un socket pour les connexions entrantes ou sortantes. :

Pour créer un socket à l’aide de Bluetooth, utilisez les paramètres suivants :

-   Le paramètre *AF* de la fonction [**Socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) est toujours défini sur **AF \_ BTH** pour les sockets Bluetooth.
-   Le paramètre de *type* de la fonction de [**Socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) est toujours un **\_ flux de chaussette**; **Chaussette \_** Les sockets DGRAM ne sont pas pris en charge par Bluetooth.
-   Pour le paramètre de *protocole* , **BTHPROTO \_ RFCOMM** est le protocole pris en charge.

Pour plus d’informations, consultez [Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**socle**](/windows/desktop/api/winsock2/nf-winsock2-socket)
</dt> </dl>

 

 