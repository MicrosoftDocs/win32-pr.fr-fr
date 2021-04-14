---
title: Message TTM_SETWINDOWTHEME (commctrl. h)
description: Définit le style visuel d’un contrôle ToolTip.
ms.assetid: eeddb91e-8eb8-4480-9ab2-5efa9e3ef48a
keywords:
- TTM_SETWINDOWTHEME les contrôles de message Windows
topic_type:
- apiref
api_name:
- TTM_SETWINDOWTHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9c3f25b62bf0fe38a679234183cd5046f60784f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509298"
---
# <a name="ttm_setwindowtheme-message"></a><span data-ttu-id="62d6e-104">\_Message atténuation SETWINDOWTHEME</span><span class="sxs-lookup"><span data-stu-id="62d6e-104">TTM\_SETWINDOWTHEME message</span></span>

<span data-ttu-id="62d6e-105">Définit le style visuel d’un contrôle ToolTip.</span><span class="sxs-lookup"><span data-stu-id="62d6e-105">Sets the visual style of a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="62d6e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="62d6e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62d6e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="62d6e-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="62d6e-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="62d6e-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="62d6e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="62d6e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="62d6e-110">Pointeur vers une chaîne Unicode qui contient le style visuel d’info-bulle à définir.</span><span class="sxs-lookup"><span data-stu-id="62d6e-110">Pointer to a Unicode string that contains the tooltip visual style to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62d6e-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="62d6e-111">Return value</span></span>

<span data-ttu-id="62d6e-112">La valeur de retour n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="62d6e-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="62d6e-113">Notes</span><span class="sxs-lookup"><span data-stu-id="62d6e-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="62d6e-114">Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="62d6e-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="62d6e-115">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="62d6e-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="62d6e-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="62d6e-116">Requirements</span></span>



| <span data-ttu-id="62d6e-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="62d6e-117">Requirement</span></span> | <span data-ttu-id="62d6e-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="62d6e-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="62d6e-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="62d6e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="62d6e-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="62d6e-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="62d6e-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="62d6e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="62d6e-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="62d6e-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="62d6e-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="62d6e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="62d6e-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="62d6e-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





