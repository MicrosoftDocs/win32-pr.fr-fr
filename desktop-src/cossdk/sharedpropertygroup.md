---
description: Crée les propriétés partagées et y accède dans un groupe de propriétés partagées.
ms.assetid: 20fd32f0-b2b2-4bed-8c59-1d1fdc8a399e
title: SharedPropertyGroup, classe (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SharedPropertyGroup
api_type:
- COM
ms.openlocfilehash: a3fff14043d67b96db99334c7bec1afee2577f7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748172"
---
# <a name="sharedpropertygroup-class"></a><span data-ttu-id="aa305-103">SharedPropertyGroup, classe</span><span class="sxs-lookup"><span data-stu-id="aa305-103">SharedPropertyGroup class</span></span>

<span data-ttu-id="aa305-104">Crée les propriétés partagées et y accède dans un groupe de propriétés partagées.</span><span class="sxs-lookup"><span data-stu-id="aa305-104">Creates and accesses the shared properties in a shared property group.</span></span>

<span data-ttu-id="aa305-105">Pour plus d’informations sur l’utilisation de l’Gestionnaire de propriétés partagé dans COM+, consultez [Gestionnaire de propriétés partagées com+](com--shared-property-manager.md).</span><span class="sxs-lookup"><span data-stu-id="aa305-105">For more information about using the Shared Property Manager in COM+, see [COM+ Shared Property Manager](com--shared-property-manager.md).</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="aa305-106">Quand implémenter</span><span class="sxs-lookup"><span data-stu-id="aa305-106">When to implement</span></span>

<span data-ttu-id="aa305-107">Cette classe est implémentée par COM+.</span><span class="sxs-lookup"><span data-stu-id="aa305-107">This class is implemented by COM+.</span></span>



| <span data-ttu-id="aa305-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aa305-108">Requirement</span></span> | <span data-ttu-id="aa305-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="aa305-109">Value</span></span> |
|------------|------------------------------------------------------|
| <span data-ttu-id="aa305-110">Interfaces</span><span class="sxs-lookup"><span data-stu-id="aa305-110">Interfaces</span></span> | [<span data-ttu-id="aa305-111">**ISharedPropertyGroup**</span><span class="sxs-lookup"><span data-stu-id="aa305-111">**ISharedPropertyGroup**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup) |



 

## <a name="when-to-use"></a><span data-ttu-id="aa305-112">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="aa305-112">When to use</span></span>

<span data-ttu-id="aa305-113">Utilisez cette classe pour accéder aux méthodes de [**ISharedPropertyGroup**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup).</span><span class="sxs-lookup"><span data-stu-id="aa305-113">Use this class to access the methods of [**ISharedPropertyGroup**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup).</span></span>

## <a name="remarks"></a><span data-ttu-id="aa305-114">Notes</span><span class="sxs-lookup"><span data-stu-id="aa305-114">Remarks</span></span>

<span data-ttu-id="aa305-115">Vous pouvez créer un objet **SharedPropertyGroup** à l’aide de la méthode [**CreatePropertyGroup**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroupmanager-createpropertygroup) de [**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager).</span><span class="sxs-lookup"><span data-stu-id="aa305-115">You can create a **SharedPropertyGroup** object using the [**CreatePropertyGroup**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroupmanager-createpropertygroup) method of [**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager).</span></span>

<span data-ttu-id="aa305-116">Pour utiliser cette classe à partir de Microsoft Visual Basic, ajoutez une référence à la bibliothèque de types des services COM+.</span><span class="sxs-lookup"><span data-stu-id="aa305-116">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="aa305-117">Un objet SharedPropertyGroup est créé en appelant la méthode [**CreatePropertyGroup**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroupmanager-createpropertygroup) de l’objet [**SharedPropertyGroupManager**](sharedpropertygroupmanager.md) .</span><span class="sxs-lookup"><span data-stu-id="aa305-117">A SharedPropertyGroup object is created by calling the [**CreatePropertyGroup**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroupmanager-createpropertygroup) method of the [**SharedPropertyGroupManager**](sharedpropertygroupmanager.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa305-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aa305-118">Requirements</span></span>



| <span data-ttu-id="aa305-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aa305-119">Requirement</span></span> | <span data-ttu-id="aa305-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="aa305-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="aa305-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aa305-121">Minimum supported client</span></span><br/> | <span data-ttu-id="aa305-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aa305-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="aa305-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aa305-123">Minimum supported server</span></span><br/> | <span data-ttu-id="aa305-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aa305-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="aa305-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="aa305-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa305-126"><dt>ComSvcs. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa305-126"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa305-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aa305-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa305-128">**ISharedPropertyGroup**</span><span class="sxs-lookup"><span data-stu-id="aa305-128">**ISharedPropertyGroup**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup)
</dt> <dt>

[<span data-ttu-id="aa305-129">**SharedProperty**</span><span class="sxs-lookup"><span data-stu-id="aa305-129">**SharedProperty**</span></span>](sharedproperty.md)
</dt> <dt>

[<span data-ttu-id="aa305-130">**SharedPropertyGroupManager**</span><span class="sxs-lookup"><span data-stu-id="aa305-130">**SharedPropertyGroupManager**</span></span>](sharedpropertygroupmanager.md)
</dt> </dl>

 

 




