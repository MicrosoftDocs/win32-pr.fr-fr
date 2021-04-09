---
description: Demande que l’opération d’interruption de l’application soit retardée.
ms.assetid: 5AB84652-165D-4173-A047-541B05848871
title: 'ISuspendingOperation :: GetDeferral, méthode (Windows. ApplicationModel. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingOperation.GetDeferral
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: 6874eb31e73fa1c20399f68850fc69204d0e0f6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862610"
---
# <a name="isuspendingoperationgetdeferral-method"></a><span data-ttu-id="a3bf5-103">ISuspendingOperation :: GetDeferral, méthode</span><span class="sxs-lookup"><span data-stu-id="a3bf5-103">ISuspendingOperation::GetDeferral method</span></span>

<span data-ttu-id="a3bf5-104">Demande que l’opération d’interruption de l’application soit retardée.</span><span class="sxs-lookup"><span data-stu-id="a3bf5-104">Requests that the app suspending operation be delayed.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3bf5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a3bf5-105">Syntax</span></span>


```C++
HRESULT GetDeferral(
  [out, retval] ISuspendingDeferral **deferral
);
```



## <a name="parameters"></a><span data-ttu-id="a3bf5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a3bf5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3bf5-107">*Report* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="a3bf5-107">*deferral* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="a3bf5-108">Suspension du report.</span><span class="sxs-lookup"><span data-stu-id="a3bf5-108">The deferral suspension.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3bf5-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a3bf5-109">Return value</span></span>

<span data-ttu-id="a3bf5-110">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a3bf5-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a3bf5-111">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a3bf5-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3bf5-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a3bf5-112">Requirements</span></span>



| <span data-ttu-id="a3bf5-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a3bf5-113">Requirement</span></span> | <span data-ttu-id="a3bf5-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="a3bf5-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3bf5-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a3bf5-115">Minimum supported client</span></span><br/> | <span data-ttu-id="a3bf5-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="a3bf5-116">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="a3bf5-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a3bf5-117">Minimum supported server</span></span><br/> | <span data-ttu-id="a3bf5-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a3bf5-118">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="a3bf5-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="a3bf5-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3bf5-120"><dt>Windows. ApplicationModel. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3bf5-120"><dt>Windows.ApplicationModel.h</dt></span></span> </dl>   |
| <span data-ttu-id="a3bf5-121">MIDL</span><span class="sxs-lookup"><span data-stu-id="a3bf5-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a3bf5-122"><dt>Windows. ApplicationModel. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a3bf5-122"><dt>Windows.ApplicationModel.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3bf5-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a3bf5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3bf5-124">**ISuspendingOperation**</span><span class="sxs-lookup"><span data-stu-id="a3bf5-124">**ISuspendingOperation**</span></span>](isuspendingoperation.md)
</dt> </dl>

 

 




