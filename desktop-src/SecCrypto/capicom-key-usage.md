---
description: L’énumération de l’utilisation de la \_ clé CAPICOM \_ définit la manière dont une clé peut être utilisée. Introduit dans CAPICOM 2,0.
ms.assetid: 7143567b-5882-44a3-ae30-fb8965fb7997
title: Énumération CAPICOM_KEY_USAGE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_KEY_USAGE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 1d44c7f3ecf35ddeb55dd96e5513261691010990
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533048"
---
# <a name="capicom_key_usage-enumeration"></a><span data-ttu-id="b02ce-104">\_ \_ Énumération de l’utilisation de la clé CAPICOM</span><span class="sxs-lookup"><span data-stu-id="b02ce-104">CAPICOM\_KEY\_USAGE enumeration</span></span>

<span data-ttu-id="b02ce-105">L’énumération de l' **\_ \_ utilisation de la clé CAPICOM** définit la manière dont une clé peut être utilisée.</span><span class="sxs-lookup"><span data-stu-id="b02ce-105">The **CAPICOM\_KEY\_USAGE** enumeration defines the ways in which a key can be used.</span></span> <span data-ttu-id="b02ce-106">Introduit dans CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="b02ce-106">Introduced in CAPICOM 2.0.</span></span>

## <a name="members"></a><span data-ttu-id="b02ce-107">Membres</span><span class="sxs-lookup"><span data-stu-id="b02ce-107">Members</span></span>



