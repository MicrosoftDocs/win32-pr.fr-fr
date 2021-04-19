---
description: 'La méthode Apply applique les valeurs de page de propriétés actuelles à l’objet associé à la page de propriétés. Cette méthode implémente la méthode IPropertyPage :: apply.'
ms.assetid: 9fe759d1-2b46-4489-b7b8-b5a35330091d
title: CBasePropertyPage. Apply, méthode (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Apply
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21d1208979cca167b059cb720c492ac51c362c39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544454"
---
# <a name="cbasepropertypageapply-method"></a><span data-ttu-id="dfd81-104">CBasePropertyPage. Apply, méthode</span><span class="sxs-lookup"><span data-stu-id="dfd81-104">CBasePropertyPage.Apply method</span></span>

<span data-ttu-id="dfd81-105">La `Apply` méthode applique les valeurs de page de propriétés actuelles à l’objet associé à la page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="dfd81-105">The `Apply` method applies the current property page values to the object associated with the property page.</span></span> <span data-ttu-id="dfd81-106">Cette méthode implémente la méthode **IPropertyPage :: apply** .</span><span class="sxs-lookup"><span data-stu-id="dfd81-106">This method implements the **IPropertyPage::Apply** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfd81-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dfd81-107">Syntax</span></span>


```C++
HRESULT Apply();
```



## <a name="parameters"></a><span data-ttu-id="dfd81-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dfd81-108">Parameters</span></span>

<span data-ttu-id="dfd81-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="dfd81-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dfd81-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dfd81-110">Return value</span></span>

<span data-ttu-id="dfd81-111">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="dfd81-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="dfd81-112">Les valeurs possibles sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="dfd81-112">Possible values include the following.</span></span>



| <span data-ttu-id="dfd81-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="dfd81-113">Return code</span></span>                                                                                  | <span data-ttu-id="dfd81-114">Description</span><span class="sxs-lookup"><span data-stu-id="dfd81-114">Description</span></span>                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="dfd81-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="dfd81-115"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="dfd81-116">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="dfd81-116">Success.</span></span><br/>            |
| <dl> <span data-ttu-id="dfd81-117"><dt>**E \_ inattendu**</dt></span><span class="sxs-lookup"><span data-stu-id="dfd81-117"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="dfd81-118">Erreur inattendue.</span><span class="sxs-lookup"><span data-stu-id="dfd81-118">Unexpected failure.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dfd81-119">Notes</span><span class="sxs-lookup"><span data-stu-id="dfd81-119">Remarks</span></span>

<span data-ttu-id="dfd81-120">Si l’indicateur [**CBasePropertyPage :: m \_ bDirty**](cbasepropertypage-m-bdirty.md) a la **valeur true**, cette méthode appelle la méthode [**CBasePropertyPage :: OnApplyChanges**](cbasepropertypage-onapplychanges.md) .</span><span class="sxs-lookup"><span data-stu-id="dfd81-120">If the [**CBasePropertyPage::m\_bDirty**](cbasepropertypage-m-bdirty.md) flag is **TRUE**, this method calls the [**CBasePropertyPage::OnApplyChanges**](cbasepropertypage-onapplychanges.md) method.</span></span> <span data-ttu-id="dfd81-121">Remplacez **OnApplyChanges** pour appliquer les modifications à l’objet.</span><span class="sxs-lookup"><span data-stu-id="dfd81-121">Override **OnApplyChanges** to apply the changes to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfd81-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dfd81-122">Requirements</span></span>



| <span data-ttu-id="dfd81-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dfd81-123">Requirement</span></span> | <span data-ttu-id="dfd81-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="dfd81-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfd81-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="dfd81-125">Header</span></span><br/>  | <dl> <span data-ttu-id="dfd81-126"><dt>Cprop. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dfd81-126"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="dfd81-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="dfd81-127">Library</span></span><br/> | <dl> <span data-ttu-id="dfd81-128"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="dfd81-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfd81-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dfd81-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfd81-130">**CBasePropertyPage, classe**</span><span class="sxs-lookup"><span data-stu-id="dfd81-130">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




