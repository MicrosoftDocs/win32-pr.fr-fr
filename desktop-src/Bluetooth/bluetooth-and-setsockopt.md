---
title: Bluetooth et setsockopt
description: Bluetooth utilise la fonction setsockopt pour définir différents paramètres associés au canal du serveur ou à la connexion.
ms.assetid: ab78baed-5556-4d7b-88a6-e3ceb93afa8c
keywords:
- Bluetooth
- setsockopt
- Bluetooth et setsockopt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70aef0914e13888f3bcb48bed5c7c90cd2585a5d22d60c27a35af605657f20c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004439"
---
# <a name="bluetooth-and-setsockopt"></a>Bluetooth et setsockopt

Bluetooth utilise la fonction [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) pour définir différents paramètres associés au canal du serveur ou à la connexion. l’utilisation de **setsockopt** avec Bluetooth présente les exigences suivantes :

-   le paramètre *s* de [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) doit être un socket Bluetooth valide.
-   Le paramètre de *niveau* de [**SETSOCKOPT**](/windows/desktop/api/winsock/nf-winsock-setsockopt) doit être sol \_ RFCOMM.

pour obtenir la liste des options de socket Bluetooth disponibles, consultez options de sockets [et de Bluetooth](bluetooth-and-socket-options.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> </dl>

 

 