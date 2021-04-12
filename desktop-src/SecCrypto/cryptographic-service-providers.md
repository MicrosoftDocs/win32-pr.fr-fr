---
description: Important cette API est déconseillée.
ms.assetid: 4e6eb2df-a917-4533-b9f1-8da39598d0b8
title: Fournisseurs de services de chiffrement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5431d8ddda1be977e2a33297613633343fc2f9c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393508"
---
# <a name="cryptographic-service-providers"></a><span data-ttu-id="18d2e-103">Fournisseurs de services de chiffrement</span><span class="sxs-lookup"><span data-stu-id="18d2e-103">Cryptographic Service Providers</span></span>

> [!IMPORTANT]
> <span data-ttu-id="18d2e-104">Cette API est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="18d2e-104">This API is deprecated.</span></span> <span data-ttu-id="18d2e-105">Les logiciels nouveaux et existants doivent commencer à utiliser les [API de cryptographie nouvelle génération.](/windows/desktop/SecCNG/cng-portal)</span><span class="sxs-lookup"><span data-stu-id="18d2e-105">New and existing software should start using [Cryptography Next Generation APIs.](/windows/desktop/SecCNG/cng-portal)</span></span> <span data-ttu-id="18d2e-106">Microsoft peut supprimer cette API dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="18d2e-106">Microsoft may remove this API in future releases.</span></span>

 

<span data-ttu-id="18d2e-107">Un [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP) contient des implémentations de normes et d’algorithmes de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="18d2e-107">A [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) contains implementations of cryptographic standards and algorithms.</span></span> <span data-ttu-id="18d2e-108">Au minimum, un CSP se compose d’une [*bibliothèque de liens dynamiques*](../secgloss/d-gly.md) (dll) qui implémente les fonctions dans [*CryptoSPI*](../secgloss/c-gly.md) (une [*interface de programme système*](../secgloss/s-gly.md)).</span><span class="sxs-lookup"><span data-stu-id="18d2e-108">At a minimum, a CSP consists of a [*dynamic-link library*](../secgloss/d-gly.md) (DLL) that implements the functions in [*CryptoSPI*](../secgloss/c-gly.md) (a [*system program interface*](../secgloss/s-gly.md)).</span></span> <span data-ttu-id="18d2e-109">La plupart des fournisseurs de services de chiffrement contiennent l’implémentation de toutes leurs propres fonctions.</span><span class="sxs-lookup"><span data-stu-id="18d2e-109">Most CSPs contain the implementation of all of their own functions.</span></span> <span data-ttu-id="18d2e-110">Certains fournisseurs de services de chiffrement, toutefois, implémentent leurs fonctions principalement dans un programme de service Windows géré par le gestionnaire de contrôle des services Windows.</span><span class="sxs-lookup"><span data-stu-id="18d2e-110">Some CSPs, however, implement their functions mainly in a Windows-based service program managed by the Windows service control manager.</span></span> <span data-ttu-id="18d2e-111">D’autres implémentent des fonctions matérielles, telles qu’une [*carte à puce*](../secgloss/s-gly.md) ou un coprocesseur sécurisé.</span><span class="sxs-lookup"><span data-stu-id="18d2e-111">Others implement functions in hardware, such as a [*smart card*](../secgloss/s-gly.md) or secure coprocessor.</span></span> <span data-ttu-id="18d2e-112">Si un fournisseur de services de chiffrement n’implémente pas ses propres fonctions, la DLL agit comme une couche directe, facilitant ainsi la communication entre le système d’exploitation et l’implémentation réelle du CSP.</span><span class="sxs-lookup"><span data-stu-id="18d2e-112">If a CSP does not implement its own functions, the DLL acts as a pass-through layer, facilitating the communication between the operating system and the actual CSP implementation.</span></span>

<span data-ttu-id="18d2e-113">Cette section comprend les rubriques suivantes.</span><span class="sxs-lookup"><span data-stu-id="18d2e-113">This section includes the following topics.</span></span>



| <span data-ttu-id="18d2e-114">Rubrique</span><span class="sxs-lookup"><span data-stu-id="18d2e-114">Topic</span></span>                                                                                      | <span data-ttu-id="18d2e-115">Contenu</span><span class="sxs-lookup"><span data-stu-id="18d2e-115">Contents</span></span>                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="18d2e-116">Types de fournisseur de chiffrement</span><span class="sxs-lookup"><span data-stu-id="18d2e-116">Cryptographic Provider Types</span></span>](cryptographic-provider-types.md)                           | <span data-ttu-id="18d2e-117">Les types de fournisseur de chiffrement sont des familles de fournisseurs de services de chiffrement qui partagent des formats de données et des protocoles de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="18d2e-117">Cryptographic provider types are families of cryptographic services providers that share data formats and cryptographic protocols.</span></span> <span data-ttu-id="18d2e-118">Les formats de données incluent les schémas de [*remplissage*](../secgloss/p-gly.md) des algorithmes, les [*longueurs de clé*](../secgloss/k-gly.md)et les modes par défaut.</span><span class="sxs-lookup"><span data-stu-id="18d2e-118">Data formats include algorithms [*padding*](../secgloss/p-gly.md) schemes, [*key lengths*](../secgloss/k-gly.md), and default modes.</span></span> |
| [<span data-ttu-id="18d2e-119">Fournisseurs de services de chiffrement Microsoft</span><span class="sxs-lookup"><span data-stu-id="18d2e-119">Microsoft Cryptographic Service Providers</span></span>](microsoft-cryptographic-service-providers.md) | <span data-ttu-id="18d2e-120">Informations détaillées sur les fournisseurs de services de chiffrement actuellement disponibles auprès de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="18d2e-120">Detailed information about CSPs currently available from Microsoft.</span></span>                                                                                                                                                                                                                                                                                       |



 

 

 
