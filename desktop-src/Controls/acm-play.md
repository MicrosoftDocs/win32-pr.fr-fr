---
title: Message ACM_PLAY (commctrl. h)
description: Lit un clip AVI dans un contrôle d’animation. Le contrôle lit le clip en arrière-plan pendant que le thread continue de s’exécuter. Vous pouvez envoyer ce message de manière explicite ou à l’aide de la macro animer \_ Play.
ms.assetid: 738b7305-bb77-441d-a198-17daf3b76039
keywords:
- ACM_PLAY les contrôles de message Windows
topic_type:
- apiref
api_name:
- ACM_PLAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e501f3718e1b8172e2b7b16566f992c26346b7f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464670"
---
# <a name="acm_play-message"></a><span data-ttu-id="c9054-106">\_Message de lecture ACM</span><span class="sxs-lookup"><span data-stu-id="c9054-106">ACM\_PLAY message</span></span>

<span data-ttu-id="c9054-107">Lit un clip AVI dans un contrôle d’animation.</span><span class="sxs-lookup"><span data-stu-id="c9054-107">Plays an AVI clip in an animation control.</span></span> <span data-ttu-id="c9054-108">Le contrôle lit le clip en arrière-plan pendant que le thread continue de s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="c9054-108">The control plays the clip in the background while the thread continues executing.</span></span> <span data-ttu-id="c9054-109">Vous pouvez envoyer ce message de manière explicite ou à l’aide de la macro [**animer \_ Play**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play) .</span><span class="sxs-lookup"><span data-stu-id="c9054-109">You can send this message explicitly or by using the [**Animate\_Play**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c9054-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c9054-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9054-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c9054-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c9054-112">**Uint** qui spécifie le nombre de relectures du clip avi.</span><span class="sxs-lookup"><span data-stu-id="c9054-112">A **UINT** that specifies the number of times to replay the AVI clip.</span></span> <span data-ttu-id="c9054-113">La valeur-1 signifie relire indéfiniment le clip.</span><span class="sxs-lookup"><span data-stu-id="c9054-113">A value of -1 means replay the clip indefinitely.</span></span>

</dd> <dt>

<span data-ttu-id="c9054-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c9054-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c9054-115">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) est l’index de base zéro de la trame dans laquelle la fonction Play commence.</span><span class="sxs-lookup"><span data-stu-id="c9054-115">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is the zero-based index of the frame where playing begins.</span></span> <span data-ttu-id="c9054-116">La valeur doit être inférieure à 65 536.</span><span class="sxs-lookup"><span data-stu-id="c9054-116">The value must be less than 65,536.</span></span> <span data-ttu-id="c9054-117">La valeur zéro signifie que commence par la première image du clip AVI.</span><span class="sxs-lookup"><span data-stu-id="c9054-117">A value of zero means begin with the first frame in the AVI clip.</span></span>

<span data-ttu-id="c9054-118">Le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) est l’index de base zéro de la trame où la séquence se termine.</span><span class="sxs-lookup"><span data-stu-id="c9054-118">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is the zero-based index of the frame where playing ends.</span></span> <span data-ttu-id="c9054-119">La valeur doit être inférieure à 65 536.</span><span class="sxs-lookup"><span data-stu-id="c9054-119">The value must be less than 65,536.</span></span> <span data-ttu-id="c9054-120">La valeur-1 signifie qu’elle se termine par la dernière image du clip AVI.</span><span class="sxs-lookup"><span data-stu-id="c9054-120">A value of -1 means end with the last frame in the AVI clip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9054-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c9054-121">Return value</span></span>

<span data-ttu-id="c9054-122">Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="c9054-122">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9054-123">Notes</span><span class="sxs-lookup"><span data-stu-id="c9054-123">Remarks</span></span>

<span data-ttu-id="c9054-124">Vous pouvez utiliser [**Animate \_ Seek**](/windows/desktop/api/Commctrl/nf-commctrl-animate_seek) pour indiquer au contrôle d’animation d’afficher un cadre particulier du clip avi.</span><span class="sxs-lookup"><span data-stu-id="c9054-124">You can use [**Animate\_Seek**](/windows/desktop/api/Commctrl/nf-commctrl-animate_seek) to direct the animation control to display a particular frame of the AVI clip.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9054-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c9054-125">Requirements</span></span>



| <span data-ttu-id="c9054-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c9054-126">Requirement</span></span> | <span data-ttu-id="c9054-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9054-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c9054-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9054-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c9054-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c9054-129">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c9054-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9054-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c9054-131">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c9054-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c9054-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="c9054-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9054-133"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9054-133"><dt>Commctrl.h</dt></span></span> </dl> |



 

