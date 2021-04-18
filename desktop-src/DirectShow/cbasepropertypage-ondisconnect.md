---
description: La méthode OnDisconnect est appelée lorsque la page de propriétés doit libérer l’objet associé.
ms.assetid: 55bab0ca-587e-405c-9025-f391cf08a620
title: CBasePropertyPage. OnDisconnect, méthode (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnDisconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: abd251d20ca82ad0374a613d9ee73f0eaee21d31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540344"
---
# <a name="cbasepropertypageondisconnect-method"></a><span data-ttu-id="1470a-103">CBasePropertyPage. OnDisconnect, méthode</span><span class="sxs-lookup"><span data-stu-id="1470a-103">CBasePropertyPage.OnDisconnect method</span></span>

<span data-ttu-id="1470a-104">La `OnDisconnect` méthode est appelée lorsque la page de propriétés doit libérer l’objet associé.</span><span class="sxs-lookup"><span data-stu-id="1470a-104">The `OnDisconnect` method is called when the property page should release the associated object.</span></span>

## <a name="syntax"></a><span data-ttu-id="1470a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1470a-105">Syntax</span></span>


```C++
virtual HRESULT OnDisconnect();
```



## <a name="parameters"></a><span data-ttu-id="1470a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1470a-106">Parameters</span></span>

<span data-ttu-id="1470a-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="1470a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1470a-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1470a-108">Return value</span></span>

<span data-ttu-id="1470a-109">L’implémentation de la classe de base retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1470a-109">The base-class implementation returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="1470a-110">Notes</span><span class="sxs-lookup"><span data-stu-id="1470a-110">Remarks</span></span>

<span data-ttu-id="1470a-111">La méthode [**CBasePropertyPage :: SetObjects**](cbasepropertypage-setobjects.md) appelle la `OnDisconnect` méthode.</span><span class="sxs-lookup"><span data-stu-id="1470a-111">The [**CBasePropertyPage::SetObjects**](cbasepropertypage-setobjects.md) method calls the `OnDisconnect` method.</span></span> <span data-ttu-id="1470a-112">Substituez `OnDisconnect` pour libérer tous les pointeurs obtenus dans la méthode [**CBasePropertyPage :: OnConnect**](cbasepropertypage-onconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="1470a-112">Override `OnDisconnect` to release any pointers that were obtained in the [**CBasePropertyPage::OnConnect**](cbasepropertypage-onconnect.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="1470a-113">Exemples</span><span class="sxs-lookup"><span data-stu-id="1470a-113">Examples</span></span>


```C++
HRESULT CMyProp::OnDisconnect(void)
{
    if (m_pOwningFilter)
    {
        m_pOwningFilter->Release();
        m_pOwningFilter = NULL;
    }
    return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="1470a-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1470a-114">Requirements</span></span>



| <span data-ttu-id="1470a-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1470a-115">Requirement</span></span> | <span data-ttu-id="1470a-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="1470a-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1470a-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="1470a-117">Header</span></span><br/>  | <dl> <span data-ttu-id="1470a-118"><dt>Cprop. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1470a-118"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="1470a-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1470a-119">Library</span></span><br/> | <dl> <span data-ttu-id="1470a-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1470a-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1470a-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1470a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1470a-122">**CBasePropertyPage, classe**</span><span class="sxs-lookup"><span data-stu-id="1470a-122">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




