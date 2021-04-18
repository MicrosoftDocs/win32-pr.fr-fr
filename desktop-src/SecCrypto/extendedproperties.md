---
description: Représente une collection d’objets ExtendedProperty.
ms.assetid: 9de25994-9f0b-47a0-b4c8-781aec782f88
title: Objet ExtendedProperties
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperties
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 512c29e43b9099d9ef577cce61bbcc3a38d68ac6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543208"
---
# <a name="extendedproperties-object"></a><span data-ttu-id="e373c-103">Objet ExtendedProperties</span><span class="sxs-lookup"><span data-stu-id="e373c-103">ExtendedProperties object</span></span>

<span data-ttu-id="e373c-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e373c-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="e373c-105">Utilisez plutôt les services d’appel de plateforme (PInvoke) pour appeler la fonction API Win32 [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) et obtenir les propriétés.</span><span class="sxs-lookup"><span data-stu-id="e373c-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API function [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) and obtain the properties.</span></span> <span data-ttu-id="e373c-106">Pour plus d’informations sur PInvoke, consultez Didacticiel sur l’appel de code non [managé](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="e373c-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="e373c-107">Le [.net et CryptoAPI via p/Invoke : part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) et [.net et CryptoAPI via p/Invoke : partie 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sous-sections de l' [extension du chiffrement .net avec CAPICOM et P/Invoke](/previous-versions/ms867087(v=msdn.10)) peuvent également s’avérer utiles.\]</span><span class="sxs-lookup"><span data-stu-id="e373c-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="e373c-108">L’objet **ExtendedProperties** représente une collection d’objets [**ExtendedProperty**](extendedproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="e373c-108">The **ExtendedProperties** object represents a collection of [**ExtendedProperty**](extendedproperty.md) objects.</span></span> <span data-ttu-id="e373c-109">Chaque objet représente une propriété étendue unique.</span><span class="sxs-lookup"><span data-stu-id="e373c-109">Each object represents a single extended property.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="e373c-110">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="e373c-110">When to use</span></span>

<span data-ttu-id="e373c-111">L’objet **ExtendedProperties** est utilisé pour effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="e373c-111">The **ExtendedProperties** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="e373c-112">Ajoutez ou supprimez un objet [**ExtendedProperty**](extendedproperty.md) de la collection.</span><span class="sxs-lookup"><span data-stu-id="e373c-112">Add or remove an [**ExtendedProperty**](extendedproperty.md) object from the collection.</span></span>
-   <span data-ttu-id="e373c-113">Récupérez le nombre de propriétés étendues dans la collection.</span><span class="sxs-lookup"><span data-stu-id="e373c-113">Retrieve the number of extended properties in the collection.</span></span>
-   <span data-ttu-id="e373c-114">Récupérez un objet [**ExtendedProperty**](extendedproperty.md) spécifique de la collection.</span><span class="sxs-lookup"><span data-stu-id="e373c-114">Retrieve a specific [**ExtendedProperty**](extendedproperty.md) object from the collection.</span></span>
-   <span data-ttu-id="e373c-115">Itérez au sein de la collection.</span><span class="sxs-lookup"><span data-stu-id="e373c-115">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="e373c-116">Membres</span><span class="sxs-lookup"><span data-stu-id="e373c-116">Members</span></span>

<span data-ttu-id="e373c-117">L’objet **ExtendedProperties** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e373c-117">The **ExtendedProperties** object has these types of members:</span></span>

-   [<span data-ttu-id="e373c-118">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e373c-118">Methods</span></span>](#methods)
-   [<span data-ttu-id="e373c-119">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e373c-119">Properties</span></span>](#extendedproperties-object)

### <a name="methods"></a><span data-ttu-id="e373c-120">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e373c-120">Methods</span></span>

<span data-ttu-id="e373c-121">L’objet **ExtendedProperties** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="e373c-121">The **ExtendedProperties** object has these methods.</span></span>



| <span data-ttu-id="e373c-122">Méthode</span><span class="sxs-lookup"><span data-stu-id="e373c-122">Method</span></span>                                      | <span data-ttu-id="e373c-123">Description</span><span class="sxs-lookup"><span data-stu-id="e373c-123">Description</span></span>                                                                                    |
|:--------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e373c-124">**Complémentaires**</span><span class="sxs-lookup"><span data-stu-id="e373c-124">**Add**</span></span>](extendedproperties-add.md)       | <span data-ttu-id="e373c-125">Ajoute un objet [**ExtendedProperty**](extendedproperty.md) à la collection.</span><span class="sxs-lookup"><span data-stu-id="e373c-125">Adds an [**ExtendedProperty**](extendedproperty.md) object to the collection.</span></span><br/>      |
| [<span data-ttu-id="e373c-126">**Installez**</span><span class="sxs-lookup"><span data-stu-id="e373c-126">**Remove**</span></span>](extendedproperties-remove.md) | <span data-ttu-id="e373c-127">Supprime un objet [**ExtendedProperty**](extendedproperty.md) de la collection.</span><span class="sxs-lookup"><span data-stu-id="e373c-127">Removes an [**ExtendedProperty**](extendedproperty.md) object from the collection.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e373c-128">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e373c-128">Properties</span></span>

<span data-ttu-id="e373c-129">L’objet **ExtendedProperties** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="e373c-129">The **ExtendedProperties** object has these properties.</span></span>



| <span data-ttu-id="e373c-130">Propriété</span><span class="sxs-lookup"><span data-stu-id="e373c-130">Property</span></span>                                                   | <span data-ttu-id="e373c-131">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="e373c-131">Access type</span></span>          | <span data-ttu-id="e373c-132">Description</span><span class="sxs-lookup"><span data-stu-id="e373c-132">Description</span></span>                                                                                                                                                                                                                     |
|:-----------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e373c-133">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="e373c-133">**\_NewEnum**</span></span>](extendedproperties-newenum.md)<br/> | <span data-ttu-id="e373c-134">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e373c-134">Read-only</span></span><br/> | <span data-ttu-id="e373c-135">Récupère une interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) sur un objet qui peut être utilisé pour énumérer la collection.</span><span class="sxs-lookup"><span data-stu-id="e373c-135">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="e373c-136">Cette propriété est masquée dans Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="e373c-136">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="e373c-137">**Saut**</span><span class="sxs-lookup"><span data-stu-id="e373c-137">**Count**</span></span>](extendedproperties-count.md)<br/>       | <span data-ttu-id="e373c-138">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e373c-138">Read-only</span></span><br/> | <span data-ttu-id="e373c-139">Récupère le nombre d’objets [**ExtendedProperty**](extendedproperty.md) dans la collection.</span><span class="sxs-lookup"><span data-stu-id="e373c-139">Retrieves the number of [**ExtendedProperty**](extendedproperty.md) objects in the collection.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="e373c-140">**Élément**</span><span class="sxs-lookup"><span data-stu-id="e373c-140">**Item**</span></span>](extendedproperties-item.md)<br/>         | <span data-ttu-id="e373c-141">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e373c-141">Read-only</span></span><br/> | <span data-ttu-id="e373c-142">Récupère un objet [**ExtendedProperty**](extendedproperty.md) qui représente la propriété étendue indexée de la collection.</span><span class="sxs-lookup"><span data-stu-id="e373c-142">Retrieves an [**ExtendedProperty**](extendedproperty.md) object that represents the indexed extended property of the collection.</span></span> <span data-ttu-id="e373c-143">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="e373c-143">This is the default property.</span></span><br/>                                                      |



 

## <a name="remarks"></a><span data-ttu-id="e373c-144">Notes</span><span class="sxs-lookup"><span data-stu-id="e373c-144">Remarks</span></span>

<span data-ttu-id="e373c-145">Impossible de créer l’objet **ExtendedProperties** .</span><span class="sxs-lookup"><span data-stu-id="e373c-145">The **ExtendedProperties** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="e373c-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e373c-146">Requirements</span></span>



| <span data-ttu-id="e373c-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e373c-147">Requirement</span></span> | <span data-ttu-id="e373c-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="e373c-148">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e373c-149">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="e373c-149">End of client support</span></span><br/> | <span data-ttu-id="e373c-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e373c-150">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e373c-151">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="e373c-151">End of server support</span></span><br/> | <span data-ttu-id="e373c-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e373c-152">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e373c-153">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="e373c-153">Redistributable</span></span><br/>       | <span data-ttu-id="e373c-154">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="e373c-154">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e373c-155">DLL</span><span class="sxs-lookup"><span data-stu-id="e373c-155">DLL</span></span><br/>                   | <dl> <span data-ttu-id="e373c-156"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e373c-156"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
