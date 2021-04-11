---
title: Bluetooth et setsockopt
description: Bluetooth utilise la fonction Setsockopt pour définir différents paramètres associés au canal du serveur ou à la connexion.
ms.assetid: ab78baed-5556-4d7b-88a6-e3ceb93afa8c
keywords:
- Bluetooth
- setsockopt
- Bluetooth et setsockopt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 943839a49788b76e597596aee9cba65fa4b8d30d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315342"
---
# <a name="bluetooth-and-setsockopt"></a>Bluetooth et setsockopt

Bluetooth utilise la fonction [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) pour définir différents paramètres associés au canal du serveur ou à la connexion. L’utilisation de **setsockopt** avec Bluetooth présente les exigences suivantes :

-   Le paramètre *s* de [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) doit être un Socket Bluetooth valide.
-   Le paramètre de *niveau* de [**SETSOCKOPT**](/windows/desktop/api/winsock/nf-winsock-setsockopt) doit être sol \_ RFCOMM.

Pour obtenir la liste des options de Socket Bluetooth disponibles, consultez [options de socket et Bluetooth](bluetooth-and-socket-options.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> </dl>

 

 