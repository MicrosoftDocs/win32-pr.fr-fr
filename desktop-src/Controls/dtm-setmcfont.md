---
title: Message DTM_SETMCFONT (commctrl. h)
description: Définit la police utilisée par le contrôle de calendrier mensuel enfant du contrôle de la date et de l’heure (PAO). Vous pouvez envoyer ce message de manière explicite ou utiliser la \_ macro DateTime SetMonthCalFont.
ms.assetid: 5033e975-9b68-438a-99c3-80ca02cd59e7
keywords:
- DTM_SETMCFONT les contrôles de message Windows
topic_type:
- apiref
api_name:
- DTM_SETMCFONT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b148ffb95acd82257265bf0bab53000b10803793
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466118"
---
# <a name="dtm_setmcfont-message"></a><span data-ttu-id="c2c30-105">\_Message DTM SETMCFONT</span><span class="sxs-lookup"><span data-stu-id="c2c30-105">DTM\_SETMCFONT message</span></span>

<span data-ttu-id="c2c30-106">Définit la police utilisée par le contrôle de calendrier mensuel enfant du contrôle de la date et de l’heure (PAO).</span><span class="sxs-lookup"><span data-stu-id="c2c30-106">Sets the font to be used by the date and time picker (DTP) control's child month calendar control.</span></span> <span data-ttu-id="c2c30-107">Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**DateTime \_ SetMonthCalFont**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalfont) .</span><span class="sxs-lookup"><span data-stu-id="c2c30-107">You can send this message explicitly or use the [**DateTime\_SetMonthCalFont**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalfont) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c2c30-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c2c30-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2c30-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c2c30-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c2c30-110">Handle de la police qui sera définie.</span><span class="sxs-lookup"><span data-stu-id="c2c30-110">A handle to the font that will be set.</span></span>

</dd> <dt>

<span data-ttu-id="c2c30-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c2c30-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c2c30-112">Spécifie si le contrôle doit être redessiné immédiatement lors de la définition de la police.</span><span class="sxs-lookup"><span data-stu-id="c2c30-112">Specifies whether the control should be redrawn immediately upon setting the font.</span></span> <span data-ttu-id="c2c30-113">Si ce paramètre a la **valeur true** , le contrôle se redessine lui-même.</span><span class="sxs-lookup"><span data-stu-id="c2c30-113">Setting this parameter to **TRUE** causes the control to redraw itself.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2c30-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c2c30-114">Return value</span></span>

<span data-ttu-id="c2c30-115">La valeur de retour de ce message n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="c2c30-115">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2c30-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c2c30-116">Requirements</span></span>



| <span data-ttu-id="c2c30-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c2c30-117">Requirement</span></span> | <span data-ttu-id="c2c30-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2c30-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c2c30-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2c30-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c2c30-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c2c30-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c2c30-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2c30-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c2c30-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c2c30-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c2c30-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="c2c30-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2c30-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2c30-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





