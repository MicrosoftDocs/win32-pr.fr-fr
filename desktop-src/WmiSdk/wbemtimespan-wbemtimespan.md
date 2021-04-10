---
description: Le constructeur de classe WBEMTimeSpan crée un objet d’intervalle de temps. Le constructeur est surchargé.
audience: developer
ms.assetid: 337dc247-9904-457a-a1f3-e1cf29b61126
ms.tgt_platform: multiple
title: 'WBEMTimeSpan :: WbemTimeSpan, constructeurs (WbemTime. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: af5724a91ab50b5286e23b3c8095163e415d95e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210725"
---
# <a name="wbemtimespanwbemtimespan-constructors"></a><span data-ttu-id="b11ba-104">Constructeurs WBEMTimeSpan :: WbemTimeSpan</span><span class="sxs-lookup"><span data-stu-id="b11ba-104">WBEMTimeSpan::WbemTimeSpan constructors</span></span>

<span data-ttu-id="b11ba-105">\[La classe [**WBEMTimeSpan**](/windows/win32/api/wbemtime/nl-wbemtime-wbemtimespan) fait partie de l’infrastructure de fournisseur WMI qui est maintenant considérée comme ayant un état final, et aucune amélioration du développement, des améliorations ou des mises à jour ne sera disponible pour les problèmes non liés à la sécurité qui affectent ces bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="b11ba-105">\[The [**WBEMTimeSpan**](/windows/win32/api/wbemtime/nl-wbemtime-wbemtimespan) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="b11ba-106">Les [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) doivent être utilisées pour tout nouveau développement.\]</span><span class="sxs-lookup"><span data-stu-id="b11ba-106">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="b11ba-107">Le constructeur de classe **WBEMTimeSpan** crée un objet d’intervalle de temps.</span><span class="sxs-lookup"><span data-stu-id="b11ba-107">The **WBEMTimeSpan** class constructor creates a time span object.</span></span> <span data-ttu-id="b11ba-108">Le constructeur est surchargé.</span><span class="sxs-lookup"><span data-stu-id="b11ba-108">The constructor is overloaded.</span></span>

### <a name="overload-list"></a><span data-ttu-id="b11ba-109">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="b11ba-109">Overload list</span></span>



| <span data-ttu-id="b11ba-110">Constructeur</span><span class="sxs-lookup"><span data-stu-id="b11ba-110">Constructor</span></span>                                                                                                 | <span data-ttu-id="b11ba-111">Description</span><span class="sxs-lookup"><span data-stu-id="b11ba-111">Description</span></span>                                                                  |
|:------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| <span data-ttu-id="b11ba-112">[**WBEMTimeSpan()**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-wbemtimespan(constbstr))</span><span class="sxs-lookup"><span data-stu-id="b11ba-112">[**WBEMTimeSpan()**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-wbemtimespan(constbstr))</span></span>                                                      | <span data-ttu-id="b11ba-113">Crée un objet d’intervalle de temps non initialisé.</span><span class="sxs-lookup"><span data-stu-id="b11ba-113">Creates an uninitialized time span object.</span></span><br/>                        |
| <span data-ttu-id="b11ba-114">[**WBEMTimeSpan (BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-wbemtimespan(constbstr))</span><span class="sxs-lookup"><span data-stu-id="b11ba-114">[**WBEMTimeSpan(BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-wbemtimespan(constbstr))</span></span>                                               | <span data-ttu-id="b11ba-115">Initialise le nouvel objet d’intervalle de temps à la valeur dans le paramètre.</span><span class="sxs-lookup"><span data-stu-id="b11ba-115">Initializes the new time span object to value in the parameter.</span></span><br/>   |
| <span data-ttu-id="b11ba-116">[**WBEMTimeSpan (int, int, int, int, int, int, int)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-wbemtimespan(int_int_int_int_int_int_int))</span><span class="sxs-lookup"><span data-stu-id="b11ba-116">[**WBEMTimeSpan(int,int,int,int,int,int,int)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-wbemtimespan(int_int_int_int_int_int_int))</span></span> | <span data-ttu-id="b11ba-117">Initialise le nouvel objet de l’intervalle de temps aux valeurs des paramètres.</span><span class="sxs-lookup"><span data-stu-id="b11ba-117">Initializes the new time span object to values in the parameters.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="b11ba-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b11ba-118">Requirements</span></span>



| <span data-ttu-id="b11ba-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b11ba-119">Requirement</span></span> | <span data-ttu-id="b11ba-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="b11ba-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b11ba-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b11ba-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b11ba-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b11ba-122">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="b11ba-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b11ba-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b11ba-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b11ba-124">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="b11ba-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="b11ba-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b11ba-126"><dt>WbemTime. h</dt></span><span class="sxs-lookup"><span data-stu-id="b11ba-126"><dt>WbemTime.h</dt></span></span> </dl>                                                                         |
| <span data-ttu-id="b11ba-127">DLL</span><span class="sxs-lookup"><span data-stu-id="b11ba-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b11ba-128"><dt>FrameDynOS.dll ; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b11ba-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="b11ba-129">�</span><span class="sxs-lookup"><span data-stu-id="b11ba-129">�</span></span>

<span data-ttu-id="b11ba-130">�</span><span class="sxs-lookup"><span data-stu-id="b11ba-130">�</span></span>
