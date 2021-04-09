---
title: Message TB_GETANCHORHIGHLIGHT (commctrl. h)
description: Récupère le paramètre de surbrillance d’ancrage d’une barre d’outils.
ms.assetid: 167d481c-8684-40eb-9323-cfa238be3643
keywords:
- TB_GETANCHORHIGHLIGHT les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_GETANCHORHIGHLIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bfff5ef1853bbf5657604c673dcc6a9be43af83
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844449"
---
# <a name="tb_getanchorhighlight-message"></a><span data-ttu-id="725fb-104">TO \_ GETANCHORHIGHLIGHT message</span><span class="sxs-lookup"><span data-stu-id="725fb-104">TB\_GETANCHORHIGHLIGHT message</span></span>

<span data-ttu-id="725fb-105">Récupère le paramètre de surbrillance d’ancrage d’une barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="725fb-105">Retrieves the anchor highlight setting for a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="725fb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="725fb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="725fb-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="725fb-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="725fb-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="725fb-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="725fb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="725fb-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="725fb-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="725fb-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="725fb-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="725fb-111">Return value</span></span>

<span data-ttu-id="725fb-112">Retourne une valeur booléenne qui indique si la mise en surbrillance de l’ancre est définie.</span><span class="sxs-lookup"><span data-stu-id="725fb-112">Returns a Boolean value that indicates if anchor highlighting is set.</span></span> <span data-ttu-id="725fb-113">Si cette valeur est différente de zéro, la mise en surbrillance de l’ancre est activée.</span><span class="sxs-lookup"><span data-stu-id="725fb-113">If this value is nonzero, anchor highlighting is enabled.</span></span> <span data-ttu-id="725fb-114">Si cette valeur est égale à zéro, elle est désactivée.</span><span class="sxs-lookup"><span data-stu-id="725fb-114">If this value is zero, it is disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="725fb-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="725fb-115">Requirements</span></span>



| <span data-ttu-id="725fb-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="725fb-116">Requirement</span></span> | <span data-ttu-id="725fb-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="725fb-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="725fb-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="725fb-118">Minimum supported client</span></span><br/> | <span data-ttu-id="725fb-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="725fb-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="725fb-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="725fb-120">Minimum supported server</span></span><br/> | <span data-ttu-id="725fb-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="725fb-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="725fb-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="725fb-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="725fb-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="725fb-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="725fb-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="725fb-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="725fb-125">**TO \_ SETANCHORHIGHLIGHT**</span><span class="sxs-lookup"><span data-stu-id="725fb-125">**TB\_SETANCHORHIGHLIGHT**</span></span>](tb-setanchorhighlight.md)
</dt> </dl>

 

 





