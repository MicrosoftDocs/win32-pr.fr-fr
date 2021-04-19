---
description: Récupère un objet d’informations de type, qui peut récupérer les informations de type pour une interface.
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
ms.openlocfilehash: fe393922206744c23b534bf8d701d6292736c65a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532644"
---
# <a name="cmediacontrolgettypeinfo-method"></a><span data-ttu-id="3cadd-103">Méthode CMediaControl. GetTypeInfo</span><span class="sxs-lookup"><span data-stu-id="3cadd-103">CMediaControl.GetTypeInfo method</span></span>

<span data-ttu-id="3cadd-104">Récupère un objet d’informations de type, qui peut récupérer les informations de type pour une interface.</span><span class="sxs-lookup"><span data-stu-id="3cadd-104">Retrieves a type-information object, which can retrieve the type information for an interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cadd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3cadd-105">Syntax</span></span>


```C++
HRESULT GetTypeInfo(
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a><span data-ttu-id="3cadd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3cadd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cadd-107">*itinfo*</span><span class="sxs-lookup"><span data-stu-id="3cadd-107">*itinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="3cadd-108">Informations de type à retourner.</span><span class="sxs-lookup"><span data-stu-id="3cadd-108">Type information to return.</span></span> <span data-ttu-id="3cadd-109">Passe zéro pour récupérer les informations de type pour l’implémentation **IDispatch** .</span><span class="sxs-lookup"><span data-stu-id="3cadd-109">Pass zero to retrieve type information for the **IDispatch** implementation.</span></span>

</dd> <dt>

<span data-ttu-id="3cadd-110">*lcid*</span><span class="sxs-lookup"><span data-stu-id="3cadd-110">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="3cadd-111">ID de paramètres régionaux pour les informations de type.</span><span class="sxs-lookup"><span data-stu-id="3cadd-111">Locale ID for the type information.</span></span> <span data-ttu-id="3cadd-112">Pour les classes qui prennent en charge les noms de membres localisés, un objet peut être en mesure de retourner des informations de type différentes pour différentes langues.</span><span class="sxs-lookup"><span data-stu-id="3cadd-112">For classes that support localized member names, an object might be able to return different type information for different languages.</span></span> <span data-ttu-id="3cadd-113">Pour les classes qui ne prennent pas en charge les noms de membres localisés, ce paramètre peut être ignoré.</span><span class="sxs-lookup"><span data-stu-id="3cadd-113">For classes that do not support localized member names, this parameter can be ignored.</span></span>

</dd> <dt>

<span data-ttu-id="3cadd-114">*ppTInfo*</span><span class="sxs-lookup"><span data-stu-id="3cadd-114">*pptinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="3cadd-115">Adresse d’un pointeur vers l’objet d’informations de type demandé.</span><span class="sxs-lookup"><span data-stu-id="3cadd-115">Address of a pointer to the type-information object requested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cadd-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3cadd-116">Return value</span></span>

<span data-ttu-id="3cadd-117">Retourne un \_ pointeur E si *ppTInfo* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="3cadd-117">Returns an E\_POINTER if *pptinfo* is invalid.</span></span> <span data-ttu-id="3cadd-118">Retourne le TYPE \_ E \_ ELEMENTNOTFOUND si *iTInfo* n’est pas égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="3cadd-118">Returns TYPE\_E\_ELEMENTNOTFOUND if *itinfo* is not zero.</span></span> <span data-ttu-id="3cadd-119">Retourne S \_ OK si réussit.</span><span class="sxs-lookup"><span data-stu-id="3cadd-119">Returns S\_OK if is successful.</span></span> <span data-ttu-id="3cadd-120">Sinon, retourne un **HRESULT** de l’un des appels pour récupérer le type.</span><span class="sxs-lookup"><span data-stu-id="3cadd-120">Otherwise, returns an **HRESULT** from one of the calls to retrieve the type.</span></span>

## <a name="requirements"></a><span data-ttu-id="3cadd-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3cadd-121">Requirements</span></span>



| <span data-ttu-id="3cadd-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3cadd-122">Requirement</span></span> | <span data-ttu-id="3cadd-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="3cadd-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cadd-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="3cadd-124">Header</span></span><br/>  | <dl> <span data-ttu-id="3cadd-125"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3cadd-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3cadd-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3cadd-126">Library</span></span><br/> | <dl> <span data-ttu-id="3cadd-127"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="3cadd-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3cadd-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3cadd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cadd-129">**CMediaControl, classe**</span><span class="sxs-lookup"><span data-stu-id="3cadd-129">**CMediaControl Class**</span></span>](cmediacontrol.md)
</dt> </dl>

 

 




