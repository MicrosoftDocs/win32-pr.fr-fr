---
description: La qualité de protection, identifiée par la directive QoP, est d’abord spécifiée par le serveur dans le test Digest, puis confirmée par le client dans la réponse de la stimulation.
ms.assetid: bee4236c-69e5-4281-a6b3-be316bac0a11
title: Qualité de la protection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4643c9e2de77647a3adf2cbf0441e31bcf5be5de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035050"
---
# <a name="quality-of-protection"></a><span data-ttu-id="304ea-103">Qualité de la protection</span><span class="sxs-lookup"><span data-stu-id="304ea-103">Quality of Protection</span></span>

<span data-ttu-id="304ea-104">La qualité de protection, identifiée par la directive QoP, est d’abord spécifiée par le serveur dans le test Digest, puis confirmée par le client dans la réponse de la stimulation.</span><span class="sxs-lookup"><span data-stu-id="304ea-104">The quality of protection, identified by the qop directive, is first specified by the server in the Digest challenge, and then confirmed by the client in the challenge response.</span></span> <span data-ttu-id="304ea-105">Si le client requiert une qualité de protection que le serveur ne prend pas en charge, le client doit mettre fin à l’authentification.</span><span class="sxs-lookup"><span data-stu-id="304ea-105">If the client requires a quality of protection that the server does not support, the client must terminate the authentication.</span></span>

<span data-ttu-id="304ea-106">Les valeurs possibles pour la directive QoP sont décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="304ea-106">The possible values for the qop directive are described in the following table.</span></span>



| <span data-ttu-id="304ea-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="304ea-107">Value</span></span>                   | <span data-ttu-id="304ea-108">Description</span><span class="sxs-lookup"><span data-stu-id="304ea-108">Description</span></span>                                                                                                                                  |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="304ea-109">authentifié</span><span class="sxs-lookup"><span data-stu-id="304ea-109">"auth"</span></span>                  | <span data-ttu-id="304ea-110">Authentification uniquement.</span><span class="sxs-lookup"><span data-stu-id="304ea-110">Authentication only.</span></span>                                                                                                                         |
| <span data-ttu-id="304ea-111">« AUTH-int »</span><span class="sxs-lookup"><span data-stu-id="304ea-111">"auth-int"</span></span>              | <span data-ttu-id="304ea-112">Authentification et vérification de l' [*intégrité*](../secgloss/i-gly.md) à l’aide de signatures.</span><span class="sxs-lookup"><span data-stu-id="304ea-112">Authentication and [*integrity*](../secgloss/i-gly.md) checking using signatures.</span></span>                  |
| <span data-ttu-id="304ea-113">(SASL uniquement) « AUTH-CONF »</span><span class="sxs-lookup"><span data-stu-id="304ea-113">(SASL only) "auth-conf"</span></span> | <span data-ttu-id="304ea-114">Vérification de l’authentification, de l’intégrité et de la confidentialité à l’aide des signatures et du chiffrement.</span><span class="sxs-lookup"><span data-stu-id="304ea-114">Authentication, integrity and confidentiality checking by using signatures and encryption.</span></span> <span data-ttu-id="304ea-115">Pour plus d’informations, consultez la page [chiffrements](ciphers.md).</span><span class="sxs-lookup"><span data-stu-id="304ea-115">For more information, see [Ciphers](ciphers.md).</span></span> |



 

<span data-ttu-id="304ea-116">La qualité de la protection est déterminée par les indicateurs de spécifications de contexte passés au SSP Microsoft Digest.</span><span class="sxs-lookup"><span data-stu-id="304ea-116">Quality of protection is determined by context requirement flags passed to the Microsoft Digest SSP.</span></span> <span data-ttu-id="304ea-117">Le tableau suivant répertorie les indicateurs relatifs à la qualité de protection et la valeur résultante de la directive QoP.</span><span class="sxs-lookup"><span data-stu-id="304ea-117">The following table lists the flags related to quality of protection, and the resulting value of the qop directive.</span></span>



