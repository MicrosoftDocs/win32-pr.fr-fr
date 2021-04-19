---
description: Fournit l'accès aux propriétés et aux méthodes exposées par un objet.
ms.assetid: 2b091b57-0855-489a-9a33-cfc75f63ad07
title: CMediaEvent. Invoke, méthode (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.Invoke
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 22482cffe11f62d50361bc950409858a2436d8a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541719"
---
# <a name="cmediaeventinvoke-method"></a><span data-ttu-id="2f974-103">CMediaEvent. Invoke, méthode</span><span class="sxs-lookup"><span data-stu-id="2f974-103">CMediaEvent.Invoke method</span></span>

<span data-ttu-id="2f974-104">Fournit l'accès aux propriétés et aux méthodes exposées par un objet.</span><span class="sxs-lookup"><span data-stu-id="2f974-104">Provides access to properties and methods exposed by an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f974-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2f974-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="2f974-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2f974-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f974-107">*dispidMember*</span><span class="sxs-lookup"><span data-stu-id="2f974-107">*dispidMember*</span></span> 
</dt> <dd>

<span data-ttu-id="2f974-108">Identificateur du membre.</span><span class="sxs-lookup"><span data-stu-id="2f974-108">Identifier of the member.</span></span> <span data-ttu-id="2f974-109">Utilisez [**CMediaEvent :: GetIDsOfNames**](cmediaevent-getidsofnames.md) ou la documentation de l’objet pour obtenir l’identificateur de dispatch.</span><span class="sxs-lookup"><span data-stu-id="2f974-109">Use [**CMediaEvent::GetIDsOfNames**](cmediaevent-getidsofnames.md) or the object's documentation to obtain the dispatch identifier.</span></span>

</dd> <dt>

<span data-ttu-id="2f974-110">*riid*</span><span class="sxs-lookup"><span data-stu-id="2f974-110">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="2f974-111">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="2f974-111">Reserved for future use.</span></span> <span data-ttu-id="2f974-112">Doit être un IID \_ null.</span><span class="sxs-lookup"><span data-stu-id="2f974-112">Must be IID\_NULL.</span></span>

</dd> <dt>

<span data-ttu-id="2f974-113">*lcid*</span><span class="sxs-lookup"><span data-stu-id="2f974-113">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="2f974-114">Contexte des paramètres régionaux dans lequel interpréter les arguments.</span><span class="sxs-lookup"><span data-stu-id="2f974-114">Locale context in which to interpret arguments.</span></span>

</dd> <dt>

<span data-ttu-id="2f974-115">*wFlags*</span><span class="sxs-lookup"><span data-stu-id="2f974-115">*wFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="2f974-116">Indicateurs décrivant le contexte de l' `CMediaEvent::Invoke` appel.</span><span class="sxs-lookup"><span data-stu-id="2f974-116">Flags describing the context of the `CMediaEvent::Invoke` call.</span></span>

</dd> <dt>

<span data-ttu-id="2f974-117">*pdispparams*</span><span class="sxs-lookup"><span data-stu-id="2f974-117">*pdispparams*</span></span> 
</dt> <dd>

<span data-ttu-id="2f974-118">Pointeur vers une structure qui contient un tableau d’arguments, un tableau d’ID de dispatch d’argument pour les arguments nommés et le nombre d’éléments dans les tableaux.</span><span class="sxs-lookup"><span data-stu-id="2f974-118">Pointer to a structure containing an array of arguments, an array of argument dispatch IDs for named arguments, and counts for the number of elements in the arrays.</span></span>

</dd> <dt>

<span data-ttu-id="2f974-119">*pvarResult*</span><span class="sxs-lookup"><span data-stu-id="2f974-119">*pvarResult*</span></span> 
</dt> <dd>

<span data-ttu-id="2f974-120">Pointeur vers l’emplacement où le résultat doit être stocké, ou **null** si l’appelant n’attend aucun résultat.</span><span class="sxs-lookup"><span data-stu-id="2f974-120">Pointer to where the result is to be stored, or **NULL** if the caller expects no result.</span></span>

</dd> <dt>

<span data-ttu-id="2f974-121">*pexcepinfo*</span><span class="sxs-lookup"><span data-stu-id="2f974-121">*pexcepinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="2f974-122">Pointeur vers une structure contenant des informations sur les exceptions.</span><span class="sxs-lookup"><span data-stu-id="2f974-122">Pointer to a structure containing exception information.</span></span>

</dd> <dt>

<span data-ttu-id="2f974-123">*puArgErr*</span><span class="sxs-lookup"><span data-stu-id="2f974-123">*puArgErr*</span></span> 
</dt> <dd>

<span data-ttu-id="2f974-124">Pointeur vers l’index du premier argument, dans le tableau **rgvarg** de la structure **DISPPARAMS** , qui comporte une erreur.</span><span class="sxs-lookup"><span data-stu-id="2f974-124">Pointer to the index of the first argument, within the **DISPPARAMS** structure's **rgvarg** array, that has an error.</span></span> <span data-ttu-id="2f974-125">Pour plus d’informations sur **DISPPARAMS**, consultez le kit de développement Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="2f974-125">For more information on **DISPPARAMS**, see the Platform SDK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f974-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2f974-126">Return value</span></span>

<span data-ttu-id="2f974-127">Retourne la \_ valeur DISP E \_ UNKNOWNINTERFACE si *riid* n’est pas un IID \_ null.</span><span class="sxs-lookup"><span data-stu-id="2f974-127">Returns DISP\_E\_UNKNOWNINTERFACE if *riid* is not IID\_NULL.</span></span> <span data-ttu-id="2f974-128">Retourne l’un des codes d’erreur de [**CMediaEvent :: GetTypeInfo**](cmediaevent-gettypeinfo.md) si l’appel échoue.</span><span class="sxs-lookup"><span data-stu-id="2f974-128">Returns one of the error codes from [**CMediaEvent::GetTypeInfo**](cmediaevent-gettypeinfo.md) if the call fails.</span></span> <span data-ttu-id="2f974-129">Sinon, retourne le **HRESULT** de l’appel à **IDispatch :: Invoke**.</span><span class="sxs-lookup"><span data-stu-id="2f974-129">Otherwise, returns the **HRESULT** from the call to **IDispatch::Invoke**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f974-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2f974-130">Requirements</span></span>



| <span data-ttu-id="2f974-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2f974-131">Requirement</span></span> | <span data-ttu-id="2f974-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="2f974-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f974-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="2f974-133">Header</span></span><br/>  | <dl> <span data-ttu-id="2f974-134"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2f974-134"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2f974-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2f974-135">Library</span></span><br/> | <dl> <span data-ttu-id="2f974-136"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="2f974-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f974-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2f974-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f974-138">**CMediaEvent, classe**</span><span class="sxs-lookup"><span data-stu-id="2f974-138">**CMediaEvent Class**</span></span>](cmediaevent.md)
</dt> </dl>

 

 




