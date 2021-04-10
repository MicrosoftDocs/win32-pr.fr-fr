---
description: Récupère des informations sur un assembly lors de l’utilisation du code managé dans le common language runtime .NET Framework.
ms.assetid: 45dcdc6a-74df-4763-ba8b-82f604db78d4
title: ClrAssemblyLocator, classe (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ClrAssemblyLocator
api_type:
- COM
ms.openlocfilehash: ff5c1d21525a950208c1b919d4dee0e2122d2e50
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860878"
---
# <a name="clrassemblylocator-class"></a><span data-ttu-id="a9e6b-103">ClrAssemblyLocator, classe</span><span class="sxs-lookup"><span data-stu-id="a9e6b-103">ClrAssemblyLocator class</span></span>

<span data-ttu-id="a9e6b-104">Récupère des informations sur un assembly lors de l’utilisation du code managé dans le common language runtime .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="a9e6b-104">Retrieves information about an assembly when using managed code in the .NET Framework common language runtime.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="a9e6b-105">Quand implémenter</span><span class="sxs-lookup"><span data-stu-id="a9e6b-105">When to implement</span></span>

<span data-ttu-id="a9e6b-106">Cette classe est implémentée par COM+.</span><span class="sxs-lookup"><span data-stu-id="a9e6b-106">This class is implemented by COM+.</span></span>



| <span data-ttu-id="a9e6b-107">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a9e6b-107">Requirement</span></span> | <span data-ttu-id="a9e6b-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="a9e6b-108">Value</span></span> |
|------------|-------------------------------------------------------|
| <span data-ttu-id="a9e6b-109">CLSID</span><span class="sxs-lookup"><span data-stu-id="a9e6b-109">CLSID</span></span>      | <span data-ttu-id="a9e6b-110">GUID \_ AssemblyLocator</span><span class="sxs-lookup"><span data-stu-id="a9e6b-110">GUID\_AssemblyLocator</span></span>                                 |
| <span data-ttu-id="a9e6b-111">ProgID</span><span class="sxs-lookup"><span data-stu-id="a9e6b-111">ProgID</span></span>     | <span data-ttu-id="a9e6b-112">L "System. EnterpriseServices. Internal. AssemblyLocator"</span><span class="sxs-lookup"><span data-stu-id="a9e6b-112">L"System.EnterpriseServices.Internal.AssemblyLocator"</span></span> |
| <span data-ttu-id="a9e6b-113">Interfaces</span><span class="sxs-lookup"><span data-stu-id="a9e6b-113">Interfaces</span></span> | [<span data-ttu-id="a9e6b-114">**IAssemblyLocator**</span><span class="sxs-lookup"><span data-stu-id="a9e6b-114">**IAssemblyLocator**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iassemblylocator)          |



 

## <a name="when-to-use"></a><span data-ttu-id="a9e6b-115">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="a9e6b-115">When to use</span></span>

<span data-ttu-id="a9e6b-116">Utilisez cette classe pour accéder aux méthodes de [**IAssemblyLocator**](/windows/desktop/api/ComSvcs/nn-comsvcs-iassemblylocator).</span><span class="sxs-lookup"><span data-stu-id="a9e6b-116">Use this class to access the methods of [**IAssemblyLocator**](/windows/desktop/api/ComSvcs/nn-comsvcs-iassemblylocator).</span></span>

## <a name="remarks"></a><span data-ttu-id="a9e6b-117">Notes</span><span class="sxs-lookup"><span data-stu-id="a9e6b-117">Remarks</span></span>

<span data-ttu-id="a9e6b-118">Pour créer cet objet, appelez [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="a9e6b-118">To create this object, call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

<span data-ttu-id="a9e6b-119">Pour utiliser cette classe à partir de Microsoft Visual Basic, ajoutez une référence à la bibliothèque de types des services COM+.</span><span class="sxs-lookup"><span data-stu-id="a9e6b-119">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="a9e6b-120">Un objet ClrAssemblyLocator peut être déclaré à l’aide de « COMSVCSLib. ClrAssemblyLocator » comme nom de classe.</span><span class="sxs-lookup"><span data-stu-id="a9e6b-120">A ClrAssemblyLocator object can be declared using "COMSVCSLib.ClrAssemblyLocator" as the class name.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9e6b-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a9e6b-121">Requirements</span></span>



| <span data-ttu-id="a9e6b-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a9e6b-122">Requirement</span></span> | <span data-ttu-id="a9e6b-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="a9e6b-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a9e6b-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9e6b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a9e6b-125">Windows XP avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a9e6b-125">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a9e6b-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9e6b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a9e6b-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a9e6b-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a9e6b-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="a9e6b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9e6b-129"><dt>ComSvcs. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9e6b-129"><dt>ComSvcs.h</dt></span></span> </dl> |



 

