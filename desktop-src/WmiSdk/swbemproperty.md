---
description: L’objet SWbemProperty représente une propriété WMI unique d’un objet managé. Cet objet ne peut pas être créé par l’appel VBScript CreateObject.
ms.assetid: 2ddcfffa-a7b4-4fd6-926d-411de27f6212
ms.tgt_platform: multiple
title: Objet SWbemProperty (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemProperty
- ISWbemProperty
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9c71db4063f5de6b48b2e8213f21ca1320a880fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210730"
---
# <a name="swbemproperty-object"></a><span data-ttu-id="5ea9b-104">Objet SWbemProperty</span><span class="sxs-lookup"><span data-stu-id="5ea9b-104">SWbemProperty object</span></span>

<span data-ttu-id="5ea9b-105">L’objet **SWbemProperty** représente une propriété WMI unique d’un objet managé.</span><span class="sxs-lookup"><span data-stu-id="5ea9b-105">The **SWbemProperty** object represents a single WMI property of a managed object.</span></span> <span data-ttu-id="5ea9b-106">Cet objet ne peut pas être créé par l’appel VBScript [CreateObject](creating-an-object-using-vbscript.md) .</span><span class="sxs-lookup"><span data-stu-id="5ea9b-106">This object cannot be created by the VBScript [CreateObject](creating-an-object-using-vbscript.md) call.</span></span>

## <a name="members"></a><span data-ttu-id="5ea9b-107">Membres</span><span class="sxs-lookup"><span data-stu-id="5ea9b-107">Members</span></span>

<span data-ttu-id="5ea9b-108">L’objet **SWbemProperty** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="5ea9b-108">The **SWbemProperty** object has these types of members:</span></span>

-   [<span data-ttu-id="5ea9b-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5ea9b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5ea9b-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5ea9b-110">Properties</span></span>

<span data-ttu-id="5ea9b-111">L’objet **SWbemProperty** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="5ea9b-111">The **SWbemProperty** object has these properties.</span></span>



| <span data-ttu-id="5ea9b-112">Propriété</span><span class="sxs-lookup"><span data-stu-id="5ea9b-112">Property</span></span>                                                     | <span data-ttu-id="5ea9b-113">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="5ea9b-113">Access type</span></span>           | <span data-ttu-id="5ea9b-114">Description</span><span class="sxs-lookup"><span data-stu-id="5ea9b-114">Description</span></span>                                                                                                                   |
|:-------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5ea9b-115">**CIMType**</span><span class="sxs-lookup"><span data-stu-id="5ea9b-115">**CIMType**</span></span>](swbemproperty-cimtype.md)<br/>          | <span data-ttu-id="5ea9b-116">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5ea9b-116">Read-only</span></span><br/>  | <span data-ttu-id="5ea9b-117">Type de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="5ea9b-117">Type of this property.</span></span><br/>                                                                                             |
| [<span data-ttu-id="5ea9b-118">**IsArray**</span><span class="sxs-lookup"><span data-stu-id="5ea9b-118">**IsArray**</span></span>](swbemproperty-isarray.md)<br/>          | <span data-ttu-id="5ea9b-119">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5ea9b-119">Read-only</span></span><br/>  | <span data-ttu-id="5ea9b-120">Valeur booléenne qui indique si cette propriété a un type de tableau.</span><span class="sxs-lookup"><span data-stu-id="5ea9b-120">Boolean value that indicates if this property has an array type.</span></span><br/>                                                   |
| [<span data-ttu-id="5ea9b-121">**IsLocal**</span><span class="sxs-lookup"><span data-stu-id="5ea9b-121">**IsLocal**</span></span>](swbemproperty-islocal.md)<br/>          | <span data-ttu-id="5ea9b-122">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5ea9b-122">Read-only</span></span><br/>  | <span data-ttu-id="5ea9b-123">Valeur booléenne qui indique si cette propriété est locale.</span><span class="sxs-lookup"><span data-stu-id="5ea9b-123">Boolean value that indicates if this property is local.</span></span><br/>                                                            |
| [<span data-ttu-id="5ea9b-124">**Nom**</span><span class="sxs-lookup"><span data-stu-id="5ea9b-124">**Name**</span></span>](swbemproperty-name.md)<br/>                | <span data-ttu-id="5ea9b-125">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5ea9b-125">Read-only</span></span><br/>  | <span data-ttu-id="5ea9b-126">Nom de cette propriété WMI.</span><span class="sxs-lookup"><span data-stu-id="5ea9b-126">Name of this WMI property.</span></span><br/>                                                                                         |
| [<span data-ttu-id="5ea9b-127">**Origine**</span><span class="sxs-lookup"><span data-stu-id="5ea9b-127">**Origin**</span></span>](swbemproperty-origin.md)<br/>            | <span data-ttu-id="5ea9b-128">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5ea9b-128">Read-only</span></span><br/>  | <span data-ttu-id="5ea9b-129">Contient la classe d’origine de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="5ea9b-129">Contains the originating class of this property.</span></span><br/>                                                                   |
| [<span data-ttu-id="5ea9b-130">**Qualificateurs\_**</span><span class="sxs-lookup"><span data-stu-id="5ea9b-130">**Qualifiers\_**</span></span>](swbemproperty-qualifiers-.md)<br/> | <span data-ttu-id="5ea9b-131">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5ea9b-131">Read-only</span></span><br/>  | <span data-ttu-id="5ea9b-132">Objet [**SWbemQualifierSet**](swbemqualifierset.md) , qui est la collection de qualificateurs pour cette propriété.</span><span class="sxs-lookup"><span data-stu-id="5ea9b-132">An [**SWbemQualifierSet**](swbemqualifierset.md) object, which is the collection of qualifiers for this property.</span></span><br/> |
| [<span data-ttu-id="5ea9b-133">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="5ea9b-133">**Value**</span></span>](swbemproperty-value.md)<br/>              | <span data-ttu-id="5ea9b-134">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5ea9b-134">Read/write</span></span><br/> | <span data-ttu-id="5ea9b-135">Valeur réelle de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="5ea9b-135">Actual value of this property.</span></span> <span data-ttu-id="5ea9b-136">Il s’agit de la propriété Automation par défaut de cet objet.</span><span class="sxs-lookup"><span data-stu-id="5ea9b-136">This is the default automation property of this object.</span></span><br/>                             |



 

## <a name="requirements"></a><span data-ttu-id="5ea9b-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5ea9b-137">Requirements</span></span>



| <span data-ttu-id="5ea9b-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5ea9b-138">Requirement</span></span> | <span data-ttu-id="5ea9b-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="5ea9b-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ea9b-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5ea9b-140">Minimum supported client</span></span><br/> | <span data-ttu-id="5ea9b-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5ea9b-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5ea9b-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5ea9b-142">Minimum supported server</span></span><br/> | <span data-ttu-id="5ea9b-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5ea9b-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5ea9b-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="5ea9b-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ea9b-145"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ea9b-145"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5ea9b-146">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="5ea9b-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="5ea9b-147"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5ea9b-147"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5ea9b-148">DLL</span><span class="sxs-lookup"><span data-stu-id="5ea9b-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ea9b-149"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ea9b-149"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="5ea9b-150">CLSID</span><span class="sxs-lookup"><span data-stu-id="5ea9b-150">CLSID</span></span><br/>                    | <span data-ttu-id="5ea9b-151">CLSID \_ SWbemProperty</span><span class="sxs-lookup"><span data-stu-id="5ea9b-151">CLSID\_SWbemProperty</span></span><br/>                                                         |
| <span data-ttu-id="5ea9b-152">IID</span><span class="sxs-lookup"><span data-stu-id="5ea9b-152">IID</span></span><br/>                      | <span data-ttu-id="5ea9b-153">IID \_ ISWbemProperty</span><span class="sxs-lookup"><span data-stu-id="5ea9b-153">IID\_ISWbemProperty</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="5ea9b-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ea9b-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ea9b-155">Scripts d’objets d’API</span><span class="sxs-lookup"><span data-stu-id="5ea9b-155">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




