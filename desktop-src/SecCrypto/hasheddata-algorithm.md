---
description: Définit ou récupère le type d’algorithme de hachage utilisé.
ms.assetid: 3f8e83f2-0e46-494b-ac63-658e663680ea
title: HashedData. algorithme, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HashedData.Algorithm
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a27dc275ce900bfd6412599cb81ad14038f96405
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543787"
---
# <a name="hasheddataalgorithm-property"></a><span data-ttu-id="6fa11-103">HashedData. algorithme, propriété</span><span class="sxs-lookup"><span data-stu-id="6fa11-103">HashedData.Algorithm property</span></span>

<span data-ttu-id="6fa11-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6fa11-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="6fa11-105">Utilisez plutôt la [**classe HashAlgorithm**](/previous-versions/windows/) dans l’espace de noms [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="6fa11-105">Instead, use the [**HashAlgorithm Class**](/previous-versions/windows/) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="6fa11-106">La propriété de l' **algorithme** définit ou récupère le type d’algorithme de hachage utilisé.</span><span class="sxs-lookup"><span data-stu-id="6fa11-106">The **Algorithm** property sets or retrieves the type of hashing algorithm used.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fa11-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6fa11-107">Syntax</span></span>


```VB
HashedData.Algorithm As CAPICOM_HASH_ALGORITHM
```



## <a name="property-value"></a><span data-ttu-id="6fa11-108">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="6fa11-108">Property value</span></span>

<span data-ttu-id="6fa11-109">Valeur de l’énumération de l' [**\_ \_ algorithme de hachage CAPICOM**](capicom-hash-algorithm.md) qui définit un algorithme de hachage.</span><span class="sxs-lookup"><span data-stu-id="6fa11-109">A value of the [**CAPICOM\_HASH\_ALGORITHM**](capicom-hash-algorithm.md) enumeration that defines a hash algorithm.</span></span> <span data-ttu-id="6fa11-110">La valeur par défaut est CAPICOM \_ hash \_ Algorithm \_ SHA1.</span><span class="sxs-lookup"><span data-stu-id="6fa11-110">The default value is CAPICOM\_HASH\_ALGORITHM\_SHA1.</span></span> <span data-ttu-id="6fa11-111">Le tableau suivant répertorie les valeurs possibles.</span><span class="sxs-lookup"><span data-stu-id="6fa11-111">The following table shows the possible values.</span></span>



