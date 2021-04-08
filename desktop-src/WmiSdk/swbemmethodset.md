---
description: Un objet SWbemMethodSet est une collection d’objets SWbemMethod. Les éléments sont récupérés à l’aide de la méthode Item. Pour plus d’informations, consultez accès à une collection. Cet objet ne peut pas être créé par l’appel VBScript CreateObject.
ms.assetid: 0ca2601f-ed40-472e-b4f2-eee750c8c8d1
ms.tgt_platform: multiple
title: Objet SWbemMethodSet (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethodSet
- ISWbemMethodSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d47c4dc8335077d6f8568be4b56200558942ac39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865662"
---
# <a name="swbemmethodset-object"></a><span data-ttu-id="a9925-106">Objet SWbemMethodSet</span><span class="sxs-lookup"><span data-stu-id="a9925-106">SWbemMethodSet object</span></span>

<span data-ttu-id="a9925-107">Un objet **SWbemMethodSet** est une collection d’objets [**SWbemMethod**](swbemmethod.md) .</span><span class="sxs-lookup"><span data-stu-id="a9925-107">An **SWbemMethodSet** object is a collection of [**SWbemMethod**](swbemmethod.md) objects.</span></span> <span data-ttu-id="a9925-108">Les éléments sont récupérés à l’aide de la méthode [**Item**](swbemmethodset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="a9925-108">Items are retrieved using the [**Item**](swbemmethodset-item.md) method.</span></span> <span data-ttu-id="a9925-109">Pour plus d’informations, consultez [accès à une collection](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="a9925-109">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span> <span data-ttu-id="a9925-110">Cet objet ne peut pas être créé par l’appel VBScript **CreateObject** .</span><span class="sxs-lookup"><span data-stu-id="a9925-110">This object cannot be created by the VBScript **CreateObject** call.</span></span>

> [!Note]  
> <span data-ttu-id="a9925-111">Dans cette version de l’API, l’accès en écriture aux informations de méthode n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="a9925-111">In this version of the API, write access to method information is not supported.</span></span> <span data-ttu-id="a9925-112">Si vous souhaitez définir des méthodes ou modifier des définitions de méthode existantes, vous pouvez définir les modifications de méthode dans un fichier MOF et soumettre les modifications à l’aide du compilateur MOF.</span><span class="sxs-lookup"><span data-stu-id="a9925-112">If you want to define methods or modify existing method definitions, you can define the method changes in a MOF file and submit the changes using the MOF Compiler.</span></span> <span data-ttu-id="a9925-113">Vous pouvez également utiliser l’API COM WMI.</span><span class="sxs-lookup"><span data-stu-id="a9925-113">Alternatively, use the WMI COM API.</span></span>

 

## <a name="members"></a><span data-ttu-id="a9925-114">Membres</span><span class="sxs-lookup"><span data-stu-id="a9925-114">Members</span></span>

<span data-ttu-id="a9925-115">L’objet **SWbemMethodSet** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a9925-115">The **SWbemMethodSet** object has these types of members:</span></span>

-   [<span data-ttu-id="a9925-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a9925-116">Methods</span></span>](#swbemmethodset-object)
-   [<span data-ttu-id="a9925-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a9925-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a9925-118">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a9925-118">Methods</span></span>

<span data-ttu-id="a9925-119">L’objet **SWbemMethodSet** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="a9925-119">The **SWbemMethodSet** object has these methods.</span></span>



| <span data-ttu-id="a9925-120">Méthode</span><span class="sxs-lookup"><span data-stu-id="a9925-120">Method</span></span>                              | <span data-ttu-id="a9925-121">Description</span><span class="sxs-lookup"><span data-stu-id="a9925-121">Description</span></span>                                                                                                                                  |
|:------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a9925-122">**Élément**</span><span class="sxs-lookup"><span data-stu-id="a9925-122">**Item**</span></span>](swbemmethodset-item.md) | <span data-ttu-id="a9925-123">Récupère un objet [**SWbemMethod**](swbemmethod.md) de la collection.</span><span class="sxs-lookup"><span data-stu-id="a9925-123">Retrieves an [**SWbemMethod**](swbemmethod.md) object from the collection.</span></span> <span data-ttu-id="a9925-124">Il s’agit de la méthode Automation par défaut de cet objet.</span><span class="sxs-lookup"><span data-stu-id="a9925-124">This is the default automation method of this object.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a9925-125">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a9925-125">Properties</span></span>

<span data-ttu-id="a9925-126">L’objet **SWbemMethodSet** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="a9925-126">The **SWbemMethodSet** object has these properties.</span></span>



| <span data-ttu-id="a9925-127">Propriété</span><span class="sxs-lookup"><span data-stu-id="a9925-127">Property</span></span>                                         | <span data-ttu-id="a9925-128">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="a9925-128">Access type</span></span>          | <span data-ttu-id="a9925-129">Description</span><span class="sxs-lookup"><span data-stu-id="a9925-129">Description</span></span>                                       |
|:-------------------------------------------------|:---------------------|:--------------------------------------------------|
| [<span data-ttu-id="a9925-130">**Saut**</span><span class="sxs-lookup"><span data-stu-id="a9925-130">**Count**</span></span>](swbemmethodset-count.md)<br/> | <span data-ttu-id="a9925-131">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a9925-131">Read-only</span></span><br/> | <span data-ttu-id="a9925-132">Nombre d’éléments dans la collection</span><span class="sxs-lookup"><span data-stu-id="a9925-132">The number of items in the collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a9925-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a9925-133">Requirements</span></span>



| <span data-ttu-id="a9925-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a9925-134">Requirement</span></span> | <span data-ttu-id="a9925-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="a9925-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9925-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9925-136">Minimum supported client</span></span><br/> | <span data-ttu-id="a9925-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a9925-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a9925-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9925-138">Minimum supported server</span></span><br/> | <span data-ttu-id="a9925-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a9925-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a9925-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="a9925-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9925-141"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9925-141"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a9925-142">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="a9925-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="a9925-143"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a9925-143"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a9925-144">DLL</span><span class="sxs-lookup"><span data-stu-id="a9925-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9925-145"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9925-145"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a9925-146">CLSID</span><span class="sxs-lookup"><span data-stu-id="a9925-146">CLSID</span></span><br/>                    | <span data-ttu-id="a9925-147">CLSID \_ SWbemMethodSet</span><span class="sxs-lookup"><span data-stu-id="a9925-147">CLSID\_SWbemMethodSet</span></span><br/>                                                        |
| <span data-ttu-id="a9925-148">IID</span><span class="sxs-lookup"><span data-stu-id="a9925-148">IID</span></span><br/>                      | <span data-ttu-id="a9925-149">IID \_ ISWbemMethodSet</span><span class="sxs-lookup"><span data-stu-id="a9925-149">IID\_ISWbemMethodSet</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="a9925-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a9925-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9925-151">Scripts d’objets d’API</span><span class="sxs-lookup"><span data-stu-id="a9925-151">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




