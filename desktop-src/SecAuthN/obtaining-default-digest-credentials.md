---
description: Les clients et les serveurs doivent obtenir des informations d’identification avant de pouvoir établir un contexte de sécurité pour l’échange de messages.
ms.assetid: a72404b8-1ec9-4f58-b3a6-09811070ea29
title: Obtention des informations d’identification Digest par défaut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12e870d6bad1c3b4ef9e889a91444e98159bc758
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202723"
---
# <a name="obtaining-default-digest-credentials"></a><span data-ttu-id="7d7da-103">Obtention des informations d’identification Digest par défaut</span><span class="sxs-lookup"><span data-stu-id="7d7da-103">Obtaining Default Digest Credentials</span></span>

<span data-ttu-id="7d7da-104">Les clients et les serveurs doivent obtenir des [*informations d’identification*](../secgloss/c-gly.md) avant de pouvoir établir un [*contexte de sécurité*](../secgloss/s-gly.md) pour l’échange de messages.</span><span class="sxs-lookup"><span data-stu-id="7d7da-104">Both clients and servers must obtain [*credentials*](../secgloss/c-gly.md) before they can establish a [*security context*](../secgloss/s-gly.md) for message exchange.</span></span> <span data-ttu-id="7d7da-105">Le comportement par défaut de la fonction [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) consiste à fournir des informations d’identification pour le principal de sécurité associé à la session d’ouverture de [*session*](../secgloss/s-gly.md)en cours.</span><span class="sxs-lookup"><span data-stu-id="7d7da-105">The default behavior of the [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) function is to provide credentials for the security principal associated with the current logon [*session*](../secgloss/s-gly.md).</span></span>

<span data-ttu-id="7d7da-106">L’exemple suivant illustre un appel côté serveur pour obtenir les informations d’identification par défaut.</span><span class="sxs-lookup"><span data-stu-id="7d7da-106">The following example demonstrates a server-side call to obtain the default credentials.</span></span>


```C++
SECURITY_STATUS SecStatus; 
TimeStamp tsLifetime; 
CredHandle hCred;
SecStatus = AcquireCredentialsHandle (
       NULL,                  // Default principal.
       WDIGEST_SP_NAME,       // Microsoft Digest SSP. 
       SECPKG_CRED_INBOUND,   // Server will use the credentials.
       NULL,                  // Use the current LOGON id.
       NULL,                  // Default credentials.
       NULL,                  // Not used with Digest SSP.
       NULL,                  // Not used with Digest SSP.
       &hCred,                // Receives the credential handle.
       &tsLifetime            // Receives the credential time limit.
);
```



<span data-ttu-id="7d7da-107">L’appel côté client pour les informations d’identification par défaut est identique, sauf que le troisième paramètre doit spécifier SECPKG \_ cred \_ sortant pour indiquer que le client utilisera le handle d’informations d’identification retourné par la fonction.</span><span class="sxs-lookup"><span data-stu-id="7d7da-107">The client-side call for default credentials is identical, except the third parameter must specify SECPKG\_CRED\_OUTBOUND to indicate that the client will use the credentials handle returned by the function.</span></span>

<span data-ttu-id="7d7da-108">Pour obtenir un exemple illustrant l’obtention d’informations d’identification pour un principal de sécurité autre que l’utilisateur connecté, consultez [obtention d’autres informations d’identification](obtaining-alternate-digest-credentials.md).</span><span class="sxs-lookup"><span data-stu-id="7d7da-108">For an example that demonstrates obtaining credentials for a security principal other than the logged on user, see [Obtaining Alternate Credentials](obtaining-alternate-digest-credentials.md).</span></span>

 

 
