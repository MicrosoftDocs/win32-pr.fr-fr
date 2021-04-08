---
description: La méthode KsQueryMediums récupère les supports pris en charge par un code confidentiel.
ms.assetid: 554bf968-6054-4f9d-95db-facf0444641f
title: 'IKsPin :: KsQueryMediums, méthode (ksproxy. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPin.KsQueryMediums
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: f037317b49bc54f5ea9db5b7a4ae039ec0a9970d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746573"
---
# <a name="ikspinksquerymediums-method"></a><span data-ttu-id="63ff7-103">IKsPin :: KsQueryMediums, méthode</span><span class="sxs-lookup"><span data-stu-id="63ff7-103">IKsPin::KsQueryMediums method</span></span>

<span data-ttu-id="63ff7-104">La `KsQueryMediums` méthode récupère les supports pris en charge par un code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="63ff7-104">The `KsQueryMediums` method retrieves the mediums supported by a pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="63ff7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="63ff7-105">Syntax</span></span>


```C++
HRESULT KsQueryMediums(
  [out] KSMULTIPLE_ITEM **ppmi
);
```



## <a name="parameters"></a><span data-ttu-id="63ff7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="63ff7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63ff7-107">*PPMI* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="63ff7-107">*ppmi* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="63ff7-108">Adresse d’un pointeur vers une structure d' [**\_ élément KSMULTIPLE**](ksmultiple-item.md) .</span><span class="sxs-lookup"><span data-stu-id="63ff7-108">Address of a pointer to a [**KSMULTIPLE\_ITEM**](ksmultiple-item.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63ff7-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="63ff7-109">Return value</span></span>

<span data-ttu-id="63ff7-110">Si la méthode est réussie, elle retourne la valeur \_ OK.</span><span class="sxs-lookup"><span data-stu-id="63ff7-110">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="63ff7-111">En cas d’échec, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="63ff7-111">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="63ff7-112">Notes</span><span class="sxs-lookup"><span data-stu-id="63ff7-112">Remarks</span></span>

<span data-ttu-id="63ff7-113">Cette méthode retourne une structure d' [**\_ élément KSMULTIPLE**](ksmultiple-item.md) allouée par la tâche, qui est suivie par zéro ou plusieurs structures [**REGPINMEDIUM**](/windows/desktop/api/strmif/ns-strmif-regpinmedium) .</span><span class="sxs-lookup"><span data-stu-id="63ff7-113">This method returns a task-allocated [**KSMULTIPLE\_ITEM**](ksmultiple-item.md) structure, which is followed by zero or more [**REGPINMEDIUM**](/windows/desktop/api/strmif/ns-strmif-regpinmedium) structures.</span></span> <span data-ttu-id="63ff7-114">Le membre **Count** de la structure de l' **\_ élément KSMULTIPLE** spécifie le nombre de structures **REGPINMEDIUM** .</span><span class="sxs-lookup"><span data-stu-id="63ff7-114">The **Count** member of the **KSMULTIPLE\_ITEM** structure specifies the number of **REGPINMEDIUM** structures.</span></span> <span data-ttu-id="63ff7-115">Chaque structure **REGPINMEDIUM** définit un support pris en charge par le code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="63ff7-115">Each **REGPINMEDIUM** structure defines a medium supported by the pin.</span></span>

<span data-ttu-id="63ff7-116">L’appelant doit libérer les structures retournées, à l’aide de la fonction **CoTaskMemFree** .</span><span class="sxs-lookup"><span data-stu-id="63ff7-116">The caller must free the returned structures, using the **CoTaskMemFree** function.</span></span>

<span data-ttu-id="63ff7-117">Vous devez inclure KS. h avant ksproxy. h.</span><span class="sxs-lookup"><span data-stu-id="63ff7-117">You must include Ks.h before Ksproxy.h.</span></span>

## <a name="examples"></a><span data-ttu-id="63ff7-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="63ff7-118">Examples</span></span>

<span data-ttu-id="63ff7-119">La fonction d’assistance suivante tente de faire correspondre un code confidentiel par rapport à un support spécifié.</span><span class="sxs-lookup"><span data-stu-id="63ff7-119">The following helper function attempts to match a pin against a specified medium.</span></span>


```C++
HRESULT FindMatchingMedium(
    IPin *pPin, 
    REGPINMEDIUM *pMedium, 
    bool *pfMatch)
{
    IKsPin* pKsPin = NULL;
    KSMULTIPLE_ITEM *pmi;

    *pfMatch = false;
    HRESULT hr = pPin->QueryInterface(IID_IKsPin, (void **)&pKsPin);
    if (FAILED(hr)) 
        return hr;  // Pin does not support IKsPin.

    hr = pKsPin->KsQueryMediums(&pmi);
    pKsPin->Release();
    if (FAILED(hr))
        return hr;  // Pin does not support mediums.

    if (pmi->Count) 
    {
        // Use pointer arithmetic to reference the first medium structure.
        REGPINMEDIUM *pTemp = (REGPINMEDIUM*)(pmi + 1);
        for (ULONG i = 0; i < pmi->Count; i++, pTemp++) 
        {
            if (pMedium->clsMedium == pTemp->clsMedium) 
            {
                *pfMatch = true;
                break;
            }
        }
    }        
    CoTaskMemFree(pmi);
    return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="63ff7-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="63ff7-120">Requirements</span></span>



| <span data-ttu-id="63ff7-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="63ff7-121">Requirement</span></span> | <span data-ttu-id="63ff7-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="63ff7-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="63ff7-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63ff7-123">Minimum supported client</span></span><br/> | <span data-ttu-id="63ff7-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="63ff7-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="63ff7-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63ff7-125">Minimum supported server</span></span><br/> | <span data-ttu-id="63ff7-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="63ff7-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="63ff7-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="63ff7-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="63ff7-128"><dt>Ksproxy. h</dt></span><span class="sxs-lookup"><span data-stu-id="63ff7-128"><dt>Ksproxy.h</dt></span></span> </dl>    |
| <span data-ttu-id="63ff7-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="63ff7-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="63ff7-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="63ff7-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63ff7-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63ff7-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63ff7-132">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="63ff7-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="63ff7-133">**Interface IKsPin**</span><span class="sxs-lookup"><span data-stu-id="63ff7-133">**IKsPin Interface**</span></span>](ikspin.md)
</dt> <dt>

[<span data-ttu-id="63ff7-134">Filtres de pilote de classe WDM</span><span class="sxs-lookup"><span data-stu-id="63ff7-134">WDM Class Driver Filters</span></span>](wdm-class-driver-filters.md)
</dt> </dl>

 

 




