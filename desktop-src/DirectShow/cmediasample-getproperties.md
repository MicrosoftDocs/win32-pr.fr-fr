---
description: 'La méthode GetProperties récupère les propriétés de l’exemple. Cette méthode implémente la méthode IMediaSample2 :: GetProperties.'
ms.assetid: c2a6d611-9c17-41fb-bb6d-f5b17f1c9966
title: CMediaSample. GetProperties, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 06ee1022f298e2f5167d348777b33fc2f1703eef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539520"
---
# <a name="cmediasamplegetproperties-method"></a><span data-ttu-id="64596-104">CMediaSample. GetProperties, méthode</span><span class="sxs-lookup"><span data-stu-id="64596-104">CMediaSample.GetProperties method</span></span>

<span data-ttu-id="64596-105">La `GetProperties` méthode récupère les propriétés de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="64596-105">The `GetProperties` method retrieves the properties of the sample.</span></span> <span data-ttu-id="64596-106">Cette méthode implémente la méthode [**IMediaSample2 :: GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) .</span><span class="sxs-lookup"><span data-stu-id="64596-106">This method implements the [**IMediaSample2::GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="64596-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="64596-107">Syntax</span></span>


```C++
HRESULT GetProperties(
   DWORD cbProperties,
   BYTE  *pbProperties
);
```



## <a name="parameters"></a><span data-ttu-id="64596-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="64596-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64596-109">*cbProperties*</span><span class="sxs-lookup"><span data-stu-id="64596-109">*cbProperties*</span></span> 
</dt> <dd>

<span data-ttu-id="64596-110">Longueur des données de propriété à récupérer, en octets.</span><span class="sxs-lookup"><span data-stu-id="64596-110">Length of property data to retrieve, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="64596-111">*pbProperties*</span><span class="sxs-lookup"><span data-stu-id="64596-111">*pbProperties*</span></span> 
</dt> <dd>

<span data-ttu-id="64596-112">Pointeur vers une mémoire tampon de taille *cbProperties*.</span><span class="sxs-lookup"><span data-stu-id="64596-112">Pointer to a buffer of size *cbProperties*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64596-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="64596-113">Return value</span></span>

<span data-ttu-id="64596-114">Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="64596-114">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="64596-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="64596-115">Return code</span></span>                                                                               | <span data-ttu-id="64596-116">Description</span><span class="sxs-lookup"><span data-stu-id="64596-116">Description</span></span>                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="64596-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="64596-117"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="64596-118">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="64596-118">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="64596-119"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="64596-119"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="64596-120">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="64596-120">**NULL** pointer argument.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="64596-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="64596-121">Requirements</span></span>



| <span data-ttu-id="64596-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="64596-122">Requirement</span></span> | <span data-ttu-id="64596-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="64596-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64596-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="64596-124">Header</span></span><br/>  | <dl> <span data-ttu-id="64596-125"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="64596-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="64596-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="64596-126">Library</span></span><br/> | <dl> <span data-ttu-id="64596-127"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="64596-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64596-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64596-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64596-129">**CMediaSample, classe**</span><span class="sxs-lookup"><span data-stu-id="64596-129">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




