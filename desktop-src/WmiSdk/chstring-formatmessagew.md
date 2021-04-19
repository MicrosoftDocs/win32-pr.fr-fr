---
description: La méthode FormatMessageW surchargée met en forme une chaîne de message.
audience: developer
ms.assetid: 45780467-d3aa-4927-aa53-60e5ee277c27
ms.tgt_platform: multiple
title: 'CHString :: FormatMessageW, méthodes (ChString. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: a4f6be83c2cec8f3ae02cdbafac8a6c10ab72578
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518515"
---
# <a name="chstringformatmessagew-methods"></a><span data-ttu-id="7b82d-103">CHString :: FormatMessageW, méthodes</span><span class="sxs-lookup"><span data-stu-id="7b82d-103">CHString::FormatMessageW methods</span></span>

<span data-ttu-id="7b82d-104">\[La classe [**CHString**](chstring.md) fait partie de l’infrastructure de fournisseur WMI qui est maintenant considérée comme ayant un état final, et aucune amélioration du développement, des améliorations ou des mises à jour ne sera disponible pour les problèmes non liés à la sécurité qui affectent ces bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="7b82d-104">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="7b82d-105">Les [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) doivent être utilisées pour tout nouveau développement.\]</span><span class="sxs-lookup"><span data-stu-id="7b82d-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="7b82d-106">La méthode **FormatMessageW** surchargée met en forme une chaîne de message.</span><span class="sxs-lookup"><span data-stu-id="7b82d-106">The overloaded **FormatMessageW** method formats a message string.</span></span>

### <a name="overload-list"></a><span data-ttu-id="7b82d-107">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="7b82d-107">Overload list</span></span>



| <span data-ttu-id="7b82d-108">Méthode</span><span class="sxs-lookup"><span data-stu-id="7b82d-108">Method</span></span>                                                              | <span data-ttu-id="7b82d-109">Description</span><span class="sxs-lookup"><span data-stu-id="7b82d-109">Description</span></span>                                                                                     |
|:--------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b82d-110">[**FormatMessageW (UINT)**](/previous-versions/windows/desktop/legacy/aa385519(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7b82d-110">[**FormatMessageW(UINT)**](/previous-versions/windows/desktop/legacy/aa385519(v=vs.85))</span></span>       | <span data-ttu-id="7b82d-111">Met en forme ce message en fonction de l’identificateur de ressource spécifié par **uint**.</span><span class="sxs-lookup"><span data-stu-id="7b82d-111">Formats this message according to the resource identifier specified by the **UINT**.</span></span><br/> |
| <span data-ttu-id="7b82d-112">[**FormatMessageW (LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-formatmessagew(lpcwstr_---))</span><span class="sxs-lookup"><span data-stu-id="7b82d-112">[**FormatMessageW(LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-formatmessagew(lpcwstr_---))</span></span> | <span data-ttu-id="7b82d-113">Met en forme cette chaîne de message en fonction du format spécifié par **LPCWSTR**.</span><span class="sxs-lookup"><span data-stu-id="7b82d-113">Formats this message string according to the format specified by the **LPCWSTR**.</span></span><br/>    |



## <a name="requirements"></a><span data-ttu-id="7b82d-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7b82d-114">Requirements</span></span>



| <span data-ttu-id="7b82d-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7b82d-115">Requirement</span></span> | <span data-ttu-id="7b82d-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="7b82d-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b82d-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b82d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7b82d-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7b82d-118">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="7b82d-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b82d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7b82d-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7b82d-120">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="7b82d-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="7b82d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b82d-122"><dt>ChString. h (inclure FwCommon. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7b82d-122"><dt>ChString.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="7b82d-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7b82d-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="7b82d-124"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7b82d-124"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="7b82d-125">DLL</span><span class="sxs-lookup"><span data-stu-id="7b82d-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b82d-126"><dt>FrameDynOS.dll ; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b82d-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="7b82d-127">�</span><span class="sxs-lookup"><span data-stu-id="7b82d-127">�</span></span>

<span data-ttu-id="7b82d-128">�</span><span class="sxs-lookup"><span data-stu-id="7b82d-128">�</span></span>
