---
description: 'Avertit l’objet de rappel que la barre d’État est en cours de mise à jour. Utilisé par IShellFolderViewCB :: MessageSFVCB.'
title: Message SFVM_UPDATESTATUSBAR (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: f1bac364-1011-4308-8b9b-8ed1800dd30d
api_name:
- SFVM_UPDATESTATUSBAR
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 14045c797d7292099c1c7b2c67f5958609d8d6b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991629"
---
# <a name="sfvm_updatestatusbar-message"></a><span data-ttu-id="8ed3c-104">\_Message SFVM UPDATESTATUSBAR</span><span class="sxs-lookup"><span data-stu-id="8ed3c-104">SFVM\_UPDATESTATUSBAR message</span></span>

<span data-ttu-id="8ed3c-105">Avertit l’objet de rappel que la barre d’État est en cours de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="8ed3c-105">Notifies the callback object that the status bar is being updated.</span></span> <span data-ttu-id="8ed3c-106">Utilisé par [**IShellFolderViewCB :: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="8ed3c-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_UPDATESTATUSBAR 

    wParam = (WPARAM)(BOOL) fInitialize;

            
```



## <a name="parameters"></a><span data-ttu-id="8ed3c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8ed3c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ed3c-108">*fInitialize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8ed3c-108">*fInitialize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ed3c-109">Valeur **booléenne** qui a la valeur **true** si la barre d’État est en cours d’initialisation.</span><span class="sxs-lookup"><span data-stu-id="8ed3c-109">A **BOOL** value that is set to **TRUE** if the status bar is being initialized.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8ed3c-110">Notes</span><span class="sxs-lookup"><span data-stu-id="8ed3c-110">Remarks</span></span>

<span data-ttu-id="8ed3c-111">Quand vous recevez cette notification :</span><span class="sxs-lookup"><span data-stu-id="8ed3c-111">When you receive this notification:</span></span>

-   <span data-ttu-id="8ed3c-112">Renvoyez \_ OK si vous devez gérer la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="8ed3c-112">Return S\_OK if you will handle the update.</span></span>
-   <span data-ttu-id="8ed3c-113">Return MAKE \_ HRESULT (gravité \_ Success, 0, 1) pour que l’objet de la vue du dossier système définisse le texte de la barre d’État.</span><span class="sxs-lookup"><span data-stu-id="8ed3c-113">Return MAKE\_HRESULT(SEVERITY\_SUCCESS,0,1) to have the system folder view object set the status bar text.</span></span>
-   <span data-ttu-id="8ed3c-114">Return E \_ Fail pour que l’objet de la vue du dossier système gère la barre d’État.</span><span class="sxs-lookup"><span data-stu-id="8ed3c-114">Return E\_FAIL to have the system folder view object handle the status bar.</span></span>

<span data-ttu-id="8ed3c-115">Le texte de la barre d’État par défaut est le suivant.</span><span class="sxs-lookup"><span data-stu-id="8ed3c-115">The default status bar text is as follows.</span></span>



| <span data-ttu-id="8ed3c-116">Statut</span><span class="sxs-lookup"><span data-stu-id="8ed3c-116">Status</span></span>                      | <span data-ttu-id="8ed3c-117">Texte de la barre d'état</span><span class="sxs-lookup"><span data-stu-id="8ed3c-117">Status bar text</span></span>                         |
|-----------------------------|-----------------------------------------|
| <span data-ttu-id="8ed3c-118">Aucun élément sélectionné</span><span class="sxs-lookup"><span data-stu-id="8ed3c-118">No items selected</span></span>           | <span data-ttu-id="8ed3c-119">« \# \# objets » (dans le dossier)</span><span class="sxs-lookup"><span data-stu-id="8ed3c-119">"\#\# objects" (in the folder)</span></span>          |
| <span data-ttu-id="8ed3c-120">Un élément sélectionné</span><span class="sxs-lookup"><span data-stu-id="8ed3c-120">One item selected</span></span>           | <span data-ttu-id="8ed3c-121">Info-bulle de l’élément, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="8ed3c-121">The infotip for the item, if available.</span></span> |
| <span data-ttu-id="8ed3c-122">Plus d’un élément sélectionné</span><span class="sxs-lookup"><span data-stu-id="8ed3c-122">More than one item selected</span></span> | <span data-ttu-id="8ed3c-123">« \# \# objets sélectionnés »</span><span class="sxs-lookup"><span data-stu-id="8ed3c-123">"\#\# objects selected"</span></span>                 |



 

## <a name="requirements"></a><span data-ttu-id="8ed3c-124">Spécifications</span><span class="sxs-lookup"><span data-stu-id="8ed3c-124">Requirements</span></span>



| <span data-ttu-id="8ed3c-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8ed3c-125">Requirement</span></span> | <span data-ttu-id="8ed3c-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="8ed3c-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8ed3c-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8ed3c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="8ed3c-128">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8ed3c-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="8ed3c-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8ed3c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="8ed3c-130">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8ed3c-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8ed3c-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="8ed3c-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ed3c-132"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ed3c-132"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
