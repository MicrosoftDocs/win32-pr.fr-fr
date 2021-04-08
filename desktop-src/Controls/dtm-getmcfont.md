---
title: Message DTM_GETMCFONT (commctrl. h)
description: Obtient la police actuellement utilisée par le contrôle de calendrier mensuel enfant du contrôle de la date et de l’heure (PAO). Vous pouvez envoyer ce message de manière explicite ou utiliser la \_ macro DateTime GetMonthCalFont.
ms.assetid: 6687a1dc-6f6d-4684-80b2-f726b08d2f3a
keywords:
- DTM_GETMCFONT les contrôles de message Windows
topic_type:
- apiref
api_name:
- DTM_GETMCFONT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d799d5dbbe5e3a4cdf7eede871f9aeac451d17a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844141"
---
# <a name="dtm_getmcfont-message"></a><span data-ttu-id="25a99-105">\_Message DTM GETMCFONT</span><span class="sxs-lookup"><span data-stu-id="25a99-105">DTM\_GETMCFONT message</span></span>

<span data-ttu-id="25a99-106">Obtient la police actuellement utilisée par le contrôle de calendrier mensuel enfant du contrôle de la date et de l’heure (PAO).</span><span class="sxs-lookup"><span data-stu-id="25a99-106">Gets the font that the date and time picker (DTP) control's child month calendar control is currently using.</span></span> <span data-ttu-id="25a99-107">Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**DateTime \_ GetMonthCalFont**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalfont) .</span><span class="sxs-lookup"><span data-stu-id="25a99-107">You can send this message explicitly or use the [**DateTime\_GetMonthCalFont**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalfont) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="25a99-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="25a99-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25a99-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="25a99-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="25a99-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="25a99-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="25a99-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="25a99-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="25a99-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="25a99-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25a99-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="25a99-113">Return value</span></span>

<span data-ttu-id="25a99-114">Retourne une valeur HFONT qui est le handle de la police actuelle.</span><span class="sxs-lookup"><span data-stu-id="25a99-114">Returns an HFONT value that is the handle to the current font.</span></span>

## <a name="requirements"></a><span data-ttu-id="25a99-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="25a99-115">Requirements</span></span>



| <span data-ttu-id="25a99-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="25a99-116">Requirement</span></span> | <span data-ttu-id="25a99-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="25a99-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="25a99-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="25a99-118">Minimum supported client</span></span><br/> | <span data-ttu-id="25a99-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="25a99-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="25a99-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="25a99-120">Minimum supported server</span></span><br/> | <span data-ttu-id="25a99-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="25a99-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="25a99-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="25a99-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="25a99-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="25a99-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





