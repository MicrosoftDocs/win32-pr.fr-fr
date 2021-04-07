---
description: 'La méthode CInstance :: SetCharSplat définit une propriété de type chaîne.'
ms.assetid: 7f59a2ea-3513-4a14-ac1a-62ed833d7192
ms.tgt_platform: multiple
title: 'Méthodes CInstance :: SetCharSplat (instance. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name: ''
api_type:
- DllExport
api_location:
- FrameDynOS.dll
- FrameDyn.dll
ms.openlocfilehash: e60f24023a9fc704f331d1d071e673720bfdc43e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952472"
---
# <a name="cinstancesetcharsplat-methods"></a><span data-ttu-id="80694-103">CInstance :: SetCharSplat, méthodes</span><span class="sxs-lookup"><span data-stu-id="80694-103">CInstance::SetCharSplat methods</span></span>

<span data-ttu-id="80694-104">\[La classe [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance) fait partie de l’infrastructure de fournisseur WMI qui est maintenant considérée comme ayant un état final, et aucune amélioration du développement, des améliorations ou des mises à jour ne sera disponible pour les problèmes non liés à la sécurité qui affectent ces bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="80694-104">\[The [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="80694-105">Les [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) doivent être utilisées pour tout nouveau développement.\]</span><span class="sxs-lookup"><span data-stu-id="80694-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="80694-106">La méthode **CInstance :: SetCharSplat** définit une propriété de type chaîne.</span><span class="sxs-lookup"><span data-stu-id="80694-106">The **CInstance::SetCharSplat** method sets a string property.</span></span>

### <a name="overload-list"></a><span data-ttu-id="80694-107">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="80694-107">Overload list</span></span>



| <span data-ttu-id="80694-108">Méthode</span><span class="sxs-lookup"><span data-stu-id="80694-108">Method</span></span>                                                                             | <span data-ttu-id="80694-109">Description</span><span class="sxs-lookup"><span data-stu-id="80694-109">Description</span></span>                        |
|:-----------------------------------------------------------------------------------|:-----------------------------------|
| <span data-ttu-id="80694-110">[**SetCharSplat (LPCWSTR, DWORD)**](/windows/desktop/api/Instance/nf-instance-cinstance-setcharsplat(lpcwstr_dword))</span><span class="sxs-lookup"><span data-stu-id="80694-110">[**SetCharSplat(LPCWSTR, DWORD)**](/windows/desktop/api/Instance/nf-instance-cinstance-setcharsplat(lpcwstr_dword))</span></span>     | <span data-ttu-id="80694-111">Définit une propriété de type chaîne.</span><span class="sxs-lookup"><span data-stu-id="80694-111">Sets a string property.</span></span><br/> |
| <span data-ttu-id="80694-112">[**SetCharSplat (LPCWSTR, LPCSTR)**](/windows/desktop/api/Instance/nf-instance-cinstance-setcharsplat(lpcwstr_lpcstr))</span><span class="sxs-lookup"><span data-stu-id="80694-112">[**SetCharSplat(LPCWSTR, LPCSTR)**](/windows/desktop/api/Instance/nf-instance-cinstance-setcharsplat(lpcwstr_lpcstr))</span></span>   | <span data-ttu-id="80694-113">Définit une propriété de type chaîne.</span><span class="sxs-lookup"><span data-stu-id="80694-113">Sets a string property.</span></span><br/> |
| <span data-ttu-id="80694-114">[**SetCharSplat (LPCWSTR, LPCWSTR)**](/windows/desktop/api/Instance/nf-instance-cinstance-setcharsplat(lpcwstr_lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="80694-114">[**SetCharSplat(LPCWSTR, LPCWSTR)**](/windows/desktop/api/Instance/nf-instance-cinstance-setcharsplat(lpcwstr_lpcwstr))</span></span> | <span data-ttu-id="80694-115">Définit une propriété de type chaîne.</span><span class="sxs-lookup"><span data-stu-id="80694-115">Sets a string property.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="80694-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="80694-116">Requirements</span></span>



| <span data-ttu-id="80694-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="80694-117">Requirement</span></span> | <span data-ttu-id="80694-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="80694-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80694-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80694-119">Minimum supported client</span></span><br/> | <span data-ttu-id="80694-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="80694-120">Windows Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="80694-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80694-121">Minimum supported server</span></span><br/> | <span data-ttu-id="80694-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="80694-122">Windows Server 2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="80694-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="80694-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="80694-124"><dt>Instance. h (inclure FwCommon. h)</dt></span><span class="sxs-lookup"><span data-stu-id="80694-124"><dt>Instance.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="80694-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="80694-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="80694-126"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="80694-126"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="80694-127">DLL</span><span class="sxs-lookup"><span data-stu-id="80694-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80694-128"><dt>FrameDynOS.dll ; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80694-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80694-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80694-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80694-130">**CInstance**</span><span class="sxs-lookup"><span data-stu-id="80694-130">**CInstance**</span></span>](/windows/desktop/api/Instance/nl-instance-cinstance)
</dt> </dl>

 

