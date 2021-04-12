---
description: 'Contrairement à l’API de chiffrement (CryptoAPI), API de chiffrement : Next Generation (CNG) sépare les fournisseurs de chiffrement des fournisseurs de stockage de clés (KSP).'
ms.assetid: bd4aadc5-d953-4971-b862-00f6d4db0572
title: Fournisseurs de stockage de clés CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: feded42b7796d05e5cec6e255df981b571eb16c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393403"
---
# <a name="cng-key-storage-providers"></a><span data-ttu-id="0f216-103">Fournisseurs de stockage de clés CNG</span><span class="sxs-lookup"><span data-stu-id="0f216-103">CNG Key Storage Providers</span></span>

<span data-ttu-id="0f216-104">Contrairement à l’API de chiffrement (CryptoAPI), API de chiffrement : Next Generation (CNG) sépare les fournisseurs de chiffrement des fournisseurs de stockage de clés (KSP).</span><span class="sxs-lookup"><span data-stu-id="0f216-104">Unlike Cryptography API (CryptoAPI), Cryptography API: Next Generation (CNG) separates cryptographic providers from key storage providers (KSPs).</span></span> <span data-ttu-id="0f216-105">KSP peut être utilisé pour créer, supprimer, exporter, importer, ouvrir et stocker des clés.</span><span class="sxs-lookup"><span data-stu-id="0f216-105">KSPs can be used to create, delete, export, import, open and store keys.</span></span> <span data-ttu-id="0f216-106">En fonction de l’implémentation, elles peuvent également être utilisées pour le chiffrement asymétrique, l’accord secret et la signature.</span><span class="sxs-lookup"><span data-stu-id="0f216-106">Depending on implementation, they can also be used for asymmetric encryption, secret agreement, and signing.</span></span> <span data-ttu-id="0f216-107">Microsoft installe les KSP suivants à partir de Windows Vista et de Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="0f216-107">Microsoft installs the following KSPs beginning with Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="0f216-108">Les fournisseurs peuvent créer et installer d’autres fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="0f216-108">Vendors can create and install other providers.</span></span>

## <a name="microsoft-software-key-storage-provider"></a><span data-ttu-id="0f216-109">Fournisseur de stockage de clés logicielles Microsoft</span><span class="sxs-lookup"><span data-stu-id="0f216-109">Microsoft Software Key Storage Provider</span></span>

<span data-ttu-id="0f216-110">Prend en charge la création et le stockage des clés logicielles, ainsi que les algorithmes suivants.</span><span class="sxs-lookup"><span data-stu-id="0f216-110">Supports software key creation and storage and the following algorithms.</span></span>



| <span data-ttu-id="0f216-111">Algorithm</span><span class="sxs-lookup"><span data-stu-id="0f216-111">Algorithm</span></span>                                          | <span data-ttu-id="0f216-112">Objectif</span><span class="sxs-lookup"><span data-stu-id="0f216-112">Purpose</span></span>                           | <span data-ttu-id="0f216-113">Longueur de la clé (bits)</span><span class="sxs-lookup"><span data-stu-id="0f216-113">Key length (bits)</span></span>                 |
|----------------------------------------------------|-----------------------------------|-----------------------------------|
| <span data-ttu-id="0f216-114">Diffie-Hellman (DH)</span><span class="sxs-lookup"><span data-stu-id="0f216-114">Diffie-Hellman (DH)</span></span>                                | <span data-ttu-id="0f216-115">Accord secret et échange de clé</span><span class="sxs-lookup"><span data-stu-id="0f216-115">Secret agreement and key exchange</span></span> | <span data-ttu-id="0f216-116">512 à 4096 par incréments de 64 bits</span><span class="sxs-lookup"><span data-stu-id="0f216-116">512 to 4096 in 64-bit increments</span></span>  |
| <span data-ttu-id="0f216-117">Algorithme de signature numérique (DSA)</span><span class="sxs-lookup"><span data-stu-id="0f216-117">Digital Signature Algorithm (DSA)</span></span>                  | <span data-ttu-id="0f216-118">Signatures</span><span class="sxs-lookup"><span data-stu-id="0f216-118">Signatures</span></span>                        | <span data-ttu-id="0f216-119">512 à 1024 par incréments de 64 bits</span><span class="sxs-lookup"><span data-stu-id="0f216-119">512 to 1024 in 64-bit increments</span></span>  |
| <span data-ttu-id="0f216-120">ECDH (Elliptic Curve Diffie-Hellman)</span><span class="sxs-lookup"><span data-stu-id="0f216-120">Elliptic Curve Diffie-Hellman (ECDH)</span></span>               | <span data-ttu-id="0f216-121">Accord secret et échange de clé</span><span class="sxs-lookup"><span data-stu-id="0f216-121">Secret agreement and key exchange</span></span> | <span data-ttu-id="0f216-122">P256, P384, P521</span><span class="sxs-lookup"><span data-stu-id="0f216-122">P256, P384, P521</span></span>                  |
| <span data-ttu-id="0f216-123">Algorithme ECDSA (Elliptic Curve Digital Signature Algorithm)</span><span class="sxs-lookup"><span data-stu-id="0f216-123">Elliptic Curve Digital Signature Algorithm (ECDSA)</span></span> | <span data-ttu-id="0f216-124">Signatures</span><span class="sxs-lookup"><span data-stu-id="0f216-124">Signatures</span></span>                        | <span data-ttu-id="0f216-125">P256, P384, P521</span><span class="sxs-lookup"><span data-stu-id="0f216-125">P256, P384, P521</span></span>                  |
| <span data-ttu-id="0f216-126">RSA</span><span class="sxs-lookup"><span data-stu-id="0f216-126">RSA</span></span>                                                | <span data-ttu-id="0f216-127">Chiffrement et signature asymétriques</span><span class="sxs-lookup"><span data-stu-id="0f216-127">Asymmetric encryption and signing</span></span> | <span data-ttu-id="0f216-128">512 à 16384 par incréments de 64 bits</span><span class="sxs-lookup"><span data-stu-id="0f216-128">512 to 16384 in 64-bit increments</span></span> |



 

