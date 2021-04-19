---
description: La méthode InsertAt insère un élément (ou plusieurs copies d’un élément) ou tous les éléments d’un autre tableau à un index spécifié.
audience: developer
ms.assetid: 1d6355bc-7df2-4aa3-8e47-0239d726ed7d
ms.tgt_platform: multiple
title: 'CHStringArray :: InsertAt, méthodes (ChStrArr. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 4047b740778c8d0adf1f2b5981b2f3aac5ba9529
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529456"
---
# <a name="chstringarrayinsertat-methods"></a><span data-ttu-id="2eb3c-103">CHStringArray :: InsertAt, méthodes</span><span class="sxs-lookup"><span data-stu-id="2eb3c-103">CHStringArray::InsertAt methods</span></span>

<span data-ttu-id="2eb3c-104">\[La classe [**CHStringArray**](/windows/win32/api/chstrarr/nl-chstrarr-chstringarray) fait partie de l’infrastructure de fournisseur WMI qui est maintenant considérée comme ayant un état final, et aucune amélioration du développement, des améliorations ou des mises à jour ne sera disponible pour les problèmes non liés à la sécurité qui affectent ces bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="2eb3c-104">\[The [**CHStringArray**](/windows/win32/api/chstrarr/nl-chstrarr-chstringarray) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="2eb3c-105">Les [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) doivent être utilisées pour tout nouveau développement.\]</span><span class="sxs-lookup"><span data-stu-id="2eb3c-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="2eb3c-106">La méthode **InsertAt** insère un élément (ou plusieurs copies d’un élément) ou tous les éléments d’un autre tableau à un index spécifié.</span><span class="sxs-lookup"><span data-stu-id="2eb3c-106">The **InsertAt** method inserts an element (or multiple copies of an element) or all the elements of another array at a specified index.</span></span>

### <a name="overload-list"></a><span data-ttu-id="2eb3c-107">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="2eb3c-107">Overload list</span></span>



| <span data-ttu-id="2eb3c-108">Méthode</span><span class="sxs-lookup"><span data-stu-id="2eb3c-108">Method</span></span>                                                                               | <span data-ttu-id="2eb3c-109">Description</span><span class="sxs-lookup"><span data-stu-id="2eb3c-109">Description</span></span>                                                                                                             |
|:-------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2eb3c-110">[**InsertAt (int, LPCWSTR, int)**](/previous-versions/windows/desktop/legacy/aa385383(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2eb3c-110">[**InsertAt(int,LPCWSTR,int)**](/previous-versions/windows/desktop/legacy/aa385383(v=vs.85))</span></span>       | <span data-ttu-id="2eb3c-111">Insère un ou plusieurs éléments à un index spécifié dans un tableau.</span><span class="sxs-lookup"><span data-stu-id="2eb3c-111">Inserts one or more elements at a specified index in an array.</span></span><br/>                                               |
| <span data-ttu-id="2eb3c-112">[**InsertAt (int, CHStringArray \* )**](/windows/win32/api/chstrarr/nf-chstrarr-chstringarray-insertat(int_chstringarray))</span><span class="sxs-lookup"><span data-stu-id="2eb3c-112">[**InsertAt(int,CHStringArray\*)**](/windows/win32/api/chstrarr/nf-chstrarr-chstringarray-insertat(int_chstringarray))</span></span> | <span data-ttu-id="2eb3c-113">Insère tous les éléments d’un autre [**CHStringArray**](/windows/win32/api/chstrarr/nl-chstrarr-chstringarray) à un index spécifié dans un tableau.</span><span class="sxs-lookup"><span data-stu-id="2eb3c-113">Inserts all the elements of another [**CHStringArray**](/windows/win32/api/chstrarr/nl-chstrarr-chstringarray) at a specified index in an array.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="2eb3c-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2eb3c-114">Requirements</span></span>



| <span data-ttu-id="2eb3c-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2eb3c-115">Requirement</span></span> | <span data-ttu-id="2eb3c-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="2eb3c-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2eb3c-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2eb3c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2eb3c-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2eb3c-118">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="2eb3c-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2eb3c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2eb3c-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2eb3c-120">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="2eb3c-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="2eb3c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="2eb3c-122"><dt>ChStrArr. h (inclure FwCommon. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2eb3c-122"><dt>ChStrArr.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="2eb3c-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2eb3c-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="2eb3c-124"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2eb3c-124"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="2eb3c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="2eb3c-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2eb3c-126"><dt>FrameDynOS.dll ; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2eb3c-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2eb3c-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2eb3c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2eb3c-128">**CHStringArray**</span><span class="sxs-lookup"><span data-stu-id="2eb3c-128">**CHStringArray**</span></span>](/windows/win32/api/chstrarr/nl-chstrarr-chstringarray)
</dt> </dl>

<span data-ttu-id="2eb3c-129">�</span><span class="sxs-lookup"><span data-stu-id="2eb3c-129">�</span></span>

<span data-ttu-id="2eb3c-130">�</span><span class="sxs-lookup"><span data-stu-id="2eb3c-130">�</span></span>
