---
description: 'CFactoryTemplate :: m_lpfnNew pointeur membre vers une fonction qui crée une instance de l’objet.'
ms.assetid: 86859bf9-e16a-4494-bf1b-1d8ddbc1c805
title: 'CFactoryTemplate :: m_lpfnNew, membre (ComBase. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lpfnNew
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ee4ec8e1503d3b260e025d154624b2d7c09bb49b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095647"
---
# <a name="cfactorytemplatem_lpfnnew-member"></a><span data-ttu-id="63ec6-103">CFactoryTemplate :: m \_ lpfnNew, membre</span><span class="sxs-lookup"><span data-stu-id="63ec6-103">CFactoryTemplate::m\_lpfnNew member</span></span>

<span data-ttu-id="63ec6-104">Pointeur vers une fonction qui crée une instance de l’objet.</span><span class="sxs-lookup"><span data-stu-id="63ec6-104">Pointer to a function that creates an instance of the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="63ec6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="63ec6-105">Syntax</span></span>


```C++
LPFNNewCOMObject m_lpfnNew;
```



## <a name="remarks"></a><span data-ttu-id="63ec6-106">Notes </span><span class="sxs-lookup"><span data-stu-id="63ec6-106">Remarks</span></span>

<span data-ttu-id="63ec6-107">Dans votre DLL, déclarez une fonction statique qui retourne un pointeur vers une nouvelle instance de l’objet.</span><span class="sxs-lookup"><span data-stu-id="63ec6-107">In your DLL, declare a static function that returns a pointer to a new instance of the object.</span></span> <span data-ttu-id="63ec6-108">Dans le modèle Factory, définissez la variable de membre **m \_ lpfnNew** sur l’adresse de cette fonction statique.</span><span class="sxs-lookup"><span data-stu-id="63ec6-108">In the factory template, set the **m\_lpfnNew** member variable to the address of this static function.</span></span>

<span data-ttu-id="63ec6-109">Le type de pointeur de fonction est [**LPFNNewCOMObject**](lpfnnewcomobject.md).</span><span class="sxs-lookup"><span data-stu-id="63ec6-109">The function pointer type is [**LPFNNewCOMObject**](lpfnnewcomobject.md).</span></span>

<span data-ttu-id="63ec6-110">L’exemple suivant montre une fonction classique pour **m \_ lpfnNew**:</span><span class="sxs-lookup"><span data-stu-id="63ec6-110">The following example shows a typical function for **m\_lpfnNew**:</span></span>


```C++
CUnknown * WINAPI CMyComponent::CreateInstance(LPUNKNOWN pUnk, HRESULT *pHr) 
{
    CMyComponent *pNewObject = 
        new CMyComponent(NAME("My Component"), pUnk, pHr );

    if (pNewObject == NULL)  
    {
        *phr = E_OUTOFMEMORY;
    }
    return pNewObject;
}
```



## <a name="requirements"></a><span data-ttu-id="63ec6-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="63ec6-111">Requirements</span></span>



| <span data-ttu-id="63ec6-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="63ec6-112">Requirement</span></span> | <span data-ttu-id="63ec6-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="63ec6-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63ec6-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="63ec6-114">Header</span></span><br/>  | <dl> <span data-ttu-id="63ec6-115"><dt>ComBase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="63ec6-115"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="63ec6-116">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="63ec6-116">Library</span></span><br/> | <dl> <span data-ttu-id="63ec6-117"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="63ec6-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63ec6-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63ec6-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63ec6-119">**CFactoryTemplate, classe**</span><span class="sxs-lookup"><span data-stu-id="63ec6-119">**CFactoryTemplate Class**</span></span>](cfactorytemplate.md)
</dt> </dl>

 

 




