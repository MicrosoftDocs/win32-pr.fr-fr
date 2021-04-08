---
title: Message LVM_GETINSERTMARK (commctrl. h)
description: Récupère la position du point d’insertion.
ms.assetid: ad00df4c-4b4b-48f1-8821-7849a216df2e
keywords:
- LVM_GETINSERTMARK les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8cba96ae7d357e3e1f5a007fa41f6b7e9e3b64f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843353"
---
# <a name="lvm_getinsertmark-message"></a><span data-ttu-id="dbc14-104">\_Message GETINSERTMARK LVM</span><span class="sxs-lookup"><span data-stu-id="dbc14-104">LVM\_GETINSERTMARK message</span></span>

<span data-ttu-id="dbc14-105">Récupère la position du point d’insertion.</span><span class="sxs-lookup"><span data-stu-id="dbc14-105">Retrieves the position of the insertion point.</span></span>

## <a name="parameters"></a><span data-ttu-id="dbc14-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dbc14-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbc14-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dbc14-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="dbc14-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="dbc14-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="dbc14-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dbc14-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="dbc14-110">Pointeur vers une structure <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">LVINSERTMARK</a> qui reçoit la position du point d’insertion.</span><span class="sxs-lookup"><span data-stu-id="dbc14-110">Pointer to a <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">LVINSERTMARK</a> structure that receives the position of the insertion point.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbc14-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dbc14-111">Return value</span></span>

<span data-ttu-id="dbc14-112">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="dbc14-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span> <span data-ttu-id="dbc14-113">La **valeur false** est retournée si la taille du membre **cbSize** de la structure [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) n’est pas égale à la taille réelle de la structure.</span><span class="sxs-lookup"><span data-stu-id="dbc14-113">**FALSE** is returned if the size in the **cbSize** member of the [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) structure does not equal the actual size of the structure.</span></span>

## <a name="remarks"></a><span data-ttu-id="dbc14-114">Notes</span><span class="sxs-lookup"><span data-stu-id="dbc14-114">Remarks</span></span>

<span data-ttu-id="dbc14-115">Un point d’insertion peut apparaître uniquement si le contrôle de liste est en mode icône, en mode petites icônes ou en mode mosaïque, et n’est pas en mode groupe.</span><span class="sxs-lookup"><span data-stu-id="dbc14-115">An insertion point can appear only if the list-view control is in icon view, small icon view, or tile view, and is not in group-view mode.</span></span>

> [!Note]  
> <span data-ttu-id="dbc14-116">Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="dbc14-116">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="dbc14-117">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="dbc14-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="dbc14-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dbc14-118">Requirements</span></span>



| <span data-ttu-id="dbc14-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dbc14-119">Requirement</span></span> | <span data-ttu-id="dbc14-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="dbc14-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dbc14-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dbc14-121">Minimum supported client</span></span><br/> | <span data-ttu-id="dbc14-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dbc14-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dbc14-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dbc14-123">Minimum supported server</span></span><br/> | <span data-ttu-id="dbc14-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dbc14-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dbc14-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="dbc14-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="dbc14-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="dbc14-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





