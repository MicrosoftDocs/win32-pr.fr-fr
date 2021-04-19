---
description: Représente une collection d’objets de certificat.
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
ms.openlocfilehash: 2e8c12c16820342c5687720a35ce81aa7b94f180
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525109"
---
# <a name="certificates-object"></a><span data-ttu-id="16166-103">Objet Certificates</span><span class="sxs-lookup"><span data-stu-id="16166-103">Certificates object</span></span>

<span data-ttu-id="16166-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="16166-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="16166-105">Utilisez plutôt la [**classe X509Certificate2Collection**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="16166-105">Instead, use the [**X509Certificate2Collection Class**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="16166-106">L' **objet** [**Certificates**](certificate.md) représente une collection d’objets de certificat.</span><span class="sxs-lookup"><span data-stu-id="16166-106">The **Certificates** object represents a collection of [**Certificate**](certificate.md) objects.</span></span> <span data-ttu-id="16166-107">Chaque objet [**certificat**](certificate.md) représente un seul [*certificat numérique*](../secgloss/d-gly.md).</span><span class="sxs-lookup"><span data-stu-id="16166-107">Each [**Certificate**](certificate.md) object represents a single [*digital certificate*](../secgloss/d-gly.md).</span></span>

<span data-ttu-id="16166-108">L’objet **Certificates** expose les interfaces suivantes :</span><span class="sxs-lookup"><span data-stu-id="16166-108">The **Certificates** object exposes the following interfaces:</span></span>

-   <span data-ttu-id="16166-109">**ICertificates2**: introduit dans CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="16166-109">**ICertificates2**: Introduced in CAPICOM 2.0.</span></span>
-   <span data-ttu-id="16166-110">**ICertificates**: introduit dans CAPICOM 1,0.</span><span class="sxs-lookup"><span data-stu-id="16166-110">**ICertificates**: Introduced in CAPICOM 1.0.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="16166-111">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="16166-111">When to use</span></span>

<span data-ttu-id="16166-112">L’objet **Certificates** est utilisé pour effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="16166-112">The **Certificates** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="16166-113">Ajoutez ou supprimez un objet de [**certificat**](certificate.md) à partir de la collection.</span><span class="sxs-lookup"><span data-stu-id="16166-113">Add or remove a [**Certificate**](certificate.md) object to or from the collection.</span></span>
-   <span data-ttu-id="16166-114">Générez un sous-ensemble de la collection en recherchant un ensemble de certificats ou en affichant une boîte de dialogue pour sélectionner les certificats.</span><span class="sxs-lookup"><span data-stu-id="16166-114">Generate a subset of the collection by finding a set of certificates or by displaying a dialog box to select the certificates.</span></span>
-   <span data-ttu-id="16166-115">Effacez tous les objets de [**certificat**](certificate.md) de la collection.</span><span class="sxs-lookup"><span data-stu-id="16166-115">Clear all the [**Certificate**](certificate.md) objects from the collection.</span></span>
-   <span data-ttu-id="16166-116">Récupérez le nombre de certificats dans la collection.</span><span class="sxs-lookup"><span data-stu-id="16166-116">Retrieve the number of certificates in the collection.</span></span>
-   <span data-ttu-id="16166-117">Récupérez un objet de [**certificat**](certificate.md) spécifique de la collection.</span><span class="sxs-lookup"><span data-stu-id="16166-117">Retrieve a specific [**Certificate**](certificate.md) object from the collection.</span></span>
-   <span data-ttu-id="16166-118">Itérez au sein de la collection.</span><span class="sxs-lookup"><span data-stu-id="16166-118">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="16166-119">Membres</span><span class="sxs-lookup"><span data-stu-id="16166-119">Members</span></span>

<span data-ttu-id="16166-120">L’objet **Certificates** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="16166-120">The **Certificates** object has these types of members:</span></span>

-   [<span data-ttu-id="16166-121">Méthodes</span><span class="sxs-lookup"><span data-stu-id="16166-121">Methods</span></span>](#methods)
-   [<span data-ttu-id="16166-122">Propriétés</span><span class="sxs-lookup"><span data-stu-id="16166-122">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="16166-123">Méthodes</span><span class="sxs-lookup"><span data-stu-id="16166-123">Methods</span></span>

<span data-ttu-id="16166-124">L’objet **Certificates** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="16166-124">The **Certificates** object has these methods.</span></span>



| <span data-ttu-id="16166-125">Méthode</span><span class="sxs-lookup"><span data-stu-id="16166-125">Method</span></span>                                | <span data-ttu-id="16166-126">Description</span><span class="sxs-lookup"><span data-stu-id="16166-126">Description</span></span>                                                                                                                                                           |
|:--------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="16166-127">**Complémentaires**</span><span class="sxs-lookup"><span data-stu-id="16166-127">**Add**</span></span>](certificates-add.md)       | <span data-ttu-id="16166-128">Ajoute un objet [**certificat**](certificate.md) à la collection.</span><span class="sxs-lookup"><span data-stu-id="16166-128">Adds a [**Certificate**](certificate.md) object to the collection.</span></span><br/> <span data-ttu-id="16166-129">(Héritée de **CertificatesICertificates2**)</span><span class="sxs-lookup"><span data-stu-id="16166-129">(Inherited from **CertificatesICertificates2**)</span></span>                                        |
| [<span data-ttu-id="16166-130">**Effacé**</span><span class="sxs-lookup"><span data-stu-id="16166-130">**Clear**</span></span>](certificates-clear.md)   | <span data-ttu-id="16166-131">Supprime tous les objets de [**certificat**](certificate.md) de la collection.</span><span class="sxs-lookup"><span data-stu-id="16166-131">Removes all [**Certificate**](certificate.md) objects from the collection.</span></span><br/> <span data-ttu-id="16166-132">(Héritée de **CertificatesICertificates2**)</span><span class="sxs-lookup"><span data-stu-id="16166-132">(Inherited from **CertificatesICertificates2**)</span></span>                                |
| [<span data-ttu-id="16166-133">**Trouver**</span><span class="sxs-lookup"><span data-stu-id="16166-133">**Find**</span></span>](certificates-find.md)     | <span data-ttu-id="16166-134">Retourne un objet de **certificats** qui contient tous les certificats qui correspondent aux critères de recherche spécifiés.</span><span class="sxs-lookup"><span data-stu-id="16166-134">Returns a **Certificates** object that contains all certificates that match the specified search criteria.</span></span><br/> <span data-ttu-id="16166-135">(Héritée de **CertificatesICertificates2**)</span><span class="sxs-lookup"><span data-stu-id="16166-135">(Inherited from **CertificatesICertificates2**)</span></span> |
| [<span data-ttu-id="16166-136">**Installez**</span><span class="sxs-lookup"><span data-stu-id="16166-136">**Remove**</span></span>](certificates-remove.md) | <span data-ttu-id="16166-137">Supprime un objet de [**certificat**](certificate.md) unique de la collection.</span><span class="sxs-lookup"><span data-stu-id="16166-137">Removes a single [**Certificate**](certificate.md) object from the collection.</span></span><br/> <span data-ttu-id="16166-138">(Héritée de **CertificatesICertificates2**)</span><span class="sxs-lookup"><span data-stu-id="16166-138">(Inherited from **CertificatesICertificates2**)</span></span>                            |
| [<span data-ttu-id="16166-139">**Enregistrer**</span><span class="sxs-lookup"><span data-stu-id="16166-139">**Save**</span></span>](certificates-save.md)     | <span data-ttu-id="16166-140">Enregistre les certificats dans un fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="16166-140">Saves the certificates to a specified file.</span></span><br/> <span data-ttu-id="16166-141">(Héritée de **CertificatesICertificates2**)</span><span class="sxs-lookup"><span data-stu-id="16166-141">(Inherited from **CertificatesICertificates2**)</span></span>                                                                |
| [<span data-ttu-id="16166-142">**Sélectionner**</span><span class="sxs-lookup"><span data-stu-id="16166-142">**Select**</span></span>](certificates-select.md) | <span data-ttu-id="16166-143">Affiche une boîte de dialogue permettant de sélectionner des certificats et retourne une collection de ces certificats sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="16166-143">Displays a dialog box for selecting certificates and returns a collection of those certificates selected.</span></span><br/> <span data-ttu-id="16166-144">(Héritée de **CertificatesICertificates2**)</span><span class="sxs-lookup"><span data-stu-id="16166-144">(Inherited from **CertificatesICertificates2**)</span></span>  |



 

### <a name="properties"></a><span data-ttu-id="16166-145">Propriétés</span><span class="sxs-lookup"><span data-stu-id="16166-145">Properties</span></span>

<span data-ttu-id="16166-146">L’objet **Certificates** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="16166-146">The **Certificates** object has these properties.</span></span>



| <span data-ttu-id="16166-147">Propriété</span><span class="sxs-lookup"><span data-stu-id="16166-147">Property</span></span>                                             | <span data-ttu-id="16166-148">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="16166-148">Access type</span></span>          | <span data-ttu-id="16166-149">Description</span><span class="sxs-lookup"><span data-stu-id="16166-149">Description</span></span>                                                                                                                                                                                                                     |
|:-----------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="16166-150">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="16166-150">**\_NewEnum**</span></span>](certificates-newenum.md)<br/> | <span data-ttu-id="16166-151">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="16166-151">Read-only</span></span><br/> | <span data-ttu-id="16166-152">Récupère une interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) sur un objet qui peut être utilisé pour énumérer la collection.</span><span class="sxs-lookup"><span data-stu-id="16166-152">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="16166-153">Cette propriété est masquée dans Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="16166-153">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="16166-154">**Saut**</span><span class="sxs-lookup"><span data-stu-id="16166-154">**Count**</span></span>](certificates-count.md)<br/>       | <span data-ttu-id="16166-155">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="16166-155">Read-only</span></span><br/> | <span data-ttu-id="16166-156">Récupère le nombre d’objets de [**certificat**](certificate.md) dans la collection.</span><span class="sxs-lookup"><span data-stu-id="16166-156">Retrieves the number of [**Certificate**](certificate.md) objects in the collection.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="16166-157">**Élément**</span><span class="sxs-lookup"><span data-stu-id="16166-157">**Item**</span></span>](certificates-item.md)<br/>         | <span data-ttu-id="16166-158">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="16166-158">Read-only</span></span><br/> | <span data-ttu-id="16166-159">Récupère un objet de [**certificat**](certificate.md) qui représente le certificat indexé de la collection.</span><span class="sxs-lookup"><span data-stu-id="16166-159">Retrieves a [**Certificate**](certificate.md) object that represents the indexed certificate of the collection.</span></span> <span data-ttu-id="16166-160">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="16166-160">This is the default property.</span></span><br/> <span data-ttu-id="16166-161">(Héritée de **CertificatesICertificates2ICertificates**)</span><span class="sxs-lookup"><span data-stu-id="16166-161">(Inherited from **CertificatesICertificates2ICertificates**)</span></span>          |



 

