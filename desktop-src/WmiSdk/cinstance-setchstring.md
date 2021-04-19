---
description: 'La méthode CInstance :: SetCHString définit une propriété de type chaîne.'
ms.assetid: a75b574d-9ee7-4930-a003-5d71c5f1d687
ms.tgt_platform: multiple
title: 'Méthodes CInstance :: SetCHString (instance. h)'
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
ms.openlocfilehash: 187c07b5cf0f867ee838f2f3725d6a82319d4634
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520643"
---
# <a name="cinstancesetchstring-methods"></a><span data-ttu-id="ded76-103">CInstance :: SetCHString, méthodes</span><span class="sxs-lookup"><span data-stu-id="ded76-103">CInstance::SetCHString methods</span></span>

<span data-ttu-id="ded76-104">\[La classe [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance) fait partie de l’infrastructure de fournisseur WMI qui est maintenant considérée comme ayant un état final, et aucune amélioration du développement, des améliorations ou des mises à jour ne sera disponible pour les problèmes non liés à la sécurité qui affectent ces bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="ded76-104">\[The [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="ded76-105">Les [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) doivent être utilisées pour tout nouveau développement.\]</span><span class="sxs-lookup"><span data-stu-id="ded76-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="ded76-106">La méthode **CInstance :: SetCHString** définit une propriété de type chaîne.</span><span class="sxs-lookup"><span data-stu-id="ded76-106">The **CInstance::SetCHString** method sets a string property.</span></span>

### <a name="overload-list"></a><span data-ttu-id="ded76-107">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="ded76-107">Overload list</span></span>



| <span data-ttu-id="ded76-108">Méthode</span><span class="sxs-lookup"><span data-stu-id="ded76-108">Method</span></span>                                                                                           | <span data-ttu-id="ded76-109">Description</span><span class="sxs-lookup"><span data-stu-id="ded76-109">Description</span></span>                        |
|:-------------------------------------------------------------------------------------------------|:-----------------------------------|
| <span data-ttu-id="ded76-110">[**SetCHString (LPCWSTR, LPCSTR)**](/windows/desktop/api/Instance/nf-instance-cinstance-setchstring(lpcwstr_lpcstr))</span><span class="sxs-lookup"><span data-stu-id="ded76-110">[**SetCHString(LPCWSTR, LPCSTR)**](/windows/desktop/api/Instance/nf-instance-cinstance-setchstring(lpcwstr_lpcstr))</span></span>                   | <span data-ttu-id="ded76-111">Définit une propriété de type chaîne.</span><span class="sxs-lookup"><span data-stu-id="ded76-111">Sets a string property.</span></span><br/> |
| <span data-ttu-id="ded76-112">[**SetCHString (LPCWSTR, const CHString&)**](/windows/win32/api/instance/nf-instance-cinstance-setchstring(lpcwstr_constchstring_))</span><span class="sxs-lookup"><span data-stu-id="ded76-112">[**SetCHString(LPCWSTR, const CHString&)**](/windows/win32/api/instance/nf-instance-cinstance-setchstring(lpcwstr_constchstring_))</span></span> | <span data-ttu-id="ded76-113">Définit une propriété de type chaîne.</span><span class="sxs-lookup"><span data-stu-id="ded76-113">Sets a string property.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="ded76-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ded76-114">Requirements</span></span>



| <span data-ttu-id="ded76-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ded76-115">Requirement</span></span> | <span data-ttu-id="ded76-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="ded76-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ded76-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ded76-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ded76-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ded76-118">Windows Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="ded76-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ded76-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ded76-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ded76-120">Windows Server 2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="ded76-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="ded76-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ded76-122"><dt>Instance. h (inclure FwCommon. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ded76-122"><dt>Instance.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="ded76-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ded76-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="ded76-124"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ded76-124"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="ded76-125">DLL</span><span class="sxs-lookup"><span data-stu-id="ded76-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ded76-126"><dt>FrameDynOS.dll ; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ded76-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ded76-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ded76-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ded76-128">**CInstance**</span><span class="sxs-lookup"><span data-stu-id="ded76-128">**CInstance**</span></span>](/windows/desktop/api/Instance/nl-instance-cinstance)
</dt> </dl>

 

