---
description: Les opérateurs d’assignation de la classe WBEMTime sont surchargés pour faciliter les conversions entre les différents formats d’heure d’exécution de Windows et ANSI C. Les différentes signatures surchargées sont répertoriées ci-dessous.
audience: developer
ms.assetid: 47978056-d46f-4f8f-99cb-8463b44da7cf
ms.tgt_platform: multiple
title: 'WBEMTime :: Operator =, opérateurs (WbemTime. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 637cc76e776060a4c36a12a9b26bd09a6c231a08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320821"
---
# <a name="wbemtimeoperator-operators"></a><span data-ttu-id="be508-104">Opérateurs WBEMTime :: Operator =</span><span class="sxs-lookup"><span data-stu-id="be508-104">WBEMTime::operator= operators</span></span>

<span data-ttu-id="be508-105">\[La classe [**WBEMTime**](wbemtime.md) fait partie de l’infrastructure de fournisseur WMI qui est maintenant considérée comme ayant un état final, et aucune amélioration du développement, des améliorations ou des mises à jour ne sera disponible pour les problèmes non liés à la sécurité qui affectent ces bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="be508-105">\[The [**WBEMTime**](wbemtime.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="be508-106">Les [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) doivent être utilisées pour tout nouveau développement.\]</span><span class="sxs-lookup"><span data-stu-id="be508-106">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="be508-107">Les opérateurs d’assignation de la classe [**WBEMTime**](wbemtime.md) sont surchargés pour faciliter les conversions entre les différents formats d’heure d’exécution de Windows et ANSI C.</span><span class="sxs-lookup"><span data-stu-id="be508-107">The [**WBEMTime**](wbemtime.md) class assignment operators are overloaded to facilitate conversions between various Windows and ANSI C run-time time formats.</span></span> <span data-ttu-id="be508-108">Les différentes signatures surchargées sont répertoriées ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="be508-108">The various overloaded signatures are listed below.</span></span>

### <a name="overload-list"></a><span data-ttu-id="be508-109">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="be508-109">Overload list</span></span>



| <span data-ttu-id="be508-110">Opérateur</span><span class="sxs-lookup"><span data-stu-id="be508-110">Operator</span></span>                                                                     | <span data-ttu-id="be508-111">Description</span><span class="sxs-lookup"><span data-stu-id="be508-111">Description</span></span>                                                    |
|:-----------------------------------------------------------------------------|:---------------------------------------------------------------|
| <span data-ttu-id="be508-112">[**opérateur = (BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constbstr))</span><span class="sxs-lookup"><span data-stu-id="be508-112">[**operator=(BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constbstr))</span></span>               | <span data-ttu-id="be508-113">Convertit un **BSTR** au format **WBEMTime** .</span><span class="sxs-lookup"><span data-stu-id="be508-113">Converts a **BSTR** to **WBEMTime** format.</span></span><br/>         |
| <span data-ttu-id="be508-114">[**Operator = (heure \_ t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(consttime_t_))</span><span class="sxs-lookup"><span data-stu-id="be508-114">[**operator=(time\_t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(consttime_t_))</span></span>        | <span data-ttu-id="be508-115">Convertit l' **heure \_ t** au format **WBEMTime** .</span><span class="sxs-lookup"><span data-stu-id="be508-115">Converts **time\_t** to **WBEMTime** format.</span></span><br/>        |
| <span data-ttu-id="be508-116">[**Operator = (FILETIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constfiletime_))</span><span class="sxs-lookup"><span data-stu-id="be508-116">[**operator=(FILETIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constfiletime_))</span></span>     | <span data-ttu-id="be508-117">Convertit **fileTime** au format **WBEMTime** .</span><span class="sxs-lookup"><span data-stu-id="be508-117">Converts **FILETIME** to **WBEMTime** format.</span></span><br/>       |
| <span data-ttu-id="be508-118">[**Operator = (struct TM&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(consttm_))</span><span class="sxs-lookup"><span data-stu-id="be508-118">[**operator=(struct tm&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(consttm_))</span></span>   | <span data-ttu-id="be508-119">Convertit une structure **TM** au format **WBEMTime** .</span><span class="sxs-lookup"><span data-stu-id="be508-119">Converts a **tm** structure to **WBEMTime** format.</span></span><br/> |
| <span data-ttu-id="be508-120">[**Operator = (SYSTEMTIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constsystemtime_))</span><span class="sxs-lookup"><span data-stu-id="be508-120">[**operator=(SYSTEMTIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constsystemtime_))</span></span> | <span data-ttu-id="be508-121">Convertit **SystemTime** au format **WBEMTime** .</span><span class="sxs-lookup"><span data-stu-id="be508-121">Converts **SYSTEMTIME** to **WBEMTime** format.</span></span><br/>     |



## <a name="requirements"></a><span data-ttu-id="be508-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="be508-122">Requirements</span></span>



| <span data-ttu-id="be508-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="be508-123">Requirement</span></span> | <span data-ttu-id="be508-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="be508-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be508-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be508-125">Minimum supported client</span></span><br/> | <span data-ttu-id="be508-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="be508-126">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="be508-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be508-127">Minimum supported server</span></span><br/> | <span data-ttu-id="be508-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="be508-128">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="be508-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="be508-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="be508-130"><dt>WbemTime. h</dt></span><span class="sxs-lookup"><span data-stu-id="be508-130"><dt>WbemTime.h</dt></span></span> </dl>                                                                         |
| <span data-ttu-id="be508-131">DLL</span><span class="sxs-lookup"><span data-stu-id="be508-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be508-132"><dt>FrameDynOS.dll ; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be508-132"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="be508-133">�</span><span class="sxs-lookup"><span data-stu-id="be508-133">�</span></span>

<span data-ttu-id="be508-134">�</span><span class="sxs-lookup"><span data-stu-id="be508-134">�</span></span>
