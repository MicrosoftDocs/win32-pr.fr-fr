---
description: L’authentification HTTP à l’aide de Microsoft Digest requiert trois mémoires tampons d’entrée pour générer une réponse de stimulation. Le tableau suivant récapitule ces mémoires tampons.
ms.assetid: 0df02be2-f42e-46d0-a206-765adf3d7a72
title: Mémoires tampons d’entrée pour la réponse de stimulation Digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 982923782b13e37a5e3531717dabf47016c60932
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112190"
---
# <a name="input-buffers-for-the-digest-challenge-response"></a><span data-ttu-id="92cea-104">Mémoires tampons d’entrée pour la réponse de stimulation Digest</span><span class="sxs-lookup"><span data-stu-id="92cea-104">Input Buffers for the Digest Challenge Response</span></span>

<span data-ttu-id="92cea-105">L’authentification HTTP à l’aide de Microsoft Digest requiert trois mémoires tampons d’entrée pour générer une réponse de stimulation.</span><span class="sxs-lookup"><span data-stu-id="92cea-105">HTTP authentication using Microsoft Digest requires three input buffers to generate a challenge response.</span></span> <span data-ttu-id="92cea-106">Le tableau suivant récapitule ces mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="92cea-106">The following table summarizes these buffers.</span></span>



| <span data-ttu-id="92cea-107">Numéro de mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="92cea-107">Buffer number</span></span> | <span data-ttu-id="92cea-108">Contient</span><span class="sxs-lookup"><span data-stu-id="92cea-108">Contains</span></span>                                                                                                                                             | <span data-ttu-id="92cea-109">Type de mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="92cea-109">Buffer type</span></span>                                                 |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="92cea-110">0</span><span class="sxs-lookup"><span data-stu-id="92cea-110">0</span></span>             | <span data-ttu-id="92cea-111">Défi reçu du serveur</span><span class="sxs-lookup"><span data-stu-id="92cea-111">Challenge received from the Server</span></span>                                                                                                                   | <span data-ttu-id="92cea-112">\_jeton SECBUFFER</span><span class="sxs-lookup"><span data-stu-id="92cea-112">SECBUFFER\_TOKEN</span></span>                                            |
| <span data-ttu-id="92cea-113">1</span><span class="sxs-lookup"><span data-stu-id="92cea-113">1</span></span>             | <span data-ttu-id="92cea-114">Méthode HTTP</span><span class="sxs-lookup"><span data-stu-id="92cea-114">HTTP Method</span></span>                                                                                                                                          | <span data-ttu-id="92cea-115">\_paramètres SECBUFFER</span><span class="sxs-lookup"><span data-stu-id="92cea-115">SECBUFFER\_PARAMS</span></span>                                           |
| <span data-ttu-id="92cea-116">2</span><span class="sxs-lookup"><span data-stu-id="92cea-116">2</span></span>             | <span data-ttu-id="92cea-117">H (entité)</span><span class="sxs-lookup"><span data-stu-id="92cea-117">H(Entity)</span></span>                                                                                                                                            | <span data-ttu-id="92cea-118">\_paramètres SECBUFFER</span><span class="sxs-lookup"><span data-stu-id="92cea-118">SECBUFFER\_PARAMS</span></span>                                           |
| <span data-ttu-id="92cea-119">3</span><span class="sxs-lookup"><span data-stu-id="92cea-119">3</span></span>             | <span data-ttu-id="92cea-120">[*Nom de principal du service*](../secgloss/s-gly.md) (SPN) du serveur cible.</span><span class="sxs-lookup"><span data-stu-id="92cea-120">The [*service principal name*](../secgloss/s-gly.md) (SPN) of the target server.</span></span> | <span data-ttu-id="92cea-121">**SECBUFFER \_ \_** \| **SECBUFFER en \_ lecture seule** de l’hôte cible</span><span class="sxs-lookup"><span data-stu-id="92cea-121">**SECBUFFER\_TARGET\_HOST** \| **SECBUFFER\_READONLY**</span></span>      |
| <span data-ttu-id="92cea-122">4</span><span class="sxs-lookup"><span data-stu-id="92cea-122">4</span></span>             | <span data-ttu-id="92cea-123">Valeurs de jeton des liaisons de canal</span><span class="sxs-lookup"><span data-stu-id="92cea-123">Channel bindings token values</span></span>                                                                                                                        | <span data-ttu-id="92cea-124">**SECBUFFER \_ \_liaisons de canal** \| **SECBUFFER \_ ReadOnly**</span><span class="sxs-lookup"><span data-stu-id="92cea-124">**SECBUFFER\_CHANNEL\_BINDINGS** \| **SECBUFFER\_READONLY**</span></span> |



 

