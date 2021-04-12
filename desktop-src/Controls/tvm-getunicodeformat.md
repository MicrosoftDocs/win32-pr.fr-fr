---
title: Message TVM_GETUNICODEFORMAT (commctrl. h)
description: Récupère l’indicateur de format de caractère Unicode pour le contrôle. Vous pouvez envoyer ce message explicitement ou utiliser la \_ macro GetUnicodeFormat TreeView.
ms.assetid: d95f61b6-9ec1-4471-b24b-efe141428747
keywords:
- TVM_GETUNICODEFORMAT les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88478d30e8da98ebf2e2325d6152087a14bc066a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032599"
---
# <a name="tvm_getunicodeformat-message"></a><span data-ttu-id="cfcb6-105">TVM \_ GETUNICODEFORMAT message</span><span class="sxs-lookup"><span data-stu-id="cfcb6-105">TVM\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="cfcb6-106">Récupère l’indicateur de format de caractère Unicode pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="cfcb6-106">Retrieves the Unicode character format flag for the control.</span></span> <span data-ttu-id="cfcb6-107">Vous pouvez envoyer ce message explicitement ou utiliser la [**macro \_ GetUnicodeFormat TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getunicodeformat) .</span><span class="sxs-lookup"><span data-stu-id="cfcb6-107">You can send this message explicitly or use the [**TreeView\_GetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getunicodeformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="cfcb6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cfcb6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfcb6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cfcb6-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="cfcb6-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="cfcb6-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="cfcb6-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cfcb6-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="cfcb6-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="cfcb6-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfcb6-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cfcb6-113">Return value</span></span>

<span data-ttu-id="cfcb6-114">Retourne l’indicateur de format Unicode pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="cfcb6-114">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="cfcb6-115">Si cette valeur est différente de zéro, le contrôle utilise des caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="cfcb6-115">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="cfcb6-116">Si cette valeur est égale à zéro, le contrôle utilise des caractères ANSI.</span><span class="sxs-lookup"><span data-stu-id="cfcb6-116">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfcb6-117">Notes</span><span class="sxs-lookup"><span data-stu-id="cfcb6-117">Remarks</span></span>

<span data-ttu-id="cfcb6-118">Pour plus d’informations sur ce message, consultez les notes relatives à [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="cfcb6-118">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfcb6-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cfcb6-119">Requirements</span></span>



| <span data-ttu-id="cfcb6-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cfcb6-120">Requirement</span></span> | <span data-ttu-id="cfcb6-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="cfcb6-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cfcb6-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cfcb6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="cfcb6-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cfcb6-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cfcb6-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cfcb6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="cfcb6-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cfcb6-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cfcb6-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="cfcb6-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfcb6-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cfcb6-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfcb6-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cfcb6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfcb6-129">**TVM \_ SETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="cfcb6-129">**TVM\_SETUNICODEFORMAT**</span></span>](tvm-setunicodeformat.md)
</dt> </dl>

 

 





