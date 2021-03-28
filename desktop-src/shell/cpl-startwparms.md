---
description: Envoyé pour notifier à CPlApplet que l’utilisateur a choisi l’icône associée à une boîte de dialogue donnée. CPlApplet doit afficher la boîte de dialogue correspondante et effectuer toutes les tâches spécifiées par l’utilisateur.
title: Message CPL_STARTWPARMS (CPL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 04ac5117-39c9-4d3f-b32d-8f8d2b515be1
api_name:
- CPL_STARTWPARMS
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 790779c1c45acbc211fe36e28b2e55d5ae2e60da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951019"
---
# <a name="cpl_startwparms-message"></a><span data-ttu-id="fb143-104">\_Message STARTWPARMS cpl</span><span class="sxs-lookup"><span data-stu-id="fb143-104">CPL\_STARTWPARMS message</span></span>

<span data-ttu-id="fb143-105">Envoyé pour notifier à [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) que l’utilisateur a choisi l’icône associée à une boîte de dialogue donnée.</span><span class="sxs-lookup"><span data-stu-id="fb143-105">Sent to notify [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) that the user has chosen the icon associated with a given dialog box.</span></span> <span data-ttu-id="fb143-106">**CPlApplet** doit afficher la boîte de dialogue correspondante et effectuer toutes les tâches spécifiées par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fb143-106">**CPlApplet** should display the corresponding dialog box and carry out any user-specified tasks.</span></span>

## <a name="parameters"></a><span data-ttu-id="fb143-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fb143-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb143-108">*uAppNum*</span><span class="sxs-lookup"><span data-stu-id="fb143-108">*uAppNum*</span></span> 
</dt> <dd>

<span data-ttu-id="fb143-109">Numéro de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="fb143-109">The dialog box number.</span></span> <span data-ttu-id="fb143-110">Ce nombre doit être compris entre zéro et une valeur inférieure à la valeur renvoyée en réponse au message [**Cpl \_ GETCOUNT**](cpl-getcount.md) (CPL \_ GetCount – 1).</span><span class="sxs-lookup"><span data-stu-id="fb143-110">This number must be in the range zero through one less than the value returned in response to the [**CPL\_GETCOUNT**](cpl-getcount.md) message (CPL\_GETCOUNT – 1).</span></span>

</dd> <dt>

<span data-ttu-id="fb143-111">*lpszExtra*</span><span class="sxs-lookup"><span data-stu-id="fb143-111">*lpszExtra*</span></span> 
</dt> <dd>

<span data-ttu-id="fb143-112">Chaîne avec des instructions supplémentaires pour l’exécution.</span><span class="sxs-lookup"><span data-stu-id="fb143-112">A string with additional directions for execution.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb143-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fb143-113">Return value</span></span>

<span data-ttu-id="fb143-114">Retourne la **valeur true** si le message a été géré, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="fb143-114">Returns **TRUE** if the message was handled, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb143-115">Notes</span><span class="sxs-lookup"><span data-stu-id="fb143-115">Remarks</span></span>

<span data-ttu-id="fb143-116">**Cpl \_ STARTWPARMS** est similaire à [**Cpl \_ DBLCLK**](cpl-dblclk.md) , mais vous permet de passer une chaîne à [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) au lieu d’un **int**. Vous pouvez utiliser cette chaîne comme une méthode flexible pour fournir des instructions détaillées pour l’exécution.</span><span class="sxs-lookup"><span data-stu-id="fb143-116">**CPL\_STARTWPARMS** is similar to [**CPL\_DBLCLK**](cpl-dblclk.md) but allows you to pass a string to [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) instead of an **int**. You can use this string as a flexible way to provide detailed directions for execution.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb143-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="fb143-117">Requirements</span></span>



| <span data-ttu-id="fb143-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fb143-118">Requirement</span></span> | <span data-ttu-id="fb143-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="fb143-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="fb143-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fb143-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fb143-121">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fb143-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="fb143-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fb143-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fb143-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fb143-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="fb143-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="fb143-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb143-125"><dt>Cpl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb143-125"><dt>Cpl.h</dt></span></span> </dl> |



 

 
