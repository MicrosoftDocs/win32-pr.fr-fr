---
title: Bluetooth et getsockopt
description: Bluetooth utilise la fonction getsockopt pour interroger différents paramètres associés au canal du serveur ou à la connexion.
ms.assetid: 9593fd6c-b55d-45d8-a9d9-87ebcd09d1bd
keywords:
- Bluetooth
- getsockopt
- Bluetooth et getsockopt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dede19b27eea39b7d1e778b3e92312a5e148c0ec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728364"
---
# <a name="bluetooth-and-getsockopt"></a>Bluetooth et getsockopt

Bluetooth utilise la fonction [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) pour interroger différents paramètres associés au canal du serveur ou à la connexion. L’utilisation de **getsockopt** avec Bluetooth présente les exigences suivantes :

-   Le paramètre *s* de [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) doit être un Socket Bluetooth valide.
-   Le paramètre de *niveau* de [**GETSOCKOPT**](/windows/desktop/api/winsock/nf-winsock-getsockopt) doit être sol \_ RFCOMM.

Pour obtenir la liste des options de Socket Bluetooth disponibles, consultez [options de socket et Bluetooth](bluetooth-and-socket-options.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> </dl>

 

 