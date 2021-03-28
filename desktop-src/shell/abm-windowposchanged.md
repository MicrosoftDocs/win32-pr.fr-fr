---
description: Notifie le système lorsque la position d’un appbar a changé. Un appbar doit appeler ce message en réponse au message WM \_ WINDOWPOSCHANGED.
ms.assetid: 8ca51f5f-b6cf-4f2c-98f4-69c992679320
title: Message ABM_WINDOWPOSCHANGED (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29c8ea6fab6960678ad030a0c1817ad5f8aaae29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484393"
---
# <a name="abm_windowposchanged-message"></a><span data-ttu-id="72d38-104">\_Message ABM WINDOWPOSCHANGED</span><span class="sxs-lookup"><span data-stu-id="72d38-104">ABM\_WINDOWPOSCHANGED message</span></span>

<span data-ttu-id="72d38-105">Notifie le système lorsque la position d’un appbar a changé.</span><span class="sxs-lookup"><span data-stu-id="72d38-105">Notifies the system when an appbar's position has changed.</span></span> <span data-ttu-id="72d38-106">Un appbar doit appeler ce message en réponse au message [**WM \_ WINDOWPOSCHANGED**](/windows/desktop/winmsg/wm-windowposchanged) .</span><span class="sxs-lookup"><span data-stu-id="72d38-106">An appbar should call this message in response to the [**WM\_WINDOWPOSCHANGED**](/windows/desktop/winmsg/wm-windowposchanged) message.</span></span>


```C++
SHAppBarMessage(ABM_WINDOWPOSCHANGED, pabd); 
```



## <a name="parameters"></a><span data-ttu-id="72d38-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="72d38-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72d38-108">*pabd*</span><span class="sxs-lookup"><span data-stu-id="72d38-108">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="72d38-109">Pointeur vers une structure [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) qui identifie le appbar à activer.</span><span class="sxs-lookup"><span data-stu-id="72d38-109">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure that identifies the appbar to activate.</span></span> <span data-ttu-id="72d38-110">Vous devez spécifier les membres **cbSize** et **HWND** lors de l’envoi de ce message. tous les autres membres sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="72d38-110">You must specify the **cbSize** and **hWnd** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72d38-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="72d38-111">Return value</span></span>

<span data-ttu-id="72d38-112">Retourne toujours la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="72d38-112">Always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="72d38-113">Notes</span><span class="sxs-lookup"><span data-stu-id="72d38-113">Remarks</span></span>

<span data-ttu-id="72d38-114">Ce message est ignoré si le membre **HWND** de la structure vers laquelle pointe *pabd* identifie un appbar de masquage automatique.</span><span class="sxs-lookup"><span data-stu-id="72d38-114">This message is ignored if the **hWnd** member of the structure pointed to by *pabd* identifies an autohide appbar.</span></span>

## <a name="requirements"></a><span data-ttu-id="72d38-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="72d38-115">Requirements</span></span>



| <span data-ttu-id="72d38-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="72d38-116">Requirement</span></span> | <span data-ttu-id="72d38-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="72d38-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="72d38-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="72d38-118">Minimum supported client</span></span><br/> | <span data-ttu-id="72d38-119">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="72d38-119">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="72d38-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="72d38-120">Minimum supported server</span></span><br/> | <span data-ttu-id="72d38-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="72d38-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="72d38-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="72d38-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="72d38-123"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="72d38-123"><dt>Shellapi.h</dt></span></span> </dl> |



 

