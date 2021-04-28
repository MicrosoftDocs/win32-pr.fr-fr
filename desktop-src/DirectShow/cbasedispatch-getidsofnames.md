---
description: CBaseDispatch. GetIDsOfNames, méthode-la méthode GetIDsOfNames mappe un ensemble de noms à un ensemble correspondant de DISPID.
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
ms.openlocfilehash: 3f3b718c95d588ffdc7fa63902e6b26ffbf11fd6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099917"
---
# <a name="cbasedispatchgetidsofnames-method"></a><span data-ttu-id="43078-103">CBaseDispatch. GetIDsOfNames, méthode</span><span class="sxs-lookup"><span data-stu-id="43078-103">CBaseDispatch.GetIDsOfNames method</span></span>

<span data-ttu-id="43078-104">La `GetIDsOfNames` méthode mappe un ensemble de noms à un ensemble correspondant de DISPID.</span><span class="sxs-lookup"><span data-stu-id="43078-104">The `GetIDsOfNames` method maps a set of names to a corresponding set of DISPIDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="43078-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="43078-105">Syntax</span></span>


```C++
HRESULT GetIDsOfNames(
   REFIID  riid,
   OLECHAR **rgszNames,
   UINT    cNames,
   LCID    lcid,
   DISPID  *rgdispid
);
```



## <a name="parameters"></a><span data-ttu-id="43078-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="43078-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43078-107">*riid*</span><span class="sxs-lookup"><span data-stu-id="43078-107">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="43078-108">Référence à un identificateur d’interface (IID) qui spécifie l’interface.</span><span class="sxs-lookup"><span data-stu-id="43078-108">Reference to an interface identifier (IID) that specifies the interface.</span></span>

</dd> <dt>

<span data-ttu-id="43078-109">*rgszNames*</span><span class="sxs-lookup"><span data-stu-id="43078-109">*rgszNames*</span></span> 
</dt> <dd>

<span data-ttu-id="43078-110">Adresse d’un tableau de chaînes de caractères larges qui contiennent les noms à mapper.</span><span class="sxs-lookup"><span data-stu-id="43078-110">Address of an array of wide-character strings that contain the names to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="43078-111">*Enregistrements CNAME*</span><span class="sxs-lookup"><span data-stu-id="43078-111">*cNames*</span></span> 
</dt> <dd>

<span data-ttu-id="43078-112">Taille du tableau donnée par le paramètre *rgszNames* .</span><span class="sxs-lookup"><span data-stu-id="43078-112">Size of the array given by the *rgszNames* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="43078-113">*lcid*</span><span class="sxs-lookup"><span data-stu-id="43078-113">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="43078-114">Contexte des paramètres régionaux dans lequel interpréter les noms.</span><span class="sxs-lookup"><span data-stu-id="43078-114">Locale context in which to interpret the names.</span></span> <span data-ttu-id="43078-115">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="43078-115">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="43078-116">*rgdispid*</span><span class="sxs-lookup"><span data-stu-id="43078-116">*rgdispid*</span></span> 
</dt> <dd>

<span data-ttu-id="43078-117">Pointeur vers un tableau qui reçoit les DISPID.</span><span class="sxs-lookup"><span data-stu-id="43078-117">Pointer to an array that receives the DISPIDs.</span></span> <span data-ttu-id="43078-118">Chaque élément de reçoit un identificateur qui correspond à l’un des noms transmis dans le paramètre *rgszNames* .</span><span class="sxs-lookup"><span data-stu-id="43078-118">Each element of receives an identifier that corresponds to one of the names passed in the *rgszNames* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43078-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="43078-119">Return value</span></span>

<span data-ttu-id="43078-120">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="43078-120">Returns an **HRESULT** value.</span></span> <span data-ttu-id="43078-121">Les valeurs possibles sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="43078-121">Possible values include the following.</span></span>



| <span data-ttu-id="43078-122">Code de retour</span><span class="sxs-lookup"><span data-stu-id="43078-122">Return code</span></span>                                                                                         | <span data-ttu-id="43078-123">Description</span><span class="sxs-lookup"><span data-stu-id="43078-123">Description</span></span>                                         |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="43078-124"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="43078-124"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="43078-125">Réussite.</span><span class="sxs-lookup"><span data-stu-id="43078-125">Success.</span></span><br/>                                 |
| <dl> <span data-ttu-id="43078-126"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="43078-126"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="43078-127">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="43078-127">Insufficient memory.</span></span><br/>                     |
| <dl> <span data-ttu-id="43078-128"><dt>**\_UNKNOWNNAME DISP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="43078-128"><dt>**DISP\_E\_UNKNOWNNAME**</dt></span></span> </dl> | <span data-ttu-id="43078-129">Un ou plusieurs noms sont inconnus.</span><span class="sxs-lookup"><span data-stu-id="43078-129">One or more of the names were not known.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="43078-130">Notes </span><span class="sxs-lookup"><span data-stu-id="43078-130">Remarks</span></span>

<span data-ttu-id="43078-131">Cette méthode se comporte comme la méthode **IDispatch :: GetIDsOfNames** , mais le paramètre *riid* spécifie l’interface sur laquelle récupérer les DISPID.</span><span class="sxs-lookup"><span data-stu-id="43078-131">This method behaves like the **IDispatch::GetIDsOfNames** method, but the *riid* parameter specifies the interface on which to retrieve DISPIDs.</span></span> <span data-ttu-id="43078-132">(Dans la version **IDispatch** , le paramètre *riid* est réservé.)</span><span class="sxs-lookup"><span data-stu-id="43078-132">(In the **IDispatch** version, the *riid* parameter is reserved.)</span></span>

<span data-ttu-id="43078-133">Si la méthode retourne DISP \_ E \_ UNKNOWNNAME, les DISPID retournés contiennent DISPID \_ Unknown pour chaque entrée correspondant à un nom inconnu.</span><span class="sxs-lookup"><span data-stu-id="43078-133">If the method returns DISP\_E\_UNKNOWNNAME, the returned DISPIDs contain DISPID\_UNKNOWN for each entry that corresponds to an unknown name.</span></span>

## <a name="requirements"></a><span data-ttu-id="43078-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="43078-134">Requirements</span></span>



| <span data-ttu-id="43078-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="43078-135">Requirement</span></span> | <span data-ttu-id="43078-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="43078-136">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43078-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="43078-137">Header</span></span><br/>  | <dl> <span data-ttu-id="43078-138"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="43078-138"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="43078-139">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="43078-139">Library</span></span><br/> | <dl> <span data-ttu-id="43078-140"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="43078-140"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43078-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43078-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43078-142">**CBaseDispatch, classe**</span><span class="sxs-lookup"><span data-stu-id="43078-142">**CBaseDispatch Class**</span></span>](cbasedispatch.md)
</dt> </dl>

 

 




