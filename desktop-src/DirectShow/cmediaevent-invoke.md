---
description: 'Méthode CMediaEvent. Invoke : fournit l’accès aux propriétés et aux méthodes exposées par un objet.'
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
ms.openlocfilehash: ea812d0c7629b98d90f3f7e535d229c707452b23
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095537"
---
# <a name="cmediaeventinvoke-method"></a><span data-ttu-id="0e8c7-103">CMediaEvent. Invoke, méthode</span><span class="sxs-lookup"><span data-stu-id="0e8c7-103">CMediaEvent.Invoke method</span></span>

<span data-ttu-id="0e8c7-104">Fournit l'accès aux propriétés et aux méthodes exposées par un objet.</span><span class="sxs-lookup"><span data-stu-id="0e8c7-104">Provides access to properties and methods exposed by an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e8c7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0e8c7-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="0e8c7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0e8c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e8c7-107">*dispidMember*</span><span class="sxs-lookup"><span data-stu-id="0e8c7-107">*dispidMember*</span></span> 
</dt> <dd>

<span data-ttu-id="0e8c7-108">Identificateur du membre.</span><span class="sxs-lookup"><span data-stu-id="0e8c7-108">Identifier of the member.</span></span> <span data-ttu-id="0e8c7-109">Utilisez [**CMediaEvent :: GetIDsOfNames**](cmediaevent-getidsofnames.md) ou la documentation de l’objet pour obtenir l’identificateur de dispatch.</span><span class="sxs-lookup"><span data-stu-id="0e8c7-109">Use [**CMediaEvent::GetIDsOfNames**](cmediaevent-getidsofnames.md) or the object's documentation to obtain the dispatch identifier.</span></span>

</dd> <dt>

<span data-ttu-id="0e8c7-110">*riid*</span><span class="sxs-lookup"><span data-stu-id="0e8c7-110">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="0e8c7-111">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="0e8c7-111">Reserved for future use.</span></span> <span data-ttu-id="0e8c7-112">Doit être un IID \_ null.</span><span class="sxs-lookup"><span data-stu-id="0e8c7-112">Must be IID\_NULL.</span></span>

</dd> <dt>

<span data-ttu-id="0e8c7-113">*lcid*</span><span class="sxs-lookup"><span data-stu-id="0e8c7-113">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="0e8c7-114">Contexte des paramètres régionaux dans lequel interpréter les arguments.</span><span class="sxs-lookup"><span data-stu-id="0e8c7-114">Locale context in which to interpret arguments.</span></span>

</dd> <dt>

<span data-ttu-id="0e8c7-115">*wFlags*</span><span class="sxs-lookup"><span data-stu-id="0e8c7-115">*wFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="0e8c7-116">Indicateurs décrivant le contexte de l' `CMediaEvent::Invoke` appel.</span><span class="sxs-lookup"><span data-stu-id="0e8c7-116">Flags describing the context of the `CMediaEvent::Invoke` call.</span></span>

</dd> <dt>

<span data-ttu-id="0e8c7-117">*pdispparams*</span><span class="sxs-lookup"><span data-stu-id="0e8c7-117">*pdispparams*</span></span> 
</dt> <dd>

<span data-ttu-id="0e8c7-118">Pointeur vers une structure qui contient un tableau d’arguments, un tableau d’ID de dispatch d’argument pour les arguments nommés et le nombre d’éléments dans les tableaux.</span><span class="sxs-lookup"><span data-stu-id="0e8c7-118">Pointer to a structure containing an array of arguments, an array of argument dispatch IDs for named arguments, and counts for the number of elements in the arrays.</span></span>

</dd> <dt>

<span data-ttu-id="0e8c7-119">*pvarResult*</span><span class="sxs-lookup"><span data-stu-id="0e8c7-119">*pvarResult*</span></span> 
</dt> <dd>

<span data-ttu-id="0e8c7-120">Pointeur vers l’emplacement où le résultat doit être stocké, ou **null** si l’appelant n’attend aucun résultat.</span><span class="sxs-lookup"><span data-stu-id="0e8c7-120">Pointer to where the result is to be stored, or **NULL** if the caller expects no result.</span></span>

</dd> <dt>

<span data-ttu-id="0e8c7-121">*pexcepinfo*</span><span class="sxs-lookup"><span data-stu-id="0e8c7-121">*pexcepinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="0e8c7-122">Pointeur vers une structure contenant des informations sur les exceptions.</span><span class="sxs-lookup"><span data-stu-id="0e8c7-122">Pointer to a structure containing exception information.</span></span>

</dd> <dt>

<span data-ttu-id="0e8c7-123">*puArgErr*</span><span class="sxs-lookup"><span data-stu-id="0e8c7-123">*puArgErr*</span></span> 
</dt> <dd>

<span data-ttu-id="0e8c7-124">Pointeur vers l’index du premier argument, dans le tableau **rgvarg** de la structure **DISPPARAMS** , qui comporte une erreur.</span><span class="sxs-lookup"><span data-stu-id="0e8c7-124">Pointer to the index of the first argument, within the **DISPPARAMS** structure's **rgvarg** array, that has an error.</span></span> <span data-ttu-id="0e8c7-125">Pour plus d’informations sur **DISPPARAMS**, consultez le kit de développement Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="0e8c7-125">For more information on **DISPPARAMS**, see the Platform SDK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e8c7-126">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0e8c7-126">Return value</span></span>

<span data-ttu-id="0e8c7-127">Retourne la \_ valeur DISP E \_ UNKNOWNINTERFACE si *riid* n’est pas un IID \_ null.</span><span class="sxs-lookup"><span data-stu-id="0e8c7-127">Returns DISP\_E\_UNKNOWNINTERFACE if *riid* is not IID\_NULL.</span></span> <span data-ttu-id="0e8c7-128">Retourne l’un des codes d’erreur de [**CMediaEvent :: GetTypeInfo**](cmediaevent-gettypeinfo.md) si l’appel échoue.</span><span class="sxs-lookup"><span data-stu-id="0e8c7-128">Returns one of the error codes from [**CMediaEvent::GetTypeInfo**](cmediaevent-gettypeinfo.md) if the call fails.</span></span> <span data-ttu-id="0e8c7-129">Sinon, retourne le **HRESULT** de l’appel à **IDispatch :: Invoke**.</span><span class="sxs-lookup"><span data-stu-id="0e8c7-129">Otherwise, returns the **HRESULT** from the call to **IDispatch::Invoke**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e8c7-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e8c7-130">Requirements</span></span>



| <span data-ttu-id="0e8c7-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e8c7-131">Requirement</span></span> | <span data-ttu-id="0e8c7-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e8c7-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e8c7-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="0e8c7-133">Header</span></span><br/>  | <dl> <span data-ttu-id="0e8c7-134"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0e8c7-134"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0e8c7-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0e8c7-135">Library</span></span><br/> | <dl> <span data-ttu-id="0e8c7-136"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0e8c7-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e8c7-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e8c7-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e8c7-138">**CMediaEvent, classe**</span><span class="sxs-lookup"><span data-stu-id="0e8c7-138">**CMediaEvent Class**</span></span>](cmediaevent.md)
</dt> </dl>

 

 




