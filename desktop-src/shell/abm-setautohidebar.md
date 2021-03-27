---
description: Inscrit ou désinscrit un appbar de masquage automatique pour un bord donné de l’écran. Si le système possède plusieurs moniteurs, le moniteur qui contient la barre des tâches principale est utilisé.
title: Message ABM_SETAUTOHIDEBAR (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 0cbd6c9c-e83f-41f8-91ed-81afaa24f524
api_name:
- ABM_SETAUTOHIDEBAR
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 53ca89008dda1233d12a7f0a9588803776ba1181
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972098"
---
# <a name="abm_setautohidebar-message"></a><span data-ttu-id="213d4-104">\_Message ABM SETAUTOHIDEBAR</span><span class="sxs-lookup"><span data-stu-id="213d4-104">ABM\_SETAUTOHIDEBAR message</span></span>

<span data-ttu-id="213d4-105">Inscrit ou désinscrit un appbar de masquage automatique pour un bord donné de l’écran.</span><span class="sxs-lookup"><span data-stu-id="213d4-105">Registers or unregisters an autohide appbar for a given edge of the screen.</span></span> <span data-ttu-id="213d4-106">Si le système possède plusieurs moniteurs, le moniteur qui contient la barre des tâches principale est utilisé.</span><span class="sxs-lookup"><span data-stu-id="213d4-106">If the system has multiple monitors, the monitor that contains the primary taskbar is used.</span></span>

> [!Note]  
> <span data-ttu-id="213d4-107">Pour inscrire ou désinscrire un appbar de masquage automatique sur un moniteur spécifique, utilisez [**ABM \_ SETAUTOHIDEBAREX**](abm-setautohidebarex.md).</span><span class="sxs-lookup"><span data-stu-id="213d4-107">To register or unregister an autohide appbar on a specific monitor, use [**ABM\_SETAUTOHIDEBAREX**](abm-setautohidebarex.md).</span></span>

 


```C++
fSuccess = (BOOL) SHAppBarMessage(ABM_SETAUTOHIDEBAR, pabd); 
```



## <a name="parameters"></a><span data-ttu-id="213d4-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="213d4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="213d4-109">*pabd*</span><span class="sxs-lookup"><span data-stu-id="213d4-109">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="213d4-110">Pointeur vers une structure [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) .</span><span class="sxs-lookup"><span data-stu-id="213d4-110">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span> <span data-ttu-id="213d4-111">Affectez la valeur **true** au membre **lParam** pour inscrire appbar ou **false** afin d’annuler son inscription.</span><span class="sxs-lookup"><span data-stu-id="213d4-111">Set the **lParam** member to **TRUE** to register the appbar or **FALSE** to unregister it.</span></span> <span data-ttu-id="213d4-112">Vous devez spécifier les membres **cbSize**, **HWND**, **uEdge** et **lParam** lors de l’envoi de ce message. tous les autres membres sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="213d4-112">You must specify the **cbSize**, **hWnd**, **uEdge**, and **lParam** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="213d4-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="213d4-113">Return value</span></span>

<span data-ttu-id="213d4-114">Retourne la **valeur true** en cas de réussite, ou **false** si une erreur se produit ou si un appbar de masquage automatique est déjà inscrit pour le bord donné.</span><span class="sxs-lookup"><span data-stu-id="213d4-114">Returns **TRUE** if successful, or **FALSE** if an error occurs or if an autohide appbar is already registered for the given edge.</span></span>

## <a name="remarks"></a><span data-ttu-id="213d4-115">Notes</span><span class="sxs-lookup"><span data-stu-id="213d4-115">Remarks</span></span>

<span data-ttu-id="213d4-116">Le système n’autorise qu’un seul appbar de masquage automatique pour chaque bord de l’écran.</span><span class="sxs-lookup"><span data-stu-id="213d4-116">The system allows only one autohide appbar for each edge of the screen.</span></span> <span data-ttu-id="213d4-117">Cela est déterminé lorsque le membre **uEdge** de la structure [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) est défini.</span><span class="sxs-lookup"><span data-stu-id="213d4-117">This is determined when the member **uEdge** of the [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="213d4-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="213d4-118">Requirements</span></span>



| <span data-ttu-id="213d4-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="213d4-119">Requirement</span></span> | <span data-ttu-id="213d4-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="213d4-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="213d4-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="213d4-121">Minimum supported client</span></span><br/> | <span data-ttu-id="213d4-122">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="213d4-122">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="213d4-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="213d4-123">Minimum supported server</span></span><br/> | <span data-ttu-id="213d4-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="213d4-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="213d4-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="213d4-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="213d4-126"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="213d4-126"><dt>Shellapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="213d4-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="213d4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="213d4-128">**ABM \_ SETAUTOHIDEBAR**</span><span class="sxs-lookup"><span data-stu-id="213d4-128">**ABM\_SETAUTOHIDEBAR**</span></span>](abm-getautohidebar.md)
</dt> <dt>

[<span data-ttu-id="213d4-129">**ABM \_ GETAUTOHIDEBAREX**</span><span class="sxs-lookup"><span data-stu-id="213d4-129">**ABM\_GETAUTOHIDEBAREX**</span></span>](abm-getautohidebarex.md)
</dt> <dt>

[<span data-ttu-id="213d4-130">**ABM \_ SETAUTOHIDEBAREX**</span><span class="sxs-lookup"><span data-stu-id="213d4-130">**ABM\_SETAUTOHIDEBAREX**</span></span>](abm-setautohidebarex.md)
</dt> </dl>

 

 




