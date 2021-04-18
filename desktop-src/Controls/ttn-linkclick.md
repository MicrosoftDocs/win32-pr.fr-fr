---
title: TTN_LINKCLICK le code de notification (commctrl. h)
description: Envoyé lorsqu’un clic est effectué sur un lien de texte à l’intérieur d’une info-bulle. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: d3e76431-5b5f-4d67-8528-db21fd939917
keywords:
- Contrôles Windows de code de notification TTN_LINKCLICK
topic_type:
- apiref
api_name:
- TTN_LINKCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c90be24910c2739b4495b651abf97156342d955b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512816"
---
# <a name="ttn_linkclick-notification-code"></a><span data-ttu-id="f0ab1-105">\_Code de notification ttn LINKCLICK</span><span class="sxs-lookup"><span data-stu-id="f0ab1-105">TTN\_LINKCLICK notification code</span></span>

<span data-ttu-id="f0ab1-106">Envoyé lorsqu’un clic est effectué sur un lien de texte à l’intérieur d’une info-bulle.</span><span class="sxs-lookup"><span data-stu-id="f0ab1-106">Sent when a text link inside a balloon tooltip is clicked.</span></span> <span data-ttu-id="f0ab1-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="f0ab1-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TTN_LINKCLICK
```



## <a name="parameters"></a><span data-ttu-id="f0ab1-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f0ab1-108">Parameters</span></span>

<span data-ttu-id="f0ab1-109">Ce code de notification n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="f0ab1-109">This notification code has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f0ab1-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f0ab1-110">Return value</span></span>

<span data-ttu-id="f0ab1-111">Valeur de retour non utilisée.</span><span class="sxs-lookup"><span data-stu-id="f0ab1-111">Return value not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0ab1-112">Notes</span><span class="sxs-lookup"><span data-stu-id="f0ab1-112">Remarks</span></span>

<span data-ttu-id="f0ab1-113">Voici un exemple de l’envoi de cette notification.</span><span class="sxs-lookup"><span data-stu-id="f0ab1-113">Following is an example of when this notification is sent.</span></span> <span data-ttu-id="f0ab1-114">Supposons que votre info-bulle contient le texte suivant : « Ceci est un <A>lien</A>».</span><span class="sxs-lookup"><span data-stu-id="f0ab1-114">Assume that your balloon tooltip contains the following text, "This is a <A>link</A>".</span></span> <span data-ttu-id="f0ab1-115">Quand l’utilisateur clique sur « Link », le contrôle ToolTip envoie un \_ Code de notification ttn LINKCLICK.</span><span class="sxs-lookup"><span data-stu-id="f0ab1-115">When "link" is clicked, the tooltip control sends a TTN\_LINKCLICK notification code.</span></span>

> [!Note]  
> <span data-ttu-id="f0ab1-116">Pour utiliser ce code de notification, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="f0ab1-116">To use this notification code, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="f0ab1-117">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="f0ab1-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f0ab1-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f0ab1-118">Requirements</span></span>



| <span data-ttu-id="f0ab1-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f0ab1-119">Requirement</span></span> | <span data-ttu-id="f0ab1-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="f0ab1-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f0ab1-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f0ab1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f0ab1-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f0ab1-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f0ab1-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f0ab1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f0ab1-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f0ab1-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f0ab1-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="f0ab1-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0ab1-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0ab1-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





