---
description: 'La méthode SetProperties définit les propriétés de l’exemple. Cette méthode implémente la méthode IMediaSample2 :: SetProperties.'
ms.assetid: 639aedf5-0c21-4578-b336-91859e40f3be
title: CMediaSample. SetProperties, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c5e6ef3c3839825586bf47259cf44783d167f503
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532524"
---
# <a name="cmediasamplesetproperties-method"></a><span data-ttu-id="05447-104">CMediaSample. SetProperties, méthode</span><span class="sxs-lookup"><span data-stu-id="05447-104">CMediaSample.SetProperties method</span></span>

<span data-ttu-id="05447-105">La `SetProperties` méthode définit les propriétés de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="05447-105">The `SetProperties` method sets the properties of the sample.</span></span> <span data-ttu-id="05447-106">Cette méthode implémente la méthode [**IMediaSample2 :: SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-setproperties) .</span><span class="sxs-lookup"><span data-stu-id="05447-106">This method implements the [**IMediaSample2::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-setproperties) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="05447-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="05447-107">Syntax</span></span>


```C++
HRESULT SetProperties(
         DWORD cbProperties,
   const BYTE  *pbProperties
);
```



## <a name="parameters"></a><span data-ttu-id="05447-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="05447-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05447-109">*cbProperties*</span><span class="sxs-lookup"><span data-stu-id="05447-109">*cbProperties*</span></span> 
</dt> <dd>

<span data-ttu-id="05447-110">Longueur des données de propriété à définir, en octets.</span><span class="sxs-lookup"><span data-stu-id="05447-110">Length of property data to set, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="05447-111">*pbProperties*</span><span class="sxs-lookup"><span data-stu-id="05447-111">*pbProperties*</span></span> 
</dt> <dd>

<span data-ttu-id="05447-112">Pointeur vers une mémoire tampon de taille *cbProperties*.</span><span class="sxs-lookup"><span data-stu-id="05447-112">Pointer to a buffer of size *cbProperties*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05447-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="05447-113">Return value</span></span>

<span data-ttu-id="05447-114">Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="05447-114">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="05447-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="05447-115">Return code</span></span>                                                                                   | <span data-ttu-id="05447-116">Description</span><span class="sxs-lookup"><span data-stu-id="05447-116">Description</span></span>                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="05447-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="05447-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="05447-118">Succès</span><span class="sxs-lookup"><span data-stu-id="05447-118">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="05447-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="05447-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="05447-120">Argument non valide</span><span class="sxs-lookup"><span data-stu-id="05447-120">Invalid argument</span></span><br/>          |
| <dl> <span data-ttu-id="05447-121"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="05447-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="05447-122">Mémoire insuffisante</span><span class="sxs-lookup"><span data-stu-id="05447-122">Insufficient memory</span></span><br/>       |
| <dl> <span data-ttu-id="05447-123"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="05447-123"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="05447-124">Argument de pointeur **null**</span><span class="sxs-lookup"><span data-stu-id="05447-124">**NULL** pointer argument</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="05447-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="05447-125">Requirements</span></span>



| <span data-ttu-id="05447-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="05447-126">Requirement</span></span> | <span data-ttu-id="05447-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="05447-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05447-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="05447-128">Header</span></span><br/>  | <dl> <span data-ttu-id="05447-129"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="05447-129"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="05447-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="05447-130">Library</span></span><br/> | <dl> <span data-ttu-id="05447-131"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="05447-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05447-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="05447-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05447-133">**CMediaSample, classe**</span><span class="sxs-lookup"><span data-stu-id="05447-133">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




