---
description: Récupère le rectangle englobant de la barre des tâches Windows.
ms.assetid: 8072bb2d-05e6-4baa-a7f4-1377b94fdd45
title: Message ABM_GETTASKBARPOS (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cb678b6e7ade1f148d2deb4b0de6c8953f019d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525431"
---
# <a name="abm_gettaskbarpos-message"></a><span data-ttu-id="06c01-103">\_Message ABM GETTASKBARPOS</span><span class="sxs-lookup"><span data-stu-id="06c01-103">ABM\_GETTASKBARPOS message</span></span>

<span data-ttu-id="06c01-104">Récupère le rectangle englobant de la barre des tâches Windows.</span><span class="sxs-lookup"><span data-stu-id="06c01-104">Retrieves the bounding rectangle of the Windows taskbar.</span></span>


```C++
fResult = (BOOL) SHAppBarMessage(ABM_GETTASKBARPOS, pabd);
```



## <a name="parameters"></a><span data-ttu-id="06c01-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="06c01-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06c01-106">*pabd*</span><span class="sxs-lookup"><span data-stu-id="06c01-106">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="06c01-107">Pointeur vers une structure [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) dont le membre **RC** reçoit le rectangle englobant, en coordonnées d’écran, de la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="06c01-107">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure whose **rc** member receives the bounding rectangle, in screen coordinates, of the taskbar.</span></span> <span data-ttu-id="06c01-108">Vous devez spécifier le **cbSize** lors de l’envoi de ce message. tous les autres membres sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="06c01-108">You must specify the **cbSize** when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06c01-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="06c01-109">Return value</span></span>

<span data-ttu-id="06c01-110">Retourne la **valeur true** en cas de réussite ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="06c01-110">Returns **TRUE** if successful; otherwise, **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="06c01-111">Notes</span><span class="sxs-lookup"><span data-stu-id="06c01-111">Remarks</span></span>

<span data-ttu-id="06c01-112">Notez que cela s’applique uniquement à la barre des tâches système.</span><span class="sxs-lookup"><span data-stu-id="06c01-112">Note that this applies only to the system taskbar.</span></span> <span data-ttu-id="06c01-113">D’autres objets, en particulier les barres d’outils fournies avec des logiciels tiers, peuvent également être présents.</span><span class="sxs-lookup"><span data-stu-id="06c01-113">Other objects, particularly toolbars supplied with third-party software, also can be present.</span></span> <span data-ttu-id="06c01-114">Par conséquent, une partie de la zone d’écran non couverte par la barre des tâches Windows peut ne pas être visible pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="06c01-114">As a result, some of the screen area not covered by the Windows taskbar might not be visible to the user.</span></span> <span data-ttu-id="06c01-115">Pour récupérer la zone de l’écran non couverte par la barre des tâches et d’autres barres de l’application, la zone de travail disponible pour votre application, utilisez la fonction [**GetMonitorInfo**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa) .</span><span class="sxs-lookup"><span data-stu-id="06c01-115">To retrieve the area of the screen not covered by both the taskbar and other app bars the working area available to your application , use the [**GetMonitorInfo**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="06c01-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="06c01-116">Requirements</span></span>



| <span data-ttu-id="06c01-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="06c01-117">Requirement</span></span> | <span data-ttu-id="06c01-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="06c01-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="06c01-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="06c01-119">Minimum supported client</span></span><br/> | <span data-ttu-id="06c01-120">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="06c01-120">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="06c01-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="06c01-121">Minimum supported server</span></span><br/> | <span data-ttu-id="06c01-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="06c01-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="06c01-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="06c01-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="06c01-124"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="06c01-124"><dt>Shellapi.h</dt></span></span> </dl> |



 

