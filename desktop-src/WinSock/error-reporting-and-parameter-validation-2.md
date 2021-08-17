---
description: Le schéma de rapport d’erreurs diffère entre les interfaces SPI et API.
ms.assetid: f4a4b406-3e3a-444f-b75a-0cf51bded1bc
title: Rapport d’erreurs et validation des paramètres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5fdec1ee6a4cd7d052ba9f94cdf62ce7de70969a521a7023a5ca41e37f6a931
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132612"
---
# <a name="error-reporting-and-parameter-validation"></a>Rapport d’erreurs et validation des paramètres

Le schéma de rapport d’erreurs diffère entre les interfaces SPI et API. Windows Les fournisseurs de services de sockets signalent des erreurs, ainsi que la fonction qui retourne, par opposition à l’approche basée sur les threads utilisée dans l’API. Le \_32.dll Ws2 utilise le code d’erreur par fonction du fournisseur de services pour mettre à jour la valeur d’erreur par thread obtenue via la fonction de l’API [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) . Toutefois, les fournisseurs de services sont toujours requis pour maintenir l’erreur basée sur socket qui peut être récupérée à l’aide de l' \_ option de socket par erreur.

Le \_32.dll Ws2 effectue une validation de paramètre uniquement sur les appels de fonction qui sont entièrement implémentés dans lui-même. Les fournisseurs de services sont responsables de l’exécution de toute leur propre validation de paramètre.

 

 



