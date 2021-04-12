---
title: Services de base du module de plateforme sécurisée
description: Le logiciel TPM fournit des services sous la forme d’une API exposée via un appel de procédure distante. Utilisez TPM pour créer un module TPM.
ms.assetid: ae6e7fe9-585d-467a-8456-e008b8ea89a0
keywords:
- Services de base TPM TBS
- GPC base services TBS, page d’hébergement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d2cbdfc1f85d6917f2e9a7a5b8e7a0fc25ebdc8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382321"
---
# <a name="tpm-base-services"></a><span data-ttu-id="bd89b-106">Services de base du module de plateforme sécurisée</span><span class="sxs-lookup"><span data-stu-id="bd89b-106">TPM Base Services</span></span>

## <a name="purpose"></a><span data-ttu-id="bd89b-107">Objectif</span><span class="sxs-lookup"><span data-stu-id="bd89b-107">Purpose</span></span>

<span data-ttu-id="bd89b-108">La fonctionnalité des services de base de la Module de plateforme sécurisée (TPM) (TBS) centralise l’accès au module de plateforme sécurisée entre les applications.</span><span class="sxs-lookup"><span data-stu-id="bd89b-108">The Trusted Platform Module (TPM) Base Services (TBS) feature centralizes TPM access across applications.</span></span>

<span data-ttu-id="bd89b-109">La fonctionnalité TBS s’exécute en tant que service système dans Windows Server 2008, Windows Vista ou des systèmes d’exploitation plus récents.</span><span class="sxs-lookup"><span data-stu-id="bd89b-109">The TBS feature runs as a system service in Windows Server 2008, Windows Vista, or newer operating systems.</span></span> <span data-ttu-id="bd89b-110">Il fournit des services comme une API exposée par le biais d’appels de procédure distante (RPC).</span><span class="sxs-lookup"><span data-stu-id="bd89b-110">It provides services as an API exposed through remote procedure calls (RPC).</span></span> <span data-ttu-id="bd89b-111">La fonctionnalité TBS utilise des priorités spécifiées en appelant des applications pour planifier de manière coopérative l’accès au TPM.</span><span class="sxs-lookup"><span data-stu-id="bd89b-111">The TBS feature uses priorities specified by calling applications to cooperatively schedule TPM access.</span></span>

> [!Note]
>
> <span data-ttu-id="bd89b-112">Le module de plateforme sécurisée peut être utilisé pour les opérations de stockage de clés.</span><span class="sxs-lookup"><span data-stu-id="bd89b-112">The TPM can be used for key storage operations.</span></span> <span data-ttu-id="bd89b-113">Toutefois, les développeurs sont encouragés à utiliser les [API de stockage de clés](/windows/desktop/SecCNG/key-storage-and-retrieval) pour ces scénarios à la place.</span><span class="sxs-lookup"><span data-stu-id="bd89b-113">However, developers are encouraged to use the [Key Storage APIs](/windows/desktop/SecCNG/key-storage-and-retrieval) for these scenarios instead.</span></span> <span data-ttu-id="bd89b-114">Les API de stockage de clé offrent les fonctionnalités permettant de créer, signer ou chiffrer des clés de chiffrement, ainsi que de les rendre persistantes. elles sont plus haut et plus faciles à utiliser que le TBS pour ces scénarios ciblés.</span><span class="sxs-lookup"><span data-stu-id="bd89b-114">The Key Storage APIs provide the functionality to create, sign or encrypt with, and persist cryptographic keys, and they are higher-level and easier to use than the TBS for these targeted scenarios.</span></span>

 

## <a name="developer-audience"></a><span data-ttu-id="bd89b-115">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="bd89b-115">Developer audience</span></span>

<span data-ttu-id="bd89b-116">TBS est destiné aux développeurs d’applications basées sur les systèmes d’exploitation Windows.</span><span class="sxs-lookup"><span data-stu-id="bd89b-116">TBS is intended for use by developers of applications based on the Windows operating systems.</span></span> <span data-ttu-id="bd89b-117">Les développeurs doivent être familiarisés avec les langages de programmation C et C++ et dans l’environnement de programmation Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="bd89b-117">Developers should be familiar with the C and C++ programming languages and the Microsoft Windows programming environment.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="bd89b-118">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="bd89b-118">Run-time requirements</span></span>

<span data-ttu-id="bd89b-119">La fonctionnalité TBS requiert au moins le système d’exploitation Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bd89b-119">The TBS feature requires at least Windows Server 2008 or Windows Vista operating system.</span></span> <span data-ttu-id="bd89b-120">Pour plus d’informations sur les exigences d’exécution d’un élément de programmation particulier, consultez la section Configuration requise de la page de référence de cet élément.</span><span class="sxs-lookup"><span data-stu-id="bd89b-120">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="bd89b-121">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="bd89b-121">In this section</span></span>



| <span data-ttu-id="bd89b-122">Rubrique</span><span class="sxs-lookup"><span data-stu-id="bd89b-122">Topic</span></span>                                         | <span data-ttu-id="bd89b-123">Description</span><span class="sxs-lookup"><span data-stu-id="bd89b-123">Description</span></span>                                                                     |
|-----------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="bd89b-124">À propos de TBS</span><span class="sxs-lookup"><span data-stu-id="bd89b-124">About TBS</span></span>](about-tbs.md)<br/>         | <span data-ttu-id="bd89b-125">Concepts clés et une vue de haut niveau de la fonctionnalité TBS.</span><span class="sxs-lookup"><span data-stu-id="bd89b-125">Key concepts and a high-level view of the TBS feature.</span></span><br/>               |
| [<span data-ttu-id="bd89b-126">Utilisation de TBS</span><span class="sxs-lookup"><span data-stu-id="bd89b-126">Using TBS</span></span>](using-tbs.md)<br/>         | <span data-ttu-id="bd89b-127">Processus et procédures TBS pour l’utilisation de l’API TBS.</span><span class="sxs-lookup"><span data-stu-id="bd89b-127">TBS processes and procedures for using the TBS API.</span></span><br/>                  |
| [<span data-ttu-id="bd89b-128">Référence TBS</span><span class="sxs-lookup"><span data-stu-id="bd89b-128">TBS Reference</span></span>](tbs-reference.md)<br/> | <span data-ttu-id="bd89b-129">Documentation sur les fonctions TBS, les structures et les codes de retour.</span><span class="sxs-lookup"><span data-stu-id="bd89b-129">Documentation about the TBS functions, structures, and return codes.</span></span><br/> |



 

 

