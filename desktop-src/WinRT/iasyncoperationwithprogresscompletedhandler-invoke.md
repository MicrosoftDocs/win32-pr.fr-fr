---
description: Appelle la méthode qui est appelée lorsque l’opération asynchrone spécifiée signale la progression.
ms.assetid: FB60DDC0-7521-4999-8DD8-175556004198
title: 'IAsyncOperationWithProgressCompletedHandler<TResult, TProgress> :: Invoke, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAsyncOperationWithProgressCompletedHandler<TResult,TProgress>.Invoke
api_type:
- COM
api_location: ''
ms.openlocfilehash: 469686cbd96dedc7f816fdd1f482d3474362688e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113119"
---
# <a name="iasyncoperationwithprogresscompletedhandlertresulttprogressinvoke-method"></a><span data-ttu-id="55011-103">IAsyncOperationWithProgressCompletedHandler<TResult, TProgress> :: Invoke, méthode</span><span class="sxs-lookup"><span data-stu-id="55011-103">IAsyncOperationWithProgressCompletedHandler<TResult,TProgress>::Invoke method</span></span>

<span data-ttu-id="55011-104">Appelle la méthode qui est appelée lorsque l’opération asynchrone spécifiée signale la progression.</span><span class="sxs-lookup"><span data-stu-id="55011-104">Invokes the method that is called when the specified asynchronous operation reports progress.</span></span>

## <a name="syntax"></a><span data-ttu-id="55011-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="55011-105">Syntax</span></span>


```C++
HRESULT Invoke(
  [in] IAsyncOperationWithProgress<TResult,TProgress> *asyncInfo
);
```



## <a name="parameters"></a><span data-ttu-id="55011-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="55011-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55011-107">*asyncInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="55011-107">*asyncInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55011-108">Type : \**[**IAsyncOperationWithProgress<TResult, TProgress>**](/previous-versions//br205807(v=vs.85)) \** _</span><span class="sxs-lookup"><span data-stu-id="55011-108">Type: \**[**IAsyncOperationWithProgress<TResult,TProgress>**](/previous-versions//br205807(v=vs.85))\** _</span></span>

<span data-ttu-id="55011-109">Action asynchrone qui signale la fin de l’opération.</span><span class="sxs-lookup"><span data-stu-id="55011-109">The asynchronous action that reports completion.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55011-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="55011-110">Return value</span></span>

<span data-ttu-id="55011-111">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="55011-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="55011-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="55011-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="55011-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="55011-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="55011-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="55011-114">Requirements</span></span>



| <span data-ttu-id="55011-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="55011-115">Requirement</span></span> | <span data-ttu-id="55011-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="55011-116">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="55011-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="55011-117">Minimum supported client</span></span><br/> | <span data-ttu-id="55011-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="55011-118">Windows 8</span></span><br/>           |
| <span data-ttu-id="55011-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="55011-119">Minimum supported server</span></span><br/> | <span data-ttu-id="55011-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="55011-120">Windows Server 2012</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="55011-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="55011-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="55011-122">[**IAsyncOperationWithProgressCompletedHandler<TResult, TProgress>**](/previous-versions//br205808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="55011-122">[**IAsyncOperationWithProgressCompletedHandler<TResult,TProgress>**](/previous-versions//br205808(v=vs.85))</span></span>
</dt> </dl>

 

 
