---
title: Message HKM_GETHOTKEY (commctrl. h)
description: Obtient le code de touche virtuel et les indicateurs de modificateur d’une touche d’accès rapide à partir d’un contrôle de touche d’accès rapide.
ms.assetid: 8b061411-604d-46ea-a082-3eca2d47d992
keywords:
- HKM_GETHOTKEY les contrôles de message Windows
topic_type:
- apiref
api_name:
- HKM_GETHOTKEY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16e23e02f32a4dd6f82f61fd735688353f48ec19
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465043"
---
# <a name="hkm_gethotkey-message"></a><span data-ttu-id="0c4ff-104">\_Message hkm GETHOTKEY</span><span class="sxs-lookup"><span data-stu-id="0c4ff-104">HKM\_GETHOTKEY message</span></span>

<span data-ttu-id="0c4ff-105">Obtient le code de touche virtuel et les indicateurs de modificateur d’une touche d’accès rapide à partir d’un contrôle de touche d’accès rapide.</span><span class="sxs-lookup"><span data-stu-id="0c4ff-105">Gets the virtual key code and modifier flags of a hot key from a hot key control.</span></span>

## <a name="parameters"></a><span data-ttu-id="0c4ff-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0c4ff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c4ff-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0c4ff-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0c4ff-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="0c4ff-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0c4ff-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0c4ff-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="0c4ff-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="0c4ff-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c4ff-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0c4ff-111">Return value</span></span>

<span data-ttu-id="0c4ff-112">Retourne le code de touche virtuel et les indicateurs de modificateur.</span><span class="sxs-lookup"><span data-stu-id="0c4ff-112">Returns the virtual key code and modifier flags.</span></span> <span data-ttu-id="0c4ff-113">Le [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) du [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) est le code de la touche virtuelle de la touche d’accès rapide.</span><span class="sxs-lookup"><span data-stu-id="0c4ff-113">The [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) of the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is the virtual key code of the hot key.</span></span> <span data-ttu-id="0c4ff-114">Le [**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) du **LOWORD** est le modificateur de clé qui spécifie les clés qui définissent une combinaison de touches d’accès rapide.</span><span class="sxs-lookup"><span data-stu-id="0c4ff-114">The [**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) of the **LOWORD** is the key modifier that specifies the keys that define a hot key combination.</span></span> <span data-ttu-id="0c4ff-115">Les indicateurs de modificateur peuvent être une combinaison des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="0c4ff-115">The modifier flags can be a combination of the following values.</span></span>



| <span data-ttu-id="0c4ff-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="0c4ff-116">Value</span></span>            | <span data-ttu-id="0c4ff-117">Signification</span><span class="sxs-lookup"><span data-stu-id="0c4ff-117">Meaning</span></span>      |
|------------------|--------------|
| <span data-ttu-id="0c4ff-118">HOTKEYF \_ ALT</span><span class="sxs-lookup"><span data-stu-id="0c4ff-118">HOTKEYF\_ALT</span></span>     | <span data-ttu-id="0c4ff-119">touche ALT</span><span class="sxs-lookup"><span data-stu-id="0c4ff-119">ALT key</span></span>      |
| <span data-ttu-id="0c4ff-120">\_contrôle HOTKEYF</span><span class="sxs-lookup"><span data-stu-id="0c4ff-120">HOTKEYF\_CONTROL</span></span> | <span data-ttu-id="0c4ff-121">Clé de contrôle</span><span class="sxs-lookup"><span data-stu-id="0c4ff-121">CONTROL key</span></span>  |
| <span data-ttu-id="0c4ff-122">HOTKEYF \_ ext</span><span class="sxs-lookup"><span data-stu-id="0c4ff-122">HOTKEYF\_EXT</span></span>     | <span data-ttu-id="0c4ff-123">Clé étendue</span><span class="sxs-lookup"><span data-stu-id="0c4ff-123">Extended key</span></span> |
| <span data-ttu-id="0c4ff-124">HOTKEYF \_ Shift</span><span class="sxs-lookup"><span data-stu-id="0c4ff-124">HOTKEYF\_SHIFT</span></span>   | <span data-ttu-id="0c4ff-125">Touche Maj</span><span class="sxs-lookup"><span data-stu-id="0c4ff-125">SHIFT key</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="0c4ff-126">Notes</span><span class="sxs-lookup"><span data-stu-id="0c4ff-126">Remarks</span></span>

<span data-ttu-id="0c4ff-127">La valeur 16 bits retournée par ce message peut être utilisée comme paramètre *wParam* dans le message [**WM \_ SETHOTKEY**](/windows/desktop/inputdev/wm-sethotkey) .</span><span class="sxs-lookup"><span data-stu-id="0c4ff-127">The 16-bit value returned by this message can be used as the *wParam* parameter in the [**WM\_SETHOTKEY**](/windows/desktop/inputdev/wm-sethotkey) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c4ff-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0c4ff-128">Requirements</span></span>



| <span data-ttu-id="0c4ff-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0c4ff-129">Requirement</span></span> | <span data-ttu-id="0c4ff-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="0c4ff-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0c4ff-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0c4ff-131">Minimum supported client</span></span><br/> | <span data-ttu-id="0c4ff-132">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0c4ff-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0c4ff-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0c4ff-133">Minimum supported server</span></span><br/> | <span data-ttu-id="0c4ff-134">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0c4ff-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0c4ff-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="0c4ff-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c4ff-136"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c4ff-136"><dt>Commctrl.h</dt></span></span> </dl> |



 

