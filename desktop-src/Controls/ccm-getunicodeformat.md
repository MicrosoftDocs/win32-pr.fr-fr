---
title: Message CCM_GETUNICODEFORMAT (commctrl. h)
description: Obtient l’indicateur de format de caractère Unicode pour le contrôle.
ms.assetid: 8a23cd1c-549e-4d48-891a-b37dbf5c524b
keywords:
- CCM_GETUNICODEFORMAT les contrôles de message Windows
topic_type:
- apiref
api_name:
- CCM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 095d49ccc57faa05e86d12df130b12ce3d542bf6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104515"
---
# <a name="ccm_getunicodeformat-message"></a><span data-ttu-id="a8647-104">\_Message CCM GETUNICODEFORMAT</span><span class="sxs-lookup"><span data-stu-id="a8647-104">CCM\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="a8647-105">Obtient l’indicateur de format de caractère Unicode pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="a8647-105">Gets the Unicode character format flag for the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="a8647-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a8647-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8647-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a8647-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a8647-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="a8647-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="a8647-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a8647-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="a8647-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="a8647-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8647-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a8647-111">Return value</span></span>

<span data-ttu-id="a8647-112">Retourne l’indicateur de format Unicode pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="a8647-112">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="a8647-113">Si cette valeur est différente de zéro, le contrôle utilise des caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="a8647-113">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="a8647-114">Si cette valeur est égale à zéro, le contrôle utilise des caractères ANSI.</span><span class="sxs-lookup"><span data-stu-id="a8647-114">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8647-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a8647-115">Requirements</span></span>



| <span data-ttu-id="a8647-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a8647-116">Requirement</span></span> | <span data-ttu-id="a8647-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="a8647-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a8647-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8647-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a8647-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a8647-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a8647-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8647-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a8647-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a8647-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a8647-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="a8647-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8647-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8647-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8647-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8647-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8647-125">**CCM \_ SETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="a8647-125">**CCM\_SETUNICODEFORMAT**</span></span>](ccm-setunicodeformat.md)
</dt> </dl>

 

 





