---
title: Message LVM_INSERTMARKHITTEST (commctrl. h)
description: Récupère le point d’insertion le plus proche d’un point spécifié.
ms.assetid: 901bb770-a36d-4d9f-a53b-d497b4df39e5
keywords:
- LVM_INSERTMARKHITTEST les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_INSERTMARKHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bdb82e924b4a5d74d152917f52c4039e0aca81b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105478"
---
# <a name="lvm_insertmarkhittest-message"></a><span data-ttu-id="0e911-104">\_Message INSERTMARKHITTEST LVM</span><span class="sxs-lookup"><span data-stu-id="0e911-104">LVM\_INSERTMARKHITTEST message</span></span>

<span data-ttu-id="0e911-105">Récupère le point d’insertion le plus proche d’un point spécifié.</span><span class="sxs-lookup"><span data-stu-id="0e911-105">Retrieves the insertion point closest to a specified point.</span></span>

## <a name="parameters"></a><span data-ttu-id="0e911-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0e911-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e911-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0e911-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0e911-108">Pointeur vers une structure de **points** qui contient les coordonnées du test d’atteinte.</span><span class="sxs-lookup"><span data-stu-id="0e911-108">Pointer to a **POINT** structure that contains the hit test coordinates.</span></span></dd> <dt>

<span data-ttu-id="0e911-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0e911-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="0e911-110">Pointeur vers une structure <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">LVINSERTMARK</a> qui spécifie le point d’insertion le plus proche des coordonnées définies par le paramètre *wParam* .</span><span class="sxs-lookup"><span data-stu-id="0e911-110">Pointer to an <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">LVINSERTMARK</a> structure that specifies the insertion point closest to the coordinates defined by the *wParam* parameter.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e911-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0e911-111">Return value</span></span>

<span data-ttu-id="0e911-112">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="0e911-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span> <span data-ttu-id="0e911-113">La **valeur false** est retournée si la taille du membre **cbSize** de la structure [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) n’est pas égale à la taille réelle de la structure, ou lorsqu’un point d’insertion ne s’applique pas à la vue actuelle.</span><span class="sxs-lookup"><span data-stu-id="0e911-113">**FALSE** is returned if the size in the **cbSize** member of the [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) structure does not equal the actual size of the structure, or when an insertion point does not apply in the current view.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e911-114">Notes</span><span class="sxs-lookup"><span data-stu-id="0e911-114">Remarks</span></span>

<span data-ttu-id="0e911-115">Un point d’insertion ne peut apparaître que si le contrôle de liste est en mode icône, en mode petite icône ou en mode mosaïque et n’est pas en mode groupe.</span><span class="sxs-lookup"><span data-stu-id="0e911-115">An insertion point can only appear if the list-view control is in icon view, small icon view, or tile view and is not in group-view mode.</span></span>

<span data-ttu-id="0e911-116">Si les points d’insertion ne s’appliquent pas à la vue, la structure [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) contient-1 dans le membre **iItem** .</span><span class="sxs-lookup"><span data-stu-id="0e911-116">If insertion points do not apply for the view, the [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) structure contains a -1 in the **iItem** member.</span></span>

> [!Note]  
> <span data-ttu-id="0e911-117">Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="0e911-117">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="0e911-118">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0e911-118">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0e911-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e911-119">Requirements</span></span>



| <span data-ttu-id="0e911-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e911-120">Requirement</span></span> | <span data-ttu-id="0e911-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e911-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0e911-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e911-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0e911-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0e911-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0e911-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e911-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0e911-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0e911-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0e911-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="0e911-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e911-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e911-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





