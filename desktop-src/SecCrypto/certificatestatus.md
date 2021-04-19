---
description: Contient des informations sur la façon de construire une chaîne d’approbation de certificat.
ms.assetid: 120cd79e-7c9b-45f3-8596-091b674e73d8
title: Objet CertificateStatus
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e9a6cb31a00f4d2943e68670930e6cbc4436b6b1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537434"
---
# <a name="certificatestatus-object"></a><span data-ttu-id="0be17-103">Objet CertificateStatus</span><span class="sxs-lookup"><span data-stu-id="0be17-103">CertificateStatus object</span></span>

<span data-ttu-id="0be17-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0be17-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="0be17-105">Utilisez plutôt la [**structure X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="0be17-105">Instead, use the [**X509ChainStatus Structure**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="0be17-106">L’objet **CertificateStatus** contient des informations sur la façon de construire une chaîne d’approbation de certificat.</span><span class="sxs-lookup"><span data-stu-id="0be17-106">The **CertificateStatus** object contains information about how to construct a certificate trust chain.</span></span>

## <a name="members"></a><span data-ttu-id="0be17-107">Membres</span><span class="sxs-lookup"><span data-stu-id="0be17-107">Members</span></span>

<span data-ttu-id="0be17-108">L’objet **CertificateStatus** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0be17-108">The **CertificateStatus** object has these types of members:</span></span>

