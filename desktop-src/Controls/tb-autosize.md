---
title: Message TB_AUTOSIZE (commctrl. h)
description: Entraîne le redimensionnement d’une barre d’outils.
ms.assetid: 11aff184-6f18-43a2-9bdc-462fc5ba1680
keywords:
- TB_AUTOSIZE les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_AUTOSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5f901463888338fd9cadf67472232efe9a25f29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519313"
---
# <a name="tb_autosize-message"></a><span data-ttu-id="e218e-104">\_Message de REdimensionnement automatique to</span><span class="sxs-lookup"><span data-stu-id="e218e-104">TB\_AUTOSIZE message</span></span>

<span data-ttu-id="e218e-105">Entraîne le redimensionnement d’une barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="e218e-105">Causes a toolbar to be resized.</span></span>

## <a name="parameters"></a><span data-ttu-id="e218e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e218e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e218e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e218e-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e218e-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="e218e-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e218e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e218e-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="e218e-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="e218e-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e218e-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e218e-111">Return value</span></span>

<span data-ttu-id="e218e-112">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="e218e-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e218e-113">Notes</span><span class="sxs-lookup"><span data-stu-id="e218e-113">Remarks</span></span>

<span data-ttu-id="e218e-114">Une application envoie le message de **\_ taille automatique to** après avoir entraîné la modification de la taille d’une barre d’outils en définissant la taille du bouton ou de la bitmap, ou en ajoutant des chaînes pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="e218e-114">An application sends the **TB\_AUTOSIZE** message after causing the size of a toolbar to change either by setting the button or bitmap size or by adding strings for the first time.</span></span>

## <a name="requirements"></a><span data-ttu-id="e218e-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e218e-115">Requirements</span></span>



| <span data-ttu-id="e218e-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e218e-116">Requirement</span></span> | <span data-ttu-id="e218e-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="e218e-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e218e-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e218e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e218e-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e218e-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e218e-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e218e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e218e-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e218e-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e218e-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="e218e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e218e-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e218e-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





