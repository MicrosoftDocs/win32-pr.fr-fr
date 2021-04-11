---
title: Message TB_ISBUTTONINDETERMINATE (commctrl. h)
description: Détermine si le bouton spécifié dans une barre d’outils est indéterminé.
ms.assetid: b4d759b3-cdbc-417b-9da4-4ed9edc38c0e
keywords:
- TB_ISBUTTONINDETERMINATE les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_ISBUTTONINDETERMINATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29fc024efcad9f0f48ae4882b019269903c249bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032615"
---
# <a name="tb_isbuttonindeterminate-message"></a><span data-ttu-id="244b2-104">TO \_ ISBUTTONINDETERMINATE message</span><span class="sxs-lookup"><span data-stu-id="244b2-104">TB\_ISBUTTONINDETERMINATE message</span></span>

<span data-ttu-id="244b2-105">Détermine si le bouton spécifié dans une barre d’outils est indéterminé.</span><span class="sxs-lookup"><span data-stu-id="244b2-105">Determines whether the specified button in a toolbar is indeterminate.</span></span>

## <a name="parameters"></a><span data-ttu-id="244b2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="244b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="244b2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="244b2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="244b2-108">Identificateur de commande du bouton.</span><span class="sxs-lookup"><span data-stu-id="244b2-108">Command identifier of the button.</span></span>

</dd> <dt>

<span data-ttu-id="244b2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="244b2-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="244b2-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="244b2-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="244b2-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="244b2-111">Return value</span></span>

<span data-ttu-id="244b2-112">Retourne une valeur différente de zéro si le bouton est indéterminé, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="244b2-112">Returns nonzero if the button is indeterminate, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="244b2-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="244b2-113">Requirements</span></span>



| <span data-ttu-id="244b2-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="244b2-114">Requirement</span></span> | <span data-ttu-id="244b2-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="244b2-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="244b2-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="244b2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="244b2-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="244b2-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="244b2-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="244b2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="244b2-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="244b2-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="244b2-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="244b2-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="244b2-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="244b2-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





