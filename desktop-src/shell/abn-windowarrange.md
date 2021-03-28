---
description: Avertit un appbar que l’utilisateur a sélectionné la commande cascade, mosaïque horizontale ou Mosaïque verticale à partir du menu contextuel de la barre des tâches.
title: Message ABN_WINDOWARRANGE (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 32eb7298-75ca-4ff8-86cf-7c9ca9d71868
api_name:
- ABN_WINDOWARRANGE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9e7d19c7233b235a1a73e160eeacb3c51415d0bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525420"
---
# <a name="abn_windowarrange-message"></a><span data-ttu-id="a3987-103">Message d’ABN \_ WINDOWARRANGE</span><span class="sxs-lookup"><span data-stu-id="a3987-103">ABN\_WINDOWARRANGE message</span></span>

<span data-ttu-id="a3987-104">Avertit un appbar que l’utilisateur a sélectionné la commande cascade, mosaïque horizontale ou Mosaïque verticale à partir du menu contextuel de la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="a3987-104">Notifies an appbar that the user has selected the Cascade, Tile Horizontally, or Tile Vertically command from the taskbar's shortcut menu.</span></span>


```C++
ABN_WINDOWARRANGE 



    fBeginning = (BOOL) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="a3987-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a3987-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3987-106">*fBeginning*</span><span class="sxs-lookup"><span data-stu-id="a3987-106">*fBeginning*</span></span> 
</dt> <dd>

<span data-ttu-id="a3987-107">Indicateur spécifiant si l’opération de cascade ou de vignette commence.</span><span class="sxs-lookup"><span data-stu-id="a3987-107">A flag specifying whether the cascade or tile operation is beginning.</span></span> <span data-ttu-id="a3987-108">Ce paramètre a la **valeur true** si l’opération commence et que les fenêtres n’ont pas encore été déplacées.</span><span class="sxs-lookup"><span data-stu-id="a3987-108">This parameter is **TRUE** if the operation is beginning and the windows have not yet been moved.</span></span> <span data-ttu-id="a3987-109">La **valeur est false** si l’opération est terminée.</span><span class="sxs-lookup"><span data-stu-id="a3987-109">It is **FALSE** if the operation has completed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3987-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a3987-110">Return value</span></span>

<span data-ttu-id="a3987-111">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="a3987-111">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3987-112">Notes</span><span class="sxs-lookup"><span data-stu-id="a3987-112">Remarks</span></span>

<span data-ttu-id="a3987-113">Le système envoie le message de notification à deux reprises avec *lParam* défini à **true** , puis avec *lParam* défini sur **false**.</span><span class="sxs-lookup"><span data-stu-id="a3987-113">The system sends this notification message twice first with *lParam* set to **TRUE** and then with *lParam* set to **FALSE**.</span></span> <span data-ttu-id="a3987-114">La première notification est envoyée avant que les fenêtres soient mises en cascade ou en mosaïque, et la seconde est envoyée après l’opération de mise en cascade ou de vignette.</span><span class="sxs-lookup"><span data-stu-id="a3987-114">The first notification is sent before the windows are cascaded or tiled, and the second is sent after the cascade or tile operation has occurred.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3987-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a3987-115">Requirements</span></span>



| <span data-ttu-id="a3987-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a3987-116">Requirement</span></span> | <span data-ttu-id="a3987-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="a3987-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a3987-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a3987-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a3987-119">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a3987-119">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a3987-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a3987-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a3987-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a3987-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a3987-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="a3987-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3987-123"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3987-123"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