## <a name="microsoft-smart-card-key-storage-provider"></a><span data-ttu-id="0f216-129">Fournisseur de stockage de clés de carte à puce Microsoft</span><span class="sxs-lookup"><span data-stu-id="0f216-129">Microsoft Smart Card Key Storage Provider</span></span>

<span data-ttu-id="0f216-130">Prend en charge la création et le stockage des clés de carte à puce, ainsi que les algorithmes suivants.</span><span class="sxs-lookup"><span data-stu-id="0f216-130">Supports smart card key creation and storage and the following algorithms.</span></span>



| <span data-ttu-id="0f216-131">Algorithm</span><span class="sxs-lookup"><span data-stu-id="0f216-131">Algorithm</span></span>                                          | <span data-ttu-id="0f216-132">Objectif</span><span class="sxs-lookup"><span data-stu-id="0f216-132">Purpose</span></span>                           | <span data-ttu-id="0f216-133">Longueur de la clé (bits)</span><span class="sxs-lookup"><span data-stu-id="0f216-133">Key length (bits)</span></span>                 |
|----------------------------------------------------|-----------------------------------|-----------------------------------|
| <span data-ttu-id="0f216-134">Diffie-Hellman (DH)</span><span class="sxs-lookup"><span data-stu-id="0f216-134">Diffie-Hellman (DH)</span></span>                                | <span data-ttu-id="0f216-135">Accord secret et échange de clé</span><span class="sxs-lookup"><span data-stu-id="0f216-135">Secret agreement and key exchange</span></span> | <span data-ttu-id="0f216-136">512 à 4096 par incréments de 64 bits</span><span class="sxs-lookup"><span data-stu-id="0f216-136">512 to 4096 in 64-bit increments</span></span>  |
| <span data-ttu-id="0f216-137">ECDH (Elliptic Curve Diffie-Hellman)</span><span class="sxs-lookup"><span data-stu-id="0f216-137">Elliptic Curve Diffie-Hellman (ECDH)</span></span>               | <span data-ttu-id="0f216-138">Accord secret et échange de clé</span><span class="sxs-lookup"><span data-stu-id="0f216-138">Secret agreement and key exchange</span></span> | <span data-ttu-id="0f216-139">P256, P384, P521</span><span class="sxs-lookup"><span data-stu-id="0f216-139">P256, P384, P521</span></span>                  |
| <span data-ttu-id="0f216-140">Algorithme ECDSA (Elliptic Curve Digital Signature Algorithm)</span><span class="sxs-lookup"><span data-stu-id="0f216-140">Elliptic Curve Digital Signature Algorithm (ECDSA)</span></span> | <span data-ttu-id="0f216-141">Signatures</span><span class="sxs-lookup"><span data-stu-id="0f216-141">Signatures</span></span>                        | <span data-ttu-id="0f216-142">P256, P384, P521</span><span class="sxs-lookup"><span data-stu-id="0f216-142">P256, P384, P521</span></span>                  |
| <span data-ttu-id="0f216-143">RSA</span><span class="sxs-lookup"><span data-stu-id="0f216-143">RSA</span></span>                                                | <span data-ttu-id="0f216-144">Chiffrement et signature asymétriques</span><span class="sxs-lookup"><span data-stu-id="0f216-144">Asymmetric encryption and signing</span></span> | <span data-ttu-id="0f216-145">512 à 16384 par incréments de 64 bits</span><span class="sxs-lookup"><span data-stu-id="0f216-145">512 to 16384 in 64-bit increments</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="0f216-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0f216-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f216-147">**Identificateurs d’algorithme CNG**</span><span class="sxs-lookup"><span data-stu-id="0f216-147">**CNG Algorithm Identifiers**</span></span>](/windows/desktop/SecCNG/cng-algorithm-identifiers)
</dt> <dt>

[<span data-ttu-id="0f216-148">Fonctions de stockage de clé CNG</span><span class="sxs-lookup"><span data-stu-id="0f216-148">CNG Key Storage Functions</span></span>](/windows/desktop/SecCNG/cng-key-storage-functions)
</dt> <dt>

[<span data-ttu-id="0f216-149">Comprendre les fournisseurs de services de chiffrement</span><span class="sxs-lookup"><span data-stu-id="0f216-149">Understanding Cryptographic Providers</span></span>](understanding-cryptographic-providers.md)
</dt> </dl>

 

 
