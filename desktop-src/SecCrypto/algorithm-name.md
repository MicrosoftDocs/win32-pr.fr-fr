---
description: Définit ou récupère l’algorithme utilisé pour la signature, l’enveloppe et le chiffrement des opérations. Il s’agit de la propriété par défaut.
ms.assetid: e1144a9c-a352-4f73-a91c-ea66f3d61608
title: Propriété Algorithm.Name
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Algorithm.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 35ff147d8db7fb409787fa938a951dfc0a2320e3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523871"
---
# <a name="algorithmname-property"></a><span data-ttu-id="9a886-104">Propriété Algorithm.Name</span><span class="sxs-lookup"><span data-stu-id="9a886-104">Algorithm.Name property</span></span>

<span data-ttu-id="9a886-105">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9a886-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="9a886-106">Utilisez plutôt la [**classe AlgorithmIdentifier**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="9a886-106">Instead, use the [**AlgorithmIdentifier Class**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="9a886-107">La propriété **Name** définit ou récupère l’algorithme utilisé pour la signature, l’enveloppe et le chiffrement des opérations.</span><span class="sxs-lookup"><span data-stu-id="9a886-107">The **Name** property sets or retrieves the algorithm used for signing, enveloping, and encrypting operations.</span></span> <span data-ttu-id="9a886-108">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="9a886-108">This is the default property.</span></span>

<span data-ttu-id="9a886-109">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="9a886-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a886-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9a886-110">Syntax</span></span>


```VB
Algorithm.Name As CAPICOM_ENCRYPTION_ALGORITHM
```



## <a name="property-value"></a><span data-ttu-id="9a886-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="9a886-111">Property value</span></span>

<span data-ttu-id="9a886-112">Valeur de l’énumération de l' [**\_ \_ algorithme de chiffrement CAPICOM**](capicom-encryption-algorithm.md) qui spécifie l’algorithme à utiliser.</span><span class="sxs-lookup"><span data-stu-id="9a886-112">A value of the [**CAPICOM\_ENCRYPTION\_ALGORITHM**](capicom-encryption-algorithm.md) enumeration that specifies which algorithm to use.</span></span> <span data-ttu-id="9a886-113">Le tableau suivant répertorie les valeurs possibles.</span><span class="sxs-lookup"><span data-stu-id="9a886-113">The following table shows the possible values.</span></span>



| <span data-ttu-id="9a886-114">Value</span><span class="sxs-lookup"><span data-stu-id="9a886-114">Value</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="9a886-115">Signification</span><span class="sxs-lookup"><span data-stu-id="9a886-115">Meaning</span></span>                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_RC2"></span><span id="capicom_encryption_algorithm_rc2"></span><dl> <span data-ttu-id="9a886-116"><dt>**\_Algorithme de chiffrement CAPICOM \_ \_ RC2**</dt></span><span class="sxs-lookup"><span data-stu-id="9a886-116"><dt>**CAPICOM\_ENCRYPTION\_ALGORITHM\_RC2**</dt></span></span> </dl>    | <span data-ttu-id="9a886-117">Utilisez le chiffrement RC2.</span><span class="sxs-lookup"><span data-stu-id="9a886-117">Use RC2 encryption.</span></span><br/>        |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_RC4"></span><span id="capicom_encryption_algorithm_rc4"></span><dl> <span data-ttu-id="9a886-118"><dt>**\_Algorithme de chiffrement CAPICOM \_ \_ RC4**</dt></span><span class="sxs-lookup"><span data-stu-id="9a886-118"><dt>**CAPICOM\_ENCRYPTION\_ALGORITHM\_RC4**</dt></span></span> </dl>    | <span data-ttu-id="9a886-119">Utilisez le chiffrement RC4.</span><span class="sxs-lookup"><span data-stu-id="9a886-119">Use RC4 encryption.</span></span><br/>        |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_DES"></span><span id="capicom_encryption_algorithm_des"></span><dl> <span data-ttu-id="9a886-120"><dt>**\_algorithme de chiffrement CAPICOM \_ \_ des**</dt></span><span class="sxs-lookup"><span data-stu-id="9a886-120"><dt>**CAPICOM\_ENCRYPTION\_ALGORITHM\_DES**</dt></span></span> </dl>    | <span data-ttu-id="9a886-121">Utilisez le chiffrement DES.</span><span class="sxs-lookup"><span data-stu-id="9a886-121">Use DES encryption.</span></span><br/>        |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_3DES"></span><span id="capicom_encryption_algorithm_3des"></span><dl> <span data-ttu-id="9a886-122"><dt>**\_Algorithme de chiffrement CAPICOM \_ \_ 3DES**</dt></span><span class="sxs-lookup"><span data-stu-id="9a886-122"><dt>**CAPICOM\_ENCRYPTION\_ALGORITHM\_3DES**</dt></span></span> </dl> | <span data-ttu-id="9a886-123">Utilisez le chiffrement triple DES.</span><span class="sxs-lookup"><span data-stu-id="9a886-123">Use triple DES encryption.</span></span><br/> |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_AES"></span><span id="capicom_encryption_algorithm_aes"></span><dl> <span data-ttu-id="9a886-124"><dt>**\_algorithme de chiffrement CAPICOM \_ \_ AES**</dt></span><span class="sxs-lookup"><span data-stu-id="9a886-124"><dt>**CAPICOM\_ENCRYPTION\_ALGORITHM\_AES**</dt></span></span> </dl>    | <span data-ttu-id="9a886-125">Utilisez l’algorithme AES.</span><span class="sxs-lookup"><span data-stu-id="9a886-125">Use the AES algorithm.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="9a886-126">Notes</span><span class="sxs-lookup"><span data-stu-id="9a886-126">Remarks</span></span>

<span data-ttu-id="9a886-127">Lorsque la valeur de cette propriété est réinitialisée, directement ou indirectement, l’intégralité de l’état de l’objet est réinitialisée.</span><span class="sxs-lookup"><span data-stu-id="9a886-127">When the value of this property is reset, directly or indirectly, the whole state of the object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a886-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9a886-128">Requirements</span></span>



| <span data-ttu-id="9a886-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9a886-129">Requirement</span></span> | <span data-ttu-id="9a886-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a886-130">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a886-131">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="9a886-131">End of client support</span></span><br/> | <span data-ttu-id="9a886-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9a886-132">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="9a886-133">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="9a886-133">End of server support</span></span><br/> | <span data-ttu-id="9a886-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9a886-134">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="9a886-135">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="9a886-135">Redistributable</span></span><br/>       | <span data-ttu-id="9a886-136">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="9a886-136">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="9a886-137">DLL</span><span class="sxs-lookup"><span data-stu-id="9a886-137">DLL</span></span><br/>                   | <dl> <span data-ttu-id="9a886-138"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a886-138"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
