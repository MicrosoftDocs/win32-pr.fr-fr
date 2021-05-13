---
description: Appelé lorsqu’une fenêtre est inscrite en tant que fenêtre d’interpréteur de commandes.
title: Méthode DShellWindowsEvents. WindowRegistered
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DShellWindowsEvents.WindowRegistered
api_type:
- COM
api_location:
- Shdocvw.dll
ms.assetid: 7faf758a-daa0-47f5-9f95-61fe3d8286ea
ms.openlocfilehash: 64bf83a88584c5d97994726696d4fb3a1e971bdf
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841450"
---
# <a name="dshellwindowseventswindowregistered-method"></a><span data-ttu-id="3f934-103">Méthode DShellWindowsEvents. WindowRegistered</span><span class="sxs-lookup"><span data-stu-id="3f934-103">DShellWindowsEvents.WindowRegistered method</span></span>

<span data-ttu-id="3f934-104">Appelé lorsqu’une fenêtre est inscrite en tant que fenêtre d’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="3f934-104">Called when a window is registered as a Shell window.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f934-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3f934-105">Syntax</span></span>


```JScript
DShellWindowsEvents.WindowRegistered(
  lCookie
)
```



## <a name="parameters"></a><span data-ttu-id="3f934-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3f934-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f934-107">*lCookie* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3f934-107">*lCookie* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f934-108">Type : **entier**</span><span class="sxs-lookup"><span data-stu-id="3f934-108">Type: **Integer**</span></span>

<span data-ttu-id="3f934-109">Cookie qui identifie la fenêtre qui a été inscrite.</span><span class="sxs-lookup"><span data-stu-id="3f934-109">The cookie that identifies the window that was registered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f934-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3f934-110">Return value</span></span>

<span data-ttu-id="3f934-111">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="3f934-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f934-112">Notes</span><span class="sxs-lookup"><span data-stu-id="3f934-112">Remarks</span></span>

<span data-ttu-id="3f934-113">Une fenêtre reçoit un cookie lorsqu’elle est inscrite en tant que fenêtre d’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="3f934-113">A window is granted a cookie when it is registered as a Shell window.</span></span> <span data-ttu-id="3f934-114">Pour plus d’informations, consultez [**Register**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register).</span><span class="sxs-lookup"><span data-stu-id="3f934-114">For more information, see [**Register**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register).</span></span>

## <a name="requirements"></a><span data-ttu-id="3f934-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3f934-115">Requirements</span></span>



| <span data-ttu-id="3f934-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3f934-116">Requirement</span></span> | <span data-ttu-id="3f934-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="3f934-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f934-118">Produit</span><span class="sxs-lookup"><span data-stu-id="3f934-118">Product</span></span><br/> | <span data-ttu-id="3f934-119">Internet Explorer 5</span><span class="sxs-lookup"><span data-stu-id="3f934-119">Internet Explorer 5</span></span><br/>                                                                                           |
| <span data-ttu-id="3f934-120">DLL</span><span class="sxs-lookup"><span data-stu-id="3f934-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="3f934-121"><dt>Shdocvw.dll (version 5.00.2014.0216 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="3f934-121"><dt>Shdocvw.dll (version 5.00.2014.0216 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f934-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f934-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f934-123">**DShellWindowsEvents**</span><span class="sxs-lookup"><span data-stu-id="3f934-123">**DShellWindowsEvents**</span></span>](dshellwindowsevents.md)
</dt> <dt>

[<span data-ttu-id="3f934-124">**WindowRevoked**</span><span class="sxs-lookup"><span data-stu-id="3f934-124">**WindowRevoked**</span></span>](dshellwindowsevents-windowrevoked.md)
</dt> <dt>

[<span data-ttu-id="3f934-125">**S’inscrire**</span><span class="sxs-lookup"><span data-stu-id="3f934-125">**Register**</span></span>](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register)
</dt> <dt>

[<span data-ttu-id="3f934-126">**RegisterPending**</span><span class="sxs-lookup"><span data-stu-id="3f934-126">**RegisterPending**</span></span>](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-registerpending)
</dt> </dl>

 

 




