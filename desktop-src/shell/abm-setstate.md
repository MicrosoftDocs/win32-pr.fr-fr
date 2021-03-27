---
description: Définit les États Masquer automatiquement et toujours en haut de la barre des tâches Windows.
title: Message ABM_SETSTATE (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: a60e156d-19ef-49b9-83fc-138d1a2169f2
api_name:
- ABM_SETSTATE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3cd21ca49d1a57d870c26e010420f978f1d9b88a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972094"
---
# <a name="abm_setstate-message"></a><span data-ttu-id="1424d-103">\_Message ABM SETSTATE</span><span class="sxs-lookup"><span data-stu-id="1424d-103">ABM\_SETSTATE message</span></span>

<span data-ttu-id="1424d-104">Définit les États Masquer automatiquement et toujours en haut de la barre des tâches Windows.</span><span class="sxs-lookup"><span data-stu-id="1424d-104">Sets the autohide and always-on-top states of the Windows taskbar.</span></span>


```C++
SHAppBarMessage(ABM_SETSTATE, pabd); 
```



## <a name="parameters"></a><span data-ttu-id="1424d-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1424d-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1424d-106">*pabd*</span><span class="sxs-lookup"><span data-stu-id="1424d-106">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="1424d-107">Pointeur vers une structure [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) .</span><span class="sxs-lookup"><span data-stu-id="1424d-107">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span> <span data-ttu-id="1424d-108">Vous devez spécifier les membres **cbSize** et **HWND** lors de l’envoi de ce message.</span><span class="sxs-lookup"><span data-stu-id="1424d-108">You must specify the **cbSize** and **hWnd** members when sending this message.</span></span> <span data-ttu-id="1424d-109">Les données de l’état souhaité sont envoyées dans le membre **lParam** en utilisant l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="1424d-109">Data for the desired state is sent in the **lParam** member using one of the following values.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="1424d-110"><span id="0"></span>**entre**</span><span class="sxs-lookup"><span data-stu-id="1424d-110"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="1424d-111">Masquage automatique et Always on-Top</span><span class="sxs-lookup"><span data-stu-id="1424d-111">Autohide and always-on-top both off</span></span>

</dd> <dt>

<span id="ABS_ALWAYSONTOP"></span><span id="abs_alwaysontop"></span>

<span data-ttu-id="1424d-112"><span id="ABS_ALWAYSONTOP"></span><span id="abs_alwaysontop"></span>**\_ALWAYSONTOP ABS**</span><span class="sxs-lookup"><span data-stu-id="1424d-112"><span id="ABS_ALWAYSONTOP"></span><span id="abs_alwaysontop"></span>**ABS\_ALWAYSONTOP**</span></span>


</dt> <dd>

<span data-ttu-id="1424d-113">Always on-Top on, masquage automatique désactivé</span><span class="sxs-lookup"><span data-stu-id="1424d-113">Always-on-top on, autohide off</span></span>

</dd> <dt>

<span id="ABS_AUTOHIDE"></span><span id="abs_autohide"></span>

<span data-ttu-id="1424d-114"><span id="ABS_AUTOHIDE"></span><span id="abs_autohide"></span>**\_masquage automatique ABS**</span><span class="sxs-lookup"><span data-stu-id="1424d-114"><span id="ABS_AUTOHIDE"></span><span id="abs_autohide"></span>**ABS\_AUTOHIDE**</span></span>


</dt> <dd>

<span data-ttu-id="1424d-115">Masquer automatiquement activé, toujours en haut</span><span class="sxs-lookup"><span data-stu-id="1424d-115">Autohide on, always-on-top off</span></span>

</dd> <dt>

<span id="ABS_AUTOHIDE___ABS_ALWAYSONTOP"></span><span id="abs_autohide___abs_alwaysontop"></span>

<span data-ttu-id="1424d-116"><span id="ABS_AUTOHIDE___ABS_ALWAYSONTOP"></span><span id="abs_autohide___abs_alwaysontop"></span>**ABS- \_ Masquer automatiquement \| ABS \_ ALWAYSONTOP**</span><span class="sxs-lookup"><span data-stu-id="1424d-116"><span id="ABS_AUTOHIDE___ABS_ALWAYSONTOP"></span><span id="abs_autohide___abs_alwaysontop"></span>**ABS\_AUTOHIDE \| ABS\_ALWAYSONTOP**</span></span>


</dt> <dd>

<span data-ttu-id="1424d-117">Masquer automatiquement et toujours en haut sur</span><span class="sxs-lookup"><span data-stu-id="1424d-117">Autohide and always-on-top both on</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1424d-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1424d-118">Return value</span></span>

<span data-ttu-id="1424d-119">Retourne toujours la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="1424d-119">Always returns **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1424d-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1424d-120">Requirements</span></span>



| <span data-ttu-id="1424d-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1424d-121">Requirement</span></span> | <span data-ttu-id="1424d-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="1424d-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1424d-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1424d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1424d-124">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1424d-124">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="1424d-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1424d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1424d-126">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1424d-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1424d-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="1424d-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="1424d-128"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1424d-128"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




