---
title: Message TB_SETTOOLTIPS (commctrl. h)
description: Associe un contrôle ToolTip à une barre d’outils.
ms.assetid: a645f1f2-9333-4e25-985a-107cffb9b97f
keywords:
- TB_SETTOOLTIPS les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 781565658d2c362ca32e36736d6e2d80c3641514
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032614"
---
# <a name="tb_settooltips-message"></a><span data-ttu-id="f0e88-104">TO \_ SETTOOLTIPS message</span><span class="sxs-lookup"><span data-stu-id="f0e88-104">TB\_SETTOOLTIPS message</span></span>

<span data-ttu-id="f0e88-105">Associe un contrôle ToolTip à une barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="f0e88-105">Associates a tooltip control with a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="f0e88-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f0e88-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0e88-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f0e88-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f0e88-108">Handle du contrôle ToolTip.</span><span class="sxs-lookup"><span data-stu-id="f0e88-108">Handle to the tooltip control.</span></span>

</dd> <dt>

<span data-ttu-id="f0e88-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f0e88-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f0e88-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="f0e88-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0e88-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f0e88-111">Return value</span></span>

<span data-ttu-id="f0e88-112">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="f0e88-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0e88-113">Notes</span><span class="sxs-lookup"><span data-stu-id="f0e88-113">Remarks</span></span>

<span data-ttu-id="f0e88-114">Les boutons ajoutés à une barre d’outils avant d’envoyer le message **to \_ SETTOOLTIPS** ne sont pas enregistrés avec le contrôle ToolTip.</span><span class="sxs-lookup"><span data-stu-id="f0e88-114">Any buttons added to a toolbar before sending the **TB\_SETTOOLTIPS** message will not be registered with the tooltip control.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0e88-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f0e88-115">Requirements</span></span>



| <span data-ttu-id="f0e88-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f0e88-116">Requirement</span></span> | <span data-ttu-id="f0e88-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="f0e88-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f0e88-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f0e88-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f0e88-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f0e88-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f0e88-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f0e88-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f0e88-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f0e88-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f0e88-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="f0e88-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0e88-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0e88-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





