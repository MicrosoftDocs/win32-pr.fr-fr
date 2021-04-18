---
description: 'La méthode IsPageDirty indique si la page de propriétés a été modifiée depuis son activation ou depuis l’appel le plus récent à IPropertyPage :: apply. Cette méthode implémente la méthode IPropertyPage :: IsPageDirty.'
ms.assetid: 95eeec26-7dbb-4add-a827-6505b40afe48
title: Méthode CBasePropertyPage. IsPageDirty (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.IsPageDirty
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c69c2e7d480f63542e146c73e56b9e692693f665
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540580"
---
# <a name="cbasepropertypageispagedirty-method"></a><span data-ttu-id="136a3-104">Méthode CBasePropertyPage. IsPageDirty</span><span class="sxs-lookup"><span data-stu-id="136a3-104">CBasePropertyPage.IsPageDirty method</span></span>

<span data-ttu-id="136a3-105">La `IsPageDirty` méthode indique si la page de propriétés a été modifiée depuis son activation ou depuis l’appel le plus récent à **IPropertyPage :: apply**.</span><span class="sxs-lookup"><span data-stu-id="136a3-105">The `IsPageDirty` method indicates whether the property page has changed since it was activated or since the most recent call to **IPropertyPage::Apply**.</span></span> <span data-ttu-id="136a3-106">Cette méthode implémente la méthode **IPropertyPage :: IsPageDirty** .</span><span class="sxs-lookup"><span data-stu-id="136a3-106">This method implements the **IPropertyPage::IsPageDirty** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="136a3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="136a3-107">Syntax</span></span>


```C++
HRESULT IsPageDirty();
```



## <a name="parameters"></a><span data-ttu-id="136a3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="136a3-108">Parameters</span></span>

<span data-ttu-id="136a3-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="136a3-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="136a3-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="136a3-110">Return value</span></span>

<span data-ttu-id="136a3-111">Retourne S \_ OK si [**CBasePropertyPage :: m \_ BDirty**](cbasepropertypage-m-bdirty.md) a la **valeur true**, ou la \_ valeur false dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="136a3-111">Returns S\_OK if [**CBasePropertyPage::m\_bDirty**](cbasepropertypage-m-bdirty.md) is **TRUE**, or S\_FALSE otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="136a3-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="136a3-112">Requirements</span></span>



| <span data-ttu-id="136a3-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="136a3-113">Requirement</span></span> | <span data-ttu-id="136a3-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="136a3-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="136a3-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="136a3-115">Header</span></span><br/>  | <dl> <span data-ttu-id="136a3-116"><dt>Cprop. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="136a3-116"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="136a3-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="136a3-117">Library</span></span><br/> | <dl> <span data-ttu-id="136a3-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="136a3-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="136a3-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="136a3-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="136a3-120">**CBasePropertyPage, classe**</span><span class="sxs-lookup"><span data-stu-id="136a3-120">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




