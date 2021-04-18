---
description: 'La méthode CheckCapabilities interroge si le flux a spécifié des fonctionnalités de recherche. Cette méthode implémente la méthode IMediaSeeking :: CheckCapabilities.'
ms.assetid: 5d37e179-9e04-44e1-acbc-dfd2682830c0
title: Méthode CSourceSeeking. CheckCapabilities (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.CheckCapabilities
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2f537973ac6c8f084ea42ba915a6293e581debef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532784"
---
# <a name="csourceseekingcheckcapabilities-method"></a><span data-ttu-id="49148-104">Méthode CSourceSeeking. CheckCapabilities</span><span class="sxs-lookup"><span data-stu-id="49148-104">CSourceSeeking.CheckCapabilities method</span></span>

<span data-ttu-id="49148-105">La `CheckCapabilities` méthode interroge si le flux a spécifié des fonctionnalités de recherche.</span><span class="sxs-lookup"><span data-stu-id="49148-105">The `CheckCapabilities` method queries whether the stream has specified seeking capabilities.</span></span> <span data-ttu-id="49148-106">Cette méthode implémente la méthode [**IMediaSeeking :: CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) .</span><span class="sxs-lookup"><span data-stu-id="49148-106">This method implements the [**IMediaSeeking::CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="49148-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="49148-107">Syntax</span></span>


```C++
HRESULT CheckCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a><span data-ttu-id="49148-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="49148-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49148-109">*pCapabilities*</span><span class="sxs-lookup"><span data-stu-id="49148-109">*pCapabilities*</span></span> 
</dt> <dd>

<span data-ttu-id="49148-110">Pointeur vers une combinaison d’opérations de bits d’un ou de plusieurs attributs de [**\_ \_ \_ capacités de recherche**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) de recherche.</span><span class="sxs-lookup"><span data-stu-id="49148-110">Pointer to a bitwise combination of one or more [**AM\_SEEKING\_SEEKING\_CAPABILITIES**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) attributes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49148-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="49148-111">Return value</span></span>

<span data-ttu-id="49148-112">Retourne l’une des valeurs **HRESULT** listées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="49148-112">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="49148-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="49148-113">Return code</span></span>                                                                               | <span data-ttu-id="49148-114">Description</span><span class="sxs-lookup"><span data-stu-id="49148-114">Description</span></span>                                                            |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="49148-115"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="49148-115"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="49148-116">Toutes les fonctionnalités de *pCapabilities* ne sont pas présentes.</span><span class="sxs-lookup"><span data-stu-id="49148-116">Not all of the capabilities in *pCapabilities* are present.</span></span><br/> |
| <dl> <span data-ttu-id="49148-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="49148-117"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="49148-118">Toutes les fonctionnalités de *pCapabilities* sont présentes.</span><span class="sxs-lookup"><span data-stu-id="49148-118">All capabilities in *pCapabilities* are present.</span></span><br/>            |
| <dl> <span data-ttu-id="49148-119"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="49148-119"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="49148-120">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="49148-120">**NULL** pointer argument.</span></span><br/>                                  |



 

## <a name="remarks"></a><span data-ttu-id="49148-121">Notes</span><span class="sxs-lookup"><span data-stu-id="49148-121">Remarks</span></span>

<span data-ttu-id="49148-122">Comme elle est implémentée, cette méthode vérifie la valeur de *\* pCapabilities* par rapport à la variable membre [**CSourceSeeking :: m \_ dwSeekingCaps**](csourceseeking-m-dwseekingcaps.md) .</span><span class="sxs-lookup"><span data-stu-id="49148-122">As implemented, this method checks the value of *\*pCapabilities* against the [**CSourceSeeking::m\_dwSeekingCaps**](csourceseeking-m-dwseekingcaps.md) member variable.</span></span> <span data-ttu-id="49148-123">Toutefois, il ne définit pas *\* pCapabilities* égal à **m \_ dwSeekingCaps**, comme décrit pour la méthode [**IMediaSeeking :: CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) .</span><span class="sxs-lookup"><span data-stu-id="49148-123">However, it does not set *\*pCapabilities* equal to **m\_dwSeekingCaps**, as described for the [**IMediaSeeking::CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) method.</span></span> <span data-ttu-id="49148-124">En outre, dans le cas où aucune des fonctionnalités spécifiées n’est disponible, la méthode ne retourne pas E \_ Fail.</span><span class="sxs-lookup"><span data-stu-id="49148-124">Also, in the case where none of the specified capabilities are available, the method does not return E\_FAIL.</span></span> <span data-ttu-id="49148-125">Une implémentation plus complète serait la suivante :</span><span class="sxs-lookup"><span data-stu-id="49148-125">A more complete implementation would be as follows:</span></span>


```C++
STDMETHODIMP CheckCapabilities(DWORD *pCapabilities)
{
    CheckPointer(pCapabilities, E_POINTER)
;
    DWORD dwCaps;
    HRESULT hr = GetCapabilities(&dwCaps);
    if (SUCCEEDED(hr))
    {
        dwCaps &= *pCapabilities;
        if (dwCaps)
        {
            hr =  (dwCaps == *pCapabilities ? S_OK : S_FALSE );
        }
        else 
        {
            hr = E_FAIL;
        }
        *pCapabilities = dwCaps;
    }
    else 
    {
        *pCapabilities = 0;
    }
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="49148-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="49148-126">Requirements</span></span>



| <span data-ttu-id="49148-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="49148-127">Requirement</span></span> | <span data-ttu-id="49148-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="49148-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49148-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="49148-129">Header</span></span><br/>  | <dl> <span data-ttu-id="49148-130"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="49148-130"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="49148-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="49148-131">Library</span></span><br/> | <dl> <span data-ttu-id="49148-132"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="49148-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49148-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="49148-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49148-134">**CSourceSeeking, classe**</span><span class="sxs-lookup"><span data-stu-id="49148-134">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




