---
title: Message TB_HITTEST (commctrl. h)
description: Détermine où un point se trouve dans un contrôle de barre d’outils.
ms.assetid: d08f3805-2042-470e-8f5a-8a6a681d1189
keywords:
- TB_HITTEST les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6264bc0191f091d3819081ddd67e428b64c84570
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941947"
---
# <a name="tb_hittest-message"></a><span data-ttu-id="65247-104">TO \_ message HITTEST</span><span class="sxs-lookup"><span data-stu-id="65247-104">TB\_HITTEST message</span></span>

<span data-ttu-id="65247-105">Détermine où un point se trouve dans un contrôle de barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="65247-105">Determines where a point lies in a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="65247-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="65247-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65247-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="65247-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="65247-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="65247-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="65247-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="65247-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="65247-110">Pointeur vers une structure de [**points**](/previous-versions//dd162805(v=vs.85)) qui contient la coordonnée x du test d’atteinte dans le membre **x** et la coordonnée y du test de positionnement dans le membre **y** .</span><span class="sxs-lookup"><span data-stu-id="65247-110">Pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure that contains the x-coordinate of the hit test in the **x** member and the y-coordinate of the hit test in the **y** member.</span></span> <span data-ttu-id="65247-111">Les coordonnées sont relatives à la zone cliente de la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="65247-111">The coordinates are relative to the toolbar's client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65247-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="65247-112">Return value</span></span>

<span data-ttu-id="65247-113">Retourne une valeur entière.</span><span class="sxs-lookup"><span data-stu-id="65247-113">Returns an integer value.</span></span> <span data-ttu-id="65247-114">Si la valeur de retour est zéro ou une valeur positive, il s’agit de l’index de base zéro de l’élément de non-séparateur dans lequel se trouve le point.</span><span class="sxs-lookup"><span data-stu-id="65247-114">If the return value is zero or a positive value, it is the zero-based index of the nonseparator item in which the point lies.</span></span> <span data-ttu-id="65247-115">Si la valeur de retour est négative, le point ne se situe pas dans un bouton.</span><span class="sxs-lookup"><span data-stu-id="65247-115">If the return value is negative, the point does not lie within a button.</span></span> <span data-ttu-id="65247-116">La valeur absolue de la valeur de retour est l’index d’un élément de séparateur ou de l’élément de non-séparateur le plus proche.</span><span class="sxs-lookup"><span data-stu-id="65247-116">The absolute value of the return value is the index of a separator item or the nearest nonseparator item.</span></span>

## <a name="requirements"></a><span data-ttu-id="65247-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="65247-117">Requirements</span></span>



| <span data-ttu-id="65247-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="65247-118">Requirement</span></span> | <span data-ttu-id="65247-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="65247-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="65247-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65247-120">Minimum supported client</span></span><br/> | <span data-ttu-id="65247-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="65247-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="65247-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65247-122">Minimum supported server</span></span><br/> | <span data-ttu-id="65247-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="65247-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="65247-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="65247-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="65247-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="65247-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

