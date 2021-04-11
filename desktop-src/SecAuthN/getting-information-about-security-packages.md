---
description: Lorsqu’un client démarre, il sélectionne un package de sécurité pour ses transactions avec un serveur, puis il contacte ce serveur. Un serveur sélectionne un ou plusieurs packages de sécurité et attend une connexion cliente.
ms.assetid: eaed162b-ef07-4295-93d9-6be91232a82e
title: Obtention d’informations sur les packages de sécurité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca690575ff7f46ef5a5b1d971b1ab9fdd91f95e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113807"
---
# <a name="getting-information-about-security-packages"></a><span data-ttu-id="336ae-104">Obtention d’informations sur les packages de sécurité</span><span class="sxs-lookup"><span data-stu-id="336ae-104">Getting Information About Security Packages</span></span>

<span data-ttu-id="336ae-105">Lorsqu’un client démarre, il sélectionne un [*package de sécurité*](/windows/desktop/SecGloss/s-gly) pour ses transactions avec un serveur, puis il contacte ce serveur.</span><span class="sxs-lookup"><span data-stu-id="336ae-105">When a client begins, it selects a [*security package*](/windows/desktop/SecGloss/s-gly) for its transactions with a server and then contacts that server.</span></span> <span data-ttu-id="336ae-106">Un serveur sélectionne un ou plusieurs packages de sécurité et attend une connexion cliente.</span><span class="sxs-lookup"><span data-stu-id="336ae-106">A server selects one or more security packages and waits for a client connection.</span></span>

<span data-ttu-id="336ae-107">Pour obtenir des informations spécifiques sur les packages de sécurité SSPI disponibles avec un SSP particulier, la fonction [**EnumerateSecurityPackages**](/windows/desktop/api/Sspi/nf-sspi-enumeratesecuritypackagesa) peut être appelée pour récupérer une structure [**SecPkgInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) .</span><span class="sxs-lookup"><span data-stu-id="336ae-107">For specific information about the SSPI security packages available with a particular SSP, the [**EnumerateSecurityPackages**](/windows/desktop/api/Sspi/nf-sspi-enumeratesecuritypackagesa) function can be called to retrieve a [**SecPkgInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) structure.</span></span>

<span data-ttu-id="336ae-108">Pour récupérer la structure de sortie, l’appelant passe à la fonction l’adresse d’un pointeur vers le type de la structure de retour.</span><span class="sxs-lookup"><span data-stu-id="336ae-108">To retrieve the output structure, the caller passes to the function the address of a pointer to the type of the return structure.</span></span> <span data-ttu-id="336ae-109">La fonction alloue de la mémoire et retourne les données à l’appelant en affectant l’adresse du tampon de données de retour à l’argument.</span><span class="sxs-lookup"><span data-stu-id="336ae-109">The function allocates memory and returns the data to the caller by assigning the address of the return data buffer to the argument.</span></span> <span data-ttu-id="336ae-110">La Convention SSPI est que la fonction alloue de la mémoire pour la structure, et que l’application appelante libère cette mémoire à l’aide de [**FreeContextBuffer**](/windows/desktop/api/Sspi/nf-sspi-freecontextbuffer).</span><span class="sxs-lookup"><span data-stu-id="336ae-110">The SSPI convention is that the function allocates memory for the structure, and the calling application frees that memory using [**FreeContextBuffer**](/windows/desktop/api/Sspi/nf-sspi-freecontextbuffer).</span></span>

<span data-ttu-id="336ae-111">L’appel de la fonction [**QuerySecurityPackageInfo**](/windows/desktop/api/Sspi/nf-sspi-querysecuritypackageinfoa) récupère les attributs d’un [*package de sécurité*](/windows/desktop/SecGloss/s-gly).</span><span class="sxs-lookup"><span data-stu-id="336ae-111">Calling the [**QuerySecurityPackageInfo**](/windows/desktop/api/Sspi/nf-sspi-querysecuritypackageinfoa) function retrieves the attributes of a [*security package*](/windows/desktop/SecGloss/s-gly).</span></span> <span data-ttu-id="336ae-112">Le serveur et le client peuvent appeler la fonction **QuerySecurityPackageInfo** pour connaître la longueur maximale du jeton de sécurité du membre **cbMaxToken** de la structure [**SecPkgInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) .</span><span class="sxs-lookup"><span data-stu-id="336ae-112">Both server and client can call the **QuerySecurityPackageInfo** function to get the maximum length of the security token from the **cbMaxToken** member of the [**SecPkgInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) structure.</span></span> <span data-ttu-id="336ae-113">Pour obtenir un exemple, consultez l’appel à la fonction **QuerySecurityPackageInfo** présentée dans [utilisation de SSPI avec un serveur Windows Sockets](using-sspi-with-a-windows-sockets-server.md).</span><span class="sxs-lookup"><span data-stu-id="336ae-113">For an example, see the call to the **QuerySecurityPackageInfo** function shown in [Using SSPI with a Windows Sockets Server](using-sspi-with-a-windows-sockets-server.md).</span></span>

<span data-ttu-id="336ae-114">Pour plus d’informations sur les fonctions de package, consultez [Package Management](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="336ae-114">For more information on package functions, see [Package Management](authentication-functions.md).</span></span>

 

 
