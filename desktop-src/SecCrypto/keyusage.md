---
description: Fournit un accès en lecture seule aux propriétés d’utilisation de la clé d’un certificat.
ms.assetid: 8b8e9076-1a4f-4383-ac4b-1322d52949f0
title: Objet KeyUsage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5d2324b4e1e06650f2eed7b63337f2bd48520498
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523868"
---
# <a name="keyusage-object"></a><span data-ttu-id="df90f-103">Objet KeyUsage</span><span class="sxs-lookup"><span data-stu-id="df90f-103">KeyUsage object</span></span>

<span data-ttu-id="df90f-104">\[L’objet **KeyUsage** est disponible pour une utilisation dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="df90f-104">\[The **KeyUsage** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="df90f-105">Utilisez plutôt la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="df90f-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="df90f-106">L’objet **KeyUsage** fournit un accès en lecture seule aux propriétés d’utilisation de la clé d’un certificat.</span><span class="sxs-lookup"><span data-stu-id="df90f-106">The **KeyUsage** object provides read-only access to key usage properties of a certificate.</span></span>

## <a name="members"></a><span data-ttu-id="df90f-107">Membres</span><span class="sxs-lookup"><span data-stu-id="df90f-107">Members</span></span>

<span data-ttu-id="df90f-108">L’objet **KeyUsage** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="df90f-108">The **KeyUsage** object has these types of members:</span></span>

-   [<span data-ttu-id="df90f-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="df90f-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="df90f-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="df90f-110">Properties</span></span>

<span data-ttu-id="df90f-111">L’objet **KeyUsage** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="df90f-111">The **KeyUsage** object has these properties.</span></span>



| <span data-ttu-id="df90f-112">Propriété</span><span class="sxs-lookup"><span data-stu-id="df90f-112">Property</span></span>                                                                           | <span data-ttu-id="df90f-113">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="df90f-113">Access type</span></span>          | <span data-ttu-id="df90f-114">Description</span><span class="sxs-lookup"><span data-stu-id="df90f-114">Description</span></span>                                                                                                                                 |
|:-----------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="df90f-115">**IsCritical**</span><span class="sxs-lookup"><span data-stu-id="df90f-115">**IsCritical**</span></span>](keyusage-iscritical.md)<br/>                               | <span data-ttu-id="df90f-116">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df90f-116">Read-only</span></span><br/> | <span data-ttu-id="df90f-117">Récupère une valeur booléenne qui indique si l’extension **KeyUsage** est marquée comme critique.</span><span class="sxs-lookup"><span data-stu-id="df90f-117">Retrieves a Boolean value that indicates whether the **KeyUsage** extension is marked critical.</span></span><br/>                                  |
| [<span data-ttu-id="df90f-118">**IsCRLSignEnabled**</span><span class="sxs-lookup"><span data-stu-id="df90f-118">**IsCRLSignEnabled**</span></span>](keyusage-iscrlsignenabled.md)<br/>                   | <span data-ttu-id="df90f-119">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df90f-119">Read-only</span></span><br/> | <span data-ttu-id="df90f-120">Récupère une valeur booléenne qui indique si le bit bit cRLSign est défini.</span><span class="sxs-lookup"><span data-stu-id="df90f-120">Retrieves a Boolean value that indicates whether the CRLSign bit is set.</span></span><br/>                                                         |
| [<span data-ttu-id="df90f-121">**IsDataEnciphermentEnabled**</span><span class="sxs-lookup"><span data-stu-id="df90f-121">**IsDataEnciphermentEnabled**</span></span>](keyusage-isdataenciphermentenabled.md)<br/> | <span data-ttu-id="df90f-122">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df90f-122">Read-only</span></span><br/> | <span data-ttu-id="df90f-123">Récupère une valeur booléenne qui indique si le bit dataEncipherment est défini.</span><span class="sxs-lookup"><span data-stu-id="df90f-123">Retrieves a Boolean value that indicates whether the dataEncipherment bit is set.</span></span><br/>                                                |
| [<span data-ttu-id="df90f-124">**IsDecipherOnlyEnabled**</span><span class="sxs-lookup"><span data-stu-id="df90f-124">**IsDecipherOnlyEnabled**</span></span>](keyusage-isdecipheronlyenabled.md)<br/>         | <span data-ttu-id="df90f-125">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df90f-125">Read-only</span></span><br/> | <span data-ttu-id="df90f-126">Récupère une valeur booléenne qui indique si le bit decipherOnly est défini.</span><span class="sxs-lookup"><span data-stu-id="df90f-126">Retrieves a Boolean value that indicates whether the decipherOnly bit is set.</span></span><br/>                                                    |
| [<span data-ttu-id="df90f-127">**IsDigitalSignatureEnabled**</span><span class="sxs-lookup"><span data-stu-id="df90f-127">**IsDigitalSignatureEnabled**</span></span>](keyusage-isdigitalsignatureenabled.md)<br/> | <span data-ttu-id="df90f-128">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df90f-128">Read-only</span></span><br/> | <span data-ttu-id="df90f-129">Récupère une valeur booléenne qui indique si le bit digitalSignature est défini.</span><span class="sxs-lookup"><span data-stu-id="df90f-129">Retrieves a Boolean value that indicates whether the digitalSignature bit is set.</span></span><br/>                                                |
| [<span data-ttu-id="df90f-130">**IsEncipherOnlyEnabled**</span><span class="sxs-lookup"><span data-stu-id="df90f-130">**IsEncipherOnlyEnabled**</span></span>](keyusage-isencipheronlyenabled.md)<br/>         | <span data-ttu-id="df90f-131">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df90f-131">Read-only</span></span><br/> | <span data-ttu-id="df90f-132">Récupère une valeur booléenne qui indique si le bit encipherOnly est défini.</span><span class="sxs-lookup"><span data-stu-id="df90f-132">Retrieves a Boolean value that indicates whether the encipherOnly bit is set.</span></span><br/>                                                    |
| [<span data-ttu-id="df90f-133">**IsKeyAgreementEnabled**</span><span class="sxs-lookup"><span data-stu-id="df90f-133">**IsKeyAgreementEnabled**</span></span>](keyusage-iskeyagreementenabled.md)<br/>         | <span data-ttu-id="df90f-134">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df90f-134">Read-only</span></span><br/> | <span data-ttu-id="df90f-135">Récupère une valeur booléenne qui indique si le bit keyAgreement est défini.</span><span class="sxs-lookup"><span data-stu-id="df90f-135">Retrieves a Boolean value that indicates whether the keyAgreement bit is set.</span></span><br/>                                                    |
| [<span data-ttu-id="df90f-136">**IsKeyCertSignEnabled**</span><span class="sxs-lookup"><span data-stu-id="df90f-136">**IsKeyCertSignEnabled**</span></span>](keyusage-iskeycertsignenabled.md)<br/>           | <span data-ttu-id="df90f-137">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df90f-137">Read-only</span></span><br/> | <span data-ttu-id="df90f-138">Récupère une valeur booléenne qui indique si le bit bit keyCertSign est défini.</span><span class="sxs-lookup"><span data-stu-id="df90f-138">Retrieves a Boolean value that indicates whether the keyCertSign bit is set.</span></span><br/>                                                     |
| [<span data-ttu-id="df90f-139">**IsKeyEnciphermentEnabled**</span><span class="sxs-lookup"><span data-stu-id="df90f-139">**IsKeyEnciphermentEnabled**</span></span>](keyusage-iskeyenciphermentenabled.md)<br/>   | <span data-ttu-id="df90f-140">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df90f-140">Read-only</span></span><br/> | <span data-ttu-id="df90f-141">Récupère une valeur booléenne qui indique si le bit keyEncipherment est défini.</span><span class="sxs-lookup"><span data-stu-id="df90f-141">Retrieves a Boolean value that indicates whether the keyEncipherment bit is set.</span></span><br/>                                                 |
| [<span data-ttu-id="df90f-142">**IsNonRepudiationEnabled**</span><span class="sxs-lookup"><span data-stu-id="df90f-142">**IsNonRepudiationEnabled**</span></span>](keyusage-isnonrepudiationenabled.md)<br/>     | <span data-ttu-id="df90f-143">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df90f-143">Read-only</span></span><br/> | <span data-ttu-id="df90f-144">Récupère une valeur booléenne qui indique si le bit nonRepudiationEnabled est défini.</span><span class="sxs-lookup"><span data-stu-id="df90f-144">Retrieves a Boolean value that indicates whether the nonRepudiationEnabled bit is set.</span></span><br/>                                           |
| [<span data-ttu-id="df90f-145">**IsPresent**</span><span class="sxs-lookup"><span data-stu-id="df90f-145">**IsPresent**</span></span>](keyusage-ispresent.md)<br/>                                 | <span data-ttu-id="df90f-146">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df90f-146">Read-only</span></span><br/> | <span data-ttu-id="df90f-147">Récupère une valeur booléenne qui indique si l’extension **KeyUsage** est présente.</span><span class="sxs-lookup"><span data-stu-id="df90f-147">Retrieves a Boolean value that indicates whether the **KeyUsage** extension is present.</span></span><br/> <span data-ttu-id="df90f-148">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="df90f-148">This is the default property.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="df90f-149">Notes</span><span class="sxs-lookup"><span data-stu-id="df90f-149">Remarks</span></span>

<span data-ttu-id="df90f-150">Impossible de créer l’objet **KeyUsage** .</span><span class="sxs-lookup"><span data-stu-id="df90f-150">The **KeyUsage** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="df90f-151">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="df90f-151">Requirements</span></span>



| <span data-ttu-id="df90f-152">Condition requise</span><span class="sxs-lookup"><span data-stu-id="df90f-152">Requirement</span></span> | <span data-ttu-id="df90f-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="df90f-153">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="df90f-154">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="df90f-154">Redistributable</span></span><br/> | <span data-ttu-id="df90f-155">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="df90f-155">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="df90f-156">DLL</span><span class="sxs-lookup"><span data-stu-id="df90f-156">DLL</span></span><br/>             | <dl> <span data-ttu-id="df90f-157"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df90f-157"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df90f-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df90f-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df90f-159">**Objets de chiffrement**</span><span class="sxs-lookup"><span data-stu-id="df90f-159">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
