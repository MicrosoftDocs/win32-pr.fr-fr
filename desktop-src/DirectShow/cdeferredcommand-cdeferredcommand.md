---
description: Méthode constructeur CDeferredCommand. CDeferredCommand.
ms.assetid: 0b372fa2-78a9-4e38-813c-f18123716c6d
title: Constructeur CDeferredCommand. CDeferredCommand (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.CDeferredCommand
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9a10d8bba48902ed2d6fd66da8483cea1ba9aacc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119787"
---
# <a name="cdeferredcommandcdeferredcommand-constructor"></a><span data-ttu-id="5d657-103">Constructeur CDeferredCommand. CDeferredCommand</span><span class="sxs-lookup"><span data-stu-id="5d657-103">CDeferredCommand.CDeferredCommand constructor</span></span>

<span data-ttu-id="5d657-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="5d657-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d657-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5d657-105">Syntax</span></span>


```C++
CDeferredCommand(
   CCmdQueue *pQ,
   LPUNKNOWN pUnk,
   HRESULT   *phr,
   LPUNKNOWN pUnkExecutor,
   REFTIME   time,
   GUID      *iid,
   long      dispidMethod,
   short     wFlags,
   long      cArgs,
   VARIANT   *pDispParams,
   VARIANT   *pvarResult,
   short     *puArgErr,
   BOOL      bStream
);
```



## <a name="parameters"></a><span data-ttu-id="5d657-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5d657-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d657-107">*Québec*</span><span class="sxs-lookup"><span data-stu-id="5d657-107">*pQ*</span></span> 
</dt> <dd>

<span data-ttu-id="5d657-108">Pointeur vers un objet qui expose l’interface [**IQueueCommand**](/windows/desktop/api/Control/nn-control-iqueuecommand) .</span><span class="sxs-lookup"><span data-stu-id="5d657-108">Pointer to an object that exposes the [**IQueueCommand**](/windows/desktop/api/Control/nn-control-iqueuecommand) interface.</span></span>

</dd> <dt>

<span data-ttu-id="5d657-109">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="5d657-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="5d657-110">Pointeur vers l’interface **IUnknown** externe pour l’agrégation.</span><span class="sxs-lookup"><span data-stu-id="5d657-110">Pointer to the outer **IUnknown** interface for aggregation.</span></span>

</dd> <dt>

<span data-ttu-id="5d657-111">*phr*</span><span class="sxs-lookup"><span data-stu-id="5d657-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="5d657-112">Pointeur vers une valeur **HRESULT** retournée.</span><span class="sxs-lookup"><span data-stu-id="5d657-112">Pointer to a returned **HRESULT** value.</span></span>

</dd> <dt>

<span data-ttu-id="5d657-113">*pUnkExecutor*</span><span class="sxs-lookup"><span data-stu-id="5d657-113">*pUnkExecutor*</span></span> 
</dt> <dd>

<span data-ttu-id="5d657-114">Pointeur vers l’objet qui exécutera cette commande.</span><span class="sxs-lookup"><span data-stu-id="5d657-114">Pointer to the object that will carry out this command.</span></span>

</dd> <dt>

<span data-ttu-id="5d657-115">*time*</span><span class="sxs-lookup"><span data-stu-id="5d657-115">*time*</span></span> 
</dt> <dd>

<span data-ttu-id="5d657-116">Heure à laquelle la commande sera exécutée.</span><span class="sxs-lookup"><span data-stu-id="5d657-116">Time at which the command will be run.</span></span>

</dd> <dt>

<span data-ttu-id="5d657-117">*vaut*</span><span class="sxs-lookup"><span data-stu-id="5d657-117">*iid*</span></span> 
</dt> <dd>

<span data-ttu-id="5d657-118">Pointeur vers l’identificateur global unique (**GUID**) de l’interface qui contient la méthode.</span><span class="sxs-lookup"><span data-stu-id="5d657-118">Pointer to the globally unique identifier (**GUID**) of the interface that contains the method.</span></span>

</dd> <dt>

<span data-ttu-id="5d657-119">*dispidMethod*</span><span class="sxs-lookup"><span data-stu-id="5d657-119">*dispidMethod*</span></span> 
</dt> <dd>

<span data-ttu-id="5d657-120">Méthode sur l’interface à appeler.</span><span class="sxs-lookup"><span data-stu-id="5d657-120">Method on the interface to call.</span></span>

</dd> <dt>

<span data-ttu-id="5d657-121">*wFlags*</span><span class="sxs-lookup"><span data-stu-id="5d657-121">*wFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="5d657-122">Contexte de l’appel.</span><span class="sxs-lookup"><span data-stu-id="5d657-122">Context of the invocation.</span></span>

</dd> <dt>

<span data-ttu-id="5d657-123">*cArgs*</span><span class="sxs-lookup"><span data-stu-id="5d657-123">*cArgs*</span></span> 
</dt> <dd>

<span data-ttu-id="5d657-124">Nombre d’arguments passés.</span><span class="sxs-lookup"><span data-stu-id="5d657-124">Number of arguments passed.</span></span>

</dd> <dt>

<span data-ttu-id="5d657-125">*pDispParams*</span><span class="sxs-lookup"><span data-stu-id="5d657-125">*pDispParams*</span></span> 
</dt> <dd>

<span data-ttu-id="5d657-126">Pointeur désignant une liste de types variant d’arguments.</span><span class="sxs-lookup"><span data-stu-id="5d657-126">Pointer to a list of argument variant types.</span></span>

</dd> <dt>

<span data-ttu-id="5d657-127">*pvarResult*</span><span class="sxs-lookup"><span data-stu-id="5d657-127">*pvarResult*</span></span> 
</dt> <dd>

<span data-ttu-id="5d657-128">Pointeur vers une liste de types variant retournée, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="5d657-128">Pointer to a returned variant type list, if any.</span></span>

</dd> <dt>

<span data-ttu-id="5d657-129">*puArgErr*</span><span class="sxs-lookup"><span data-stu-id="5d657-129">*puArgErr*</span></span> 
</dt> <dd>

<span data-ttu-id="5d657-130">Pointeur vers le dernier argument de la liste de paramètres *pDispParams* avec une erreur.</span><span class="sxs-lookup"><span data-stu-id="5d657-130">Pointer to the last argument in the *pDispParams* parameter list with an error.</span></span>

</dd> <dt>

<span data-ttu-id="5d657-131">*bStream*</span><span class="sxs-lookup"><span data-stu-id="5d657-131">*bStream*</span></span> 
</dt> <dd>

<span data-ttu-id="5d657-132">Valeur indiquant si l’heure de la commande différée est en temps de flux (**true**) ou en temps de présentation (**false**).</span><span class="sxs-lookup"><span data-stu-id="5d657-132">Value indicating whether the deferred command time is in stream time (**TRUE**) or presentation time (**FALSE**).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5d657-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5d657-133">Requirements</span></span>



| <span data-ttu-id="5d657-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5d657-134">Requirement</span></span> | <span data-ttu-id="5d657-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d657-135">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d657-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="5d657-136">Header</span></span><br/>  | <dl> <span data-ttu-id="5d657-137"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5d657-137"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5d657-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5d657-138">Library</span></span><br/> | <dl> <span data-ttu-id="5d657-139"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5d657-139"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d657-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d657-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d657-141">**CDeferredCommand, classe**</span><span class="sxs-lookup"><span data-stu-id="5d657-141">**CDeferredCommand Class**</span></span>](cdeferredcommand.md)
</dt> </dl>

 

 




