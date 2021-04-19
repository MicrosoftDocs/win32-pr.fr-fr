---
description: Représente une chaîne d’approbation de certificat.
ms.assetid: 45ed686f-4a7f-4df9-8366-98b825c3c657
title: Chaîne (objet)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Chain
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5fa3432767ccfdb60a2e3bc0a50ddbbcf565e0aa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545428"
---
# <a name="chain-object"></a><span data-ttu-id="78897-103">Chaîne (objet)</span><span class="sxs-lookup"><span data-stu-id="78897-103">Chain object</span></span>

<span data-ttu-id="78897-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="78897-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="78897-105">Utilisez plutôt la [**classe X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="78897-105">Instead, use the [**X509Chain Class**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="78897-106">L’objet **chaîne** représente une chaîne d’approbation de certificat.</span><span class="sxs-lookup"><span data-stu-id="78897-106">The **Chain** object represents a certificate trust chain.</span></span>

<span data-ttu-id="78897-107">Cet objet fournit des propriétés et des méthodes pour générer une chaîne d’approbation de certificat afin de vérifier la validité des certificats.</span><span class="sxs-lookup"><span data-stu-id="78897-107">This object provides properties and methods to build a certificate trust chain to check the validity of certificates.</span></span> <span data-ttu-id="78897-108">La chaîne est créée à l’aide de la valeur de la propriété [**CertificateStatus. CheckFlag**](certificatestatus-checkflag.md) et des paramètres de stratégie d’un objet [**CertificateStatus**](certificatestatus.md) .</span><span class="sxs-lookup"><span data-stu-id="78897-108">The chain is built using the [**CertificateStatus.CheckFlag**](certificatestatus-checkflag.md) property value and the policy settings of a [**CertificateStatus**](certificatestatus.md) object.</span></span>

<span data-ttu-id="78897-109">L’objet **chaîne** expose les interfaces suivantes :</span><span class="sxs-lookup"><span data-stu-id="78897-109">The **Chain** object exposes the following interfaces:</span></span>

-   <span data-ttu-id="78897-110">**IChain2**: introduit dans CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="78897-110">**IChain2**: Introduced in CAPICOM 2.0.</span></span>
-   <span data-ttu-id="78897-111">**IChain**: introduit dans CAPICOM 1,0.</span><span class="sxs-lookup"><span data-stu-id="78897-111">**IChain**: Introduced in CAPICOM 1.0.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="78897-112">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="78897-112">When to use</span></span>

<span data-ttu-id="78897-113">L’objet de **chaîne** est utilisé pour effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="78897-113">The **Chain** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="78897-114">Créer une chaîne d’approbation de certificat.</span><span class="sxs-lookup"><span data-stu-id="78897-114">Build a certificate trust chain.</span></span>
-   <span data-ttu-id="78897-115">Obtenez les OID de toutes les stratégies d’application et de certificat valides pour la chaîne.</span><span class="sxs-lookup"><span data-stu-id="78897-115">Obtain the OIDs of all the certificate and application policies valid for the chain.</span></span>
-   <span data-ttu-id="78897-116">Vérifiez l’état des certificats dans la chaîne.</span><span class="sxs-lookup"><span data-stu-id="78897-116">Verify the status of the certificates in the chain.</span></span>
-   <span data-ttu-id="78897-117">Obtenir des informations d’erreur étendues.</span><span class="sxs-lookup"><span data-stu-id="78897-117">Obtain extended error information.</span></span>
-   <span data-ttu-id="78897-118">Récupérez la collection de certificats dans la chaîne.</span><span class="sxs-lookup"><span data-stu-id="78897-118">Retrieve the collection of certificates in the chain.</span></span>

## <a name="members"></a><span data-ttu-id="78897-119">Membres</span><span class="sxs-lookup"><span data-stu-id="78897-119">Members</span></span>

<span data-ttu-id="78897-120">L’objet de **chaîne** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="78897-120">The **Chain** object has these types of members:</span></span>

-   [<span data-ttu-id="78897-121">Méthodes</span><span class="sxs-lookup"><span data-stu-id="78897-121">Methods</span></span>](#methods)
-   [<span data-ttu-id="78897-122">Propriétés</span><span class="sxs-lookup"><span data-stu-id="78897-122">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="78897-123">Méthodes</span><span class="sxs-lookup"><span data-stu-id="78897-123">Methods</span></span>

<span data-ttu-id="78897-124">L’objet de **chaîne** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="78897-124">The **Chain** object has these methods.</span></span>



| <span data-ttu-id="78897-125">Méthode</span><span class="sxs-lookup"><span data-stu-id="78897-125">Method</span></span>                                                   | <span data-ttu-id="78897-126">Description</span><span class="sxs-lookup"><span data-stu-id="78897-126">Description</span></span>                                                                                                                                                                                                                                                                                                       |
|:---------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="78897-127">**ApplicationPolicies**</span><span class="sxs-lookup"><span data-stu-id="78897-127">**ApplicationPolicies**</span></span>](chain-applicationpolicies.md) | <span data-ttu-id="78897-128">Retourne une collection d' [**OID**](oids.md) qui représente les OID de stratégie d’application valides pour la chaîne.</span><span class="sxs-lookup"><span data-stu-id="78897-128">Returns an [**OIDs**](oids.md) collection that represents the application policy OIDs valid for the chain.</span></span><br/> <span data-ttu-id="78897-129">(Héritée de **ChainIChain2**)</span><span class="sxs-lookup"><span data-stu-id="78897-129">(Inherited from **ChainIChain2**)</span></span>                                                                                                                                                          |
| [<span data-ttu-id="78897-130">**Build**</span><span class="sxs-lookup"><span data-stu-id="78897-130">**Build**</span></span>](chain-build.md)                             | <span data-ttu-id="78897-131">Génère une chaîne de vérification de certificat à partir d’un certificat de fin vers le [*certificat racine*](../secgloss/r-gly.md)approuvé, en retournant une valeur booléenne qui indique la validité globale de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="78897-131">Builds a certificate verification chain from an end certificate to the trusted [*root certificate*](../secgloss/r-gly.md), returning a Boolean value that indicates the overall validity of the chain.</span></span><br/> <span data-ttu-id="78897-132">(Héritée de **ChainIChain2IChain**)</span><span class="sxs-lookup"><span data-stu-id="78897-132">(Inherited from **ChainIChain2IChain**)</span></span> |
| [<span data-ttu-id="78897-133">**CertificatePolicies**</span><span class="sxs-lookup"><span data-stu-id="78897-133">**CertificatePolicies**</span></span>](chain-certificatepolicies.md) | <span data-ttu-id="78897-134">Retourne une collection d' [**OID**](oids.md) qui représente les OID de stratégie de certificat valides pour la chaîne.</span><span class="sxs-lookup"><span data-stu-id="78897-134">Returns an [**OIDs**](oids.md) collection that represents the certificate policy OIDs valid for the chain.</span></span><br/> <span data-ttu-id="78897-135">(Héritée de **ChainIChain2**)</span><span class="sxs-lookup"><span data-stu-id="78897-135">(Inherited from **ChainIChain2**)</span></span>                                                                                                                                                          |
| [<span data-ttu-id="78897-136">**ExtendedErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="78897-136">**ExtendedErrorInfo**</span></span>](chain-extendederrorinfo.md)     | <span data-ttu-id="78897-137">Retourne une chaîne qui contient des informations d’erreur supplémentaires sur l’entrée indexée.</span><span class="sxs-lookup"><span data-stu-id="78897-137">Returns a string that contains additional error information about the indexed entry.</span></span><br/> <span data-ttu-id="78897-138">(Héritée de **ChainIChain2**)</span><span class="sxs-lookup"><span data-stu-id="78897-138">(Inherited from **ChainIChain2**)</span></span>                                                                                                                                                                                 |



 

### <a name="properties"></a><span data-ttu-id="78897-139">Propriétés</span><span class="sxs-lookup"><span data-stu-id="78897-139">Properties</span></span>

<span data-ttu-id="78897-140">L’objet de **chaîne** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="78897-140">The **Chain** object has these properties.</span></span>



| <span data-ttu-id="78897-141">Propriété</span><span class="sxs-lookup"><span data-stu-id="78897-141">Property</span></span>                                              | <span data-ttu-id="78897-142">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="78897-142">Access type</span></span>          | <span data-ttu-id="78897-143">Description</span><span class="sxs-lookup"><span data-stu-id="78897-143">Description</span></span>                                                                                                                                                                                 |
|:------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="78897-144">**Certificats**</span><span class="sxs-lookup"><span data-stu-id="78897-144">**Certificates**</span></span>](chain-certificates.md)<br/> | <span data-ttu-id="78897-145">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="78897-145">Read-only</span></span><br/> | <span data-ttu-id="78897-146">Récupère une collection de [**certificats**](certificates.md) qui représente les certificats dans la chaîne.</span><span class="sxs-lookup"><span data-stu-id="78897-146">Retrieves a [**Certificates**](certificates.md) collection that represents the certificates in the chain.</span></span> <span data-ttu-id="78897-147">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="78897-147">This is the default property.</span></span><br/> <span data-ttu-id="78897-148">(Héritée de **ChainIChain2IChain**)</span><span class="sxs-lookup"><span data-stu-id="78897-148">(Inherited from **ChainIChain2IChain**)</span></span> |
| [<span data-ttu-id="78897-149">**Statu**</span><span class="sxs-lookup"><span data-stu-id="78897-149">**Status**</span></span>](chain-status.md)<br/>             | <span data-ttu-id="78897-150">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="78897-150">Read-only</span></span><br/> | <span data-ttu-id="78897-151">Récupère l’état de validité de la chaîne ou d’un certificat spécifique dans la chaîne.</span><span class="sxs-lookup"><span data-stu-id="78897-151">Retrieves the validity status of the chain or a specific certificate in the chain.</span></span><br/> <span data-ttu-id="78897-152">(Héritée de **ChainIChain2IChain**)</span><span class="sxs-lookup"><span data-stu-id="78897-152">(Inherited from **ChainIChain2IChain**)</span></span>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="78897-153">Notes</span><span class="sxs-lookup"><span data-stu-id="78897-153">Remarks</span></span>

<span data-ttu-id="78897-154">L’objet de **chaîne** peut être créé et il est sécurisé pour les scripts.</span><span class="sxs-lookup"><span data-stu-id="78897-154">The **Chain** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="78897-155">Le ProgID de l’objet **chaîne** est «CAPICOM. Chaîne. 2».</span><span class="sxs-lookup"><span data-stu-id="78897-155">The ProgID for the **Chain** object is "CAPICOM.Chain.2".</span></span>

<span data-ttu-id="78897-156">**CAPICOM 1. *x*:** le ProgID de l’objet **chaîne** est CAPICOM. Chaîne. 1.</span><span class="sxs-lookup"><span data-stu-id="78897-156">**CAPICOM 1.*x*:** The ProgID for the **Chain** object is CAPICOM.Chain.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="78897-157">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="78897-157">Requirements</span></span>



| <span data-ttu-id="78897-158">Condition requise</span><span class="sxs-lookup"><span data-stu-id="78897-158">Requirement</span></span> | <span data-ttu-id="78897-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="78897-159">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="78897-160">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="78897-160">End of client support</span></span><br/> | <span data-ttu-id="78897-161">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="78897-161">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="78897-162">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="78897-162">End of server support</span></span><br/> | <span data-ttu-id="78897-163">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="78897-163">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="78897-164">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="78897-164">Redistributable</span></span><br/>       | <span data-ttu-id="78897-165">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="78897-165">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="78897-166">DLL</span><span class="sxs-lookup"><span data-stu-id="78897-166">DLL</span></span><br/>                   | <dl> <span data-ttu-id="78897-167"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78897-167"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78897-168">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="78897-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78897-169">**Objets de chiffrement**</span><span class="sxs-lookup"><span data-stu-id="78897-169">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
