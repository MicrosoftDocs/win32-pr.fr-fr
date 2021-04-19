---
title: Méthode IMsTscAxEvents OnUserNameAcquired
description: Appelée lorsque le nom d’utilisateur a été acquis par le contrôle.
ms.assetid: 0653B28B-2D46-429F-8A36-5656786C0B26
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnUserNameAcquired
- Méthode OnUserNameAcquired Services Bureau à distance, interface IMsTscAxEvents
- Services Bureau à distance de l’interface IMsTscAxEvents, méthode OnUserNameAcquired
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnUserNameAcquired
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf5d77f0eb739daa54f8385112b79f67f279eae9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513612"
---
# <a name="imstscaxeventsonusernameacquired-method"></a><span data-ttu-id="df331-106">IMsTscAxEvents :: OnUserNameAcquired, méthode</span><span class="sxs-lookup"><span data-stu-id="df331-106">IMsTscAxEvents::OnUserNameAcquired method</span></span>

<span data-ttu-id="df331-107">Appelée lorsque le nom d’utilisateur a été acquis par le contrôle.</span><span class="sxs-lookup"><span data-stu-id="df331-107">Called when the user name has been acquired by the control.</span></span>

## <a name="syntax"></a><span data-ttu-id="df331-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="df331-108">Syntax</span></span>


```C++
void OnUserNameAcquired(
   BSTR bstrUserName
);
```



## <a name="parameters"></a><span data-ttu-id="df331-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="df331-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df331-110">*bstrUserName*</span><span class="sxs-lookup"><span data-stu-id="df331-110">*bstrUserName*</span></span> 
</dt> <dd>

<span data-ttu-id="df331-111">Nom d'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="df331-111">The user name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df331-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="df331-112">Return value</span></span>

<span data-ttu-id="df331-113">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="df331-113">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="df331-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="df331-114">Requirements</span></span>



| <span data-ttu-id="df331-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="df331-115">Requirement</span></span> | <span data-ttu-id="df331-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="df331-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="df331-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="df331-117">Minimum supported client</span></span><br/> | <span data-ttu-id="df331-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="df331-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="df331-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="df331-119">Minimum supported server</span></span><br/> | <span data-ttu-id="df331-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="df331-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="df331-121">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="df331-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="df331-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df331-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="df331-123">DLL</span><span class="sxs-lookup"><span data-stu-id="df331-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df331-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df331-124"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="df331-125">IID</span><span class="sxs-lookup"><span data-stu-id="df331-125">IID</span></span><br/>                      | <span data-ttu-id="df331-126">IMsTscAxEvents est défini en tant que 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="df331-126">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="df331-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df331-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df331-128">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="df331-128">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





