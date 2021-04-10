---
title: Message RB_GETRECT (commctrl. h)
description: Récupère le rectangle englobant pour une bande donnée dans un contrôle rebar.
ms.assetid: e272b090-1e4d-4cff-87f0-557ad8116e7e
keywords:
- RB_GETRECT les contrôles de message Windows
topic_type:
- apiref
api_name:
- RB_GETRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76b9d5de00b638a3767df461595ff01316b23183
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104200559"
---
# <a name="rb_getrect-message"></a><span data-ttu-id="ec699-104">\_Message GETRECT RB</span><span class="sxs-lookup"><span data-stu-id="ec699-104">RB\_GETRECT message</span></span>

<span data-ttu-id="ec699-105">Récupère le rectangle englobant pour une bande donnée dans un contrôle rebar.</span><span class="sxs-lookup"><span data-stu-id="ec699-105">Retrieves the bounding rectangle for a given band in a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="ec699-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ec699-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec699-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ec699-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ec699-108">Index de base zéro d’une bande dans le contrôle rebar.</span><span class="sxs-lookup"><span data-stu-id="ec699-108">Zero-based index of a band in the rebar control.</span></span>

</dd> <dt>

<span data-ttu-id="ec699-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ec699-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ec699-110">Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui recevra les limites de la bande rebar.</span><span class="sxs-lookup"><span data-stu-id="ec699-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that will receive the bounds of the rebar band.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec699-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ec699-111">Return value</span></span>

<span data-ttu-id="ec699-112">Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="ec699-112">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec699-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ec699-113">Requirements</span></span>



| <span data-ttu-id="ec699-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ec699-114">Requirement</span></span> | <span data-ttu-id="ec699-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec699-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ec699-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ec699-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ec699-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ec699-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ec699-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ec699-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ec699-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ec699-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ec699-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="ec699-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec699-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec699-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

