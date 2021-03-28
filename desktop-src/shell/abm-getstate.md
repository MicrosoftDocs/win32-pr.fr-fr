---
description: Récupère les États Masquer automatiquement et toujours en haut de la barre des tâches Windows.
title: Message ABM_GETSTATE (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 18e16752-16be-492b-a4fa-c951e18dc86c
api_name:
- ABM_GETSTATE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 71225cd8d93de09a07cb0049066e52be08c18a36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318125"
---
# <a name="abm_getstate-message"></a><span data-ttu-id="b30ab-103">\_Message ABM GETSTATE</span><span class="sxs-lookup"><span data-stu-id="b30ab-103">ABM\_GETSTATE message</span></span>

<span data-ttu-id="b30ab-104">Récupère les États Masquer automatiquement et toujours en haut de la barre des tâches Windows.</span><span class="sxs-lookup"><span data-stu-id="b30ab-104">Retrieves the autohide and always-on-top states of the Windows taskbar.</span></span>


```C++
uState = (UINT) SHAppBarMessage(ABM_GETSTATE, pabd);
```



## <a name="parameters"></a><span data-ttu-id="b30ab-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b30ab-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b30ab-106">*pabd*</span><span class="sxs-lookup"><span data-stu-id="b30ab-106">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="b30ab-107">Pointeur vers une structure [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) .</span><span class="sxs-lookup"><span data-stu-id="b30ab-107">Pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span> <span data-ttu-id="b30ab-108">Vous devez spécifier le membre **cbSize** lors de l’envoi de ce message. tous les autres membres sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="b30ab-108">You must specify the **cbSize** member when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b30ab-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b30ab-109">Return value</span></span>

<span data-ttu-id="b30ab-110">Retourne zéro si la barre des tâches n’est ni dans l’état de masquage automatique ni toujours en haut.</span><span class="sxs-lookup"><span data-stu-id="b30ab-110">Returns zero if the taskbar is neither in the autohide nor always-on-top state.</span></span> <span data-ttu-id="b30ab-111">Dans le cas contraire, la valeur de retour est l’une des valeurs suivantes, ou les deux :</span><span class="sxs-lookup"><span data-stu-id="b30ab-111">Otherwise, the return value is one or both of the following:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b30ab-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="b30ab-112">Return code</span></span></th>
<th><span data-ttu-id="b30ab-113">Description</span><span class="sxs-lookup"><span data-stu-id="b30ab-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="b30ab-114"><dt><strong>ABS_ALWAYSONTOP</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b30ab-114"><dt><strong>ABS_ALWAYSONTOP</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="b30ab-115">La barre des tâches est dans l’État Always on Top.</span><span class="sxs-lookup"><span data-stu-id="b30ab-115">The taskbar is in the always-on-top state.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="b30ab-116">À partir de Windows 7, ABS_ALWAYSONTOP n’est plus renvoyé car la barre des tâches est toujours dans cet État.</span><span class="sxs-lookup"><span data-stu-id="b30ab-116">As of Windows 7, ABS_ALWAYSONTOP is no longer returned because the taskbar is always in that state.</span></span> <span data-ttu-id="b30ab-117">Le code plus ancien doit être mis à jour pour ignorer l’absence de cette valeur dans ne pas supposer que la valeur de retour signifie que la barre des tâches ne se trouve pas dans l’État Always on Top.</span><span class="sxs-lookup"><span data-stu-id="b30ab-117">Older code should be updated to ignore the absence of this value in not assume that return value to mean that the taskbar is not in the always-on-top state.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="b30ab-118"><dt><strong>ABS_AUTOHIDE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b30ab-118"><dt><strong>ABS_AUTOHIDE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="b30ab-119">La barre des tâches est dans l’État Masquer automatiquement.</span><span class="sxs-lookup"><span data-stu-id="b30ab-119">The taskbar is in the autohide state.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="b30ab-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b30ab-120">Requirements</span></span>



| <span data-ttu-id="b30ab-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b30ab-121">Requirement</span></span> | <span data-ttu-id="b30ab-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="b30ab-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b30ab-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b30ab-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b30ab-124">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b30ab-124">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b30ab-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b30ab-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b30ab-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b30ab-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b30ab-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="b30ab-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b30ab-128"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b30ab-128"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




