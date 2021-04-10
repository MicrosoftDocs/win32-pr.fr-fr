---
title: Message DTM_GETIDEALSIZE (commctrl. h)
description: Obtient la taille nécessaire pour afficher le contrôle sans découpage. Envoyez ce message explicitement ou à l’aide de la \_ macro DateTime GetIdealSize.
ms.assetid: 15ec26a1-645b-4a96-af66-1031e1a46c6c
keywords:
- DTM_GETIDEALSIZE les contrôles de message Windows
topic_type:
- apiref
api_name:
- DTM_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a979883f431fea4627f52fe19c3716341e3f2328
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104200546"
---
# <a name="dtm_getidealsize-message"></a><span data-ttu-id="0d1bc-105">\_Message DTM GETIDEALSIZE</span><span class="sxs-lookup"><span data-stu-id="0d1bc-105">DTM\_GETIDEALSIZE message</span></span>

<span data-ttu-id="0d1bc-106">Obtient la taille nécessaire pour afficher le contrôle sans découpage.</span><span class="sxs-lookup"><span data-stu-id="0d1bc-106">Gets the size needed to display the control without clipping.</span></span> <span data-ttu-id="0d1bc-107">Envoyez ce message explicitement ou à l’aide de la macro [**DateTime \_ GetIdealSize**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getidealsize) .</span><span class="sxs-lookup"><span data-stu-id="0d1bc-107">Send this message explicitly or by using the [**DateTime\_GetIdealSize**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getidealsize) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0d1bc-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0d1bc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d1bc-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0d1bc-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0d1bc-110">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="0d1bc-110">Not used.</span></span> <span data-ttu-id="0d1bc-111">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="0d1bc-111">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="0d1bc-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0d1bc-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0d1bc-113">Pointeur vers une structure de [**taille**](/previous-versions//dd145106(v=vs.85)) pour recevoir la taille idéale.</span><span class="sxs-lookup"><span data-stu-id="0d1bc-113">A pointer to a [**SIZE**](/previous-versions//dd145106(v=vs.85)) structure to receive the ideal size.</span></span> <span data-ttu-id="0d1bc-114">L’application appelante est chargée d’allouer cette structure.</span><span class="sxs-lookup"><span data-stu-id="0d1bc-114">The calling application is responsible for allocating this structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d1bc-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0d1bc-115">Return value</span></span>

<span data-ttu-id="0d1bc-116">Retourne la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="0d1bc-116">Returns **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d1bc-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0d1bc-117">Requirements</span></span>



| <span data-ttu-id="0d1bc-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0d1bc-118">Requirement</span></span> | <span data-ttu-id="0d1bc-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="0d1bc-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0d1bc-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d1bc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0d1bc-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0d1bc-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0d1bc-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d1bc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0d1bc-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0d1bc-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0d1bc-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="0d1bc-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d1bc-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d1bc-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

