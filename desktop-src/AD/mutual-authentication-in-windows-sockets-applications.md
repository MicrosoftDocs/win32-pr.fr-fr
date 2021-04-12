---
title: Authentification mutuelle dans les applications Windows Sockets
description: Les services Microsoft Windows Sockets peuvent utiliser les API d’inscription et de résolution (RnR) pour publier des services, ou ils peuvent utiliser des points de connexion de service.
ms.assetid: 2b73a754-4f16-41a2-8441-a4ee5f80035c
ms.tgt_platform: multiple
keywords:
- Authentification mutuelle dans les applications Windows Sockets
- Active Directory, utilisation, authentification mutuelle, dans les applications Windows Sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29062fa5c9fa7b9b003f1c3aa6f8bc384a785f83
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104190753"
---
# <a name="mutual-authentication-in-windows-sockets-applications"></a><span data-ttu-id="da8d5-105">Authentification mutuelle dans les applications Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="da8d5-105">Mutual Authentication in Windows Sockets Applications</span></span>

<span data-ttu-id="da8d5-106">Les services Microsoft Windows Sockets peuvent utiliser les API d’inscription et de résolution (RnR) pour publier des services, ou ils peuvent utiliser des points de connexion de service.</span><span class="sxs-lookup"><span data-stu-id="da8d5-106">Microsoft Windows Sockets services can use the Registration and Resolution (RnR) APIs to publish services, or they can use service connection points.</span></span>

<span data-ttu-id="da8d5-107">Pour plus d’informations et pour obtenir un exemple de code qui montre comment effectuer une authentification mutuelle pour un service Windows Sockets qui publie à l’aide d’un point de connexion de service, consultez [authentification mutuelle dans un service Windows Sockets avec SCP](mutual-authentication-in-a-windows-sockets-service-with-an-scp.md).</span><span class="sxs-lookup"><span data-stu-id="da8d5-107">For more information and a code example that shows how to perform mutual authentication for a Windows Sockets service that publishes using a service connection point, see [Mutual Authentication in a Windows Sockets Service with an SCP](mutual-authentication-in-a-windows-sockets-service-with-an-scp.md).</span></span> <span data-ttu-id="da8d5-108">Cet exemple de code utilise un package de sécurité SSPI pour gérer les négociations d’authentification entre un client et le service WinSock.</span><span class="sxs-lookup"><span data-stu-id="da8d5-108">This code example uses an SSPI security package to manage the authentication negotiations between a client and the WinSock service.</span></span>

<span data-ttu-id="da8d5-109">Un service WinSock RnR peut utiliser un code similaire pour effectuer une authentification mutuelle à l’aide d’un package SSPI.</span><span class="sxs-lookup"><span data-stu-id="da8d5-109">A WinSock RnR service can use similar code to perform mutual authentication using an SSPI package.</span></span> <span data-ttu-id="da8d5-110">Dans ce cas, le service compose ses SPN à l’aide du nom unique de l’entrée du service dans le conteneur WinsockServices dans le répertoire.</span><span class="sxs-lookup"><span data-stu-id="da8d5-110">In this case, the service would compose its SPNs using the distinguished name of the service's entry in the WinsockServices container in the directory.</span></span>

<span data-ttu-id="da8d5-111">Par exemple, si le service s’inscrit lui-même avec le nom « WinSockRnRSampleService », vous devez composer le SPN du service à partir du nom unique suivant :</span><span class="sxs-lookup"><span data-stu-id="da8d5-111">For example, if the service registers itself with the name "WinSockRnRSampleService", you would compose the service's SPN from the following distinguished name:</span></span>


```C++
cn=WinSockRnRSampleService,cn=WinsockServices,cn=System,<domain DN>
```



 

 




