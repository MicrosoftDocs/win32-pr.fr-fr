---
description: Récupère le handle du appbar de masquage automatique associé à un bord de l’écran. Si le système possède plusieurs moniteurs, le moniteur qui contient la barre des tâches principale est utilisé.
title: Message ABM_GETAUTOHIDEBAR (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 545dd1d9-8cbb-4ff3-b871-4908ecac56db
api_name:
- ABM_GETAUTOHIDEBAR
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 979825a9dbc28a89e3579419542877faacbace45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112363"
---
# <a name="abm_getautohidebar-message"></a><span data-ttu-id="65b83-104">\_Message ABM GETAUTOHIDEBAR</span><span class="sxs-lookup"><span data-stu-id="65b83-104">ABM\_GETAUTOHIDEBAR message</span></span>

<span data-ttu-id="65b83-105">Récupère le handle du appbar de masquage automatique associé à un bord de l’écran.</span><span class="sxs-lookup"><span data-stu-id="65b83-105">Retrieves the handle to the autohide appbar associated with an edge of the screen.</span></span> <span data-ttu-id="65b83-106">Si le système possède plusieurs moniteurs, le moniteur qui contient la barre des tâches principale est utilisé.</span><span class="sxs-lookup"><span data-stu-id="65b83-106">If the system has multiple monitors, the monitor that contains the primary taskbar is used.</span></span>

> [!Note]  
> <span data-ttu-id="65b83-107">Pour interroger un appbar de masquage automatique sur une analyse spécifique, utilisez [**ABM \_ GETAUTOHIDEBAREX**](abm-getautohidebarex.md).</span><span class="sxs-lookup"><span data-stu-id="65b83-107">To query for an autohide appbar on a specific monitor, use [**ABM\_GETAUTOHIDEBAREX**](abm-getautohidebarex.md).</span></span>

 


```C++
hwndAutoHide = (HWND) SHAppBarMessage(ABM_GETAUTOHIDEBAR, pabd);
```



## <a name="parameters"></a><span data-ttu-id="65b83-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="65b83-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65b83-109">*pabd*</span><span class="sxs-lookup"><span data-stu-id="65b83-109">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="65b83-110">Pointeur vers une structure [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) qui spécifie le bord d’écran.</span><span class="sxs-lookup"><span data-stu-id="65b83-110">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure that specifies the screen edge.</span></span> <span data-ttu-id="65b83-111">Vous devez spécifier les membres **cbSize** et **uEdge** lors de l’envoi de ce message. tous les autres membres sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="65b83-111">You must specify the **cbSize** and **uEdge** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65b83-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="65b83-112">Return value</span></span>

<span data-ttu-id="65b83-113">Retourne le handle du appbar de masquage automatique.</span><span class="sxs-lookup"><span data-stu-id="65b83-113">Returns the handle to the autohide appbar.</span></span> <span data-ttu-id="65b83-114">La valeur de retour est **null** si une erreur se produit ou si aucun appbar de masquage automatique n’est associé au bord donné.</span><span class="sxs-lookup"><span data-stu-id="65b83-114">The return value is **NULL** if an error occurs or if no autohide appbar is associated with the given edge.</span></span>

## <a name="requirements"></a><span data-ttu-id="65b83-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="65b83-115">Requirements</span></span>



| <span data-ttu-id="65b83-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="65b83-116">Requirement</span></span> | <span data-ttu-id="65b83-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="65b83-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="65b83-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65b83-118">Minimum supported client</span></span><br/> | <span data-ttu-id="65b83-119">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="65b83-119">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="65b83-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65b83-120">Minimum supported server</span></span><br/> | <span data-ttu-id="65b83-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="65b83-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="65b83-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="65b83-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="65b83-123"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="65b83-123"><dt>Shellapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65b83-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65b83-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65b83-125">**ABM \_ SETAUTOHIDEBAR**</span><span class="sxs-lookup"><span data-stu-id="65b83-125">**ABM\_SETAUTOHIDEBAR**</span></span>](abm-setautohidebar.md)
</dt> <dt>

[<span data-ttu-id="65b83-126">**ABM \_ GETAUTOHIDEBAREX**</span><span class="sxs-lookup"><span data-stu-id="65b83-126">**ABM\_GETAUTOHIDEBAREX**</span></span>](abm-getautohidebarex.md)
</dt> <dt>

[<span data-ttu-id="65b83-127">**ABM \_ SETAUTOHIDEBAREX**</span><span class="sxs-lookup"><span data-stu-id="65b83-127">**ABM\_SETAUTOHIDEBAREX**</span></span>](abm-setautohidebarex.md)
</dt> </dl>

 

 




