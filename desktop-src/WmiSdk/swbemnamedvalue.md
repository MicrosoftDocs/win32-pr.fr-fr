---
description: L’objet SWbemNamedValue représente une valeur nommée unique qui appartient à l’objet de collection SWbemNamedValueSet. Cet objet ne peut pas être créé par l’appel VBScript CreateObject.
ms.assetid: 3f72afcd-6e10-4200-804d-918e3eb2862f
ms.tgt_platform: multiple
title: Objet SWbemNamedValue (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValue
- ISWbemNamedValue
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3668321256fea7ed8109e54f6b4df55bbd42867c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534544"
---
# <a name="swbemnamedvalue-object"></a><span data-ttu-id="0d26a-104">Objet SWbemNamedValue</span><span class="sxs-lookup"><span data-stu-id="0d26a-104">SWbemNamedValue object</span></span>

<span data-ttu-id="0d26a-105">L’objet **SWbemNamedValue** représente une valeur nommée unique qui appartient à l’objet de collection [**SWbemNamedValueSet**](swbemnamedvalueset.md) .</span><span class="sxs-lookup"><span data-stu-id="0d26a-105">The **SWbemNamedValue** object represents a single named value that belongs to the [**SWbemNamedValueSet**](swbemnamedvalueset.md) collection object.</span></span> <span data-ttu-id="0d26a-106">Cet objet ne peut pas être créé par l’appel VBScript [**CreateObject**](creating-an-object-using-vbscript.md) .</span><span class="sxs-lookup"><span data-stu-id="0d26a-106">This object cannot be created by the VBScript [**CreateObject**](creating-an-object-using-vbscript.md) call.</span></span>

## <a name="members"></a><span data-ttu-id="0d26a-107">Membres</span><span class="sxs-lookup"><span data-stu-id="0d26a-107">Members</span></span>

<span data-ttu-id="0d26a-108">L’objet **SWbemNamedValue** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0d26a-108">The **SWbemNamedValue** object has these types of members:</span></span>

-   [<span data-ttu-id="0d26a-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0d26a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0d26a-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0d26a-110">Properties</span></span>

<span data-ttu-id="0d26a-111">L’objet **SWbemNamedValue** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="0d26a-111">The **SWbemNamedValue** object has these properties.</span></span>



| <span data-ttu-id="0d26a-112">Propriété</span><span class="sxs-lookup"><span data-stu-id="0d26a-112">Property</span></span>                                          | <span data-ttu-id="0d26a-113">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="0d26a-113">Access type</span></span>           | <span data-ttu-id="0d26a-114">Description</span><span class="sxs-lookup"><span data-stu-id="0d26a-114">Description</span></span>                                                                                    |
|:--------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0d26a-115">**Nom**</span><span class="sxs-lookup"><span data-stu-id="0d26a-115">**Name**</span></span>](swbemnamedvalue-name.md)<br/>   | <span data-ttu-id="0d26a-116">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0d26a-116">Read-only</span></span><br/>  | <span data-ttu-id="0d26a-117">Nom de l’élément **SWbemNamedValue** .</span><span class="sxs-lookup"><span data-stu-id="0d26a-117">Name of the **SWbemNamedValue** item.</span></span><br/>                                               |
| [<span data-ttu-id="0d26a-118">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="0d26a-118">**Value**</span></span>](swbemnamedvalue-value.md)<br/> | <span data-ttu-id="0d26a-119">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0d26a-119">Read/write</span></span><br/> | <span data-ttu-id="0d26a-120">Valeur de l’élément **SWbemNamedValue** .</span><span class="sxs-lookup"><span data-stu-id="0d26a-120">Value of the **SWbemNamedValue** item.</span></span> <span data-ttu-id="0d26a-121">Il s’agit de la propriété par défaut de cet objet.</span><span class="sxs-lookup"><span data-stu-id="0d26a-121">This is the default property of this object.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0d26a-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0d26a-122">Requirements</span></span>



| <span data-ttu-id="0d26a-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0d26a-123">Requirement</span></span> | <span data-ttu-id="0d26a-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="0d26a-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d26a-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d26a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="0d26a-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0d26a-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0d26a-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d26a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="0d26a-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0d26a-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0d26a-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="0d26a-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d26a-130"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d26a-130"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="0d26a-131">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="0d26a-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="0d26a-132"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0d26a-132"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0d26a-133">DLL</span><span class="sxs-lookup"><span data-stu-id="0d26a-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d26a-134"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d26a-134"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="0d26a-135">CLSID</span><span class="sxs-lookup"><span data-stu-id="0d26a-135">CLSID</span></span><br/>                    | <span data-ttu-id="0d26a-136">CLSID \_ SWbemNamedValue</span><span class="sxs-lookup"><span data-stu-id="0d26a-136">CLSID\_SWbemNamedValue</span></span><br/>                                                       |
| <span data-ttu-id="0d26a-137">IID</span><span class="sxs-lookup"><span data-stu-id="0d26a-137">IID</span></span><br/>                      | <span data-ttu-id="0d26a-138">IID \_ ISWbemNamedValue</span><span class="sxs-lookup"><span data-stu-id="0d26a-138">IID\_ISWbemNamedValue</span></span><br/>                                                        |



## <a name="see-also"></a><span data-ttu-id="0d26a-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d26a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d26a-140">Scripts d’objets d’API</span><span class="sxs-lookup"><span data-stu-id="0d26a-140">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




