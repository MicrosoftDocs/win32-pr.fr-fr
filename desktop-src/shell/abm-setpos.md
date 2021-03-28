---
description: Définit la taille et la position à l’écran d’un appbar.
ms.assetid: b3c56278-b9a2-4e08-bf98-7b3e4c8bd082
title: Message ABM_SETPOS (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6886249f42638745ca038aa1f216ddc995f0e7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525426"
---
# <a name="abm_setpos-message"></a><span data-ttu-id="18607-103">\_Message ABM SetPos</span><span class="sxs-lookup"><span data-stu-id="18607-103">ABM\_SETPOS message</span></span>

<span data-ttu-id="18607-104">Définit la taille et la position à l’écran d’un appbar.</span><span class="sxs-lookup"><span data-stu-id="18607-104">Sets the size and screen position of an appbar.</span></span> <span data-ttu-id="18607-105">Le message spécifie un bord d’écran et le rectangle englobant pour le appbar.</span><span class="sxs-lookup"><span data-stu-id="18607-105">The message specifies a screen edge and the bounding rectangle for the appbar.</span></span> <span data-ttu-id="18607-106">Le système peut ajuster le rectangle englobant de sorte que le appbar n’interfère pas avec la barre des tâches Windows ou tout autre barres.</span><span class="sxs-lookup"><span data-stu-id="18607-106">The system may adjust the bounding rectangle so that the appbar does not interfere with the Windows taskbar or any other appbars.</span></span>


```C++
SHAppBarMessage(ABM_SETPOS, pabd); 
```



## <a name="parameters"></a><span data-ttu-id="18607-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="18607-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18607-108">*pabd*</span><span class="sxs-lookup"><span data-stu-id="18607-108">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="18607-109">Pointeur vers une structure [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) .</span><span class="sxs-lookup"><span data-stu-id="18607-109">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span> <span data-ttu-id="18607-110">Le membre **uEdge** spécifie un bord d’écran et le membre **RC** contient le rectangle englobant.</span><span class="sxs-lookup"><span data-stu-id="18607-110">The **uEdge** member specifies a screen edge, and the **rc** member contains the bounding rectangle.</span></span> <span data-ttu-id="18607-111">Lorsque la fonction [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) retourne, **RC** contient le rectangle englobant approuvé.</span><span class="sxs-lookup"><span data-stu-id="18607-111">When the [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) function returns, **rc** contains the approved bounding rectangle.</span></span> <span data-ttu-id="18607-112">Vous devez spécifier les membres **cbSize**, **HWND**, **uEdge** et **RC** lors de l’envoi de ce message. tous les autres membres sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="18607-112">You must specify the **cbSize**, **hWnd**, **uEdge**, and **rc** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18607-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="18607-113">Return value</span></span>

<span data-ttu-id="18607-114">Retourne toujours la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="18607-114">Always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="18607-115">Notes</span><span class="sxs-lookup"><span data-stu-id="18607-115">Remarks</span></span>

<span data-ttu-id="18607-116">Ce message amène le système à envoyer le message de notification [**ABN \_ POSCHANGED**](abn-poschanged.md) à tous les barres.</span><span class="sxs-lookup"><span data-stu-id="18607-116">This message causes the system to send the [**ABN\_POSCHANGED**](abn-poschanged.md) notification message to all appbars.</span></span>

## <a name="requirements"></a><span data-ttu-id="18607-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="18607-117">Requirements</span></span>



| <span data-ttu-id="18607-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="18607-118">Requirement</span></span> | <span data-ttu-id="18607-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="18607-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="18607-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18607-120">Minimum supported client</span></span><br/> | <span data-ttu-id="18607-121">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="18607-121">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="18607-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18607-122">Minimum supported server</span></span><br/> | <span data-ttu-id="18607-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="18607-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="18607-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="18607-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="18607-125"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="18607-125"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




