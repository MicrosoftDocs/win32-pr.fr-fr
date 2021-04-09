---
title: Fournisseurs de sécurité
description: L’interface SSPI (Security Support Provider Interface) assure la prise en charge de l’authentification mutuelle et est exposée directement via les API et les services SSPI en couche sur SSPI, y compris RPC.
ms.assetid: 3aa64aa1-c707-489f-a0a3-08bf6ac151ec
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcf033550c2a2da66b7eab05f23289ba988690e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028590"
---
# <a name="security-providers"></a><span data-ttu-id="fd501-103">Fournisseurs de sécurité</span><span class="sxs-lookup"><span data-stu-id="fd501-103">Security Providers</span></span>

<span data-ttu-id="fd501-104">L’interface SSPI (Security Support Provider Interface) assure la prise en charge de l’authentification mutuelle et est exposée directement via les API et les services SSPI en couche sur SSPI, y compris RPC.</span><span class="sxs-lookup"><span data-stu-id="fd501-104">The Security Support Provider Interface (SSPI) provides support for mutual authentication and is exposed directly through the SSPI APIs and services layered on SSPI, including RPC.</span></span>

<span data-ttu-id="fd501-105">Tous les packages de sécurité disponibles pour SSPI ne prennent pas en charge l’authentification mutuelle.</span><span class="sxs-lookup"><span data-stu-id="fd501-105">Not all security packages available to SSPI support mutual authentication.</span></span> <span data-ttu-id="fd501-106">Pour obtenir une authentification mutuelle, l’application doit demander une authentification mutuelle et un package de sécurité qui la prend en charge.</span><span class="sxs-lookup"><span data-stu-id="fd501-106">To obtain mutual authentication, the application must request mutual authentication and a security package that supports it.</span></span> <span data-ttu-id="fd501-107">Par exemple, l’exemple de code dans [l’authentification mutuelle dans un service Windows Sockets avec un SCP](mutual-authentication-in-a-windows-sockets-service-with-an-scp.md) utilise le package « Negotiate » dans Secur32.dll, qui est inclus dans Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="fd501-107">For example, the code example in [Mutual Authentication in a Windows Sockets Service with an SCP](mutual-authentication-in-a-windows-sockets-service-with-an-scp.md) uses the "negotiate" package in Secur32.dll, which is included with Windows 2000.</span></span>

 

 




