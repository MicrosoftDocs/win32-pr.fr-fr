---
description: 'Certificates, objet : représente une collection d’objets de certificat.'
ms.assetid: 82011c49-38fb-4261-8fb3-b76859da8a9e
title: Objet Certificates
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 8efb9221f39b8544eabe8f6c00d21f6cfdf20c14
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098387"
---
# <a name="certificates-object"></a><span data-ttu-id="2a7de-103">Objet Certificates</span><span class="sxs-lookup"><span data-stu-id="2a7de-103">Certificates object</span></span>

<span data-ttu-id="2a7de-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2a7de-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="2a7de-105">Utilisez plutôt la [**classe X509Certificate2Collection**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="2a7de-105">Instead, use the [**X509Certificate2Collection Class**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="2a7de-106">L' **objet** [**Certificates**](certificate.md) représente une collection d’objets de certificat.</span><span class="sxs-lookup"><span data-stu-id="2a7de-106">The **Certificates** object represents a collection of [**Certificate**](certificate.md) objects.</span></span> <span data-ttu-id="2a7de-107">Chaque objet [**certificat**](certificate.md) représente un seul [*certificat numérique*](../secgloss/d-gly.md).</span><span class="sxs-lookup"><span data-stu-id="2a7de-107">Each [**Certificate**](certificate.md) object represents a single [*digital certificate*](../secgloss/d-gly.md).</span></span>

<span data-ttu-id="2a7de-108">L’objet **Certificates** expose les interfaces suivantes :</span><span class="sxs-lookup"><span data-stu-id="2a7de-108">The **Certificates** object exposes the following interfaces:</span></span>

-   <span data-ttu-id="2a7de-109">**ICertificates2**: introduit dans CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="2a7de-109">**ICertificates2**: Introduced in CAPICOM 2.0.</span></span>
-   <span data-ttu-id="2a7de-110">**ICertificates**: introduit dans CAPICOM 1,0.</span><span class="sxs-lookup"><span data-stu-id="2a7de-110">**ICertificates**: Introduced in CAPICOM 1.0.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="2a7de-111">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="2a7de-111">When to use</span></span>

<span data-ttu-id="2a7de-112">L’objet **Certificates** est utilisé pour effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="2a7de-112">The **Certificates** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="2a7de-113">Ajoutez ou supprimez un objet de [**certificat**](certificate.md) à partir de la collection.</span><span class="sxs-lookup"><span data-stu-id="2a7de-113">Add or remove a [**Certificate**](certificate.md) object to or from the collection.</span></span>
-   <span data-ttu-id="2a7de-114">Générez un sous-ensemble de la collection en recherchant un ensemble de certificats ou en affichant une boîte de dialogue pour sélectionner les certificats.</span><span class="sxs-lookup"><span data-stu-id="2a7de-114">Generate a subset of the collection by finding a set of certificates or by displaying a dialog box to select the certificates.</span></span>
-   <span data-ttu-id="2a7de-115">Effacez tous les objets de [**certificat**](certificate.md) de la collection.</span><span class="sxs-lookup"><span data-stu-id="2a7de-115">Clear all the [**Certificate**](certificate.md) objects from the collection.</span></span>
-   <span data-ttu-id="2a7de-116">Récupérez le nombre de certificats dans la collection.</span><span class="sxs-lookup"><span data-stu-id="2a7de-116">Retrieve the number of certificates in the collection.</span></span>
-   <span data-ttu-id="2a7de-117">Récupérez un objet de [**certificat**](certificate.md) spécifique de la collection.</span><span class="sxs-lookup"><span data-stu-id="2a7de-117">Retrieve a specific [**Certificate**](certificate.md) object from the collection.</span></span>
-   <span data-ttu-id="2a7de-118">Itérez au sein de la collection.</span><span class="sxs-lookup"><span data-stu-id="2a7de-118">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="2a7de-119">Membres</span><span class="sxs-lookup"><span data-stu-id="2a7de-119">Members</span></span>

<span data-ttu-id="2a7de-120">L’objet **Certificates** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2a7de-120">The **Certificates** object has these types of members:</span></span>

