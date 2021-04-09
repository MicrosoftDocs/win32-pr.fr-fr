---
description: Le fournisseur de services de chiffrement amélioré de Microsoft fournit une application offrant une sécurité renforcée par rapport au fournisseur de services de chiffrement de base Microsoft. Une longueur de clé supérieure offre aux utilisateurs une meilleure protection des données sensibles.
ms.assetid: cd16705c-c617-4843-a303-52d1019a60bb
title: Comparaison de la longueur de clé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34a82bd4ffe942a58bba4c246f92e83fa1e1ef03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869013"
---
# <a name="key-length-comparison"></a><span data-ttu-id="574be-104">Comparaison de la longueur de clé</span><span class="sxs-lookup"><span data-stu-id="574be-104">Key Length Comparison</span></span>

<span data-ttu-id="574be-105">Le fournisseur de services de chiffrement amélioré de Microsoft fournit une application offrant une sécurité renforcée par rapport au fournisseur de services de chiffrement de base Microsoft.</span><span class="sxs-lookup"><span data-stu-id="574be-105">The Microsoft Enhanced Cryptographic Provider provides an application with stronger security than currently available with the Microsoft Base Cryptographic Provider.</span></span> <span data-ttu-id="574be-106">Une longueur de clé supérieure offre aux utilisateurs une meilleure protection des données sensibles.</span><span class="sxs-lookup"><span data-stu-id="574be-106">Greater key length gives users more protection for sensitive data.</span></span>

<span data-ttu-id="574be-107">Le tableau suivant répertorie les [*longueurs de clé*](../secgloss/k-gly.md) par défaut prises en charge par le fournisseur de base et le fournisseur amélioré pour les algorithmes standard.</span><span class="sxs-lookup"><span data-stu-id="574be-107">The following table lists the default [*key lengths*](../secgloss/k-gly.md) supported by the Base Provider and the Enhanced Provider for standard algorithms.</span></span>



| <span data-ttu-id="574be-108">Algorithm</span><span class="sxs-lookup"><span data-stu-id="574be-108">Algorithm</span></span>                                                                                | <span data-ttu-id="574be-109">Fournisseur de base</span><span class="sxs-lookup"><span data-stu-id="574be-109">Base Provider</span></span> | <span data-ttu-id="574be-110">Fournisseurs forts et améliorés</span><span class="sxs-lookup"><span data-stu-id="574be-110">Strong and Enhanced Providers</span></span> |
|------------------------------------------------------------------------------------------|---------------|-------------------------------|
| <span data-ttu-id="574be-111">Échange de clés RSA</span><span class="sxs-lookup"><span data-stu-id="574be-111">RSA Key Exchange</span></span>                                                                         | <span data-ttu-id="574be-112">512 bits</span><span class="sxs-lookup"><span data-stu-id="574be-112">512-bit</span></span>       | <span data-ttu-id="574be-113">1 024 bits</span><span class="sxs-lookup"><span data-stu-id="574be-113">1,024-bit</span></span>                     |
| <span data-ttu-id="574be-114">Signature RSA</span><span class="sxs-lookup"><span data-stu-id="574be-114">RSA Signature</span></span>                                                                            | <span data-ttu-id="574be-115">512 bits</span><span class="sxs-lookup"><span data-stu-id="574be-115">512-bit</span></span>       | <span data-ttu-id="574be-116">1 024 bits</span><span class="sxs-lookup"><span data-stu-id="574be-116">1,024-bit</span></span>                     |
| <span data-ttu-id="574be-117">RC2</span><span class="sxs-lookup"><span data-stu-id="574be-117">RC2</span></span>                                                                                      | <span data-ttu-id="574be-118">40 bits</span><span class="sxs-lookup"><span data-stu-id="574be-118">40-bit</span></span>        | <span data-ttu-id="574be-119">128 bits</span><span class="sxs-lookup"><span data-stu-id="574be-119">128-bit</span></span>                       |
| <span data-ttu-id="574be-120">RC4</span><span class="sxs-lookup"><span data-stu-id="574be-120">RC4</span></span>                                                                                      | <span data-ttu-id="574be-121">40 bits</span><span class="sxs-lookup"><span data-stu-id="574be-121">40-bit</span></span>        | <span data-ttu-id="574be-122">128 bits</span><span class="sxs-lookup"><span data-stu-id="574be-122">128-bit</span></span>                       |
| <span data-ttu-id="574be-123">DES</span><span class="sxs-lookup"><span data-stu-id="574be-123">DES</span></span>                                                                                      | <span data-ttu-id="574be-124">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="574be-124">Not supported</span></span> | <span data-ttu-id="574be-125">56 bits</span><span class="sxs-lookup"><span data-stu-id="574be-125">56-bit</span></span>                        |
| <span data-ttu-id="574be-126">[*Triple des*](../secgloss/t-gly.md) (2-clé)</span><span class="sxs-lookup"><span data-stu-id="574be-126">[*Triple DES*](../secgloss/t-gly.md) (2-key)</span></span> | <span data-ttu-id="574be-127">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="574be-127">Not supported</span></span> | <span data-ttu-id="574be-128">112 bits</span><span class="sxs-lookup"><span data-stu-id="574be-128">112-bit</span></span>                       |
| <span data-ttu-id="574be-129">Triple DES (3 touches)</span><span class="sxs-lookup"><span data-stu-id="574be-129">Triple DES (3-key)</span></span>                                                                       | <span data-ttu-id="574be-130">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="574be-130">Not supported</span></span> | <span data-ttu-id="574be-131">168 bits</span><span class="sxs-lookup"><span data-stu-id="574be-131">168-bit</span></span>                       |



 

