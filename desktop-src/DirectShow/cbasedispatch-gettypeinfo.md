---
description: La méthode GetTypeInfo récupère les informations de type de l’objet, qui peuvent ensuite être utilisées pour obtenir les informations de type d’une interface.
ms.assetid: aa06b97c-541b-44fc-bdef-97fd1f014e85
title: Méthode CBaseDispatch. GetTypeInfo (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseDispatch.GetTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1f63d79327d2f2bf2a60f06e0290aa34891e78ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532862"
---
# <a name="cbasedispatchgettypeinfo-method"></a><span data-ttu-id="7d1cb-103">Méthode CBaseDispatch. GetTypeInfo</span><span class="sxs-lookup"><span data-stu-id="7d1cb-103">CBaseDispatch.GetTypeInfo method</span></span>

<span data-ttu-id="7d1cb-104">La `GetTypeInfo` méthode récupère les informations de type de l’objet, qui peuvent ensuite être utilisées pour obtenir les informations de type d’une interface.</span><span class="sxs-lookup"><span data-stu-id="7d1cb-104">The `GetTypeInfo` method retrieves the type information for the object, which can then be used to get the type information for an interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d1cb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7d1cb-105">Syntax</span></span>


```C++
HRESULT GetTypeInfo(
   REFIID    riid,
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a><span data-ttu-id="7d1cb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7d1cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d1cb-107">*riid*</span><span class="sxs-lookup"><span data-stu-id="7d1cb-107">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="7d1cb-108">Référence à un identificateur d’interface (IID) qui spécifie l’interface.</span><span class="sxs-lookup"><span data-stu-id="7d1cb-108">Reference to an interface identifier (IID) that specifies the interface.</span></span>

</dd> <dt>

<span data-ttu-id="7d1cb-109">*itinfo*</span><span class="sxs-lookup"><span data-stu-id="7d1cb-109">*itinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="7d1cb-110">Informations de type à retourner.</span><span class="sxs-lookup"><span data-stu-id="7d1cb-110">Type information to return.</span></span> <span data-ttu-id="7d1cb-111">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="7d1cb-111">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="7d1cb-112">*lcid*</span><span class="sxs-lookup"><span data-stu-id="7d1cb-112">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="7d1cb-113">Identificateur de paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="7d1cb-113">Locale identifier.</span></span>

</dd> <dt>

<span data-ttu-id="7d1cb-114">*ppTInfo*</span><span class="sxs-lookup"><span data-stu-id="7d1cb-114">*pptinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="7d1cb-115">Adresse d’une variable qui reçoit un pointeur **ITypeInfo** .</span><span class="sxs-lookup"><span data-stu-id="7d1cb-115">Address of a variable that receives an **ITypeInfo** pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d1cb-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7d1cb-116">Return value</span></span>

<span data-ttu-id="7d1cb-117">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7d1cb-117">Returns an **HRESULT** value.</span></span> <span data-ttu-id="7d1cb-118">Les valeurs possibles sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="7d1cb-118">Possible values include the following.</span></span>



| <span data-ttu-id="7d1cb-119">Code de retour</span><span class="sxs-lookup"><span data-stu-id="7d1cb-119">Return code</span></span>                                                                                             | <span data-ttu-id="7d1cb-120">Description</span><span class="sxs-lookup"><span data-stu-id="7d1cb-120">Description</span></span>                                    |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="7d1cb-121"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7d1cb-121"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="7d1cb-122">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="7d1cb-122">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="7d1cb-123"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="7d1cb-123"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="7d1cb-124">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="7d1cb-124">**NULL** pointer argument.</span></span><br/>          |
| <dl> <span data-ttu-id="7d1cb-125"><dt>**TAPEZ \_ E \_ ELEMENTNOTFOUND**</dt></span><span class="sxs-lookup"><span data-stu-id="7d1cb-125"><dt>**TYPE\_E\_ELEMENTNOTFOUND**</dt></span></span> </dl> | <span data-ttu-id="7d1cb-126">Le paramètre *iTInfo* n’est pas égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="7d1cb-126">The *itinfo* parameter is not zero.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7d1cb-127">Notes</span><span class="sxs-lookup"><span data-stu-id="7d1cb-127">Remarks</span></span>

<span data-ttu-id="7d1cb-128">Cette méthode se comporte comme la méthode **IDispatch :: GetTypeInfo** .</span><span class="sxs-lookup"><span data-stu-id="7d1cb-128">This method behaves like the **IDispatch::GetTypeInfo** method.</span></span> <span data-ttu-id="7d1cb-129">Toutefois, il comprend un paramètre supplémentaire, *riid*, qui spécifie l’interface pour laquelle récupérer les informations de type.</span><span class="sxs-lookup"><span data-stu-id="7d1cb-129">However, it includes an additional parameter, *riid*, which specifies the interface for which to retrieve type information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d1cb-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7d1cb-130">Requirements</span></span>



| <span data-ttu-id="7d1cb-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7d1cb-131">Requirement</span></span> | <span data-ttu-id="7d1cb-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="7d1cb-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d1cb-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="7d1cb-133">Header</span></span><br/>  | <dl> <span data-ttu-id="7d1cb-134"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7d1cb-134"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7d1cb-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7d1cb-135">Library</span></span><br/> | <dl> <span data-ttu-id="7d1cb-136"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7d1cb-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d1cb-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7d1cb-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d1cb-138">**CBaseDispatch, classe**</span><span class="sxs-lookup"><span data-stu-id="7d1cb-138">**CBaseDispatch Class**</span></span>](cbasedispatch.md)
</dt> </dl>

 

 




