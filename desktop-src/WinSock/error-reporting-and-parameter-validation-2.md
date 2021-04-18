---
description: Le schéma de rapport d’erreurs diffère entre les interfaces SPI et API.
ms.assetid: f4a4b406-3e3a-444f-b75a-0cf51bded1bc
title: Rapport d’erreurs et validation des paramètres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 291fa2ed950d916be39b1a696f5fe8ad6f07280c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519300"
---
# <a name="error-reporting-and-parameter-validation"></a>Rapport d’erreurs et validation des paramètres

Le schéma de rapport d’erreurs diffère entre les interfaces SPI et API. Les fournisseurs de services Windows Sockets signalent des erreurs, ainsi que la fonction qui retourne, par opposition à l’approche basée sur les threads utilisée dans l’API. Le \_32.dll Ws2 utilise le code d’erreur par fonction du fournisseur de services pour mettre à jour la valeur d’erreur par thread obtenue via la fonction de l’API [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) . Toutefois, les fournisseurs de services sont toujours requis pour maintenir l’erreur basée sur socket qui peut être récupérée à l’aide de l' \_ option de socket par erreur.

Le \_32.dll Ws2 effectue une validation de paramètre uniquement sur les appels de fonction qui sont entièrement implémentés dans lui-même. Les fournisseurs de services sont responsables de l’exécution de toute leur propre validation de paramètre.

 

 



