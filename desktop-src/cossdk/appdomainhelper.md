---
description: Lie un objet managé à un domaine d’application, qui est un environnement isolé dans lequel les applications s’exécutent.
ms.assetid: 9357ea5d-6f86-4747-a923-16575ff13122
title: AppDomainHelper, classe (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AppDomainHelper
api_type:
- COM
ms.openlocfilehash: 6b4fbedbca631ec49dc2e416d939abdeb239e5b8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523444"
---
# <a name="appdomainhelper-class"></a><span data-ttu-id="7d682-103">AppDomainHelper, classe</span><span class="sxs-lookup"><span data-stu-id="7d682-103">AppDomainHelper class</span></span>

<span data-ttu-id="7d682-104">Lie un objet managé à un domaine d’application, qui est un environnement isolé dans lequel les applications s’exécutent.</span><span class="sxs-lookup"><span data-stu-id="7d682-104">Binds a managed object to an application domain, which is an isolated environment where applications execute.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="7d682-105">Quand implémenter</span><span class="sxs-lookup"><span data-stu-id="7d682-105">When to implement</span></span>

<span data-ttu-id="7d682-106">Cette classe est implémentée par COM+.</span><span class="sxs-lookup"><span data-stu-id="7d682-106">This class is implemented by COM+.</span></span>



| <span data-ttu-id="7d682-107">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7d682-107">Requirement</span></span> | <span data-ttu-id="7d682-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="7d682-108">Value</span></span> |
|------------|-------------------------------------------------------|
| <span data-ttu-id="7d682-109">CLSID</span><span class="sxs-lookup"><span data-stu-id="7d682-109">CLSID</span></span>      | <span data-ttu-id="7d682-110">GUID \_ AppDomainHelper</span><span class="sxs-lookup"><span data-stu-id="7d682-110">GUID\_AppDomainHelper</span></span>                                 |
| <span data-ttu-id="7d682-111">ProgID</span><span class="sxs-lookup"><span data-stu-id="7d682-111">ProgID</span></span>     | <span data-ttu-id="7d682-112">L "System. EnterpriseServices. Internal. AppDomainHelper"</span><span class="sxs-lookup"><span data-stu-id="7d682-112">L"System.EnterpriseServices.Internal.AppDomainHelper"</span></span> |
| <span data-ttu-id="7d682-113">Interfaces</span><span class="sxs-lookup"><span data-stu-id="7d682-113">Interfaces</span></span> | [<span data-ttu-id="7d682-114">**IAppDomainHelper**</span><span class="sxs-lookup"><span data-stu-id="7d682-114">**IAppDomainHelper**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iappdomainhelper)          |



 

## <a name="when-to-use"></a><span data-ttu-id="7d682-115">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="7d682-115">When to use</span></span>

<span data-ttu-id="7d682-116">Utilisez cette classe pour accéder aux méthodes de [**IAppDomainHelper**](/windows/desktop/api/ComSvcs/nn-comsvcs-iappdomainhelper).</span><span class="sxs-lookup"><span data-stu-id="7d682-116">Use this class to access the methods of [**IAppDomainHelper**](/windows/desktop/api/ComSvcs/nn-comsvcs-iappdomainhelper).</span></span>

## <a name="remarks"></a><span data-ttu-id="7d682-117">Notes</span><span class="sxs-lookup"><span data-stu-id="7d682-117">Remarks</span></span>

<span data-ttu-id="7d682-118">Pour créer cet objet, appelez [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="7d682-118">To create this object, call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

<span data-ttu-id="7d682-119">Pour utiliser cette classe à partir de Microsoft Visual Basic, ajoutez une référence à la bibliothèque de types des services COM+.</span><span class="sxs-lookup"><span data-stu-id="7d682-119">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="7d682-120">Un objet AppDomainHelper peut être déclaré à l’aide de « COMSVCSLib. AppDomainHelper » comme nom de classe.</span><span class="sxs-lookup"><span data-stu-id="7d682-120">An AppDomainHelper object can be declared using "COMSVCSLib.AppDomainHelper" as the class name.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d682-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7d682-121">Requirements</span></span>



| <span data-ttu-id="7d682-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7d682-122">Requirement</span></span> | <span data-ttu-id="7d682-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="7d682-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7d682-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7d682-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7d682-125">Windows XP avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7d682-125">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7d682-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7d682-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7d682-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7d682-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7d682-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="7d682-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d682-129"><dt>ComSvcs. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d682-129"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d682-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7d682-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d682-131">**IAppDomainHelper**</span><span class="sxs-lookup"><span data-stu-id="7d682-131">**IAppDomainHelper**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iappdomainhelper)
</dt> </dl>

 

