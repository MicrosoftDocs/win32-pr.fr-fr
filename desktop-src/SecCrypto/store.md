---
description: Fournit des propriétés et des méthodes que vous pouvez utiliser pour choisir, gérer et utiliser des magasins de certificats et les certificats de ces magasins.
ms.assetid: de4eecf7-c03b-4733-ac29-d5b26b873dba
title: Objet Store
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4e8a14fcecf0ded2e4e1a56e2b98e4ac4838b776
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541624"
---
# <a name="store-object"></a><span data-ttu-id="23e34-103">Objet Store</span><span class="sxs-lookup"><span data-stu-id="23e34-103">Store object</span></span>

<span data-ttu-id="23e34-104">\[L’objet **Store** peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="23e34-104">\[The **Store** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="23e34-105">Utilisez plutôt la [**classe X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="23e34-105">Instead, use the [**X509Store Class**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="23e34-106">L’objet **Store** fournit des propriétés et des méthodes que vous pouvez utiliser pour choisir, gérer et utiliser des [*magasins de certificats*](../secgloss/c-gly.md) et les certificats de ces magasins.</span><span class="sxs-lookup"><span data-stu-id="23e34-106">The **Store** object provides properties and methods that you can use to choose, manage, and use [*certificate stores*](../secgloss/c-gly.md) and the certificates in those stores.</span></span> <span data-ttu-id="23e34-107">CAPICOM peut utiliser les magasins de l’utilisateur actuel, de l’ordinateur local, de la mémoire et de la Active Directory.</span><span class="sxs-lookup"><span data-stu-id="23e34-107">CAPICOM can use Current-User, Local-Machine, memory, and Active Directory stores.</span></span> <span data-ttu-id="23e34-108">En outre, les magasins prennent en charge les magasins de certificats basés sur une carte à puce.</span><span class="sxs-lookup"><span data-stu-id="23e34-108">Also, stores support smart card–based certificate stores.</span></span> <span data-ttu-id="23e34-109">Les développeurs doivent savoir que certaines méthodes peuvent échouer avec certains magasins si des opérations sont tentées pour lesquelles l’utilisateur ne dispose pas de droits.</span><span class="sxs-lookup"><span data-stu-id="23e34-109">Developers should be aware that some methods may fail with some stores if operations are attempted for which the user does not have rights.</span></span>

## <a name="members"></a><span data-ttu-id="23e34-110">Membres</span><span class="sxs-lookup"><span data-stu-id="23e34-110">Members</span></span>

<span data-ttu-id="23e34-111">L’objet **Store** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="23e34-111">The **Store** object has these types of members:</span></span>

-   [<span data-ttu-id="23e34-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="23e34-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="23e34-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="23e34-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="23e34-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="23e34-114">Methods</span></span>

<span data-ttu-id="23e34-115">L’objet **Store** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="23e34-115">The **Store** object has these methods.</span></span>



| <span data-ttu-id="23e34-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="23e34-116">Method</span></span>                         | <span data-ttu-id="23e34-117">Description</span><span class="sxs-lookup"><span data-stu-id="23e34-117">Description</span></span>                                                                                                                                                                                                      |
|:-------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="23e34-118">**Complémentaires**</span><span class="sxs-lookup"><span data-stu-id="23e34-118">**Add**</span></span>](store-add.md)       | <span data-ttu-id="23e34-119">Ajoute un objet [**certificat**](certificate.md) au magasin de certificats ouvert.</span><span class="sxs-lookup"><span data-stu-id="23e34-119">Adds a [**Certificate**](certificate.md) object to the open certificate store.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="23e34-120">**Fermer**</span><span class="sxs-lookup"><span data-stu-id="23e34-120">**Close**</span></span>](store-close.md)   | <span data-ttu-id="23e34-121">Ferme un magasin de certificats ouvert.</span><span class="sxs-lookup"><span data-stu-id="23e34-121">Closes an open certificate store.</span></span><br/> <span data-ttu-id="23e34-122">**CAPICOM 2.0.0.3 et versions antérieures :** La méthode [**Close**](store-close.md) n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="23e34-122">**CAPICOM 2.0.0.3 and earlier:** The [**Close**](store-close.md) method is not supported.</span></span><br/>                                                               |
| [<span data-ttu-id="23e34-123">**Supprimer**</span><span class="sxs-lookup"><span data-stu-id="23e34-123">**Delete**</span></span>](store-delete.md) | <span data-ttu-id="23e34-124">Supprime le magasin de certificats représenté par l’objet de [**magasin**](certificate.md) actuel.</span><span class="sxs-lookup"><span data-stu-id="23e34-124">Deletes the certificate store represented by the current [**Store**](certificate.md) object.</span></span><br/> <span data-ttu-id="23e34-125">**CAPICOM 2.0.0.3 et versions antérieures :** La méthode [**Delete**](store-delete.md) n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="23e34-125">**CAPICOM 2.0.0.3 and earlier:** The [**Delete**](store-delete.md) method is not supported.</span></span><br/> |
| [<span data-ttu-id="23e34-126">**Exporter**</span><span class="sxs-lookup"><span data-stu-id="23e34-126">**Export**</span></span>](store-export.md) | <span data-ttu-id="23e34-127">Exporte le magasin d’un [*objet BLOB*](../secgloss/b-gly.md)encodé.</span><span class="sxs-lookup"><span data-stu-id="23e34-127">Exports the store of an encoded [*BLOB*](../secgloss/b-gly.md).</span></span><br/>                                                                                                       |
| [<span data-ttu-id="23e34-128">**Importer**</span><span class="sxs-lookup"><span data-stu-id="23e34-128">**Import**</span></span>](store-import.md) | <span data-ttu-id="23e34-129">Importe un magasin précédemment exporté.</span><span class="sxs-lookup"><span data-stu-id="23e34-129">Imports a previously exported store.</span></span><br/>                                                                                                                                                                  |
| [<span data-ttu-id="23e34-130">**Load**</span><span class="sxs-lookup"><span data-stu-id="23e34-130">**Load**</span></span>](store-load.md)     | <span data-ttu-id="23e34-131">Importe des objets de [**certificat**](certificate.md) à partir d’un fichier dans le magasin.</span><span class="sxs-lookup"><span data-stu-id="23e34-131">Imports [**Certificate**](certificate.md) objects from a file into the store.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="23e34-132">**Afficher**</span><span class="sxs-lookup"><span data-stu-id="23e34-132">**Open**</span></span>](store-open.md)     | <span data-ttu-id="23e34-133">Ouvre un magasin de certificats.</span><span class="sxs-lookup"><span data-stu-id="23e34-133">Opens a certificate store.</span></span><br/>                                                                                                                                                                            |
| [<span data-ttu-id="23e34-134">**Installez**</span><span class="sxs-lookup"><span data-stu-id="23e34-134">**Remove**</span></span>](store-remove.md) | <span data-ttu-id="23e34-135">Supprime un objet [**certificat**](certificate.md) d’un magasin ouvert.</span><span class="sxs-lookup"><span data-stu-id="23e34-135">Removes a [**Certificate**](certificate.md) object from an open store.</span></span><br/>                                                                                                                               |



 

### <a name="properties"></a><span data-ttu-id="23e34-136">Propriétés</span><span class="sxs-lookup"><span data-stu-id="23e34-136">Properties</span></span>

<span data-ttu-id="23e34-137">L’objet **Store** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="23e34-137">The **Store** object has these properties.</span></span>



| <span data-ttu-id="23e34-138">Propriété</span><span class="sxs-lookup"><span data-stu-id="23e34-138">Property</span></span>                                              | <span data-ttu-id="23e34-139">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="23e34-139">Access type</span></span>          | <span data-ttu-id="23e34-140">Description</span><span class="sxs-lookup"><span data-stu-id="23e34-140">Description</span></span>                                                                                                                                                                                           |
|:------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="23e34-141">**Certificats**</span><span class="sxs-lookup"><span data-stu-id="23e34-141">**Certificates**</span></span>](store-certificates.md)<br/> | <span data-ttu-id="23e34-142">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="23e34-142">Read-only</span></span><br/> | <span data-ttu-id="23e34-143">Récupère la collection de [**certificats**](certificates.md) du magasin.</span><span class="sxs-lookup"><span data-stu-id="23e34-143">Retrieves the [**Certificates**](certificates.md) collection of the store.</span></span> <span data-ttu-id="23e34-144">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="23e34-144">This is the default property.</span></span><br/>                                                                                  |
| [<span data-ttu-id="23e34-145">**Lieu**</span><span class="sxs-lookup"><span data-stu-id="23e34-145">**Location**</span></span>](store-location.md)<br/>         | <span data-ttu-id="23e34-146">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="23e34-146">Read-only</span></span><br/> | <span data-ttu-id="23e34-147">Récupère l’emplacement du magasin de certificats que cet objet représente.</span><span class="sxs-lookup"><span data-stu-id="23e34-147">Retrieves the location of the certificate store that this object represents.</span></span><br/> <span data-ttu-id="23e34-148">**CAPICOM 2.0.0.3 et versions antérieures :** La propriété d' [**emplacement**](store-location.md) n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="23e34-148">**CAPICOM 2.0.0.3 and earlier:** The [**Location**](store-location.md) property is not supported.</span></span><br/> |
| [<span data-ttu-id="23e34-149">**Nom**</span><span class="sxs-lookup"><span data-stu-id="23e34-149">**Name**</span></span>](store-name.md)<br/>                 | <span data-ttu-id="23e34-150">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="23e34-150">Read-only</span></span><br/> | <span data-ttu-id="23e34-151">Récupère le nom du magasin de certificats que cet objet représente.</span><span class="sxs-lookup"><span data-stu-id="23e34-151">Retrieves the name of the certificate store that this object represents.</span></span><br/> <span data-ttu-id="23e34-152">**CAPICOM 2.0.0.3 et versions antérieures :** La propriété [**Name**](store-name.md) n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="23e34-152">**CAPICOM 2.0.0.3 and earlier:** The [**Name**](store-name.md) property is not supported.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="23e34-153">Notes</span><span class="sxs-lookup"><span data-stu-id="23e34-153">Remarks</span></span>

<span data-ttu-id="23e34-154">L’objet **Store** peut être créé et il est sécurisé pour l’écriture de scripts.</span><span class="sxs-lookup"><span data-stu-id="23e34-154">The **Store** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="23e34-155">Le ProgID de l’objet **Store** est CAPICOM. Store. 2.</span><span class="sxs-lookup"><span data-stu-id="23e34-155">The ProgID for the **Store** object is CAPICOM.Store.2.</span></span>

<span data-ttu-id="23e34-156">**CAPICOM 1. *x*:** le ProgID de l’objet **Store** est CAPICOM. Store. 1.</span><span class="sxs-lookup"><span data-stu-id="23e34-156">**CAPICOM 1.*x*:** The ProgID for the **Store** object is CAPICOM.Store.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="23e34-157">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="23e34-157">Requirements</span></span>



| <span data-ttu-id="23e34-158">Condition requise</span><span class="sxs-lookup"><span data-stu-id="23e34-158">Requirement</span></span> | <span data-ttu-id="23e34-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="23e34-159">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="23e34-160">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="23e34-160">Redistributable</span></span><br/> | <span data-ttu-id="23e34-161">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="23e34-161">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="23e34-162">DLL</span><span class="sxs-lookup"><span data-stu-id="23e34-162">DLL</span></span><br/>             | <dl> <span data-ttu-id="23e34-163"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23e34-163"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23e34-164">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="23e34-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23e34-165">**Objets de chiffrement**</span><span class="sxs-lookup"><span data-stu-id="23e34-165">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
