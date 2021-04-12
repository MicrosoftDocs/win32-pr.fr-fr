---
description: Méthode surchargée qui libère la mémoire qui contient le chemin d’accès.
audience: developer
ms.assetid: 9164d7b2-15b8-4b73-ab8c-68ed45692ea0
ms.tgt_platform: multiple
title: 'CObjectPathParser :: Free, méthodes (ObjPath. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 86494e569f68d8eff8b691c648ec5e221b28b39d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203970"
---
# <a name="cobjectpathparserfree-methods"></a><span data-ttu-id="70042-103">CObjectPathParser :: Free, méthodes</span><span class="sxs-lookup"><span data-stu-id="70042-103">CObjectPathParser::Free methods</span></span>

<span data-ttu-id="70042-104">\[La classe [**CObjectPathParser**](/windows/win32/api/objpath/nl-objpath-cobjectpathparser) fait partie de l’infrastructure de fournisseur WMI qui est maintenant considérée comme ayant un état final, et aucune amélioration du développement, des améliorations ou des mises à jour ne sera disponible pour les problèmes non liés à la sécurité qui affectent ces bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="70042-104">\[The [**CObjectPathParser**](/windows/win32/api/objpath/nl-objpath-cobjectpathparser) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="70042-105">Les [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) doivent être utilisées pour tout nouveau développement.\]</span><span class="sxs-lookup"><span data-stu-id="70042-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="70042-106">Méthode surchargée qui libère la mémoire qui contient le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="70042-106">An overloaded method that releases the memory that contains the path.</span></span>

### <a name="overload-list"></a><span data-ttu-id="70042-107">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="70042-107">Overload list</span></span>



| <span data-ttu-id="70042-108">Méthode</span><span class="sxs-lookup"><span data-stu-id="70042-108">Method</span></span>                                                                     | <span data-ttu-id="70042-109">Description</span><span class="sxs-lookup"><span data-stu-id="70042-109">Description</span></span>                                                                          |
|:---------------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| <span data-ttu-id="70042-110">[**Gratuit (LPWSTR)**](/windows/win32/api/objpath/nf-objpath-cobjectpathparser-free(lpwstr))</span><span class="sxs-lookup"><span data-stu-id="70042-110">[**Free(LPWSTR)**](/windows/win32/api/objpath/nf-objpath-cobjectpathparser-free(lpwstr))</span></span>                     | <span data-ttu-id="70042-111">Libère la mémoire qui contient le chemin d’accès non analysé.</span><span class="sxs-lookup"><span data-stu-id="70042-111">Releases the memory that contains the unparsed path.</span></span><br/>                      |
| <span data-ttu-id="70042-112">[**Gratuit (ParsedObjectPath)**](/windows/win32/api/objpath/nf-objpath-cobjectpathparser-free(parsedobjectpath))</span><span class="sxs-lookup"><span data-stu-id="70042-112">[**Free(ParsedObjectPath)**](/windows/win32/api/objpath/nf-objpath-cobjectpathparser-free(parsedobjectpath))</span></span> | <span data-ttu-id="70042-113">Libère la mémoire qui contient la structure qui a le chemin d’accès analysé.</span><span class="sxs-lookup"><span data-stu-id="70042-113">Releases the memory that contains the structure that has the parsed path.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="70042-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="70042-114">Requirements</span></span>



| <span data-ttu-id="70042-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="70042-115">Requirement</span></span> | <span data-ttu-id="70042-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="70042-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70042-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="70042-117">Minimum supported client</span></span><br/> | <span data-ttu-id="70042-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="70042-118">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="70042-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="70042-119">Minimum supported server</span></span><br/> | <span data-ttu-id="70042-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="70042-120">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="70042-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="70042-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="70042-122"><dt>ObjPath. h (inclure ObjPath. h)</dt></span><span class="sxs-lookup"><span data-stu-id="70042-122"><dt>ObjPath.h (include ObjPath.h)</dt></span></span> </dl>                                                      |
| <span data-ttu-id="70042-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="70042-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="70042-124"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="70042-124"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="70042-125">DLL</span><span class="sxs-lookup"><span data-stu-id="70042-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70042-126"><dt>FrameDynOS.dll ; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70042-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70042-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="70042-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70042-128">**CObjectPathParser**</span><span class="sxs-lookup"><span data-stu-id="70042-128">**CObjectPathParser**</span></span>](/windows/win32/api/objpath/nl-objpath-cobjectpathparser)
</dt> </dl>

<span data-ttu-id="70042-129">�</span><span class="sxs-lookup"><span data-stu-id="70042-129">�</span></span>

<span data-ttu-id="70042-130">�</span><span class="sxs-lookup"><span data-stu-id="70042-130">�</span></span>
