---
description: Crée des groupes de propriétés partagées et pour obtenir l’accès aux groupes de propriétés partagés existants.
ms.assetid: 4ba05806-afda-4926-8ca4-abbf15ed8278
title: SharedPropertyGroupManager, classe (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SharedPropertyGroupManager
api_type:
- COM
ms.openlocfilehash: 680c5caef996d329e18192193f30841f61f02f27
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860977"
---
# <a name="sharedpropertygroupmanager-class"></a><span data-ttu-id="c492c-103">SharedPropertyGroupManager, classe</span><span class="sxs-lookup"><span data-stu-id="c492c-103">SharedPropertyGroupManager class</span></span>

<span data-ttu-id="c492c-104">Crée des groupes de propriétés partagées et pour obtenir l’accès aux groupes de propriétés partagés existants.</span><span class="sxs-lookup"><span data-stu-id="c492c-104">Creates shared property groups and to obtain access to existing shared property groups.</span></span>

<span data-ttu-id="c492c-105">Pour plus d’informations sur l’utilisation de l’Gestionnaire de propriétés partagé dans COM+, consultez [Gestionnaire de propriétés partagées com+](com--shared-property-manager.md).</span><span class="sxs-lookup"><span data-stu-id="c492c-105">For more information about using the Shared Property Manager in COM+, see [COM+ Shared Property Manager](com--shared-property-manager.md).</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="c492c-106">Quand implémenter</span><span class="sxs-lookup"><span data-stu-id="c492c-106">When to implement</span></span>

<span data-ttu-id="c492c-107">Cette classe est implémentée par COM+.</span><span class="sxs-lookup"><span data-stu-id="c492c-107">This class is implemented by COM+.</span></span>



| <span data-ttu-id="c492c-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c492c-108">Requirement</span></span> | <span data-ttu-id="c492c-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="c492c-109">Value</span></span> |
|------------|--------------------------------------------------------------------|
| <span data-ttu-id="c492c-110">CLSID</span><span class="sxs-lookup"><span data-stu-id="c492c-110">CLSID</span></span>      | <span data-ttu-id="c492c-111">CLSID \_ SharedPropertyGroupManager</span><span class="sxs-lookup"><span data-stu-id="c492c-111">CLSID\_SharedPropertyGroupManager</span></span>                                  |
| <span data-ttu-id="c492c-112">ProgID</span><span class="sxs-lookup"><span data-stu-id="c492c-112">ProgID</span></span>     | <span data-ttu-id="c492c-113">L "MTxSpm. SharedPropertyGroupManager"</span><span class="sxs-lookup"><span data-stu-id="c492c-113">L"MTxSpm.SharedPropertyGroupManager"</span></span>                               |
| <span data-ttu-id="c492c-114">Interfaces</span><span class="sxs-lookup"><span data-stu-id="c492c-114">Interfaces</span></span> | [<span data-ttu-id="c492c-115">**ISharedPropertyGroupManager**</span><span class="sxs-lookup"><span data-stu-id="c492c-115">**ISharedPropertyGroupManager**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager) |



 

## <a name="when-to-use"></a><span data-ttu-id="c492c-116">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="c492c-116">When to use</span></span>

<span data-ttu-id="c492c-117">Utilisez cette classe pour accéder aux méthodes de [**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager).</span><span class="sxs-lookup"><span data-stu-id="c492c-117">Use this class to access the methods of [**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager).</span></span>

## <a name="remarks"></a><span data-ttu-id="c492c-118">Notes</span><span class="sxs-lookup"><span data-stu-id="c492c-118">Remarks</span></span>

<span data-ttu-id="c492c-119">Pour créer cet objet, appelez [**IObjectContext :: CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance).</span><span class="sxs-lookup"><span data-stu-id="c492c-119">To create this object, call [**IObjectContext::CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance).</span></span>

<span data-ttu-id="c492c-120">Pour utiliser cette classe à partir de Microsoft Visual Basic, ajoutez une référence à la bibliothèque de types des services COM+.</span><span class="sxs-lookup"><span data-stu-id="c492c-120">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="c492c-121">Un objet SharedPropertyGroupManager peut être déclaré à l’aide de « COMSVCSLib. SharedPropertyGroupManager » comme nom de classe.</span><span class="sxs-lookup"><span data-stu-id="c492c-121">A SharedPropertyGroupManager object can be declared using "COMSVCSLib.SharedPropertyGroupManager" as the class name.</span></span>

## <a name="requirements"></a><span data-ttu-id="c492c-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c492c-122">Requirements</span></span>



| <span data-ttu-id="c492c-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c492c-123">Requirement</span></span> | <span data-ttu-id="c492c-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="c492c-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c492c-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c492c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c492c-126">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c492c-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="c492c-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c492c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c492c-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c492c-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c492c-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="c492c-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="c492c-130"><dt>ComSvcs. h</dt></span><span class="sxs-lookup"><span data-stu-id="c492c-130"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c492c-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c492c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c492c-132">**ISharedPropertyGroupManager**</span><span class="sxs-lookup"><span data-stu-id="c492c-132">**ISharedPropertyGroupManager**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager)
</dt> <dt>

[<span data-ttu-id="c492c-133">**SharedProperty**</span><span class="sxs-lookup"><span data-stu-id="c492c-133">**SharedProperty**</span></span>](sharedproperty.md)
</dt> <dt>

[<span data-ttu-id="c492c-134">**SharedPropertyGroup**</span><span class="sxs-lookup"><span data-stu-id="c492c-134">**SharedPropertyGroup**</span></span>](sharedpropertygroup.md)
</dt> </dl>

 

 




