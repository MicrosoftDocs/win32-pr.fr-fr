---
description: 'Méthode CMediaControl. Invoke : fournit l’accès aux propriétés et aux méthodes exposées par un objet.'
ms.assetid: 05006f1e-24ff-4ed2-8291-2ba48495fec0
title: CMediaControl. Invoke, méthode (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl.Invoke
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fe077b2c69f603eef8737cbf7ea8c514e9b90c85
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085637"
---
# <a name="cmediacontrolinvoke-method"></a><span data-ttu-id="02d13-103">CMediaControl. Invoke, méthode</span><span class="sxs-lookup"><span data-stu-id="02d13-103">CMediaControl.Invoke method</span></span>

<span data-ttu-id="02d13-104">Fournit l'accès aux propriétés et aux méthodes exposées par un objet.</span><span class="sxs-lookup"><span data-stu-id="02d13-104">Provides access to properties and methods exposed by an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="02d13-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="02d13-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="02d13-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="02d13-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02d13-107">*dispidMember*</span><span class="sxs-lookup"><span data-stu-id="02d13-107">*dispidMember*</span></span> 
</dt> <dd>

<span data-ttu-id="02d13-108">Identificateur du membre.</span><span class="sxs-lookup"><span data-stu-id="02d13-108">Identifier of the member.</span></span> <span data-ttu-id="02d13-109">Utilisez [**CMediaControl :: GetIDsOfNames**](cmediacontrol-getidsofnames.md) ou la documentation de l’objet pour obtenir l’identificateur de dispatch.</span><span class="sxs-lookup"><span data-stu-id="02d13-109">Use [**CMediaControl::GetIDsOfNames**](cmediacontrol-getidsofnames.md) or the object's documentation to obtain the dispatch identifier.</span></span>

</dd> <dt>

<span data-ttu-id="02d13-110">*riid*</span><span class="sxs-lookup"><span data-stu-id="02d13-110">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="02d13-111">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="02d13-111">Reserved for future use.</span></span> <span data-ttu-id="02d13-112">Doit être un IID \_ null.</span><span class="sxs-lookup"><span data-stu-id="02d13-112">Must be IID\_NULL.</span></span>

</dd> <dt>

<span data-ttu-id="02d13-113">*lcid*</span><span class="sxs-lookup"><span data-stu-id="02d13-113">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="02d13-114">Contexte des paramètres régionaux dans lequel interpréter les arguments.</span><span class="sxs-lookup"><span data-stu-id="02d13-114">Locale context in which to interpret arguments.</span></span>

</dd> <dt>

<span data-ttu-id="02d13-115">*wFlags*</span><span class="sxs-lookup"><span data-stu-id="02d13-115">*wFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="02d13-116">Indicateurs décrivant le contexte de l' `CMediaControl::Invoke` appel.</span><span class="sxs-lookup"><span data-stu-id="02d13-116">Flags describing the context of the `CMediaControl::Invoke` call.</span></span>

</dd> <dt>

<span data-ttu-id="02d13-117">*pdispparams*</span><span class="sxs-lookup"><span data-stu-id="02d13-117">*pdispparams*</span></span> 
</dt> <dd>

<span data-ttu-id="02d13-118">Pointeur vers une structure qui contient un tableau d’arguments, un tableau d’ID de dispatch d’argument pour les arguments nommés et le nombre d’éléments dans les tableaux.</span><span class="sxs-lookup"><span data-stu-id="02d13-118">Pointer to a structure containing an array of arguments, an array of argument dispatch IDs for named arguments, and counts for number of elements in the arrays.</span></span>

</dd> <dt>

<span data-ttu-id="02d13-119">*pvarResult*</span><span class="sxs-lookup"><span data-stu-id="02d13-119">*pvarResult*</span></span> 
</dt> <dd>

<span data-ttu-id="02d13-120">Pointeur vers l’emplacement où le résultat doit être stocké, ou **null** si l’appelant n’attend aucun résultat.</span><span class="sxs-lookup"><span data-stu-id="02d13-120">Pointer to where the result is to be stored, or **NULL** if the caller expects no result.</span></span>

</dd> <dt>

<span data-ttu-id="02d13-121">*pexcepinfo*</span><span class="sxs-lookup"><span data-stu-id="02d13-121">*pexcepinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="02d13-122">Pointeur vers une structure contenant des informations sur les exceptions.</span><span class="sxs-lookup"><span data-stu-id="02d13-122">Pointer to a structure containing exception information.</span></span>

</dd> <dt>

<span data-ttu-id="02d13-123">*puArgErr*</span><span class="sxs-lookup"><span data-stu-id="02d13-123">*puArgErr*</span></span> 
</dt> <dd>

<span data-ttu-id="02d13-124">Pointeur vers l’index du premier argument, dans le tableau **rgvarg** de la structure **DISPPARAMS** , qui comporte une erreur.</span><span class="sxs-lookup"><span data-stu-id="02d13-124">Pointer to the index of the first argument, within the **DISPPARAMS** structure's **rgvarg** array, that has an error.</span></span> <span data-ttu-id="02d13-125">Pour plus d’informations sur **DISPPARAMS**, consultez le kit de développement Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="02d13-125">For more information on **DISPPARAMS**, see the Platform SDK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02d13-126">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="02d13-126">Return value</span></span>

<span data-ttu-id="02d13-127">Retourne la \_ valeur DISP E \_ UNKNOWNINTERFACE si *riid* n’est pas un IID \_ null.</span><span class="sxs-lookup"><span data-stu-id="02d13-127">Returns DISP\_E\_UNKNOWNINTERFACE if *riid* is not IID\_NULL.</span></span> <span data-ttu-id="02d13-128">Retourne l’un des codes d’erreur de [**CMediaControl :: GetTypeInfo**](cmediacontrol-gettypeinfo.md) si l’appel échoue.</span><span class="sxs-lookup"><span data-stu-id="02d13-128">Returns one of the error codes from [**CMediaControl::GetTypeInfo**](cmediacontrol-gettypeinfo.md) if the call fails.</span></span> <span data-ttu-id="02d13-129">Sinon, retourne le **HRESULT** de l’appel à **IDispatch :: Invoke**.</span><span class="sxs-lookup"><span data-stu-id="02d13-129">Otherwise, returns the **HRESULT** from the call to **IDispatch::Invoke**.</span></span>

## <a name="requirements"></a><span data-ttu-id="02d13-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="02d13-130">Requirements</span></span>



| <span data-ttu-id="02d13-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="02d13-131">Requirement</span></span> | <span data-ttu-id="02d13-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="02d13-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02d13-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="02d13-133">Header</span></span><br/>  | <dl> <span data-ttu-id="02d13-134"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="02d13-134"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="02d13-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="02d13-135">Library</span></span><br/> | <dl> <span data-ttu-id="02d13-136"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="02d13-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02d13-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="02d13-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02d13-138">**CMediaControl, classe**</span><span class="sxs-lookup"><span data-stu-id="02d13-138">**CMediaControl Class**</span></span>](cmediacontrol.md)
</dt> </dl>

 

 




