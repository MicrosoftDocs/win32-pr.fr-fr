---
description: Indique au système qu’un appbar a été activé. Un appbar doit appeler ce message en réponse au message WM \_ Activate.
ms.assetid: 16011302-7c2d-4c34-9953-51cceb96e4b3
title: Message ABM_ACTIVATE (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94a44bcc33efcd3d1a9af5e7e2abca33893e9fe9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112366"
---
# <a name="abm_activate-message"></a><span data-ttu-id="1aa3c-104">ABM \_ activer le message</span><span class="sxs-lookup"><span data-stu-id="1aa3c-104">ABM\_ACTIVATE message</span></span>

<span data-ttu-id="1aa3c-105">Indique au système qu’un appbar a été activé.</span><span class="sxs-lookup"><span data-stu-id="1aa3c-105">Notifies the system that an appbar has been activated.</span></span> <span data-ttu-id="1aa3c-106">Un appbar doit appeler ce message en réponse au message [**WM \_ Activate**](/windows/desktop/inputdev/wm-activate) .</span><span class="sxs-lookup"><span data-stu-id="1aa3c-106">An appbar should call this message in response to the [**WM\_ACTIVATE**](/windows/desktop/inputdev/wm-activate) message.</span></span>


```C++

SHAppBarMessage(ABM_ACTIVATE, pabd); 

            
```



## <a name="parameters"></a><span data-ttu-id="1aa3c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1aa3c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1aa3c-108">*pabd*</span><span class="sxs-lookup"><span data-stu-id="1aa3c-108">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="1aa3c-109">Pointeur vers une structure [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) qui identifie le appbar à activer.</span><span class="sxs-lookup"><span data-stu-id="1aa3c-109">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure that identifies the appbar to activate.</span></span> <span data-ttu-id="1aa3c-110">Vous devez spécifier les membres **cbSize** et **HWND** lors de l’envoi de ce message. tous les autres membres sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="1aa3c-110">You must specify the **cbSize** and **hWnd** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1aa3c-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1aa3c-111">Return value</span></span>

<span data-ttu-id="1aa3c-112">Retourne toujours la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="1aa3c-112">Always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1aa3c-113">Notes</span><span class="sxs-lookup"><span data-stu-id="1aa3c-113">Remarks</span></span>

<span data-ttu-id="1aa3c-114">Ce message est ignoré si le membre **HWND** de la structure vers laquelle pointe *pabd* identifie un appbar de masquage automatique.</span><span class="sxs-lookup"><span data-stu-id="1aa3c-114">This message is ignored if the **hWnd** member of the structure pointed to by *pabd* identifies an autohide appbar.</span></span> <span data-ttu-id="1aa3c-115">Le système définit automatiquement l’ordre de plan pour les barres de masquage automatique.</span><span class="sxs-lookup"><span data-stu-id="1aa3c-115">The system automatically sets the z-order for autohide appbars.</span></span>

## <a name="requirements"></a><span data-ttu-id="1aa3c-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1aa3c-116">Requirements</span></span>



| <span data-ttu-id="1aa3c-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1aa3c-117">Requirement</span></span> | <span data-ttu-id="1aa3c-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="1aa3c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1aa3c-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1aa3c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1aa3c-120">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1aa3c-120">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="1aa3c-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1aa3c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1aa3c-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1aa3c-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1aa3c-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="1aa3c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1aa3c-124"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1aa3c-124"><dt>Shellapi.h</dt></span></span> </dl> |



 

