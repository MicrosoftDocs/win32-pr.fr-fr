---
description: Annule l’inscription d’un appbar en le supprimant de la liste interne du système. Le système n’envoie plus de messages de notification à appbar ou empêche d’autres applications d’utiliser la zone d’écran utilisée par le appbar.
title: Message ABM_REMOVE (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3da73a52-3dbb-4133-a9bd-86540e1c4154
api_name:
- ABM_REMOVE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7f4530869b9f68772c28fefd6130ff8e4b6ffbec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862138"
---
# <a name="abm_remove-message"></a><span data-ttu-id="47e8a-104">ABM \_ supprimer le message</span><span class="sxs-lookup"><span data-stu-id="47e8a-104">ABM\_REMOVE message</span></span>

<span data-ttu-id="47e8a-105">Annule l’inscription d’un appbar en le supprimant de la liste interne du système.</span><span class="sxs-lookup"><span data-stu-id="47e8a-105">Unregisters an appbar by removing it from the system's internal list.</span></span> <span data-ttu-id="47e8a-106">Le système n’envoie plus de messages de notification à appbar ou empêche d’autres applications d’utiliser la zone d’écran utilisée par le appbar.</span><span class="sxs-lookup"><span data-stu-id="47e8a-106">The system no longer sends notification messages to the appbar or prevents other applications from using the screen area used by the appbar.</span></span>


```C++
                SHAppBarMessage(ABM_REMOVE, pabd); 
            
```



## <a name="parameters"></a><span data-ttu-id="47e8a-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="47e8a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47e8a-108">*pabd*</span><span class="sxs-lookup"><span data-stu-id="47e8a-108">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="47e8a-109">Pointeur vers une structure [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) qui contient le handle du appbar dont l’inscription doit être annulée.</span><span class="sxs-lookup"><span data-stu-id="47e8a-109">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure that contains the handle to the appbar to unregister.</span></span> <span data-ttu-id="47e8a-110">Vous devez spécifier les membres **cbSize** et **HWND** lors de l’envoi de ce message. tous les autres membres sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="47e8a-110">You must specify the **cbSize** and **hWnd** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47e8a-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="47e8a-111">Return value</span></span>

<span data-ttu-id="47e8a-112">Retourne toujours la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="47e8a-112">Always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="47e8a-113">Notes</span><span class="sxs-lookup"><span data-stu-id="47e8a-113">Remarks</span></span>

<span data-ttu-id="47e8a-114">Ce message amène le système à envoyer le message de notification [**ABN \_ POSCHANGED**](abn-poschanged.md) à tous les barres.</span><span class="sxs-lookup"><span data-stu-id="47e8a-114">This message causes the system to send the [**ABN\_POSCHANGED**](abn-poschanged.md) notification message to all appbars.</span></span>

## <a name="requirements"></a><span data-ttu-id="47e8a-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="47e8a-115">Requirements</span></span>



| <span data-ttu-id="47e8a-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="47e8a-116">Requirement</span></span> | <span data-ttu-id="47e8a-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="47e8a-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="47e8a-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="47e8a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="47e8a-119">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="47e8a-119">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="47e8a-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="47e8a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="47e8a-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="47e8a-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="47e8a-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="47e8a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="47e8a-123"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="47e8a-123"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




