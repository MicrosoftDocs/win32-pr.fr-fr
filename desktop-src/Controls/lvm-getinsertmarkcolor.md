---
title: Message LVM_GETINSERTMARKCOLOR (commctrl. h)
description: Récupère la couleur du point d’insertion.
ms.assetid: 1e98023a-9d26-4b87-bee4-bee4939ccfca
keywords:
- LVM_GETINSERTMARKCOLOR les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b18d6e9ed277f447f5097c0954819029d24b9cbb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106678"
---
# <a name="lvm_getinsertmarkcolor-message"></a><span data-ttu-id="7c069-104">\_Message GETINSERTMARKCOLOR LVM</span><span class="sxs-lookup"><span data-stu-id="7c069-104">LVM\_GETINSERTMARKCOLOR message</span></span>

<span data-ttu-id="7c069-105">Récupère la couleur du point d’insertion.</span><span class="sxs-lookup"><span data-stu-id="7c069-105">Retrieves the color of the insertion point.</span></span>

## <a name="parameters"></a><span data-ttu-id="7c069-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7c069-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c069-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7c069-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="7c069-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="7c069-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="7c069-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7c069-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="7c069-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="7c069-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c069-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7c069-111">Return value</span></span>

<span data-ttu-id="7c069-112">Retourne une structure **COLORREF** qui contient la couleur du point d’insertion.</span><span class="sxs-lookup"><span data-stu-id="7c069-112">Returns a **COLORREF** structure that contains the color of the insertion point.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c069-113">Notes</span><span class="sxs-lookup"><span data-stu-id="7c069-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7c069-114">Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="7c069-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="7c069-115">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7c069-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7c069-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7c069-116">Requirements</span></span>



| <span data-ttu-id="7c069-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7c069-117">Requirement</span></span> | <span data-ttu-id="7c069-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c069-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7c069-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c069-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7c069-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7c069-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7c069-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c069-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7c069-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7c069-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7c069-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="7c069-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c069-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c069-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





