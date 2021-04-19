---
title: Message TB_GETMAXSIZE (commctrl. h)
description: Récupère la taille totale de tous les boutons et séparateurs visibles dans la barre d’outils.
ms.assetid: 560e6ce2-00ef-46c3-b1d8-fbe0ac79c888
keywords:
- TB_GETMAXSIZE les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_GETMAXSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4829e65d90c04181369dd73b9c54634f1077144
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510158"
---
# <a name="tb_getmaxsize-message"></a><span data-ttu-id="6d920-104">TO \_ GETMAXSIZE message</span><span class="sxs-lookup"><span data-stu-id="6d920-104">TB\_GETMAXSIZE message</span></span>

<span data-ttu-id="6d920-105">Récupère la taille totale de tous les boutons et séparateurs visibles dans la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="6d920-105">Retrieves the total size of all of the visible buttons and separators in the toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="6d920-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6d920-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d920-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6d920-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6d920-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="6d920-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6d920-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6d920-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6d920-110">Pointeur vers une structure de [**taille**](/previous-versions//dd145106(v=vs.85)) qui reçoit la taille des éléments.</span><span class="sxs-lookup"><span data-stu-id="6d920-110">Pointer to a [**SIZE**](/previous-versions//dd145106(v=vs.85)) structure that receives the size of the items.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d920-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6d920-111">Return value</span></span>

<span data-ttu-id="6d920-112">Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="6d920-112">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d920-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6d920-113">Requirements</span></span>



| <span data-ttu-id="6d920-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6d920-114">Requirement</span></span> | <span data-ttu-id="6d920-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="6d920-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6d920-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d920-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6d920-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6d920-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6d920-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d920-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6d920-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6d920-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6d920-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="6d920-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d920-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d920-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

