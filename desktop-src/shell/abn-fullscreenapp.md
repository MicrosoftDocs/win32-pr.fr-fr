---
description: Avertit un appbar lorsqu’une application en plein écran est en mode d’ouverture ou de fermeture. Cette notification est envoyée sous la forme d’un message défini par l’application qui est défini par le \_ nouveau message ABM.
title: Message ABN_FULLSCREENAPP (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: c67ec934-088c-43e0-bff4-900d76a456e5
api_name:
- ABN_FULLSCREENAPP
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d73a30c9f40fc494603afd4a6cbb990f81290c8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112359"
---
# <a name="abn_fullscreenapp-message"></a><span data-ttu-id="cb258-104">Message d’ABN \_ FULLSCREENAPP</span><span class="sxs-lookup"><span data-stu-id="cb258-104">ABN\_FULLSCREENAPP message</span></span>

<span data-ttu-id="cb258-105">Avertit un appbar lorsqu’une application en plein écran est en mode d’ouverture ou de fermeture.</span><span class="sxs-lookup"><span data-stu-id="cb258-105">Notifies an appbar when a full-screen application is opening or closing.</span></span> <span data-ttu-id="cb258-106">Cette notification est envoyée sous la forme d’un message défini par l’application qui est défini par [**le \_ nouveau message ABM**](abm-new.md) .</span><span class="sxs-lookup"><span data-stu-id="cb258-106">This notification is sent in the form of an application-defined message that is set by the [**ABM\_NEW**](abm-new.md) message.</span></span>


```C++

ABN_FULLSCREENAPP 

    fOpen = (BOOL) lParam; 

            
```



## <a name="parameters"></a><span data-ttu-id="cb258-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cb258-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb258-108">*fOpen*</span><span class="sxs-lookup"><span data-stu-id="cb258-108">*fOpen*</span></span> 
</dt> <dd>

<span data-ttu-id="cb258-109">Indicateur spécifiant si une application en plein écran est en mode d’ouverture ou de fermeture.</span><span class="sxs-lookup"><span data-stu-id="cb258-109">A flag specifying whether a full-screen application is opening or closing.</span></span> <span data-ttu-id="cb258-110">Ce paramètre a la **valeur true** si l’application s’ouvre ou **false** si elle est en fermeture.</span><span class="sxs-lookup"><span data-stu-id="cb258-110">This parameter is **TRUE** if the application is opening or **FALSE** if it is closing.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb258-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cb258-111">Return value</span></span>

<span data-ttu-id="cb258-112">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="cb258-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb258-113">Notes</span><span class="sxs-lookup"><span data-stu-id="cb258-113">Remarks</span></span>

<span data-ttu-id="cb258-114">Lors de l’ouverture d’une application en plein écran, un appbar doit se placer au bas de l’ordre de plan.</span><span class="sxs-lookup"><span data-stu-id="cb258-114">When a full-screen application is opening, an appbar must drop to the bottom of the z-order.</span></span> <span data-ttu-id="cb258-115">Lorsqu’il se ferme, appbar doit restaurer sa position dans l’ordre de plan.</span><span class="sxs-lookup"><span data-stu-id="cb258-115">When it is closing, the appbar should restore its z-order position.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb258-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="cb258-116">Requirements</span></span>



| <span data-ttu-id="cb258-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cb258-117">Requirement</span></span> | <span data-ttu-id="cb258-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb258-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cb258-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb258-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cb258-120">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cb258-120">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="cb258-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb258-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cb258-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cb258-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cb258-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="cb258-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb258-124"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb258-124"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




