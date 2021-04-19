---
description: La méthode format met en forme et stocke une série de caractères et de valeurs dans une chaîne CHString.
audience: developer
ms.assetid: 95d24b0e-3580-4a5d-8dad-50d44ef1ca39
ms.tgt_platform: multiple
title: 'CHString :: format, méthodes (ChString. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 7187d2c691c6efb2054d766ae432c55be893cd05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527933"
---
# <a name="chstringformat-methods"></a><span data-ttu-id="aaf2b-103">CHString :: format, méthodes</span><span class="sxs-lookup"><span data-stu-id="aaf2b-103">CHString::Format methods</span></span>

<span data-ttu-id="aaf2b-104">\[La classe [**CHString**](chstring.md) fait partie de l’infrastructure de fournisseur WMI qui est maintenant considérée comme ayant un état final, et aucune amélioration du développement, des améliorations ou des mises à jour ne sera disponible pour les problèmes non liés à la sécurité qui affectent ces bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="aaf2b-104">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="aaf2b-105">Les [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) doivent être utilisées pour tout nouveau développement.\]</span><span class="sxs-lookup"><span data-stu-id="aaf2b-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="aaf2b-106">La méthode **format** met en forme et stocke une série de caractères et de valeurs dans une chaîne [**CHString**](chstring.md) .</span><span class="sxs-lookup"><span data-stu-id="aaf2b-106">The **Format** method formats and stores a series of characters and values in a [**CHString**](chstring.md) string.</span></span>

### <a name="overload-list"></a><span data-ttu-id="aaf2b-107">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="aaf2b-107">Overload list</span></span>



| <span data-ttu-id="aaf2b-108">Méthode</span><span class="sxs-lookup"><span data-stu-id="aaf2b-108">Method</span></span>                                              | <span data-ttu-id="aaf2b-109">Description</span><span class="sxs-lookup"><span data-stu-id="aaf2b-109">Description</span></span>                                                                                      |
|:----------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aaf2b-110">[**Format (UINT)**](/previous-versions/windows/desktop/legacy/aa385532(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="aaf2b-110">[**Format(UINT)**](/previous-versions/windows/desktop/legacy/aa385532(v=vs.85))</span></span>       | <span data-ttu-id="aaf2b-111">Met en forme ce CHString en fonction de l’identificateur de ressource spécifié par **uint**.</span><span class="sxs-lookup"><span data-stu-id="aaf2b-111">Formats this CHString according to the resource identifier specified by the **UINT**.</span></span><br/> |
| <span data-ttu-id="aaf2b-112">[**Format (LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-format(lpcwstr_---))</span><span class="sxs-lookup"><span data-stu-id="aaf2b-112">[**Format(LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-format(lpcwstr_---))</span></span> | <span data-ttu-id="aaf2b-113">Met en forme ce CHString en fonction du format spécifié par **LPCWSTR**.</span><span class="sxs-lookup"><span data-stu-id="aaf2b-113">Formats this CHString according to the format specified by the **LPCWSTR**.</span></span><br/>           |



## <a name="requirements"></a><span data-ttu-id="aaf2b-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aaf2b-114">Requirements</span></span>



| <span data-ttu-id="aaf2b-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aaf2b-115">Requirement</span></span> | <span data-ttu-id="aaf2b-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="aaf2b-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aaf2b-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aaf2b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="aaf2b-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aaf2b-118">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="aaf2b-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aaf2b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="aaf2b-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aaf2b-120">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="aaf2b-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="aaf2b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="aaf2b-122"><dt>ChString. h (inclure FwCommon. h)</dt></span><span class="sxs-lookup"><span data-stu-id="aaf2b-122"><dt>ChString.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="aaf2b-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="aaf2b-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="aaf2b-124"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aaf2b-124"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="aaf2b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="aaf2b-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aaf2b-126"><dt>FrameDynOS.dll ; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aaf2b-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="aaf2b-127">�</span><span class="sxs-lookup"><span data-stu-id="aaf2b-127">�</span></span>

<span data-ttu-id="aaf2b-128">�</span><span class="sxs-lookup"><span data-stu-id="aaf2b-128">�</span></span>
