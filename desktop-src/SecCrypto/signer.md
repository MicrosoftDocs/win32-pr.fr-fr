---
description: Établit le signataire d’un objet SignedData ou SignedCode.
ms.assetid: fca6489c-56cf-472f-ac0f-73ba531fa212
title: Objet signataire
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 974341eb996f2b5d3701757a5352ef56e2837390
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539302"
---
# <a name="signer-object"></a><span data-ttu-id="0c673-103">Objet signataire</span><span class="sxs-lookup"><span data-stu-id="0c673-103">Signer object</span></span>

<span data-ttu-id="0c673-104">\[L’objet **signataire** peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="0c673-104">\[The **Signer** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="0c673-105">Utilisez plutôt la [**classe CmsSigner**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="0c673-105">Instead, use the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="0c673-106">L’objet **signataire** établit le signataire d’un objet [**SignedData**](signeddata.md) ou [**SignedCode**](signedcode.md) .</span><span class="sxs-lookup"><span data-stu-id="0c673-106">The **Signer** object establishes the signer of a [**SignedData**](signeddata.md) or [**SignedCode**](signedcode.md) object.</span></span> <span data-ttu-id="0c673-107">Le [**certificat**](certificate.md) de l’objet **signataire** doit avoir une clé privée disponible qui peut être utilisée pour signer des données.</span><span class="sxs-lookup"><span data-stu-id="0c673-107">The [**Certificate**](certificate.md) of the **Signer** object must have an available private key that can be used to sign data.</span></span>

## <a name="members"></a><span data-ttu-id="0c673-108">Membres</span><span class="sxs-lookup"><span data-stu-id="0c673-108">Members</span></span>

<span data-ttu-id="0c673-109">L’objet **signataire** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0c673-109">The **Signer** object has these types of members:</span></span>

-   [<span data-ttu-id="0c673-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0c673-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="0c673-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0c673-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0c673-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0c673-112">Methods</span></span>

<span data-ttu-id="0c673-113">L’objet **signataire** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="0c673-113">The **Signer** object has these methods.</span></span>



| <span data-ttu-id="0c673-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="0c673-114">Method</span></span>                      | <span data-ttu-id="0c673-115">Description</span><span class="sxs-lookup"><span data-stu-id="0c673-115">Description</span></span>                                                       |
|:----------------------------|:------------------------------------------------------------------|
| [<span data-ttu-id="0c673-116">**Load**</span><span class="sxs-lookup"><span data-stu-id="0c673-116">**Load**</span></span>](signer-load.md) | <span data-ttu-id="0c673-117">Charge un certificat de signature à partir d’un fichier PFX spécifié.</span><span class="sxs-lookup"><span data-stu-id="0c673-117">Loads a signing certificate from a specified PFX file.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="0c673-118">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0c673-118">Properties</span></span>

<span data-ttu-id="0c673-119">L’objet **signataire** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="0c673-119">The **Signer** object has these properties.</span></span>



| <span data-ttu-id="0c673-120">Propriété</span><span class="sxs-lookup"><span data-stu-id="0c673-120">Property</span></span>                                                                     | <span data-ttu-id="0c673-121">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="0c673-121">Access type</span></span>           | <span data-ttu-id="0c673-122">Description</span><span class="sxs-lookup"><span data-stu-id="0c673-122">Description</span></span>                                                                                                                                                                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0c673-123">**AuthenticatedAttributes**</span><span class="sxs-lookup"><span data-stu-id="0c673-123">**AuthenticatedAttributes**</span></span>](signer-authenticatedattributes.md)<br/> | <span data-ttu-id="0c673-124">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0c673-124">Read-only</span></span><br/>  | <span data-ttu-id="0c673-125">Collection d’attributs authentifiés.</span><span class="sxs-lookup"><span data-stu-id="0c673-125">The collection of authenticated attributes.</span></span><br/>                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="0c673-126">**Certificat**</span><span class="sxs-lookup"><span data-stu-id="0c673-126">**Certificate**</span></span>](signer-certificate.md)<br/>                         | <span data-ttu-id="0c673-127">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0c673-127">Read/write</span></span><br/> | <span data-ttu-id="0c673-128">Objet de [**certificat**](certificate.md) qui représente le certificat d’un signataire des données.</span><span class="sxs-lookup"><span data-stu-id="0c673-128">The [**Certificate**](certificate.md) object that represents the certificate of a signer of the data.</span></span><br/> <span data-ttu-id="0c673-129">Lorsque la valeur de cette propriété est réinitialisée, directement ou indirectement, l’intégralité de l' [*État*](../secgloss/s-gly.md) de l’objet est réinitialisée.</span><span class="sxs-lookup"><span data-stu-id="0c673-129">When the value of this property is reset, directly or indirectly, the whole [*state*](../secgloss/s-gly.md) of the object is reset.</span></span><br/> <span data-ttu-id="0c673-130">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="0c673-130">This is the default property.</span></span><br/> |
| [<span data-ttu-id="0c673-131">**Mutation**</span><span class="sxs-lookup"><span data-stu-id="0c673-131">**Chain**</span></span>](signer-chain.md)<br/>                                     | <span data-ttu-id="0c673-132">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0c673-132">Read-only</span></span><br/>  | <span data-ttu-id="0c673-133">Chaîne du signataire.</span><span class="sxs-lookup"><span data-stu-id="0c673-133">The chain of the signer.</span></span><br/>                                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="0c673-134">**Options**</span><span class="sxs-lookup"><span data-stu-id="0c673-134">**Options**</span></span>](signer-options.md)<br/>                                 | <span data-ttu-id="0c673-135">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0c673-135">Read/write</span></span><br/> | <span data-ttu-id="0c673-136">Définit ou récupère l’option de certificat du signataire.</span><span class="sxs-lookup"><span data-stu-id="0c673-136">Sets or retrieves the signer's certificate option.</span></span><br/>                                                                                                                                                                                                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="0c673-137">Notes</span><span class="sxs-lookup"><span data-stu-id="0c673-137">Remarks</span></span>

<span data-ttu-id="0c673-138">L’objet **signataire** peut être créé et il est sécurisé pour les scripts.</span><span class="sxs-lookup"><span data-stu-id="0c673-138">The **Signer** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="0c673-139">Le ProgID de l’objet **signataire** est CAPICOM. Signataire. 2.</span><span class="sxs-lookup"><span data-stu-id="0c673-139">The ProgID for the **Signer** object is CAPICOM.Signer.2.</span></span>

<span data-ttu-id="0c673-140">**CAPICOM 1. *x*:** le ProgID de l’objet **signataire** est CAPICOM. Signataire. 1.</span><span class="sxs-lookup"><span data-stu-id="0c673-140">**CAPICOM 1.*x*:** The ProgID for the **Signer** object is CAPICOM.Signer.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c673-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0c673-141">Requirements</span></span>



| <span data-ttu-id="0c673-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0c673-142">Requirement</span></span> | <span data-ttu-id="0c673-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="0c673-143">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0c673-144">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="0c673-144">Redistributable</span></span><br/> | <span data-ttu-id="0c673-145">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="0c673-145">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="0c673-146">DLL</span><span class="sxs-lookup"><span data-stu-id="0c673-146">DLL</span></span><br/>             | <dl> <span data-ttu-id="0c673-147"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c673-147"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c673-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c673-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c673-149">**Objets de chiffrement**</span><span class="sxs-lookup"><span data-stu-id="0c673-149">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
