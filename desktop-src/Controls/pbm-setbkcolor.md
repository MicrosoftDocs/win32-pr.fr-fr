---
title: Message PBM_SETBKCOLOR (commctrl. h)
description: Définit la couleur d’arrière-plan dans la barre de progression.
ms.assetid: e28af958-babb-4c2e-9202-89b608c22f8e
keywords:
- PBM_SETBKCOLOR les contrôles de message Windows
topic_type:
- apiref
api_name:
- PBM_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ddfaf84695221cf998275d76a9d2d67773150da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742540"
---
# <a name="pbm_setbkcolor-message"></a><span data-ttu-id="2c22c-104">\_Message PBM SETBKCOLOR</span><span class="sxs-lookup"><span data-stu-id="2c22c-104">PBM\_SETBKCOLOR message</span></span>

<span data-ttu-id="2c22c-105">Définit la couleur d’arrière-plan dans la barre de progression.</span><span class="sxs-lookup"><span data-stu-id="2c22c-105">Sets the background color in the progress bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="2c22c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2c22c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c22c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2c22c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2c22c-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="2c22c-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="2c22c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2c22c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2c22c-110">Valeur **COLORREF** qui spécifie la nouvelle couleur d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="2c22c-110">**COLORREF** value that specifies the new background color.</span></span> <span data-ttu-id="2c22c-111">Spécifiez la \_ valeur CLR par défaut pour faire en sorte que la barre de progression utilise sa couleur d’arrière-plan par défaut.</span><span class="sxs-lookup"><span data-stu-id="2c22c-111">Specify the CLR\_DEFAULT value to cause the progress bar to use its default background color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c22c-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2c22c-112">Return value</span></span>

<span data-ttu-id="2c22c-113">Retourne la couleur d’arrière-plan précédente ou la \_ valeur CLR par défaut si la couleur d’arrière-plan est la couleur par défaut.</span><span class="sxs-lookup"><span data-stu-id="2c22c-113">Returns the previous background color, or CLR\_DEFAULT if the background color is the default color.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c22c-114">Notes</span><span class="sxs-lookup"><span data-stu-id="2c22c-114">Remarks</span></span>

<span data-ttu-id="2c22c-115">Lorsque les styles visuels sont activés, ce message n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="2c22c-115">When visual styles are enabled, this message has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c22c-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2c22c-116">Requirements</span></span>



| <span data-ttu-id="2c22c-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2c22c-117">Requirement</span></span> | <span data-ttu-id="2c22c-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="2c22c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2c22c-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c22c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2c22c-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2c22c-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2c22c-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c22c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2c22c-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2c22c-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2c22c-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="2c22c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c22c-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c22c-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





