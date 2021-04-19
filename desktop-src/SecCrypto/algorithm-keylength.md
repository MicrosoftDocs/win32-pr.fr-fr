---
description: Définit ou récupère la longueur de la clé.
ms.assetid: c0176d2d-c000-4529-af45-1cc9060ca56a
title: Propriété d’algorithme. KeyLength
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Algorithm.KeyLength
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0aa5dbaeeebe2daaf925b5d5f3aa82b36053fc39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523477"
---
# <a name="algorithmkeylength-property"></a><span data-ttu-id="4a5ef-103">Propriété d’algorithme. KeyLength</span><span class="sxs-lookup"><span data-stu-id="4a5ef-103">Algorithm.KeyLength property</span></span>

<span data-ttu-id="4a5ef-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4a5ef-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="4a5ef-105">Utilisez plutôt la [**classe AlgorithmIdentifier**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="4a5ef-105">Instead, use the [**AlgorithmIdentifier Class**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="4a5ef-106">La propriété **KeyLength** définit ou récupère la longueur de la clé.</span><span class="sxs-lookup"><span data-stu-id="4a5ef-106">The **KeyLength** property sets or retrieves the length of the key.</span></span>

<span data-ttu-id="4a5ef-107">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="4a5ef-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a5ef-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4a5ef-108">Syntax</span></span>


```VB
Algorithm.KeyLength As CAPICOM_ENCRYPTION_KEY_LENGTH
```



## <a name="property-value"></a><span data-ttu-id="4a5ef-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="4a5ef-109">Property value</span></span>

<span data-ttu-id="4a5ef-110">Valeur de l’énumération de la [**longueur de \_ \_ clé \_ de chiffrement CAPICOM**](capicom-encryption-key-length.md) qui spécifie la longueur de clé.</span><span class="sxs-lookup"><span data-stu-id="4a5ef-110">A value of the [**CAPICOM\_ENCRYPTION\_KEY\_LENGTH**](capicom-encryption-key-length.md) enumeration that specifies the key length.</span></span> <span data-ttu-id="4a5ef-111">Le tableau suivant répertorie les valeurs possibles.</span><span class="sxs-lookup"><span data-stu-id="4a5ef-111">The following table shows the possible values.</span></span>