| <span data-ttu-id="304ea-118">Indicateur</span><span class="sxs-lookup"><span data-stu-id="304ea-118">Flag</span></span>                         | <span data-ttu-id="304ea-119">valeur QoP</span><span class="sxs-lookup"><span data-stu-id="304ea-119">qop value</span></span>               |
|------------------------------|-------------------------|
| <span data-ttu-id="304ea-120">*Xxx* \_ confidentialité des demandes \_</span><span class="sxs-lookup"><span data-stu-id="304ea-120">*XXX*\_REQ\_CONFIDENTIALITY</span></span>  | <span data-ttu-id="304ea-121">« AUTH-conf » (SASL uniquement)</span><span class="sxs-lookup"><span data-stu-id="304ea-121">"auth-conf" (SASL only)</span></span> |
| <span data-ttu-id="304ea-122">*Xxx* \_ détection de la \_ RElecture de la demande \_</span><span class="sxs-lookup"><span data-stu-id="304ea-122">*XXX*\_REQ\_REPLAY\_DETECT</span></span>   | <span data-ttu-id="304ea-123">« AUTH-int »</span><span class="sxs-lookup"><span data-stu-id="304ea-123">"auth-int"</span></span>              |
| <span data-ttu-id="304ea-124">*Xxx* \_ \_détection de séquence de demande \_</span><span class="sxs-lookup"><span data-stu-id="304ea-124">*XXX*\_REQ\_SEQUENCE\_DETECT</span></span> | <span data-ttu-id="304ea-125">« AUTH-int »</span><span class="sxs-lookup"><span data-stu-id="304ea-125">"auth-int"</span></span>              |
| <span data-ttu-id="304ea-126">*Xxx* \_ intégrité de la demande \_</span><span class="sxs-lookup"><span data-stu-id="304ea-126">*XXX*\_REQ\_INTEGRITY</span></span>        | <span data-ttu-id="304ea-127">« AUTH-int »</span><span class="sxs-lookup"><span data-stu-id="304ea-127">"auth-int"</span></span>              |
| <span data-ttu-id="304ea-128">(aucun)</span><span class="sxs-lookup"><span data-stu-id="304ea-128">(none)</span></span>                       | <span data-ttu-id="304ea-129">authentifié</span><span class="sxs-lookup"><span data-stu-id="304ea-129">"auth"</span></span>                  |



 

> [!Note]  
> <span data-ttu-id="304ea-130">Les indicateurs d’exigence de contexte spécifiés par les applications serveur ont un préfixe ASC, et ceux spécifiés par les clients sont préfixés par ISC.</span><span class="sxs-lookup"><span data-stu-id="304ea-130">Context requirement flags specified by server applications have a prefix of ASC, and those specified by clients are prefixed with ISC.</span></span> <span data-ttu-id="304ea-131">Pour déterminer les valeurs d’indicateur utilisées par votre application, remplacez l’un de ces préfixes par *xxx*.</span><span class="sxs-lookup"><span data-stu-id="304ea-131">To determine the flag values used by your application, substitute one of these prefixes for *XXX*.</span></span>

 

<span data-ttu-id="304ea-132">Pour obtenir des informations supplémentaires sur le serveur, consultez [génération de la demande de résumé](generating-the-digest-challenge.md).</span><span class="sxs-lookup"><span data-stu-id="304ea-132">For additional server-related information, see [Generating the Digest Challenge](generating-the-digest-challenge.md).</span></span>

<span data-ttu-id="304ea-133">Pour obtenir des informations supplémentaires sur le client, consultez [génération de la réponse](generating-the-digest-challenge-response.md)aux demandes de test Digest.</span><span class="sxs-lookup"><span data-stu-id="304ea-133">For additional client-related information, see [Generating the Digest Challenge Response](generating-the-digest-challenge-response.md).</span></span>

 

 
