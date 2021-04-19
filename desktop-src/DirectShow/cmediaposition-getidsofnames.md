---
description: La méthode GetIDsOfNames mappe un ensemble de noms à un ensemble correspondant de DISPID.
ms.assetid: 4d3780ff-905f-4166-86d4-32395090b5cb
title: CMediaPosition. GetIDsOfNames, méthode (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.GetIDsOfNames
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dc2c7eee4304bb32ac1af2759bc2f094aca1d592
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523446"
---
# <a name="cmediapositiongetidsofnames-method"></a><span data-ttu-id="77434-103">CMediaPosition. GetIDsOfNames, méthode</span><span class="sxs-lookup"><span data-stu-id="77434-103">CMediaPosition.GetIDsOfNames method</span></span>

<span data-ttu-id="77434-104">La `GetIDsOfNames` méthode mappe un ensemble de noms à un ensemble correspondant de DISPID.</span><span class="sxs-lookup"><span data-stu-id="77434-104">The `GetIDsOfNames` method maps a set of names to a corresponding set of DISPIDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="77434-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="77434-105">Syntax</span></span>


```C++
HRESULT GetIDsOfNames(
   REFIID  riid,
   OLECHAR **rgszNames,
   UINT    cNames,
   LCID    lcid,
   DISPID  *rgdispid
);
```



## <a name="parameters"></a><span data-ttu-id="77434-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="77434-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77434-107">*riid*</span><span class="sxs-lookup"><span data-stu-id="77434-107">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="77434-108">Réservé.</span><span class="sxs-lookup"><span data-stu-id="77434-108">Reserved.</span></span> <span data-ttu-id="77434-109">Utilisez l’IID \_ null.</span><span class="sxs-lookup"><span data-stu-id="77434-109">Use IID\_NULL.</span></span>

</dd> <dt>

<span data-ttu-id="77434-110">*rgszNames*</span><span class="sxs-lookup"><span data-stu-id="77434-110">*rgszNames*</span></span> 
</dt> <dd>

<span data-ttu-id="77434-111">Adresse d’un tableau de chaînes de caractères larges qui contiennent les noms à mapper.</span><span class="sxs-lookup"><span data-stu-id="77434-111">Address of an array of wide-character strings that contain the names to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="77434-112">*Enregistrements CNAME*</span><span class="sxs-lookup"><span data-stu-id="77434-112">*cNames*</span></span> 
</dt> <dd>

<span data-ttu-id="77434-113">Taille du tableau donnée par le paramètre *rgszNames* .</span><span class="sxs-lookup"><span data-stu-id="77434-113">Size of the array given by the *rgszNames* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="77434-114">*lcid*</span><span class="sxs-lookup"><span data-stu-id="77434-114">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="77434-115">Contexte des paramètres régionaux dans lequel interpréter les noms.</span><span class="sxs-lookup"><span data-stu-id="77434-115">Locale context in which to interpret the names.</span></span> <span data-ttu-id="77434-116">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="77434-116">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="77434-117">*rgdispid*</span><span class="sxs-lookup"><span data-stu-id="77434-117">*rgdispid*</span></span> 
</dt> <dd>

<span data-ttu-id="77434-118">Pointeur vers un tableau qui reçoit les DISPID.</span><span class="sxs-lookup"><span data-stu-id="77434-118">Pointer to an array that receives the DISPIDs.</span></span> <span data-ttu-id="77434-119">Chaque élément de reçoit un identificateur qui correspond à l’un des noms transmis dans le paramètre *rgszNames* .</span><span class="sxs-lookup"><span data-stu-id="77434-119">Each element of receives an identifier that corresponds to one of the names passed in the *rgszNames* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77434-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="77434-120">Return value</span></span>

<span data-ttu-id="77434-121">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="77434-121">Returns an **HRESULT** value.</span></span> <span data-ttu-id="77434-122">Les valeurs possibles sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="77434-122">Possible values include the following.</span></span>



| <span data-ttu-id="77434-123">Code de retour</span><span class="sxs-lookup"><span data-stu-id="77434-123">Return code</span></span>                                                                                         | <span data-ttu-id="77434-124">Description</span><span class="sxs-lookup"><span data-stu-id="77434-124">Description</span></span>                                         |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="77434-125"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="77434-125"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="77434-126">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="77434-126">Success.</span></span><br/>                                 |
| <dl> <span data-ttu-id="77434-127"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="77434-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="77434-128">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="77434-128">Insufficient memory.</span></span><br/>                     |
| <dl> <span data-ttu-id="77434-129"><dt>**\_UNKNOWNNAME DISP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="77434-129"><dt>**DISP\_E\_UNKNOWNNAME**</dt></span></span> </dl> | <span data-ttu-id="77434-130">Un ou plusieurs noms sont inconnus.</span><span class="sxs-lookup"><span data-stu-id="77434-130">One or more of the names were not known.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="77434-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="77434-131">Requirements</span></span>



| <span data-ttu-id="77434-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="77434-132">Requirement</span></span> | <span data-ttu-id="77434-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="77434-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77434-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="77434-134">Header</span></span><br/>  | <dl> <span data-ttu-id="77434-135"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="77434-135"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="77434-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="77434-136">Library</span></span><br/> | <dl> <span data-ttu-id="77434-137"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="77434-137"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77434-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="77434-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77434-139">**CMediaPosition, classe**</span><span class="sxs-lookup"><span data-stu-id="77434-139">**CMediaPosition Class**</span></span>](cmediaposition.md)
</dt> </dl>

 

 




