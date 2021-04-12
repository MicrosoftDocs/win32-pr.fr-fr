---
title: Message TDM_SET_PROGRESS_BAR_POS (commctrl. h)
description: Définit la position de la barre de progression dans une boîte de dialogue de tâche.
ms.assetid: 82247d70-8527-4195-87af-5c4e5fd1d1a2
keywords:
- TDM_SET_PROGRESS_BAR_POS les contrôles de message Windows
topic_type:
- apiref
api_name:
- TDM_SET_PROGRESS_BAR_POS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58e12b67c218f21c72f28089a3246d52c6165740
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464243"
---
# <a name="tdm_set_progress_bar_pos-message"></a><span data-ttu-id="1a4f0-104">Message de PDV de la barre de progression de l' \_ ensemble TDM \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="1a4f0-104">TDM\_SET\_PROGRESS\_BAR\_POS message</span></span>

<span data-ttu-id="1a4f0-105">Définit la position de la barre de progression dans une boîte de dialogue de tâche.</span><span class="sxs-lookup"><span data-stu-id="1a4f0-105">Sets the position of the progress bar in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="1a4f0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1a4f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a4f0-107">*wParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1a4f0-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a4f0-108">**Entier** qui spécifie la nouvelle position.</span><span class="sxs-lookup"><span data-stu-id="1a4f0-108">An **int** that specifies the new position.</span></span>

</dd> <dt>

<span data-ttu-id="1a4f0-109">*lParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1a4f0-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a4f0-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="1a4f0-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a4f0-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1a4f0-111">Return value</span></span>

<span data-ttu-id="1a4f0-112">Retourne la position précédente.</span><span class="sxs-lookup"><span data-stu-id="1a4f0-112">Returns the previous position.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a4f0-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1a4f0-113">Requirements</span></span>



| <span data-ttu-id="1a4f0-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1a4f0-114">Requirement</span></span> | <span data-ttu-id="1a4f0-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="1a4f0-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1a4f0-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1a4f0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1a4f0-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1a4f0-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1a4f0-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1a4f0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1a4f0-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1a4f0-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1a4f0-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="1a4f0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a4f0-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a4f0-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





