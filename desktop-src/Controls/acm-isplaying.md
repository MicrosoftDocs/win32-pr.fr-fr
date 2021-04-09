---
title: Message ACM_ISPLAYING (commctrl. h)
description: Vérifie si un clip Audio-Video entrelacé (AVI) est lu. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro animer \_ IsPlaying.
ms.assetid: ebb0c92a-99d2-49c1-9de1-8bdbd032be3a
keywords:
- ACM_ISPLAYING les contrôles de message Windows
topic_type:
- apiref
api_name:
- ACM_ISPLAYING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f663872ce02b9520e3e033cb5bc5a3da12bb3c3c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032569"
---
# <a name="acm_isplaying-message"></a><span data-ttu-id="6c20f-105">\_Message ISPLAYING ACM</span><span class="sxs-lookup"><span data-stu-id="6c20f-105">ACM\_ISPLAYING message</span></span>

<span data-ttu-id="6c20f-106">Vérifie si un clip Audio-Video entrelacé (AVI) est lu.</span><span class="sxs-lookup"><span data-stu-id="6c20f-106">Checks whether an Audio-Video Interleaved (AVI) clip is playing.</span></span> <span data-ttu-id="6c20f-107">Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**animer \_ IsPlaying**](/windows/desktop/api/Commctrl/nf-commctrl-animate_isplaying) .</span><span class="sxs-lookup"><span data-stu-id="6c20f-107">You can send this message explicitly or use the [**Animate\_IsPlaying**](/windows/desktop/api/Commctrl/nf-commctrl-animate_isplaying) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6c20f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6c20f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c20f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6c20f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c20f-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="6c20f-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="6c20f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6c20f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c20f-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="6c20f-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c20f-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6c20f-113">Return value</span></span>

<span data-ttu-id="6c20f-114">Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="6c20f-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c20f-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6c20f-115">Requirements</span></span>



| <span data-ttu-id="6c20f-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6c20f-116">Requirement</span></span> | <span data-ttu-id="6c20f-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="6c20f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6c20f-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6c20f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6c20f-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6c20f-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6c20f-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6c20f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6c20f-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6c20f-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6c20f-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="6c20f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c20f-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c20f-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





