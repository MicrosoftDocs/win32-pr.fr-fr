---
title: Message CBEM_GETIMAGELIST (commctrl. h)
description: Obtient le handle d’une liste d’images assignée à un contrôle ComboBoxEx.
ms.assetid: d577f920-b8f7-4d51-9507-765b7f925408
keywords:
- CBEM_GETIMAGELIST les contrôles de message Windows
topic_type:
- apiref
api_name:
- CBEM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d143b8483fb5fb97ebd65fa2a98640089f6d548
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106518105"
---
# <a name="cbem_getimagelist-message"></a><span data-ttu-id="6765f-104">\_Message CBEM GETIMAGELIST</span><span class="sxs-lookup"><span data-stu-id="6765f-104">CBEM\_GETIMAGELIST message</span></span>

<span data-ttu-id="6765f-105">Obtient le handle d’une liste d’images assignée à un contrôle ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="6765f-105">Gets the handle to an image list assigned to a ComboBoxEx control.</span></span>

## <a name="parameters"></a><span data-ttu-id="6765f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6765f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6765f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6765f-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6765f-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="6765f-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6765f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6765f-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6765f-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="6765f-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6765f-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6765f-111">Return value</span></span>

<span data-ttu-id="6765f-112">Retourne le handle de la liste d’images assignée au contrôle en cas de réussite, ou **null** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="6765f-112">Returns the handle to the image list assigned to the control if successful, or **NULL** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="6765f-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6765f-113">Requirements</span></span>



| <span data-ttu-id="6765f-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6765f-114">Requirement</span></span> | <span data-ttu-id="6765f-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="6765f-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6765f-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6765f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6765f-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6765f-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6765f-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6765f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6765f-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6765f-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6765f-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="6765f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6765f-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6765f-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





