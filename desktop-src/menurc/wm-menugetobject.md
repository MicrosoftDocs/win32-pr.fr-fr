---
title: Message WM_MENUGETOBJECT (winuser. h)
description: Envoyé au propriétaire d’un menu glisser-déplacer lorsque le curseur de la souris entre dans un élément de menu ou se déplace du centre de l’élément vers le haut ou le bas de l’élément.
ms.assetid: 08348e43-3d21-4543-b624-5504575efced
keywords:
- WM_MENUGETOBJECT des menus de message et d’autres ressources
topic_type:
- apiref
api_name:
- WM_MENUGETOBJECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08e124c7f2757a0d6d1d2ac0904052b6d3c255ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519202"
---
# <a name="wm_menugetobject-message"></a><span data-ttu-id="768b0-104">\_Message WM MENUGETOBJECT</span><span class="sxs-lookup"><span data-stu-id="768b0-104">WM\_MENUGETOBJECT message</span></span>

<span data-ttu-id="768b0-105">Envoyé au propriétaire d’un menu glisser-déplacer lorsque le curseur de la souris entre dans un élément de menu ou se déplace du centre de l’élément vers le haut ou le bas de l’élément.</span><span class="sxs-lookup"><span data-stu-id="768b0-105">Sent to the owner of a drag-and-drop menu when the mouse cursor enters a menu item or moves from the center of the item to the top or bottom of the item.</span></span>


```C++
#define WM_MENUGETOBJECT                0x0124
```



## <a name="parameters"></a><span data-ttu-id="768b0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="768b0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="768b0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="768b0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="768b0-108">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="768b0-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="768b0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="768b0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="768b0-110">Pointeur vers une structure [**MENUGETOBJECTINFO**](/windows/win32/api/winuser/ns-winuser-menugetobjectinfo) .</span><span class="sxs-lookup"><span data-stu-id="768b0-110">A pointer to a [**MENUGETOBJECTINFO**](/windows/win32/api/winuser/ns-winuser-menugetobjectinfo) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="768b0-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="768b0-111">Return value</span></span>

<span data-ttu-id="768b0-112">L’application doit retourner l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="768b0-112">The application should return one of the following values.</span></span>



| <span data-ttu-id="768b0-113">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="768b0-113">Return code/value</span></span>                                                                                                                                                | <span data-ttu-id="768b0-114">Description</span><span class="sxs-lookup"><span data-stu-id="768b0-114">Description</span></span>                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="768b0-115"><dt>**MNGO \_ Noerreur**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="768b0-115"><dt>**MNGO\_NOERROR**</dt> <dt>0x00000001</dt></span></span> </dl>     | <span data-ttu-id="768b0-116">Un pointeur d’interface a été retourné dans le membre **pvObj** de [**MENUGETOBJECTINFO**](/windows/win32/api/winuser/ns-winuser-menugetobjectinfo)</span><span class="sxs-lookup"><span data-stu-id="768b0-116">An interface pointer was returned in the **pvObj** member of [**MENUGETOBJECTINFO**](/windows/win32/api/winuser/ns-winuser-menugetobjectinfo)</span></span><br/> |
| <dl> <span data-ttu-id="768b0-117"><dt>**MNGO \_ Nointerface**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="768b0-117"><dt>**MNGO\_NOINTERFACE**</dt> <dt>0x00000000</dt></span></span> </dl> | <span data-ttu-id="768b0-118">L’interface n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="768b0-118">The interface is not supported.</span></span><br/>                                                                             |



 

## <a name="requirements"></a><span data-ttu-id="768b0-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="768b0-119">Requirements</span></span>



| <span data-ttu-id="768b0-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="768b0-120">Requirement</span></span> | <span data-ttu-id="768b0-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="768b0-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="768b0-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="768b0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="768b0-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="768b0-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="768b0-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="768b0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="768b0-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="768b0-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="768b0-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="768b0-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="768b0-127"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="768b0-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="768b0-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="768b0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="768b0-129">Vue d’ensemble des menus</span><span class="sxs-lookup"><span data-stu-id="768b0-129">Menus Overview</span></span>](menus.md)
</dt> </dl>

 

 





