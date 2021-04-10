---
description: La classe CWbemProviderGlue expose les méthodes suivantes.
ms.assetid: E09290AF-1C2E-458A-811E-5357D470D3DF
ms.tgt_platform: multiple
title: Méthodes CWbemProviderGlue
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dea54ffdeaa6b74cda3b830ea65fdc17f8ffa129
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952157"
---
# <a name="cwbemproviderglue-methods"></a><span data-ttu-id="f085b-103">Méthodes CWbemProviderGlue</span><span class="sxs-lookup"><span data-stu-id="f085b-103">CWbemProviderGlue Methods</span></span>

<span data-ttu-id="f085b-104">\[La classe [**CWbemProviderGlue**](/windows/desktop/api/WbemGlue/nl-wbemglue-cwbemproviderglue) fait partie de l’infrastructure de fournisseur WMI qui est maintenant considérée comme ayant un état final, et aucune amélioration du développement, des améliorations ou des mises à jour ne sera disponible pour les problèmes non liés à la sécurité qui affectent ces bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="f085b-104">\[The [**CWbemProviderGlue**](/windows/desktop/api/WbemGlue/nl-wbemglue-cwbemproviderglue) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="f085b-105">Les [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) doivent être utilisées pour tout nouveau développement.\]</span><span class="sxs-lookup"><span data-stu-id="f085b-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="f085b-106">La classe [**CWbemProviderGlue**](/windows/desktop/api/WbemGlue/nl-wbemglue-cwbemproviderglue) expose les méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="f085b-106">The [**CWbemProviderGlue**](/windows/desktop/api/WbemGlue/nl-wbemglue-cwbemproviderglue) class exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f085b-107">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="f085b-107">In this section</span></span>

-   <span data-ttu-id="f085b-108">[**Méthode FrameworkLoginDLL**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-frameworklogindll(lpcwstr_plong))</span><span class="sxs-lookup"><span data-stu-id="f085b-108">[**FrameworkLoginDLL method**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-frameworklogindll(lpcwstr_plong))</span></span>
-   <span data-ttu-id="f085b-109">[**Méthode FrameworkLogoffDLL**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-frameworklogoffdll(lpcwstr_plong))</span><span class="sxs-lookup"><span data-stu-id="f085b-109">[**FrameworkLogoffDLL method**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-frameworklogoffdll(lpcwstr_plong))</span></span>
-   <span data-ttu-id="f085b-110">[**Méthode GetAllDerivedInstances**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getallderivedinstances(lpcwstr_trefpointercollection_cinstance__methodcontext_lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="f085b-110">[**GetAllDerivedInstances method**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getallderivedinstances(lpcwstr_trefpointercollection_cinstance__methodcontext_lpcwstr))</span></span>
-   [<span data-ttu-id="f085b-111">**Méthode GetAllDerivedInstancesAsynch**</span><span class="sxs-lookup"><span data-stu-id="f085b-111">**GetAllDerivedInstancesAsynch method**</span></span>](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getallderivedinstancesasynch)
-   [<span data-ttu-id="f085b-112">**Méthode GetAllInstances**</span><span class="sxs-lookup"><span data-stu-id="f085b-112">**GetAllInstances method**</span></span>](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getallinstances)
-   [<span data-ttu-id="f085b-113">**Méthode GetAllInstancesAsynch**</span><span class="sxs-lookup"><span data-stu-id="f085b-113">**GetAllInstancesAsynch method**</span></span>](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getallinstancesasynch)
-   <span data-ttu-id="f085b-114">[**Méthodes GetEmptyInstance**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getemptyinstance(methodcontext_lpcwstr_cinstance_lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="f085b-114">[**GetEmptyInstance methods**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getemptyinstance(methodcontext_lpcwstr_cinstance_lpcwstr))</span></span>
-   <span data-ttu-id="f085b-115">[**Méthode GetInstanceByPath**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getinstancebypath(lpcwstr_cinstance_methodcontext))</span><span class="sxs-lookup"><span data-stu-id="f085b-115">[**GetInstanceByPath method**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getinstancebypath(lpcwstr_cinstance_methodcontext))</span></span>
-   [<span data-ttu-id="f085b-116">**Méthode GetInstanceKeysByPath**</span><span class="sxs-lookup"><span data-stu-id="f085b-116">**GetInstanceKeysByPath method**</span></span>](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getinstancekeysbypath)
-   [<span data-ttu-id="f085b-117">**Méthode GetInstancePropertiesByPath**</span><span class="sxs-lookup"><span data-stu-id="f085b-117">**GetInstancePropertiesByPath method**</span></span>](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getinstancepropertiesbypath)
-   <span data-ttu-id="f085b-118">[**Méthode GetInstancesByQuery**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getinstancesbyquery(lpcwstr_trefpointercollection_cinstance__methodcontext_lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="f085b-118">[**GetInstancesByQuery method**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getinstancesbyquery(lpcwstr_trefpointercollection_cinstance__methodcontext_lpcwstr))</span></span>
-   [<span data-ttu-id="f085b-119">**Méthode GetInstancesByQueryAsynch**</span><span class="sxs-lookup"><span data-stu-id="f085b-119">**GetInstancesByQueryAsynch method**</span></span>](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getinstancesbyqueryasynch)
-   <span data-ttu-id="f085b-120">[**Méthode GetNameSpaceConnection**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getnamespaceconnection(lpcwstr_methodcontext))</span><span class="sxs-lookup"><span data-stu-id="f085b-120">[**GetNameSpaceConnection method**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getnamespaceconnection(lpcwstr_methodcontext))</span></span>
-   <span data-ttu-id="f085b-121">[**Méthode IsDerivedFrom**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-isderivedfrom(lpcwstr_lpcwstr_methodcontext_lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="f085b-121">[**IsDerivedFrom method**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-isderivedfrom(lpcwstr_lpcwstr_methodcontext_lpcwstr))</span></span>
-   [<span data-ttu-id="f085b-122">**Méthode SetStatusObject**</span><span class="sxs-lookup"><span data-stu-id="f085b-122">**SetStatusObject method**</span></span>](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-setstatusobject)

 

 
