---
title: Message TB_GETINSERTMARK (commctrl. h)
description: Récupère la marque d’insertion actuelle pour la barre d’outils.
ms.assetid: b22770a4-e859-451d-a726-279bbc49b984
keywords:
- TB_GETINSERTMARK les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_GETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b45a4cafbd49c709e9ca5b8e9afeda51323de491
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032484"
---
# <a name="tb_getinsertmark-message"></a><span data-ttu-id="414d9-104">TO \_ GETINSERTMARK message</span><span class="sxs-lookup"><span data-stu-id="414d9-104">TB\_GETINSERTMARK message</span></span>

<span data-ttu-id="414d9-105">Récupère la marque d’insertion actuelle pour la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="414d9-105">Retrieves the current insertion mark for the toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="414d9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="414d9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="414d9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="414d9-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="414d9-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="414d9-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="414d9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="414d9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="414d9-110">Pointeur vers une structure [**TBINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark) qui reçoit la marque d’insertion.</span><span class="sxs-lookup"><span data-stu-id="414d9-110">Pointer to a [**TBINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark) structure that receives the insertion mark.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="414d9-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="414d9-111">Return value</span></span>

<span data-ttu-id="414d9-112">Retourne toujours la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="414d9-112">Always returns **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="414d9-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="414d9-113">Requirements</span></span>



| <span data-ttu-id="414d9-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="414d9-114">Requirement</span></span> | <span data-ttu-id="414d9-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="414d9-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="414d9-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="414d9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="414d9-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="414d9-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="414d9-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="414d9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="414d9-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="414d9-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="414d9-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="414d9-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="414d9-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="414d9-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="414d9-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="414d9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="414d9-123">**TO \_ SETINSERTMARK**</span><span class="sxs-lookup"><span data-stu-id="414d9-123">**TB\_SETINSERTMARK**</span></span>](tb-setinsertmark.md)
</dt> </dl>

 

 





