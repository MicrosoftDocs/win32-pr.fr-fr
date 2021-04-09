---
title: Message DTM_SETFORMAT (commctrl. h)
description: Définit l’affichage d’un contrôle de sélecteur de date et heure (PAO) basé sur une chaîne de format donnée. Vous pouvez envoyer ce message de manière explicite ou utiliser la \_ macro DateTime SetFormat.
ms.assetid: a89fa3ad-9894-4c52-ab56-fb62208e39b3
keywords:
- DTM_SETFORMAT les contrôles de message Windows
topic_type:
- apiref
api_name:
- DTM_SETFORMAT
- DTM_SETFORMATA
- DTM_SETFORMATW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17669ed2e1ed23e3b090b77701bbe05d23a5ccb8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033061"
---
# <a name="dtm_setformat-message"></a><span data-ttu-id="0173b-105">\_Message DTM SETFORMAT</span><span class="sxs-lookup"><span data-stu-id="0173b-105">DTM\_SETFORMAT message</span></span>

<span data-ttu-id="0173b-106">Définit l’affichage d’un contrôle de sélecteur de date et heure (PAO) basé sur une chaîne de format donnée.</span><span class="sxs-lookup"><span data-stu-id="0173b-106">Sets the display of a date and time picker (DTP) control based on a given format string.</span></span> <span data-ttu-id="0173b-107">Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**DateTime \_ SetFormat**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setformat) .</span><span class="sxs-lookup"><span data-stu-id="0173b-107">You can send this message explicitly or use the [**DateTime\_SetFormat**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0173b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0173b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0173b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0173b-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0173b-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="0173b-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0173b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0173b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0173b-112">Pointeur vers une [chaîne de format](date-and-time-picker-controls.md) se terminant par zéro qui définit l’affichage souhaité.</span><span class="sxs-lookup"><span data-stu-id="0173b-112">A pointer to a zero-terminated [format string](date-and-time-picker-controls.md) that defines the desired display.</span></span> <span data-ttu-id="0173b-113">Si ce paramètre a la **valeur null** , le contrôle est réinitialisé à la chaîne de format par défaut pour le style actuel.</span><span class="sxs-lookup"><span data-stu-id="0173b-113">Setting this parameter to **NULL** will reset the control to the default format string for the current style.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0173b-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0173b-114">Return value</span></span>

<span data-ttu-id="0173b-115">Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="0173b-115">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0173b-116">Notes</span><span class="sxs-lookup"><span data-stu-id="0173b-116">Remarks</span></span>

<span data-ttu-id="0173b-117">Il est acceptable d’inclure des caractères supplémentaires dans la chaîne de format pour produire un affichage plus riche.</span><span class="sxs-lookup"><span data-stu-id="0173b-117">It is acceptable to include extra characters within the format string to produce a more rich display.</span></span> <span data-ttu-id="0173b-118">Toutefois, tous les caractères sans format doivent être placés entre guillemets simples.</span><span class="sxs-lookup"><span data-stu-id="0173b-118">However, any nonformat characters must be enclosed within single quotes.</span></span> <span data-ttu-id="0173b-119">Par exemple, la chaîne de format « » aujourd’hui est : «HH » : « m » : « ddddMMMdd », « yyy » produirait une sortie telle que « Today is : 04:22:31 mardi Mar 23, 1996 ».</span><span class="sxs-lookup"><span data-stu-id="0173b-119">For example, the format string "'Today is: 'hh':'m':'s ddddMMMdd', 'yyy" would produce output like "Today is: 04:22:31 Tuesday Mar 23, 1996".</span></span>

> [!Note]  
> <span data-ttu-id="0173b-120">Un contrôle de PAO effectue le suivi des modifications de paramètres régionaux lorsqu’il utilise la chaîne de format par défaut.</span><span class="sxs-lookup"><span data-stu-id="0173b-120">A DTP control tracks locale changes when it is using the default format string.</span></span> <span data-ttu-id="0173b-121">Si vous définissez une chaîne de format personnalisée, elle ne sera pas mise à jour en réponse aux modifications des paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="0173b-121">If you set a custom format string, it will not be updated in response to locale changes.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0173b-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0173b-122">Requirements</span></span>



| <span data-ttu-id="0173b-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0173b-123">Requirement</span></span> | <span data-ttu-id="0173b-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="0173b-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0173b-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0173b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="0173b-126">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0173b-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0173b-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0173b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="0173b-128">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0173b-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0173b-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="0173b-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="0173b-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0173b-130"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="0173b-131">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="0173b-131">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="0173b-132">**DTM \_ SETFORMATW** (Unicode) et **DTM \_ SETFORMATA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="0173b-132">**DTM\_SETFORMATW** (Unicode) and **DTM\_SETFORMATA** (ANSI)</span></span><br/>               |



 

 





