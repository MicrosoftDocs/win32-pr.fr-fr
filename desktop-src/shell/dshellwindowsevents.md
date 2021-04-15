---
description: Reçoit les événements d’inscription de la fenêtre IShellWindows.
ms.assetid: c340296d-f8eb-43a1-809d-912ea7412fe2
title: Objet DShellWindowsEvents (exdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DShellWindowsEvents
api_type:
- COM
api_location:
- Shdocvw.dll
ms.openlocfilehash: 7df1571556b5f2942f181b4c88b22ff3bc83f273
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "104983015"
---
# <a name="dshellwindowsevents-object"></a><span data-ttu-id="0bba7-103">Objet DShellWindowsEvents</span><span class="sxs-lookup"><span data-stu-id="0bba7-103">DShellWindowsEvents object</span></span>

<span data-ttu-id="0bba7-104">Reçoit les événements d’inscription de la fenêtre [**IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows) .</span><span class="sxs-lookup"><span data-stu-id="0bba7-104">Receives [**IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows) window registration events.</span></span>

## <a name="members"></a><span data-ttu-id="0bba7-105">Membres</span><span class="sxs-lookup"><span data-stu-id="0bba7-105">Members</span></span>

<span data-ttu-id="0bba7-106">L’objet **DShellWindowsEvents** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0bba7-106">The **DShellWindowsEvents** object has these types of members:</span></span>

-   [<span data-ttu-id="0bba7-107">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0bba7-107">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0bba7-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0bba7-108">Methods</span></span>

<span data-ttu-id="0bba7-109">L’objet **DShellWindowsEvents** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="0bba7-109">The **DShellWindowsEvents** object has these methods.</span></span>



| <span data-ttu-id="0bba7-110">Méthode</span><span class="sxs-lookup"><span data-stu-id="0bba7-110">Method</span></span>                                                           | <span data-ttu-id="0bba7-111">Description</span><span class="sxs-lookup"><span data-stu-id="0bba7-111">Description</span></span>                                                       |
|:-----------------------------------------------------------------|:------------------------------------------------------------------|
| [<span data-ttu-id="0bba7-112">**WindowRegistered**</span><span class="sxs-lookup"><span data-stu-id="0bba7-112">**WindowRegistered**</span></span>](dshellwindowsevents-windowregistered.md) | <span data-ttu-id="0bba7-113">Appelé lorsqu’une fenêtre est inscrite en tant que fenêtre d’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="0bba7-113">Called when a window is registered as a Shell window.</span></span> <br/> |
| [<span data-ttu-id="0bba7-114">**WindowRevoked**</span><span class="sxs-lookup"><span data-stu-id="0bba7-114">**WindowRevoked**</span></span>](dshellwindowsevents-windowrevoked.md)       | <span data-ttu-id="0bba7-115">Appelé lorsque l’inscription d’une fenêtre d’interpréteur de commandes est révoquée.</span><span class="sxs-lookup"><span data-stu-id="0bba7-115">Called when a Shell window's registration is revoked.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="0bba7-116">Notes</span><span class="sxs-lookup"><span data-stu-id="0bba7-116">Remarks</span></span>

<span data-ttu-id="0bba7-117">Utilisez **DShellWindowsEvents** pour surveiller le moment où une fenêtre d’interpréteur de commandes est inscrite ou révoquée.</span><span class="sxs-lookup"><span data-stu-id="0bba7-117">Use **DShellWindowsEvents** to monitor when a Shell window is registered or revoked.</span></span> <span data-ttu-id="0bba7-118">Pour plus d’informations, consultez [**IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows).</span><span class="sxs-lookup"><span data-stu-id="0bba7-118">For more information, see [**IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows).</span></span>

## <a name="requirements"></a><span data-ttu-id="0bba7-119">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0bba7-119">Requirements</span></span>



| <span data-ttu-id="0bba7-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0bba7-120">Requirement</span></span> | <span data-ttu-id="0bba7-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="0bba7-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bba7-122">Produit</span><span class="sxs-lookup"><span data-stu-id="0bba7-122">Product</span></span><br/> | <span data-ttu-id="0bba7-123">Internet Explorer 5</span><span class="sxs-lookup"><span data-stu-id="0bba7-123">Internet Explorer 5</span></span><br/>                                                                                           |
| <span data-ttu-id="0bba7-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="0bba7-124">Header</span></span><br/>  | <dl> <span data-ttu-id="0bba7-125"><dt>Exdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0bba7-125"><dt>Exdisp.h</dt></span></span> </dl>                                      |
| <span data-ttu-id="0bba7-126">DLL</span><span class="sxs-lookup"><span data-stu-id="0bba7-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="0bba7-127"><dt>Shdocvw.dll (version 5.00.2014.0216 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="0bba7-127"><dt>Shdocvw.dll (version 5.00.2014.0216 or later)</dt></span></span> </dl> |
| <span data-ttu-id="0bba7-128">IID</span><span class="sxs-lookup"><span data-stu-id="0bba7-128">IID</span></span><br/>     | <span data-ttu-id="0bba7-129">IID \_ IShellWindows</span><span class="sxs-lookup"><span data-stu-id="0bba7-129">IID\_IShellWindows</span></span><br/>                                                                                            |



## <a name="see-also"></a><span data-ttu-id="0bba7-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0bba7-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bba7-131">**ShellWindows**</span><span class="sxs-lookup"><span data-stu-id="0bba7-131">**ShellWindows**</span></span>](shellwindows.md)
</dt> </dl>

 

 




