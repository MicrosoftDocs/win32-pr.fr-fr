---
description: La méthode GetHRESULT, récupère la valeur HRESULT de la commande appelée.
ms.assetid: 7e88a2bd-6b1b-4e59-b185-5dfd501fc37a
title: Méthode CDeferredCommand. GetHRESULT, (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.GetHResult
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5b09049bc443991dabe07a7626ffc42097feceee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538160"
---
# <a name="cdeferredcommandgethresult-method"></a><span data-ttu-id="f955f-103">Méthode CDeferredCommand. GetHRESULT,</span><span class="sxs-lookup"><span data-stu-id="f955f-103">CDeferredCommand.GetHResult method</span></span>

<span data-ttu-id="f955f-104">La `GetHResult` méthode récupère la valeur **HRESULT** à partir de la commande appelée.</span><span class="sxs-lookup"><span data-stu-id="f955f-104">The `GetHResult` method retrieves the **HRESULT** value from the invoked command.</span></span>

## <a name="syntax"></a><span data-ttu-id="f955f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f955f-105">Syntax</span></span>


```C++
HRESULT GetHResult(
   HRESULT *phrResult
);
```



## <a name="parameters"></a><span data-ttu-id="f955f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f955f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f955f-107">*phrResult*</span><span class="sxs-lookup"><span data-stu-id="f955f-107">*phrResult*</span></span> 
</dt> <dd>

<span data-ttu-id="f955f-108">Pointeur vers la valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f955f-108">Pointer to the **HRESULT** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f955f-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f955f-109">Return value</span></span>

<span data-ttu-id="f955f-110">Retourne E \_ Abort si **m \_ PQueue** a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="f955f-110">Returns E\_ABORT if **m\_pQueue** is **NULL**.</span></span> <span data-ttu-id="f955f-111">Sinon, retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f955f-111">Otherwise, returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="f955f-112">Notes</span><span class="sxs-lookup"><span data-stu-id="f955f-112">Remarks</span></span>

<span data-ttu-id="f955f-113">Cette fonction membre implémente la méthode [**IDeferredCommand :: GetHRESULT,**](/windows/desktop/api/Control/nf-control-ideferredcommand-gethresult) .</span><span class="sxs-lookup"><span data-stu-id="f955f-113">This member function implements the [**IDeferredCommand::GetHResult**](/windows/desktop/api/Control/nf-control-ideferredcommand-gethresult) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f955f-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f955f-114">Requirements</span></span>



| <span data-ttu-id="f955f-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f955f-115">Requirement</span></span> | <span data-ttu-id="f955f-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="f955f-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f955f-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="f955f-117">Header</span></span><br/>  | <dl> <span data-ttu-id="f955f-118"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f955f-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f955f-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f955f-119">Library</span></span><br/> | <dl> <span data-ttu-id="f955f-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f955f-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f955f-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f955f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f955f-122">**CDeferredCommand, classe**</span><span class="sxs-lookup"><span data-stu-id="f955f-122">**CDeferredCommand Class**</span></span>](cdeferredcommand.md)
</dt> </dl>

 

 




