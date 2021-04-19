---
description: 'La méthode SetPageSite initialise la page de propriétés et fournit un pointeur vers l’interface IPropertyPageSite du frame de propriété. Cette méthode implémente la méthode IPropertyPage :: SetPageSite.'
ms.assetid: 16c4633f-2f91-4b1b-a47c-4ef945c3af00
title: Méthode CBasePropertyPage. SetPageSite (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.SetPageSite
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a165ff60971cef3d2373e0f07b2abee554308279
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542474"
---
# <a name="cbasepropertypagesetpagesite-method"></a><span data-ttu-id="da373-104">Méthode CBasePropertyPage. SetPageSite</span><span class="sxs-lookup"><span data-stu-id="da373-104">CBasePropertyPage.SetPageSite method</span></span>

<span data-ttu-id="da373-105">La `SetPageSite` méthode initialise la page de propriétés et fournit un pointeur vers l’interface **IPropertyPageSite** du frame de propriété.</span><span class="sxs-lookup"><span data-stu-id="da373-105">The `SetPageSite` method initializes the property page and provides a pointer to the property frame's **IPropertyPageSite** interface.</span></span> <span data-ttu-id="da373-106">Cette méthode implémente la méthode **IPropertyPage :: SetPageSite** .</span><span class="sxs-lookup"><span data-stu-id="da373-106">This method implements the **IPropertyPage::SetPageSite** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="da373-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="da373-107">Syntax</span></span>


```C++
HRESULT SetPageSite(
   IPropertyPageSite *pPageSite
);
```



## <a name="parameters"></a><span data-ttu-id="da373-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="da373-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da373-109">*pPageSite*</span><span class="sxs-lookup"><span data-stu-id="da373-109">*pPageSite*</span></span> 
</dt> <dd>

<span data-ttu-id="da373-110">Pointeur vers l’interface **IPropertyPageSite** .</span><span class="sxs-lookup"><span data-stu-id="da373-110">Pointer to the **IPropertyPageSite** interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da373-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="da373-111">Return value</span></span>

<span data-ttu-id="da373-112">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="da373-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="da373-113">Les valeurs possibles sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="da373-113">Possible values include the following.</span></span>



| <span data-ttu-id="da373-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="da373-114">Return code</span></span>                                                                                  | <span data-ttu-id="da373-115">Description</span><span class="sxs-lookup"><span data-stu-id="da373-115">Description</span></span>                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="da373-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="da373-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="da373-117">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="da373-117">Success.</span></span><br/>            |
| <dl> <span data-ttu-id="da373-118"><dt>**E \_ inattendu**</dt></span><span class="sxs-lookup"><span data-stu-id="da373-118"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="da373-119">Erreur inattendue.</span><span class="sxs-lookup"><span data-stu-id="da373-119">Unexpected failure.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="da373-120">Notes</span><span class="sxs-lookup"><span data-stu-id="da373-120">Remarks</span></span>

<span data-ttu-id="da373-121">La méthode stocke le pointeur *pPageSite* dans la variable membre [**CBasePropertyPage :: m \_ pPageSite**](cbasepropertypage-m-ppagesite.md) .</span><span class="sxs-lookup"><span data-stu-id="da373-121">The method stores the *pPageSite* pointer in the [**CBasePropertyPage::m\_pPageSite**](cbasepropertypage-m-ppagesite.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="da373-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="da373-122">Requirements</span></span>



| <span data-ttu-id="da373-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="da373-123">Requirement</span></span> | <span data-ttu-id="da373-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="da373-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da373-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="da373-125">Header</span></span><br/>  | <dl> <span data-ttu-id="da373-126"><dt>Cprop. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="da373-126"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="da373-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="da373-127">Library</span></span><br/> | <dl> <span data-ttu-id="da373-128"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="da373-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da373-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da373-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da373-130">**CBasePropertyPage, classe**</span><span class="sxs-lookup"><span data-stu-id="da373-130">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




