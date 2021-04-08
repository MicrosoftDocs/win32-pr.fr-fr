---
title: Message IPM_ISBLANK (commctrl. h)
description: Détermine si tous les champs du contrôle d’adresse IP sont vides.
ms.assetid: 6e35b848-943a-4475-890a-01fc3d8ed97d
keywords:
- IPM_ISBLANK les contrôles de message Windows
topic_type:
- apiref
api_name:
- IPM_ISBLANK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19f5a33ee3c35779a02cdfcb0fcb7066098f3160
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843889"
---
# <a name="ipm_isblank-message"></a><span data-ttu-id="7c4c7-104">\_Message IsBlank IPM</span><span class="sxs-lookup"><span data-stu-id="7c4c7-104">IPM\_ISBLANK message</span></span>

<span data-ttu-id="7c4c7-105">Détermine si tous les champs du contrôle d’adresse IP sont vides.</span><span class="sxs-lookup"><span data-stu-id="7c4c7-105">Determines if all fields in the IP address control are blank.</span></span>

## <a name="parameters"></a><span data-ttu-id="7c4c7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7c4c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c4c7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7c4c7-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="7c4c7-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="7c4c7-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="7c4c7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7c4c7-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="7c4c7-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="7c4c7-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c4c7-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7c4c7-111">Return value</span></span>

<span data-ttu-id="7c4c7-112">Retourne une valeur différente de zéro si tous les champs sont vides, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="7c4c7-112">Returns nonzero if all fields are blank, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c4c7-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7c4c7-113">Requirements</span></span>



| <span data-ttu-id="7c4c7-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7c4c7-114">Requirement</span></span> | <span data-ttu-id="7c4c7-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c4c7-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7c4c7-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c4c7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7c4c7-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7c4c7-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7c4c7-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c4c7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7c4c7-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7c4c7-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7c4c7-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="7c4c7-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c4c7-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c4c7-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





