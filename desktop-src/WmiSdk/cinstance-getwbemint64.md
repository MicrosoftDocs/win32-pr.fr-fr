---
description: 'La méthode CInstance :: GetWBEMINT64 récupère une propriété de type entier 64 bits.'
ms.assetid: b51d0c51-3b72-4358-8fc3-d1dbc298b4d9
ms.tgt_platform: multiple
title: 'Méthodes CInstance :: GetWBEMINT64 (instance. h)'
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
ms.openlocfilehash: 3d7b7a9f4091125bd722aea197c1670defb0c21b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319686"
---
# <a name="cinstancegetwbemint64-methods"></a><span data-ttu-id="7a538-103">CInstance :: GetWBEMINT64, méthodes</span><span class="sxs-lookup"><span data-stu-id="7a538-103">CInstance::GetWBEMINT64 methods</span></span>

<span data-ttu-id="7a538-104">\[La classe [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance) fait partie de l’infrastructure de fournisseur WMI qui est maintenant considérée comme ayant un état final, et aucune amélioration du développement, des améliorations ou des mises à jour ne sera disponible pour les problèmes non liés à la sécurité qui affectent ces bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="7a538-104">\[The [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="7a538-105">Les [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) doivent être utilisées pour tout nouveau développement.\]</span><span class="sxs-lookup"><span data-stu-id="7a538-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="7a538-106">La méthode **CInstance :: GetWBEMINT64** récupère une propriété de type entier 64 bits.</span><span class="sxs-lookup"><span data-stu-id="7a538-106">The **CInstance::GetWBEMINT64** method retrieves a 64-bit integer property.</span></span>

### <a name="overload-list"></a><span data-ttu-id="7a538-107">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="7a538-107">Overload list</span></span>



| <span data-ttu-id="7a538-108">Méthode</span><span class="sxs-lookup"><span data-stu-id="7a538-108">Method</span></span>                                                                                   | <span data-ttu-id="7a538-109">Description</span><span class="sxs-lookup"><span data-stu-id="7a538-109">Description</span></span>                                     |
|:-----------------------------------------------------------------------------------------|:------------------------------------------------|
| <span data-ttu-id="7a538-110">[**GetWBEMINT64 (LPCWSTR, LONGLONG&)**](/windows/win32/api/instance/nf-instance-cinstance-getwbemint64(lpcwstr_longlong_))</span><span class="sxs-lookup"><span data-stu-id="7a538-110">[**GetWBEMINT64(LPCWSTR, LONGLONG&)**](/windows/win32/api/instance/nf-instance-cinstance-getwbemint64(lpcwstr_longlong_))</span></span>   | <span data-ttu-id="7a538-111">Récupère une propriété de type entier 64 bits.</span><span class="sxs-lookup"><span data-stu-id="7a538-111">Retrieves a 64-bit integer property.</span></span><br/> |
| <span data-ttu-id="7a538-112">[**GetWBEMINT64 (LPCWSTR, WBEMINT64&)**](/windows/win32/api/instance/nf-instance-cinstance-getwbemint64(lpcwstr_ulonglong_))</span><span class="sxs-lookup"><span data-stu-id="7a538-112">[**GetWBEMINT64(LPCWSTR, WBEMINT64&)**](/windows/win32/api/instance/nf-instance-cinstance-getwbemint64(lpcwstr_ulonglong_))</span></span> | <span data-ttu-id="7a538-113">Récupère une propriété de type entier 64 bits.</span><span class="sxs-lookup"><span data-stu-id="7a538-113">Retrieves a 64-bit integer property.</span></span><br/> |
| <span data-ttu-id="7a538-114">[**GetWBEMINT64 (LPCWSTR, ULONGLONG&)**](/windows/win32/api/instance/nf-instance-cinstance-getwbemint64(lpcwstr_ulonglong_))</span><span class="sxs-lookup"><span data-stu-id="7a538-114">[**GetWBEMINT64(LPCWSTR, ULONGLONG&)**](/windows/win32/api/instance/nf-instance-cinstance-getwbemint64(lpcwstr_ulonglong_))</span></span> | <span data-ttu-id="7a538-115">Récupère une propriété de type entier 64 bits.</span><span class="sxs-lookup"><span data-stu-id="7a538-115">Retrieves a 64-bit integer property.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="7a538-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7a538-116">Requirements</span></span>



| <span data-ttu-id="7a538-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7a538-117">Requirement</span></span> | <span data-ttu-id="7a538-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="7a538-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a538-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a538-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7a538-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7a538-120">Windows Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="7a538-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a538-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7a538-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7a538-122">Windows Server 2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="7a538-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="7a538-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a538-124"><dt>Instance. h (inclure FwCommon. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7a538-124"><dt>Instance.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="7a538-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7a538-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="7a538-126"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7a538-126"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="7a538-127">DLL</span><span class="sxs-lookup"><span data-stu-id="7a538-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a538-128"><dt>FrameDynOS.dll ; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a538-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a538-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7a538-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a538-130">**CInstance**</span><span class="sxs-lookup"><span data-stu-id="7a538-130">**CInstance**</span></span>](/windows/desktop/api/Instance/nl-instance-cinstance)
</dt> </dl>

 

