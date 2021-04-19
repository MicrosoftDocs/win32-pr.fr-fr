---
description: La méthode FindPinNumber récupère le numéro d’un pin spécifié sur le filtre.
ms.assetid: c9366fcc-7b13-4e43-883e-6003c32fadec
title: Méthode CSource. FindPinNumber (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.FindPinNumber
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6a71c65efd97c48eed58fb7d0b5aa8fcc2f178e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523876"
---
# <a name="csourcefindpinnumber-method"></a><span data-ttu-id="d3b60-103">Méthode CSource. FindPinNumber</span><span class="sxs-lookup"><span data-stu-id="d3b60-103">CSource.FindPinNumber method</span></span>

<span data-ttu-id="d3b60-104">La `FindPinNumber` méthode récupère le numéro d’un pin spécifié sur le filtre.</span><span class="sxs-lookup"><span data-stu-id="d3b60-104">The `FindPinNumber` method retrieves the number of a specified pin on the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3b60-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d3b60-105">Syntax</span></span>


```C++
int FindPinNumber(
   IPin *iPin
);
```



## <a name="parameters"></a><span data-ttu-id="d3b60-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d3b60-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3b60-107">*iPin*</span><span class="sxs-lookup"><span data-stu-id="d3b60-107">*iPin*</span></span> 
</dt> <dd>

<span data-ttu-id="d3b60-108">Pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) du pin.</span><span class="sxs-lookup"><span data-stu-id="d3b60-108">Pointer to the pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3b60-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d3b60-109">Return value</span></span>

<span data-ttu-id="d3b60-110">Retourne le numéro de code confidentiel, ou 1 si le code PIN est introuvable sur ce filtre.</span><span class="sxs-lookup"><span data-stu-id="d3b60-110">Returns the pin number, or  1 if the pin is not found on this filter.</span></span> <span data-ttu-id="d3b60-111">Le premier code PIN est numéroté à zéro.</span><span class="sxs-lookup"><span data-stu-id="d3b60-111">The first pin is numbered zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3b60-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d3b60-112">Requirements</span></span>



| <span data-ttu-id="d3b60-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d3b60-113">Requirement</span></span> | <span data-ttu-id="d3b60-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="d3b60-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3b60-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="d3b60-115">Header</span></span><br/>  | <dl> <span data-ttu-id="d3b60-116"><dt>Source. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d3b60-116"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="d3b60-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d3b60-117">Library</span></span><br/> | <dl> <span data-ttu-id="d3b60-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d3b60-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3b60-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d3b60-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3b60-120">**CSource, classe**</span><span class="sxs-lookup"><span data-stu-id="d3b60-120">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 




