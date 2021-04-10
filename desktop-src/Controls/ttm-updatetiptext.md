---
title: Message TTM_UPDATETIPTEXT (commctrl. h)
description: Définit le texte d’info-bulle d’un outil.
ms.assetid: 2a7432dd-76f9-42b4-b639-178dce1d89ef
keywords:
- TTM_UPDATETIPTEXT les contrôles de message Windows
topic_type:
- apiref
api_name:
- TTM_UPDATETIPTEXT
- TTM_UPDATETIPTEXTA
- TTM_UPDATETIPTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6c94b14ec83c190ce019ecba1413d2fa05f0103
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104434"
---
# <a name="ttm_updatetiptext-message"></a><span data-ttu-id="191c9-104">\_Message atténuation UPDATETIPTEXT</span><span class="sxs-lookup"><span data-stu-id="191c9-104">TTM\_UPDATETIPTEXT message</span></span>

<span data-ttu-id="191c9-105">Définit le texte d’info-bulle d’un outil.</span><span class="sxs-lookup"><span data-stu-id="191c9-105">Sets the tooltip text for a tool.</span></span>

## <a name="parameters"></a><span data-ttu-id="191c9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="191c9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="191c9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="191c9-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="191c9-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="191c9-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="191c9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="191c9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="191c9-110">Pointeur vers une structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) .</span><span class="sxs-lookup"><span data-stu-id="191c9-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span> <span data-ttu-id="191c9-111">Les membres **HINST** et **lpszText** doivent spécifier le handle d’instance et l’adresse du texte.</span><span class="sxs-lookup"><span data-stu-id="191c9-111">The **hinst** and **lpszText** members must specify the instance handle and the address of the text.</span></span> <span data-ttu-id="191c9-112">Les membres **HWND** et **UID** identifient l’outil à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="191c9-112">The **hwnd** and **uId** members identify the tool to update.</span></span> <span data-ttu-id="191c9-113">Le membre **cbSize** de cette structure doit être rempli avant l’envoi de ce message.</span><span class="sxs-lookup"><span data-stu-id="191c9-113">The **cbSize** member of this structure must be filled in before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="191c9-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="191c9-114">Return value</span></span>

<span data-ttu-id="191c9-115">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="191c9-115">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="191c9-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="191c9-116">Requirements</span></span>



| <span data-ttu-id="191c9-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="191c9-117">Requirement</span></span> | <span data-ttu-id="191c9-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="191c9-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="191c9-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="191c9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="191c9-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="191c9-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="191c9-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="191c9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="191c9-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="191c9-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="191c9-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="191c9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="191c9-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="191c9-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="191c9-125">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="191c9-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="191c9-126">**Atténuation \_ UPDATETIPTEXTW** (Unicode) et **atténuation \_ UPDATETIPTEXTA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="191c9-126">**TTM\_UPDATETIPTEXTW** (Unicode) and **TTM\_UPDATETIPTEXTA** (ANSI)</span></span><br/>       |



 

 





