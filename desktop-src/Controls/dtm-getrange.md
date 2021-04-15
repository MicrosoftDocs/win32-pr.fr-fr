---
title: Message DTM_GETRANGE (commctrl. h)
description: Obtient l’heure système actuelle minimale et maximale autorisée pour un contrôle de sélecteur de dates et d’heures (PAO). Vous pouvez envoyer ce message de manière explicite ou utiliser la \_ macro DateTime GetRange.
ms.assetid: 190cada6-49ee-483f-a464-d3d789127159
keywords:
- DTM_GETRANGE les contrôles de message Windows
topic_type:
- apiref
api_name:
- DTM_GETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a50a2ae9fe4ca77198f9e63548f709e0f571fdb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466119"
---
# <a name="dtm_getrange-message"></a><span data-ttu-id="3ccf2-105">\_Message DTM GETRANGE</span><span class="sxs-lookup"><span data-stu-id="3ccf2-105">DTM\_GETRANGE message</span></span>

<span data-ttu-id="3ccf2-106">Obtient l’heure système actuelle minimale et maximale autorisée pour un contrôle de sélecteur de dates et d’heures (PAO).</span><span class="sxs-lookup"><span data-stu-id="3ccf2-106">Gets the current minimum and maximum allowable system times for a date and time picker (DTP) control.</span></span> <span data-ttu-id="3ccf2-107">Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**DateTime \_ GetRange**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getrange) .</span><span class="sxs-lookup"><span data-stu-id="3ccf2-107">You can send this message explicitly or use the [**DateTime\_GetRange**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getrange) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="3ccf2-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3ccf2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ccf2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3ccf2-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="3ccf2-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="3ccf2-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="3ccf2-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3ccf2-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3ccf2-112">Pointeur vers un tableau à deux éléments de structures [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) .</span><span class="sxs-lookup"><span data-stu-id="3ccf2-112">A pointer to a two-element array of [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structures.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ccf2-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3ccf2-113">Return value</span></span>

<span data-ttu-id="3ccf2-114">Retourne une valeur **DWORD** qui est une combinaison de GDTR \_ min ou GDTR \_ Max.</span><span class="sxs-lookup"><span data-stu-id="3ccf2-114">Returns a **DWORD** value that is a combination of GDTR\_MIN or GDTR\_MAX.</span></span> <span data-ttu-id="3ccf2-115">Le premier élément du tableau [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) contient l’heure minimale autorisée si GDTR \_ min est défini.</span><span class="sxs-lookup"><span data-stu-id="3ccf2-115">The first element of the [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) array contains the minimum allowable time if GDTR\_MIN is set.</span></span> <span data-ttu-id="3ccf2-116">Le deuxième élément du tableau **SystemTime** contient le temps maximal autorisé si GDTR \_ Max est défini.</span><span class="sxs-lookup"><span data-stu-id="3ccf2-116">The second element of the **SYSTEMTIME** array contains the maximum allowable time if GDTR\_MAX is set.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ccf2-117">Notes</span><span class="sxs-lookup"><span data-stu-id="3ccf2-117">Remarks</span></span>

<span data-ttu-id="3ccf2-118">Le sélecteur de date et d’heure affiche uniquement les dates/heures qui se trouvent dans la plage spécifiée, ce qui empêche l’utilisateur de sélectionner une date et une heure situées en dehors de la plage.</span><span class="sxs-lookup"><span data-stu-id="3ccf2-118">The date and time picker displays only dates/times that fall within the specified range, preventing the user from selecting a date and time that falls outside the range.</span></span> <span data-ttu-id="3ccf2-119">Si le message [**DTM \_ SETSYSTEMTIME**](dtm-setsystemtime.md) spécifie une date et une heure qui se situent en dehors de la plage, l’opération échoue.</span><span class="sxs-lookup"><span data-stu-id="3ccf2-119">If the [**DTM\_SETSYSTEMTIME**](dtm-setsystemtime.md) message specifies a date and time that falls outside the range, it will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ccf2-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3ccf2-120">Requirements</span></span>



| <span data-ttu-id="3ccf2-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3ccf2-121">Requirement</span></span> | <span data-ttu-id="3ccf2-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="3ccf2-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3ccf2-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3ccf2-123">Minimum supported client</span></span><br/> | <span data-ttu-id="3ccf2-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3ccf2-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3ccf2-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3ccf2-125">Minimum supported server</span></span><br/> | <span data-ttu-id="3ccf2-126">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3ccf2-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3ccf2-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="3ccf2-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ccf2-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ccf2-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

