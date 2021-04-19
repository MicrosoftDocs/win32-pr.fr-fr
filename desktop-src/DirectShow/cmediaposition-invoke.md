---
description: La méthode Invoke fournit l’accès aux propriétés et aux méthodes exposées par l’objet.
ms.assetid: 3c03751d-239b-4cc5-bfab-8d1aed1074b8
title: CMediaPosition. Invoke, méthode (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.Invoke
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3955848bf2a87e0983ddd7dc3bef48f157ae6648
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537119"
---
# <a name="cmediapositioninvoke-method"></a><span data-ttu-id="1da89-103">CMediaPosition. Invoke, méthode</span><span class="sxs-lookup"><span data-stu-id="1da89-103">CMediaPosition.Invoke method</span></span>

<span data-ttu-id="1da89-104">La `Invoke` méthode fournit l’accès aux propriétés et aux méthodes exposées par l’objet.</span><span class="sxs-lookup"><span data-stu-id="1da89-104">The `Invoke` method provides access to properties and methods exposed by the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="1da89-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1da89-105">Syntax</span></span>


```C++
HRESULT Invoke(
   DISPID     dispidMember,
   REFIID     riid,
   LCID       lcid,
   WORD       wFlags,
   DISPPARAMS *pdispparams,
   VARIANT    *pvarResult,
   EXCEPINFO  *pexcepinfo,
   UINT       *puArgErr
);
```



## <a name="parameters"></a><span data-ttu-id="1da89-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1da89-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1da89-107">*dispidMember*</span><span class="sxs-lookup"><span data-stu-id="1da89-107">*dispidMember*</span></span> 
</dt> <dd>

<span data-ttu-id="1da89-108">Identificateur du membre.</span><span class="sxs-lookup"><span data-stu-id="1da89-108">Identifier of the member.</span></span> <span data-ttu-id="1da89-109">Utilisez [**CMediaPosition :: GetIDsOfNames**](cmediaposition-getidsofnames.md) pour obtenir l’identificateur de dispatch.</span><span class="sxs-lookup"><span data-stu-id="1da89-109">Use [**CMediaPosition::GetIDsOfNames**](cmediaposition-getidsofnames.md) to obtain the dispatch identifier.</span></span>

</dd> <dt>

<span data-ttu-id="1da89-110">*riid*</span><span class="sxs-lookup"><span data-stu-id="1da89-110">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="1da89-111">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="1da89-111">Reserved for future use.</span></span> <span data-ttu-id="1da89-112">Doit être un IID \_ null.</span><span class="sxs-lookup"><span data-stu-id="1da89-112">Must be IID\_NULL.</span></span>

</dd> <dt>

<span data-ttu-id="1da89-113">*lcid*</span><span class="sxs-lookup"><span data-stu-id="1da89-113">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="1da89-114">Contexte des paramètres régionaux dans lequel interpréter les arguments.</span><span class="sxs-lookup"><span data-stu-id="1da89-114">Locale context in which to interpret arguments.</span></span>

</dd> <dt>

<span data-ttu-id="1da89-115">*wFlags*</span><span class="sxs-lookup"><span data-stu-id="1da89-115">*wFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="1da89-116">Indicateurs décrivant le contexte de l'appel.</span><span class="sxs-lookup"><span data-stu-id="1da89-116">Flags describing the context of the call.</span></span>

</dd> <dt>

<span data-ttu-id="1da89-117">*pdispparams*</span><span class="sxs-lookup"><span data-stu-id="1da89-117">*pdispparams*</span></span> 
</dt> <dd>

<span data-ttu-id="1da89-118">Pointeur vers une structure **DIPPARAMS** qui contient les arguments.</span><span class="sxs-lookup"><span data-stu-id="1da89-118">Pointer to a **DIPPARAMS** structure that contains the arguments.</span></span>

</dd> <dt>

<span data-ttu-id="1da89-119">*pvarResult*</span><span class="sxs-lookup"><span data-stu-id="1da89-119">*pvarResult*</span></span> 
</dt> <dd>

<span data-ttu-id="1da89-120">Pointeur vers un **Variant** qui reçoit le résultat, ou **null** si l’appelant n’attend aucun résultat.</span><span class="sxs-lookup"><span data-stu-id="1da89-120">Pointer to a **VARIANT** that receives the result, or **NULL** if the caller expects no result.</span></span>

</dd> <dt>

<span data-ttu-id="1da89-121">*pexcepinfo*</span><span class="sxs-lookup"><span data-stu-id="1da89-121">*pexcepinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="1da89-122">Pointeur vers une structure qui reçoit des informations sur l’exception.</span><span class="sxs-lookup"><span data-stu-id="1da89-122">Pointer to a structure that receives exception information.</span></span>

</dd> <dt>

<span data-ttu-id="1da89-123">*puArgErr*</span><span class="sxs-lookup"><span data-stu-id="1da89-123">*puArgErr*</span></span> 
</dt> <dd>

<span data-ttu-id="1da89-124">Pointeur vers une variable qui reçoit l’index du premier argument qui génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="1da89-124">Pointer to a variable that receives the index of the first argument that causes an error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1da89-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1da89-125">Return value</span></span>

<span data-ttu-id="1da89-126">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1da89-126">Returns an **HRESULT** value.</span></span> <span data-ttu-id="1da89-127">Les valeurs possibles sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="1da89-127">Possible values include the following.</span></span>



| <span data-ttu-id="1da89-128">Code de retour</span><span class="sxs-lookup"><span data-stu-id="1da89-128">Return code</span></span>                                                                                              | <span data-ttu-id="1da89-129">Description</span><span class="sxs-lookup"><span data-stu-id="1da89-129">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="1da89-130"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1da89-130"><dt>**S\_OK**</dt></span></span> </dl>                     | <span data-ttu-id="1da89-131">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="1da89-131">Success.</span></span><br/>                              |
| <dl> <span data-ttu-id="1da89-132"><dt>**\_UNKNOWNINTERFACE DISP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1da89-132"><dt>**DISP\_E\_UNKNOWNINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="1da89-133">Le paramètre *riid* n’est pas une valeur d’IID \_ null</span><span class="sxs-lookup"><span data-stu-id="1da89-133">The *riid* parameter is not IID\_NULL</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1da89-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1da89-134">Requirements</span></span>



| <span data-ttu-id="1da89-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1da89-135">Requirement</span></span> | <span data-ttu-id="1da89-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="1da89-136">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1da89-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="1da89-137">Header</span></span><br/>  | <dl> <span data-ttu-id="1da89-138"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1da89-138"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1da89-139">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1da89-139">Library</span></span><br/> | <dl> <span data-ttu-id="1da89-140"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1da89-140"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1da89-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1da89-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1da89-142">**CMediaPosition, classe**</span><span class="sxs-lookup"><span data-stu-id="1da89-142">**CMediaPosition Class**</span></span>](cmediaposition.md)
</dt> </dl>

 

 




