---
title: Message CCM_SETWINDOWTHEME (commctrl. h)
description: Définit le style visuel d’un contrôle.
ms.assetid: 0200fa11-847f-477c-92e0-790b4d1ca0ef
keywords:
- CCM_SETWINDOWTHEME les contrôles de message Windows
topic_type:
- apiref
api_name:
- CCM_SETWINDOWTHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cea8996273a0c9d03123ce58f5fbb0dfb099be94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465918"
---
# <a name="ccm_setwindowtheme-message"></a><span data-ttu-id="928ae-104">\_Message CCM SETWINDOWTHEME</span><span class="sxs-lookup"><span data-stu-id="928ae-104">CCM\_SETWINDOWTHEME message</span></span>

<span data-ttu-id="928ae-105">Définit le style visuel d’un contrôle.</span><span class="sxs-lookup"><span data-stu-id="928ae-105">Sets the visual style of a control.</span></span>

## <a name="parameters"></a><span data-ttu-id="928ae-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="928ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="928ae-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="928ae-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="928ae-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="928ae-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="928ae-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="928ae-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="928ae-110">Pointeur vers une chaîne Unicode qui contient le style visuel de contrôle à définir.</span><span class="sxs-lookup"><span data-stu-id="928ae-110">A pointer to a Unicode string that contains the control visual style to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="928ae-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="928ae-111">Return value</span></span>

<span data-ttu-id="928ae-112">La valeur de retour n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="928ae-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="928ae-113">Notes</span><span class="sxs-lookup"><span data-stu-id="928ae-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="928ae-114">Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="928ae-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="928ae-115">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="928ae-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="928ae-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="928ae-116">Requirements</span></span>



| <span data-ttu-id="928ae-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="928ae-117">Requirement</span></span> | <span data-ttu-id="928ae-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="928ae-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="928ae-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="928ae-119">Minimum supported client</span></span><br/> | <span data-ttu-id="928ae-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="928ae-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="928ae-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="928ae-121">Minimum supported server</span></span><br/> | <span data-ttu-id="928ae-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="928ae-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="928ae-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="928ae-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="928ae-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="928ae-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





