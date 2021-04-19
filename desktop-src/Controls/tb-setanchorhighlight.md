---
title: Message TB_SETANCHORHIGHLIGHT (commctrl. h)
description: Définit le paramètre de surbrillance d’ancrage pour une barre d’outils.
ms.assetid: d31652d5-e9cf-4bf3-8f90-818eb078fa87
keywords:
- TB_SETANCHORHIGHLIGHT les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_SETANCHORHIGHLIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 809f71e446f7768d637258152db1dd2d56346dfd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106518057"
---
# <a name="tb_setanchorhighlight-message"></a><span data-ttu-id="b8054-104">TO \_ SETANCHORHIGHLIGHT message</span><span class="sxs-lookup"><span data-stu-id="b8054-104">TB\_SETANCHORHIGHLIGHT message</span></span>

<span data-ttu-id="b8054-105">Définit le paramètre de surbrillance d’ancrage pour une barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="b8054-105">Sets the anchor highlight setting for a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="b8054-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b8054-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8054-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b8054-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b8054-108">Valeur **booléenne** qui spécifie si la mise en surbrillance de l’ancre est activée ou désactivée.</span><span class="sxs-lookup"><span data-stu-id="b8054-108">**BOOL** value that specifies if anchor highlighting is enabled or disabled.</span></span> <span data-ttu-id="b8054-109">Si cette valeur est différente de zéro, la mise en surbrillance de l’ancre est activée.</span><span class="sxs-lookup"><span data-stu-id="b8054-109">If this value is nonzero, anchor highlighting will be enabled.</span></span> <span data-ttu-id="b8054-110">Si cette valeur est égale à zéro, la mise en surbrillance de l’ancre est désactivée.</span><span class="sxs-lookup"><span data-stu-id="b8054-110">If this value is zero, anchor highlighting will be disabled.</span></span>

</dd> <dt>

<span data-ttu-id="b8054-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b8054-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b8054-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="b8054-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8054-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b8054-113">Return value</span></span>

<span data-ttu-id="b8054-114">Retourne le paramètre de surbrillance d’ancrage précédent.</span><span class="sxs-lookup"><span data-stu-id="b8054-114">Returns the previous anchor highlight setting.</span></span> <span data-ttu-id="b8054-115">Si cette valeur est différente de zéro, la mise en surbrillance de l’ancre a été activée.</span><span class="sxs-lookup"><span data-stu-id="b8054-115">If this value is nonzero, anchor highlighting was enabled.</span></span> <span data-ttu-id="b8054-116">Si cette valeur est égale à zéro, la mise en surbrillance de l’ancre était désactivée.</span><span class="sxs-lookup"><span data-stu-id="b8054-116">If this value is zero, anchor highlighting was disabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8054-117">Notes</span><span class="sxs-lookup"><span data-stu-id="b8054-117">Remarks</span></span>

<span data-ttu-id="b8054-118">La mise en surbrillance d’ancre dans une barre d’outils signifie que le dernier élément mis en surbrillance reste en surbrillance jusqu’à ce qu’un autre élément</span><span class="sxs-lookup"><span data-stu-id="b8054-118">Anchor highlighting in a toolbar means that the last highlighted item will remain highlighted until another item is highlighted.</span></span> <span data-ttu-id="b8054-119">Cela se produit même si le curseur quitte le contrôle ToolBar.</span><span class="sxs-lookup"><span data-stu-id="b8054-119">This occurs even if the cursor leaves the toolbar control.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8054-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b8054-120">Requirements</span></span>



| <span data-ttu-id="b8054-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b8054-121">Requirement</span></span> | <span data-ttu-id="b8054-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8054-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b8054-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b8054-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b8054-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b8054-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b8054-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b8054-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b8054-126">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b8054-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b8054-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="b8054-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8054-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8054-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