| <span data-ttu-id="4a5ef-112">Value</span><span class="sxs-lookup"><span data-stu-id="4a5ef-112">Value</span></span>                                                                                                                                                                                                                                        | <span data-ttu-id="4a5ef-113">Signification</span><span class="sxs-lookup"><span data-stu-id="4a5ef-113">Meaning</span></span>                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_MAXIMUM"></span><span id="capicom_encryption_key_length_maximum"></span><dl> <span data-ttu-id="4a5ef-114"><dt>**\_ \_ \_ longueur maximale de la clé de chiffrement CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4a5ef-114"><dt>**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_MAXIMUM**</dt></span></span> </dl>     | <span data-ttu-id="4a5ef-115">Utilisez la longueur de clé maximale disponible avec l’algorithme de chiffrement indiqué.</span><span class="sxs-lookup"><span data-stu-id="4a5ef-115">Use the maximum key length available with the indicated encryption algorithm.</span></span><br/> |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_40_BITS"></span><span id="capicom_encryption_key_length_40_bits"></span><dl> <span data-ttu-id="4a5ef-116"><dt>**\_Longueur de clé de chiffrement capicom \_ \_ \_ 40 \_ bits**</dt></span><span class="sxs-lookup"><span data-stu-id="4a5ef-116"><dt>**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_40\_BITS**</dt></span></span> </dl>    | <span data-ttu-id="4a5ef-117">Utilisez des clés 40 bits.</span><span class="sxs-lookup"><span data-stu-id="4a5ef-117">Use 40-bit keys.</span></span><br/>                                                              |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_56_BITS"></span><span id="capicom_encryption_key_length_56_bits"></span><dl> <span data-ttu-id="4a5ef-118"><dt>**\_Longueur de clé de chiffrement capicom \_ \_ \_ 56 \_ bits**</dt></span><span class="sxs-lookup"><span data-stu-id="4a5ef-118"><dt>**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_56\_BITS**</dt></span></span> </dl>    | <span data-ttu-id="4a5ef-119">Utilisez des clés 56 bits si elles sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="4a5ef-119">Use 56-bit keys if available.</span></span><br/>                                                 |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_128_BITS"></span><span id="capicom_encryption_key_length_128_bits"></span><dl> <span data-ttu-id="4a5ef-120"><dt>**\_Longueur de clé de chiffrement capicom \_ \_ \_ 128 \_ bits**</dt></span><span class="sxs-lookup"><span data-stu-id="4a5ef-120"><dt>**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_128\_BITS**</dt></span></span> </dl> | <span data-ttu-id="4a5ef-121">Utilisez des clés 128 bits si elles sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="4a5ef-121">Use 128-bit keys if available.</span></span><br/>                                                |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_192_BITS"></span><span id="capicom_encryption_key_length_192_bits"></span><dl> <span data-ttu-id="4a5ef-122"><dt>**\_Longueur de clé de chiffrement capicom \_ \_ \_ 192 \_ bits**</dt></span><span class="sxs-lookup"><span data-stu-id="4a5ef-122"><dt>**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_192\_BITS**</dt></span></span> </dl> | <span data-ttu-id="4a5ef-123">Utilisez des clés 192 bits.</span><span class="sxs-lookup"><span data-stu-id="4a5ef-123">Use 192-bit keys.</span></span> <span data-ttu-id="4a5ef-124">Cette longueur de clé n’est disponible que pour AES.</span><span class="sxs-lookup"><span data-stu-id="4a5ef-124">This key length is available only for AES.</span></span><br/>                  |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_256_BITS"></span><span id="capicom_encryption_key_length_256_bits"></span><dl> <span data-ttu-id="4a5ef-125"><dt>**\_Longueur de clé de chiffrement capicom \_ \_ \_ 256 \_ bits**</dt></span><span class="sxs-lookup"><span data-stu-id="4a5ef-125"><dt>**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_256\_BITS**</dt></span></span> </dl> | <span data-ttu-id="4a5ef-126">Utilisez des clés 256 bits.</span><span class="sxs-lookup"><span data-stu-id="4a5ef-126">Use 256-bit keys.</span></span> <span data-ttu-id="4a5ef-127">Cette longueur de clé n’est disponible que pour AES.</span><span class="sxs-lookup"><span data-stu-id="4a5ef-127">This key length is available only for AES.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="4a5ef-128">Notes</span><span class="sxs-lookup"><span data-stu-id="4a5ef-128">Remarks</span></span>

<span data-ttu-id="4a5ef-129">Lorsque des algorithmes de chiffrement DES et 3DES sont utilisés, les longueurs de clé sont standard et la propriété **KeyLength** est ignorée.</span><span class="sxs-lookup"><span data-stu-id="4a5ef-129">When DES and 3DES encryption algorithms are used, the key lengths are standard and the **KeyLength** property is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a5ef-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4a5ef-130">Requirements</span></span>



| <span data-ttu-id="4a5ef-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4a5ef-131">Requirement</span></span> | <span data-ttu-id="4a5ef-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="4a5ef-132">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a5ef-133">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="4a5ef-133">End of client support</span></span><br/> | <span data-ttu-id="4a5ef-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4a5ef-134">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="4a5ef-135">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="4a5ef-135">End of server support</span></span><br/> | <span data-ttu-id="4a5ef-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4a5ef-136">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="4a5ef-137">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="4a5ef-137">Redistributable</span></span><br/>       | <span data-ttu-id="4a5ef-138">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="4a5ef-138">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="4a5ef-139">DLL</span><span class="sxs-lookup"><span data-stu-id="4a5ef-139">DLL</span></span><br/>                   | <dl> <span data-ttu-id="4a5ef-140"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a5ef-140"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a5ef-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4a5ef-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a5ef-142">**Algorithme**</span><span class="sxs-lookup"><span data-stu-id="4a5ef-142">**Algorithm**</span></span>](algorithm.md)
</dt> </dl>

 

 
