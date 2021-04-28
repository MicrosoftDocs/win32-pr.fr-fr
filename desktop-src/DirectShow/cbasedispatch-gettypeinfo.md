---
description: 'Méthode CBaseDispatch. GetTypeInfo : la méthode GetTypeInfo récupère les informations de type de l’objet, qui peuvent ensuite être utilisées pour obtenir les informations de type d’une interface.'
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
ms.openlocfilehash: a9b1e21133b4fa561c743fefc6282c777b444e6f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108120117"
---
# <a name="cbasedispatchgettypeinfo-method"></a><span data-ttu-id="b4ecd-103">Méthode CBaseDispatch. GetTypeInfo</span><span class="sxs-lookup"><span data-stu-id="b4ecd-103">CBaseDispatch.GetTypeInfo method</span></span>

<span data-ttu-id="b4ecd-104">La `GetTypeInfo` méthode récupère les informations de type de l’objet, qui peuvent ensuite être utilisées pour obtenir les informations de type d’une interface.</span><span class="sxs-lookup"><span data-stu-id="b4ecd-104">The `GetTypeInfo` method retrieves the type information for the object, which can then be used to get the type information for an interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4ecd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b4ecd-105">Syntax</span></span>


```C++
HRESULT GetTypeInfo(
   REFIID    riid,
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a><span data-ttu-id="b4ecd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b4ecd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4ecd-107">*riid*</span><span class="sxs-lookup"><span data-stu-id="b4ecd-107">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="b4ecd-108">Référence à un identificateur d’interface (IID) qui spécifie l’interface.</span><span class="sxs-lookup"><span data-stu-id="b4ecd-108">Reference to an interface identifier (IID) that specifies the interface.</span></span>

</dd> <dt>

<span data-ttu-id="b4ecd-109">*itinfo*</span><span class="sxs-lookup"><span data-stu-id="b4ecd-109">*itinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="b4ecd-110">Informations de type à retourner.</span><span class="sxs-lookup"><span data-stu-id="b4ecd-110">Type information to return.</span></span> <span data-ttu-id="b4ecd-111">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="b4ecd-111">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="b4ecd-112">*lcid*</span><span class="sxs-lookup"><span data-stu-id="b4ecd-112">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="b4ecd-113">Identificateur de paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="b4ecd-113">Locale identifier.</span></span>

</dd> <dt>

<span data-ttu-id="b4ecd-114">*ppTInfo*</span><span class="sxs-lookup"><span data-stu-id="b4ecd-114">*pptinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="b4ecd-115">Adresse d’une variable qui reçoit un pointeur **ITypeInfo** .</span><span class="sxs-lookup"><span data-stu-id="b4ecd-115">Address of a variable that receives an **ITypeInfo** pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4ecd-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b4ecd-116">Return value</span></span>

<span data-ttu-id="b4ecd-117">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b4ecd-117">Returns an **HRESULT** value.</span></span> <span data-ttu-id="b4ecd-118">Les valeurs possibles sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="b4ecd-118">Possible values include the following.</span></span>



| <span data-ttu-id="b4ecd-119">Code de retour</span><span class="sxs-lookup"><span data-stu-id="b4ecd-119">Return code</span></span>                                                                                             | <span data-ttu-id="b4ecd-120">Description</span><span class="sxs-lookup"><span data-stu-id="b4ecd-120">Description</span></span>                                    |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="b4ecd-121"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b4ecd-121"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="b4ecd-122">Réussite.</span><span class="sxs-lookup"><span data-stu-id="b4ecd-122">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="b4ecd-123"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="b4ecd-123"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="b4ecd-124">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="b4ecd-124">**NULL** pointer argument.</span></span><br/>          |
| <dl> <span data-ttu-id="b4ecd-125"><dt>**TAPEZ \_ E \_ ELEMENTNOTFOUND**</dt></span><span class="sxs-lookup"><span data-stu-id="b4ecd-125"><dt>**TYPE\_E\_ELEMENTNOTFOUND**</dt></span></span> </dl> | <span data-ttu-id="b4ecd-126">Le paramètre *iTInfo* n’est pas égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="b4ecd-126">The *itinfo* parameter is not zero.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b4ecd-127">Notes </span><span class="sxs-lookup"><span data-stu-id="b4ecd-127">Remarks</span></span>

<span data-ttu-id="b4ecd-128">Cette méthode se comporte comme la méthode **IDispatch :: GetTypeInfo** .</span><span class="sxs-lookup"><span data-stu-id="b4ecd-128">This method behaves like the **IDispatch::GetTypeInfo** method.</span></span> <span data-ttu-id="b4ecd-129">Toutefois, il comprend un paramètre supplémentaire, *riid*, qui spécifie l’interface pour laquelle récupérer les informations de type.</span><span class="sxs-lookup"><span data-stu-id="b4ecd-129">However, it includes an additional parameter, *riid*, which specifies the interface for which to retrieve type information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4ecd-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b4ecd-130">Requirements</span></span>



| <span data-ttu-id="b4ecd-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b4ecd-131">Requirement</span></span> | <span data-ttu-id="b4ecd-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4ecd-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4ecd-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="b4ecd-133">Header</span></span><br/>  | <dl> <span data-ttu-id="b4ecd-134"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b4ecd-134"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b4ecd-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b4ecd-135">Library</span></span><br/> | <dl> <span data-ttu-id="b4ecd-136"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b4ecd-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4ecd-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4ecd-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4ecd-138">**CBaseDispatch, classe**</span><span class="sxs-lookup"><span data-stu-id="b4ecd-138">**CBaseDispatch Class**</span></span>](cbasedispatch.md)
</dt> </dl>

 

 




