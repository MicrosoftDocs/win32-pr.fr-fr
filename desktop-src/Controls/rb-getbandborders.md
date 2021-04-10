---
title: Message RB_GETBANDBORDERS (commctrl. h)
description: Récupère les bordures d’une bande. Le résultat de ce message peut être utilisé pour calculer la zone utilisable dans une bande.
ms.assetid: 45f2ae7e-636e-474b-a0d0-5235c6401e6a
keywords:
- RB_GETBANDBORDERS les contrôles de message Windows
topic_type:
- apiref
api_name:
- RB_GETBANDBORDERS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 521dfecaf5e2573b30f606b7b4d7ecdec9bd896d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942460"
---
# <a name="rb_getbandborders-message"></a><span data-ttu-id="6c049-105">\_Message GETBANDBORDERS RB</span><span class="sxs-lookup"><span data-stu-id="6c049-105">RB\_GETBANDBORDERS message</span></span>

<span data-ttu-id="6c049-106">Récupère les bordures d’une bande.</span><span class="sxs-lookup"><span data-stu-id="6c049-106">Retrieves the borders of a band.</span></span> <span data-ttu-id="6c049-107">Le résultat de ce message peut être utilisé pour calculer la zone utilisable dans une bande.</span><span class="sxs-lookup"><span data-stu-id="6c049-107">The result of this message can be used to calculate the usable area in a band.</span></span>

## <a name="parameters"></a><span data-ttu-id="6c049-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6c049-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c049-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6c049-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c049-110">Index de base zéro de la bande pour laquelle les bordures seront récupérées.</span><span class="sxs-lookup"><span data-stu-id="6c049-110">Zero-based index of the band for which the borders will be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="6c049-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6c049-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c049-112">Pointeur désignant une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui recevra les bordures de la bande.</span><span class="sxs-lookup"><span data-stu-id="6c049-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that will receive the band borders.</span></span> <span data-ttu-id="6c049-113">Si le contrôle rebar a le style [**RBS \_ BANDBORDERS**](rebar-control-styles.md) , chaque membre de cette structure recevra le nombre de pixels, sur le côté correspondant de la bande, qui constituent la bordure.</span><span class="sxs-lookup"><span data-stu-id="6c049-113">If the rebar control has the [**RBS\_BANDBORDERS**](rebar-control-styles.md) style, each member of this structure will receive the number of pixels, on the corresponding side of the band, that constitute the border.</span></span> <span data-ttu-id="6c049-114">Si le contrôle rebar n’a pas le style **RBS \_ BANDBORDERS** , seul le membre de **gauche** de cette structure reçoit des informations valides.</span><span class="sxs-lookup"><span data-stu-id="6c049-114">If the rebar control does not have the **RBS\_BANDBORDERS** style, only the **left** member of this structure receives valid information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c049-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6c049-115">Return value</span></span>

<span data-ttu-id="6c049-116">La valeur de retour n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="6c049-116">The return value is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c049-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6c049-117">Requirements</span></span>



| <span data-ttu-id="6c049-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6c049-118">Requirement</span></span> | <span data-ttu-id="6c049-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="6c049-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6c049-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6c049-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6c049-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6c049-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6c049-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6c049-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6c049-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6c049-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6c049-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="6c049-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c049-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c049-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

