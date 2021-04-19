---
description: Fournit des propriétés et des méthodes permettant d’établir le contenu à signer à l’aide d’une signature numérique, de signer ou de signer des données numériquement, et de vérifier la signature numérique des données signées. Le message signé est au \# format PKCS 7.
ms.assetid: 500437e8-a637-4e89-9ac9-aa3ea20d437f
title: Objet SignedData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6d0424826f7dc5d041b877ced1cd7f50490d7801
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542461"
---
# <a name="signeddata-object"></a><span data-ttu-id="97fa1-104">Objet SignedData</span><span class="sxs-lookup"><span data-stu-id="97fa1-104">SignedData object</span></span>

<span data-ttu-id="97fa1-105">\[L’objet **SignedData** peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="97fa1-105">\[The **SignedData** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="97fa1-106">Utilisez plutôt la [**classe SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="97fa1-106">Instead, use the [**SignedCms Class**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="97fa1-107">L’objet **SignedData** fournit des propriétés et des méthodes permettant d’établir le contenu à signer à l’aide d’une [*signature numérique*](../secgloss/d-gly.md), de signer ou de signer des données numériquement, et de vérifier la signature numérique des données signées.</span><span class="sxs-lookup"><span data-stu-id="97fa1-107">The **SignedData** object provides properties and methods to establish the content to be signed with a [*digital signature*](../secgloss/d-gly.md), to sign or cosign data digitally, and to verify the digital signature of signed data.</span></span> <span data-ttu-id="97fa1-108">Le message signé est au \# format PKCS 7.</span><span class="sxs-lookup"><span data-stu-id="97fa1-108">The signed message is in PKCS \#7 format.</span></span>

<span data-ttu-id="97fa1-109">Une signature de données, si elle est vérifiée, prouve l’association entre un signataire et des données et indique que les données n’ont pas été modifiées après la création de la signature.</span><span class="sxs-lookup"><span data-stu-id="97fa1-109">A data signature, if verified, proves the association between a signer and data and shows that the data was not changed in any way after the signature was created.</span></span>

## <a name="members"></a><span data-ttu-id="97fa1-110">Membres</span><span class="sxs-lookup"><span data-stu-id="97fa1-110">Members</span></span>

<span data-ttu-id="97fa1-111">L’objet **SignedData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="97fa1-111">The **SignedData** object has these types of members:</span></span>

-   [<span data-ttu-id="97fa1-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="97fa1-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="97fa1-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="97fa1-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="97fa1-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="97fa1-114">Methods</span></span>

<span data-ttu-id="97fa1-115">L’objet **SignedData** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="97fa1-115">The **SignedData** object has these methods.</span></span>



| <span data-ttu-id="97fa1-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="97fa1-116">Method</span></span>                              | <span data-ttu-id="97fa1-117">Description</span><span class="sxs-lookup"><span data-stu-id="97fa1-117">Description</span></span>                                                         |
|:------------------------------------|:--------------------------------------------------------------------|
| [<span data-ttu-id="97fa1-118">**Cosigne**</span><span class="sxs-lookup"><span data-stu-id="97fa1-118">**CoSign**</span></span>](signeddata-cosign.md) | <span data-ttu-id="97fa1-119">Cosigne un message déjà signé.</span><span class="sxs-lookup"><span data-stu-id="97fa1-119">Cosigns an already signed message.</span></span><br/>                       |
| [<span data-ttu-id="97fa1-120">**Expéditeur**</span><span class="sxs-lookup"><span data-stu-id="97fa1-120">**Sign**</span></span>](signeddata-sign.md)     | <span data-ttu-id="97fa1-121">Crée une signature numérique sur le contenu à signer.</span><span class="sxs-lookup"><span data-stu-id="97fa1-121">Creates a digital signature on the content to be signed.</span></span><br/> |
| [<span data-ttu-id="97fa1-122">**Vérifier**</span><span class="sxs-lookup"><span data-stu-id="97fa1-122">**Verify**</span></span>](signeddata-verify.md) | <span data-ttu-id="97fa1-123">Détermine la validité d’une signature ou de signatures.</span><span class="sxs-lookup"><span data-stu-id="97fa1-123">Determines the validity of a signature or signatures.</span></span><br/>    |



 

### <a name="properties"></a><span data-ttu-id="97fa1-124">Propriétés</span><span class="sxs-lookup"><span data-stu-id="97fa1-124">Properties</span></span>

<span data-ttu-id="97fa1-125">L’objet **SignedData** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="97fa1-125">The **SignedData** object has these properties.</span></span>



| <span data-ttu-id="97fa1-126">Propriété</span><span class="sxs-lookup"><span data-stu-id="97fa1-126">Property</span></span>                                                   | <span data-ttu-id="97fa1-127">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="97fa1-127">Access type</span></span>           | <span data-ttu-id="97fa1-128">Description</span><span class="sxs-lookup"><span data-stu-id="97fa1-128">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:-----------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="97fa1-129">**Certificats**</span><span class="sxs-lookup"><span data-stu-id="97fa1-129">**Certificates**</span></span>](signeddata-certificates.md)<br/> | <span data-ttu-id="97fa1-130">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="97fa1-130">Read-only</span></span><br/>  | <span data-ttu-id="97fa1-131">Récupère la collection de [**certificats**](certificates.md) des données signées.</span><span class="sxs-lookup"><span data-stu-id="97fa1-131">Retrieves the [**Certificates**](certificates.md) collection of the signed data.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="97fa1-132">**Content**</span><span class="sxs-lookup"><span data-stu-id="97fa1-132">**Content**</span></span>](signeddata-content.md)<br/>           | <span data-ttu-id="97fa1-133">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="97fa1-133">Read/write</span></span><br/> | <span data-ttu-id="97fa1-134">Données à signer.</span><span class="sxs-lookup"><span data-stu-id="97fa1-134">Data to be signed.</span></span> <span data-ttu-id="97fa1-135">Cette propriété doit être initialisée avant l’appel de la méthode [**Sign**](signeddata-sign.md) .</span><span class="sxs-lookup"><span data-stu-id="97fa1-135">This property must be initialized before the [**Sign**](signeddata-sign.md) method is called.</span></span><br/> <span data-ttu-id="97fa1-136">Lorsque la valeur de cette propriété est réinitialisée, directement ou indirectement, l’intégralité de l' [*État*](../secgloss/s-gly.md) de l’objet est réinitialisée, et toute signature associée à l’objet avant la modification de la propriété est perdue.</span><span class="sxs-lookup"><span data-stu-id="97fa1-136">When the value of this property is reset, directly or indirectly, the whole [*state*](../secgloss/s-gly.md) of the object is reset, and any signature that was associated with the object before the property was changed is lost.</span></span><br/> <span data-ttu-id="97fa1-137">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="97fa1-137">This is the default property.</span></span><br/> |
| [<span data-ttu-id="97fa1-138">**Signataires**</span><span class="sxs-lookup"><span data-stu-id="97fa1-138">**Signers**</span></span>](signeddata-signers.md)<br/>           | <span data-ttu-id="97fa1-139">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="97fa1-139">Read-only</span></span><br/>  | <span data-ttu-id="97fa1-140">Récupère la collection de [**signataires**](signers.md) qui représente les créateurs de signature des données.</span><span class="sxs-lookup"><span data-stu-id="97fa1-140">Retrieves the [**Signers**](signers.md) collection that represents the signature creators of the data.</span></span><br/>                                                                                                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="97fa1-141">Notes</span><span class="sxs-lookup"><span data-stu-id="97fa1-141">Remarks</span></span>

<span data-ttu-id="97fa1-142">L’objet **SignedData** peut être créé et il est sécurisé pour les scripts.</span><span class="sxs-lookup"><span data-stu-id="97fa1-142">The **SignedData** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="97fa1-143">Le ProgID de l’objet **SignedData** est CAPICOM. SignedData. 1.</span><span class="sxs-lookup"><span data-stu-id="97fa1-143">The ProgID for the **SignedData** object is CAPICOM.SignedData.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="97fa1-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="97fa1-144">Requirements</span></span>



| <span data-ttu-id="97fa1-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="97fa1-145">Requirement</span></span> | <span data-ttu-id="97fa1-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="97fa1-146">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="97fa1-147">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="97fa1-147">Redistributable</span></span><br/> | <span data-ttu-id="97fa1-148">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="97fa1-148">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="97fa1-149">DLL</span><span class="sxs-lookup"><span data-stu-id="97fa1-149">DLL</span></span><br/>             | <dl> <span data-ttu-id="97fa1-150"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97fa1-150"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97fa1-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="97fa1-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97fa1-152">**Objets de chiffrement**</span><span class="sxs-lookup"><span data-stu-id="97fa1-152">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
