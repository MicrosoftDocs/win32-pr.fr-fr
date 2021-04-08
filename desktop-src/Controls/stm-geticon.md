---
title: Message STM_GETICON (winuser. h)
description: Une application envoie le \_ message STM GETICON pour récupérer un handle vers l’icône associée à un contrôle statique avec le style d' \_ icône SS.
ms.assetid: e6b0a006-696b-401d-b894-b1db697c8939
keywords:
- STM_GETICON les contrôles de message Windows
topic_type:
- apiref
api_name:
- STM_GETICON
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f64f55d2a2f8315b99526e51a69891f6f0056e8b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103125"
---
# <a name="stm_geticon-message"></a><span data-ttu-id="4a8b9-104">\_Message GETICON STM</span><span class="sxs-lookup"><span data-stu-id="4a8b9-104">STM\_GETICON message</span></span>

<span data-ttu-id="4a8b9-105">Une application envoie le message **STM \_ GETICON** pour récupérer un handle vers l’icône associée à un contrôle statique avec le style d' \_ icône SS.</span><span class="sxs-lookup"><span data-stu-id="4a8b9-105">An application sends the **STM\_GETICON** message to retrieve a handle to the icon associated with a static control that has the SS\_ICON style.</span></span>

## <a name="parameters"></a><span data-ttu-id="4a8b9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4a8b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a8b9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4a8b9-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4a8b9-108">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="4a8b9-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="4a8b9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4a8b9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4a8b9-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="4a8b9-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a8b9-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4a8b9-111">Return value</span></span>

<span data-ttu-id="4a8b9-112">La valeur de retour est un handle de l’icône, ou **null** si le contrôle statique n’a pas d’icône associée ou si une erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="4a8b9-112">The return value is a handle to the icon, or **NULL** if either the static control has no associated icon or if an error occurred.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a8b9-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4a8b9-113">Requirements</span></span>



| <span data-ttu-id="4a8b9-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4a8b9-114">Requirement</span></span> | <span data-ttu-id="4a8b9-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="4a8b9-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a8b9-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4a8b9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4a8b9-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4a8b9-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4a8b9-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4a8b9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4a8b9-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4a8b9-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4a8b9-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="4a8b9-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a8b9-121"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4a8b9-121"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a8b9-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4a8b9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a8b9-123">**\_SETICON STM**</span><span class="sxs-lookup"><span data-stu-id="4a8b9-123">**STM\_SETICON**</span></span>](stm-seticon.md)
</dt> </dl>

 

 





