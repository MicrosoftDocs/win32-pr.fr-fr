---
title: Message HDM_SETORDERARRAY (commctrl. h)
description: Définit l’ordre de gauche à droite des éléments d’en-tête. Vous pouvez envoyer ce message explicitement ou utiliser la macro d’en-tête \_ SetOrderArray.
ms.assetid: 094c424f-10bd-484d-8236-937811b703a6
keywords:
- HDM_SETORDERARRAY les contrôles de message Windows
topic_type:
- apiref
api_name:
- HDM_SETORDERARRAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f07874bfc102babec18b142a087b14e330044ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465479"
---
# <a name="hdm_setorderarray-message"></a><span data-ttu-id="d1565-105">\_Message HDM SETORDERARRAY</span><span class="sxs-lookup"><span data-stu-id="d1565-105">HDM\_SETORDERARRAY message</span></span>

<span data-ttu-id="d1565-106">Définit l’ordre de gauche à droite des éléments d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="d1565-106">Sets the left-to-right order of header items.</span></span> <span data-ttu-id="d1565-107">Vous pouvez envoyer ce message explicitement ou utiliser la macro d' [**en-tête \_ SetOrderArray**](/windows/desktop/api/Commctrl/nf-commctrl-header_setorderarray) .</span><span class="sxs-lookup"><span data-stu-id="d1565-107">You can send this message explicitly or use the [**Header\_SetOrderArray**](/windows/desktop/api/Commctrl/nf-commctrl-header_setorderarray) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d1565-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d1565-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1565-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d1565-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d1565-110">Taille de la mémoire tampon au niveau de *lParam*, dans les éléments.</span><span class="sxs-lookup"><span data-stu-id="d1565-110">The size of the buffer at *lParam*, in elements.</span></span> <span data-ttu-id="d1565-111">Cette valeur doit être égale à la valeur retournée par [**HDM \_ GETITEMCOUNT**](hdm-getitemcount.md).</span><span class="sxs-lookup"><span data-stu-id="d1565-111">This value must equal the value returned by [**HDM\_GETITEMCOUNT**](hdm-getitemcount.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1565-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d1565-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d1565-113">Pointeur vers un tableau qui spécifie l’ordre dans lequel les éléments doivent être affichés, de gauche à droite.</span><span class="sxs-lookup"><span data-stu-id="d1565-113">A pointer to an array that specifies the order in which items should be displayed, from left to right.</span></span> <span data-ttu-id="d1565-114">Par exemple, si le contenu du tableau est {2,0,1} , le contrôle affiche l’élément 2, l’élément 0 et l’élément 1, de gauche à droite.</span><span class="sxs-lookup"><span data-stu-id="d1565-114">For example, if the contents of the array are {2,0,1}, the control displays item 2, item 0, and item 1, from left to right.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1565-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d1565-115">Return value</span></span>

<span data-ttu-id="d1565-116">Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="d1565-116">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1565-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d1565-117">Requirements</span></span>



| <span data-ttu-id="d1565-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d1565-118">Requirement</span></span> | <span data-ttu-id="d1565-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1565-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d1565-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1565-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d1565-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d1565-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d1565-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1565-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d1565-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d1565-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d1565-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="d1565-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1565-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1565-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





