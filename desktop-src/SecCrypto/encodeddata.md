---
description: Représente un bloc de données encodées ASN. 1.
ms.assetid: af7acc5f-da0a-4235-8496-05db94664ea5
title: Objet EncodedData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncodedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d05fce31ad4ef08bf9f573c0158a683bdbeba739
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530025"
---
# <a name="encodeddata-object"></a><span data-ttu-id="279cf-103">Objet EncodedData</span><span class="sxs-lookup"><span data-stu-id="279cf-103">EncodedData object</span></span>

<span data-ttu-id="279cf-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="279cf-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="279cf-105">Utilisez plutôt la [**classe AsnEncodedData**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="279cf-105">Instead, use the [**AsnEncodedData Class**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="279cf-106">L’objet **EncodedData** représente un bloc de données encodées ASN. 1.</span><span class="sxs-lookup"><span data-stu-id="279cf-106">The **EncodedData** object represents a block of ASN.1 encoded data.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="279cf-107">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="279cf-107">When to use</span></span>

<span data-ttu-id="279cf-108">L’objet **EncodedData** est retourné par plusieurs propriétés de l’objet CAPICOM.</span><span class="sxs-lookup"><span data-stu-id="279cf-108">The **EncodedData** object is returned by several CAPICOM object properties.</span></span> <span data-ttu-id="279cf-109">Une fois retourné, cet objet est utilisé pour effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="279cf-109">When returned, this object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="279cf-110">Obtient une représentation sous forme de chaîne des données encodées.</span><span class="sxs-lookup"><span data-stu-id="279cf-110">Obtain a string representation of the encoded data.</span></span>
-   <span data-ttu-id="279cf-111">Obtenez l’objet décodeur, s’il existe, qui est associé aux données encodées.</span><span class="sxs-lookup"><span data-stu-id="279cf-111">Obtain the decoder object, if it exists, that is associated with the encoded data.</span></span>
-   <span data-ttu-id="279cf-112">Déterminez le type de données encodées.</span><span class="sxs-lookup"><span data-stu-id="279cf-112">Determine the type of encoded data.</span></span>

## <a name="members"></a><span data-ttu-id="279cf-113">Membres</span><span class="sxs-lookup"><span data-stu-id="279cf-113">Members</span></span>

<span data-ttu-id="279cf-114">L’objet **EncodedData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="279cf-114">The **EncodedData** object has these types of members:</span></span>

-   [<span data-ttu-id="279cf-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="279cf-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="279cf-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="279cf-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="279cf-117">Méthodes</span><span class="sxs-lookup"><span data-stu-id="279cf-117">Methods</span></span>

<span data-ttu-id="279cf-118">L’objet **EncodedData** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="279cf-118">The **EncodedData** object has these methods.</span></span>



| <span data-ttu-id="279cf-119">Méthode</span><span class="sxs-lookup"><span data-stu-id="279cf-119">Method</span></span>                                 | <span data-ttu-id="279cf-120">Description</span><span class="sxs-lookup"><span data-stu-id="279cf-120">Description</span></span>                                                     |
|:---------------------------------------|:----------------------------------------------------------------|
| [<span data-ttu-id="279cf-121">**Décodeur**</span><span class="sxs-lookup"><span data-stu-id="279cf-121">**Decoder**</span></span>](encodeddata-decoder.md) | <span data-ttu-id="279cf-122">Obtient un objet décodeur, s’il en existe un.</span><span class="sxs-lookup"><span data-stu-id="279cf-122">Obtains a decoder object, if one exists.</span></span><br/>             |
| [<span data-ttu-id="279cf-123">**Format**</span><span class="sxs-lookup"><span data-stu-id="279cf-123">**Format**</span></span>](encodeddata-format.md)   | <span data-ttu-id="279cf-124">Retourne une représentation sous forme de chaîne des données encodées.</span><span class="sxs-lookup"><span data-stu-id="279cf-124">Returns a string representation of the encoded data.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="279cf-125">Propriétés</span><span class="sxs-lookup"><span data-stu-id="279cf-125">Properties</span></span>

<span data-ttu-id="279cf-126">L’objet **EncodedData** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="279cf-126">The **EncodedData** object has these properties.</span></span>



| <span data-ttu-id="279cf-127">Propriété</span><span class="sxs-lookup"><span data-stu-id="279cf-127">Property</span></span>                                      | <span data-ttu-id="279cf-128">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="279cf-128">Access type</span></span>          | <span data-ttu-id="279cf-129">Description</span><span class="sxs-lookup"><span data-stu-id="279cf-129">Description</span></span>                                                          |
|:----------------------------------------------|:---------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="279cf-130">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="279cf-130">**Value**</span></span>](encodeddata-value.md)<br/> | <span data-ttu-id="279cf-131">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="279cf-131">Read-only</span></span><br/> | <span data-ttu-id="279cf-132">Récupère les données encodées.</span><span class="sxs-lookup"><span data-stu-id="279cf-132">Retrieves the encoded data.</span></span> <span data-ttu-id="279cf-133">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="279cf-133">This is the default property.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="279cf-134">Notes</span><span class="sxs-lookup"><span data-stu-id="279cf-134">Remarks</span></span>

<span data-ttu-id="279cf-135">Le seul type de données encodées pris en charge est [**certificatePolicies**](certificatepolicies.md).</span><span class="sxs-lookup"><span data-stu-id="279cf-135">The only supported type of encoded data is [**CertificatePolicies**](certificatepolicies.md).</span></span>

<span data-ttu-id="279cf-136">Impossible de créer l’objet **EncodedData** .</span><span class="sxs-lookup"><span data-stu-id="279cf-136">The **EncodedData** object cannot be created.</span></span>

<span data-ttu-id="279cf-137">Les propriétés suivantes de l’objet CAPICOM retournent un objet **EncodedData** :</span><span class="sxs-lookup"><span data-stu-id="279cf-137">The following CAPICOM object properties return an **EncodedData** object:</span></span>

-   <span data-ttu-id="279cf-138">**PublicKey. EncodedKey**</span><span class="sxs-lookup"><span data-stu-id="279cf-138">**PublicKey.EncodedKey**</span></span>
-   <span data-ttu-id="279cf-139">**PublicKey. EncodedParameters**</span><span class="sxs-lookup"><span data-stu-id="279cf-139">**PublicKey.EncodedParameters**</span></span>
-   <span data-ttu-id="279cf-140">**Extension. EncodedData**</span><span class="sxs-lookup"><span data-stu-id="279cf-140">**Extension.EncodedData**</span></span>
-   <span data-ttu-id="279cf-141">**Policy. EncodedData**</span><span class="sxs-lookup"><span data-stu-id="279cf-141">**Policy.EncodedData**</span></span>

## <a name="requirements"></a><span data-ttu-id="279cf-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="279cf-142">Requirements</span></span>



| <span data-ttu-id="279cf-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="279cf-143">Requirement</span></span> | <span data-ttu-id="279cf-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="279cf-144">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="279cf-145">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="279cf-145">End of client support</span></span><br/> | <span data-ttu-id="279cf-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="279cf-146">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="279cf-147">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="279cf-147">End of server support</span></span><br/> | <span data-ttu-id="279cf-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="279cf-148">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="279cf-149">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="279cf-149">Redistributable</span></span><br/>       | <span data-ttu-id="279cf-150">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="279cf-150">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="279cf-151">DLL</span><span class="sxs-lookup"><span data-stu-id="279cf-151">DLL</span></span><br/>                   | <dl> <span data-ttu-id="279cf-152"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="279cf-152"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
