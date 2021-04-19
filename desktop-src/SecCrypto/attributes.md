---
description: Représente une collection d’objets Attribute.
ms.assetid: 6116e61e-3ec5-4992-90ab-e3c7ced291b6
title: Objet Attributes
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2493d4e1bbcbeb2dc7e7b335513beb84c3f28d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523549"
---
# <a name="attributes-object"></a><span data-ttu-id="fb764-103">Objet Attributes</span><span class="sxs-lookup"><span data-stu-id="fb764-103">Attributes object</span></span>

<span data-ttu-id="fb764-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fb764-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="fb764-105">Utilisez plutôt la [**classe CryptographicAttributeObjectCollection**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="fb764-105">Instead, use the [**CryptographicAttributeObjectCollection Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="fb764-106">L' **objet** Attributes représente une collection d’objets [**attribute**](attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="fb764-106">The **Attributes** object represents a collection of [**Attribute**](attribute.md) objects.</span></span> <span data-ttu-id="fb764-107">Chaque objet d' [**attribut**](attribute.md) représente un attribut unique d’un message.</span><span class="sxs-lookup"><span data-stu-id="fb764-107">Each [**Attribute**](attribute.md) object represents a single attribute of a message.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="fb764-108">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="fb764-108">When to use</span></span>

<span data-ttu-id="fb764-109">L’objet **attributes** est utilisé pour effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="fb764-109">The **Attributes** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="fb764-110">Ajoutez ou supprimez un objet [**attribut**](attribute.md) spécifique de la collection.</span><span class="sxs-lookup"><span data-stu-id="fb764-110">Add or remove a specific [**Attribute**](attribute.md) object from the collection.</span></span>
-   <span data-ttu-id="fb764-111">Efface la collection.</span><span class="sxs-lookup"><span data-stu-id="fb764-111">Clear the collection.</span></span>
-   <span data-ttu-id="fb764-112">Récupérez le nombre d’attributs dans la collection.</span><span class="sxs-lookup"><span data-stu-id="fb764-112">Retrieve the number of attributes in the collection.</span></span>
-   <span data-ttu-id="fb764-113">Récupérez un objet [**attribut**](attribute.md) spécifique de la collection.</span><span class="sxs-lookup"><span data-stu-id="fb764-113">Retrieve a specific [**Attribute**](attribute.md) object from the collection.</span></span>
-   <span data-ttu-id="fb764-114">Itérez au sein de la collection.</span><span class="sxs-lookup"><span data-stu-id="fb764-114">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="fb764-115">Membres</span><span class="sxs-lookup"><span data-stu-id="fb764-115">Members</span></span>

<span data-ttu-id="fb764-116">L’objet **attributes** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="fb764-116">The **Attributes** object has these types of members:</span></span>

