---
description: La méthode CRendererInputPin est une méthode de constructeur.
ms.assetid: 272f864e-d6a8-4a9e-b72f-892147db9970
title: Constructeur CRendererInputPin. CRendererInputPin (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.CRendererInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f6888b234b87a48fc89f70c0db36122cbf7289ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526466"
---
# <a name="crendererinputpincrendererinputpin-constructor"></a><span data-ttu-id="d8c92-103">Constructeur CRendererInputPin. CRendererInputPin</span><span class="sxs-lookup"><span data-stu-id="d8c92-103">CRendererInputPin.CRendererInputPin constructor</span></span>

<span data-ttu-id="d8c92-104">La `CRendererInputPin` méthode est une méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="d8c92-104">The `CRendererInputPin` method is a constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8c92-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d8c92-105">Syntax</span></span>


```C++
CRendererInputPin(
   CBaseRenderer *pRenderer,
   HRESULT       *phr,
   LPCWSTR       Name
);
```



## <a name="parameters"></a><span data-ttu-id="d8c92-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d8c92-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8c92-107">*pRenderer*</span><span class="sxs-lookup"><span data-stu-id="d8c92-107">*pRenderer*</span></span> 
</dt> <dd>

<span data-ttu-id="d8c92-108">Pointeur vers l’objet [**CBaseRenderer**](cbaserenderer.md) qui implémente le filtre.</span><span class="sxs-lookup"><span data-stu-id="d8c92-108">Pointer to the [**CBaseRenderer**](cbaserenderer.md) object that implements the filter.</span></span>

</dd> <dt>

<span data-ttu-id="d8c92-109">*phr*</span><span class="sxs-lookup"><span data-stu-id="d8c92-109">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="d8c92-110">Pointeur vers une variable qui reçoit une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d8c92-110">Pointer to a variable that receives an **HRESULT** value.</span></span>

</dd> <dt>

<span data-ttu-id="d8c92-111">*Nom*</span><span class="sxs-lookup"><span data-stu-id="d8c92-111">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="d8c92-112">Pointeur vers une chaîne de caractères larges contenant l’identificateur de code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="d8c92-112">Pointer to a wide-character string containing the pin identifier.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d8c92-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d8c92-113">Requirements</span></span>



| <span data-ttu-id="d8c92-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d8c92-114">Requirement</span></span> | <span data-ttu-id="d8c92-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="d8c92-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8c92-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="d8c92-116">Header</span></span><br/>  | <dl> <span data-ttu-id="d8c92-117"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d8c92-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d8c92-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d8c92-118">Library</span></span><br/> | <dl> <span data-ttu-id="d8c92-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d8c92-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8c92-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8c92-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8c92-121">**CRendererInputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="d8c92-121">**CRendererInputPin Class**</span></span>](crendererinputpin.md)
</dt> </dl>

 

 