| <span data-ttu-id="b02ce-108">Membre</span><span class="sxs-lookup"><span data-stu-id="b02ce-108">Member</span></span>                                      | <span data-ttu-id="b02ce-109">Description</span><span class="sxs-lookup"><span data-stu-id="b02ce-109">Description</span></span>                                                                                                                      | <span data-ttu-id="b02ce-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="b02ce-110">Value</span></span>      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|------------|
| <span data-ttu-id="b02ce-111">**utilisation de la \_ \_ clé de signature numérique \_ CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="b02ce-111">**CAPICOM\_DIGITAL\_SIGNATURE\_KEY\_USAGE**</span></span> | <span data-ttu-id="b02ce-112">La clé peut être utilisée pour créer une signature numérique.</span><span class="sxs-lookup"><span data-stu-id="b02ce-112">The key can be used to create a digital signature.</span></span><br/>                                                                    | <span data-ttu-id="b02ce-113">0x00000080</span><span class="sxs-lookup"><span data-stu-id="b02ce-113">0x00000080</span></span> |
| <span data-ttu-id="b02ce-114">**utilisation de la \_ clé de non- \_ RÉPUDIation CAPICOM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b02ce-114">**CAPICOM\_NON\_REPUDIATION\_KEY\_USAGE**</span></span>   | <span data-ttu-id="b02ce-115">La clé peut être utilisée pour la non- [*répudiation*](../secgloss/n-gly.md).</span><span class="sxs-lookup"><span data-stu-id="b02ce-115">The key can be used for [*nonrepudiation*](../secgloss/n-gly.md).</span></span><br/> | <span data-ttu-id="b02ce-116">0x00000040</span><span class="sxs-lookup"><span data-stu-id="b02ce-116">0x00000040</span></span> |
| <span data-ttu-id="b02ce-117">**utilisation de la \_ \_ clé de chiffrement de la clé CAPICOM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b02ce-117">**CAPICOM\_KEY\_ENCIPHERMENT\_KEY\_USAGE**</span></span>  | <span data-ttu-id="b02ce-118">La clé peut être utilisée pour chiffrer une clé.</span><span class="sxs-lookup"><span data-stu-id="b02ce-118">The key can be used to encrypt a key.</span></span><br/>                                                                                 | <span data-ttu-id="b02ce-119">0x00000020</span><span class="sxs-lookup"><span data-stu-id="b02ce-119">0x00000020</span></span> |
| <span data-ttu-id="b02ce-120">**utilisation de la \_ \_ clé de chiffrement des données CAPICOM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b02ce-120">**CAPICOM\_DATA\_ENCIPHERMENT\_KEY\_USAGE**</span></span> | <span data-ttu-id="b02ce-121">La clé peut être utilisée pour chiffrer les données.</span><span class="sxs-lookup"><span data-stu-id="b02ce-121">The key can be used to encrypt data.</span></span><br/>                                                                                  | <span data-ttu-id="b02ce-122">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b02ce-122">0x00000010</span></span> |
| <span data-ttu-id="b02ce-123">**utilisation de la \_ \_ clé de \_ \_ l’accord de clé CAPICOM**</span><span class="sxs-lookup"><span data-stu-id="b02ce-123">**CAPICOM\_KEY\_AGREEMENT\_KEY\_USAGE**</span></span>     | <span data-ttu-id="b02ce-124">La clé peut être utilisée pour l’accord de clé.</span><span class="sxs-lookup"><span data-stu-id="b02ce-124">The key can be used for key agreement.</span></span><br/>                                                                                | <span data-ttu-id="b02ce-125">0x00000008</span><span class="sxs-lookup"><span data-stu-id="b02ce-125">0x00000008</span></span> |
| <span data-ttu-id="b02ce-126">**utilisation de la \_ \_ clé de \_ signature du certificat \_ de clé \_ CAPICOM**</span><span class="sxs-lookup"><span data-stu-id="b02ce-126">**CAPICOM\_KEY\_CERT\_SIGN\_KEY\_USAGE**</span></span>    | <span data-ttu-id="b02ce-127">La clé peut être utilisée pour la signature de certificat de clé.</span><span class="sxs-lookup"><span data-stu-id="b02ce-127">The key can be used for key certificate signing.</span></span> <span data-ttu-id="b02ce-128">Cette valeur est équivalente à \_ l’utilisation de la \_ clé de signature de la liste de révocation de certificats en mode hors connexion \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="b02ce-128">This value is equivalent to CAPICOM\_OFFLINE\_CRL\_SIGN\_KEY\_USAGE.</span></span><br/> | <span data-ttu-id="b02ce-129">0x00000004</span><span class="sxs-lookup"><span data-stu-id="b02ce-129">0x00000004</span></span> |
| <span data-ttu-id="b02ce-130">**\_ \_ utilisation de la clé de signature de la liste de révocation de certificats hors connexion CAPICOM \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b02ce-130">**CAPICOM\_OFFLINE\_CRL\_SIGN\_KEY\_USAGE**</span></span> | <span data-ttu-id="b02ce-131">La clé peut être utilisée pour la signature de certificat de clé.</span><span class="sxs-lookup"><span data-stu-id="b02ce-131">The key can be used for key certificate signing.</span></span> <span data-ttu-id="b02ce-132">Cette valeur est équivalente à l’utilisation de la \_ clé de signature du certificat de clé CAPICOM \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="b02ce-132">This value is equivalent to CAPICOM\_KEY\_CERT\_SIGN\_KEY\_USAGE.</span></span><br/>    | <span data-ttu-id="b02ce-133">0x00000002</span><span class="sxs-lookup"><span data-stu-id="b02ce-133">0x00000002</span></span> |
| <span data-ttu-id="b02ce-134">**\_utilisation de la \_ clé de signature de la liste de révocation de certificats CAPICOM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b02ce-134">**CAPICOM\_CRL\_SIGN\_KEY\_USAGE**</span></span>          | <span data-ttu-id="b02ce-135">La clé peut être utilisée pour la signature.</span><span class="sxs-lookup"><span data-stu-id="b02ce-135">The key can be used for signing.</span></span><br/>                                                                                      | <span data-ttu-id="b02ce-136">0x00000002</span><span class="sxs-lookup"><span data-stu-id="b02ce-136">0x00000002</span></span> |
| <span data-ttu-id="b02ce-137">**utilisation de la \_ clé d’ENchiffrement CAPICOM \_ uniquement \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b02ce-137">**CAPICOM\_ENCIPHER\_ONLY\_KEY\_USAGE**</span></span>     | <span data-ttu-id="b02ce-138">La clé peut uniquement être utilisée pour chiffrer.</span><span class="sxs-lookup"><span data-stu-id="b02ce-138">The key can only be used to encrypt.</span></span><br/>                                                                                  | <span data-ttu-id="b02ce-139">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b02ce-139">0x00000001</span></span> |
| <span data-ttu-id="b02ce-140">**l’utilisation de la clé pour le \_ déchiffrement de CAPICOM \_ uniquement \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b02ce-140">**CAPICOM\_DECIPHER\_ONLY\_KEY\_USAGE**</span></span>     | <span data-ttu-id="b02ce-141">La clé ne peut être utilisée que pour le déchiffrement.</span><span class="sxs-lookup"><span data-stu-id="b02ce-141">The key can only be used to decrypt.</span></span><br/>                                                                                  | <span data-ttu-id="b02ce-142">0x00008000</span><span class="sxs-lookup"><span data-stu-id="b02ce-142">0x00008000</span></span> |



## <a name="requirements"></a><span data-ttu-id="b02ce-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b02ce-143">Requirements</span></span>



| <span data-ttu-id="b02ce-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b02ce-144">Requirement</span></span> | <span data-ttu-id="b02ce-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="b02ce-145">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b02ce-146">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="b02ce-146">Redistributable</span></span><br/> | <span data-ttu-id="b02ce-147">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="b02ce-147">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="b02ce-148">En-tête</span><span class="sxs-lookup"><span data-stu-id="b02ce-148">Header</span></span><br/>          | <dl> <span data-ttu-id="b02ce-149"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="b02ce-149"><dt>Capicom.h</dt></span></span> </dl> |



 

 