-   [<span data-ttu-id="fb764-117">Méthodes</span><span class="sxs-lookup"><span data-stu-id="fb764-117">Methods</span></span>](#methods)
-   [<span data-ttu-id="fb764-118">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fb764-118">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="fb764-119">Méthodes</span><span class="sxs-lookup"><span data-stu-id="fb764-119">Methods</span></span>

<span data-ttu-id="fb764-120">L’objet **attributes** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="fb764-120">The **Attributes** object has these methods.</span></span>



| <span data-ttu-id="fb764-121">Méthode</span><span class="sxs-lookup"><span data-stu-id="fb764-121">Method</span></span>                              | <span data-ttu-id="fb764-122">Description</span><span class="sxs-lookup"><span data-stu-id="fb764-122">Description</span></span>                                                                       |
|:------------------------------------|:----------------------------------------------------------------------------------|
| [<span data-ttu-id="fb764-123">**Complémentaires**</span><span class="sxs-lookup"><span data-stu-id="fb764-123">**Add**</span></span>](attributes-add.md)       | <span data-ttu-id="fb764-124">Ajoute un objet d' [**attribut**](attribute.md) à la collection.</span><span class="sxs-lookup"><span data-stu-id="fb764-124">Adds an [**Attribute**](attribute.md) object to the collection.</span></span><br/>       |
| [<span data-ttu-id="fb764-125">**Effacé**</span><span class="sxs-lookup"><span data-stu-id="fb764-125">**Clear**</span></span>](attributes-clear.md)   | <span data-ttu-id="fb764-126">Efface tous les objets [**attribut**](attribute.md) de la collection.</span><span class="sxs-lookup"><span data-stu-id="fb764-126">Clears all [**Attribute**](attribute.md) objects from the collection.</span></span><br/> |
| [<span data-ttu-id="fb764-127">**Installez**</span><span class="sxs-lookup"><span data-stu-id="fb764-127">**Remove**</span></span>](attributes-remove.md) | <span data-ttu-id="fb764-128">Supprime un objet d' [**attribut**](attribute.md) de la collection.</span><span class="sxs-lookup"><span data-stu-id="fb764-128">Removes an [**Attribute**](attribute.md) object from the collection.</span></span><br/>  |



 

### <a name="properties"></a><span data-ttu-id="fb764-129">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fb764-129">Properties</span></span>

<span data-ttu-id="fb764-130">L’objet **attributes** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="fb764-130">The **Attributes** object has these properties.</span></span>



| <span data-ttu-id="fb764-131">Propriété</span><span class="sxs-lookup"><span data-stu-id="fb764-131">Property</span></span>                                           | <span data-ttu-id="fb764-132">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="fb764-132">Access type</span></span>          | <span data-ttu-id="fb764-133">Description</span><span class="sxs-lookup"><span data-stu-id="fb764-133">Description</span></span>                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fb764-134">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="fb764-134">**\_NewEnum**</span></span>](attributes-newenum.md)<br/> | <span data-ttu-id="fb764-135">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fb764-135">Read-only</span></span><br/> | <span data-ttu-id="fb764-136">Récupère une interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) sur un objet qui peut être utilisé pour énumérer la collection.</span><span class="sxs-lookup"><span data-stu-id="fb764-136">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="fb764-137">Cette propriété est masquée dans Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="fb764-137">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="fb764-138">**Saut**</span><span class="sxs-lookup"><span data-stu-id="fb764-138">**Count**</span></span>](attributes-count.md)<br/>       | <span data-ttu-id="fb764-139">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fb764-139">Read-only</span></span><br/> | <span data-ttu-id="fb764-140">Récupère le nombre d’objets [**attribute**](attribute.md) dans la collection.</span><span class="sxs-lookup"><span data-stu-id="fb764-140">Retrieves the number of [**Attribute**](attribute.md) objects in the collection.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="fb764-141">**Élément**</span><span class="sxs-lookup"><span data-stu-id="fb764-141">**Item**</span></span>](attributes-item.md)<br/>         | <span data-ttu-id="fb764-142">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fb764-142">Read-only</span></span><br/> | <span data-ttu-id="fb764-143">Récupère l’objet d' [**attribut**](attribute.md) qui représente l’attribut indexé.</span><span class="sxs-lookup"><span data-stu-id="fb764-143">Retrieves the [**Attribute**](attribute.md) object that represents the indexed attribute.</span></span> <span data-ttu-id="fb764-144">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="fb764-144">This is the default property.</span></span><br/>                                                                                             |



 

## <a name="remarks"></a><span data-ttu-id="fb764-145">Notes</span><span class="sxs-lookup"><span data-stu-id="fb764-145">Remarks</span></span>

<span data-ttu-id="fb764-146">Impossible de créer l’objet **attributes** .</span><span class="sxs-lookup"><span data-stu-id="fb764-146">The **Attributes** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb764-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fb764-147">Requirements</span></span>



| <span data-ttu-id="fb764-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fb764-148">Requirement</span></span> | <span data-ttu-id="fb764-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="fb764-149">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb764-150">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="fb764-150">End of client support</span></span><br/> | <span data-ttu-id="fb764-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fb764-151">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="fb764-152">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="fb764-152">End of server support</span></span><br/> | <span data-ttu-id="fb764-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fb764-153">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="fb764-154">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="fb764-154">Redistributable</span></span><br/>       | <span data-ttu-id="fb764-155">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="fb764-155">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="fb764-156">DLL</span><span class="sxs-lookup"><span data-stu-id="fb764-156">DLL</span></span><br/>                   | <dl> <span data-ttu-id="fb764-157"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb764-157"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb764-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fb764-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb764-159">Objets de chiffrement</span><span class="sxs-lookup"><span data-stu-id="fb764-159">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
