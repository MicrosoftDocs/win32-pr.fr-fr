---
description: L’installation des classes de service, l’inscription des instances de service et des opérations de requête de base sont toutes mappées relativement directement de l’API au SPI.
ms.assetid: 2ae937f6-e0a6-4a02-9838-0a42575bae66
title: Mappage de la résolution de noms entre les fonctions API et SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad02896ea15fb1b7c7e2aa2e01d9ec0727492da43d0446819dd1f2e04ad591d2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733623"
---
# <a name="name-resolution-mapping-between-api-and-spi-functions"></a>Mappage de la résolution de noms entre les fonctions API et SPI

L’installation des classes de service, l’inscription des instances de service et des opérations de requête de base sont toutes mappées relativement directement de l’API au SPI. La fonction [**WSAGetServiceClassNameByClassId**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida) n’a pas de fonction correspondante dans l’index SPI, car cette fonction est implémentée dans Ws2 \_32.dll en effectuant un appel à [**NSPGetServiceClassInfo**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo).

Les fonctions d’assistance [**WSAAddressToString**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaddresstostringa) et [**WSAStringToAddress n'**](/windows/desktop/api/Winsock2/nf-winsock2-wsastringtoaddressa) sont mappées aux fonctions correspondantes dans l’API de transport, car seul un fournisseur de transport sait nécessairement comment effectuer la traduction sur une structure [**sockaddr**](sockaddr-2.md) .

 

 



