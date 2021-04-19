---
description: 'Opérateur de soustraction de classe WBEMTime (&\# 8211 ;) a été surchargé vers :'
audience: developer
ms.assetid: 0fa51aab-7ea2-4af7-bb12-1646388b0405
ms.tgt_platform: multiple
title: 'WBEMTime :: Operator-Operators (WbemTime. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 39256ba9d922ea9d3eef8e442115e840b963ca71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106525720"
---
# <a name="wbemtimeoperator--operators"></a><span data-ttu-id="149ea-103">WBEMTime :: Operator-, opérateurs</span><span class="sxs-lookup"><span data-stu-id="149ea-103">WBEMTime::operator- operators</span></span>

<span data-ttu-id="149ea-104">\[La classe [**WBEMTime**](wbemtime.md) fait partie de l’infrastructure de fournisseur WMI qui est maintenant considérée comme ayant un état final, et aucune amélioration du développement, des améliorations ou des mises à jour ne sera disponible pour les problèmes non liés à la sécurité qui affectent ces bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="149ea-104">\[The [**WBEMTime**](wbemtime.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="149ea-105">Les [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) doivent être utilisées pour tout nouveau développement.\]</span><span class="sxs-lookup"><span data-stu-id="149ea-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="149ea-106">L’opérateur de soustraction de classe [**WBEMTime**](wbemtime.md) () a été surchargé vers :</span><span class="sxs-lookup"><span data-stu-id="149ea-106">The [**WBEMTime**](wbemtime.md) class subtraction operator (�) has been overloaded to:</span></span>

-   <span data-ttu-id="149ea-107">Soustraire un intervalle de temps du temps d’un objet pour produire un nouvel objet d’heure qui contient le temps résultant.</span><span class="sxs-lookup"><span data-stu-id="149ea-107">Subtract a time span from an object's time to produce a new time object that contains the resulting time.</span></span>
-   <span data-ttu-id="149ea-108">Soustraire une heure de l’heure de l’objet pour produire un nouvel objet d’intervalle de temps qui contient la différence entre les deux fois.</span><span class="sxs-lookup"><span data-stu-id="149ea-108">Subtract a time from the object's time to produce a new time span object that contains the difference between the two times.</span></span>

### <a name="overload-list"></a><span data-ttu-id="149ea-109">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="149ea-109">Overload list</span></span>



| <span data-ttu-id="149ea-110">Opérateur</span><span class="sxs-lookup"><span data-stu-id="149ea-110">Operator</span></span>                                                                         | <span data-ttu-id="149ea-111">Description</span><span class="sxs-lookup"><span data-stu-id="149ea-111">Description</span></span>                                                                      |
|:---------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="149ea-112">**Operator-(WBEMTime&)**</span><span class="sxs-lookup"><span data-stu-id="149ea-112">**operator-(WBEMTime&)**</span></span>](/windows/win32/api/rrascfg/nf-rrascfg-ieapproviderconfig-initialize)         | <span data-ttu-id="149ea-113">Soustrait un **WBEMTime** d’un **WBEMTime**.</span><span class="sxs-lookup"><span data-stu-id="149ea-113">Subtracts a **WBEMTime** from a **WBEMTime**.</span></span><br/>                         |
| <span data-ttu-id="149ea-114">[**Operator-(WBEMTimeSpan&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-sub(constwbemtimespan_))</span><span class="sxs-lookup"><span data-stu-id="149ea-114">[**operator-(WBEMTimeSpan&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-sub(constwbemtimespan_))</span></span> | <span data-ttu-id="149ea-115">Soustrait un [**WBEMTimeSpan**](/windows/win32/api/wbemtime/nl-wbemtime-wbemtimespan) d’un **WBEMTime**.</span><span class="sxs-lookup"><span data-stu-id="149ea-115">Subtracts a [**WBEMTimeSpan**](/windows/win32/api/wbemtime/nl-wbemtime-wbemtimespan) from a **WBEMTime**.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="149ea-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="149ea-116">Requirements</span></span>



| <span data-ttu-id="149ea-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="149ea-117">Requirement</span></span> | <span data-ttu-id="149ea-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="149ea-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="149ea-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="149ea-119">Minimum supported client</span></span><br/> | <span data-ttu-id="149ea-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="149ea-120">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="149ea-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="149ea-121">Minimum supported server</span></span><br/> | <span data-ttu-id="149ea-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="149ea-122">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="149ea-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="149ea-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="149ea-124"><dt>WbemTime. h</dt></span><span class="sxs-lookup"><span data-stu-id="149ea-124"><dt>WbemTime.h</dt></span></span> </dl>                                                                         |
| <span data-ttu-id="149ea-125">DLL</span><span class="sxs-lookup"><span data-stu-id="149ea-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="149ea-126"><dt>FrameDynOS.dll ; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="149ea-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="149ea-127">�</span><span class="sxs-lookup"><span data-stu-id="149ea-127">�</span></span>

<span data-ttu-id="149ea-128">�</span><span class="sxs-lookup"><span data-stu-id="149ea-128">�</span></span>