<span data-ttu-id="92cea-125">La mémoire tampon zéro contient la stimulation du condensé reçue du serveur en réponse à la demande initiale d’une ressource protégée par l’accès.</span><span class="sxs-lookup"><span data-stu-id="92cea-125">Buffer zero contains the Digest challenge received from the server in response to the initial request for an access-protected resource.</span></span>

<span data-ttu-id="92cea-126">La mémoire tampon 1 contient la représentation sous forme de chaîne de la méthode, telle que « obtient » ou « poster ».</span><span class="sxs-lookup"><span data-stu-id="92cea-126">Buffer 1 contains the string representation of the method, such as "GET" or "POST".</span></span> <span data-ttu-id="92cea-127">La méthode est utilisée dans le calcul de a2, comme décrit dans le [document RFC 2617](https://www.ietf.org/rfc/rfc2617.txt).</span><span class="sxs-lookup"><span data-stu-id="92cea-127">The method is used in the calculation of A2, as described in [RFC 2617](https://www.ietf.org/rfc/rfc2617.txt).</span></span>

<span data-ttu-id="92cea-128">La mémoire tampon 2 est le hachage [*MD5*](../secgloss/m-gly.md) du corps de l’entité du message, comme décrit dans le document RFC 2617.</span><span class="sxs-lookup"><span data-stu-id="92cea-128">Buffer 2 is the [*MD5*](../secgloss/m-gly.md) hash of the message's entity-body as described in RFC 2617.</span></span>

<span data-ttu-id="92cea-129">La mémoire tampon 3 contient le nom principal de service du serveur cible au format UTF-8 quand Digest est utilisé avec les liaisons de canal.</span><span class="sxs-lookup"><span data-stu-id="92cea-129">Buffer 3 contains the SPN of the target server in UTF-8 formatting when Digest is used with channel bindings.</span></span>

<span data-ttu-id="92cea-130">Buffer 4 contient la valeur du jeton de liaison de canal quand Digest est utilisé avec les liaisons de canal.</span><span class="sxs-lookup"><span data-stu-id="92cea-130">Buffer 4 contains the channel binding token value when Digest is used with channel bindings.</span></span>

## <a name="input-buffers-for-sasl"></a><span data-ttu-id="92cea-131">Mémoires tampons d’entrée pour SASL</span><span class="sxs-lookup"><span data-stu-id="92cea-131">Input Buffers for SASL</span></span>

<span data-ttu-id="92cea-132">Mémoire tampon d’approvisionnement zéro uniquement.</span><span class="sxs-lookup"><span data-stu-id="92cea-132">Supply buffer zero only.</span></span> <span data-ttu-id="92cea-133">Pour la compatibilité avec d’autres SSP, vous pouvez appeler [**InitializeSecurityContext (Digest)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) sans une demande de serveur valide.</span><span class="sxs-lookup"><span data-stu-id="92cea-133">For compatibility with other SSPs, you may call [**InitializeSecurityContext (Digest)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) without a valid server challenge.</span></span> <span data-ttu-id="92cea-134">Dans ce cas, le paramètre *pInput* doit avoir la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="92cea-134">In this case the *pInput* parameter should be set to **NULL**.</span></span>

 

 
