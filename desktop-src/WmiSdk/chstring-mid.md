---
description: La méthode Mid extrait une sous-chaîne de longueur nCount caractères à partir d’une chaîne CHString, en commençant à la position Npremier (de base zéro). La méthode retourne une copie de la sous-chaîne extraite.
audience: developer
ms.assetid: 2036813b-f991-4ca3-95d3-8bbe858aae09
ms.tgt_platform: multiple
title: 'CHString :: Mid, méthodes (ChString. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 5d05259128f80bcb21d00144d19002ca58ce39c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106544924"
---
# <a name="chstringmid-methods"></a><span data-ttu-id="59097-104">CHString :: Mid, méthodes</span><span class="sxs-lookup"><span data-stu-id="59097-104">CHString::Mid methods</span></span>

<span data-ttu-id="59097-105">\[La classe [**CHString**](chstring.md) fait partie de l’infrastructure de fournisseur WMI qui est maintenant considérée comme ayant un état final, et aucune amélioration du développement, des améliorations ou des mises à jour ne sera disponible pour les problèmes non liés à la sécurité qui affectent ces bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="59097-105">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="59097-106">Les [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) doivent être utilisées pour tout nouveau développement.\]</span><span class="sxs-lookup"><span data-stu-id="59097-106">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="59097-107">La méthode **Mid** extrait une sous-chaîne de longueur *nCount* caractères à partir d’une chaîne [**CHString**](chstring.md) , en commençant à la position *npremier* (de base zéro).</span><span class="sxs-lookup"><span data-stu-id="59097-107">The **Mid** method extracts a substring of length *nCount* characters from a [**CHString**](chstring.md) string, starting at position *nFirst* (zero-based).</span></span> <span data-ttu-id="59097-108">La méthode retourne une copie de la sous-chaîne extraite.</span><span class="sxs-lookup"><span data-stu-id="59097-108">The method returns a copy of the extracted substring.</span></span>

### <a name="overload-list"></a><span data-ttu-id="59097-109">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="59097-109">Overload list</span></span>



| <span data-ttu-id="59097-110">Méthode</span><span class="sxs-lookup"><span data-stu-id="59097-110">Method</span></span>                                        | <span data-ttu-id="59097-111">Description</span><span class="sxs-lookup"><span data-stu-id="59097-111">Description</span></span>                                                              |
|:----------------------------------------------|:-------------------------------------------------------------------------|
| <span data-ttu-id="59097-112">[**Mid (int, int)**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int_int))</span><span class="sxs-lookup"><span data-stu-id="59097-112">[**Mid(int,int)**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int_int))</span></span> | <span data-ttu-id="59097-113">Extrait une sous-chaîne de longueur et de point de début spécifiés.</span><span class="sxs-lookup"><span data-stu-id="59097-113">Extracts a substring of specified length and beginning point.</span></span><br/> |
| <span data-ttu-id="59097-114">[**Mid (int)**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int))</span><span class="sxs-lookup"><span data-stu-id="59097-114">[**Mid(int)**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int))</span></span>         | <span data-ttu-id="59097-115">Extrait une sous-chaîne en commençant par int.</span><span class="sxs-lookup"><span data-stu-id="59097-115">Extracts a substring beginning at int.</span></span><br/>                        |



## <a name="requirements"></a><span data-ttu-id="59097-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="59097-116">Requirements</span></span>



| <span data-ttu-id="59097-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="59097-117">Requirement</span></span> | <span data-ttu-id="59097-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="59097-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59097-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59097-119">Minimum supported client</span></span><br/> | <span data-ttu-id="59097-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="59097-120">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="59097-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59097-121">Minimum supported server</span></span><br/> | <span data-ttu-id="59097-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="59097-122">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="59097-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="59097-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="59097-124"><dt>ChString. h (inclure FwCommon. h)</dt></span><span class="sxs-lookup"><span data-stu-id="59097-124"><dt>ChString.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="59097-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="59097-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="59097-126"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="59097-126"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="59097-127">DLL</span><span class="sxs-lookup"><span data-stu-id="59097-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59097-128"><dt>FrameDynOS.dll ; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59097-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="59097-129">�</span><span class="sxs-lookup"><span data-stu-id="59097-129">�</span></span>

<span data-ttu-id="59097-130">�</span><span class="sxs-lookup"><span data-stu-id="59097-130">�</span></span>
