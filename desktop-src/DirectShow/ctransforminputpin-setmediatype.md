---
description: 'Méthode CTransformInputPin. SetMediaType : la méthode SetMediaType définit le type de média pour la connexion.'
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
ms.openlocfilehash: 9af7310dbbf8830d7469c1a72ae43b946f1fbc69
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094997"
---
# <a name="ctransforminputpinsetmediatype-method"></a><span data-ttu-id="01d30-103">Méthode CTransformInputPin. SetMediaType</span><span class="sxs-lookup"><span data-stu-id="01d30-103">CTransformInputPin.SetMediaType method</span></span>

<span data-ttu-id="01d30-104">La `SetMediaType` méthode définit le type de média pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="01d30-104">The `SetMediaType` method sets the media type for the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="01d30-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="01d30-105">Syntax</span></span>


```C++
HRESULT SetMediaType(
   const CMediaType *mt
);
```



## <a name="parameters"></a><span data-ttu-id="01d30-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="01d30-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01d30-107">*MT*</span><span class="sxs-lookup"><span data-stu-id="01d30-107">*mt*</span></span> 
</dt> <dd>

<span data-ttu-id="01d30-108">Pointeur vers un objet [**CMediaType**](cmediatype.md) qui spécifie le type de média.</span><span class="sxs-lookup"><span data-stu-id="01d30-108">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01d30-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="01d30-109">Return value</span></span>

<span data-ttu-id="01d30-110">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="01d30-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="01d30-111">Notes </span><span class="sxs-lookup"><span data-stu-id="01d30-111">Remarks</span></span>

<span data-ttu-id="01d30-112">Cette méthode remplace la méthode [**CBasePin :: SetMediaType**](cbasepin-setmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="01d30-112">This method overrides the [**CBasePin::SetMediaType**](cbasepin-setmediatype.md) method.</span></span> <span data-ttu-id="01d30-113">Elle appelle la méthode [**CTransformFilter :: SetMediaType**](ctransformfilter-setmediatype.md) du filtre pour informer le filtre.</span><span class="sxs-lookup"><span data-stu-id="01d30-113">It calls the filter's [**CTransformFilter::SetMediaType**](ctransformfilter-setmediatype.md) method to inform the filter.</span></span>

<span data-ttu-id="01d30-114">Le code confidentiel doit vérifier que le type de média est acceptable avant d’appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="01d30-114">The pin must verify that the media type is acceptable before calling this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="01d30-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="01d30-115">Requirements</span></span>



| <span data-ttu-id="01d30-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="01d30-116">Requirement</span></span> | <span data-ttu-id="01d30-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="01d30-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01d30-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="01d30-118">Header</span></span><br/>  | <dl> <span data-ttu-id="01d30-119"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="01d30-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="01d30-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="01d30-120">Library</span></span><br/> | <dl> <span data-ttu-id="01d30-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="01d30-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




