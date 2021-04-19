---
description: Représente une collection d’objets OID.
ms.assetid: 2c4ff87a-58e1-46aa-9680-29062b05308c
title: Objet OID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 894689c214d8b7d352a2453d2d62c847866b9bc5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542462"
---
# <a name="oids-object"></a><span data-ttu-id="cb809-103">Objet OID</span><span class="sxs-lookup"><span data-stu-id="cb809-103">OIDs object</span></span>

<span data-ttu-id="cb809-104">\[L’objet **OID** est disponible pour une utilisation dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="cb809-104">\[The **OIDs** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="cb809-105">Utilisez plutôt la [**classe OidCollection**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="cb809-105">Instead, use the [**OidCollection Class**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="cb809-106">L’objet **OID** représente une collection d’objets [**OID**](oid.md) .</span><span class="sxs-lookup"><span data-stu-id="cb809-106">The **OIDs** object represents a collection of [**OID**](oid.md) objects.</span></span> <span data-ttu-id="cb809-107">Chaque objet [**OID**](oid.md) représente un identificateur d’objet unique.</span><span class="sxs-lookup"><span data-stu-id="cb809-107">Each [**OID**](oid.md) object represents a single object identifier.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="cb809-108">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="cb809-108">When to use</span></span>

<span data-ttu-id="cb809-109">L’objet **OID** est utilisé pour effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="cb809-109">The **OIDs** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="cb809-110">Ajoutez ou supprimez un objet [**OID**](oid.md) de la collection.</span><span class="sxs-lookup"><span data-stu-id="cb809-110">Add or remove an [**OID**](oid.md) object from the collection.</span></span>
-   <span data-ttu-id="cb809-111">Effacez tous les objets [**OID**](oid.md) de la collection.</span><span class="sxs-lookup"><span data-stu-id="cb809-111">Clear all the [**OID**](oid.md) objects from the collection.</span></span>
-   <span data-ttu-id="cb809-112">Récupérez le nombre d’identificateurs d’objet dans la collection.</span><span class="sxs-lookup"><span data-stu-id="cb809-112">Retrieve the number of object identifiers in the collection.</span></span>
-   <span data-ttu-id="cb809-113">Récupérez un objet [**OID**](oid.md) spécifique de la collection.</span><span class="sxs-lookup"><span data-stu-id="cb809-113">Retrieve a specific [**OID**](oid.md) object from the collection.</span></span>
-   <span data-ttu-id="cb809-114">Itérez au sein de la collection.</span><span class="sxs-lookup"><span data-stu-id="cb809-114">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="cb809-115">Membres</span><span class="sxs-lookup"><span data-stu-id="cb809-115">Members</span></span>

<span data-ttu-id="cb809-116">L’objet **OID** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="cb809-116">The **OIDs** object has these types of members:</span></span>

-   [<span data-ttu-id="cb809-117">Méthodes</span><span class="sxs-lookup"><span data-stu-id="cb809-117">Methods</span></span>](#methods)
-   [<span data-ttu-id="cb809-118">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cb809-118">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="cb809-119">Méthodes</span><span class="sxs-lookup"><span data-stu-id="cb809-119">Methods</span></span>

<span data-ttu-id="cb809-120">L’objet **OID** possède les méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="cb809-120">The **OIDs** object has these methods.</span></span>



| <span data-ttu-id="cb809-121">Méthode</span><span class="sxs-lookup"><span data-stu-id="cb809-121">Method</span></span>                        | <span data-ttu-id="cb809-122">Description</span><span class="sxs-lookup"><span data-stu-id="cb809-122">Description</span></span>                                                                  |
|:------------------------------|:-----------------------------------------------------------------------------|
| [<span data-ttu-id="cb809-123">**Complémentaires**</span><span class="sxs-lookup"><span data-stu-id="cb809-123">**Add**</span></span>](oids-add.md)       | <span data-ttu-id="cb809-124">Ajoute un objet [**OID**](oid.md) à la collection.</span><span class="sxs-lookup"><span data-stu-id="cb809-124">Adds an [**OID**](oid.md) object to the collection.</span></span><br/>              |
| [<span data-ttu-id="cb809-125">**Effacé**</span><span class="sxs-lookup"><span data-stu-id="cb809-125">**Clear**</span></span>](oids-clear.md)   | <span data-ttu-id="cb809-126">Efface tous les objets [**OID**](oid.md) de la collection.</span><span class="sxs-lookup"><span data-stu-id="cb809-126">Clears all [**OID**](oid.md) objects from the collection.</span></span><br/>        |
| [<span data-ttu-id="cb809-127">**Installez**</span><span class="sxs-lookup"><span data-stu-id="cb809-127">**Remove**</span></span>](oids-remove.md) | <span data-ttu-id="cb809-128">Supprime un objet [**OID**](oid.md) indexé de la collection.</span><span class="sxs-lookup"><span data-stu-id="cb809-128">Removes an indexed [**OID**](oid.md) object from the collection.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="cb809-129">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cb809-129">Properties</span></span>

<span data-ttu-id="cb809-130">L’objet **OID** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="cb809-130">The **OIDs** object has these properties.</span></span>



| <span data-ttu-id="cb809-131">Propriété</span><span class="sxs-lookup"><span data-stu-id="cb809-131">Property</span></span>                                     | <span data-ttu-id="cb809-132">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="cb809-132">Access type</span></span>          | <span data-ttu-id="cb809-133">Description</span><span class="sxs-lookup"><span data-stu-id="cb809-133">Description</span></span>                                                                                                                                                                                                                     |
|:---------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cb809-134">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="cb809-134">**\_NewEnum**</span></span>](oids-newenum.md)<br/> | <span data-ttu-id="cb809-135">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cb809-135">Read-only</span></span><br/> | <span data-ttu-id="cb809-136">Récupère une interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) sur un objet qui peut être utilisé pour énumérer la collection.</span><span class="sxs-lookup"><span data-stu-id="cb809-136">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="cb809-137">Cette propriété est masquée dans Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="cb809-137">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="cb809-138">**Saut**</span><span class="sxs-lookup"><span data-stu-id="cb809-138">**Count**</span></span>](oids-count.md)<br/>       | <span data-ttu-id="cb809-139">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cb809-139">Read-only</span></span><br/> | <span data-ttu-id="cb809-140">Récupère le nombre d’objets [**OID**](oid.md) de la collection.</span><span class="sxs-lookup"><span data-stu-id="cb809-140">Retrieves the number of [**OID**](oid.md) objects in the collection.</span></span><br/>                                                                                                                                                |
| [<span data-ttu-id="cb809-141">**Élément**</span><span class="sxs-lookup"><span data-stu-id="cb809-141">**Item**</span></span>](oids-item.md)<br/>         | <span data-ttu-id="cb809-142">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cb809-142">Read-only</span></span><br/> | <span data-ttu-id="cb809-143">Récupère un objet [**OID**](oid.md) indexé de la collection.</span><span class="sxs-lookup"><span data-stu-id="cb809-143">Retrieves an indexed [**OID**](oid.md) object from the collection.</span></span> <span data-ttu-id="cb809-144">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="cb809-144">This is the default property.</span></span><br/>                                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="cb809-145">Notes</span><span class="sxs-lookup"><span data-stu-id="cb809-145">Remarks</span></span>

<span data-ttu-id="cb809-146">Impossible de créer l’objet **OID** .</span><span class="sxs-lookup"><span data-stu-id="cb809-146">The **OIDs** object cannot be created.</span></span>

<span data-ttu-id="cb809-147">L’objet **OID** est utilisé par les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="cb809-147">The **OIDs** object is used by the following properties:</span></span>

-   [<span data-ttu-id="cb809-148">**CertificateStatus.ApplicationPolicies**</span><span class="sxs-lookup"><span data-stu-id="cb809-148">**CertificateStatus.ApplicationPolicies**</span></span>](certificatestatus-applicationpolicies.md)
-   [<span data-ttu-id="cb809-149">**CertificateStatus.CertificatePolicies**</span><span class="sxs-lookup"><span data-stu-id="cb809-149">**CertificateStatus.CertificatePolicies**</span></span>](certificatestatus-certificatepolicies.md)

## <a name="requirements"></a><span data-ttu-id="cb809-150">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cb809-150">Requirements</span></span>



| <span data-ttu-id="cb809-151">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cb809-151">Requirement</span></span> | <span data-ttu-id="cb809-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb809-152">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cb809-153">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="cb809-153">Redistributable</span></span><br/> | <span data-ttu-id="cb809-154">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="cb809-154">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="cb809-155">DLL</span><span class="sxs-lookup"><span data-stu-id="cb809-155">DLL</span></span><br/>             | <dl> <span data-ttu-id="cb809-156"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb809-156"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
