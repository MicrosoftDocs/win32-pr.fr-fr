---
description: 'La méthode SetObjects fournit des pointeurs IUnknown pour les objets associés à la page de propriétés. Cette méthode implémente la méthode IPropertyPage :: SetObjects.'
ms.assetid: 11ca1e70-772c-414e-9647-7e4c4084c0d3
title: Méthode CBasePropertyPage. SetObjects (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.SetObjects
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 197c5eb82de76fb5a5f606d8a161e853b0c1e8f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539291"
---
# <a name="cbasepropertypagesetobjects-method"></a><span data-ttu-id="6d1dd-104">Méthode CBasePropertyPage. SetObjects</span><span class="sxs-lookup"><span data-stu-id="6d1dd-104">CBasePropertyPage.SetObjects method</span></span>

<span data-ttu-id="6d1dd-105">La `SetObjects` méthode fournit des pointeurs **IUnknown** pour les objets associés à la page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="6d1dd-105">The `SetObjects` method provides **IUnknown** pointers for the objects associated with the property page.</span></span> <span data-ttu-id="6d1dd-106">Cette méthode implémente la méthode **IPropertyPage :: SetObjects** .</span><span class="sxs-lookup"><span data-stu-id="6d1dd-106">This method implements the **IPropertyPage::SetObjects** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d1dd-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6d1dd-107">Syntax</span></span>


```C++
HRESULT SetObjects(
   ULONG     cObjects,
   LPUNKNOWN *ppUnk
);
```



## <a name="parameters"></a><span data-ttu-id="6d1dd-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6d1dd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d1dd-109">*cObjects*</span><span class="sxs-lookup"><span data-stu-id="6d1dd-109">*cObjects*</span></span> 
</dt> <dd>

<span data-ttu-id="6d1dd-110">Spécifie le nombre de pointeurs **IUnknown** dans le tableau spécifié par *ppUnk*.</span><span class="sxs-lookup"><span data-stu-id="6d1dd-110">Specifies the number of **IUnknown** pointers in the array specified by *ppUnk*.</span></span>

</dd> <dt>

<span data-ttu-id="6d1dd-111">*ppUnk*</span><span class="sxs-lookup"><span data-stu-id="6d1dd-111">*ppUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="6d1dd-112">Spécifie un tableau de pointeurs **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="6d1dd-112">Specifies an array of **IUnknown** pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d1dd-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6d1dd-113">Return value</span></span>

<span data-ttu-id="6d1dd-114">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6d1dd-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="6d1dd-115">Les valeurs possibles sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="6d1dd-115">Possible values include the following.</span></span>



| <span data-ttu-id="6d1dd-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="6d1dd-116">Return code</span></span>                                                                                  | <span data-ttu-id="6d1dd-117">Description</span><span class="sxs-lookup"><span data-stu-id="6d1dd-117">Description</span></span>                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="6d1dd-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6d1dd-118"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="6d1dd-119">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="6d1dd-119">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="6d1dd-120"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="6d1dd-120"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="6d1dd-121">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="6d1dd-121">**NULL** pointer argument.</span></span><br/> |
| <dl> <span data-ttu-id="6d1dd-122"><dt>**E \_ inattendu**</dt></span><span class="sxs-lookup"><span data-stu-id="6d1dd-122"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="6d1dd-123">Erreur inattendue.</span><span class="sxs-lookup"><span data-stu-id="6d1dd-123">Unexpected failure.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="6d1dd-124">Notes</span><span class="sxs-lookup"><span data-stu-id="6d1dd-124">Remarks</span></span>

<span data-ttu-id="6d1dd-125">Bien que *ppUnk* spécifie un tableau de pointeurs **IUnknown** , la classe **CBasePropertyPage** est conçue uniquement pour prendre en charge un objet associé.</span><span class="sxs-lookup"><span data-stu-id="6d1dd-125">Although *ppUnk* specifies an array of **IUnknown** pointers, the **CBasePropertyPage** class is designed only to support one associated object.</span></span> <span data-ttu-id="6d1dd-126">Si *CObjects* est supérieur à 1, la méthode retourne E \_ inattendue.</span><span class="sxs-lookup"><span data-stu-id="6d1dd-126">If *cObjects* is greater than 1, the method returns E\_UNEXPECTED.</span></span>

<span data-ttu-id="6d1dd-127">Si *CObjects* est égal à 1, cette méthode appelle la méthode [**CBasePropertyPage :: OnConnect**](cbasepropertypage-onconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="6d1dd-127">If *cObjects* equals 1, this method calls the [**CBasePropertyPage::OnConnect**](cbasepropertypage-onconnect.md) method.</span></span> <span data-ttu-id="6d1dd-128">Si *CObjects* est égal à 0, cette méthode appelle la méthode [**CBasePropertyPage :: OnDisconnect**](cbasepropertypage-ondisconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="6d1dd-128">If *cObjects* equals 0, this method calls the [**CBasePropertyPage::OnDisconnect**](cbasepropertypage-ondisconnect.md) method.</span></span> <span data-ttu-id="6d1dd-129">La classe dérivée doit substituer ces deux méthodes ; Pour plus d’informations, consultez les notes relatives à ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="6d1dd-129">The derived class should override both of those methods; for details, see the remarks for those methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d1dd-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6d1dd-130">Requirements</span></span>



| <span data-ttu-id="6d1dd-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6d1dd-131">Requirement</span></span> | <span data-ttu-id="6d1dd-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="6d1dd-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d1dd-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="6d1dd-133">Header</span></span><br/>  | <dl> <span data-ttu-id="6d1dd-134"><dt>Cprop. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6d1dd-134"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="6d1dd-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6d1dd-135">Library</span></span><br/> | <dl> <span data-ttu-id="6d1dd-136"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="6d1dd-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d1dd-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6d1dd-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d1dd-138">**CBasePropertyPage, classe**</span><span class="sxs-lookup"><span data-stu-id="6d1dd-138">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




