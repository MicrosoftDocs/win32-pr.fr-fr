---
description: La méthode CheckMediaType détermine si un type de média proposé est compatible avec le format d’affichage.
ms.assetid: 567663cf-c79f-4549-9fa9-b16da957d2b1
title: Méthode CImageDisplay. CheckMediaType (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a8ebcdbe6bbfe6538a2ea166be0816f31954c7d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525157"
---
# <a name="cimagedisplaycheckmediatype-method"></a><span data-ttu-id="5c177-103">Méthode CImageDisplay. CheckMediaType</span><span class="sxs-lookup"><span data-stu-id="5c177-103">CImageDisplay.CheckMediaType method</span></span>

<span data-ttu-id="5c177-104">La `CheckMediaType` méthode détermine si un type de média proposé est compatible avec le format d’affichage.</span><span class="sxs-lookup"><span data-stu-id="5c177-104">The `CheckMediaType` method determines whether a proposed media type is compatible with the display format.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c177-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5c177-105">Syntax</span></span>


```C++
HRESULT CheckMediaType(
   const CMediaType *pmtIn
);
```



## <a name="parameters"></a><span data-ttu-id="5c177-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5c177-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c177-107">*pmtIn*</span><span class="sxs-lookup"><span data-stu-id="5c177-107">*pmtIn*</span></span> 
</dt> <dd>

<span data-ttu-id="5c177-108">Pointeur vers un objet [**CMediaType**](cmediatype.md) qui contient le type de média.</span><span class="sxs-lookup"><span data-stu-id="5c177-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c177-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5c177-109">Return value</span></span>

<span data-ttu-id="5c177-110">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5c177-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="5c177-111">Les valeurs possibles sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="5c177-111">Possible values include the following.</span></span>



| <span data-ttu-id="5c177-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="5c177-112">Return code</span></span>                                                                                  | <span data-ttu-id="5c177-113">Description</span><span class="sxs-lookup"><span data-stu-id="5c177-113">Description</span></span>                              |
|----------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="5c177-114"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="5c177-114"><dt>**E\_FAIL**</dt></span></span> </dl>       | <span data-ttu-id="5c177-115">Type de média non valide.</span><span class="sxs-lookup"><span data-stu-id="5c177-115">Invalid media type.</span></span><br/>           |
| <dl> <span data-ttu-id="5c177-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="5c177-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="5c177-117">Type de média non valide.</span><span class="sxs-lookup"><span data-stu-id="5c177-117">Invalid media type.</span></span><br/>           |
| <dl> <span data-ttu-id="5c177-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5c177-118"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="5c177-119">Le type de média est compatible.</span><span class="sxs-lookup"><span data-stu-id="5c177-119">The media type is compatible.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5c177-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5c177-120">Requirements</span></span>



| <span data-ttu-id="5c177-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5c177-121">Requirement</span></span> | <span data-ttu-id="5c177-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="5c177-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c177-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="5c177-123">Header</span></span><br/>  | <dl> <span data-ttu-id="5c177-124"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5c177-124"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5c177-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5c177-125">Library</span></span><br/> | <dl> <span data-ttu-id="5c177-126"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5c177-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c177-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5c177-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c177-128">**CImageDisplay, classe**</span><span class="sxs-lookup"><span data-stu-id="5c177-128">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




