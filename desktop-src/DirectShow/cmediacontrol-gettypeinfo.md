---
description: 'Méthode CMediaControl. GetTypeInfo : récupère un objet d’informations de type, qui peut récupérer les informations de type pour une interface.'
ms.assetid: 2014485f-d937-415d-a2fc-0c69269b5237
title: Méthode CMediaControl. GetTypeInfo (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl.GetTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 857dbdeee9a2add9ab77cae0ff97d69699d2dd2e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099127"
---
# <a name="cmediacontrolgettypeinfo-method"></a><span data-ttu-id="f3158-103">Méthode CMediaControl. GetTypeInfo</span><span class="sxs-lookup"><span data-stu-id="f3158-103">CMediaControl.GetTypeInfo method</span></span>

<span data-ttu-id="f3158-104">Récupère un objet d’informations de type, qui peut récupérer les informations de type pour une interface.</span><span class="sxs-lookup"><span data-stu-id="f3158-104">Retrieves a type-information object, which can retrieve the type information for an interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3158-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f3158-105">Syntax</span></span>


```C++
HRESULT GetTypeInfo(
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a><span data-ttu-id="f3158-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f3158-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3158-107">*itinfo*</span><span class="sxs-lookup"><span data-stu-id="f3158-107">*itinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="f3158-108">Informations de type à retourner.</span><span class="sxs-lookup"><span data-stu-id="f3158-108">Type information to return.</span></span> <span data-ttu-id="f3158-109">Passe zéro pour récupérer les informations de type pour l’implémentation **IDispatch** .</span><span class="sxs-lookup"><span data-stu-id="f3158-109">Pass zero to retrieve type information for the **IDispatch** implementation.</span></span>

</dd> <dt>

<span data-ttu-id="f3158-110">*lcid*</span><span class="sxs-lookup"><span data-stu-id="f3158-110">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="f3158-111">ID de paramètres régionaux pour les informations de type.</span><span class="sxs-lookup"><span data-stu-id="f3158-111">Locale ID for the type information.</span></span> <span data-ttu-id="f3158-112">Pour les classes qui prennent en charge les noms de membres localisés, un objet peut être en mesure de retourner des informations de type différentes pour différentes langues.</span><span class="sxs-lookup"><span data-stu-id="f3158-112">For classes that support localized member names, an object might be able to return different type information for different languages.</span></span> <span data-ttu-id="f3158-113">Pour les classes qui ne prennent pas en charge les noms de membres localisés, ce paramètre peut être ignoré.</span><span class="sxs-lookup"><span data-stu-id="f3158-113">For classes that do not support localized member names, this parameter can be ignored.</span></span>

</dd> <dt>

<span data-ttu-id="f3158-114">*ppTInfo*</span><span class="sxs-lookup"><span data-stu-id="f3158-114">*pptinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="f3158-115">Adresse d’un pointeur vers l’objet d’informations de type demandé.</span><span class="sxs-lookup"><span data-stu-id="f3158-115">Address of a pointer to the type-information object requested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3158-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f3158-116">Return value</span></span>

<span data-ttu-id="f3158-117">Retourne un \_ pointeur E si *ppTInfo* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="f3158-117">Returns an E\_POINTER if *pptinfo* is invalid.</span></span> <span data-ttu-id="f3158-118">Retourne le TYPE \_ E \_ ELEMENTNOTFOUND si *iTInfo* n’est pas égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="f3158-118">Returns TYPE\_E\_ELEMENTNOTFOUND if *itinfo* is not zero.</span></span> <span data-ttu-id="f3158-119">Retourne S \_ OK si réussit.</span><span class="sxs-lookup"><span data-stu-id="f3158-119">Returns S\_OK if is successful.</span></span> <span data-ttu-id="f3158-120">Sinon, retourne un **HRESULT** de l’un des appels pour récupérer le type.</span><span class="sxs-lookup"><span data-stu-id="f3158-120">Otherwise, returns an **HRESULT** from one of the calls to retrieve the type.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3158-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f3158-121">Requirements</span></span>



| <span data-ttu-id="f3158-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f3158-122">Requirement</span></span> | <span data-ttu-id="f3158-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3158-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3158-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="f3158-124">Header</span></span><br/>  | <dl> <span data-ttu-id="f3158-125"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f3158-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f3158-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f3158-126">Library</span></span><br/> | <dl> <span data-ttu-id="f3158-127"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f3158-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3158-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3158-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3158-129">**CMediaControl, classe**</span><span class="sxs-lookup"><span data-stu-id="f3158-129">**CMediaControl Class**</span></span>](cmediacontrol.md)
</dt> </dl>

 

 




