---
description: La taille d’une demande d’accès Digest doit être inférieure à 2048 octets.
ms.assetid: 16c6728a-966b-436f-902d-3e12368986b6
title: Contenu d’une demande de résumé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97f90dd78ae28536f6e2d07882f69335975df14d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112199"
---
# <a name="contents-of-a-digest-challenge"></a><span data-ttu-id="7ab9a-103">Contenu d’une demande de résumé</span><span class="sxs-lookup"><span data-stu-id="7ab9a-103">Contents of a Digest Challenge</span></span>

<span data-ttu-id="7ab9a-104">La taille d’une demande d’accès Digest doit être inférieure à 2048 octets.</span><span class="sxs-lookup"><span data-stu-id="7ab9a-104">The size of a Digest Access challenge must be less than 2048 bytes.</span></span> <span data-ttu-id="7ab9a-105">L’exemple suivant montre une stimulation assignée à la chaîne de caractères szChallenge.</span><span class="sxs-lookup"><span data-stu-id="7ab9a-105">The following example shows a challenge assigned to the character string szChallenge.</span></span>


```C++
szChallenge = "realm=\"Microsoft_Example_Forest\",";
algorithm = "MD5-sess\", qop=\"auth\", nonce=\"0123456789abcdef\"";
```



> [!Note]  
> <span data-ttu-id="7ab9a-106">La chaîne de stimulation est placée entre guillemets doubles et contient des guillemets doubles incorporés.</span><span class="sxs-lookup"><span data-stu-id="7ab9a-106">The challenge string is enclosed in double quotes and contains embedded double quotes.</span></span> <span data-ttu-id="7ab9a-107">Les guillemets doubles incorporés doivent être précédés d’une barre oblique inverse ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="7ab9a-107">Embedded double quotes must be preceded (escaped) with a backslash (\\).</span></span>

 

<span data-ttu-id="7ab9a-108">Un challenge Digest peut contenir les directives suivantes.</span><span class="sxs-lookup"><span data-stu-id="7ab9a-108">A Digest challenge can contain the following directives.</span></span>



