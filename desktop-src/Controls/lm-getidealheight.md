---
title: Message LM_GETIDEALHEIGHT (commctrl. h)
description: 'LM_GETIDEALHEIGHT message : récupère la hauteur par défaut d’un lien pour la largeur actuelle du contrôle.'
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
ms.openlocfilehash: 1d6e82f259124e6da285ed2357d48ca07d5f8c08
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112397"
---
# <a name="lm_getidealheight-message"></a><span data-ttu-id="7f142-104">\_Message LM GETIDEALHEIGHT</span><span class="sxs-lookup"><span data-stu-id="7f142-104">LM\_GETIDEALHEIGHT message</span></span>

<span data-ttu-id="7f142-105">Récupère la hauteur par défaut d’un lien pour la largeur actuelle du contrôle.</span><span class="sxs-lookup"><span data-stu-id="7f142-105">Retrieves the preferred height of a link for the control's current width.</span></span>

## <a name="parameters"></a><span data-ttu-id="7f142-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7f142-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f142-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7f142-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="7f142-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="7f142-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="7f142-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7f142-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="7f142-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="7f142-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f142-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7f142-111">Return value</span></span>

<span data-ttu-id="7f142-112">Entier représentant la hauteur préférée du texte du lien, en pixels.</span><span class="sxs-lookup"><span data-stu-id="7f142-112">Integer representing the preferred height of the link text, in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f142-113">Notes </span><span class="sxs-lookup"><span data-stu-id="7f142-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7f142-114">Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="7f142-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="7f142-115">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7f142-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7f142-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7f142-116">Requirements</span></span>



| <span data-ttu-id="7f142-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7f142-117">Requirement</span></span> | <span data-ttu-id="7f142-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="7f142-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7f142-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7f142-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7f142-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7f142-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7f142-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7f142-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7f142-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7f142-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7f142-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="7f142-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f142-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f142-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





