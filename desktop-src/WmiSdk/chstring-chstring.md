---
description: Chacun des constructeurs suivants Initialise un nouvel objet CHString avec les données spécifiées.
audience: developer
ms.assetid: d49e1600-d5d4-4c44-81c5-1b8c53b768de
ms.tgt_platform: multiple
title: 'CHString :: CHString, constructeurs (ChString. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 711d2f28680a9f273ff808876e30e92f66336b89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203158"
---
# <a name="chstringchstring-constructors"></a><span data-ttu-id="dbb94-103">Constructeurs CHString :: CHString</span><span class="sxs-lookup"><span data-stu-id="dbb94-103">CHString::CHString constructors</span></span>

<span data-ttu-id="dbb94-104">\[La classe [**CHString**](chstring.md) fait partie de l’infrastructure de fournisseur WMI qui est maintenant considérée comme ayant un état final, et aucune amélioration du développement, des améliorations ou des mises à jour ne sera disponible pour les problèmes non liés à la sécurité qui affectent ces bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="dbb94-104">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="dbb94-105">Les [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) doivent être utilisées pour tout nouveau développement.\]</span><span class="sxs-lookup"><span data-stu-id="dbb94-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="dbb94-106">Chacun des constructeurs suivants Initialise un nouvel objet [**CHString**](chstring.md) avec les données spécifiées.</span><span class="sxs-lookup"><span data-stu-id="dbb94-106">Each of the following constructors initializes a new [**CHString**](chstring.md) object with the specified data.</span></span>

### <a name="overload-list"></a><span data-ttu-id="dbb94-107">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="dbb94-107">Overload list</span></span>



| <span data-ttu-id="dbb94-108">Constructeur</span><span class="sxs-lookup"><span data-stu-id="dbb94-108">Constructor</span></span>                                                                        | <span data-ttu-id="dbb94-109">Description</span><span class="sxs-lookup"><span data-stu-id="dbb94-109">Description</span></span>                                                  |
|:-----------------------------------------------------------------------------------|:-------------------------------------------------------------|
| [<span data-ttu-id="dbb94-110">**CHString()**</span><span class="sxs-lookup"><span data-stu-id="dbb94-110">**CHString()**</span></span>](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)                                          | <span data-ttu-id="dbb94-111">Crée un objet CHString vide.</span><span class="sxs-lookup"><span data-stu-id="dbb94-111">Creates an empty CHString object.</span></span><br/>                 |
| <span data-ttu-id="dbb94-112">[**CHString (LPCSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcstr))</span><span class="sxs-lookup"><span data-stu-id="dbb94-112">[**CHString(LPCSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcstr))</span></span>                              | <span data-ttu-id="dbb94-113">Initialise avec la valeur LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="dbb94-113">Initializes with the LPCSTR value.</span></span><br/>                |
| <span data-ttu-id="dbb94-114">[**CHString (LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="dbb94-114">[**CHString(LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcwstr))</span></span>                            | <span data-ttu-id="dbb94-115">Initialise avec la valeur LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="dbb94-115">Initializes with the LPCWSTR value.</span></span><br/>               |
| <span data-ttu-id="dbb94-116">[**CHString (WCHAR, int)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(wchar_int))</span><span class="sxs-lookup"><span data-stu-id="dbb94-116">[**CHString(WCHAR,int)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(wchar_int))</span></span>                        | <span data-ttu-id="dbb94-117">Initialise avec des copies int de la valeur WCHAR.</span><span class="sxs-lookup"><span data-stu-id="dbb94-117">Initializes with int copies of the WCHAR value.</span></span><br/>   |
| <span data-ttu-id="dbb94-118">[**CHString (LPCWSTR, int)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcwstr_int))</span><span class="sxs-lookup"><span data-stu-id="dbb94-118">[**CHString(LPCWSTR,int)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcwstr_int))</span></span>                    | <span data-ttu-id="dbb94-119">Initialise avec des copies int de la valeur LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="dbb94-119">Initializes with int copies of the LPCWSTR value.</span></span><br/> |
| <span data-ttu-id="dbb94-120">[**CHString (const CHString&)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(constchstring_))</span><span class="sxs-lookup"><span data-stu-id="dbb94-120">[**CHString(const CHString&)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(constchstring_))</span></span>            | <span data-ttu-id="dbb94-121">Réplique le paramètre CHString.</span><span class="sxs-lookup"><span data-stu-id="dbb94-121">Replicates the CHString parameter.</span></span><br/>                |
| <span data-ttu-id="dbb94-122">[**CHString (const signed char \* )**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(constunsignedchar))</span><span class="sxs-lookup"><span data-stu-id="dbb94-122">[**CHString(const unsigned char\*)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(constunsignedchar))</span></span> | <span data-ttu-id="dbb94-123">Initialise avec la valeur pointée par char \* .</span><span class="sxs-lookup"><span data-stu-id="dbb94-123">Initializes with the value pointed to by char\*.</span></span><br/>  |



## <a name="requirements"></a><span data-ttu-id="dbb94-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dbb94-124">Requirements</span></span>



| <span data-ttu-id="dbb94-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dbb94-125">Requirement</span></span> | <span data-ttu-id="dbb94-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="dbb94-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbb94-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dbb94-127">Minimum supported client</span></span><br/> | <span data-ttu-id="dbb94-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dbb94-128">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="dbb94-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dbb94-129">Minimum supported server</span></span><br/> | <span data-ttu-id="dbb94-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dbb94-130">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="dbb94-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="dbb94-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="dbb94-132"><dt>ChString. h (inclure FwCommon. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dbb94-132"><dt>ChString.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="dbb94-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="dbb94-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="dbb94-134"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dbb94-134"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="dbb94-135">DLL</span><span class="sxs-lookup"><span data-stu-id="dbb94-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dbb94-136"><dt>FrameDynOS.dll ; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dbb94-136"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="dbb94-137">�</span><span class="sxs-lookup"><span data-stu-id="dbb94-137">�</span></span>

<span data-ttu-id="dbb94-138">�</span><span class="sxs-lookup"><span data-stu-id="dbb94-138">�</span></span>
