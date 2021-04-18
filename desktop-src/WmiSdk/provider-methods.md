---
description: La classe de fournisseur expose les méthodes suivantes.
ms.assetid: AD0BCAC7-6B5C-4BAF-9641-37D315D3E7B1
ms.tgt_platform: multiple
title: Méthodes de fournisseur
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdb4d8f5d012b5209519670562a7f735a34e6f84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536209"
---
# <a name="provider-methods"></a><span data-ttu-id="a27b6-103">Méthodes de fournisseur</span><span class="sxs-lookup"><span data-stu-id="a27b6-103">Provider Methods</span></span>

<span data-ttu-id="a27b6-104">\[La classe de [**fournisseur**](/windows/desktop/api/Provider/nl-provider-provider) fait partie de l’infrastructure de fournisseur WMI qui est maintenant considérée comme ayant un état final, et aucun développement, amélioration ou mise à jour supplémentaire n’est disponible pour les problèmes non liés à la sécurité qui affectent ces bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="a27b6-104">\[The [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="a27b6-105">Les [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) doivent être utilisées pour tout nouveau développement.\]</span><span class="sxs-lookup"><span data-stu-id="a27b6-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="a27b6-106">La classe de [**fournisseur**](/windows/desktop/api/Provider/nl-provider-provider) expose les méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="a27b6-106">The [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) class exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a27b6-107">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="a27b6-107">In this section</span></span>

-   [<span data-ttu-id="a27b6-108">**Commit, méthode**</span><span class="sxs-lookup"><span data-stu-id="a27b6-108">**Commit method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-commit)
-   [<span data-ttu-id="a27b6-109">**Méthode CreateNewInstance**</span><span class="sxs-lookup"><span data-stu-id="a27b6-109">**CreateNewInstance method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-createnewinstance)
-   <span data-ttu-id="a27b6-110">[**DeleteInstance, méthode**](/windows/desktop/api/Provider/nf-provider-provider-deleteinstance(parsedobjectpath_long_methodcontext))</span><span class="sxs-lookup"><span data-stu-id="a27b6-110">[**DeleteInstance method**](/windows/desktop/api/Provider/nf-provider-provider-deleteinstance(parsedobjectpath_long_methodcontext))</span></span>
-   [<span data-ttu-id="a27b6-111">**Méthode EnumerateInstances**</span><span class="sxs-lookup"><span data-stu-id="a27b6-111">**EnumerateInstances method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-enumerateinstances)
-   <span data-ttu-id="a27b6-112">[**ExecMethod, méthode**](/windows/desktop/api/Provider/nf-provider-provider-execmethod(parsedobjectpath_bstr_long_cinstance_cinstance_methodcontext))</span><span class="sxs-lookup"><span data-stu-id="a27b6-112">[**ExecMethod method**](/windows/desktop/api/Provider/nf-provider-provider-execmethod(parsedobjectpath_bstr_long_cinstance_cinstance_methodcontext))</span></span>
-   [<span data-ttu-id="a27b6-113">**ExecQuery, méthode**</span><span class="sxs-lookup"><span data-stu-id="a27b6-113">**ExecQuery method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-execquery)
-   [<span data-ttu-id="a27b6-114">**Flush, méthode**</span><span class="sxs-lookup"><span data-stu-id="a27b6-114">**Flush method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-flush)
-   [<span data-ttu-id="a27b6-115">**Méthode GetLocalComputerName**</span><span class="sxs-lookup"><span data-stu-id="a27b6-115">**GetLocalComputerName method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-getlocalcomputername)
-   [<span data-ttu-id="a27b6-116">**Méthode GetLocalInstancePath**</span><span class="sxs-lookup"><span data-stu-id="a27b6-116">**GetLocalInstancePath method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-getlocalinstancepath)
-   [<span data-ttu-id="a27b6-117">**GetNamespace, méthode**</span><span class="sxs-lookup"><span data-stu-id="a27b6-117">**GetNamespace method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-getnamespace)
-   <span data-ttu-id="a27b6-118">[**GetObject, méthode**](/windows/desktop/api/Provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_))</span><span class="sxs-lookup"><span data-stu-id="a27b6-118">[**GetObject method**](/windows/desktop/api/Provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_))</span></span>
-   [<span data-ttu-id="a27b6-119">**Méthode GetProviderName**</span><span class="sxs-lookup"><span data-stu-id="a27b6-119">**GetProviderName method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-getprovidername)
-   [<span data-ttu-id="a27b6-120">**Méthode MakeLocalPath**</span><span class="sxs-lookup"><span data-stu-id="a27b6-120">**MakeLocalPath method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-makelocalpath)
-   [<span data-ttu-id="a27b6-121">**Méthode du fournisseur**</span><span class="sxs-lookup"><span data-stu-id="a27b6-121">**Provider method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-provider)
-   <span data-ttu-id="a27b6-122">[**Méthode PutInstance**](/windows/desktop/api/Provider/nf-provider-provider-putinstance(constcinstance__long))</span><span class="sxs-lookup"><span data-stu-id="a27b6-122">[**PutInstance method**](/windows/desktop/api/Provider/nf-provider-provider-putinstance(constcinstance__long))</span></span>
-   [<span data-ttu-id="a27b6-123">**Méthode SetCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a27b6-123">**SetCreationClassName method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-setcreationclassname)
-   [<span data-ttu-id="a27b6-124">**Méthode ValidateDeletionFlags**</span><span class="sxs-lookup"><span data-stu-id="a27b6-124">**ValidateDeletionFlags method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-validatedeletionflags)
-   [<span data-ttu-id="a27b6-125">**Méthode ValidateEnumerationFlags**</span><span class="sxs-lookup"><span data-stu-id="a27b6-125">**ValidateEnumerationFlags method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-validateenumerationflags)
-   [<span data-ttu-id="a27b6-126">**Méthode ValidateFlags**</span><span class="sxs-lookup"><span data-stu-id="a27b6-126">**ValidateFlags method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-validateflags)
-   [<span data-ttu-id="a27b6-127">**Méthode ValidateGetObjFlags**</span><span class="sxs-lookup"><span data-stu-id="a27b6-127">**ValidateGetObjFlags method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-validategetobjflags)
-   [<span data-ttu-id="a27b6-128">**Méthode ValidateMethodFlags**</span><span class="sxs-lookup"><span data-stu-id="a27b6-128">**ValidateMethodFlags method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-validatemethodflags)
-   [<span data-ttu-id="a27b6-129">**Méthode ValidatePutInstanceFlags**</span><span class="sxs-lookup"><span data-stu-id="a27b6-129">**ValidatePutInstanceFlags method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-validateputinstanceflags)
-   [<span data-ttu-id="a27b6-130">**Méthode ValidateQueryFlags**</span><span class="sxs-lookup"><span data-stu-id="a27b6-130">**ValidateQueryFlags method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-validatequeryflags)

 

 
