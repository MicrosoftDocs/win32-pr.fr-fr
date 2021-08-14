---
title: Fournisseurs de sécurité
description: L’interface SSPI (Security Support Provider Interface) assure la prise en charge de l’authentification mutuelle et est exposée directement via les API et les services SSPI en couche sur SSPI, y compris RPC.
ms.assetid: 3aa64aa1-c707-489f-a0a3-08bf6ac151ec
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3685ad95b5e339853be947170bb0a8681a376d8d2f34368534d02b3b0cbdf4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118183654"
---
# <a name="security-providers"></a>Fournisseurs de sécurité

L’interface SSPI (Security Support Provider Interface) assure la prise en charge de l’authentification mutuelle et est exposée directement via les API et les services SSPI en couche sur SSPI, y compris RPC.

Tous les packages de sécurité disponibles pour SSPI ne prennent pas en charge l’authentification mutuelle. Pour obtenir une authentification mutuelle, l’application doit demander une authentification mutuelle et un package de sécurité qui la prend en charge. par exemple, l’exemple de code dans [l’authentification mutuelle dans un Service Windows sockets avec SCP](mutual-authentication-in-a-windows-sockets-service-with-an-scp.md) utilise le package « negotiate » dans Secur32.dll, qui est inclus avec Windows 2000.

 

 




