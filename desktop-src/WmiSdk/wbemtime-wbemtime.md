---
description: Le constructeur de classe WBEMTime facilite les conversions entre les différents formats d’heure d’exécution de Windows et ANSI C.
audience: developer
ms.assetid: 8b0ce221-2186-4aed-a474-00f88cef6350
ms.tgt_platform: multiple
title: 'WBEMTime :: WBEMTime, constructeurs (WbemTime. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 778b9af2e732b3d294b0348ff2d2b91b60518d45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526962"
---
# <a name="wbemtimewbemtime-constructors"></a><span data-ttu-id="980c5-103">Constructeurs WBEMTime :: WBEMTime</span><span class="sxs-lookup"><span data-stu-id="980c5-103">WBEMTime::WBEMTime constructors</span></span>

<span data-ttu-id="980c5-104">\[La classe [**WBEMTime**](wbemtime.md) fait partie de l’infrastructure de fournisseur WMI qui est maintenant considérée comme ayant un état final, et aucune amélioration du développement, des améliorations ou des mises à jour ne sera disponible pour les problèmes non liés à la sécurité qui affectent ces bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="980c5-104">\[The [**WBEMTime**](wbemtime.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="980c5-105">Les [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) doivent être utilisées pour tout nouveau développement.\]</span><span class="sxs-lookup"><span data-stu-id="980c5-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="980c5-106">Le constructeur de classe **WBEMTime** facilite les conversions entre les différents formats d’heure d’exécution de Windows et ANSI C.</span><span class="sxs-lookup"><span data-stu-id="980c5-106">The **WBEMTime** class constructor facilitates conversions between various Windows and ANSI C run-time time formats.</span></span>

### <a name="overload-list"></a><span data-ttu-id="980c5-107">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="980c5-107">Overload list</span></span>



| <span data-ttu-id="980c5-108">Constructeur</span><span class="sxs-lookup"><span data-stu-id="980c5-108">Constructor</span></span>                                                                 | <span data-ttu-id="980c5-109">Description</span><span class="sxs-lookup"><span data-stu-id="980c5-109">Description</span></span>                                                               |
|:----------------------------------------------------------------------------|:--------------------------------------------------------------------------|
| <span data-ttu-id="980c5-110">[**WBEMTime()**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constbstr))</span><span class="sxs-lookup"><span data-stu-id="980c5-110">[**WBEMTime()**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constbstr))</span></span>                                   | <span data-ttu-id="980c5-111">Crée un objet de temps non initialisé.</span><span class="sxs-lookup"><span data-stu-id="980c5-111">Creates an uninitialized time object.</span></span><br/>                          |
| <span data-ttu-id="980c5-112">[**WBEMTime (BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constbstr))</span><span class="sxs-lookup"><span data-stu-id="980c5-112">[**WBEMTime(BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constbstr))</span></span>                           | <span data-ttu-id="980c5-113">Initialise le nouvel objet d’heure à la valeur du paramètre.</span><span class="sxs-lookup"><span data-stu-id="980c5-113">Initializes the new time object to the value in the parameter.</span></span><br/> |
| <span data-ttu-id="980c5-114">[**WBEMTime (const Time \_ t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(consttime_t_))</span><span class="sxs-lookup"><span data-stu-id="980c5-114">[**WBEMTime(const time\_t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(consttime_t_))</span></span>        | <span data-ttu-id="980c5-115">Initialise le nouvel objet d’heure à la valeur du paramètre.</span><span class="sxs-lookup"><span data-stu-id="980c5-115">Initializes the new time object to the value in the parameter.</span></span><br/> |
| <span data-ttu-id="980c5-116">[**WBEMTime (const struct TM)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(consttm_))</span><span class="sxs-lookup"><span data-stu-id="980c5-116">[**WBEMTime(const struct tm)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(consttm_))</span></span>    | <span data-ttu-id="980c5-117">Initialise le nouvel objet d’heure à la valeur du paramètre.</span><span class="sxs-lookup"><span data-stu-id="980c5-117">Initializes the new time object to the value in the parameter.</span></span><br/> |
| <span data-ttu-id="980c5-118">[**WBEMTime (const FILETIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constfiletime_))</span><span class="sxs-lookup"><span data-stu-id="980c5-118">[**WBEMTime(const FILETIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constfiletime_))</span></span>     | <span data-ttu-id="980c5-119">Initialise le nouvel objet d’heure à la valeur du paramètre.</span><span class="sxs-lookup"><span data-stu-id="980c5-119">Initializes the new time object to the value in the parameter.</span></span><br/> |
| <span data-ttu-id="980c5-120">[**WBEMTime (const SYSTEMTIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constsystemtime_))</span><span class="sxs-lookup"><span data-stu-id="980c5-120">[**WBEMTime(const SYSTEMTIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constsystemtime_))</span></span> | <span data-ttu-id="980c5-121">Initialise le nouvel objet d’heure à la valeur du paramètre.</span><span class="sxs-lookup"><span data-stu-id="980c5-121">Initializes the new time object to the value in the parameter.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="980c5-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="980c5-122">Requirements</span></span>



| <span data-ttu-id="980c5-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="980c5-123">Requirement</span></span> | <span data-ttu-id="980c5-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="980c5-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="980c5-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="980c5-125">Minimum supported client</span></span><br/> | <span data-ttu-id="980c5-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="980c5-126">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="980c5-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="980c5-127">Minimum supported server</span></span><br/> | <span data-ttu-id="980c5-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="980c5-128">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="980c5-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="980c5-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="980c5-130"><dt>WbemTime. h</dt></span><span class="sxs-lookup"><span data-stu-id="980c5-130"><dt>WbemTime.h</dt></span></span> </dl>                                                                         |
| <span data-ttu-id="980c5-131">DLL</span><span class="sxs-lookup"><span data-stu-id="980c5-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="980c5-132"><dt>FrameDynOS.dll ; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="980c5-132"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="980c5-133">�</span><span class="sxs-lookup"><span data-stu-id="980c5-133">�</span></span>

<span data-ttu-id="980c5-134">�</span><span class="sxs-lookup"><span data-stu-id="980c5-134">�</span></span>
