---
description: Fournit des fonctionnalités étendues pour SWbemObject. À l’instar de SWbemObject, les méthodes de cet objet étendu peuvent être utilisées par tous les objets WMI.
ms.assetid: 944d4cdc-ad35-4b53-b755-f10131a087fb
ms.tgt_platform: multiple
title: Objet SWbemObjectEx (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectEx
- SetFromText_
- ISWbemObjectEx
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: abed8c1d58687203aaeb32918cf15b2785b92622
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527802"
---
# <a name="swbemobjectex-object"></a><span data-ttu-id="900f3-104">Objet SWbemObjectEx</span><span class="sxs-lookup"><span data-stu-id="900f3-104">SWbemObjectEx object</span></span>

<span data-ttu-id="900f3-105">L’objet **SWbemObjectEx** fournit des fonctionnalités étendues pour [**SWbemObject**](swbemobject.md).</span><span class="sxs-lookup"><span data-stu-id="900f3-105">The **SWbemObjectEx** object provides extended functionality for [**SWbemObject**](swbemobject.md).</span></span> <span data-ttu-id="900f3-106">À l’instar de **SWbemObject**, les méthodes de cet objet étendu peuvent être utilisées par tous les objets WMI.</span><span class="sxs-lookup"><span data-stu-id="900f3-106">Like **SWbemObject**, the methods of this extended object can be used by all WMI objects.</span></span> <span data-ttu-id="900f3-107">Cet objet ne peut pas être créé par l’appel VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="900f3-107">This object cannot be created by the VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) call.</span></span>

## <a name="members"></a><span data-ttu-id="900f3-108">Membres</span><span class="sxs-lookup"><span data-stu-id="900f3-108">Members</span></span>

<span data-ttu-id="900f3-109">L’objet **SWbemObjectEx** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="900f3-109">The **SWbemObjectEx** object has these types of members:</span></span>

-   [<span data-ttu-id="900f3-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="900f3-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="900f3-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="900f3-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="900f3-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="900f3-112">Methods</span></span>

<span data-ttu-id="900f3-113">L’objet **SWbemObjectEx** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="900f3-113">The **SWbemObjectEx** object has these methods.</span></span>



| <span data-ttu-id="900f3-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="900f3-114">Method</span></span>                                      | <span data-ttu-id="900f3-115">Description</span><span class="sxs-lookup"><span data-stu-id="900f3-115">Description</span></span>                                                              |
|:--------------------------------------------|:-------------------------------------------------------------------------|
| [<span data-ttu-id="900f3-116">**GetText\_**</span><span class="sxs-lookup"><span data-stu-id="900f3-116">**GetText\_**</span></span>](swbemobjectex-gettext-.md) | <span data-ttu-id="900f3-117">Retourne un fichier texte qui affiche le contenu d’un objet en XML.</span><span class="sxs-lookup"><span data-stu-id="900f3-117">Returns a text file showing the contents of an object in XML.</span></span><br/> |
| [<span data-ttu-id="900f3-118">**Générer\_**</span><span class="sxs-lookup"><span data-stu-id="900f3-118">**Refresh\_**</span></span>](swbemobjectex-refresh-.md) | <span data-ttu-id="900f3-119">Actualise les données d’un objet.</span><span class="sxs-lookup"><span data-stu-id="900f3-119">Refreshes data in an object.</span></span><br/>                                  |
| <span data-ttu-id="900f3-120">**SetFromText\_**</span><span class="sxs-lookup"><span data-stu-id="900f3-120">**SetFromText\_**</span></span>                           | <span data-ttu-id="900f3-121">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="900f3-121">Reserved for future use.</span></span><br/>                                      |



 

### <a name="properties"></a><span data-ttu-id="900f3-122">Propriétés</span><span class="sxs-lookup"><span data-stu-id="900f3-122">Properties</span></span>

<span data-ttu-id="900f3-123">L’objet **SWbemObjectEx** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="900f3-123">The **SWbemObjectEx** object has these properties.</span></span>



| <span data-ttu-id="900f3-124">Propriété</span><span class="sxs-lookup"><span data-stu-id="900f3-124">Property</span></span>                                                                 | <span data-ttu-id="900f3-125">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="900f3-125">Access type</span></span>           | <span data-ttu-id="900f3-126">Description</span><span class="sxs-lookup"><span data-stu-id="900f3-126">Description</span></span>                                                                                                                                              |
|:-------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="900f3-127">**SystemProperties\_**</span><span class="sxs-lookup"><span data-stu-id="900f3-127">**SystemProperties\_**</span></span>](swbemobjectex-systemproperties-.md)<br/> | <span data-ttu-id="900f3-128">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="900f3-128">Read/write</span></span><br/> | <span data-ttu-id="900f3-129">Objet [**SWbemPropertySet**](swbempropertyset.md) qui contient la collection de propriétés système qui s’appliquent à **SWbemObjectEx**.</span><span class="sxs-lookup"><span data-stu-id="900f3-129">An [**SWbemPropertySet**](swbempropertyset.md) object that contains the collection of system properties that apply to the **SWbemObjectEx**.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="900f3-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="900f3-130">Requirements</span></span>



| <span data-ttu-id="900f3-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="900f3-131">Requirement</span></span> | <span data-ttu-id="900f3-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="900f3-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="900f3-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="900f3-133">Minimum supported client</span></span><br/> | <span data-ttu-id="900f3-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="900f3-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="900f3-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="900f3-135">Minimum supported server</span></span><br/> | <span data-ttu-id="900f3-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="900f3-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="900f3-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="900f3-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="900f3-138"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="900f3-138"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="900f3-139">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="900f3-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="900f3-140"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="900f3-140"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="900f3-141">DLL</span><span class="sxs-lookup"><span data-stu-id="900f3-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="900f3-142"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="900f3-142"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="900f3-143">CLSID</span><span class="sxs-lookup"><span data-stu-id="900f3-143">CLSID</span></span><br/>                    | <span data-ttu-id="900f3-144">CLSID \_ SWbemObjectEx</span><span class="sxs-lookup"><span data-stu-id="900f3-144">CLSID\_SWbemObjectEx</span></span><br/>                                                         |
| <span data-ttu-id="900f3-145">IID</span><span class="sxs-lookup"><span data-stu-id="900f3-145">IID</span></span><br/>                      | <span data-ttu-id="900f3-146">IID \_ ISWbemObjectEx</span><span class="sxs-lookup"><span data-stu-id="900f3-146">IID\_ISWbemObjectEx</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="900f3-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="900f3-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="900f3-148">Scripts d’objets d’API</span><span class="sxs-lookup"><span data-stu-id="900f3-148">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> <dt>

[<span data-ttu-id="900f3-149">**M**</span><span class="sxs-lookup"><span data-stu-id="900f3-149">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="900f3-150">WbemObjectTextFormatEnum</span><span class="sxs-lookup"><span data-stu-id="900f3-150">WbemObjectTextFormatEnum</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum)
</dt> </dl>

 

