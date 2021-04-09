---
description: Définit ou récupère la valeur d’une propriété partagée.
ms.assetid: 19ed8d50-3ac1-408e-9f25-09f284d025f1
title: SharedProperty, classe (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SharedProperty
api_type:
- COM
ms.openlocfilehash: a7a7857ad280ad722601bdced6c25d04b03dc0b3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110554"
---
# <a name="sharedproperty-class"></a><span data-ttu-id="dbe0c-103">SharedProperty, classe</span><span class="sxs-lookup"><span data-stu-id="dbe0c-103">SharedProperty class</span></span>

<span data-ttu-id="dbe0c-104">Définit ou récupère la valeur d’une propriété partagée.</span><span class="sxs-lookup"><span data-stu-id="dbe0c-104">Sets or retrieves the value of a shared property.</span></span>

<span data-ttu-id="dbe0c-105">Pour obtenir des informations générales sur l’utilisation de l’Gestionnaire de propriétés partagé dans COM+, consultez [Gestionnaire de propriétés partagées com+](com--shared-property-manager.md).</span><span class="sxs-lookup"><span data-stu-id="dbe0c-105">For general information about using the Shared Property Manager in COM+, see [COM+ Shared Property Manager](com--shared-property-manager.md).</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="dbe0c-106">Quand implémenter</span><span class="sxs-lookup"><span data-stu-id="dbe0c-106">When to implement</span></span>

<span data-ttu-id="dbe0c-107">Cette classe est implémentée par COM+.</span><span class="sxs-lookup"><span data-stu-id="dbe0c-107">This class is implemented by COM+.</span></span>



| <span data-ttu-id="dbe0c-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dbe0c-108">Requirement</span></span> | <span data-ttu-id="dbe0c-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="dbe0c-109">Value</span></span> |
|------------|--------------------------------------------|
| <span data-ttu-id="dbe0c-110">Interfaces</span><span class="sxs-lookup"><span data-stu-id="dbe0c-110">Interfaces</span></span> | [<span data-ttu-id="dbe0c-111">**ISharedProperty**</span><span class="sxs-lookup"><span data-stu-id="dbe0c-111">**ISharedProperty**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedproperty) |



 

## <a name="when-to-use"></a><span data-ttu-id="dbe0c-112">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="dbe0c-112">When to use</span></span>

<span data-ttu-id="dbe0c-113">Utilisez cette classe pour accéder aux méthodes de [**ISharedProperty**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedproperty).</span><span class="sxs-lookup"><span data-stu-id="dbe0c-113">Use this class to access the methods of [**ISharedProperty**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedproperty).</span></span>

## <a name="remarks"></a><span data-ttu-id="dbe0c-114">Notes</span><span class="sxs-lookup"><span data-stu-id="dbe0c-114">Remarks</span></span>

<span data-ttu-id="dbe0c-115">Vous pouvez créer un objet **SharedProperty** à l’aide des méthodes [**CreateProperty**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createproperty) ou [**CreatePropertyByPosition**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createpropertybyposition) de [**ISharedPropertyGroup**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup).</span><span class="sxs-lookup"><span data-stu-id="dbe0c-115">You can create a **SharedProperty** object by using the [**CreateProperty**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createproperty) or [**CreatePropertyByPosition**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createpropertybyposition) methods of [**ISharedPropertyGroup**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup).</span></span>

<span data-ttu-id="dbe0c-116">Pour utiliser cette classe à partir de Microsoft Visual Basic, ajoutez une référence à la bibliothèque de types des services COM+.</span><span class="sxs-lookup"><span data-stu-id="dbe0c-116">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="dbe0c-117">Un objet SharedProperty est créé en appelant les méthodes [**CreateProperty**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createproperty) ou [**CreatePropertyByPosition**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createpropertybyposition) de l’objet [**SharedPropertyGroup**](sharedpropertygroup.md) .</span><span class="sxs-lookup"><span data-stu-id="dbe0c-117">A SharedProperty object is created by calling the [**CreateProperty**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createproperty) or [**CreatePropertyByPosition**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createpropertybyposition) methods of the [**SharedPropertyGroup**](sharedpropertygroup.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbe0c-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dbe0c-118">Requirements</span></span>



| <span data-ttu-id="dbe0c-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dbe0c-119">Requirement</span></span> | <span data-ttu-id="dbe0c-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="dbe0c-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="dbe0c-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dbe0c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="dbe0c-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dbe0c-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="dbe0c-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dbe0c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="dbe0c-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dbe0c-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="dbe0c-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="dbe0c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="dbe0c-126"><dt>ComSvcs. h</dt></span><span class="sxs-lookup"><span data-stu-id="dbe0c-126"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbe0c-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dbe0c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbe0c-128">**ISharedProperty**</span><span class="sxs-lookup"><span data-stu-id="dbe0c-128">**ISharedProperty**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedproperty)
</dt> <dt>

[<span data-ttu-id="dbe0c-129">**SharedPropertyGroup**</span><span class="sxs-lookup"><span data-stu-id="dbe0c-129">**SharedPropertyGroup**</span></span>](sharedpropertygroup.md)
</dt> <dt>

[<span data-ttu-id="dbe0c-130">**SharedPropertyGroupManager**</span><span class="sxs-lookup"><span data-stu-id="dbe0c-130">**SharedPropertyGroupManager**</span></span>](sharedpropertygroupmanager.md)
</dt> </dl>

 

 




