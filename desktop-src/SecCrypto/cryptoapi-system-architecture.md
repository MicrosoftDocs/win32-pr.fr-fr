---
description: Explique l’architecture système CryptoAPI.
ms.assetid: 244329bb-fc71-4ab9-8831-a9478108ffa3
title: Architecture du système CryptoAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86d5dcf1756c9b581d75d4e52d57fbce089976a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318233"
---
# <a name="cryptoapi-system-architecture"></a><span data-ttu-id="630a5-103">Architecture du système CryptoAPI</span><span class="sxs-lookup"><span data-stu-id="630a5-103">CryptoAPI System Architecture</span></span>

<span data-ttu-id="630a5-104">L’architecture système CryptoAPI est composée de cinq domaines fonctionnels majeurs :</span><span class="sxs-lookup"><span data-stu-id="630a5-104">The CryptoAPI system architecture is composed of five major functional areas:</span></span>

-   [<span data-ttu-id="630a5-105">Fonctions de chiffrement de base</span><span class="sxs-lookup"><span data-stu-id="630a5-105">Base Cryptographic Functions</span></span>](#base-cryptographic-functions)
-   [<span data-ttu-id="630a5-106">Fonctions de codage/décodage de certificat</span><span class="sxs-lookup"><span data-stu-id="630a5-106">Certificate Encode/Decode Functions</span></span>](#certificate-encodedecode-functions)
-   [<span data-ttu-id="630a5-107">Fonctions du magasin de certificats</span><span class="sxs-lookup"><span data-stu-id="630a5-107">Certificate Store Functions</span></span>](#certificate-store-functions)
-   [<span data-ttu-id="630a5-108">Fonctions de message simplifiées</span><span class="sxs-lookup"><span data-stu-id="630a5-108">Simplified Message Functions</span></span>](#simplified-message-functions)
-   [<span data-ttu-id="630a5-109">Fonctions de message de bas niveau</span><span class="sxs-lookup"><span data-stu-id="630a5-109">Low-level Message Functions</span></span>](#low-level-message-functions)

## <a name="base-cryptographic-functions"></a><span data-ttu-id="630a5-110">Fonctions de chiffrement de base</span><span class="sxs-lookup"><span data-stu-id="630a5-110">Base Cryptographic Functions</span></span>

-   <span data-ttu-id="630a5-111">*Fonctions de contexte* utilisées pour se connecter à un CSP.</span><span class="sxs-lookup"><span data-stu-id="630a5-111">*Context functions* used to connect to a CSP.</span></span> <span data-ttu-id="630a5-112">Ces fonctions permettent aux applications de choisir un CSP spécifique par nom ou de choisir un CSP spécifique qui peut fournir une classe de fonctionnalité nécessaire.</span><span class="sxs-lookup"><span data-stu-id="630a5-112">These functions enable applications to choose a specific CSP by name or to choose a specific CSP that can provide a needed class of functionality.</span></span>
-   <span data-ttu-id="630a5-113">[*Fonctions de génération de clés*](../secgloss/k-gly.md) utilisées pour générer et stocker des [*clés de chiffrement*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="630a5-113">[*Key generation functions*](../secgloss/k-gly.md) used to generate and store [*cryptographic keys*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="630a5-114">La prise en charge complète est incluse pour la modification des [*modes de chaînage*](../secgloss/c-gly.md), des [*vecteurs d’initialisation*](../secgloss/i-gly.md)et d’autres fonctionnalités de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="630a5-114">Full support is included for changing [*chaining modes*](../secgloss/c-gly.md), [*initialization vectors*](../secgloss/i-gly.md), and other encryption features.</span></span> <span data-ttu-id="630a5-115">Pour plus d’informations, consultez [génération de clés et fonctions d’échange](cryptography-functions.md).</span><span class="sxs-lookup"><span data-stu-id="630a5-115">For more information, see [Key Generation and Exchange Functions](cryptography-functions.md).</span></span>
-   <span data-ttu-id="630a5-116">*Fonctions d’échange de clés* utilisées pour échanger ou transmettre des clés.</span><span class="sxs-lookup"><span data-stu-id="630a5-116">*Key exchange functions* used to exchange or transmit keys.</span></span> <span data-ttu-id="630a5-117">Pour plus d’informations, consultez [stockage de clé de chiffrement et Exchange](cryptographic-key-storage-and-exchange.md) , [génération de clés et fonctions Exchange](cryptography-functions.md).</span><span class="sxs-lookup"><span data-stu-id="630a5-117">For more information, see [Cryptographic Key Storage and Exchange](cryptographic-key-storage-and-exchange.md) and [Key Generation and Exchange Functions](cryptography-functions.md).</span></span>

## <a name="certificate-encodedecode-functions"></a><span data-ttu-id="630a5-118">Fonctions de codage/décodage de certificat</span><span class="sxs-lookup"><span data-stu-id="630a5-118">Certificate Encode/Decode Functions</span></span>

-   <span data-ttu-id="630a5-119">Fonctions utilisées pour chiffrer ou déchiffrer des données.</span><span class="sxs-lookup"><span data-stu-id="630a5-119">Functions used to encrypt or decrypt data.</span></span> <span data-ttu-id="630a5-120">La prise en charge est également incluse pour le [*hachage*](../secgloss/h-gly.md) des données.</span><span class="sxs-lookup"><span data-stu-id="630a5-120">Support is also included for [*hashing*](../secgloss/h-gly.md) data.</span></span> <span data-ttu-id="630a5-121">Pour plus d’informations, consultez [fonctions de chiffrement et](cryptography-functions.md) de déchiffrement des données et [chiffrement et déchiffrement des données](data-encryption-and-decryption.md).</span><span class="sxs-lookup"><span data-stu-id="630a5-121">For more information, see [Data Encryption and Decryption Functions](cryptography-functions.md) and [Data Encryption and Decryption](data-encryption-and-decryption.md).</span></span>

## <a name="certificate-store-functions"></a><span data-ttu-id="630a5-122">Fonctions du magasin de certificats</span><span class="sxs-lookup"><span data-stu-id="630a5-122">Certificate Store Functions</span></span>

-   <span data-ttu-id="630a5-123">Fonctions utilisées pour gérer les collections de certificats numériques.</span><span class="sxs-lookup"><span data-stu-id="630a5-123">Functions used to manage collections of digital certificates.</span></span> <span data-ttu-id="630a5-124">Pour plus d’informations, consultez [certificats numériques](digital-certificates.md) et [fonctions du magasin de certificats](cryptography-functions.md).</span><span class="sxs-lookup"><span data-stu-id="630a5-124">For more information, see [Digital Certificates](digital-certificates.md) and [Certificate Store Functions](cryptography-functions.md).</span></span>

## <a name="simplified-message-functions"></a><span data-ttu-id="630a5-125">Fonctions de message simplifiées</span><span class="sxs-lookup"><span data-stu-id="630a5-125">Simplified Message Functions</span></span>

-   <span data-ttu-id="630a5-126">Fonctions utilisées pour chiffrer et déchiffrer les messages et les données.</span><span class="sxs-lookup"><span data-stu-id="630a5-126">Functions used to encrypt and decrypt messages and data.</span></span>
-   <span data-ttu-id="630a5-127">Fonctions utilisées pour signer les messages et les données.</span><span class="sxs-lookup"><span data-stu-id="630a5-127">Functions used to sign messages and data.</span></span>
-   <span data-ttu-id="630a5-128">Fonctions utilisées pour vérifier l’authenticité des signatures sur les messages reçus et les données associées.</span><span class="sxs-lookup"><span data-stu-id="630a5-128">Functions used to verify the authenticity of signatures on received messages and related data.</span></span>

<span data-ttu-id="630a5-129">Pour plus d’informations, consultez [messages simplifiés](simplified-messages.md) et [fonctions de message simplifiées](cryptography-functions.md).</span><span class="sxs-lookup"><span data-stu-id="630a5-129">For more information, see [Simplified Messages](simplified-messages.md) and [Simplified Message Functions](cryptography-functions.md).</span></span>

## <a name="low-level-message-functions"></a><span data-ttu-id="630a5-130">Fonctions de message de bas niveau</span><span class="sxs-lookup"><span data-stu-id="630a5-130">Low-level Message Functions</span></span>

-   <span data-ttu-id="630a5-131">Fonctions utilisées pour effectuer toutes les tâches effectuées par les fonctions de message simplifiées.</span><span class="sxs-lookup"><span data-stu-id="630a5-131">Functions used to perform all of the tasks performed by the simplified message functions.</span></span> <span data-ttu-id="630a5-132">Les fonctions de message de bas niveau offrent plus de flexibilité que les fonctions de message simplifiées, mais nécessitent davantage d’appels de fonction.</span><span class="sxs-lookup"><span data-stu-id="630a5-132">The low-level message functions provide more flexibility than the simplified message functions but require more function calls.</span></span> <span data-ttu-id="630a5-133">Pour plus d’informations, consultez [messages de bas niveau](low-level-messages.md) et [fonctions de message de bas niveau](cryptography-functions.md).</span><span class="sxs-lookup"><span data-stu-id="630a5-133">For more information, see [Low-level Messages](low-level-messages.md) and [Low-level Message Functions](cryptography-functions.md).</span></span>

![architecture CryptoAPI](images/cryparch.png)

<span data-ttu-id="630a5-135">Chacune des zones fonctionnelles a un mot clé dans son nom de fonction qui indique sa zone fonctionnelle.</span><span class="sxs-lookup"><span data-stu-id="630a5-135">Each of the functional areas has a key word in its function name that indicates its functional area.</span></span>



| <span data-ttu-id="630a5-136">Zone fonctionnelle</span><span class="sxs-lookup"><span data-stu-id="630a5-136">Functional area</span></span>              | <span data-ttu-id="630a5-137">Convention de nom de fonction</span><span class="sxs-lookup"><span data-stu-id="630a5-137">Function name convention</span></span> |
|------------------------------|--------------------------|
| <span data-ttu-id="630a5-138">Fonctions de chiffrement de base</span><span class="sxs-lookup"><span data-stu-id="630a5-138">Base cryptographic functions</span></span> | <span data-ttu-id="630a5-139">Compliqué</span><span class="sxs-lookup"><span data-stu-id="630a5-139">Crypt</span></span>                    |
| <span data-ttu-id="630a5-140">Fonctions d’encodage/décodage</span><span class="sxs-lookup"><span data-stu-id="630a5-140">Encoding/decoding functions</span></span>  | <span data-ttu-id="630a5-141">Compliqué</span><span class="sxs-lookup"><span data-stu-id="630a5-141">Crypt</span></span>                    |
| <span data-ttu-id="630a5-142">Fonctions du magasin de certificats</span><span class="sxs-lookup"><span data-stu-id="630a5-142">Certificate store functions</span></span>  | <span data-ttu-id="630a5-143">Magasin</span><span class="sxs-lookup"><span data-stu-id="630a5-143">Store</span></span>                    |
| <span data-ttu-id="630a5-144">Fonctions de message simplifiées</span><span class="sxs-lookup"><span data-stu-id="630a5-144">Simplified message functions</span></span> | <span data-ttu-id="630a5-145">Message</span><span class="sxs-lookup"><span data-stu-id="630a5-145">Message</span></span>                  |
| <span data-ttu-id="630a5-146">Fonctions de message de bas niveau</span><span class="sxs-lookup"><span data-stu-id="630a5-146">Low-level message functions</span></span>  | <span data-ttu-id="630a5-147">Fragment</span><span class="sxs-lookup"><span data-stu-id="630a5-147">Msg</span></span>                      |



 

<span data-ttu-id="630a5-148">Les applications utilisent des fonctions dans tous ces domaines.</span><span class="sxs-lookup"><span data-stu-id="630a5-148">Applications use functions in all of these areas.</span></span> <span data-ttu-id="630a5-149">Ces fonctions, prises ensemble, composent CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="630a5-149">These functions, taken together, make up CryptoAPI.</span></span> <span data-ttu-id="630a5-150">Les [*fonctions de chiffrement de base*](../secgloss/b-gly.md) utilisent les CSP pour les algorithmes de chiffrement nécessaires et pour la génération et le stockage sécurisé des [clés de chiffrement](cryptographic-keys.md).</span><span class="sxs-lookup"><span data-stu-id="630a5-150">The [*base cryptographic functions*](../secgloss/b-gly.md) use the CSPs for the necessary cryptographic algorithms and for the generation and secure storage of [cryptographic keys](cryptographic-keys.md).</span></span>

<span data-ttu-id="630a5-151">Deux types de clés de chiffrement sont utilisés : les [*clés de session*](../secgloss/s-gly.md), qui sont utilisées pour un chiffrement/déchiffrement unique, et les [*paires de clés publique/privée*](../secgloss/p-gly.md), qui sont utilisées de façon plus permanente.</span><span class="sxs-lookup"><span data-stu-id="630a5-151">Two different kinds of cryptographic keys are used: [*session keys*](../secgloss/s-gly.md), which are used for a single encryption/decryption, and [*public/private key pairs*](../secgloss/p-gly.md), which are used on a more permanent basis.</span></span>

> [!Note]  
> <span data-ttu-id="630a5-152">Bien qu’une application puisse communiquer directement avec l’une des cinq zones fonctionnelles, elle ne peut pas communiquer directement avec un CSP.</span><span class="sxs-lookup"><span data-stu-id="630a5-152">Although an application can communicate directly with any of the five functional areas, it cannot communicate directly with a CSP.</span></span> <span data-ttu-id="630a5-153">Toutes les communications entre les applications et CSP se produisent par le biais des [*fonctions de chiffrement de base*](../secgloss/b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="630a5-153">All application-to-CSP communications occur through the [*base cryptographic functions*](../secgloss/b-gly.md).</span></span> <span data-ttu-id="630a5-154">Les fonctions de chiffrement de base ont un paramètre qui spécifie le fournisseur de services de chiffrement à utiliser.</span><span class="sxs-lookup"><span data-stu-id="630a5-154">Base cryptographic functions have a parameter that specifies which CSP to use.</span></span> <span data-ttu-id="630a5-155">Ce paramètre peut avoir la valeur **null** pour sélectionner un CSP par défaut.</span><span class="sxs-lookup"><span data-stu-id="630a5-155">This parameter can be set to **NULL** to select a default CSP.</span></span>

 

 

 
