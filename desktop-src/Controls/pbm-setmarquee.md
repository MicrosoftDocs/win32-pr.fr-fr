---
title: Message PBM_SETMARQUEE (commctrl. h)
description: Définit la barre de progression en mode texte défilant. La barre de progression se déplace alors comme un texte défilant.
ms.assetid: 6501bcb9-a711-470f-874f-f3484d3613b6
keywords:
- PBM_SETMARQUEE les contrôles de message Windows
topic_type:
- apiref
api_name:
- PBM_SETMARQUEE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9229291113f034924cf9ce8112c0e99376d37932
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942471"
---
# <a name="pbm_setmarquee-message"></a><span data-ttu-id="ca6de-105">\_Message PBM SETMARQUEE</span><span class="sxs-lookup"><span data-stu-id="ca6de-105">PBM\_SETMARQUEE message</span></span>

<span data-ttu-id="ca6de-106">Définit la barre de progression en mode texte défilant.</span><span class="sxs-lookup"><span data-stu-id="ca6de-106">Sets the progress bar to marquee mode.</span></span> <span data-ttu-id="ca6de-107">La barre de progression se déplace alors comme un texte défilant.</span><span class="sxs-lookup"><span data-stu-id="ca6de-107">This causes the progress bar to move like a marquee.</span></span>

## <a name="parameters"></a><span data-ttu-id="ca6de-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ca6de-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca6de-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ca6de-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ca6de-110">Indique s’il faut activer ou désactiver le mode texte défilant.</span><span class="sxs-lookup"><span data-stu-id="ca6de-110">Indicates whether to turn the marquee mode on or off.</span></span>

</dd> <dt>

<span data-ttu-id="ca6de-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ca6de-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ca6de-112">Durée, en millisecondes, entre les mises à jour de l’animation de texte défilant.</span><span class="sxs-lookup"><span data-stu-id="ca6de-112">Time, in milliseconds, between marquee animation updates.</span></span> <span data-ttu-id="ca6de-113">Si ce paramètre est égal à zéro, l’animation de texte défilant est mise à jour toutes les 30 millisecondes.</span><span class="sxs-lookup"><span data-stu-id="ca6de-113">If this parameter is zero, the marquee animation is updated every 30 milliseconds.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca6de-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ca6de-114">Return value</span></span>

<span data-ttu-id="ca6de-115">Retourne toujours la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="ca6de-115">Always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca6de-116">Notes</span><span class="sxs-lookup"><span data-stu-id="ca6de-116">Remarks</span></span>

<span data-ttu-id="ca6de-117">Utilisez ce message lorsque vous ne connaissez pas la progression vers l’achèvement, mais que vous souhaitez indiquer la progression.</span><span class="sxs-lookup"><span data-stu-id="ca6de-117">Use this message when you do not know the amount of progress toward completion but wish to indicate that progress is being made.</span></span>

<span data-ttu-id="ca6de-118">Envoyez le message **PBM \_ SETMARQUEE** pour démarrer ou arrêter l’animation.</span><span class="sxs-lookup"><span data-stu-id="ca6de-118">Send the **PBM\_SETMARQUEE** message to start or stop the animation.</span></span>

> [!Note]  
> <span data-ttu-id="ca6de-119">Vous devez définir le style du contrôle [**sur \_ PBS**](progress-bar-control-styles.md) pour tenter de démarrer l’animation.</span><span class="sxs-lookup"><span data-stu-id="ca6de-119">You must set the control style to [**PBS\_MARQUEE**](progress-bar-control-styles.md) before attempting to start the animation.</span></span>

 

> [!Note]  
> <span data-ttu-id="ca6de-120">Ce message requiert ComCtl32.dll version 6,00 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="ca6de-120">This message requires ComCtl32.dll version 6.00 or later.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ca6de-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ca6de-121">Requirements</span></span>



| <span data-ttu-id="ca6de-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ca6de-122">Requirement</span></span> | <span data-ttu-id="ca6de-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="ca6de-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ca6de-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca6de-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ca6de-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ca6de-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ca6de-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca6de-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ca6de-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ca6de-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ca6de-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="ca6de-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca6de-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca6de-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





