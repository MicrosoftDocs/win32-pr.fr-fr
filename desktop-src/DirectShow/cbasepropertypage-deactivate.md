---
description: La méthode Deactivate détruit la fenêtre de boîte de dialogue. Cette méthode implémente la méthode IPropertyPage ::D eactivate.
ms.assetid: f2d2f15f-15f6-4902-bafc-f58a684ff193
title: CBasePropertyPage. Deactivate, méthode (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Deactivate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 63a843502fc735cc41ff3656e83ef3d6cb839a19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545535"
---
# <a name="cbasepropertypagedeactivate-method"></a><span data-ttu-id="5697a-104">CBasePropertyPage. Deactivate, méthode</span><span class="sxs-lookup"><span data-stu-id="5697a-104">CBasePropertyPage.Deactivate method</span></span>

<span data-ttu-id="5697a-105">La `Deactivate` méthode détruit la fenêtre de boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="5697a-105">The `Deactivate` method destroys the dialog window.</span></span> <span data-ttu-id="5697a-106">Cette méthode implémente la méthode **IPropertyPage ::D eactivate** .</span><span class="sxs-lookup"><span data-stu-id="5697a-106">This method implements the **IPropertyPage::Deactivate** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5697a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5697a-107">Syntax</span></span>


```C++
HRESULT Deactivate();
```



## <a name="parameters"></a><span data-ttu-id="5697a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5697a-108">Parameters</span></span>

<span data-ttu-id="5697a-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="5697a-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5697a-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5697a-110">Return value</span></span>

<span data-ttu-id="5697a-111">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5697a-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="5697a-112">Les valeurs possibles sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="5697a-112">Possible values include the following.</span></span>



| <span data-ttu-id="5697a-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="5697a-113">Return code</span></span>                                                                                  | <span data-ttu-id="5697a-114">Description</span><span class="sxs-lookup"><span data-stu-id="5697a-114">Description</span></span>                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="5697a-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5697a-115"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="5697a-116">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="5697a-116">Success.</span></span><br/>            |
| <dl> <span data-ttu-id="5697a-117"><dt>**E \_ inattendu**</dt></span><span class="sxs-lookup"><span data-stu-id="5697a-117"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="5697a-118">Erreur inattendue.</span><span class="sxs-lookup"><span data-stu-id="5697a-118">Unexpected failure.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5697a-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5697a-119">Requirements</span></span>



| <span data-ttu-id="5697a-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5697a-120">Requirement</span></span> | <span data-ttu-id="5697a-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="5697a-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5697a-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="5697a-122">Header</span></span><br/>  | <dl> <span data-ttu-id="5697a-123"><dt>Cprop. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5697a-123"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="5697a-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5697a-124">Library</span></span><br/> | <dl> <span data-ttu-id="5697a-125"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5697a-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5697a-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5697a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5697a-127">**CBasePropertyPage, classe**</span><span class="sxs-lookup"><span data-stu-id="5697a-127">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> <dt>

[<span data-ttu-id="5697a-128">**CBasePropertyPage :: OnDeactivate**</span><span class="sxs-lookup"><span data-stu-id="5697a-128">**CBasePropertyPage::OnDeactivate**</span></span>](cbasepropertypage-ondeactivate.md)
</dt> </dl>

 

 




