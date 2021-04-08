---
title: Message LVM_SETINSERTMARK (commctrl. h)
description: Définit le point d’insertion à la position définie.
ms.assetid: 32cf5a11-918a-4dc4-bf10-88b3c26f26cc
keywords:
- LVM_SETINSERTMARK les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_SETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dab80b1b73b620ce94b75aecab90f6bdd69bf228
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102884"
---
# <a name="lvm_setinsertmark-message"></a><span data-ttu-id="ba4d4-104">\_Message SETINSERTMARK LVM</span><span class="sxs-lookup"><span data-stu-id="ba4d4-104">LVM\_SETINSERTMARK message</span></span>

<span data-ttu-id="ba4d4-105">Définit le point d’insertion à la position définie.</span><span class="sxs-lookup"><span data-stu-id="ba4d4-105">Sets the insertion point to the defined position.</span></span>

## <a name="parameters"></a><span data-ttu-id="ba4d4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ba4d4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba4d4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ba4d4-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ba4d4-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="ba4d4-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ba4d4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ba4d4-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ba4d4-110">Pointeur vers une structure <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">LVINSERTMARK</a> qui spécifie où définir le point d’insertion.</span><span class="sxs-lookup"><span data-stu-id="ba4d4-110">Pointer to a <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">LVINSERTMARK</a> structure that specifies where to set the insertion point.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba4d4-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ba4d4-111">Return value</span></span>

<span data-ttu-id="ba4d4-112">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="ba4d4-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span> <span data-ttu-id="ba4d4-113">La **valeur false** est retournée si la taille du membre **cbSize** de la structure [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) n’est pas égale à la taille réelle de la structure, ou lorsqu’un point d’insertion ne s’applique pas à la vue actuelle.</span><span class="sxs-lookup"><span data-stu-id="ba4d4-113">**FALSE** is returned if the size in the **cbSize** member of the [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) structure does not equal the actual size of the structure, or when an insertion point does not apply in the current view.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba4d4-114">Notes</span><span class="sxs-lookup"><span data-stu-id="ba4d4-114">Remarks</span></span>

<span data-ttu-id="ba4d4-115">Un point d’insertion ne peut apparaître que si le contrôle de liste est en mode icône, en mode petites icônes ou en mode mosaïque, et n’est pas en mode de vue groupe.</span><span class="sxs-lookup"><span data-stu-id="ba4d4-115">An insertion point can only appear if the list-view control is in icon view, small icon view, or tile view, and is not in group-view mode.</span></span>

> [!Note]  
> <span data-ttu-id="ba4d4-116">Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="ba4d4-116">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="ba4d4-117">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ba4d4-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ba4d4-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ba4d4-118">Requirements</span></span>



| <span data-ttu-id="ba4d4-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ba4d4-119">Requirement</span></span> | <span data-ttu-id="ba4d4-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="ba4d4-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ba4d4-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ba4d4-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ba4d4-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ba4d4-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ba4d4-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ba4d4-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ba4d4-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ba4d4-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ba4d4-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="ba4d4-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba4d4-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba4d4-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





