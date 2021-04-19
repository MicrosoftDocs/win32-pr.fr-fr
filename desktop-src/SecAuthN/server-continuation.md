---
description: En fonction du code de retour d’un appel précédent à AcceptSecurityContext (général), le serveur peut attendre une réponse du client et peut participer à des échanges supplémentaires avec le client.
ms.assetid: 281e1f81-3524-4034-bee5-cef6b13cf402
title: Continuation du serveur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22fba8a60bea12daae0e6aaf93fed55fead5738c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534245"
---
# <a name="server-continuation"></a><span data-ttu-id="d0ae6-103">Continuation du serveur</span><span class="sxs-lookup"><span data-stu-id="d0ae6-103">Server Continuation</span></span>

<span data-ttu-id="d0ae6-104">En fonction du code de retour d’un appel précédent à [**AcceptSecurityContext (général)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext), le serveur peut attendre une réponse du client et peut participer à des échanges supplémentaires avec le client.</span><span class="sxs-lookup"><span data-stu-id="d0ae6-104">Based on the return code from a previous call to [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext), the server can wait for a response from the client and can participate in additional exchanges with the client.</span></span> <span data-ttu-id="d0ae6-105">Pour continuer le protocole d’authentification, le serveur répète les appels à **AcceptSecurityContext (général)**.</span><span class="sxs-lookup"><span data-stu-id="d0ae6-105">To continue the authentication protocol, the server repeats calls to **AcceptSecurityContext (General)**.</span></span>

<span data-ttu-id="d0ae6-106">L’état retourné par [**AcceptSecurityContext (général)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) est vérifié pour déterminer si le serveur doit attendre des messages supplémentaires du client.</span><span class="sxs-lookup"><span data-stu-id="d0ae6-106">The status returned by [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) is checked to see if the server needs to wait for additional messages from the client.</span></span> <span data-ttu-id="d0ae6-107">Dans la plupart des protocoles d’authentification, il existe un nombre maximal d’échanges même pour l’authentification mutuelle.</span><span class="sxs-lookup"><span data-stu-id="d0ae6-107">In most authentication protocols, there is a maximum number of exchanges even for mutual authentication.</span></span> <span data-ttu-id="d0ae6-108">À l’heure actuelle, les [*protocoles*](../secgloss/k-gly.md) NTLM et Kerberos effectuent une authentification mutuelle avec trois échanges.</span><span class="sxs-lookup"><span data-stu-id="d0ae6-108">Currently, both the NTLM and [*Kerberos protocols*](../secgloss/k-gly.md) do mutual authentication with three exchanges.</span></span>

 

 