| <span data-ttu-id="7ab9a-109">Directive</span><span class="sxs-lookup"><span data-stu-id="7ab9a-109">Directive</span></span>         | <span data-ttu-id="7ab9a-110">Description</span><span class="sxs-lookup"><span data-stu-id="7ab9a-110">Description</span></span>                                                                                                                                                                                                                                                                                            |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ab9a-111">realm</span><span class="sxs-lookup"><span data-stu-id="7ab9a-111">realm</span></span>             | <span data-ttu-id="7ab9a-112">Indicateur défini par l’implémentation au client sur lequel les [*informations d’identification*](/windows/desktop/SecGloss/c-gly) sont requises.</span><span class="sxs-lookup"><span data-stu-id="7ab9a-112">An implementation-defined hint to the client about which [*credentials*](/windows/desktop/SecGloss/c-gly) are required.</span></span> <span data-ttu-id="7ab9a-113">Le client doit afficher ces informations à l’utilisateur s’il demande des informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="7ab9a-113">The client should display this information to the user if it is prompting for credentials.</span></span>                                                  |
| <span data-ttu-id="7ab9a-114">algorithme</span><span class="sxs-lookup"><span data-stu-id="7ab9a-114">algorithm</span></span>         | <span data-ttu-id="7ab9a-115">Microsoft Digest prend en charge MD5 et MD5-sess.</span><span class="sxs-lookup"><span data-stu-id="7ab9a-115">Microsoft Digest supports MD5 and MD5-Sess.</span></span> <span data-ttu-id="7ab9a-116">Pour des performances optimales, utilisez MD5-sess.</span><span class="sxs-lookup"><span data-stu-id="7ab9a-116">For optimal performance, use MD5-Sess.</span></span>                                                                                                                                                                                                                     |
| <span data-ttu-id="7ab9a-117">qop</span><span class="sxs-lookup"><span data-stu-id="7ab9a-117">qop</span></span>               | <span data-ttu-id="7ab9a-118">Cette directive peut être définie sur auth, auth-int ou auth-CONF.</span><span class="sxs-lookup"><span data-stu-id="7ab9a-118">This directive can be set to auth, auth-int, or auth-conf.</span></span> <span data-ttu-id="7ab9a-119">Pour plus d’informations, consultez [qualité de la protection et des chiffrements](quality-of-protection-and-ciphers.md).</span><span class="sxs-lookup"><span data-stu-id="7ab9a-119">For more information, see [Quality of Protection and Ciphers](quality-of-protection-and-ciphers.md).</span></span>                                                                                                                                       |
| <span data-ttu-id="7ab9a-120">nonce</span><span class="sxs-lookup"><span data-stu-id="7ab9a-120">nonce</span></span>             | <span data-ttu-id="7ab9a-121">Valeur encodée unique générée par le serveur pour chaque stimulation.</span><span class="sxs-lookup"><span data-stu-id="7ab9a-121">A unique encoded value generated by the server for each challenge.</span></span> <span data-ttu-id="7ab9a-122">Cette valeur ne doit pas être modifiée par le client.</span><span class="sxs-lookup"><span data-stu-id="7ab9a-122">This value must not be altered by the client.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="7ab9a-123">manière</span><span class="sxs-lookup"><span data-stu-id="7ab9a-123">opaque</span></span>            | <span data-ttu-id="7ab9a-124">Contient une référence pour le [*contexte de sécurité*](/windows/desktop/SecGloss/s-gly) en cours d’établissement.</span><span class="sxs-lookup"><span data-stu-id="7ab9a-124">Contains a reference for the [*security context*](/windows/desktop/SecGloss/s-gly) that is being established.</span></span> <span data-ttu-id="7ab9a-125">Pour plus d’informations, consultez [maintenance du contexte de sécurité entre les connexions](maintaining-the-security-context-between-connections.md).</span><span class="sxs-lookup"><span data-stu-id="7ab9a-125">For more information, see [Maintaining the Security Context Between Connections](maintaining-the-security-context-between-connections.md).</span></span> |
| <span data-ttu-id="7ab9a-126">chiffrement (SASL uniquement)</span><span class="sxs-lookup"><span data-stu-id="7ab9a-126">cipher(SASL only)</span></span> | <span data-ttu-id="7ab9a-127">Liste des chiffrements pris en charge par le serveur.</span><span class="sxs-lookup"><span data-stu-id="7ab9a-127">The list of ciphers that the server supports.</span></span> <span data-ttu-id="7ab9a-128">Cet élément peut être présent dans un challenge SASL Digest uniquement si la directive QoP spécifie auth-CONF.</span><span class="sxs-lookup"><span data-stu-id="7ab9a-128">This element can be present in a Digest SASL challenge only if the qop directive specifies auth-conf.</span></span> <span data-ttu-id="7ab9a-129">Pour plus d’informations, consultez [qualité de la protection et des chiffrements](quality-of-protection-and-ciphers.md).</span><span class="sxs-lookup"><span data-stu-id="7ab9a-129">For more information, see [Quality of Protection and Ciphers](quality-of-protection-and-ciphers.md).</span></span>                                              |
| <span data-ttu-id="7ab9a-130">charset</span><span class="sxs-lookup"><span data-stu-id="7ab9a-130">charset</span></span>           | <span data-ttu-id="7ab9a-131">Cette directive peut être définie sur UTF-8 Si le serveur peut traiter les noms d’utilisateur et les domaines encodés en UTF-8.</span><span class="sxs-lookup"><span data-stu-id="7ab9a-131">This directive can be set to utf-8 if the server can process UTF-8–encoded user names and realms.</span></span> <span data-ttu-id="7ab9a-132">Si le client comprend la directive CharSet, il peut répondre en utilisant des valeurs encodées en UTF-8.</span><span class="sxs-lookup"><span data-stu-id="7ab9a-132">If the client understands the charset directive, it can respond by using UTF-8–encoded values.</span></span>                                                                                                       |



 

<span data-ttu-id="7ab9a-133">Microsoft Digest génère la chaîne de Challenge Digest pour les applications serveur.</span><span class="sxs-lookup"><span data-stu-id="7ab9a-133">Microsoft Digest generates the Digest challenge string for server applications.</span></span> <span data-ttu-id="7ab9a-134">Pour plus d’informations, consultez [génération de la demande de résumé](generating-the-digest-challenge.md).</span><span class="sxs-lookup"><span data-stu-id="7ab9a-134">For details, see [Generating the Digest Challenge](generating-the-digest-challenge.md).</span></span>

 

 
