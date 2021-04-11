---
title: Message RB_SETWINDOWTHEME (commctrl. h)
description: Définit le style visuel d’un contrôle rebar.
ms.assetid: 5b32b354-3e25-4d02-9334-cc57acf41a73
keywords:
- RB_SETWINDOWTHEME les contrôles de message Windows
topic_type:
- apiref
api_name:
- RB_SETWINDOWTHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e136562394d26dd56d8d4c0c9ae916948144dbb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104779"
---
# <a name="rb_setwindowtheme-message"></a><span data-ttu-id="997bc-104">\_Message SETWINDOWTHEME RB</span><span class="sxs-lookup"><span data-stu-id="997bc-104">RB\_SETWINDOWTHEME message</span></span>

<span data-ttu-id="997bc-105">Définit le style visuel d’un contrôle rebar.</span><span class="sxs-lookup"><span data-stu-id="997bc-105">Sets the visual style of a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="997bc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="997bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="997bc-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="997bc-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="997bc-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="997bc-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="997bc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="997bc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="997bc-110">Pointeur vers une chaîne Unicode qui contient le style visuel rebar à définir.</span><span class="sxs-lookup"><span data-stu-id="997bc-110">Pointer to a Unicode string that contains the rebar visual style to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="997bc-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="997bc-111">Return value</span></span>

<span data-ttu-id="997bc-112">La valeur de retour n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="997bc-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="997bc-113">Notes</span><span class="sxs-lookup"><span data-stu-id="997bc-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="997bc-114">Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="997bc-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="997bc-115">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="997bc-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="997bc-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="997bc-116">Requirements</span></span>



| <span data-ttu-id="997bc-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="997bc-117">Requirement</span></span> | <span data-ttu-id="997bc-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="997bc-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="997bc-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="997bc-119">Minimum supported client</span></span><br/> | <span data-ttu-id="997bc-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="997bc-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="997bc-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="997bc-121">Minimum supported server</span></span><br/> | <span data-ttu-id="997bc-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="997bc-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="997bc-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="997bc-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="997bc-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="997bc-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





