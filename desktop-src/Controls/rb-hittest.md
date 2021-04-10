---
title: Message RB_HITTEST (commctrl. h)
description: Détermine la partie d’une bande rebar située à un point donné sur l’écran, si une bande rebar existe à ce point.
ms.assetid: 8f27db21-50d8-438f-a44c-2e65dd93fa2a
keywords:
- RB_HITTEST les contrôles de message Windows
topic_type:
- apiref
api_name:
- RB_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e17283bfce255672391ba9d8b6acd60fe41045b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032417"
---
# <a name="rb_hittest-message"></a><span data-ttu-id="ebc22-104">\_Message RB HITTEST</span><span class="sxs-lookup"><span data-stu-id="ebc22-104">RB\_HITTEST message</span></span>

<span data-ttu-id="ebc22-105">Détermine la partie d’une bande rebar située à un point donné sur l’écran, si une bande rebar existe à ce point.</span><span class="sxs-lookup"><span data-stu-id="ebc22-105">Determines which portion of a rebar band is at a given point on the screen, if a rebar band exists at that point.</span></span>

## <a name="parameters"></a><span data-ttu-id="ebc22-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ebc22-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebc22-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ebc22-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ebc22-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="ebc22-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ebc22-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ebc22-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ebc22-110">Pointeur vers une structure [**RBHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-rbhittestinfo) .</span><span class="sxs-lookup"><span data-stu-id="ebc22-110">Pointer to an [**RBHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-rbhittestinfo) structure.</span></span> <span data-ttu-id="ebc22-111">Avant d’envoyer le message, le membre **PT** de cette structure doit être initialisé au point qui fera l’élément d’un test de positionnement, en coordonnées clientes.</span><span class="sxs-lookup"><span data-stu-id="ebc22-111">Before sending the message, the **pt** member of this structure must be initialized to the point that will be hit tested, in client coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebc22-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ebc22-112">Return value</span></span>

<span data-ttu-id="ebc22-113">Retourne l’index de base zéro de la bande au point donné, ou-1 si aucune bande de rebar n’était au point.</span><span class="sxs-lookup"><span data-stu-id="ebc22-113">Returns the zero-based index of the band at the given point, or -1 if no rebar band was at the point.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebc22-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ebc22-114">Requirements</span></span>



| <span data-ttu-id="ebc22-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ebc22-115">Requirement</span></span> | <span data-ttu-id="ebc22-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="ebc22-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ebc22-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ebc22-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ebc22-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ebc22-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ebc22-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ebc22-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ebc22-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ebc22-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ebc22-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="ebc22-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ebc22-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ebc22-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





