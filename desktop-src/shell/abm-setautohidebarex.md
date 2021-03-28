---
description: Inscrit ou désinscrit un appbar de masquage automatique pour un bord donné de l’écran. Ce message étend ABM \_ SETAUTOHIDEBAR en vous permettant de spécifier un moniteur particulier, à utiliser dans plusieurs situations d’analyse.
title: Message ABM_SETAUTOHIDEBAREX (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C437727C-3FF6-4598-9D81-A39FCC2EF1C4
api_name:
- ABM_SETAUTOHIDEBAREX
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ba4e1474d3b57465fa68446fd7ab787c9a62570b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "104996464"
---
# <a name="abm_setautohidebarex-message"></a><span data-ttu-id="5fd62-104">\_Message ABM SETAUTOHIDEBAREX</span><span class="sxs-lookup"><span data-stu-id="5fd62-104">ABM\_SETAUTOHIDEBAREX message</span></span>

<span data-ttu-id="5fd62-105">Inscrit ou désinscrit un appbar de masquage automatique pour un bord donné de l’écran.</span><span class="sxs-lookup"><span data-stu-id="5fd62-105">Registers or unregisters an autohide appbar for a given edge of the screen.</span></span> <span data-ttu-id="5fd62-106">Ce message étend [**ABM \_ SETAUTOHIDEBAR**](abm-setautohidebar.md) en vous permettant de spécifier un moniteur particulier, à utiliser dans plusieurs situations d’analyse.</span><span class="sxs-lookup"><span data-stu-id="5fd62-106">This message extends [**ABM\_SETAUTOHIDEBAR**](abm-setautohidebar.md) by enabling you to specify a particular monitor, for use in multiple monitor situations.</span></span>


```C++
fSuccess = (BOOL) SHAppBarMessage(ABM_SETAUTOHIDEBAR, pabd); 
```



## <a name="parameters"></a><span data-ttu-id="5fd62-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5fd62-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fd62-108">*pabd*</span><span class="sxs-lookup"><span data-stu-id="5fd62-108">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="5fd62-109">Pointeur vers une structure [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) .</span><span class="sxs-lookup"><span data-stu-id="5fd62-109">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span> <span data-ttu-id="5fd62-110">Affectez la valeur **true** au membre **lParam** pour inscrire appbar ou **false** afin d’annuler son inscription.</span><span class="sxs-lookup"><span data-stu-id="5fd62-110">Set the **lParam** member is to **TRUE** to register the appbar or **FALSE** to unregister it.</span></span> <span data-ttu-id="5fd62-111">Vous devez spécifier les membres **cbSize**, **HWND**, **uEdge**, **RC** et **lParam** lors de l’envoi de ce message. tous les autres membres sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="5fd62-111">You must specify the **cbSize**, **hWnd**, **uEdge**, **rc**, and **lParam** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fd62-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5fd62-112">Return value</span></span>

<span data-ttu-id="5fd62-113">Retourne la **valeur true** en cas de réussite, ou **false** si une erreur se produit ou si un appbar de masquage automatique est déjà inscrit pour le bord donné sur l’analyse donnée.</span><span class="sxs-lookup"><span data-stu-id="5fd62-113">Returns **TRUE** if successful, or **FALSE** if an error occurs or if an autohide appbar is already registered for the given edge on the given monitor.</span></span>

## <a name="remarks"></a><span data-ttu-id="5fd62-114">Notes</span><span class="sxs-lookup"><span data-stu-id="5fd62-114">Remarks</span></span>

<span data-ttu-id="5fd62-115">Le système n’autorise qu’un seul appbar de masquage automatique pour chaque bord de chaque moniteur.</span><span class="sxs-lookup"><span data-stu-id="5fd62-115">The system allows only one autohide appbar for each edge of each monitor.</span></span> <span data-ttu-id="5fd62-116">Le moniteur est déterminé par le membre **RC** et le bord est déterminé par le membre **uEdge** de la structure [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) .</span><span class="sxs-lookup"><span data-stu-id="5fd62-116">The monitor is determined by the **rc** member and the edge is determined by the **uEdge** member of the [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fd62-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="5fd62-117">Requirements</span></span>



| <span data-ttu-id="5fd62-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5fd62-118">Requirement</span></span> | <span data-ttu-id="5fd62-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="5fd62-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5fd62-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="5fd62-120">Header</span></span><br/> | <dl> <span data-ttu-id="5fd62-121"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="5fd62-121"><dt>Shellapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fd62-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5fd62-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fd62-123">**ABM \_ GETAUTOHIDEBAR**</span><span class="sxs-lookup"><span data-stu-id="5fd62-123">**ABM\_GETAUTOHIDEBAR**</span></span>](abm-getautohidebar.md)
</dt> <dt>

[<span data-ttu-id="5fd62-124">**ABM \_ GETAUTOHIDEBAREX**</span><span class="sxs-lookup"><span data-stu-id="5fd62-124">**ABM\_GETAUTOHIDEBAREX**</span></span>](abm-getautohidebarex.md)
</dt> <dt>

[<span data-ttu-id="5fd62-125">**ABM \_ SETAUTOHIDEBAR**</span><span class="sxs-lookup"><span data-stu-id="5fd62-125">**ABM\_SETAUTOHIDEBAR**</span></span>](abm-setautohidebar.md)
</dt> </dl>

 

 




