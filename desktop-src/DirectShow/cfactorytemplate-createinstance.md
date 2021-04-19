---
description: La méthode CreateInstance appelle la fonction de création d’objet pour la classe.
ms.assetid: 8a7d5c56-867d-432d-a0c2-97b8e3cf8a69
title: CFactoryTemplate. CreateInstance, méthode (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CFactoryTemplate.CreateInstance
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0f67ba528943bc2a468419fc84db44359745d4a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540545"
---
# <a name="cfactorytemplatecreateinstance-method"></a><span data-ttu-id="060fa-103">CFactoryTemplate. CreateInstance, méthode</span><span class="sxs-lookup"><span data-stu-id="060fa-103">CFactoryTemplate.CreateInstance method</span></span>

<span data-ttu-id="060fa-104">La `CreateInstance` méthode appelle la fonction de création d’objet pour la classe.</span><span class="sxs-lookup"><span data-stu-id="060fa-104">The `CreateInstance` method calls the object-creation function for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="060fa-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="060fa-105">Syntax</span></span>


```C++
CUnknown* CreateInstance(
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="060fa-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="060fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="060fa-107">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="060fa-107">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="060fa-108">Pointeur vers l’interface **IUnknown** d’agrégation.</span><span class="sxs-lookup"><span data-stu-id="060fa-108">Pointer to the aggregating **IUnknown** interface.</span></span>

</dd> <dt>

<span data-ttu-id="060fa-109">*phr*</span><span class="sxs-lookup"><span data-stu-id="060fa-109">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="060fa-110">Pointeur vers une variable qui reçoit une valeur **HRESULT** indiquant la réussite ou l’échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="060fa-110">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="060fa-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="060fa-111">Return value</span></span>

<span data-ttu-id="060fa-112">Retourne une instance de l’objet de classe.</span><span class="sxs-lookup"><span data-stu-id="060fa-112">Returns an instance of the class object.</span></span>

## <a name="remarks"></a><span data-ttu-id="060fa-113">Notes</span><span class="sxs-lookup"><span data-stu-id="060fa-113">Remarks</span></span>

<span data-ttu-id="060fa-114">La méthode **IClassFactory :: CreateInstance** appelle cette méthode de classe.</span><span class="sxs-lookup"><span data-stu-id="060fa-114">The **IClassFactory::CreateInstance** method calls this class method.</span></span> <span data-ttu-id="060fa-115">Cette méthode appelle la fonction vers laquelle pointe la variable membre [**CFactoryTemplate :: m \_ lpfnNew**](cfactorytemplate-m-lpfnnew.md) .</span><span class="sxs-lookup"><span data-stu-id="060fa-115">This method calls the function pointed to by the [**CFactoryTemplate::m\_lpfnNew**](cfactorytemplate-m-lpfnnew.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="060fa-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="060fa-116">Requirements</span></span>



| <span data-ttu-id="060fa-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="060fa-117">Requirement</span></span> | <span data-ttu-id="060fa-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="060fa-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="060fa-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="060fa-119">Header</span></span><br/>  | <dl> <span data-ttu-id="060fa-120"><dt>ComBase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="060fa-120"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="060fa-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="060fa-121">Library</span></span><br/> | <dl> <span data-ttu-id="060fa-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="060fa-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="060fa-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="060fa-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="060fa-124">**CFactoryTemplate, classe**</span><span class="sxs-lookup"><span data-stu-id="060fa-124">**CFactoryTemplate Class**</span></span>](cfactorytemplate.md)
</dt> </dl>

 

 




