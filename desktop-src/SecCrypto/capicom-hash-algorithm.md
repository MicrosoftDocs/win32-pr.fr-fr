---
description: L' \_ \_ énumération de l’algorithme de hachage CAPICOM définit un algorithme de hachage.
ms.assetid: 5373b6cc-944a-4d83-ac71-59edcb2af94e
title: Énumération CAPICOM_HASH_ALGORITHM (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_HASH_ALGORITHM
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 14ee06437f7b6e32c58415e5b9d77a75929250a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534980"
---
# <a name="capicom_hash_algorithm-enumeration"></a><span data-ttu-id="93b1f-103">\_Énumération de l' \_ algorithme de hachage CAPICOM</span><span class="sxs-lookup"><span data-stu-id="93b1f-103">CAPICOM\_HASH\_ALGORITHM enumeration</span></span>

<span data-ttu-id="93b1f-104">L’énumération de l' **\_ \_ algorithme de hachage CAPICOM** définit un algorithme de hachage.</span><span class="sxs-lookup"><span data-stu-id="93b1f-104">The **CAPICOM\_HASH\_ALGORITHM** enumeration defines a hash algorithm.</span></span>

## <a name="members"></a><span data-ttu-id="93b1f-105">Membres</span><span class="sxs-lookup"><span data-stu-id="93b1f-105">Members</span></span>



| <span data-ttu-id="93b1f-106">Membre</span><span class="sxs-lookup"><span data-stu-id="93b1f-106">Member</span></span>                                 | <span data-ttu-id="93b1f-107">Description</span><span class="sxs-lookup"><span data-stu-id="93b1f-107">Description</span></span>                                                                                                                                                                 | <span data-ttu-id="93b1f-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="93b1f-108">Value</span></span> |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="93b1f-109">**\_Algorithme de hachage \_ CAPICOM \_ SHA1**</span><span class="sxs-lookup"><span data-stu-id="93b1f-109">**CAPICOM\_HASH\_ALGORITHM\_SHA1**</span></span>     | <span data-ttu-id="93b1f-110">[*Algorithme de hachage sécurisé*](../secgloss/s-gly.md) (SHA) qui génère un résumé de message 160 bits.</span><span class="sxs-lookup"><span data-stu-id="93b1f-110">[*Secure Hash Algorithm*](../secgloss/s-gly.md) (SHA) that generates a 160-bit message digest.</span></span><br/> | <span data-ttu-id="93b1f-111">0</span><span class="sxs-lookup"><span data-stu-id="93b1f-111">0</span></span>     |
| <span data-ttu-id="93b1f-112">**MD2 de l' \_ algorithme de hachage CAPICOM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="93b1f-112">**CAPICOM\_HASH\_ALGORITHM\_MD2**</span></span>      | <span data-ttu-id="93b1f-113">Algorithme de hachage MD2.</span><span class="sxs-lookup"><span data-stu-id="93b1f-113">MD2 hashing algorithm.</span></span><br/>                                                                                                                                           | <span data-ttu-id="93b1f-114">1</span><span class="sxs-lookup"><span data-stu-id="93b1f-114">1</span></span>     |
| <span data-ttu-id="93b1f-115">**\_Algorithme de hachage \_ CAPICOM \_ MD4**</span><span class="sxs-lookup"><span data-stu-id="93b1f-115">**CAPICOM\_HASH\_ALGORITHM\_MD4**</span></span>      | <span data-ttu-id="93b1f-116">Algorithme de hachage MD4.</span><span class="sxs-lookup"><span data-stu-id="93b1f-116">MD4 hashing algorithm.</span></span><br/>                                                                                                                                           | <span data-ttu-id="93b1f-117">2</span><span class="sxs-lookup"><span data-stu-id="93b1f-117">2</span></span>     |
| <span data-ttu-id="93b1f-118">**\_Algorithme de hachage \_ CAPICOM \_ MD5**</span><span class="sxs-lookup"><span data-stu-id="93b1f-118">**CAPICOM\_HASH\_ALGORITHM\_MD5**</span></span>      | <span data-ttu-id="93b1f-119">Algorithme de hachage MD5.</span><span class="sxs-lookup"><span data-stu-id="93b1f-119">MD5 hashing algorithm.</span></span><br/>                                                                                                                                           | <span data-ttu-id="93b1f-120">3</span><span class="sxs-lookup"><span data-stu-id="93b1f-120">3</span></span>     |
| <span data-ttu-id="93b1f-121">**\_Algorithme de hachage \_ capicom \_ SHA \_ 256**</span><span class="sxs-lookup"><span data-stu-id="93b1f-121">**CAPICOM\_HASH\_ALGORITHM\_SHA\_256**</span></span> | <span data-ttu-id="93b1f-122">Algorithme de hachage SHA-256.</span><span class="sxs-lookup"><span data-stu-id="93b1f-122">SHA-256 hash algorithm.</span></span><br/> <span data-ttu-id="93b1f-123">**CAPICOM 2.0.0.3 et versions antérieures :** Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="93b1f-123">**CAPICOM 2.0.0.3 and earlier:** This value is not supported.</span></span><br/>                                                                 | <span data-ttu-id="93b1f-124">4</span><span class="sxs-lookup"><span data-stu-id="93b1f-124">4</span></span>     |
| <span data-ttu-id="93b1f-125">**\_Algorithme de hachage \_ capicom \_ SHA \_ 384**</span><span class="sxs-lookup"><span data-stu-id="93b1f-125">**CAPICOM\_HASH\_ALGORITHM\_SHA\_384**</span></span> | <span data-ttu-id="93b1f-126">Algorithme de hachage SHA-384.</span><span class="sxs-lookup"><span data-stu-id="93b1f-126">SHA-384 hash algorithm.</span></span><br/> <span data-ttu-id="93b1f-127">**CAPICOM 2.0.0.3 et versions antérieures :** Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="93b1f-127">**CAPICOM 2.0.0.3 and earlier:** This value is not supported.</span></span><br/>                                                                 | <span data-ttu-id="93b1f-128">5</span><span class="sxs-lookup"><span data-stu-id="93b1f-128">5</span></span>     |
| <span data-ttu-id="93b1f-129">**\_Algorithme de hachage \_ capicom \_ SHA \_ 512**</span><span class="sxs-lookup"><span data-stu-id="93b1f-129">**CAPICOM\_HASH\_ALGORITHM\_SHA\_512**</span></span> | <span data-ttu-id="93b1f-130">Algorithme de hachage SHA-512.</span><span class="sxs-lookup"><span data-stu-id="93b1f-130">SHA-512 hash algorithm.</span></span><br/> <span data-ttu-id="93b1f-131">**CAPICOM 2.0.0.3 et versions antérieures :** Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="93b1f-131">**CAPICOM 2.0.0.3 and earlier:** This value is not supported.</span></span><br/>                                                                 | <span data-ttu-id="93b1f-132">6</span><span class="sxs-lookup"><span data-stu-id="93b1f-132">6</span></span>     |



## <a name="remarks"></a><span data-ttu-id="93b1f-133">Notes</span><span class="sxs-lookup"><span data-stu-id="93b1f-133">Remarks</span></span>

<span data-ttu-id="93b1f-134">L’énumération de l' **\_ \_ algorithme de hachage CAPICOM** est utilisée par la propriété [**HashedData. Algorithm**](hasheddata-algorithm.md) .</span><span class="sxs-lookup"><span data-stu-id="93b1f-134">The **CAPICOM\_HASH\_ALGORITHM** enumeration is used by the [**HashedData.Algorithm**](hasheddata-algorithm.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="93b1f-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="93b1f-135">Requirements</span></span>



| <span data-ttu-id="93b1f-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="93b1f-136">Requirement</span></span> | <span data-ttu-id="93b1f-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="93b1f-137">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="93b1f-138">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="93b1f-138">Redistributable</span></span><br/> | <span data-ttu-id="93b1f-139">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="93b1f-139">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="93b1f-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="93b1f-140">Header</span></span><br/>          | <dl> <span data-ttu-id="93b1f-141"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="93b1f-141"><dt>Capicom.h</dt></span></span> </dl> |



 

 
