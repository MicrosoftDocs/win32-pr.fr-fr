---
title: Message HDM_ORDERTOINDEX (commctrl. h)
description: Récupère une valeur d’index pour un élément en fonction de son ordre dans le contrôle d’en-tête. Vous pouvez envoyer ce message explicitement ou utiliser la macro d’en-tête \_ OrderToIndex.
ms.assetid: vs|controls|~\controls\header\messages\hdm_ordertoindex.htm
keywords:
- HDM_ORDERTOINDEX les contrôles de message Windows
topic_type:
- apiref
api_name:
- HDM_ORDERTOINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b65d10fb27c9a07639ebbd5770a53d72cbf0aba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032796"
---
# <a name="hdm_ordertoindex-message"></a><span data-ttu-id="367bf-105">\_Message HDM ORDERTOINDEX</span><span class="sxs-lookup"><span data-stu-id="367bf-105">HDM\_ORDERTOINDEX message</span></span>

<span data-ttu-id="367bf-106">Récupère une valeur d’index pour un élément en fonction de son ordre dans le contrôle d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="367bf-106">Retrieves an index value for an item based on its order in the header control.</span></span> <span data-ttu-id="367bf-107">Vous pouvez envoyer ce message explicitement ou utiliser la macro d' [**en-tête \_ OrderToIndex**](/windows/desktop/api/Commctrl/nf-commctrl-header_ordertoindex) .</span><span class="sxs-lookup"><span data-stu-id="367bf-107">You can send this message explicitly or use the [**Header\_OrderToIndex**](/windows/desktop/api/Commctrl/nf-commctrl-header_ordertoindex) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="367bf-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="367bf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="367bf-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="367bf-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="367bf-110">Ordre dans lequel l’élément apparaît dans le contrôle d’en-tête, de gauche à droite.</span><span class="sxs-lookup"><span data-stu-id="367bf-110">The order in which the item appears within the header control, from left to right.</span></span> <span data-ttu-id="367bf-111">Par exemple, la valeur d’index de l’élément dans la colonne la plus à gauche serait 0.</span><span class="sxs-lookup"><span data-stu-id="367bf-111">For example, the index value of the item in the far left column would be 0.</span></span> <span data-ttu-id="367bf-112">La valeur de l’élément suivant à droite est 1, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="367bf-112">The value for the next item to the right would be 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="367bf-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="367bf-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="367bf-114">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="367bf-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="367bf-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="367bf-115">Return value</span></span>

<span data-ttu-id="367bf-116">Retourne INT qui indique l’index de l’élément.</span><span class="sxs-lookup"><span data-stu-id="367bf-116">Returns INT that indicates the item index.</span></span> <span data-ttu-id="367bf-117">Si *wParam* n’est pas valide (valeur négative ou trop grande), le retour est égal à *wParam*.</span><span class="sxs-lookup"><span data-stu-id="367bf-117">If *wParam* is invalid (negative or too large), the return equals *wParam*.</span></span>

## <a name="requirements"></a><span data-ttu-id="367bf-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="367bf-118">Requirements</span></span>



| <span data-ttu-id="367bf-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="367bf-119">Requirement</span></span> | <span data-ttu-id="367bf-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="367bf-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="367bf-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="367bf-121">Minimum supported client</span></span><br/> | <span data-ttu-id="367bf-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="367bf-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="367bf-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="367bf-123">Minimum supported server</span></span><br/> | <span data-ttu-id="367bf-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="367bf-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="367bf-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="367bf-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="367bf-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="367bf-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





