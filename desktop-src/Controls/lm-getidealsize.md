---
title: Message LM_GETIDEALSIZE (commctrl. h)
description: 'LM_GETIDEALSIZE message : récupère la hauteur par défaut d’un lien pour la largeur actuelle du contrôle.'
ms.assetid: 63aad7eb-26ee-41d2-90d4-65fdcf0f182a
keywords:
- LM_GETIDEALSIZE les contrôles de message Windows
topic_type:
- apiref
api_name:
- LM_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 761fb5f6e5f7a2e2e9b1b9cc862b9a8f2c0fcd1f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112387"
---
# <a name="lm_getidealsize-message"></a><span data-ttu-id="c95e2-104">\_Message LM GETIDEALSIZE</span><span class="sxs-lookup"><span data-stu-id="c95e2-104">LM\_GETIDEALSIZE message</span></span>

<span data-ttu-id="c95e2-105">Récupère la hauteur par défaut d’un lien pour la largeur actuelle du contrôle.</span><span class="sxs-lookup"><span data-stu-id="c95e2-105">Retrieves the preferred height of a link for the control's current width.</span></span>

## <a name="parameters"></a><span data-ttu-id="c95e2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c95e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c95e2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c95e2-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c95e2-108">Largeur maximale du lien, en pixels.</span><span class="sxs-lookup"><span data-stu-id="c95e2-108">Maximum width of the link, in pixels.</span></span></dd> <dt>

<span data-ttu-id="c95e2-109">*lParam* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c95e2-109">*lParam* \[out\]</span></span>
</dt> <dd><span data-ttu-id="c95e2-110">Lorsque ce message est retourné, contient un pointeur vers une structure de <a href="/previous-versions//dd145106(v=vs.85)">**taille**</a> .</span><span class="sxs-lookup"><span data-stu-id="c95e2-110">When this message returns, contains a pointer to a <a href="/previous-versions//dd145106(v=vs.85)">**SIZE**</a> structure.</span></span> <span data-ttu-id="c95e2-111">Le membre **CY** de cette structure indique la hauteur idéale du contrôle pour la largeur donnée.</span><span class="sxs-lookup"><span data-stu-id="c95e2-111">The **cy** member of this structure indicates the ideal height of the control for the given width.</span></span> <span data-ttu-id="c95e2-112">Il ajuste le membre **CX** en fonction de la quantité d’espace réellement nécessaire.</span><span class="sxs-lookup"><span data-stu-id="c95e2-112">It adjusts the **cx** member to the amount of space actually needed.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c95e2-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c95e2-113">Return value</span></span>

<span data-ttu-id="c95e2-114">Entier qui représente la hauteur préférée du texte du lien, en pixels.</span><span class="sxs-lookup"><span data-stu-id="c95e2-114">Integer that represents the preferred height of the link text, in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="c95e2-115">Notes </span><span class="sxs-lookup"><span data-stu-id="c95e2-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c95e2-116">Pour utiliser cette API, vous devez fournir un manifeste qui spécifie Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="c95e2-116">To use this API, you must provide a manifest that specifies Comclt32.dll version 6.0.</span></span> <span data-ttu-id="c95e2-117">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c95e2-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c95e2-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c95e2-118">Requirements</span></span>



| <span data-ttu-id="c95e2-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c95e2-119">Requirement</span></span> | <span data-ttu-id="c95e2-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="c95e2-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c95e2-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c95e2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c95e2-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c95e2-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c95e2-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c95e2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c95e2-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c95e2-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c95e2-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="c95e2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c95e2-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c95e2-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

