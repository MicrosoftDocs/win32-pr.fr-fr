---
description: 'Mappe une fonction membre unique et un ensemble facultatif de paramètres à un jeu correspondant d’identificateurs de dispatch entier, qui peut être utilisé lors des appels suivants à la fonction membre CMediaEvent :: Invoke.'
ms.assetid: 04e607e6-0b68-4371-aacf-01af308a56a3
title: CMediaEvent. GetIDsOfNames, méthode (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.GetIDsOfNames
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 191fa85264e4e7e22aa67f409db20cebd68f4319
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537860"
---
# <a name="cmediaeventgetidsofnames-method"></a><span data-ttu-id="1c412-103">CMediaEvent. GetIDsOfNames, méthode</span><span class="sxs-lookup"><span data-stu-id="1c412-103">CMediaEvent.GetIDsOfNames method</span></span>

<span data-ttu-id="1c412-104">Mappe une fonction membre unique et un ensemble facultatif de paramètres à un jeu correspondant d’identificateurs de dispatch entier, qui peut être utilisé lors des appels suivants à la fonction membre [**CMediaEvent :: Invoke**](cmediaevent-invoke.md) .</span><span class="sxs-lookup"><span data-stu-id="1c412-104">Maps a single member function and an optional set of parameters to a corresponding set of integer dispatch identifiers, which can be used upon subsequent calls to the [**CMediaEvent::Invoke**](cmediaevent-invoke.md) member function.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c412-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1c412-105">Syntax</span></span>


```C++
HRESULT GetIDsOfNames(
   REFIID  riid,
   OLECHAR **rgszNames,
   UINT    cNames,
   LCID    lcid,
   DISPID  *rgdispid
);
```



## <a name="parameters"></a><span data-ttu-id="1c412-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1c412-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c412-107">*riid*</span><span class="sxs-lookup"><span data-stu-id="1c412-107">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="1c412-108">Identificateur de référence.</span><span class="sxs-lookup"><span data-stu-id="1c412-108">Reference identifier.</span></span> <span data-ttu-id="1c412-109">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="1c412-109">Reserved for future use.</span></span> <span data-ttu-id="1c412-110">Doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="1c412-110">Must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1c412-111">*rgszNames*</span><span class="sxs-lookup"><span data-stu-id="1c412-111">*rgszNames*</span></span> 
</dt> <dd>

<span data-ttu-id="1c412-112">Adresse d’un pointeur vers un tableau de noms passé à mapper.</span><span class="sxs-lookup"><span data-stu-id="1c412-112">Address of a pointer to a passed-in array of names to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="1c412-113">*Enregistrements CNAME*</span><span class="sxs-lookup"><span data-stu-id="1c412-113">*cNames*</span></span> 
</dt> <dd>

<span data-ttu-id="1c412-114">Compte des noms à mapper.</span><span class="sxs-lookup"><span data-stu-id="1c412-114">Count of the names to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="1c412-115">*lcid*</span><span class="sxs-lookup"><span data-stu-id="1c412-115">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="1c412-116">Contexte des paramètres régionaux dans lequel interpréter les noms.</span><span class="sxs-lookup"><span data-stu-id="1c412-116">Locale context in which to interpret the names.</span></span>

</dd> <dt>

<span data-ttu-id="1c412-117">*rgdispid*</span><span class="sxs-lookup"><span data-stu-id="1c412-117">*rgdispid*</span></span> 
</dt> <dd>

<span data-ttu-id="1c412-118">Pointeur vers un tableau alloué par l’appelant, dont chaque élément contient un ID correspondant à l’un des noms transmis dans le tableau *rgszNames* .</span><span class="sxs-lookup"><span data-stu-id="1c412-118">Pointer to a caller-allocated array, each element of which contains an ID corresponding to one of the names passed in the *rgszNames* array.</span></span> <span data-ttu-id="1c412-119">Le premier élément représente le nom du membre ; les éléments suivants représentent chacun des paramètres du membre.</span><span class="sxs-lookup"><span data-stu-id="1c412-119">The first element represents the member name; the subsequent elements represent each of the member's parameters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c412-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1c412-120">Return value</span></span>

<span data-ttu-id="1c412-121">Retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="1c412-121">Returns one of the following values.</span></span>



| <span data-ttu-id="1c412-122">Code de retour</span><span class="sxs-lookup"><span data-stu-id="1c412-122">Return code</span></span>                                                                                            | <span data-ttu-id="1c412-123">Description</span><span class="sxs-lookup"><span data-stu-id="1c412-123">Description</span></span>                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1c412-124"><dt>**Impossible d’avoir un \_ \_ \_ CLSID inconnu**</dt></span><span class="sxs-lookup"><span data-stu-id="1c412-124"><dt>**DISP\_E\_UNKNOWN\_CLSID**</dt></span></span> </dl> | <span data-ttu-id="1c412-125">Le CLSID n’a pas été reconnu.</span><span class="sxs-lookup"><span data-stu-id="1c412-125">The CLSID was not recognized.</span></span><br/>                                                                                                             |
| <dl> <span data-ttu-id="1c412-126"><dt>**\_UNKNOWNNAME DISP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1c412-126"><dt>**DISP\_E\_UNKNOWNNAME**</dt></span></span> </dl>    | <span data-ttu-id="1c412-127">Un ou plusieurs noms sont inconnus.</span><span class="sxs-lookup"><span data-stu-id="1c412-127">One or more of the names were not known.</span></span> <span data-ttu-id="1c412-128">Les DISPID retournés contiennent \_ un DISPID inconnu pour chaque entrée correspondant à un nom inconnu.</span><span class="sxs-lookup"><span data-stu-id="1c412-128">The returned DISPIDs contain DISPID\_UNKNOWN for each entry that corresponds to an unknown name.</span></span><br/> |
| <dl> <span data-ttu-id="1c412-129"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="1c412-129"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>          | <span data-ttu-id="1c412-130">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="1c412-130">Out of memory.</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="1c412-131"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1c412-131"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="1c412-132">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="1c412-132">Success.</span></span><br/>                                                                                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="1c412-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1c412-133">Requirements</span></span>



| <span data-ttu-id="1c412-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1c412-134">Requirement</span></span> | <span data-ttu-id="1c412-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="1c412-135">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c412-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="1c412-136">Header</span></span><br/>  | <dl> <span data-ttu-id="1c412-137"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1c412-137"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1c412-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1c412-138">Library</span></span><br/> | <dl> <span data-ttu-id="1c412-139"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1c412-139"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c412-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1c412-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c412-141">**CMediaEvent, classe**</span><span class="sxs-lookup"><span data-stu-id="1c412-141">**CMediaEvent Class**</span></span>](cmediaevent.md)
</dt> </dl>

 

 




