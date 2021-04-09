---
title: Message RB_SETBARINFO (commctrl. h)
description: Définit les caractéristiques d’un contrôle rebar.
ms.assetid: e4413d46-574f-4ccd-b5fd-3ba6c1e3924b
keywords:
- RB_SETBARINFO les contrôles de message Windows
topic_type:
- apiref
api_name:
- RB_SETBARINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b360bc0b4d14963619aad8f769634d7dd0ad17e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032414"
---
# <a name="rb_setbarinfo-message"></a><span data-ttu-id="285a1-104">\_Message SETBARINFO RB</span><span class="sxs-lookup"><span data-stu-id="285a1-104">RB\_SETBARINFO message</span></span>

<span data-ttu-id="285a1-105">Définit les caractéristiques d’un contrôle rebar.</span><span class="sxs-lookup"><span data-stu-id="285a1-105">Sets the characteristics of a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="285a1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="285a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="285a1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="285a1-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="285a1-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="285a1-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="285a1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="285a1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="285a1-110">Pointeur vers une structure [**REBARINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarinfo) qui contient les informations à définir.</span><span class="sxs-lookup"><span data-stu-id="285a1-110">Pointer to a [**REBARINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarinfo) structure that contains the information to be set.</span></span> <span data-ttu-id="285a1-111">Vous devez définir le membre **cbSize** de cette structure sur **sizeof**(REBARINFO) avant d’envoyer ce message.</span><span class="sxs-lookup"><span data-stu-id="285a1-111">You must set the **cbSize** member of this structure to **sizeof**(REBARINFO) before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="285a1-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="285a1-112">Return value</span></span>

<span data-ttu-id="285a1-113">Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="285a1-113">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="285a1-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="285a1-114">Requirements</span></span>



| <span data-ttu-id="285a1-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="285a1-115">Requirement</span></span> | <span data-ttu-id="285a1-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="285a1-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="285a1-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="285a1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="285a1-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="285a1-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="285a1-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="285a1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="285a1-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="285a1-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="285a1-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="285a1-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="285a1-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="285a1-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





