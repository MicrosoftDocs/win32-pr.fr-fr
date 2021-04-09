---
description: L’installation des classes de service, l’inscription des instances de service et des opérations de requête de base sont toutes mappées relativement directement de l’API au SPI.
ms.assetid: 2ae937f6-e0a6-4a02-9838-0a42575bae66
title: Mappage de la résolution de noms entre les fonctions API et SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a031ea8af72bb2733fc647c817a850ab7f311b1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862557"
---
# <a name="name-resolution-mapping-between-api-and-spi-functions"></a>Mappage de la résolution de noms entre les fonctions API et SPI

L’installation des classes de service, l’inscription des instances de service et des opérations de requête de base sont toutes mappées relativement directement de l’API au SPI. La fonction [**WSAGetServiceClassNameByClassId**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida) n’a pas de fonction correspondante dans l’index SPI, car cette fonction est implémentée dans Ws2 \_32.dll en effectuant un appel à [**NSPGetServiceClassInfo**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo).

Les fonctions d’assistance [**WSAAddressToString**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaddresstostringa) et [**WSAStringToAddress n'**](/windows/desktop/api/Winsock2/nf-winsock2-wsastringtoaddressa) sont mappées aux fonctions correspondantes dans l’API de transport, car seul un fournisseur de transport sait nécessairement comment effectuer la traduction sur une structure [**sockaddr**](sockaddr-2.md) .

 

 



