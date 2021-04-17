---
description: Demande une taille et une position à l’écran pour un appbar.
ms.assetid: 061a30fb-a68a-464e-ad8c-0bda672b57d9
title: Message ABM_QUERYPOS (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08f25ef636b2c55d8442df49f86a59b537694c31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318122"
---
# <a name="abm_querypos-message"></a><span data-ttu-id="928e3-103">\_Message ABM QUERYPOS</span><span class="sxs-lookup"><span data-stu-id="928e3-103">ABM\_QUERYPOS message</span></span>

<span data-ttu-id="928e3-104">Demande une taille et une position à l’écran pour un appbar.</span><span class="sxs-lookup"><span data-stu-id="928e3-104">Requests a size and screen position for an appbar.</span></span> <span data-ttu-id="928e3-105">Lorsque la demande est effectuée, le message propose un bord d’écran et un rectangle englobant pour le appbar.</span><span class="sxs-lookup"><span data-stu-id="928e3-105">When the request is made, the message proposes a screen edge and a bounding rectangle for the appbar.</span></span> <span data-ttu-id="928e3-106">Le système ajuste le rectangle englobant de sorte que le appbar n’interfère pas avec la barre des tâches Windows ou tout autre barres.</span><span class="sxs-lookup"><span data-stu-id="928e3-106">The system adjusts the bounding rectangle so that the appbar does not interfere with the Windows taskbar or any other appbars.</span></span>


```C++
SHAppBarMessage(ABM_QUERYPOS, pabd); 
```



## <a name="parameters"></a><span data-ttu-id="928e3-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="928e3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="928e3-108">*pabd*</span><span class="sxs-lookup"><span data-stu-id="928e3-108">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="928e3-109">Pointeur vers une structure [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) .</span><span class="sxs-lookup"><span data-stu-id="928e3-109">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span> <span data-ttu-id="928e3-110">Le membre **uEdge** spécifie un bord d’écran et le membre **RC** contient le rectangle englobant proposé.</span><span class="sxs-lookup"><span data-stu-id="928e3-110">The **uEdge** member specifies a screen edge, and the **rc** member contains the proposed bounding rectangle.</span></span> <span data-ttu-id="928e3-111">Lorsque la fonction [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) retourne, **RC** contient le rectangle englobant approuvé.</span><span class="sxs-lookup"><span data-stu-id="928e3-111">When the [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) function returns, **rc** contains the approved bounding rectangle.</span></span> <span data-ttu-id="928e3-112">Vous devez spécifier les membres **cbSize**, **HWND**, **uEdge** et **RC** lors de l’envoi de ce message. tous les autres membres sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="928e3-112">You must specify the **cbSize**, **hWnd**, **uEdge**, and **rc** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="928e3-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="928e3-113">Return value</span></span>

<span data-ttu-id="928e3-114">Retourne toujours la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="928e3-114">Always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="928e3-115">Notes</span><span class="sxs-lookup"><span data-stu-id="928e3-115">Remarks</span></span>

<span data-ttu-id="928e3-116">Un appbar doit envoyer ce message avant d’envoyer le message [**ABM \_ SetPos**](abm-setpos.md) .</span><span class="sxs-lookup"><span data-stu-id="928e3-116">An appbar should send this message before sending the [**ABM\_SETPOS**](abm-setpos.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="928e3-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="928e3-117">Requirements</span></span>



| <span data-ttu-id="928e3-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="928e3-118">Requirement</span></span> | <span data-ttu-id="928e3-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="928e3-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="928e3-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="928e3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="928e3-121">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="928e3-121">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="928e3-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="928e3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="928e3-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="928e3-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="928e3-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="928e3-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="928e3-125"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="928e3-125"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




