---
description: Récupère le handle du appbar de masquage automatique associé à un bord de l’écran. Ce message étend ABM \_ GETAUTOHIDEBAR en vous permettant de spécifier un moniteur particulier, à utiliser dans plusieurs situations d’analyse.
title: Message ABM_GETAUTOHIDEBAREX (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 538EA230-06DF-4441-A6AA-9DD613521BE1
api_name:
- ABM_GETAUTOHIDEBAREX
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2ef95739a1031efb199e6acd99686e0858a9630e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "104982970"
---
# <a name="abm_getautohidebarex-message"></a><span data-ttu-id="51c1c-104">\_Message ABM GETAUTOHIDEBAREX</span><span class="sxs-lookup"><span data-stu-id="51c1c-104">ABM\_GETAUTOHIDEBAREX message</span></span>

<span data-ttu-id="51c1c-105">Récupère le handle du appbar de masquage automatique associé à un bord de l’écran.</span><span class="sxs-lookup"><span data-stu-id="51c1c-105">Retrieves the handle to the autohide appbar associated with an edge of the screen.</span></span> <span data-ttu-id="51c1c-106">Ce message étend [**ABM \_ GETAUTOHIDEBAR**](abm-getautohidebar.md) en vous permettant de spécifier un moniteur particulier, à utiliser dans plusieurs situations d’analyse.</span><span class="sxs-lookup"><span data-stu-id="51c1c-106">This message extends [**ABM\_GETAUTOHIDEBAR**](abm-getautohidebar.md) by enabling you to specify a particular monitor, for use in multiple monitor situations.</span></span>


```C++
hwndAutoHide = (HWND) SHAppBarMessage(ABM_GETAUTOHIDEBAR, pabd);
```



## <a name="parameters"></a><span data-ttu-id="51c1c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="51c1c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51c1c-108">*pabd*</span><span class="sxs-lookup"><span data-stu-id="51c1c-108">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="51c1c-109">Pointeur vers une structure [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) qui spécifie le bord d’écran et le moniteur.</span><span class="sxs-lookup"><span data-stu-id="51c1c-109">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure that specifies the screen edge and monitor.</span></span> <span data-ttu-id="51c1c-110">Vous devez spécifier les membres **cbSize**, **uEdge** et **RC** lors de l’envoi de ce message. tous les autres membres sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="51c1c-110">You must specify the **cbSize**, **uEdge**, and **rc** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51c1c-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="51c1c-111">Return value</span></span>

<span data-ttu-id="51c1c-112">Retourne le handle du appbar de masquage automatique.</span><span class="sxs-lookup"><span data-stu-id="51c1c-112">Returns the handle to the autohide appbar.</span></span> <span data-ttu-id="51c1c-113">La valeur de retour est **null** si une erreur se produit ou si aucun appbar de masquage automatique n’est associé au bord donné du moniteur donné.</span><span class="sxs-lookup"><span data-stu-id="51c1c-113">The return value is **NULL** if an error occurs or if no autohide appbar is associated with the given edge of the given monitor.</span></span>

## <a name="requirements"></a><span data-ttu-id="51c1c-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="51c1c-114">Requirements</span></span>



| <span data-ttu-id="51c1c-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="51c1c-115">Requirement</span></span> | <span data-ttu-id="51c1c-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="51c1c-116">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="51c1c-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="51c1c-117">Header</span></span><br/> | <dl> <span data-ttu-id="51c1c-118"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="51c1c-118"><dt>Shellapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51c1c-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="51c1c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51c1c-120">**ABM \_ GETAUTOHIDEBAR**</span><span class="sxs-lookup"><span data-stu-id="51c1c-120">**ABM\_GETAUTOHIDEBAR**</span></span>](abm-getautohidebar.md)
</dt> <dt>

[<span data-ttu-id="51c1c-121">**ABM \_ SETAUTOHIDEBAR**</span><span class="sxs-lookup"><span data-stu-id="51c1c-121">**ABM\_SETAUTOHIDEBAR**</span></span>](abm-setautohidebar.md)
</dt> <dt>

[<span data-ttu-id="51c1c-122">**ABM \_ SETAUTOHIDEBAREX**</span><span class="sxs-lookup"><span data-stu-id="51c1c-122">**ABM\_SETAUTOHIDEBAREX**</span></span>](abm-setautohidebarex.md)
</dt> </dl>

 

 




