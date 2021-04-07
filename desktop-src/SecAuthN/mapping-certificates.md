---
description: Mappage des certificats
ms.assetid: 4139f927-54f4-4968-a9eb-020401bb536d
title: Mappage des certificats
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 397a9ef8822d4f191ae37cdb998166fa54c2b12d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758259"
---
# <a name="mapping-certificates"></a><span data-ttu-id="9f568-103">Mappage des certificats</span><span class="sxs-lookup"><span data-stu-id="9f568-103">Mapping Certificates</span></span>

> [!Note]  
> <span data-ttu-id="9f568-104">Les informations contenues dans cette rubrique ne sont valides que pour les serveurs qui requièrent l’authentification du client.</span><span class="sxs-lookup"><span data-stu-id="9f568-104">The information in this topic is valid only for servers that require client authentication.</span></span>

 

<span data-ttu-id="9f568-105">Lorsqu’une application serveur requiert l’authentification du client, Schannel tente automatiquement de mapper le certificat fourni par le client à un compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9f568-105">When a server application requires client authentication, Schannel automatically attempts to map the certificate supplied by the client to a user account.</span></span>

<span data-ttu-id="9f568-106">Une fois [*le contexte de sécurité*](../secgloss/s-gly.md) établi, l’application serveur peut utiliser la fonction [**QuerySecurityContextToken**](/windows/desktop/api/Sspi/nf-sspi-querysecuritycontexttoken) pour obtenir un [*jeton d’accès*](../secgloss/a-gly.md) pour le compte d’utilisateur auquel le [*certificat client*](../secgloss/c-gly.md) a été mappé.</span><span class="sxs-lookup"><span data-stu-id="9f568-106">After the [*security context*](../secgloss/s-gly.md) has been established, the server application can use the [**QuerySecurityContextToken**](/windows/desktop/api/Sspi/nf-sspi-querysecuritycontexttoken) function to obtain an [*access token*](../secgloss/a-gly.md) for the user account to which the [*client certificate*](../secgloss/c-gly.md) was mapped.</span></span> <span data-ttu-id="9f568-107">En outre, le serveur peut utiliser la fonction [**ImpersonateSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext) pour emprunter l’identité du client.</span><span class="sxs-lookup"><span data-stu-id="9f568-107">Also, the server can use the [**ImpersonateSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext) function to impersonate the client.</span></span>

<span data-ttu-id="9f568-108">Pour plus d’informations sur l’authentification, consultez [exécution de l’authentification à l’aide de Schannel](performing-authentication-using-schannel.md).</span><span class="sxs-lookup"><span data-stu-id="9f568-108">For more information on authentication, see [Performing Authentication Using Schannel](performing-authentication-using-schannel.md).</span></span>

 

 
