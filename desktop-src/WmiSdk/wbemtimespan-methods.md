---
description: La classe WBEMTimeSpan expose les méthodes suivantes.
ms.assetid: 7D450EE2-C52F-4B78-B6B1-9FD74394C3DE
ms.tgt_platform: multiple
title: Méthodes WBEMTimeSpan
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d516f22a7ecd5468d53bda44ce47edbe4504d1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534148"
---
# <a name="wbemtimespan-methods"></a><span data-ttu-id="1b682-103">Méthodes WBEMTimeSpan</span><span class="sxs-lookup"><span data-stu-id="1b682-103">WBEMTimeSpan Methods</span></span>

<span data-ttu-id="1b682-104">\[La classe [**WBEMTimeSpan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan) fait partie de l’infrastructure de fournisseur WMI qui est maintenant considérée comme ayant un état final, et aucune amélioration du développement, des améliorations ou des mises à jour ne sera disponible pour les problèmes non liés à la sécurité qui affectent ces bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="1b682-104">\[The [**WBEMTimeSpan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="1b682-105">Les [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) doivent être utilisées pour tout nouveau développement.\]</span><span class="sxs-lookup"><span data-stu-id="1b682-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="1b682-106">La classe [**WBEMTimeSpan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan) expose les méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="1b682-106">The [**WBEMTimeSpan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan) class exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1b682-107">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="1b682-107">In this section</span></span>

-   <span data-ttu-id="1b682-108">[**Constructeurs WbemTimeSpan**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtimespan-wbemtimespan(constbstr))</span><span class="sxs-lookup"><span data-stu-id="1b682-108">[**WbemTimeSpan constructors**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtimespan-wbemtimespan(constbstr))</span></span>
-   [<span data-ttu-id="1b682-109">**Clear, méthode**</span><span class="sxs-lookup"><span data-stu-id="1b682-109">**Clear method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtimespan-clear)
-   [<span data-ttu-id="1b682-110">**GetBSTR (méthode)**</span><span class="sxs-lookup"><span data-stu-id="1b682-110">**GetBSTR method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtimespan-getbstr)
-   [<span data-ttu-id="1b682-111">**GetTime, méthode**</span><span class="sxs-lookup"><span data-stu-id="1b682-111">**GetTime method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtimespan-gettime)
-   [<span data-ttu-id="1b682-112">**Méthode IsOk**</span><span class="sxs-lookup"><span data-stu-id="1b682-112">**IsOk method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtimespan-isok)
-   <span data-ttu-id="1b682-113">[**operator= (méthode)**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-assign(constfiletime_))</span><span class="sxs-lookup"><span data-stu-id="1b682-113">[**operator= method**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-assign(constfiletime_))</span></span>
-   [<span data-ttu-id="1b682-114">**Operator +, méthode**</span><span class="sxs-lookup"><span data-stu-id="1b682-114">**operator+ method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-operator-add)
-   [<span data-ttu-id="1b682-115">**Operator + =, méthode**</span><span class="sxs-lookup"><span data-stu-id="1b682-115">**operator+= method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-operator-add-assign)
-   [<span data-ttu-id="1b682-116">**Operator-Method**</span><span class="sxs-lookup"><span data-stu-id="1b682-116">**operator- method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-operator-sub)
-   [<span data-ttu-id="1b682-117">**Operator-=, méthode**</span><span class="sxs-lookup"><span data-stu-id="1b682-117">**operator-= method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-operator-sub-assign)
-   [<span data-ttu-id="1b682-118">**Operator = =, méthode**</span><span class="sxs-lookup"><span data-stu-id="1b682-118">**operator == method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-operator-equal-equal-to)
-   [<span data-ttu-id="1b682-119">**Operator ! =, méthode**</span><span class="sxs-lookup"><span data-stu-id="1b682-119">**operator != method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-operator-not-equal-to)
-   [<span data-ttu-id="1b682-120">**méthode > Operator**</span><span class="sxs-lookup"><span data-stu-id="1b682-120">**operator > method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-greater-than)
-   [<span data-ttu-id="1b682-121">**Operator >=, méthode**</span><span class="sxs-lookup"><span data-stu-id="1b682-121">**operator >= method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-greater-than-equal-to)
-   [<span data-ttu-id="1b682-122">**méthode < Operator**</span><span class="sxs-lookup"><span data-stu-id="1b682-122">**operator < method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-operator-less-than)
-   [<span data-ttu-id="1b682-123">**Operator <=, méthode**</span><span class="sxs-lookup"><span data-stu-id="1b682-123">**operator <= method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-operator-less-than-equal-to)

 

 
