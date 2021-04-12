---
description: Vous pouvez utiliser les propriétés de l’objet SWbemQualifier pour représenter un qualificateur unique d’une classe, d’une instance, d’une propriété ou d’un paramètre de méthode WMI. Cet objet ne peut pas être créé par l’appel VBScript CreateObject.
ms.assetid: b5dbe98a-e1d8-4679-a563-c88760d08b79
ms.tgt_platform: multiple
title: Objet SWbemQualifier (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifier
- ISWbemQualifier
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5e9a49832ffa1e38fbe6ee0f71e1f6a39c1b0ba2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202150"
---
# <a name="swbemqualifier-object"></a><span data-ttu-id="a5300-104">Objet SWbemQualifier</span><span class="sxs-lookup"><span data-stu-id="a5300-104">SWbemQualifier object</span></span>

<span data-ttu-id="a5300-105">Vous pouvez utiliser les propriétés de l’objet **SWbemQualifier** pour représenter un qualificateur unique d’une classe, d’une instance, d’une propriété ou d’un paramètre de méthode WMI.</span><span class="sxs-lookup"><span data-stu-id="a5300-105">You can use the properties of the **SWbemQualifier** object to represent a single qualifier of a WMI class, instance, property, or method parameter.</span></span> <span data-ttu-id="a5300-106">Cet objet ne peut pas être créé par l’appel VBScript [CreateObject](creating-an-object-using-vbscript.md) .</span><span class="sxs-lookup"><span data-stu-id="a5300-106">This object cannot be created by the VBScript [CreateObject](creating-an-object-using-vbscript.md) call.</span></span>

## <a name="members"></a><span data-ttu-id="a5300-107">Membres</span><span class="sxs-lookup"><span data-stu-id="a5300-107">Members</span></span>

<span data-ttu-id="a5300-108">L’objet **SWbemQualifier** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a5300-108">The **SWbemQualifier** object has these types of members:</span></span>

-   [<span data-ttu-id="a5300-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a5300-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a5300-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a5300-110">Properties</span></span>

<span data-ttu-id="a5300-111">L’objet **SWbemQualifier** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="a5300-111">The **SWbemQualifier** object has these properties.</span></span>



| <span data-ttu-id="a5300-112">Propriété</span><span class="sxs-lookup"><span data-stu-id="a5300-112">Property</span></span>                                                                       | <span data-ttu-id="a5300-113">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="a5300-113">Access type</span></span>           | <span data-ttu-id="a5300-114">Description</span><span class="sxs-lookup"><span data-stu-id="a5300-114">Description</span></span>                                                                                           |
|:-------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a5300-115">**IsAmended**</span><span class="sxs-lookup"><span data-stu-id="a5300-115">**IsAmended**</span></span>](swbemqualifier-isamended.md)<br/>                       | <span data-ttu-id="a5300-116">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a5300-116">Read-only</span></span><br/>  | <span data-ttu-id="a5300-117">Valeur booléenne qui indique si ce qualificateur a été localisé à l’aide d’une opération de fusion.</span><span class="sxs-lookup"><span data-stu-id="a5300-117">Boolean value that indicates if this qualifier has been localized using a merge operation.</span></span><br/> |
| [<span data-ttu-id="a5300-118">**IsLocal**</span><span class="sxs-lookup"><span data-stu-id="a5300-118">**IsLocal**</span></span>](swbemqualifier-islocal.md)<br/>                           | <span data-ttu-id="a5300-119">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a5300-119">Read-only</span></span><br/>  | <span data-ttu-id="a5300-120">Valeur booléenne qui indique si ce qualificateur est local.</span><span class="sxs-lookup"><span data-stu-id="a5300-120">Boolean value that indicates if this qualifier is local.</span></span><br/>                                   |
| [<span data-ttu-id="a5300-121">**IsOverridable**</span><span class="sxs-lookup"><span data-stu-id="a5300-121">**IsOverridable**</span></span>](swbemqualifier-isoverridable.md)<br/>               | <span data-ttu-id="a5300-122">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a5300-122">Read/write</span></span><br/> | <span data-ttu-id="a5300-123">Valeur booléenne qui indique si ce qualificateur peut être substitué lorsqu’il est propagé.</span><span class="sxs-lookup"><span data-stu-id="a5300-123">Boolean value that indicates if this qualifier can be overridden when propagated.</span></span><br/>          |
| [<span data-ttu-id="a5300-124">**Nom**</span><span class="sxs-lookup"><span data-stu-id="a5300-124">**Name**</span></span>](swbemqualifier-name.md)<br/>                                 | <span data-ttu-id="a5300-125">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a5300-125">Read-only</span></span><br/>  | <span data-ttu-id="a5300-126">Nom de ce qualificateur.</span><span class="sxs-lookup"><span data-stu-id="a5300-126">Name of this qualifier.</span></span><br/>                                                                    |
| [<span data-ttu-id="a5300-127">**PropagatesToInstance**</span><span class="sxs-lookup"><span data-stu-id="a5300-127">**PropagatesToInstance**</span></span>](swbemqualifier-propagatestoinstance.md)<br/> | <span data-ttu-id="a5300-128">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a5300-128">Read/write</span></span><br/> | <span data-ttu-id="a5300-129">Valeur booléenne qui indique si ce qualificateur peut être propagé à une instance.</span><span class="sxs-lookup"><span data-stu-id="a5300-129">Boolean value that indicates if this qualifier can be propagated to an instance.</span></span><br/>           |
| [<span data-ttu-id="a5300-130">**PropagatesToSubClass**</span><span class="sxs-lookup"><span data-stu-id="a5300-130">**PropagatesToSubClass**</span></span>](swbemqualifier-propagatestosubclass.md)<br/> | <span data-ttu-id="a5300-131">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a5300-131">Read-only</span></span><br/>  | <span data-ttu-id="a5300-132">Valeur booléenne qui indique si ce qualificateur peut être propagé à une sous-classe.</span><span class="sxs-lookup"><span data-stu-id="a5300-132">Boolean value that indicates if this qualifier can be propagated to a subclass.</span></span><br/>            |
| [<span data-ttu-id="a5300-133">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="a5300-133">**Value**</span></span>](swbemqualifier-value.md)<br/>                               | <span data-ttu-id="a5300-134">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a5300-134">Read/write</span></span><br/> | <span data-ttu-id="a5300-135">Valeur de type variant de ce qualificateur.</span><span class="sxs-lookup"><span data-stu-id="a5300-135">Variant value of this qualifier.</span></span> <span data-ttu-id="a5300-136">Il s’agit de la propriété par défaut de cet objet.</span><span class="sxs-lookup"><span data-stu-id="a5300-136">This is the default property of this object.</span></span><br/>              |



 

## <a name="requirements"></a><span data-ttu-id="a5300-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a5300-137">Requirements</span></span>



| <span data-ttu-id="a5300-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a5300-138">Requirement</span></span> | <span data-ttu-id="a5300-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="a5300-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a5300-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5300-140">Minimum supported client</span></span><br/> | <span data-ttu-id="a5300-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a5300-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a5300-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5300-142">Minimum supported server</span></span><br/> | <span data-ttu-id="a5300-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a5300-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a5300-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="a5300-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5300-145"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5300-145"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a5300-146">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="a5300-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="a5300-147"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a5300-147"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a5300-148">DLL</span><span class="sxs-lookup"><span data-stu-id="a5300-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5300-149"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5300-149"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a5300-150">CLSID</span><span class="sxs-lookup"><span data-stu-id="a5300-150">CLSID</span></span><br/>                    | <span data-ttu-id="a5300-151">CLSID \_ SWbemQualifier</span><span class="sxs-lookup"><span data-stu-id="a5300-151">CLSID\_SWbemQualifier</span></span><br/>                                                        |
| <span data-ttu-id="a5300-152">IID</span><span class="sxs-lookup"><span data-stu-id="a5300-152">IID</span></span><br/>                      | <span data-ttu-id="a5300-153">IID \_ ISWbemQualifier</span><span class="sxs-lookup"><span data-stu-id="a5300-153">IID\_ISWbemQualifier</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="a5300-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5300-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5300-155">Scripts d’objets d’API</span><span class="sxs-lookup"><span data-stu-id="a5300-155">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




