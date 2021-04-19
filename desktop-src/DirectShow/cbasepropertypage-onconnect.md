---
description: La méthode OnConnect fournit un pointeur IUnknown vers l’objet associé à la page de propriétés.
ms.assetid: 74cae8e1-5347-4e3d-ba5f-6a4efec2ddae
title: CBasePropertyPage. OnConnect, méthode (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 38f83a7c491f1591cece8d5d85eb4525a1059d2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523451"
---
# <a name="cbasepropertypageonconnect-method"></a><span data-ttu-id="791da-103">CBasePropertyPage. OnConnect, méthode</span><span class="sxs-lookup"><span data-stu-id="791da-103">CBasePropertyPage.OnConnect method</span></span>

<span data-ttu-id="791da-104">La `OnConnect` méthode fournit un pointeur **IUnknown** vers l’objet associé à la page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="791da-104">The `OnConnect` method provides an **IUnknown** pointer to the object associated with the property page.</span></span>

## <a name="syntax"></a><span data-ttu-id="791da-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="791da-105">Syntax</span></span>


```C++
virtual HRESULT OnConnect(
   IUnknown *pUnknown
);
```



## <a name="parameters"></a><span data-ttu-id="791da-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="791da-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="791da-107">*pUnknown*</span><span class="sxs-lookup"><span data-stu-id="791da-107">*pUnknown*</span></span> 
</dt> <dd>

<span data-ttu-id="791da-108">Pointeur vers l’interface **IUnknown** de l’objet.</span><span class="sxs-lookup"><span data-stu-id="791da-108">Pointer to the **IUnknown** interface of the object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="791da-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="791da-109">Return value</span></span>

<span data-ttu-id="791da-110">L’implémentation de la classe de base retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="791da-110">The base-class implementation returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="791da-111">Notes</span><span class="sxs-lookup"><span data-stu-id="791da-111">Remarks</span></span>

<span data-ttu-id="791da-112">La méthode [**CBasePropertyPage :: SetObjects**](cbasepropertypage-setobjects.md) appelle la `OnConnect` méthode.</span><span class="sxs-lookup"><span data-stu-id="791da-112">The [**CBasePropertyPage::SetObjects**](cbasepropertypage-setobjects.md) method calls the `OnConnect` method.</span></span> <span data-ttu-id="791da-113">Substituez cette méthode pour stocker un pointeur vers l’objet spécifié par *pUnknown*.</span><span class="sxs-lookup"><span data-stu-id="791da-113">Override this method to store a pointer to the object specified by *pUnknown*.</span></span> <span data-ttu-id="791da-114">Vous pouvez soit stocker le pointeur *pUnknown* lui-même, soit demander ce pointeur pour d’autres interfaces.</span><span class="sxs-lookup"><span data-stu-id="791da-114">You can either store the *pUnknown* pointer itself, or query that pointer for other interfaces.</span></span> <span data-ttu-id="791da-115">Si vous stockez le pointeur *pUnknown* , appelez **AddRef** avant `OnConnect` returns.</span><span class="sxs-lookup"><span data-stu-id="791da-115">If you store the *pUnknown* pointer, call **AddRef** before `OnConnect` returns.</span></span>

<span data-ttu-id="791da-116">Dans la méthode [**CBasePropertyPage :: OnActivate**](cbasepropertypage-onactivate.md) , utilisez le pointeur stocké (ou les pointeurs) pour récupérer les valeurs initiales des propriétés de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="791da-116">In the [**CBasePropertyPage::OnActivate**](cbasepropertypage-onactivate.md) method, use the stored pointer (or pointers) to retrieve initial values for the dialog properties.</span></span> <span data-ttu-id="791da-117">Dans la méthode [**CBasePropertyPage :: OnApplyChanges**](cbasepropertypage-onapplychanges.md) , appliquez toutes les modifications à l’objet.</span><span class="sxs-lookup"><span data-stu-id="791da-117">In the [**CBasePropertyPage::OnApplyChanges**](cbasepropertypage-onapplychanges.md) method, apply any changes back to the object.</span></span> <span data-ttu-id="791da-118">Libérez tous les pointeurs dans la méthode [**CBasePropertyPage :: OnDisconnect**](cbasepropertypage-ondisconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="791da-118">Release all pointers in the [**CBasePropertyPage::OnDisconnect**](cbasepropertypage-ondisconnect.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="791da-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="791da-119">Examples</span></span>


```C++
HRESULT CMyProp::OnConnect(IUnknown *pUnk)
{
    ASSERT(m_pOwningFilter == NULL);
    HRESULT hr;
    // Query pUnk for the filter's custom interface.
    hr = pUnk->QueryInterface(IID_ISomeCustomInterface,
             reinterpret_cast<void**>(&m_pOwningFilter));
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="791da-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="791da-120">Requirements</span></span>



| <span data-ttu-id="791da-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="791da-121">Requirement</span></span> | <span data-ttu-id="791da-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="791da-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="791da-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="791da-123">Header</span></span><br/>  | <dl> <span data-ttu-id="791da-124"><dt>Cprop. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="791da-124"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="791da-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="791da-125">Library</span></span><br/> | <dl> <span data-ttu-id="791da-126"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="791da-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="791da-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="791da-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="791da-128">**CBasePropertyPage, classe**</span><span class="sxs-lookup"><span data-stu-id="791da-128">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