<span data-ttu-id="574be-132">Les algorithmes [*des*](../secgloss/d-gly.md) et [*triple des*](../secgloss/t-gly.md) sont pris en charge dans le fournisseur amélioré.</span><span class="sxs-lookup"><span data-stu-id="574be-132">[*DES*](../secgloss/d-gly.md) and [*Triple DES*](../secgloss/t-gly.md) algorithms are supported in the Enhanced Provider.</span></span>

<span data-ttu-id="574be-133">Le fournisseur amélioré est à compatibilité descendante avec le fournisseur de base distribué avec les versions antérieures de CryptoAPI, avec l’exception suivante.</span><span class="sxs-lookup"><span data-stu-id="574be-133">The Enhanced Provider is backward-compatible with the Base Provider distributed with earlier versions of CryptoAPI with the following exception.</span></span> <span data-ttu-id="574be-134">Le fournisseur de base et le fournisseur amélioré peuvent uniquement générer des clés de session de longueur de clé par défaut.</span><span class="sxs-lookup"><span data-stu-id="574be-134">Both the base provider and the Enhanced Provider can only generate session keys of default key length.</span></span> <span data-ttu-id="574be-135">La longueur par défaut des clés de session pour le fournisseur de base est de 40 bits.</span><span class="sxs-lookup"><span data-stu-id="574be-135">The default length of session keys for the Base Provider is 40 bits.</span></span> <span data-ttu-id="574be-136">La longueur de clé par défaut pour le fournisseur amélioré est 128 bits.</span><span class="sxs-lookup"><span data-stu-id="574be-136">The default key length for the Enhanced Provider is 128 bits.</span></span> <span data-ttu-id="574be-137">Le fournisseur amélioré ne peut pas créer de clés avec des longueurs de clé compatibles avec le fournisseur de base.</span><span class="sxs-lookup"><span data-stu-id="574be-137">The Enhanced Provider cannot create keys with Base Provider-compatible key lengths.</span></span> <span data-ttu-id="574be-138">Toutefois, le fournisseur amélioré peut importer des longueurs de clé de n’importe quelle taille, jusqu’à 128 bits.</span><span class="sxs-lookup"><span data-stu-id="574be-138">However, the Enhanced Provider can import key lengths of any size, up to 128 bits.</span></span>

 

 