-   [<span data-ttu-id="0be17-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0be17-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="0be17-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0be17-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0be17-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0be17-111">Methods</span></span>

<span data-ttu-id="0be17-112">L’objet **CertificateStatus** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="0be17-112">The **CertificateStatus** object has these methods.</span></span>



| <span data-ttu-id="0be17-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="0be17-113">Method</span></span>                                                               | <span data-ttu-id="0be17-114">Description</span><span class="sxs-lookup"><span data-stu-id="0be17-114">Description</span></span>                                                                                                                                  |
|:---------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0be17-115">**ApplicationPolicies**</span><span class="sxs-lookup"><span data-stu-id="0be17-115">**ApplicationPolicies**</span></span>](certificatestatus-applicationpolicies.md) | <span data-ttu-id="0be17-116">Retourne une collection d' [**OID**](oids.md) qui représente les OID de stratégie d’application.</span><span class="sxs-lookup"><span data-stu-id="0be17-116">Returns an [**OIDs**](oids.md) collection that represents the application policy OIDs.</span></span><br/>                                           |
| [<span data-ttu-id="0be17-117">**CertificatePolicies**</span><span class="sxs-lookup"><span data-stu-id="0be17-117">**CertificatePolicies**</span></span>](certificatestatus-certificatepolicies.md) | <span data-ttu-id="0be17-118">Retourne une collection d' [**OID**](oids.md) qui représente les OID de stratégie de certificat utilisés pendant la génération de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="0be17-118">Returns an [**OIDs**](oids.md) collection that represents the certificate policy OIDs used during chain building.</span></span><br/>                |
| [<span data-ttu-id="0be17-119">**EKU**</span><span class="sxs-lookup"><span data-stu-id="0be17-119">**EKU**</span></span>](certificatestatus-eku.md)                                 | <span data-ttu-id="0be17-120">Retourne l’objet [**EKU**](eku.md) utilisé pour définir les éléments EKU à vérifier lors de l’établissement de l’état de validité d’un certificat.</span><span class="sxs-lookup"><span data-stu-id="0be17-120">Returns the [**EKU**](eku.md) object used to set the EKU elements to be checked in establishing a certificate's validity status.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="0be17-121">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0be17-121">Properties</span></span>

<span data-ttu-id="0be17-122">L’objet **CertificateStatus** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="0be17-122">The **CertificateStatus** object has these properties.</span></span>



| <span data-ttu-id="0be17-123">Propriété</span><span class="sxs-lookup"><span data-stu-id="0be17-123">Property</span></span>                                                                        | <span data-ttu-id="0be17-124">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="0be17-124">Access type</span></span>           | <span data-ttu-id="0be17-125">Description</span><span class="sxs-lookup"><span data-stu-id="0be17-125">Description</span></span>                                                                                                                                                                                                                                                       |
|:--------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0be17-126">**Certificats**</span><span class="sxs-lookup"><span data-stu-id="0be17-126">**Certificates**</span></span>](certificatestatus-certificates.md)<br/>               | <span data-ttu-id="0be17-127">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0be17-127">Read/write</span></span><br/> | <span data-ttu-id="0be17-128">Définit ou récupère la collection de certificats qui peuvent être utilisés pour créer la chaîne de certificats.</span><span class="sxs-lookup"><span data-stu-id="0be17-128">Sets or retrieves the collection of certificates that can be used to build the certificate chain.</span></span><br/> <span data-ttu-id="0be17-129">**CAPICOM 2.0.0.3 et versions antérieures :** La propriété des [**certificats**](certificatestatus-certificates.md) n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="0be17-129">**CAPICOM 2.0.0.3 and earlier:** The [**Certificates**](certificatestatus-certificates.md) property is not supported.</span></span><br/>                    |
| [<span data-ttu-id="0be17-130">**CheckFlag**</span><span class="sxs-lookup"><span data-stu-id="0be17-130">**CheckFlag**</span></span>](certificatestatus-checkflag.md)<br/>                     | <span data-ttu-id="0be17-131">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0be17-131">Read/write</span></span><br/> | <span data-ttu-id="0be17-132">Indicateur de contrôle de validité.</span><span class="sxs-lookup"><span data-stu-id="0be17-132">Validity check flag.</span></span> <span data-ttu-id="0be17-133">Les valeurs peuvent être jointes à l’aide d’un opérateur **or** logique.</span><span class="sxs-lookup"><span data-stu-id="0be17-133">Values can be joined by using a logical **OR** operator.</span></span> <span data-ttu-id="0be17-134">L’indicateur de vérification par défaut est [**CAPICOM \_ vérifier \_ en \_ ligne**](capicom-check-flag.md).</span><span class="sxs-lookup"><span data-stu-id="0be17-134">The default check flag is [**CAPICOM\_CHECK\_ONLINE\_ALL**](capicom-check-flag.md).</span></span><br/>                                                                                     |
| [<span data-ttu-id="0be17-135">**Venir**</span><span class="sxs-lookup"><span data-stu-id="0be17-135">**Result**</span></span>](certificatestatus-result.md)<br/>                           | <span data-ttu-id="0be17-136">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0be17-136">Read-only</span></span><br/>  | <span data-ttu-id="0be17-137">Indique si le certificat est valide.</span><span class="sxs-lookup"><span data-stu-id="0be17-137">Indicates whether the certificate is valid.</span></span> <span data-ttu-id="0be17-138">La validité du certificat est vérifiée à l’aide de la valeur actuelle de la propriété [**CheckFlag**](certificatestatus-checkflag.md) et des paramètres de stratégie du certificat.</span><span class="sxs-lookup"><span data-stu-id="0be17-138">The certificate's validity is checked using the current setting of the [**CheckFlag**](certificatestatus-checkflag.md) property and the policy settings of the certificate.</span></span> <span data-ttu-id="0be17-139">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="0be17-139">This is the default property.</span></span><br/> |
| [<span data-ttu-id="0be17-140">**UrlRetrievalTimeout**</span><span class="sxs-lookup"><span data-stu-id="0be17-140">**UrlRetrievalTimeout**</span></span>](certificatestatus-urlretrievaltimeout.md)<br/> | <span data-ttu-id="0be17-141">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0be17-141">Read/write</span></span><br/> | <span data-ttu-id="0be17-142">Définit ou récupère la durée pendant laquelle une URL est déterminée pour être inaccessible.</span><span class="sxs-lookup"><span data-stu-id="0be17-142">Sets or retrieves the length of time before a URL is determined to be unreachable.</span></span><br/>                                                                                                                                                                     |
| [<span data-ttu-id="0be17-143">**VerificationTime**</span><span class="sxs-lookup"><span data-stu-id="0be17-143">**VerificationTime**</span></span>](certificatestatus-verificationtime.md)<br/>       | <span data-ttu-id="0be17-144">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0be17-144">Read/write</span></span><br/> | <span data-ttu-id="0be17-145">Définit ou récupère l’heure à laquelle le certificat a été vérifié.</span><span class="sxs-lookup"><span data-stu-id="0be17-145">Sets or retrieves the time that the certificate was verified.</span></span><br/>                                                                                                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="0be17-146">Notes</span><span class="sxs-lookup"><span data-stu-id="0be17-146">Remarks</span></span>

<span data-ttu-id="0be17-147">Impossible de créer l’objet **CertificateStatus** .</span><span class="sxs-lookup"><span data-stu-id="0be17-147">The **CertificateStatus** object cannot be created.</span></span>

<span data-ttu-id="0be17-148">L’objet **CertificateStatus** est retourné par la méthode [**Certificate. IsValid**](certificate-isvalid.md) .</span><span class="sxs-lookup"><span data-stu-id="0be17-148">The **CertificateStatus** object is returned by the [**Certificate.IsValid**](certificate-isvalid.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0be17-149">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0be17-149">Requirements</span></span>



| <span data-ttu-id="0be17-150">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0be17-150">Requirement</span></span> | <span data-ttu-id="0be17-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="0be17-151">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0be17-152">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="0be17-152">End of client support</span></span><br/> | <span data-ttu-id="0be17-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0be17-153">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="0be17-154">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="0be17-154">End of server support</span></span><br/> | <span data-ttu-id="0be17-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0be17-155">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="0be17-156">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="0be17-156">Redistributable</span></span><br/>       | <span data-ttu-id="0be17-157">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="0be17-157">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="0be17-158">DLL</span><span class="sxs-lookup"><span data-stu-id="0be17-158">DLL</span></span><br/>                   | <dl> <span data-ttu-id="0be17-159"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0be17-159"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0be17-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0be17-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0be17-161">**Objets de chiffrement**</span><span class="sxs-lookup"><span data-stu-id="0be17-161">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="0be17-162">**Mutation**</span><span class="sxs-lookup"><span data-stu-id="0be17-162">**Chain**</span></span>](chain.md)
</dt> </dl>

 

 
