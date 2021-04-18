---
description: 'Mappe une fonction membre unique et un ensemble facultatif de paramètres à un jeu correspondant d’identificateurs de dispatch entier (DISPID), qui peuvent être utilisés lors des appels suivants à la fonction membre CMediaControl :: Invoke.'
ms.assetid: 9ce1b1aa-ea03-4a65-bff7-e46771cd0772
title: CMediaControl. GetIDsOfNames, méthode (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl.GetIDsOfNames
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f906db9540f0429e1e7831284e55edf8c29b6a03
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533077"
---
# <a name="cmediacontrolgetidsofnames-method"></a><span data-ttu-id="01b9f-103">CMediaControl. GetIDsOfNames, méthode</span><span class="sxs-lookup"><span data-stu-id="01b9f-103">CMediaControl.GetIDsOfNames method</span></span>

<span data-ttu-id="01b9f-104">Mappe une fonction membre unique et un ensemble facultatif de paramètres à un jeu correspondant d’identificateurs de dispatch entier (DISPID), qui peuvent être utilisés lors des appels suivants à la fonction membre [**CMediaControl :: Invoke**](cmediacontrol-invoke.md) .</span><span class="sxs-lookup"><span data-stu-id="01b9f-104">Maps a single member function and an optional set of parameters to a corresponding set of integer dispatch identifiers (DISPIDs), which can be used upon subsequent calls to the [**CMediaControl::Invoke**](cmediacontrol-invoke.md) member function.</span></span>

## <a name="syntax"></a><span data-ttu-id="01b9f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="01b9f-105">Syntax</span></span>


```C++
HRESULT GetIDsOfNames(
   REFIID  riid,
   OLECHAR **rgszNames,
   UINT    cNames,
   LCID    lcid,
   DISPID  *rgdispid
);
```



## <a name="parameters"></a><span data-ttu-id="01b9f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="01b9f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01b9f-107">*riid*</span><span class="sxs-lookup"><span data-stu-id="01b9f-107">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="01b9f-108">Identificateur de référence.</span><span class="sxs-lookup"><span data-stu-id="01b9f-108">Reference identifier.</span></span> <span data-ttu-id="01b9f-109">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="01b9f-109">Reserved for future use.</span></span> <span data-ttu-id="01b9f-110">Doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="01b9f-110">Must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="01b9f-111">*rgszNames*</span><span class="sxs-lookup"><span data-stu-id="01b9f-111">*rgszNames*</span></span> 
</dt> <dd>

<span data-ttu-id="01b9f-112">Adresse d’un pointeur vers un tableau de noms passé à mapper.</span><span class="sxs-lookup"><span data-stu-id="01b9f-112">Address of a pointer to a passed-in array of names to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="01b9f-113">*Enregistrements CNAME*</span><span class="sxs-lookup"><span data-stu-id="01b9f-113">*cNames*</span></span> 
</dt> <dd>

<span data-ttu-id="01b9f-114">Compte des noms à mapper.</span><span class="sxs-lookup"><span data-stu-id="01b9f-114">Count of the names to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="01b9f-115">*lcid*</span><span class="sxs-lookup"><span data-stu-id="01b9f-115">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="01b9f-116">Contexte des paramètres régionaux dans lequel interpréter les noms.</span><span class="sxs-lookup"><span data-stu-id="01b9f-116">Locale context in which to interpret the names.</span></span>

</dd> <dt>

<span data-ttu-id="01b9f-117">*rgdispid*</span><span class="sxs-lookup"><span data-stu-id="01b9f-117">*rgdispid*</span></span> 
</dt> <dd>

<span data-ttu-id="01b9f-118">Pointeur vers un tableau alloué par l’appelant, dont chaque élément contient un ID correspondant à l’un des noms transmis dans le tableau *rgszNames* .</span><span class="sxs-lookup"><span data-stu-id="01b9f-118">Pointer to a caller-allocated array, each element of which contains an ID corresponding to one of the names passed in the *rgszNames* array.</span></span> <span data-ttu-id="01b9f-119">Le premier élément représente le nom du membre ; les éléments suivants représentent chacun des paramètres du membre.</span><span class="sxs-lookup"><span data-stu-id="01b9f-119">The first element represents the member name; the subsequent elements represent each of the member's parameters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01b9f-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="01b9f-120">Return value</span></span>

<span data-ttu-id="01b9f-121">Retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="01b9f-121">Returns one of the following values.</span></span>



| <span data-ttu-id="01b9f-122">Code de retour</span><span class="sxs-lookup"><span data-stu-id="01b9f-122">Return code</span></span>                                                                                            | <span data-ttu-id="01b9f-123">Description</span><span class="sxs-lookup"><span data-stu-id="01b9f-123">Description</span></span>                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="01b9f-124"><dt>**Impossible d’avoir un \_ \_ \_ CLSID inconnu**</dt></span><span class="sxs-lookup"><span data-stu-id="01b9f-124"><dt>**DISP\_E\_UNKNOWN\_CLSID**</dt></span></span> </dl> | <span data-ttu-id="01b9f-125">Le CLSID n’a pas été reconnu.</span><span class="sxs-lookup"><span data-stu-id="01b9f-125">The CLSID was not recognized.</span></span><br/>                                                                                                             |
| <dl> <span data-ttu-id="01b9f-126"><dt>**\_UNKNOWNNAME DISP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="01b9f-126"><dt>**DISP\_E\_UNKNOWNNAME**</dt></span></span> </dl>    | <span data-ttu-id="01b9f-127">Un ou plusieurs noms sont inconnus.</span><span class="sxs-lookup"><span data-stu-id="01b9f-127">One or more of the names were not known.</span></span> <span data-ttu-id="01b9f-128">Les DISPID retournés contiennent \_ un DISPID inconnu pour chaque entrée correspondant à un nom inconnu.</span><span class="sxs-lookup"><span data-stu-id="01b9f-128">The returned DISPIDs contain DISPID\_UNKNOWN for each entry that corresponds to an unknown name.</span></span><br/> |
| <dl> <span data-ttu-id="01b9f-129"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="01b9f-129"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>          | <span data-ttu-id="01b9f-130">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="01b9f-130">Out of memory.</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="01b9f-131"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="01b9f-131"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="01b9f-132">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="01b9f-132">Success.</span></span><br/>                                                                                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="01b9f-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="01b9f-133">Requirements</span></span>



| <span data-ttu-id="01b9f-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="01b9f-134">Requirement</span></span> | <span data-ttu-id="01b9f-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="01b9f-135">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01b9f-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="01b9f-136">Header</span></span><br/>  | <dl> <span data-ttu-id="01b9f-137"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="01b9f-137"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="01b9f-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="01b9f-138">Library</span></span><br/> | <dl> <span data-ttu-id="01b9f-139"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="01b9f-139"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01b9f-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01b9f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01b9f-141">**CMediaControl, classe**</span><span class="sxs-lookup"><span data-stu-id="01b9f-141">**CMediaControl Class**</span></span>](cmediacontrol.md)
</dt> </dl>

 

 