| <span data-ttu-id="6fa11-112">Value</span><span class="sxs-lookup"><span data-stu-id="6fa11-112">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="6fa11-113">Signification</span><span class="sxs-lookup"><span data-stu-id="6fa11-113">Meaning</span></span>                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_HASH_ALGORITHM_SHA1"></span><span id="capicom_hash_algorithm_sha1"></span><dl> <span data-ttu-id="6fa11-114"><dt>**\_Algorithme de hachage \_ CAPICOM \_ SHA1**</dt></span><span class="sxs-lookup"><span data-stu-id="6fa11-114"><dt>**CAPICOM\_HASH\_ALGORITHM\_SHA1**</dt></span></span> </dl>           | <span data-ttu-id="6fa11-115">Algorithme de hachage SHA1.</span><span class="sxs-lookup"><span data-stu-id="6fa11-115">SHA1 hashing algorithm.</span></span><br/>                                                                          |
| <span id="CAPICOM_HASH_ALGORITHM_MD2"></span><span id="capicom_hash_algorithm_md2"></span><dl> <span data-ttu-id="6fa11-116"><dt>**MD2 de l' \_ algorithme de hachage CAPICOM \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6fa11-116"><dt>**CAPICOM\_HASH\_ALGORITHM\_MD2**</dt></span></span> </dl>              | <span data-ttu-id="6fa11-117">Algorithme de hachage MD2.</span><span class="sxs-lookup"><span data-stu-id="6fa11-117">MD2 hashing algorithm.</span></span><br/>                                                                           |
| <span id="CAPICOM_HASH_ALGORITHM_MD4"></span><span id="capicom_hash_algorithm_md4"></span><dl> <span data-ttu-id="6fa11-118"><dt>**\_Algorithme de hachage \_ CAPICOM \_ MD4**</dt></span><span class="sxs-lookup"><span data-stu-id="6fa11-118"><dt>**CAPICOM\_HASH\_ALGORITHM\_MD4**</dt></span></span> </dl>              | <span data-ttu-id="6fa11-119">Algorithme de hachage MD4.</span><span class="sxs-lookup"><span data-stu-id="6fa11-119">MD4 hashing algorithm.</span></span><br/>                                                                           |
| <span id="CAPICOM_HASH_ALGORITHM_MD5"></span><span id="capicom_hash_algorithm_md5"></span><dl> <span data-ttu-id="6fa11-120"><dt>**\_Algorithme de hachage \_ CAPICOM \_ MD5**</dt></span><span class="sxs-lookup"><span data-stu-id="6fa11-120"><dt>**CAPICOM\_HASH\_ALGORITHM\_MD5**</dt></span></span> </dl>              | <span data-ttu-id="6fa11-121">Algorithme de hachage MD5.</span><span class="sxs-lookup"><span data-stu-id="6fa11-121">MD5 hashing algorithm.</span></span><br/>                                                                           |
| <span id="CAPICOM_HASH_ALGORITHM_SHA_256"></span><span id="capicom_hash_algorithm_sha_256"></span><dl> <span data-ttu-id="6fa11-122"><dt>**\_Algorithme de hachage \_ capicom \_ SHA \_ 256**</dt></span><span class="sxs-lookup"><span data-stu-id="6fa11-122"><dt>**CAPICOM\_HASH\_ALGORITHM\_SHA\_256**</dt></span></span> </dl> | <span data-ttu-id="6fa11-123">Algorithme de hachage SHA-256.</span><span class="sxs-lookup"><span data-stu-id="6fa11-123">SHA-256 hash algorithm.</span></span><br/> <span data-ttu-id="6fa11-124">**CAPICOM 2.0.0.3 et versions antérieures :** Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="6fa11-124">**CAPICOM 2.0.0.3 and earlier:** This value is not supported.</span></span><br/> |
| <span id="CAPICOM_HASH_ALGORITHM_SHA_384"></span><span id="capicom_hash_algorithm_sha_384"></span><dl> <span data-ttu-id="6fa11-125"><dt>**\_Algorithme de hachage \_ capicom \_ SHA \_ 384**</dt></span><span class="sxs-lookup"><span data-stu-id="6fa11-125"><dt>**CAPICOM\_HASH\_ALGORITHM\_SHA\_384**</dt></span></span> </dl> | <span data-ttu-id="6fa11-126">Algorithme de hachage SHA-384.</span><span class="sxs-lookup"><span data-stu-id="6fa11-126">SHA-384 hash algorithm.</span></span><br/> <span data-ttu-id="6fa11-127">**CAPICOM 2.0.0.3 et versions antérieures :** Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="6fa11-127">**CAPICOM 2.0.0.3 and earlier:** This value is not supported.</span></span><br/> |
| <span id="CAPICOM_HASH_ALGORITHM_SHA_512"></span><span id="capicom_hash_algorithm_sha_512"></span><dl> <span data-ttu-id="6fa11-128"><dt>**\_Algorithme de hachage \_ capicom \_ SHA \_ 512**</dt></span><span class="sxs-lookup"><span data-stu-id="6fa11-128"><dt>**CAPICOM\_HASH\_ALGORITHM\_SHA\_512**</dt></span></span> </dl> | <span data-ttu-id="6fa11-129">Algorithme de hachage SHA-512.</span><span class="sxs-lookup"><span data-stu-id="6fa11-129">SHA-512 hash algorithm.</span></span><br/> <span data-ttu-id="6fa11-130">**CAPICOM 2.0.0.3 et versions antérieures :** Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="6fa11-130">**CAPICOM 2.0.0.3 and earlier:** This value is not supported.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6fa11-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6fa11-131">Requirements</span></span>



| <span data-ttu-id="6fa11-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6fa11-132">Requirement</span></span> | <span data-ttu-id="6fa11-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="6fa11-133">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6fa11-134">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="6fa11-134">End of client support</span></span><br/> | <span data-ttu-id="6fa11-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6fa11-135">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="6fa11-136">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="6fa11-136">End of server support</span></span><br/> | <span data-ttu-id="6fa11-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6fa11-137">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="6fa11-138">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="6fa11-138">Redistributable</span></span><br/>       | <span data-ttu-id="6fa11-139">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="6fa11-139">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="6fa11-140">DLL</span><span class="sxs-lookup"><span data-stu-id="6fa11-140">DLL</span></span><br/>                   | <dl> <span data-ttu-id="6fa11-141"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6fa11-141"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fa11-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6fa11-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fa11-143">**HashedData**</span><span class="sxs-lookup"><span data-stu-id="6fa11-143">**HashedData**</span></span>](hasheddata.md)
</dt> </dl>

 

 