-   [<span data-ttu-id="2a7de-121">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2a7de-121">Methods</span></span>](#methods)
-   [<span data-ttu-id="2a7de-122">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2a7de-122">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2a7de-123">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2a7de-123">Methods</span></span>

<span data-ttu-id="2a7de-124">L’objet **Certificates** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="2a7de-124">The **Certificates** object has these methods.</span></span>



| <span data-ttu-id="2a7de-125">Méthode</span><span class="sxs-lookup"><span data-stu-id="2a7de-125">Method</span></span>                                | <span data-ttu-id="2a7de-126">Description</span><span class="sxs-lookup"><span data-stu-id="2a7de-126">Description</span></span>                                                                                                                                                           |
|:--------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2a7de-127">**Complémentaires**</span><span class="sxs-lookup"><span data-stu-id="2a7de-127">**Add**</span></span>](certificates-add.md)       | <span data-ttu-id="2a7de-128">Ajoute un objet [**certificat**](certificate.md) à la collection.</span><span class="sxs-lookup"><span data-stu-id="2a7de-128">Adds a [**Certificate**](certificate.md) object to the collection.</span></span><br/> <span data-ttu-id="2a7de-129">(Héritée de **CertificatesICertificates2**)</span><span class="sxs-lookup"><span data-stu-id="2a7de-129">(Inherited from **CertificatesICertificates2**)</span></span>                                        |
| [<span data-ttu-id="2a7de-130">**Effacer**</span><span class="sxs-lookup"><span data-stu-id="2a7de-130">**Clear**</span></span>](certificates-clear.md)   | <span data-ttu-id="2a7de-131">Supprime tous les objets de [**certificat**](certificate.md) de la collection.</span><span class="sxs-lookup"><span data-stu-id="2a7de-131">Removes all [**Certificate**](certificate.md) objects from the collection.</span></span><br/> <span data-ttu-id="2a7de-132">(Héritée de **CertificatesICertificates2**)</span><span class="sxs-lookup"><span data-stu-id="2a7de-132">(Inherited from **CertificatesICertificates2**)</span></span>                                |
| [<span data-ttu-id="2a7de-133">**Rechercher**</span><span class="sxs-lookup"><span data-stu-id="2a7de-133">**Find**</span></span>](certificates-find.md)     | <span data-ttu-id="2a7de-134">Retourne un objet de **certificats** qui contient tous les certificats qui correspondent aux critères de recherche spécifiés.</span><span class="sxs-lookup"><span data-stu-id="2a7de-134">Returns a **Certificates** object that contains all certificates that match the specified search criteria.</span></span><br/> <span data-ttu-id="2a7de-135">(Héritée de **CertificatesICertificates2**)</span><span class="sxs-lookup"><span data-stu-id="2a7de-135">(Inherited from **CertificatesICertificates2**)</span></span> |
| [<span data-ttu-id="2a7de-136">**Supprimer**</span><span class="sxs-lookup"><span data-stu-id="2a7de-136">**Remove**</span></span>](certificates-remove.md) | <span data-ttu-id="2a7de-137">Supprime un objet de [**certificat**](certificate.md) unique de la collection.</span><span class="sxs-lookup"><span data-stu-id="2a7de-137">Removes a single [**Certificate**](certificate.md) object from the collection.</span></span><br/> <span data-ttu-id="2a7de-138">(Héritée de **CertificatesICertificates2**)</span><span class="sxs-lookup"><span data-stu-id="2a7de-138">(Inherited from **CertificatesICertificates2**)</span></span>                            |
| [<span data-ttu-id="2a7de-139">**Enregistrer**</span><span class="sxs-lookup"><span data-stu-id="2a7de-139">**Save**</span></span>](certificates-save.md)     | <span data-ttu-id="2a7de-140">Enregistre les certificats dans un fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="2a7de-140">Saves the certificates to a specified file.</span></span><br/> <span data-ttu-id="2a7de-141">(Héritée de **CertificatesICertificates2**)</span><span class="sxs-lookup"><span data-stu-id="2a7de-141">(Inherited from **CertificatesICertificates2**)</span></span>                                                                |
| [<span data-ttu-id="2a7de-142">**Sélectionner**</span><span class="sxs-lookup"><span data-stu-id="2a7de-142">**Select**</span></span>](certificates-select.md) | <span data-ttu-id="2a7de-143">Affiche une boîte de dialogue permettant de sélectionner des certificats et retourne une collection de ces certificats sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="2a7de-143">Displays a dialog box for selecting certificates and returns a collection of those certificates selected.</span></span><br/> <span data-ttu-id="2a7de-144">(Héritée de **CertificatesICertificates2**)</span><span class="sxs-lookup"><span data-stu-id="2a7de-144">(Inherited from **CertificatesICertificates2**)</span></span>  |



 

### <a name="properties"></a><span data-ttu-id="2a7de-145">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2a7de-145">Properties</span></span>

<span data-ttu-id="2a7de-146">L’objet **Certificates** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="2a7de-146">The **Certificates** object has these properties.</span></span>



| <span data-ttu-id="2a7de-147">Propriété</span><span class="sxs-lookup"><span data-stu-id="2a7de-147">Property</span></span>                                             | <span data-ttu-id="2a7de-148">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="2a7de-148">Access type</span></span>          | <span data-ttu-id="2a7de-149">Description</span><span class="sxs-lookup"><span data-stu-id="2a7de-149">Description</span></span>                                                                                                                                                                                                                     |
|:-----------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2a7de-150">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="2a7de-150">**\_NewEnum**</span></span>](certificates-newenum.md)<br/> | <span data-ttu-id="2a7de-151">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2a7de-151">Read-only</span></span><br/> | <span data-ttu-id="2a7de-152">Récupère une interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) sur un objet qui peut être utilisé pour énumérer la collection.</span><span class="sxs-lookup"><span data-stu-id="2a7de-152">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="2a7de-153">Cette propriété est masquée dans Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="2a7de-153">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="2a7de-154">**Saut**</span><span class="sxs-lookup"><span data-stu-id="2a7de-154">**Count**</span></span>](certificates-count.md)<br/>       | <span data-ttu-id="2a7de-155">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2a7de-155">Read-only</span></span><br/> | <span data-ttu-id="2a7de-156">Récupère le nombre d’objets de [**certificat**](certificate.md) dans la collection.</span><span class="sxs-lookup"><span data-stu-id="2a7de-156">Retrieves the number of [**Certificate**](certificate.md) objects in the collection.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="2a7de-157">**Élément**</span><span class="sxs-lookup"><span data-stu-id="2a7de-157">**Item**</span></span>](certificates-item.md)<br/>         | <span data-ttu-id="2a7de-158">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2a7de-158">Read-only</span></span><br/> | <span data-ttu-id="2a7de-159">Récupère un objet de [**certificat**](certificate.md) qui représente le certificat indexé de la collection.</span><span class="sxs-lookup"><span data-stu-id="2a7de-159">Retrieves a [**Certificate**](certificate.md) object that represents the indexed certificate of the collection.</span></span> <span data-ttu-id="2a7de-160">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="2a7de-160">This is the default property.</span></span><br/> <span data-ttu-id="2a7de-161">(Héritée de **CertificatesICertificates2ICertificates**)</span><span class="sxs-lookup"><span data-stu-id="2a7de-161">(Inherited from **CertificatesICertificates2ICertificates**)</span></span>          |



 

