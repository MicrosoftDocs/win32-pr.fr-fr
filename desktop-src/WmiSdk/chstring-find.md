---
description: La méthode Find recherche dans une chaîne la première correspondance d’une sous-chaîne.
audience: developer
ms.assetid: 98a7c5ad-5bc7-4918-b978-45d2b439f250
ms.tgt_platform: multiple
title: 'CHString :: Find, méthodes (ChString. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 5996ca5c06e2101fad834ce2e37df31ee435fbb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538383"
---
# <a name="chstringfind-methods"></a><span data-ttu-id="66215-103">CHString :: Find, méthodes</span><span class="sxs-lookup"><span data-stu-id="66215-103">CHString::Find methods</span></span>

<span data-ttu-id="66215-104">\[La classe [**CHString**](chstring.md) fait partie de l’infrastructure de fournisseur WMI qui est maintenant considérée comme ayant un état final, et aucune amélioration du développement, des améliorations ou des mises à jour ne sera disponible pour les problèmes non liés à la sécurité qui affectent ces bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="66215-104">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="66215-105">Les [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) doivent être utilisées pour tout nouveau développement.\]</span><span class="sxs-lookup"><span data-stu-id="66215-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="66215-106">La méthode **Find** recherche dans une chaîne la première correspondance d’une sous-chaîne.</span><span class="sxs-lookup"><span data-stu-id="66215-106">The **Find** method searches a string for the first match of a substring.</span></span>

### <a name="overload-list"></a><span data-ttu-id="66215-107">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="66215-107">Overload list</span></span>



| <span data-ttu-id="66215-108">Méthode</span><span class="sxs-lookup"><span data-stu-id="66215-108">Method</span></span>                                          | <span data-ttu-id="66215-109">Description</span><span class="sxs-lookup"><span data-stu-id="66215-109">Description</span></span>                                             |
|:------------------------------------------------|:--------------------------------------------------------|
| <span data-ttu-id="66215-110">[**Rechercher (WCHAR)**](/windows/win32/api/chstring/nf-chstring-chstring-find(lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="66215-110">[**Find(WCHAR)**](/windows/win32/api/chstring/nf-chstring-chstring-find(lpcwstr))</span></span>     | <span data-ttu-id="66215-111">Recherche les **WSTR** dans cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="66215-111">Searches for the **WSTR** in this string.</span></span><br/>    |
| <span data-ttu-id="66215-112">[**Rechercher (LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-find(lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="66215-112">[**Find(LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-find(lpcwstr))</span></span> | <span data-ttu-id="66215-113">Recherche les **LPCWSTR** dans cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="66215-113">Searches for the **LPCWSTR** in this string.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="66215-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="66215-114">Requirements</span></span>



| <span data-ttu-id="66215-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="66215-115">Requirement</span></span> | <span data-ttu-id="66215-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="66215-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66215-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66215-117">Minimum supported client</span></span><br/> | <span data-ttu-id="66215-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="66215-118">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="66215-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66215-119">Minimum supported server</span></span><br/> | <span data-ttu-id="66215-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="66215-120">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="66215-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="66215-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="66215-122"><dt>ChString. h (inclure FwCommon. h)</dt></span><span class="sxs-lookup"><span data-stu-id="66215-122"><dt>ChString.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="66215-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="66215-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="66215-124"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="66215-124"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="66215-125">DLL</span><span class="sxs-lookup"><span data-stu-id="66215-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66215-126"><dt>FrameDynOS.dll ; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66215-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="66215-127">�</span><span class="sxs-lookup"><span data-stu-id="66215-127">�</span></span>

<span data-ttu-id="66215-128">�</span><span class="sxs-lookup"><span data-stu-id="66215-128">�</span></span>
