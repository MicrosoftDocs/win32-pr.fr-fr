---
description: La méthode GetLocalOffsetForDate retourne le décalage en minutes (+ ou &\# 8211 ;) entre l’heure GMT et l’heure locale pour l’heure fournie dans l’argument.
audience: developer
ms.assetid: 15cc5f45-604c-4335-bcd3-92d62dc15420
ms.tgt_platform: multiple
title: 'WBEMTime :: GetLocalOffsetForDate, méthodes (WbemTime. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: e2c10cd076e18a803f0cb22b2798c09091cc70b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866861"
---
# <a name="wbemtimegetlocaloffsetfordate-methods"></a><span data-ttu-id="d46ff-103">WBEMTime :: GetLocalOffsetForDate, méthodes</span><span class="sxs-lookup"><span data-stu-id="d46ff-103">WBEMTime::GetLocalOffsetForDate methods</span></span>

<span data-ttu-id="d46ff-104">\[La classe [**WBEMTime**](wbemtime.md) fait partie de l’infrastructure de fournisseur WMI qui est maintenant considérée comme ayant un état final, et aucune amélioration du développement, des améliorations ou des mises à jour ne sera disponible pour les problèmes non liés à la sécurité qui affectent ces bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="d46ff-104">\[The [**WBEMTime**](wbemtime.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="d46ff-105">Les [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) doivent être utilisées pour tout nouveau développement.\]</span><span class="sxs-lookup"><span data-stu-id="d46ff-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="d46ff-106">La méthode **GetLocalOffsetForDate** retourne le décalage en minutes (+ ou) entre l’heure GMT et l’heure locale pour l’heure fournie dans l’argument.</span><span class="sxs-lookup"><span data-stu-id="d46ff-106">The **GetLocalOffsetForDate** method returns the offset in minutes (+ or �) between GMT and local time for the time supplied in the argument.</span></span>

### <a name="overload-list"></a><span data-ttu-id="d46ff-107">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="d46ff-107">Overload list</span></span>



| <span data-ttu-id="d46ff-108">Méthode</span><span class="sxs-lookup"><span data-stu-id="d46ff-108">Method</span></span>                                                                                           | <span data-ttu-id="d46ff-109">Description</span><span class="sxs-lookup"><span data-stu-id="d46ff-109">Description</span></span>                                           |
|:-------------------------------------------------------------------------------------------------|:------------------------------------------------------|
| <span data-ttu-id="d46ff-110">[**GetLocalOffsetForDate (heure \_ t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(consttime_t_))</span><span class="sxs-lookup"><span data-stu-id="d46ff-110">[**GetLocalOffsetForDate(time\_t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(consttime_t_))</span></span>         | <span data-ttu-id="d46ff-111">L’argument est une référence à une **heure \_ t**.</span><span class="sxs-lookup"><span data-stu-id="d46ff-111">Argument is a reference to a **time\_t**.</span></span><br/>  |
| <span data-ttu-id="d46ff-112">[**GetLocalOffsetForDate (FILETIME \* )**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(constfiletime))</span><span class="sxs-lookup"><span data-stu-id="d46ff-112">[**GetLocalOffsetForDate(FILETIME\*)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(constfiletime))</span></span>     | <span data-ttu-id="d46ff-113">L’argument est un pointeur vers **fileTime**.</span><span class="sxs-lookup"><span data-stu-id="d46ff-113">Argument is a pointer to a **FILETIME**.</span></span><br/>   |
| [<span data-ttu-id="d46ff-114">**GetLocalOffsetForDate (struct TM \* )**</span><span class="sxs-lookup"><span data-stu-id="d46ff-114">**GetLocalOffsetForDate(struct tm\*)**</span></span>](/windows/desktop/api/wbemtime/nf-wbemtime-wbemtime-getstructtm)   | <span data-ttu-id="d46ff-115">L’argument est un pointeur vers la structure **TM** .</span><span class="sxs-lookup"><span data-stu-id="d46ff-115">Argument is a pointer to **tm** structure.</span></span><br/> |
| <span data-ttu-id="d46ff-116">[**GetLocalOffsetForDate (SYSTEMTIME \* )**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(constsystemtime))</span><span class="sxs-lookup"><span data-stu-id="d46ff-116">[**GetLocalOffsetForDate(SYSTEMTIME\*)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(constsystemtime))</span></span> | <span data-ttu-id="d46ff-117">L’argument est un pointeur vers un **SystemTime**.</span><span class="sxs-lookup"><span data-stu-id="d46ff-117">Argument is a pointer to a **SYSTEMTIME**.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="d46ff-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d46ff-118">Requirements</span></span>



| <span data-ttu-id="d46ff-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d46ff-119">Requirement</span></span> | <span data-ttu-id="d46ff-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="d46ff-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d46ff-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d46ff-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d46ff-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d46ff-122">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="d46ff-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d46ff-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d46ff-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d46ff-124">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="d46ff-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="d46ff-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d46ff-126"><dt>WbemTime. h</dt></span><span class="sxs-lookup"><span data-stu-id="d46ff-126"><dt>WbemTime.h</dt></span></span> </dl>                                                                         |
| <span data-ttu-id="d46ff-127">DLL</span><span class="sxs-lookup"><span data-stu-id="d46ff-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d46ff-128"><dt>FrameDynOS.dll ; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d46ff-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="d46ff-129">�</span><span class="sxs-lookup"><span data-stu-id="d46ff-129">�</span></span>

<span data-ttu-id="d46ff-130">�</span><span class="sxs-lookup"><span data-stu-id="d46ff-130">�</span></span>
