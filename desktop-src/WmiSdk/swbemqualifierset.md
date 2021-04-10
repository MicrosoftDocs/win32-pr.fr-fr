---
description: Un objet SWbemQualifierSet est une collection d’objets SWbemQualifier.
ms.assetid: 7ac5469c-357b-499d-a558-30bf760c5311
ms.tgt_platform: multiple
title: Objet SWbemQualifierSet (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifierSet
- ISWbemQualifierSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e74b495313e8061cc6e08e255d1d055bb2f72a92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042758"
---
# <a name="swbemqualifierset-object"></a><span data-ttu-id="88d77-103">Objet SWbemQualifierSet</span><span class="sxs-lookup"><span data-stu-id="88d77-103">SWbemQualifierSet object</span></span>

<span data-ttu-id="88d77-104">Un objet **SWbemQualifierSet** est une collection d’objets [**SWbemQualifier**](swbemqualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="88d77-104">An **SWbemQualifierSet** object is a collection of [**SWbemQualifier**](swbemqualifier.md) objects.</span></span> <span data-ttu-id="88d77-105">Les éléments sont ajoutés à la collection à l’aide de la méthode [**Add**](swbemqualifierset-add.md) , récupérés à partir de la collection à l’aide de la méthode [**Item**](swbemqualifierset-item.md) et supprimés de la collection à l’aide de la méthode [**Remove**](swbemqualifierset-remove.md) .</span><span class="sxs-lookup"><span data-stu-id="88d77-105">Items are added to the collection using the [**Add**](swbemqualifierset-add.md) method, retrieved from the collection using the [**Item**](swbemqualifierset-item.md) method, and removed from the collection using the [**Remove**](swbemqualifierset-remove.md) method.</span></span> <span data-ttu-id="88d77-106">Cet objet ne peut pas être créé par l’appel VBScript [CreateObject](creating-an-object-using-vbscript.md) .</span><span class="sxs-lookup"><span data-stu-id="88d77-106">This object cannot be created by the VBScript [CreateObject](creating-an-object-using-vbscript.md) call.</span></span>

<span data-ttu-id="88d77-107">Pour plus d’informations, consultez [accès à une collection](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="88d77-107">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

<span data-ttu-id="88d77-108">Les objets [**SWbemQualifier**](swbemqualifier.md) qui composent une collection **SWbemQualifierSet** décrivent les qualificateurs attachés à une classe, une instance, une méthode ou un paramètre de méthode WMI.</span><span class="sxs-lookup"><span data-stu-id="88d77-108">The [**SWbemQualifier**](swbemqualifier.md) objects that make up an **SWbemQualifierSet** collection describe the qualifiers attached to a WMI class, instance, method, or method parameter.</span></span>

## <a name="members"></a><span data-ttu-id="88d77-109">Membres</span><span class="sxs-lookup"><span data-stu-id="88d77-109">Members</span></span>

<span data-ttu-id="88d77-110">L’objet **SWbemQualifierSet** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="88d77-110">The **SWbemQualifierSet** object has these types of members:</span></span>

-   [<span data-ttu-id="88d77-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="88d77-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="88d77-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="88d77-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="88d77-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="88d77-113">Methods</span></span>

<span data-ttu-id="88d77-114">L’objet **SWbemQualifierSet** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="88d77-114">The **SWbemQualifierSet** object has these methods.</span></span>



| <span data-ttu-id="88d77-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="88d77-115">Method</span></span>                                     | <span data-ttu-id="88d77-116">Description</span><span class="sxs-lookup"><span data-stu-id="88d77-116">Description</span></span>                                                                                                 |
|:-------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="88d77-117">**Complémentaires**</span><span class="sxs-lookup"><span data-stu-id="88d77-117">**Add**</span></span>](swbemqualifierset-add.md)       | <span data-ttu-id="88d77-118">Ajoute un objet [**SWbemQualifier**](swbemqualifier.md) à la collection **SWbemQualifierSet** .</span><span class="sxs-lookup"><span data-stu-id="88d77-118">Adds an [**SWbemQualifier**](swbemqualifier.md) object to the **SWbemQualifierSet** collection.</span></span><br/> |
| [<span data-ttu-id="88d77-119">**Élément**</span><span class="sxs-lookup"><span data-stu-id="88d77-119">**Item**</span></span>](swbemqualifierset-item.md)     | <span data-ttu-id="88d77-120">Retourne un objet nommé [**SWbemQualifier**](swbemqualifier.md) à partir de la collection.</span><span class="sxs-lookup"><span data-stu-id="88d77-120">Returns a named [**SWbemQualifier**](swbemqualifier.md) object from the collection.</span></span><br/>             |
| [<span data-ttu-id="88d77-121">**Installez**</span><span class="sxs-lookup"><span data-stu-id="88d77-121">**Remove**</span></span>](swbemqualifierset-remove.md) | <span data-ttu-id="88d77-122">Supprime un qualificateur nommé de la collection.</span><span class="sxs-lookup"><span data-stu-id="88d77-122">Deletes a named qualifier from the collection.</span></span><br/>                                                   |



 

### <a name="properties"></a><span data-ttu-id="88d77-123">Propriétés</span><span class="sxs-lookup"><span data-stu-id="88d77-123">Properties</span></span>

<span data-ttu-id="88d77-124">L’objet **SWbemQualifierSet** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="88d77-124">The **SWbemQualifierSet** object has these properties.</span></span>



| <span data-ttu-id="88d77-125">Propriété</span><span class="sxs-lookup"><span data-stu-id="88d77-125">Property</span></span>                                            | <span data-ttu-id="88d77-126">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="88d77-126">Access type</span></span>          | <span data-ttu-id="88d77-127">Description</span><span class="sxs-lookup"><span data-stu-id="88d77-127">Description</span></span>                                                                     |
|:----------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="88d77-128">**Saut**</span><span class="sxs-lookup"><span data-stu-id="88d77-128">**Count**</span></span>](swbemqualifierset-count.md)<br/> | <span data-ttu-id="88d77-129">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="88d77-129">Read-only</span></span><br/> | <span data-ttu-id="88d77-130">Contient le nombre d’éléments d’une collection **SWbemQualifierSet** .</span><span class="sxs-lookup"><span data-stu-id="88d77-130">Contains the number of items in an **SWbemQualifierSet** collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="88d77-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="88d77-131">Requirements</span></span>



| <span data-ttu-id="88d77-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="88d77-132">Requirement</span></span> | <span data-ttu-id="88d77-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="88d77-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="88d77-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="88d77-134">Minimum supported client</span></span><br/> | <span data-ttu-id="88d77-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="88d77-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="88d77-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="88d77-136">Minimum supported server</span></span><br/> | <span data-ttu-id="88d77-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="88d77-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="88d77-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="88d77-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="88d77-139"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="88d77-139"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="88d77-140">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="88d77-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="88d77-141"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="88d77-141"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="88d77-142">DLL</span><span class="sxs-lookup"><span data-stu-id="88d77-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88d77-143"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88d77-143"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="88d77-144">CLSID</span><span class="sxs-lookup"><span data-stu-id="88d77-144">CLSID</span></span><br/>                    | <span data-ttu-id="88d77-145">CLSID \_ SWbemQualifierSet</span><span class="sxs-lookup"><span data-stu-id="88d77-145">CLSID\_SWbemQualifierSet</span></span><br/>                                                     |
| <span data-ttu-id="88d77-146">IID</span><span class="sxs-lookup"><span data-stu-id="88d77-146">IID</span></span><br/>                      | <span data-ttu-id="88d77-147">IID \_ ISWbemQualifierSet</span><span class="sxs-lookup"><span data-stu-id="88d77-147">IID\_ISWbemQualifierSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="88d77-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="88d77-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88d77-149">Scripts d’objets d’API</span><span class="sxs-lookup"><span data-stu-id="88d77-149">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




