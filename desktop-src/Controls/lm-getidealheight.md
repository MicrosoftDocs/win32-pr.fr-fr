---
title: Message LM_GETIDEALHEIGHT (commctrl. h)
description: Récupère la hauteur par défaut d’un lien pour la largeur actuelle du contrôle.
ms.assetid: bf6ef3c1-89bc-4c56-9384-085fd00234e1
keywords:
- LM_GETIDEALHEIGHT les contrôles de message Windows
topic_type:
- apiref
api_name:
- LM_GETIDEALHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a92f24d63cc8f58e260d79dafd0555429d65d20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843102"
---
# <a name="lm_getidealheight-message"></a><span data-ttu-id="c8ecb-104">\_Message LM GETIDEALHEIGHT</span><span class="sxs-lookup"><span data-stu-id="c8ecb-104">LM\_GETIDEALHEIGHT message</span></span>

<span data-ttu-id="c8ecb-105">Récupère la hauteur par défaut d’un lien pour la largeur actuelle du contrôle.</span><span class="sxs-lookup"><span data-stu-id="c8ecb-105">Retrieves the preferred height of a link for the control's current width.</span></span>

## <a name="parameters"></a><span data-ttu-id="c8ecb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c8ecb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8ecb-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c8ecb-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c8ecb-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="c8ecb-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c8ecb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c8ecb-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c8ecb-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="c8ecb-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8ecb-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c8ecb-111">Return value</span></span>

<span data-ttu-id="c8ecb-112">Entier représentant la hauteur préférée du texte du lien, en pixels.</span><span class="sxs-lookup"><span data-stu-id="c8ecb-112">Integer representing the preferred height of the link text, in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8ecb-113">Notes</span><span class="sxs-lookup"><span data-stu-id="c8ecb-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c8ecb-114">Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="c8ecb-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="c8ecb-115">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c8ecb-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c8ecb-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c8ecb-116">Requirements</span></span>



| <span data-ttu-id="c8ecb-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c8ecb-117">Requirement</span></span> | <span data-ttu-id="c8ecb-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="c8ecb-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c8ecb-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c8ecb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c8ecb-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c8ecb-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c8ecb-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c8ecb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c8ecb-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c8ecb-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c8ecb-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="c8ecb-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8ecb-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8ecb-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





