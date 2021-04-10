---
title: Message TBM_GETBUDDY (commctrl. h)
description: Récupère le handle d’une fenêtre associée du contrôle TrackBar à un emplacement donné. L’emplacement spécifié est relatif à l’orientation du contrôle (horizontale ou verticale).
ms.assetid: 69e4e467-150d-4505-b1c2-2ed9dd83f1a6
keywords:
- TBM_GETBUDDY les contrôles de message Windows
topic_type:
- apiref
api_name:
- TBM_GETBUDDY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4c076f001a1dff62541c3aa32bc12744b30c012
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942905"
---
# <a name="tbm_getbuddy-message"></a><span data-ttu-id="6c60d-105">\_Message TBM GETBUDDY</span><span class="sxs-lookup"><span data-stu-id="6c60d-105">TBM\_GETBUDDY message</span></span>

<span data-ttu-id="6c60d-106">Récupère le handle d’une fenêtre associée du contrôle TrackBar à un emplacement donné.</span><span class="sxs-lookup"><span data-stu-id="6c60d-106">Retrieves the handle to a trackbar control buddy window at a given location.</span></span> <span data-ttu-id="6c60d-107">L’emplacement spécifié est relatif à l’orientation du contrôle (horizontale ou verticale).</span><span class="sxs-lookup"><span data-stu-id="6c60d-107">The specified location is relative to the control's orientation (horizontal or vertical).</span></span>

## <a name="parameters"></a><span data-ttu-id="6c60d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6c60d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c60d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6c60d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c60d-110">Valeur indiquant le descripteur de fenêtre associée qui sera récupéré, par emplacement relatif.</span><span class="sxs-lookup"><span data-stu-id="6c60d-110">Value indicating which buddy window handle will be retrieved, by relative location.</span></span> <span data-ttu-id="6c60d-111">Cette valeur peut être l'une des suivantes :</span><span class="sxs-lookup"><span data-stu-id="6c60d-111">This value can be one of the following:</span></span>



| <span data-ttu-id="6c60d-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="6c60d-112">Value</span></span>                                                                                                                                    | <span data-ttu-id="6c60d-113">Signification</span><span class="sxs-lookup"><span data-stu-id="6c60d-113">Meaning</span></span>                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <span data-ttu-id="6c60d-114"><dt>VRAI \* \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="6c60d-114"><dt>\*\*\*\*TRUE\*\*\*\*</dt></span></span> </dl>    | <span data-ttu-id="6c60d-115">Récupère le handle de l’ami à gauche du TrackBar.</span><span class="sxs-lookup"><span data-stu-id="6c60d-115">Retrieves the handle to the buddy to the left of the trackbar.</span></span> <span data-ttu-id="6c60d-116">Si le contrôle TrackBar utilise le style [**tbs \_ vert**](trackbar-control-styles.md) , le message récupère l’ami au-dessus du TrackBar.</span><span class="sxs-lookup"><span data-stu-id="6c60d-116">If the trackbar control uses the [**TBS\_VERT**](trackbar-control-styles.md) style, the message will retrieve the buddy above the trackbar.</span></span><br/>  |
| <span id="FALSE"></span><span id="false"></span><dl> <span data-ttu-id="6c60d-117"><dt>FALSe \* \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="6c60d-117"><dt>\*\*\*\*FALSE\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="6c60d-118">Récupère le handle de l’ami à droite du TrackBar.</span><span class="sxs-lookup"><span data-stu-id="6c60d-118">Retrieves the handle to the buddy to the right of the trackbar.</span></span> <span data-ttu-id="6c60d-119">Si le contrôle TrackBar utilise le style [**tbs \_ vert**](trackbar-control-styles.md) , le message récupère l’ami sous le TrackBar.</span><span class="sxs-lookup"><span data-stu-id="6c60d-119">If the trackbar control uses the [**TBS\_VERT**](trackbar-control-styles.md) style, the message will retrieve the buddy below the trackbar.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6c60d-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6c60d-120">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6c60d-121">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="6c60d-121">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c60d-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6c60d-122">Return value</span></span>

<span data-ttu-id="6c60d-123">Retourne le handle de la fenêtre associée à l’emplacement spécifié par *wParam*, ou **null** si aucune fenêtre associée n’existe à cet emplacement.</span><span class="sxs-lookup"><span data-stu-id="6c60d-123">Returns the handle to the buddy window at the location specified by *wParam*, or **NULL** if no buddy window exists at that location.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c60d-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6c60d-124">Requirements</span></span>



| <span data-ttu-id="6c60d-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6c60d-125">Requirement</span></span> | <span data-ttu-id="6c60d-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="6c60d-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6c60d-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6c60d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6c60d-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6c60d-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6c60d-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6c60d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6c60d-130">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6c60d-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6c60d-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="6c60d-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c60d-132"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c60d-132"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





