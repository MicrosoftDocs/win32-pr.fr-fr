---
title: Message HDM_LAYOUT (commctrl. h)
description: Récupère les informations utilisées pour définir la taille et la position du contrôle d’en-tête dans le rectangle cible de la fenêtre parente. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro disposition d’en-tête \_ .
ms.assetid: 0763e483-f01d-4739-8c61-1c52d1aad0b4
keywords:
- HDM_LAYOUT les contrôles de message Windows
topic_type:
- apiref
api_name:
- HDM_LAYOUT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a70fc46dee52f52862136dbe583db9f6d7a0e13e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032890"
---
# <a name="hdm_layout-message"></a><span data-ttu-id="4fe57-105">\_Message de disposition HDM</span><span class="sxs-lookup"><span data-stu-id="4fe57-105">HDM\_LAYOUT message</span></span>

<span data-ttu-id="4fe57-106">Récupère les informations utilisées pour définir la taille et la position du contrôle d’en-tête dans le rectangle cible de la fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="4fe57-106">Retrieves information used to set the size and position of the header control within the target rectangle of the parent window.</span></span> <span data-ttu-id="4fe57-107">Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**\_ disposition d’en-tête**](/windows/desktop/api/Commctrl/nf-commctrl-header_layout) .</span><span class="sxs-lookup"><span data-stu-id="4fe57-107">You can send this message explicitly or use the [**Header\_Layout**](/windows/desktop/api/Commctrl/nf-commctrl-header_layout) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="4fe57-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4fe57-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fe57-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4fe57-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="4fe57-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="4fe57-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="4fe57-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4fe57-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4fe57-112">Pointeur vers une structure [**HDLAYOUT**](/windows/win32/api/commctrl/ns-commctrl-hdlayout) .</span><span class="sxs-lookup"><span data-stu-id="4fe57-112">A pointer to an [**HDLAYOUT**](/windows/win32/api/commctrl/ns-commctrl-hdlayout) structure.</span></span> <span data-ttu-id="4fe57-113">Le membre **PRC** spécifie les coordonnées d’un rectangle, tandis que le membre **pwpos** reçoit la taille et la position du contrôle header dans le rectangle.</span><span class="sxs-lookup"><span data-stu-id="4fe57-113">The **prc** member specifies the coordinates of a rectangle, and the **pwpos** member receives the size and position for the header control within the rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fe57-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4fe57-114">Return value</span></span>

<span data-ttu-id="4fe57-115">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="4fe57-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4fe57-116">Notes</span><span class="sxs-lookup"><span data-stu-id="4fe57-116">Remarks</span></span>

<span data-ttu-id="4fe57-117">Le membre **pwpos** de la structure *lParam* reçoit les valeurs de taille et de position appropriées pour positionner le contrôle le long du bord supérieur du rectangle spécifié.</span><span class="sxs-lookup"><span data-stu-id="4fe57-117">The **pwpos** member of the *lParam* structure receives size and position values appropriate for positioning the control along the top of the specified rectangle.</span></span> <span data-ttu-id="4fe57-118">La valeur de hauteur est la somme des hauteurs des bordures horizontales du contrôle et de la hauteur moyenne des caractères de la police actuellement sélectionnée dans le contexte de périphérique du contrôle.</span><span class="sxs-lookup"><span data-stu-id="4fe57-118">The height value is the sum of the heights of the control's horizontal borders and the average height of characters in the font currently selected into the control's device context.</span></span>

<span data-ttu-id="4fe57-119">Pour utiliser **la \_ disposition HDM** pour définir la taille et la position initiales d’un contrôle header, définissez l’état de visibilité initial du contrôle afin qu’il soit masqué.</span><span class="sxs-lookup"><span data-stu-id="4fe57-119">To use **HDM\_LAYOUT** to set the initial size and position of a header control, set the initial visibility state of the control so that it is hidden.</span></span> <span data-ttu-id="4fe57-120">Après l’envoi de la **\_ disposition HDM** pour récupérer les valeurs de taille et de position, utilisez la fonction [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) pour définir la nouvelle taille, la position et l’état de visibilité.</span><span class="sxs-lookup"><span data-stu-id="4fe57-120">After sending **HDM\_LAYOUT** to retrieve the size and position values, use the [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) function to set the new size, position, and visibility state.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fe57-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4fe57-121">Requirements</span></span>



| <span data-ttu-id="4fe57-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4fe57-122">Requirement</span></span> | <span data-ttu-id="4fe57-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="4fe57-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4fe57-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4fe57-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4fe57-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4fe57-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4fe57-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4fe57-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4fe57-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4fe57-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4fe57-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="4fe57-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="4fe57-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4fe57-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