## <a name="remarks"></a><span data-ttu-id="16166-162">Notes</span><span class="sxs-lookup"><span data-stu-id="16166-162">Remarks</span></span>

<span data-ttu-id="16166-163">L’objet **certificats** peut être créé et il est sécurisé pour l’écriture de scripts.</span><span class="sxs-lookup"><span data-stu-id="16166-163">The **Certificates** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="16166-164">Le ProgID de l’objet **Certificates** est «CAPICOM. Certificats. 2».</span><span class="sxs-lookup"><span data-stu-id="16166-164">The ProgID for the **Certificates** object is "CAPICOM.Certificates.2".</span></span>

<span data-ttu-id="16166-165">**CAPICOM 1. *x*:** le ProgID de l’objet **Certificates** est «CAPICOM. Certificats. 1».</span><span class="sxs-lookup"><span data-stu-id="16166-165">**CAPICOM 1.*x*:** The ProgID for the **Certificates** object is "CAPICOM.Certificates.1".</span></span>

## <a name="requirements"></a><span data-ttu-id="16166-166">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="16166-166">Requirements</span></span>



| <span data-ttu-id="16166-167">Condition requise</span><span class="sxs-lookup"><span data-stu-id="16166-167">Requirement</span></span> | <span data-ttu-id="16166-168">Valeur</span><span class="sxs-lookup"><span data-stu-id="16166-168">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="16166-169">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="16166-169">End of client support</span></span><br/> | <span data-ttu-id="16166-170">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="16166-170">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="16166-171">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="16166-171">End of server support</span></span><br/> | <span data-ttu-id="16166-172">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="16166-172">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="16166-173">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="16166-173">Redistributable</span></span><br/>       | <span data-ttu-id="16166-174">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="16166-174">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="16166-175">DLL</span><span class="sxs-lookup"><span data-stu-id="16166-175">DLL</span></span><br/>                   | <dl> <span data-ttu-id="16166-176"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16166-176"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16166-177">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16166-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16166-178">**Objets de chiffrement**</span><span class="sxs-lookup"><span data-stu-id="16166-178">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
