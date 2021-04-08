---
description: Prend en charge les signatures numériques et le chiffrement des données. Il est considéré comme un fournisseur de services de chiffrement à usage général (CSP).
ms.assetid: da0b50ec-25a6-40dd-af83-73500b4a4c08
title: PROV_RSA_AES
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1fa8d01e9fd212f2c39ab5615b12931738bc926
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034942"
---
# <a name="prov_rsa_aes"></a><span data-ttu-id="ec632-104">\_RSA \_ AES Prov.</span><span class="sxs-lookup"><span data-stu-id="ec632-104">PROV\_RSA\_AES</span></span>

<span data-ttu-id="ec632-105">Le \_ type de \_ fournisseur RSA AES Prov prend en charge les [signatures numériques](digital-signatures.md) et le chiffrement des données.</span><span class="sxs-lookup"><span data-stu-id="ec632-105">The PROV\_RSA\_AES provider type supports both [digital signatures](digital-signatures.md) and data encryption.</span></span> <span data-ttu-id="ec632-106">Il est considéré comme un [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) à usage général (CSP).</span><span class="sxs-lookup"><span data-stu-id="ec632-106">It is considered a general purpose [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span> <span data-ttu-id="ec632-107">L' [*algorithme de clé publique*](../secgloss/p-gly.md) RSA est utilisé pour toutes les opérations de [*clé publique*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="ec632-107">The RSA [*public key algorithm*](../secgloss/p-gly.md) is used for all [*public key*](../secgloss/p-gly.md) operations.</span></span>

## <a name="algorithms-supported"></a><span data-ttu-id="ec632-108">Algorithmes pris en charge</span><span class="sxs-lookup"><span data-stu-id="ec632-108">Algorithms Supported</span></span>

<span data-ttu-id="ec632-109">Pour obtenir une description de chacun de ces algorithmes, consultez le Glossaire.</span><span class="sxs-lookup"><span data-stu-id="ec632-109">For descriptions of each of these algorithms, see the glossary.</span></span>



| <span data-ttu-id="ec632-110">Objectif</span><span class="sxs-lookup"><span data-stu-id="ec632-110">Purpose</span></span>      | <span data-ttu-id="ec632-111">Algorithmes pris en charge</span><span class="sxs-lookup"><span data-stu-id="ec632-111">Supported algorithms</span></span>                                                                                                                                                                                                                                                                                       |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec632-112">Échange de clés</span><span class="sxs-lookup"><span data-stu-id="ec632-112">Key Exchange</span></span> | [<span data-ttu-id="ec632-113">*RSA*</span><span class="sxs-lookup"><span data-stu-id="ec632-113">*RSA*</span></span>](../secgloss/r-gly.md)<br/>                                                                                                                                                                                                                                     |
| <span data-ttu-id="ec632-114">Signature</span><span class="sxs-lookup"><span data-stu-id="ec632-114">Signature</span></span>    | [<span data-ttu-id="ec632-115">*RSA*</span><span class="sxs-lookup"><span data-stu-id="ec632-115">*RSA*</span></span>](../secgloss/r-gly.md)<br/>                                                                                                                                                                                                                                     |
| <span data-ttu-id="ec632-116">Chiffrement</span><span class="sxs-lookup"><span data-stu-id="ec632-116">Encryption</span></span>   | [<span data-ttu-id="ec632-117">*RC2*</span><span class="sxs-lookup"><span data-stu-id="ec632-117">*RC2*</span></span>](../secgloss/r-gly.md)<br/> [<span data-ttu-id="ec632-118">*RC4*</span><span class="sxs-lookup"><span data-stu-id="ec632-118">*RC4*</span></span>](../secgloss/r-gly.md)<br/> <span data-ttu-id="ec632-119">[*Advanced Encryption Standard*](../secgloss/a-gly.md) (AES)</span><span class="sxs-lookup"><span data-stu-id="ec632-119">[*Advanced Encryption Standard*](../secgloss/a-gly.md) (AES)</span></span> <br/>                                                       |
| <span data-ttu-id="ec632-120">Hashing</span><span class="sxs-lookup"><span data-stu-id="ec632-120">Hashing</span></span>      | [<span data-ttu-id="ec632-121">*MD2*</span><span class="sxs-lookup"><span data-stu-id="ec632-121">*MD2*</span></span>](../secgloss/m-gly.md)<br/> [<span data-ttu-id="ec632-122">*MD4*</span><span class="sxs-lookup"><span data-stu-id="ec632-122">*MD4*</span></span>](../secgloss/m-gly.md)<br/> [<span data-ttu-id="ec632-123">*MD5*</span><span class="sxs-lookup"><span data-stu-id="ec632-123">*MD5*</span></span>](../secgloss/m-gly.md)<br/> [<span data-ttu-id="ec632-124">*SHA-1*</span><span class="sxs-lookup"><span data-stu-id="ec632-124">*SHA-1*</span></span>](../secgloss/s-gly.md)<br/> <span data-ttu-id="ec632-125">SHA-2 (SHA-256, SHA-384 et SHA-512)</span><span class="sxs-lookup"><span data-stu-id="ec632-125">SHA-2 (SHA-256, SHA-384, and SHA-512)</span></span><br/> |



 

## <a name="related-documentation"></a><span data-ttu-id="ec632-126">Documentations associées</span><span class="sxs-lookup"><span data-stu-id="ec632-126">Related Documentation</span></span>

<span data-ttu-id="ec632-127">Ce type de fournisseur est défini par Microsoft et RSA Data Security.</span><span class="sxs-lookup"><span data-stu-id="ec632-127">This provider type is defined by Microsoft and RSA Data Security.</span></span> <span data-ttu-id="ec632-128">Il est décrit dans les documents suivants :</span><span class="sxs-lookup"><span data-stu-id="ec632-128">It is described in the following documents:</span></span>

-   <span data-ttu-id="ec632-129">*Guide du programmeur du fournisseur de services de chiffrement Microsoft*, microsoft, 1996.</span><span class="sxs-lookup"><span data-stu-id="ec632-129">*Microsoft Cryptographic Service Provider Programmer's Guide*, Microsoft, 1996.</span></span>
-   <span data-ttu-id="ec632-130">RSA Laboratories, normes de chiffrement à clé publique, RSA Data Security, novembre 1993.</span><span class="sxs-lookup"><span data-stu-id="ec632-130">RSA Laboratories, Public Key Cryptography Standards, RSA Data Security, November 1993.</span></span>

> [!Note]  
> <span data-ttu-id="ec632-131">Ces ressources peuvent ne pas être disponibles dans certaines langues et dans certains pays ou régions.</span><span class="sxs-lookup"><span data-stu-id="ec632-131">These resources may not be available in some languages and countries or regions.</span></span>

 

 

 
