---
description: Définit la longueur de clé à utiliser dans le chiffrement.
ms.assetid: a91e75db-f81e-4908-b795-34be7a1c242d
title: Énumération CAPICOM_ENCRYPTION_KEY_LENGTH (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ENCRYPTION_KEY_LENGTH
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 4f3e64df1e706ef20a83f4da5c81cda2a08ed331
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537127"
---
# <a name="capicom_encryption_key_length-enumeration"></a><span data-ttu-id="43bed-103">\_Énumération de la \_ longueur de clé de CHIFFREment CAPICOM \_</span><span class="sxs-lookup"><span data-stu-id="43bed-103">CAPICOM\_ENCRYPTION\_KEY\_LENGTH enumeration</span></span>

<span data-ttu-id="43bed-104">Le type d’énumération de la **longueur de \_ \_ clé \_ de chiffrement CAPICOM** définit la [*longueur de clé*](../secgloss/k-gly.md) à utiliser dans le chiffrement.</span><span class="sxs-lookup"><span data-stu-id="43bed-104">The **CAPICOM\_ENCRYPTION\_KEY\_LENGTH** enumeration type defines the [*key length*](../secgloss/k-gly.md) to be used in encryption.</span></span>

## <a name="members"></a><span data-ttu-id="43bed-105">Membres</span><span class="sxs-lookup"><span data-stu-id="43bed-105">Members</span></span>



| <span data-ttu-id="43bed-106">Membre</span><span class="sxs-lookup"><span data-stu-id="43bed-106">Member</span></span>                                          | <span data-ttu-id="43bed-107">Description</span><span class="sxs-lookup"><span data-stu-id="43bed-107">Description</span></span>                                                                               | <span data-ttu-id="43bed-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="43bed-108">Value</span></span>     |
|-------------------------------------------------|-------------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="43bed-109">**\_ \_ \_ longueur maximale de la clé de chiffrement CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="43bed-109">**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_MAXIMUM**</span></span>   | <span data-ttu-id="43bed-110">Utilise la longueur de clé maximale disponible avec l’algorithme de chiffrement indiqué.</span><span class="sxs-lookup"><span data-stu-id="43bed-110">Uses the maximum key length available with the indicated encryption algorithm.</span></span><br/> | <span data-ttu-id="43bed-111">0</span><span class="sxs-lookup"><span data-stu-id="43bed-111">0</span></span>         |
| <span data-ttu-id="43bed-112">**\_Longueur de clé de chiffrement capicom \_ \_ \_ 40 \_ bits**</span><span class="sxs-lookup"><span data-stu-id="43bed-112">**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_40\_BITS**</span></span>  | <span data-ttu-id="43bed-113">Utilise des clés 40 bits.</span><span class="sxs-lookup"><span data-stu-id="43bed-113">Uses 40-bit keys.</span></span><br/>                                                              | <span data-ttu-id="43bed-114">1</span><span class="sxs-lookup"><span data-stu-id="43bed-114">1</span></span>         |
| <span data-ttu-id="43bed-115">**\_Longueur de clé de chiffrement capicom \_ \_ \_ 56 \_ bits**</span><span class="sxs-lookup"><span data-stu-id="43bed-115">**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_56\_BITS**</span></span>  | <span data-ttu-id="43bed-116">Utilise des clés 56 bits si elles sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="43bed-116">Uses 56-bit keys if available.</span></span><br/>                                                 | <span data-ttu-id="43bed-117">2</span><span class="sxs-lookup"><span data-stu-id="43bed-117">2</span></span>         |
| <span data-ttu-id="43bed-118">**\_Longueur de clé de chiffrement capicom \_ \_ \_ 128 \_ bits**</span><span class="sxs-lookup"><span data-stu-id="43bed-118">**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_128\_BITS**</span></span> | <span data-ttu-id="43bed-119">Utilise des clés 128 bits si elles sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="43bed-119">Uses 128-bit keys if available.</span></span><br/>                                                | <span data-ttu-id="43bed-120">3</span><span class="sxs-lookup"><span data-stu-id="43bed-120">3</span></span>         |
| <span data-ttu-id="43bed-121">**\_Longueur de clé de chiffrement capicom \_ \_ \_ 192 \_ bits**</span><span class="sxs-lookup"><span data-stu-id="43bed-121">**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_192\_BITS**</span></span> | <span data-ttu-id="43bed-122">Utilise des clés 192 bits.</span><span class="sxs-lookup"><span data-stu-id="43bed-122">Uses 192-bit keys.</span></span> <span data-ttu-id="43bed-123">Cette longueur de clé n’est disponible que pour AES.</span><span class="sxs-lookup"><span data-stu-id="43bed-123">This key length is available only for AES.</span></span><br/>                  | <span data-ttu-id="43bed-124">4//v 2.0</span><span class="sxs-lookup"><span data-stu-id="43bed-124">4 // v2.0</span></span> |
| <span data-ttu-id="43bed-125">**\_Longueur de clé de chiffrement capicom \_ \_ \_ 256 \_ bits**</span><span class="sxs-lookup"><span data-stu-id="43bed-125">**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_256\_BITS**</span></span> | <span data-ttu-id="43bed-126">Utilise des clés 256 bits.</span><span class="sxs-lookup"><span data-stu-id="43bed-126">Uses 256-bit keys.</span></span> <span data-ttu-id="43bed-127">Cette longueur de clé n’est disponible que pour AES.</span><span class="sxs-lookup"><span data-stu-id="43bed-127">This key length is available only for AES.</span></span><br/>                  | <span data-ttu-id="43bed-128">5//v 2.0</span><span class="sxs-lookup"><span data-stu-id="43bed-128">5 // v2.0</span></span> |



## <a name="remarks"></a><span data-ttu-id="43bed-129">Notes</span><span class="sxs-lookup"><span data-stu-id="43bed-129">Remarks</span></span>

<span data-ttu-id="43bed-130">Le type d’énumération de la **\_ longueur de \_ clé \_ de chiffrement CAPICOM** est utilisé par la propriété [**Algorithm. KeyLength**](algorithm-keylength.md) .</span><span class="sxs-lookup"><span data-stu-id="43bed-130">The **CAPICOM\_ENCRYPTION\_KEY\_LENGTH** enumeration type is used by the [**Algorithm.KeyLength**](algorithm-keylength.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="43bed-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="43bed-131">Requirements</span></span>



| <span data-ttu-id="43bed-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="43bed-132">Requirement</span></span> | <span data-ttu-id="43bed-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="43bed-133">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="43bed-134">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="43bed-134">Redistributable</span></span><br/> | <span data-ttu-id="43bed-135">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="43bed-135">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="43bed-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="43bed-136">Header</span></span><br/>          | <dl> <span data-ttu-id="43bed-137"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="43bed-137"><dt>Capicom.h</dt></span></span> </dl> |



 

 
