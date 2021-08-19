---
title: authentification mutuelle dans des Applications Windows sockets
description: les services de sockets Microsoft Windows peuvent utiliser les api d’inscription et de résolution (RnR) pour publier des services, ou ils peuvent utiliser des points de connexion de service.
ms.assetid: 2b73a754-4f16-41a2-8441-a4ee5f80035c
ms.tgt_platform: multiple
keywords:
- authentification mutuelle dans des Applications Windows sockets
- Active Directory, utilisation, authentification mutuelle, dans les applications Windows sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96a7267159f826d572a8efd101ab86338f5a24c6966b8d2af3a260e1f4af6244
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025747"
---
# <a name="mutual-authentication-in-windows-sockets-applications"></a>authentification mutuelle dans des Applications Windows sockets

les services de sockets Microsoft Windows peuvent utiliser les api d’inscription et de résolution (RnR) pour publier des services, ou ils peuvent utiliser des points de connexion de service.

pour plus d’informations et pour obtenir un exemple de code qui montre comment effectuer une authentification mutuelle pour un service de sockets Windows qui publie à l’aide d’un point de connexion de service, consultez [authentification mutuelle dans un service de sockets Windows avec SCP](mutual-authentication-in-a-windows-sockets-service-with-an-scp.md). Cet exemple de code utilise un package de sécurité SSPI pour gérer les négociations d’authentification entre un client et le service WinSock.

Un service WinSock RnR peut utiliser un code similaire pour effectuer une authentification mutuelle à l’aide d’un package SSPI. Dans ce cas, le service compose ses SPN à l’aide du nom unique de l’entrée du service dans le conteneur WinsockServices dans le répertoire.

Par exemple, si le service s’inscrit lui-même avec le nom « WinSockRnRSampleService », vous devez composer le SPN du service à partir du nom unique suivant :


```C++
cn=WinSockRnRSampleService,cn=WinsockServices,cn=System,<domain DN>
```



 

 




