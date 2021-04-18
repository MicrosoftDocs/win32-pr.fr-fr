---
title: Message CBEM_SETWINDOWTHEME (commctrl. h)
description: Définit le style visuel d’un contrôle ComboBoxEx.
ms.assetid: 064f9a24-42be-42f4-bee3-e7320fe8c366
keywords:
- CBEM_SETWINDOWTHEME les contrôles de message Windows
topic_type:
- apiref
api_name:
- CBEM_SETWINDOWTHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cda1e5c46bb6216c413737c44b5785ac26925f6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511770"
---
# <a name="cbem_setwindowtheme-message"></a><span data-ttu-id="65287-104">\_Message CBEM SETWINDOWTHEME</span><span class="sxs-lookup"><span data-stu-id="65287-104">CBEM\_SETWINDOWTHEME message</span></span>

<span data-ttu-id="65287-105">Définit le style visuel d’un contrôle ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="65287-105">Sets the visual style of a ComboBoxEx control.</span></span>

## <a name="parameters"></a><span data-ttu-id="65287-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="65287-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65287-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="65287-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="65287-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="65287-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="65287-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="65287-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="65287-110">Pointeur vers une chaîne Unicode qui contient le style visuel de contrôle à définir.</span><span class="sxs-lookup"><span data-stu-id="65287-110">A pointer to a Unicode string that contains the control visual style to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65287-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="65287-111">Return value</span></span>

<span data-ttu-id="65287-112">La valeur de retour n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="65287-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="65287-113">Notes</span><span class="sxs-lookup"><span data-stu-id="65287-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="65287-114">Pour utiliser ce message, vous devez fournir un manifeste spécifiant la version 6,0 de Comclt32.</span><span class="sxs-lookup"><span data-stu-id="65287-114">To use this message, you must provide a manifest specifying Comclt32 version 6.0.</span></span> <span data-ttu-id="65287-115">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="65287-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="65287-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="65287-116">Requirements</span></span>



| <span data-ttu-id="65287-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="65287-117">Requirement</span></span> | <span data-ttu-id="65287-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="65287-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="65287-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65287-119">Minimum supported client</span></span><br/> | <span data-ttu-id="65287-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="65287-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="65287-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65287-121">Minimum supported server</span></span><br/> | <span data-ttu-id="65287-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="65287-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="65287-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="65287-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="65287-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="65287-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





