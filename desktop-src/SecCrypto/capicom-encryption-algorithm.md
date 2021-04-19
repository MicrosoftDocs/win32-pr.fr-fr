---
description: Définit les algorithmes à utiliser dans le chiffrement et le déchiffrement.
ms.assetid: c7aacd1c-02f6-4cf5-9305-50e2330f243c
title: Énumération CAPICOM_ENCRYPTION_ALGORITHM (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ENCRYPTION_ALGORITHM
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 19626ba560ead406005612db3ed90cabc61d98ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528519"
---
# <a name="capicom_encryption_algorithm-enumeration"></a><span data-ttu-id="cbaff-103">\_Énumération de l’algorithme de chiffrement CAPICOM \_</span><span class="sxs-lookup"><span data-stu-id="cbaff-103">CAPICOM\_ENCRYPTION\_ALGORITHM enumeration</span></span>

<span data-ttu-id="cbaff-104">Le type d’énumération de l' **\_ \_ algorithme de chiffrement CAPICOM** définit les algorithmes à utiliser dans le chiffrement et le déchiffrement.</span><span class="sxs-lookup"><span data-stu-id="cbaff-104">The **CAPICOM\_ENCRYPTION\_ALGORITHM** enumeration type defines the algorithms to be used in encryption and decryption.</span></span>

## <a name="members"></a><span data-ttu-id="cbaff-105">Membres</span><span class="sxs-lookup"><span data-stu-id="cbaff-105">Members</span></span>



| <span data-ttu-id="cbaff-106">Membre</span><span class="sxs-lookup"><span data-stu-id="cbaff-106">Member</span></span>                                   | <span data-ttu-id="cbaff-107">Description</span><span class="sxs-lookup"><span data-stu-id="cbaff-107">Description</span></span>                                                                                                                                                                                              | <span data-ttu-id="cbaff-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="cbaff-108">Value</span></span>     |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="cbaff-109">**\_Algorithme de chiffrement CAPICOM \_ \_ RC2**</span><span class="sxs-lookup"><span data-stu-id="cbaff-109">**CAPICOM\_ENCRYPTION\_ALGORITHM\_RC2**</span></span>  | <span data-ttu-id="cbaff-110">Utilisez le chiffrement RSA RC2.</span><span class="sxs-lookup"><span data-stu-id="cbaff-110">Use RSA RC2 encryption.</span></span><br/>                                                                                                                                                                       | <span data-ttu-id="cbaff-111">0</span><span class="sxs-lookup"><span data-stu-id="cbaff-111">0</span></span>         |
| <span data-ttu-id="cbaff-112">**\_Algorithme de chiffrement CAPICOM \_ \_ RC4**</span><span class="sxs-lookup"><span data-stu-id="cbaff-112">**CAPICOM\_ENCRYPTION\_ALGORITHM\_RC4**</span></span>  | <span data-ttu-id="cbaff-113">Utilisez le chiffrement RSA RC4.</span><span class="sxs-lookup"><span data-stu-id="cbaff-113">Use RSA RC4 encryption.</span></span><br/>                                                                                                                                                                       | <span data-ttu-id="cbaff-114">1</span><span class="sxs-lookup"><span data-stu-id="cbaff-114">1</span></span>         |
| <span data-ttu-id="cbaff-115">**\_algorithme de chiffrement CAPICOM \_ \_ des**</span><span class="sxs-lookup"><span data-stu-id="cbaff-115">**CAPICOM\_ENCRYPTION\_ALGORITHM\_DES**</span></span>  | <span data-ttu-id="cbaff-116">Utilisez le chiffrement DES.</span><span class="sxs-lookup"><span data-stu-id="cbaff-116">Use DES encryption.</span></span><br/>                                                                                                                                                                           | <span data-ttu-id="cbaff-117">2</span><span class="sxs-lookup"><span data-stu-id="cbaff-117">2</span></span>         |
| <span data-ttu-id="cbaff-118">**\_Algorithme de chiffrement CAPICOM \_ \_ 3DES**</span><span class="sxs-lookup"><span data-stu-id="cbaff-118">**CAPICOM\_ENCRYPTION\_ALGORITHM\_3DES**</span></span> | <span data-ttu-id="cbaff-119">Utilisez le chiffrement triple DES.</span><span class="sxs-lookup"><span data-stu-id="cbaff-119">Use triple DES encryption.</span></span><br/>                                                                                                                                                                    | <span data-ttu-id="cbaff-120">3</span><span class="sxs-lookup"><span data-stu-id="cbaff-120">3</span></span>         |
| <span data-ttu-id="cbaff-121">**\_algorithme de chiffrement CAPICOM \_ \_ AES**</span><span class="sxs-lookup"><span data-stu-id="cbaff-121">**CAPICOM\_ENCRYPTION\_ALGORITHM\_AES**</span></span>  | <span data-ttu-id="cbaff-122">Utilisez l’algorithme [*Advanced Encryption Standard*](../secgloss/a-gly.md) (AES).</span><span class="sxs-lookup"><span data-stu-id="cbaff-122">Use the [*Advanced Encryption Standard*](../secgloss/a-gly.md) (AES) algorithm.</span></span> <span data-ttu-id="cbaff-123">Cette valeur est valide pour l’objet [**EncryptedData**](encrypteddata.md) uniquement.</span><span class="sxs-lookup"><span data-stu-id="cbaff-123">This value is valid for the [**EncryptedData**](encrypteddata.md) object only.</span></span><br/> | <span data-ttu-id="cbaff-124">4//v 2.0</span><span class="sxs-lookup"><span data-stu-id="cbaff-124">4 // v2.0</span></span> |



## <a name="remarks"></a><span data-ttu-id="cbaff-125">Notes</span><span class="sxs-lookup"><span data-stu-id="cbaff-125">Remarks</span></span>

<span data-ttu-id="cbaff-126">Le type d’énumération de l' **\_ \_ algorithme de chiffrement CAPICOM** est utilisé par la propriété [**Algorithm.Name**](algorithm-name.md) .</span><span class="sxs-lookup"><span data-stu-id="cbaff-126">The **CAPICOM\_ENCRYPTION\_ALGORITHM** enumeration type is used by the [**Algorithm.Name**](algorithm-name.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbaff-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cbaff-127">Requirements</span></span>



| <span data-ttu-id="cbaff-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cbaff-128">Requirement</span></span> | <span data-ttu-id="cbaff-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="cbaff-129">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cbaff-130">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="cbaff-130">Redistributable</span></span><br/> | <span data-ttu-id="cbaff-131">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="cbaff-131">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="cbaff-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="cbaff-132">Header</span></span><br/>          | <dl> <span data-ttu-id="cbaff-133"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="cbaff-133"><dt>Capicom.h</dt></span></span> </dl> |



 

 
