---
title: Message TB_ISBUTTONHIGHLIGHTED (commctrl. h)
description: Vérifie l’état de mise en surbrillance d’un bouton de barre d’outils.
ms.assetid: d5aab670-a989-46f2-b4f8-d8a8968cbe07
keywords:
- TB_ISBUTTONHIGHLIGHTED les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_ISBUTTONHIGHLIGHTED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f53e25058fee8fa5dcac218a641277ac46aed4e7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032616"
---
# <a name="tb_isbuttonhighlighted-message"></a><span data-ttu-id="0aa6d-104">TO \_ ISBUTTONHIGHLIGHTED message</span><span class="sxs-lookup"><span data-stu-id="0aa6d-104">TB\_ISBUTTONHIGHLIGHTED message</span></span>

<span data-ttu-id="0aa6d-105">Vérifie l’état de mise en surbrillance d’un bouton de barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="0aa6d-105">Checks the highlight state of a toolbar button.</span></span>

## <a name="parameters"></a><span data-ttu-id="0aa6d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0aa6d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0aa6d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0aa6d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0aa6d-108">Identificateur de commande pour un bouton de barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="0aa6d-108">Command identifier for a toolbar button.</span></span>

</dd> <dt>

<span data-ttu-id="0aa6d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0aa6d-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="0aa6d-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="0aa6d-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0aa6d-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0aa6d-111">Return value</span></span>

<span data-ttu-id="0aa6d-112">Retourne une valeur différente de zéro si le bouton est mis en surbrillance, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="0aa6d-112">Returns nonzero if the button is highlighted, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="0aa6d-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0aa6d-113">Requirements</span></span>



| <span data-ttu-id="0aa6d-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0aa6d-114">Requirement</span></span> | <span data-ttu-id="0aa6d-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="0aa6d-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0aa6d-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0aa6d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0aa6d-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0aa6d-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0aa6d-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0aa6d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0aa6d-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0aa6d-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0aa6d-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="0aa6d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0aa6d-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0aa6d-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