## <a name="remarks"></a><span data-ttu-id="2a7de-162">Notes </span><span class="sxs-lookup"><span data-stu-id="2a7de-162">Remarks</span></span>

<span data-ttu-id="2a7de-163">L’objet **certificats** peut être créé et il est sécurisé pour l’écriture de scripts.</span><span class="sxs-lookup"><span data-stu-id="2a7de-163">The **Certificates** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="2a7de-164">Le ProgID de l’objet **Certificates** est «CAPICOM. Certificats. 2».</span><span class="sxs-lookup"><span data-stu-id="2a7de-164">The ProgID for the **Certificates** object is "CAPICOM.Certificates.2".</span></span>

<span data-ttu-id="2a7de-165">**CAPICOM 1. *x*:** le ProgID de l’objet **Certificates** est «CAPICOM. Certificats. 1».</span><span class="sxs-lookup"><span data-stu-id="2a7de-165">**CAPICOM 1.*x*:** The ProgID for the **Certificates** object is "CAPICOM.Certificates.1".</span></span>

## <a name="requirements"></a><span data-ttu-id="2a7de-166">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2a7de-166">Requirements</span></span>



| <span data-ttu-id="2a7de-167">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2a7de-167">Requirement</span></span> | <span data-ttu-id="2a7de-168">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a7de-168">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2a7de-169">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="2a7de-169">End of client support</span></span><br/> | <span data-ttu-id="2a7de-170">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2a7de-170">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="2a7de-171">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="2a7de-171">End of server support</span></span><br/> | <span data-ttu-id="2a7de-172">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2a7de-172">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="2a7de-173">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="2a7de-173">Redistributable</span></span><br/>       | <span data-ttu-id="2a7de-174">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="2a7de-174">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="2a7de-175">DLL</span><span class="sxs-lookup"><span data-stu-id="2a7de-175">DLL</span></span><br/>                   | <dl> <span data-ttu-id="2a7de-176"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a7de-176"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a7de-177">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2a7de-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a7de-178">**Objets de chiffrement**</span><span class="sxs-lookup"><span data-stu-id="2a7de-178">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
