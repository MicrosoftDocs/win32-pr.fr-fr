---
description: Un objet SWbemPropertySet est une collection d’objets SWbemProperty.
ms.assetid: 0edad17b-facc-4885-9ce4-561ca6f57a66
ms.tgt_platform: multiple
title: Objet SWbemPropertySet (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPropertySet
- ISWbemPropertySet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 05ae5d5e0bfbc5ab0733e00e4649baa2849d3446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106539729"
---
# <a name="swbempropertyset-object"></a><span data-ttu-id="5a183-103">Objet SWbemPropertySet</span><span class="sxs-lookup"><span data-stu-id="5a183-103">SWbemPropertySet object</span></span>

<span data-ttu-id="5a183-104">Un objet **SWbemPropertySet** est une collection d’objets [**SWbemProperty**](swbemproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="5a183-104">An **SWbemPropertySet** object is a collection of [**SWbemProperty**](swbemproperty.md) objects.</span></span> <span data-ttu-id="5a183-105">Vous pouvez ajouter des éléments à la collection à l’aide de la méthode [**Add**](swbempropertyset-add.md) , récupérer des éléments de la collection à l’aide de la méthode [**Item**](swbempropertyset-item.md) et supprimer des éléments de la collection à l’aide de la méthode [**Remove**](swbempropertyset-remove.md) .</span><span class="sxs-lookup"><span data-stu-id="5a183-105">You can add items to the collection using the [**Add**](swbempropertyset-add.md) method, retrieve items from the collection using the [**Item**](swbempropertyset-item.md) method, and remove items from the collection using the [**Remove**](swbempropertyset-remove.md) method.</span></span> <span data-ttu-id="5a183-106">Pour plus d’informations, consultez [accès à une collection](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="5a183-106">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span> <span data-ttu-id="5a183-107">Cet objet ne peut pas être créé par l’appel VBScript [CreateObject](creating-an-object-using-vbscript.md) .</span><span class="sxs-lookup"><span data-stu-id="5a183-107">This object cannot be created by the VBScript [CreateObject](creating-an-object-using-vbscript.md) call.</span></span>

<span data-ttu-id="5a183-108">Les objets [**SWbemProperty**](swbemproperty.md) qui composent une collection **SWbemPropertySet** sont utilisés pour décrire les propriétés d’une instance ou d’une classe WMI unique.</span><span class="sxs-lookup"><span data-stu-id="5a183-108">The [**SWbemProperty**](swbemproperty.md) objects that make up an **SWbemPropertySet** collection are used to describe the properties of a single WMI class or instance.</span></span>

## <a name="members"></a><span data-ttu-id="5a183-109">Membres</span><span class="sxs-lookup"><span data-stu-id="5a183-109">Members</span></span>

<span data-ttu-id="5a183-110">L’objet **SWbemPropertySet** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="5a183-110">The **SWbemPropertySet** object has these types of members:</span></span>

-   [<span data-ttu-id="5a183-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5a183-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="5a183-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5a183-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5a183-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5a183-113">Methods</span></span>

<span data-ttu-id="5a183-114">L’objet **SWbemPropertySet** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="5a183-114">The **SWbemPropertySet** object has these methods.</span></span>



| <span data-ttu-id="5a183-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="5a183-115">Method</span></span>                                    | <span data-ttu-id="5a183-116">Description</span><span class="sxs-lookup"><span data-stu-id="5a183-116">Description</span></span>                                                                                                                     |
|:------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5a183-117">**Complémentaires**</span><span class="sxs-lookup"><span data-stu-id="5a183-117">**Add**</span></span>](swbempropertyset-add.md)       | <span data-ttu-id="5a183-118">Ajoute un objet [**SWbemProperty**](swbemproperty.md) à la collection **SWbemPropertySet** .</span><span class="sxs-lookup"><span data-stu-id="5a183-118">Adds an [**SWbemProperty**](swbemproperty.md) object to the **SWbemPropertySet** collection.</span></span><br/>                        |
| [<span data-ttu-id="5a183-119">**Élément**</span><span class="sxs-lookup"><span data-stu-id="5a183-119">**Item**</span></span>](swbempropertyset-item.md)     | <span data-ttu-id="5a183-120">Obtient un [**SWbemProperty**](swbemproperty.md) nommé à partir de la collection.</span><span class="sxs-lookup"><span data-stu-id="5a183-120">Gets a named [**SWbemProperty**](swbemproperty.md) from the collection.</span></span> <span data-ttu-id="5a183-121">Il s’agit de la méthode par défaut pour cet objet.</span><span class="sxs-lookup"><span data-stu-id="5a183-121">This is the default method for this object.</span></span><br/> |
| [<span data-ttu-id="5a183-122">**Installez**</span><span class="sxs-lookup"><span data-stu-id="5a183-122">**Remove**</span></span>](swbempropertyset-remove.md) | <span data-ttu-id="5a183-123">Supprime un objet [**SWbemProperty**](swbemproperty.md) de la collection.</span><span class="sxs-lookup"><span data-stu-id="5a183-123">Deletes an [**SWbemProperty**](swbemproperty.md) object from the collection.</span></span><br/>                                        |



 

### <a name="properties"></a><span data-ttu-id="5a183-124">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5a183-124">Properties</span></span>

<span data-ttu-id="5a183-125">L’objet **SWbemPropertySet** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="5a183-125">The **SWbemPropertySet** object has these properties.</span></span>



| <span data-ttu-id="5a183-126">Propriété</span><span class="sxs-lookup"><span data-stu-id="5a183-126">Property</span></span>                                           | <span data-ttu-id="5a183-127">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="5a183-127">Access type</span></span>          | <span data-ttu-id="5a183-128">Description</span><span class="sxs-lookup"><span data-stu-id="5a183-128">Description</span></span>                                                            |
|:---------------------------------------------------|:---------------------|:-----------------------------------------------------------------------|
| [<span data-ttu-id="5a183-129">**Saut**</span><span class="sxs-lookup"><span data-stu-id="5a183-129">**Count**</span></span>](swbempropertyset-count.md)<br/> | <span data-ttu-id="5a183-130">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5a183-130">Read-only</span></span><br/> | <span data-ttu-id="5a183-131">Nombre d’éléments dans la collection **SWbemPropertySet** .</span><span class="sxs-lookup"><span data-stu-id="5a183-131">The number of items in the **SWbemPropertySet** collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="5a183-132">Exemples</span><span class="sxs-lookup"><span data-stu-id="5a183-132">Examples</span></span>

<span data-ttu-id="5a183-133">L’exemple VBScript suivant montre comment [**SWbemPropertySet. Remove**](swbempropertyset-remove.md) peut retourner **wbemErrResetToDefault** si la propriété est substituée.</span><span class="sxs-lookup"><span data-stu-id="5a183-133">The following VBScript sample demonstrates how [**SWbemPropertySet.Remove**](swbempropertyset-remove.md) can return **wbemErrResetToDefault** if the property is overridden.</span></span>


```VB
on error resume next 

'Create a keyed class with a defaulted property
set service = GetObject("Winmgmts:")
set emptyclass = service.Get
emptyclass.path_.class = "REMOVETEST00"
set prop = emptyclass.properties_.add ("p", 19)

prop.qualifiers_.add "key", true
emptyclass.properties_.add ("q", 19).Value = 12

emptyclass.put_

'create an instance and override the property
set instance = service.get ("RemoveTest00").spawninstance_

instance.properties_("q").Value = 24
instance.properties_("p").Value = 1
instance.put_

'retrieve the instance and remove the property
set instance = service.get ("removetest00=1")
set property = instance.properties_ ("q")

WScript.echo "Overridden value of property is [24]:", property.value
WScript.echo ""

instance.properties_.remove "q"
set property = instance.properties_ ("q")
WScript.echo "Value of property after removal is [12]:", property.value
WScript.echo ""

if err <> 0 then
 WScript.Echo "0x" & Hex(Err.Number), Err.Description, Err.Source
end if
```



## <a name="requirements"></a><span data-ttu-id="5a183-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5a183-134">Requirements</span></span>



| <span data-ttu-id="5a183-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5a183-135">Requirement</span></span> | <span data-ttu-id="5a183-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="5a183-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a183-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a183-137">Minimum supported client</span></span><br/> | <span data-ttu-id="5a183-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5a183-138">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5a183-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a183-139">Minimum supported server</span></span><br/> | <span data-ttu-id="5a183-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5a183-140">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5a183-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="5a183-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a183-142"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a183-142"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5a183-143">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="5a183-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="5a183-144"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5a183-144"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5a183-145">DLL</span><span class="sxs-lookup"><span data-stu-id="5a183-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a183-146"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a183-146"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="5a183-147">CLSID</span><span class="sxs-lookup"><span data-stu-id="5a183-147">CLSID</span></span><br/>                    | <span data-ttu-id="5a183-148">CLSID \_ SWbemPropertySet</span><span class="sxs-lookup"><span data-stu-id="5a183-148">CLSID\_SWbemPropertySet</span></span><br/>                                                      |
| <span data-ttu-id="5a183-149">IID</span><span class="sxs-lookup"><span data-stu-id="5a183-149">IID</span></span><br/>                      | <span data-ttu-id="5a183-150">IID \_ ISWbemPropertySet</span><span class="sxs-lookup"><span data-stu-id="5a183-150">IID\_ISWbemPropertySet</span></span><br/>                                                       |



## <a name="see-also"></a><span data-ttu-id="5a183-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5a183-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a183-152">Scripts d’objets d’API</span><span class="sxs-lookup"><span data-stu-id="5a183-152">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




