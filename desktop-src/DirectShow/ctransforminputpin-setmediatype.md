---
description: La méthode SetMediaType définit le type de média pour la connexion.
ms.assetid: 8e83380f-ba38-4fb8-ac32-40d68a4efea6
title: Méthode CTransformInputPin. SetMediaType (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b42531a003fbad1a2a08864390a512296c440e64
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531131"
---
# <a name="ctransforminputpinsetmediatype-method"></a><span data-ttu-id="99350-103">Méthode CTransformInputPin. SetMediaType</span><span class="sxs-lookup"><span data-stu-id="99350-103">CTransformInputPin.SetMediaType method</span></span>

<span data-ttu-id="99350-104">La `SetMediaType` méthode définit le type de média pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="99350-104">The `SetMediaType` method sets the media type for the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="99350-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="99350-105">Syntax</span></span>


```C++
HRESULT SetMediaType(
   const CMediaType *mt
);
```



## <a name="parameters"></a><span data-ttu-id="99350-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="99350-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99350-107">*MT*</span><span class="sxs-lookup"><span data-stu-id="99350-107">*mt*</span></span> 
</dt> <dd>

<span data-ttu-id="99350-108">Pointeur vers un objet [**CMediaType**](cmediatype.md) qui spécifie le type de média.</span><span class="sxs-lookup"><span data-stu-id="99350-108">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99350-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="99350-109">Return value</span></span>

<span data-ttu-id="99350-110">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="99350-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="99350-111">Notes</span><span class="sxs-lookup"><span data-stu-id="99350-111">Remarks</span></span>

<span data-ttu-id="99350-112">Cette méthode remplace la méthode [**CBasePin :: SetMediaType**](cbasepin-setmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="99350-112">This method overrides the [**CBasePin::SetMediaType**](cbasepin-setmediatype.md) method.</span></span> <span data-ttu-id="99350-113">Elle appelle la méthode [**CTransformFilter :: SetMediaType**](ctransformfilter-setmediatype.md) du filtre pour informer le filtre.</span><span class="sxs-lookup"><span data-stu-id="99350-113">It calls the filter's [**CTransformFilter::SetMediaType**](ctransformfilter-setmediatype.md) method to inform the filter.</span></span>

<span data-ttu-id="99350-114">Le code confidentiel doit vérifier que le type de média est acceptable avant d’appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="99350-114">The pin must verify that the media type is acceptable before calling this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="99350-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="99350-115">Requirements</span></span>



| <span data-ttu-id="99350-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="99350-116">Requirement</span></span> | <span data-ttu-id="99350-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="99350-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99350-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="99350-118">Header</span></span><br/>  | <dl> <span data-ttu-id="99350-119"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="99350-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="99350-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="99350-120">Library</span></span><br/> | <dl> <span data-ttu-id="99350-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="99350-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




