---
title: Message HDM_SETITEM (commctrl. h)
description: Définit les attributs de l’élément spécifié dans un contrôle header. Vous pouvez envoyer ce message explicitement ou utiliser la macro d’en-tête \_ SetItem.
ms.assetid: c8f0d526-3ebe-48c5-8aea-ea3703e2d983
keywords:
- HDM_SETITEM les contrôles de message Windows
topic_type:
- apiref
api_name:
- HDM_SETITEM
- HDM_SETITEMA
- HDM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71b03a05b909cf8c7887edd2031f5346c419f1cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466342"
---
# <a name="hdm_setitem-message"></a><span data-ttu-id="51e78-105">\_Message HDM SETITEM</span><span class="sxs-lookup"><span data-stu-id="51e78-105">HDM\_SETITEM message</span></span>

<span data-ttu-id="51e78-106">Définit les attributs de l’élément spécifié dans un contrôle header.</span><span class="sxs-lookup"><span data-stu-id="51e78-106">Sets the attributes of the specified item in a header control.</span></span> <span data-ttu-id="51e78-107">Vous pouvez envoyer ce message explicitement ou utiliser la macro d' [**en-tête \_ SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_setitem) .</span><span class="sxs-lookup"><span data-stu-id="51e78-107">You can send this message explicitly or use the [**Header\_SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_setitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="51e78-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="51e78-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51e78-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="51e78-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="51e78-110">Index actuel de l’élément dont les attributs doivent être modifiés.</span><span class="sxs-lookup"><span data-stu-id="51e78-110">The current index of the item whose attributes are to be changed.</span></span>

</dd> <dt>

<span data-ttu-id="51e78-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="51e78-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="51e78-112">Pointeur vers une structure [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) qui contient des informations d’élément.</span><span class="sxs-lookup"><span data-stu-id="51e78-112">A pointer to an [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) structure that contains item information.</span></span> <span data-ttu-id="51e78-113">Lorsque ce message est envoyé, le membre de **masque** de la structure doit être défini pour indiquer les attributs qui sont définis.</span><span class="sxs-lookup"><span data-stu-id="51e78-113">When this message is sent, the **mask** member of the structure must be set to indicate which attributes are being set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51e78-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="51e78-114">Return value</span></span>

<span data-ttu-id="51e78-115">Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="51e78-115">Returns nonzero upon success, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="51e78-116">Notes</span><span class="sxs-lookup"><span data-stu-id="51e78-116">Remarks</span></span>

<span data-ttu-id="51e78-117">La structure [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) qui prend en charge ce message prend en charge les informations sur l’ordre des éléments et la liste d’images.</span><span class="sxs-lookup"><span data-stu-id="51e78-117">The [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) structure that supports this message supports item order and image list information.</span></span> <span data-ttu-id="51e78-118">À l’aide de ces membres, vous pouvez contrôler l’ordre dans lequel les éléments sont affichés et spécifier les images à afficher avec les éléments.</span><span class="sxs-lookup"><span data-stu-id="51e78-118">By using these members, you can control the order in which items are displayed and specify images to appear with items.</span></span>

## <a name="requirements"></a><span data-ttu-id="51e78-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="51e78-119">Requirements</span></span>



| <span data-ttu-id="51e78-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="51e78-120">Requirement</span></span> | <span data-ttu-id="51e78-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="51e78-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="51e78-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="51e78-122">Minimum supported client</span></span><br/> | <span data-ttu-id="51e78-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="51e78-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="51e78-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="51e78-124">Minimum supported server</span></span><br/> | <span data-ttu-id="51e78-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="51e78-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="51e78-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="51e78-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="51e78-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="51e78-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="51e78-128">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="51e78-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="51e78-129">**HDM \_ SETITEMW** (Unicode) et **HDM \_ SETITEMA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="51e78-129">**HDM\_SETITEMW** (Unicode) and **HDM\_SETITEMA** (ANSI)</span></span><br/>                   |



 

 





