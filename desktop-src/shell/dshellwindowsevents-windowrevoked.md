---
description: Appelé lorsque l’inscription d’une fenêtre d’interpréteur de commandes est révoquée.
title: Méthode DShellWindowsEvents. WindowRevoked
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DShellWindowsEvents.WindowRevoked
api_type:
- COM
api_location:
- Shdocvw.dll
ms.assetid: 92e8653f-7f41-4e0b-97e5-429fddc51951
ms.openlocfilehash: 7ed78dcaa545b2321b04aff9ff2f4e711f93c992
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843180"
---
# <a name="dshellwindowseventswindowrevoked-method"></a><span data-ttu-id="c97c1-103">Méthode DShellWindowsEvents. WindowRevoked</span><span class="sxs-lookup"><span data-stu-id="c97c1-103">DShellWindowsEvents.WindowRevoked method</span></span>

<span data-ttu-id="c97c1-104">Appelé lorsque l’inscription d’une fenêtre d’interpréteur de commandes est révoquée.</span><span class="sxs-lookup"><span data-stu-id="c97c1-104">Called when a Shell window's registration is revoked.</span></span>

## <a name="syntax"></a><span data-ttu-id="c97c1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c97c1-105">Syntax</span></span>


```JScript
DShellWindowsEvents.WindowRevoked(
  lCookie
)
```



## <a name="parameters"></a><span data-ttu-id="c97c1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c97c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c97c1-107">*lCookie* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c97c1-107">*lCookie* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c97c1-108">Type : **entier**</span><span class="sxs-lookup"><span data-stu-id="c97c1-108">Type: **Integer**</span></span>

<span data-ttu-id="c97c1-109">Cookie qui identifie la fenêtre qui a été révoquée.</span><span class="sxs-lookup"><span data-stu-id="c97c1-109">The cookie that identifies the window that was revoked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c97c1-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c97c1-110">Return value</span></span>

<span data-ttu-id="c97c1-111">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="c97c1-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c97c1-112">Notes</span><span class="sxs-lookup"><span data-stu-id="c97c1-112">Remarks</span></span>

<span data-ttu-id="c97c1-113">Une fenêtre reçoit un cookie lorsqu’elle est inscrite en tant que fenêtre d’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="c97c1-113">A window is granted a cookie when it is registered as a Shell window.</span></span> <span data-ttu-id="c97c1-114">Pour plus d’informations, consultez [**Register**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register).</span><span class="sxs-lookup"><span data-stu-id="c97c1-114">For more information, see [**Register**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register).</span></span>

## <a name="requirements"></a><span data-ttu-id="c97c1-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c97c1-115">Requirements</span></span>



| <span data-ttu-id="c97c1-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c97c1-116">Requirement</span></span> | <span data-ttu-id="c97c1-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="c97c1-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c97c1-118">Produit</span><span class="sxs-lookup"><span data-stu-id="c97c1-118">Product</span></span><br/> | <span data-ttu-id="c97c1-119">Internet Explorer 5</span><span class="sxs-lookup"><span data-stu-id="c97c1-119">Internet Explorer 5</span></span><br/>                                                                                           |
| <span data-ttu-id="c97c1-120">DLL</span><span class="sxs-lookup"><span data-stu-id="c97c1-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="c97c1-121"><dt>Shdocvw.dll (version 5.00.2014.0216 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="c97c1-121"><dt>Shdocvw.dll (version 5.00.2014.0216 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c97c1-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c97c1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c97c1-123">**DShellWindowsEvents**</span><span class="sxs-lookup"><span data-stu-id="c97c1-123">**DShellWindowsEvents**</span></span>](dshellwindowsevents.md)
</dt> <dt>

[<span data-ttu-id="c97c1-124">**WindowRegistered**</span><span class="sxs-lookup"><span data-stu-id="c97c1-124">**WindowRegistered**</span></span>](dshellwindowsevents-windowregistered.md)
</dt> <dt>

[<span data-ttu-id="c97c1-125">**Révoquer**</span><span class="sxs-lookup"><span data-stu-id="c97c1-125">**Revoke**</span></span>](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-revoke)
</dt> </dl>

 

 




