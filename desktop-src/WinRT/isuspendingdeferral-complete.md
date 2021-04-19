---
description: Indique au système que l’application a enregistré ses données et qu’elle est prête à être suspendue.
ms.assetid: 5C79AFBA-34E6-4C0B-95A0-731E10D8A17A
title: 'ISuspendingDeferral :: Complete, méthode (Windows. ApplicationModel. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingDeferral.Complete
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: 62febd5fac6aab4a0c5ddd7e6a70fa0e3c3f78ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516250"
---
# <a name="isuspendingdeferralcomplete-method"></a><span data-ttu-id="c7ac7-103">ISuspendingDeferral :: Complete, méthode</span><span class="sxs-lookup"><span data-stu-id="c7ac7-103">ISuspendingDeferral::Complete method</span></span>

<span data-ttu-id="c7ac7-104">Indique au système que l’application a enregistré ses données et qu’elle est prête à être suspendue.</span><span class="sxs-lookup"><span data-stu-id="c7ac7-104">Notifies the system that the app has saved its data and is ready to be suspended.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7ac7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c7ac7-105">Syntax</span></span>


```C++
HRESULT Complete();
```



## <a name="parameters"></a><span data-ttu-id="c7ac7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c7ac7-106">Parameters</span></span>

<span data-ttu-id="c7ac7-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="c7ac7-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c7ac7-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c7ac7-108">Return value</span></span>

<span data-ttu-id="c7ac7-109">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c7ac7-109">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c7ac7-110">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c7ac7-110">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7ac7-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c7ac7-111">Requirements</span></span>



| <span data-ttu-id="c7ac7-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c7ac7-112">Requirement</span></span> | <span data-ttu-id="c7ac7-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="c7ac7-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7ac7-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7ac7-114">Minimum supported client</span></span><br/> | <span data-ttu-id="c7ac7-115">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c7ac7-115">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="c7ac7-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7ac7-116">Minimum supported server</span></span><br/> | <span data-ttu-id="c7ac7-117">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c7ac7-117">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="c7ac7-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="c7ac7-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7ac7-119"><dt>Windows. ApplicationModel. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7ac7-119"><dt>Windows.ApplicationModel.h</dt></span></span> </dl>   |
| <span data-ttu-id="c7ac7-120">MIDL</span><span class="sxs-lookup"><span data-stu-id="c7ac7-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c7ac7-121"><dt>Windows. ApplicationModel. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c7ac7-121"><dt>Windows.ApplicationModel.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7ac7-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7ac7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7ac7-123">**ISuspendingDeferral**</span><span class="sxs-lookup"><span data-stu-id="c7ac7-123">**ISuspendingDeferral**</span></span>](isuspendingdeferral.md)
</dt> </dl>

 

 




