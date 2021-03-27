---
description: Avertit un appbar lorsqu’un événement qui peut affecter la taille et la position du appbar.
ms.assetid: 1016a362-4d2b-410e-aec9-c1cc8f497778
title: Message ABN_POSCHANGED (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24b0a800b1c112cba18fbadbba79a999ec83c77e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972086"
---
# <a name="abn_poschanged-message"></a><span data-ttu-id="d745a-103">Message d’ABN \_ POSCHANGED</span><span class="sxs-lookup"><span data-stu-id="d745a-103">ABN\_POSCHANGED message</span></span>

<span data-ttu-id="d745a-104">Avertit un appbar lorsqu’un événement qui peut affecter la taille et la position du appbar.</span><span class="sxs-lookup"><span data-stu-id="d745a-104">Notifies an appbar when an event has occurred that may affect the appbar's size and position.</span></span> <span data-ttu-id="d745a-105">Les événements incluent les modifications de la taille, de la position et de l’état de visibilité de la barre des tâches, ainsi que l’ajout, la suppression ou le redimensionnement d’un autre appbar sur le même côté de l’écran.</span><span class="sxs-lookup"><span data-stu-id="d745a-105">Events include changes in the taskbar's size, position, and visibility state, as well as the addition, removal, or resizing of another appbar on the same side of the screen.</span></span>


```C++
ABN_POSCHANGED
```



## <a name="parameters"></a><span data-ttu-id="d745a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d745a-106">Parameters</span></span>

<span data-ttu-id="d745a-107">Ce message n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="d745a-107">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d745a-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d745a-108">Return value</span></span>

<span data-ttu-id="d745a-109">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="d745a-109">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d745a-110">Notes</span><span class="sxs-lookup"><span data-stu-id="d745a-110">Remarks</span></span>

<span data-ttu-id="d745a-111">Un appbar doit répondre à ce message de notification en envoyant les messages [**ABM \_ QUERYPOS**](abm-querypos.md) et [**ABM \_ SetPos**](abm-setpos.md) .</span><span class="sxs-lookup"><span data-stu-id="d745a-111">An appbar should respond to this notification message by sending the [**ABM\_QUERYPOS**](abm-querypos.md) and [**ABM\_SETPOS**](abm-setpos.md) messages.</span></span> <span data-ttu-id="d745a-112">Si sa position a changé, appbar doit appeler la fonction [**MoveWindow**](/windows/desktop/api/winuser/nf-winuser-movewindow) pour se déplacer vers la nouvelle position.</span><span class="sxs-lookup"><span data-stu-id="d745a-112">If its position has changed, the appbar should call the [**MoveWindow**](/windows/desktop/api/winuser/nf-winuser-movewindow) function to move itself to the new position.</span></span>

## <a name="requirements"></a><span data-ttu-id="d745a-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d745a-113">Requirements</span></span>



| <span data-ttu-id="d745a-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d745a-114">Requirement</span></span> | <span data-ttu-id="d745a-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="d745a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d745a-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d745a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d745a-117">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d745a-117">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d745a-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d745a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d745a-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d745a-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d745a-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="d745a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d745a-121"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d745a-121"><dt>Shellapi.h</dt></span></span> </dl> |



 

