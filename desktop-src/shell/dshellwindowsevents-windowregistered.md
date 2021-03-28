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
ms.openlocfilehash: b12ed98c6b2a11e5886ed9e76d324a1a6842cda8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "104983066"
---
# <a name="dshellwindowseventswindowregistered-method"></a><span data-ttu-id="fd2c8-103">Méthode DShellWindowsEvents. WindowRegistered</span><span class="sxs-lookup"><span data-stu-id="fd2c8-103">DShellWindowsEvents.WindowRegistered method</span></span>

<span data-ttu-id="fd2c8-104">Appelé lorsqu’une fenêtre est inscrite en tant que fenêtre d’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="fd2c8-104">Called when a window is registered as a Shell window.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd2c8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fd2c8-105">Syntax</span></span>


```JScript
DShellWindowsEvents.WindowRegistered(
  lCookie
)
```



## <a name="parameters"></a><span data-ttu-id="fd2c8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fd2c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd2c8-107">*lCookie* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fd2c8-107">*lCookie* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd2c8-108">Type : **entier**</span><span class="sxs-lookup"><span data-stu-id="fd2c8-108">Type: **Integer**</span></span>

<span data-ttu-id="fd2c8-109">Cookie qui identifie la fenêtre qui a été inscrite.</span><span class="sxs-lookup"><span data-stu-id="fd2c8-109">The cookie that identifies the window that was registered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd2c8-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fd2c8-110">Return value</span></span>

<span data-ttu-id="fd2c8-111">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="fd2c8-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd2c8-112">Notes</span><span class="sxs-lookup"><span data-stu-id="fd2c8-112">Remarks</span></span>

<span data-ttu-id="fd2c8-113">Une fenêtre reçoit un cookie lorsqu’elle est inscrite en tant que fenêtre d’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="fd2c8-113">A window is granted a cookie when it is registered as a Shell window.</span></span> <span data-ttu-id="fd2c8-114">Pour plus d’informations, consultez [**Register**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register).</span><span class="sxs-lookup"><span data-stu-id="fd2c8-114">For more information, see [**Register**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register).</span></span>

## <a name="requirements"></a><span data-ttu-id="fd2c8-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="fd2c8-115">Requirements</span></span>



| <span data-ttu-id="fd2c8-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fd2c8-116">Requirement</span></span> | <span data-ttu-id="fd2c8-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd2c8-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd2c8-118">Produit</span><span class="sxs-lookup"><span data-stu-id="fd2c8-118">Product</span></span><br/> | <span data-ttu-id="fd2c8-119">Internet Explorer 5</span><span class="sxs-lookup"><span data-stu-id="fd2c8-119">Internet Explorer 5</span></span><br/>                                                                                           |
| <span data-ttu-id="fd2c8-120">DLL</span><span class="sxs-lookup"><span data-stu-id="fd2c8-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="fd2c8-121"><dt>Shdocvw.dll (version 5.00.2014.0216 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="fd2c8-121"><dt>Shdocvw.dll (version 5.00.2014.0216 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd2c8-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd2c8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd2c8-123">**DShellWindowsEvents**</span><span class="sxs-lookup"><span data-stu-id="fd2c8-123">**DShellWindowsEvents**</span></span>](dshellwindowsevents.md)
</dt> <dt>

[<span data-ttu-id="fd2c8-124">**WindowRevoked**</span><span class="sxs-lookup"><span data-stu-id="fd2c8-124">**WindowRevoked**</span></span>](dshellwindowsevents-windowrevoked.md)
</dt> <dt>

[<span data-ttu-id="fd2c8-125">**S’inscrire**</span><span class="sxs-lookup"><span data-stu-id="fd2c8-125">**Register**</span></span>](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register)
</dt> <dt>

[<span data-ttu-id="fd2c8-126">**RegisterPending**</span><span class="sxs-lookup"><span data-stu-id="fd2c8-126">**RegisterPending**</span></span>](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-registerpending)
</dt> </dl>

 

 




