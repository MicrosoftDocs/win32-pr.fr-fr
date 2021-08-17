---
description: installation du Service dans le SPI de Windows sockets 2 (Winsock).
ms.assetid: a303fbcf-9122-422a-9b12-d00a5df0fc0f
title: Installation du Service dans le SPI Windows sockets 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faad2431add9b20ebd3358c48469f382596b658de1339525b147b094a7c3786c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740523"
---
# <a name="service-installation-in-the-windows-sockets-2-spi"></a>Installation du Service dans le SPI Windows sockets 2

-   [**NSPInstallServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspinstallserviceclass)
-   [**NSPRemoveServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspremoveserviceclass)
-   [**NSPSetService**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspsetservice)

Quand la classe de service requise n’existe pas encore, un client SPI d’espace de noms utilise [**NSPInstallServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspinstallserviceclass) pour installer une nouvelle classe de service en fournissant un nom de classe de service, un GUID pour l’identificateur de classe de service et une série de structures [**WSANSCLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) . Ces structures sont spécifiques à un espace de noms particulier et fournissent des valeurs communes telles que des numéros de port TCP recommandés ou des identificateurs SAP SAP. Une classe de service peut être supprimée en appelant [**NSPRemoveServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspremoveserviceclass) et en fournissant le GUID correspondant à l’identificateur de classe.

Une fois qu’une classe de service existe, des instances spécifiques d’un service peuvent être installées ou supprimées via [**NSPSetService**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspsetservice). Cette fonction prend une structure [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) comme paramètre d’entrée avec un code d’opération et des indicateurs d’opération. Le code d’opération indique si le service est en cours d’installation ou de suppression. La structure **WSAQUERYSET** fournit toutes les informations pertinentes relatives au service, notamment l’identificateur de classe de service, le nom de service (pour cette instance), l’identificateur d’espace de noms applicable et les informations de protocole, ainsi qu’un ensemble d’adresses de transport vers lequel le service écoute.

 

 



