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
ms.openlocfilehash: b036bdde2916c2fa037d1b6e286a2096d9e1d8bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "104983082"
---
# <a name="dshellwindowseventswindowrevoked-method"></a><span data-ttu-id="4443f-103">Méthode DShellWindowsEvents. WindowRevoked</span><span class="sxs-lookup"><span data-stu-id="4443f-103">DShellWindowsEvents.WindowRevoked method</span></span>

<span data-ttu-id="4443f-104">Appelé lorsque l’inscription d’une fenêtre d’interpréteur de commandes est révoquée.</span><span class="sxs-lookup"><span data-stu-id="4443f-104">Called when a Shell window's registration is revoked.</span></span>

## <a name="syntax"></a><span data-ttu-id="4443f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4443f-105">Syntax</span></span>


```JScript
DShellWindowsEvents.WindowRevoked(
  lCookie
)
```



## <a name="parameters"></a><span data-ttu-id="4443f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4443f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4443f-107">*lCookie* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4443f-107">*lCookie* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4443f-108">Type : **entier**</span><span class="sxs-lookup"><span data-stu-id="4443f-108">Type: **Integer**</span></span>

<span data-ttu-id="4443f-109">Cookie qui identifie la fenêtre qui a été révoquée.</span><span class="sxs-lookup"><span data-stu-id="4443f-109">The cookie that identifies the window that was revoked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4443f-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4443f-110">Return value</span></span>

<span data-ttu-id="4443f-111">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="4443f-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4443f-112">Notes</span><span class="sxs-lookup"><span data-stu-id="4443f-112">Remarks</span></span>

<span data-ttu-id="4443f-113">Une fenêtre reçoit un cookie lorsqu’elle est inscrite en tant que fenêtre d’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="4443f-113">A window is granted a cookie when it is registered as a Shell window.</span></span> <span data-ttu-id="4443f-114">Pour plus d’informations, consultez [**Register**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register).</span><span class="sxs-lookup"><span data-stu-id="4443f-114">For more information, see [**Register**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register).</span></span>

## <a name="requirements"></a><span data-ttu-id="4443f-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="4443f-115">Requirements</span></span>



| <span data-ttu-id="4443f-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4443f-116">Requirement</span></span> | <span data-ttu-id="4443f-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="4443f-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4443f-118">Produit</span><span class="sxs-lookup"><span data-stu-id="4443f-118">Product</span></span><br/> | <span data-ttu-id="4443f-119">Internet Explorer 5</span><span class="sxs-lookup"><span data-stu-id="4443f-119">Internet Explorer 5</span></span><br/>                                                                                           |
| <span data-ttu-id="4443f-120">DLL</span><span class="sxs-lookup"><span data-stu-id="4443f-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="4443f-121"><dt>Shdocvw.dll (version 5.00.2014.0216 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="4443f-121"><dt>Shdocvw.dll (version 5.00.2014.0216 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4443f-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4443f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4443f-123">**DShellWindowsEvents**</span><span class="sxs-lookup"><span data-stu-id="4443f-123">**DShellWindowsEvents**</span></span>](dshellwindowsevents.md)
</dt> <dt>

[<span data-ttu-id="4443f-124">**WindowRegistered**</span><span class="sxs-lookup"><span data-stu-id="4443f-124">**WindowRegistered**</span></span>](dshellwindowsevents-windowregistered.md)
</dt> <dt>

[<span data-ttu-id="4443f-125">**Révoquer**</span><span class="sxs-lookup"><span data-stu-id="4443f-125">**Revoke**</span></span>](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-revoke)
</dt> </dl>

 

 




