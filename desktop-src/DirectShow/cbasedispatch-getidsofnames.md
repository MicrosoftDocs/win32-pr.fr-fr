---
description: La méthode GetIDsOfNames mappe un ensemble de noms à un ensemble correspondant de DISPID.
ms.assetid: 0c0a2726-e89a-4eaf-aab0-e7e9e82e3c34
title: CBaseDispatch. GetIDsOfNames, méthode (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseDispatch.GetIDsOfNames
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cf11e4aa298f924b69c299c2f411dde88e28e5b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520805"
---
# <a name="cbasedispatchgetidsofnames-method"></a><span data-ttu-id="ce4ff-103">CBaseDispatch. GetIDsOfNames, méthode</span><span class="sxs-lookup"><span data-stu-id="ce4ff-103">CBaseDispatch.GetIDsOfNames method</span></span>

<span data-ttu-id="ce4ff-104">La `GetIDsOfNames` méthode mappe un ensemble de noms à un ensemble correspondant de DISPID.</span><span class="sxs-lookup"><span data-stu-id="ce4ff-104">The `GetIDsOfNames` method maps a set of names to a corresponding set of DISPIDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce4ff-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ce4ff-105">Syntax</span></span>


```C++
HRESULT GetIDsOfNames(
   REFIID  riid,
   OLECHAR **rgszNames,
   UINT    cNames,
   LCID    lcid,
   DISPID  *rgdispid
);
```



## <a name="parameters"></a><span data-ttu-id="ce4ff-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ce4ff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce4ff-107">*riid*</span><span class="sxs-lookup"><span data-stu-id="ce4ff-107">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="ce4ff-108">Référence à un identificateur d’interface (IID) qui spécifie l’interface.</span><span class="sxs-lookup"><span data-stu-id="ce4ff-108">Reference to an interface identifier (IID) that specifies the interface.</span></span>

</dd> <dt>

<span data-ttu-id="ce4ff-109">*rgszNames*</span><span class="sxs-lookup"><span data-stu-id="ce4ff-109">*rgszNames*</span></span> 
</dt> <dd>

<span data-ttu-id="ce4ff-110">Adresse d’un tableau de chaînes de caractères larges qui contiennent les noms à mapper.</span><span class="sxs-lookup"><span data-stu-id="ce4ff-110">Address of an array of wide-character strings that contain the names to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="ce4ff-111">*Enregistrements CNAME*</span><span class="sxs-lookup"><span data-stu-id="ce4ff-111">*cNames*</span></span> 
</dt> <dd>

<span data-ttu-id="ce4ff-112">Taille du tableau donnée par le paramètre *rgszNames* .</span><span class="sxs-lookup"><span data-stu-id="ce4ff-112">Size of the array given by the *rgszNames* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ce4ff-113">*lcid*</span><span class="sxs-lookup"><span data-stu-id="ce4ff-113">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="ce4ff-114">Contexte des paramètres régionaux dans lequel interpréter les noms.</span><span class="sxs-lookup"><span data-stu-id="ce4ff-114">Locale context in which to interpret the names.</span></span> <span data-ttu-id="ce4ff-115">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="ce4ff-115">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ce4ff-116">*rgdispid*</span><span class="sxs-lookup"><span data-stu-id="ce4ff-116">*rgdispid*</span></span> 
</dt> <dd>

<span data-ttu-id="ce4ff-117">Pointeur vers un tableau qui reçoit les DISPID.</span><span class="sxs-lookup"><span data-stu-id="ce4ff-117">Pointer to an array that receives the DISPIDs.</span></span> <span data-ttu-id="ce4ff-118">Chaque élément de reçoit un identificateur qui correspond à l’un des noms transmis dans le paramètre *rgszNames* .</span><span class="sxs-lookup"><span data-stu-id="ce4ff-118">Each element of receives an identifier that corresponds to one of the names passed in the *rgszNames* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce4ff-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ce4ff-119">Return value</span></span>

<span data-ttu-id="ce4ff-120">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ce4ff-120">Returns an **HRESULT** value.</span></span> <span data-ttu-id="ce4ff-121">Les valeurs possibles sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="ce4ff-121">Possible values include the following.</span></span>



| <span data-ttu-id="ce4ff-122">Code de retour</span><span class="sxs-lookup"><span data-stu-id="ce4ff-122">Return code</span></span>                                                                                         | <span data-ttu-id="ce4ff-123">Description</span><span class="sxs-lookup"><span data-stu-id="ce4ff-123">Description</span></span>                                         |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="ce4ff-124"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ce4ff-124"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="ce4ff-125">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="ce4ff-125">Success.</span></span><br/>                                 |
| <dl> <span data-ttu-id="ce4ff-126"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="ce4ff-126"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="ce4ff-127">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="ce4ff-127">Insufficient memory.</span></span><br/>                     |
| <dl> <span data-ttu-id="ce4ff-128"><dt>**\_UNKNOWNNAME DISP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ce4ff-128"><dt>**DISP\_E\_UNKNOWNNAME**</dt></span></span> </dl> | <span data-ttu-id="ce4ff-129">Un ou plusieurs noms sont inconnus.</span><span class="sxs-lookup"><span data-stu-id="ce4ff-129">One or more of the names were not known.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ce4ff-130">Notes</span><span class="sxs-lookup"><span data-stu-id="ce4ff-130">Remarks</span></span>

<span data-ttu-id="ce4ff-131">Cette méthode se comporte comme la méthode **IDispatch :: GetIDsOfNames** , mais le paramètre *riid* spécifie l’interface sur laquelle récupérer les DISPID.</span><span class="sxs-lookup"><span data-stu-id="ce4ff-131">This method behaves like the **IDispatch::GetIDsOfNames** method, but the *riid* parameter specifies the interface on which to retrieve DISPIDs.</span></span> <span data-ttu-id="ce4ff-132">(Dans la version **IDispatch** , le paramètre *riid* est réservé.)</span><span class="sxs-lookup"><span data-stu-id="ce4ff-132">(In the **IDispatch** version, the *riid* parameter is reserved.)</span></span>

<span data-ttu-id="ce4ff-133">Si la méthode retourne DISP \_ E \_ UNKNOWNNAME, les DISPID retournés contiennent DISPID \_ Unknown pour chaque entrée correspondant à un nom inconnu.</span><span class="sxs-lookup"><span data-stu-id="ce4ff-133">If the method returns DISP\_E\_UNKNOWNNAME, the returned DISPIDs contain DISPID\_UNKNOWN for each entry that corresponds to an unknown name.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce4ff-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ce4ff-134">Requirements</span></span>



| <span data-ttu-id="ce4ff-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ce4ff-135">Requirement</span></span> | <span data-ttu-id="ce4ff-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="ce4ff-136">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce4ff-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="ce4ff-137">Header</span></span><br/>  | <dl> <span data-ttu-id="ce4ff-138"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ce4ff-138"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ce4ff-139">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ce4ff-139">Library</span></span><br/> | <dl> <span data-ttu-id="ce4ff-140"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ce4ff-140"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce4ff-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ce4ff-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce4ff-142">**CBaseDispatch, classe**</span><span class="sxs-lookup"><span data-stu-id="ce4ff-142">**CBaseDispatch Class**</span></span>](cbasedispatch.md)
</dt> </dl>

 

 




