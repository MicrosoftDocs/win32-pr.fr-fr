---
description: La méthode GetEmptyInstance récupère une instance non remplie unique de la classe spécifiée.
audience: developer
ms.assetid: 2873b466-3782-4d63-a777-5b25e3fb7615
ms.tgt_platform: multiple
title: 'CWbemProviderGlue :: GetEmptyInstance, méthodes (WbemGlue. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 853afbf3789969fbfca66d5f9cb40f41eadf7630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521508"
---
# <a name="cwbemprovidergluegetemptyinstance-methods"></a><span data-ttu-id="7643d-103">CWbemProviderGlue :: GetEmptyInstance, méthodes</span><span class="sxs-lookup"><span data-stu-id="7643d-103">CWbemProviderGlue::GetEmptyInstance methods</span></span>

<span data-ttu-id="7643d-104">\[La classe [**CWbemProviderGlue**](/windows/win32/api/wbemglue/nl-wbemglue-cwbemproviderglue) fait partie de l’infrastructure de fournisseur WMI qui est maintenant considérée comme ayant un état final, et aucune amélioration du développement, des améliorations ou des mises à jour ne sera disponible pour les problèmes non liés à la sécurité qui affectent ces bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="7643d-104">\[The [**CWbemProviderGlue**](/windows/win32/api/wbemglue/nl-wbemglue-cwbemproviderglue) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="7643d-105">Les [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) doivent être utilisées pour tout nouveau développement.\]</span><span class="sxs-lookup"><span data-stu-id="7643d-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="7643d-106">La méthode **GetEmptyInstance** récupère une instance non remplie unique de la classe spécifiée.</span><span class="sxs-lookup"><span data-stu-id="7643d-106">The **GetEmptyInstance** method retrieves a single unpopulated instance of the specified class.</span></span>

### <a name="overload-list"></a><span data-ttu-id="7643d-107">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="7643d-107">Overload list</span></span>



| <span data-ttu-id="7643d-108">Méthode</span><span class="sxs-lookup"><span data-stu-id="7643d-108">Method</span></span>                                                                                                                                            | <span data-ttu-id="7643d-109">Description</span><span class="sxs-lookup"><span data-stu-id="7643d-109">Description</span></span>                                                                |
|:--------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------|
| <span data-ttu-id="7643d-110">[**GetEmptyInstance (LPCWSTR, CInstance, LPCWSTR)**](/windows/win32/api/wbemglue/nf-wbemglue-cwbemproviderglue-getemptyinstance(methodcontext_lpcwstr_cinstance_lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="7643d-110">[**GetEmptyInstance(LPCWSTR,CInstance,LPCWSTR)**](/windows/win32/api/wbemglue/nf-wbemglue-cwbemproviderglue-getemptyinstance(methodcontext_lpcwstr_cinstance_lpcwstr))</span></span>                            | <span data-ttu-id="7643d-111">Récupère une instance non remplie unique de la classe spécifiée.</span><span class="sxs-lookup"><span data-stu-id="7643d-111">Retrieves a single unpopulated instance of the specified class.</span></span><br/> |
| <span data-ttu-id="7643d-112">[**GetEmptyInstance (MethodContext, LPCWSTR, CInstance, LPCWSTR)**](/windows/win32/api/wbemglue/nf-wbemglue-cwbemproviderglue-getemptyinstance(methodcontext_lpcwstr_cinstance_lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="7643d-112">[**GetEmptyInstance(MethodContext,LPCWSTR,CInstance,LPCWSTR)**](/windows/win32/api/wbemglue/nf-wbemglue-cwbemproviderglue-getemptyinstance(methodcontext_lpcwstr_cinstance_lpcwstr))</span></span> | <span data-ttu-id="7643d-113">Récupère une instance non remplie unique de la classe spécifiée.</span><span class="sxs-lookup"><span data-stu-id="7643d-113">Retrieves a single unpopulated instance of the specified class.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="7643d-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7643d-114">Requirements</span></span>



| <span data-ttu-id="7643d-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7643d-115">Requirement</span></span> | <span data-ttu-id="7643d-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="7643d-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7643d-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7643d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7643d-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7643d-118">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="7643d-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7643d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7643d-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7643d-120">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="7643d-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="7643d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7643d-122"><dt>WbemGlue. h (inclure FwCommon. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7643d-122"><dt>WbemGlue.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="7643d-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7643d-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="7643d-124"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7643d-124"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="7643d-125">DLL</span><span class="sxs-lookup"><span data-stu-id="7643d-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7643d-126"><dt>FrameDynOS.dll ; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7643d-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="7643d-127">�</span><span class="sxs-lookup"><span data-stu-id="7643d-127">�</span></span>

<span data-ttu-id="7643d-128">�</span><span class="sxs-lookup"><span data-stu-id="7643d-128">�</span></span>
