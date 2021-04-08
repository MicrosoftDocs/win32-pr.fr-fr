---
title: Message SB_GETICON (commctrl. h)
description: Récupère l’icône pour un composant dans une barre d’État.
ms.assetid: f99508e3-afa8-48fd-b87a-fce41c4410ff
keywords:
- SB_GETICON les contrôles de message Windows
topic_type:
- apiref
api_name:
- SB_GETICON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab86809df54d796b8e83f05f2a2b9041450ce2fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844002"
---
# <a name="sb_geticon-message"></a><span data-ttu-id="52591-104">\_Message SB GETICON</span><span class="sxs-lookup"><span data-stu-id="52591-104">SB\_GETICON message</span></span>

<span data-ttu-id="52591-105">Récupère l’icône pour un composant dans une barre d’État.</span><span class="sxs-lookup"><span data-stu-id="52591-105">Retrieves the icon for a part in a status bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="52591-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="52591-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52591-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="52591-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="52591-108">Index de base zéro de la partie qui contient l’icône à récupérer.</span><span class="sxs-lookup"><span data-stu-id="52591-108">Zero-based index of the part that contains the icon to be retrieved.</span></span> <span data-ttu-id="52591-109">Si ce paramètre a la valeur-1, la barre d’État est supposée être une barre d’état de [mode simple](status-bars.md) .</span><span class="sxs-lookup"><span data-stu-id="52591-109">If this parameter is -1, the status bar is assumed to be a [Simple Mode](status-bars.md) status bar.</span></span>

</dd> <dt>

<span data-ttu-id="52591-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="52591-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="52591-111">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="52591-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52591-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="52591-112">Return value</span></span>

<span data-ttu-id="52591-113">Retourne le handle de l’icône en cas de réussite, ou **null** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="52591-113">Returns the handle to the icon if successful, or **NULL** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="52591-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="52591-114">Requirements</span></span>



| <span data-ttu-id="52591-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="52591-115">Requirement</span></span> | <span data-ttu-id="52591-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="52591-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="52591-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="52591-117">Minimum supported client</span></span><br/> | <span data-ttu-id="52591-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="52591-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="52591-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="52591-119">Minimum supported server</span></span><br/> | <span data-ttu-id="52591-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="52591-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="52591-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="52591-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="52591-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="52591-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





