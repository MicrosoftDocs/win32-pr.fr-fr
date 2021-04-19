---
description: 'La méthode CanSeekForward détermine si le flux peut être recherché par progression. Cette méthode implémente la méthode IMediaPosition :: CanSeekForward.'
ms.assetid: ccb2db8d-b52e-4e3d-b49b-9689197a974a
title: Méthode CPosPassThru. CanSeekForward (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CanSeekForward
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 701bfdff1d3a3a37dc0e3935aa82bfca2e01cfcb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541344"
---
# <a name="cpospassthrucanseekforward-method"></a><span data-ttu-id="d1594-104">Méthode CPosPassThru. CanSeekForward</span><span class="sxs-lookup"><span data-stu-id="d1594-104">CPosPassThru.CanSeekForward method</span></span>

<span data-ttu-id="d1594-105">La `CanSeekForward` méthode détermine si le flux peut être recherché.</span><span class="sxs-lookup"><span data-stu-id="d1594-105">The `CanSeekForward` method determines whether the stream can be seeked forward.</span></span> <span data-ttu-id="d1594-106">Cette méthode implémente la méthode [**IMediaPosition :: CanSeekForward**](/windows/desktop/api/Control/nf-control-imediaposition-canseekforward) .</span><span class="sxs-lookup"><span data-stu-id="d1594-106">This method implements the [**IMediaPosition::CanSeekForward**](/windows/desktop/api/Control/nf-control-imediaposition-canseekforward) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1594-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d1594-107">Syntax</span></span>


```C++
HRESULT CanSeekForward(
   LONG *pCanSeekForward
);
```



## <a name="parameters"></a><span data-ttu-id="d1594-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d1594-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1594-109">*pCanSeekForward*</span><span class="sxs-lookup"><span data-stu-id="d1594-109">*pCanSeekForward*</span></span> 
</dt> <dd>

<span data-ttu-id="d1594-110">Pointeur vers une variable qui reçoit la valeur OATRUE si le filtre peut effectuer une recherche vers l’avant ou OAFALSE dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="d1594-110">Pointer to a variable that receives the value OATRUE if the filter can seek forward, or OAFALSE otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1594-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d1594-111">Return value</span></span>

<span data-ttu-id="d1594-112">Retourne la valeur **HRESULT** de la broche connectée.</span><span class="sxs-lookup"><span data-stu-id="d1594-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1594-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d1594-113">Requirements</span></span>



| <span data-ttu-id="d1594-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d1594-114">Requirement</span></span> | <span data-ttu-id="d1594-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1594-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1594-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="d1594-116">Header</span></span><br/>  | <dl> <span data-ttu-id="d1594-117"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d1594-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d1594-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d1594-118">Library</span></span><br/> | <dl> <span data-ttu-id="d1594-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d1594-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1594-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1594-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1594-121">**CPosPassThru, classe**</span><span class="sxs-lookup"><span data-stu-id="d1594-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




