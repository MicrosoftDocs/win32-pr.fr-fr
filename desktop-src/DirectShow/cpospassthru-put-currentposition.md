---
description: La \_ méthode put CurrentPosition définit la position actuelle, par rapport à la durée totale du flux. Cette méthode implémente la méthode IMediaPosition ::p ut \_ CurrentPosition.
ms.assetid: 22d7e9e4-47da-45b5-9be0-3c5128f90353
title: Méthode CPosPassThru.put_CurrentPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_CurrentPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 85426636a34d0e197b36496d5a38a847c61b9501
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526467"
---
# <a name="cpospassthruput_currentposition-method"></a><span data-ttu-id="1fdc2-104">CPosPassThru. put \_ CurrentPosition, méthode</span><span class="sxs-lookup"><span data-stu-id="1fdc2-104">CPosPassThru.put\_CurrentPosition method</span></span>

<span data-ttu-id="1fdc2-105">La `put_CurrentPosition` méthode définit la position actuelle, par rapport à la durée totale du flux.</span><span class="sxs-lookup"><span data-stu-id="1fdc2-105">The `put_CurrentPosition` method sets the current position, relative to the total duration of the stream.</span></span> <span data-ttu-id="1fdc2-106">Cette méthode implémente la méthode [**IMediaPosition ::p ut \_ CurrentPosition**](/windows/desktop/api/Control/nf-control-imediaposition-put_currentposition) .</span><span class="sxs-lookup"><span data-stu-id="1fdc2-106">This method implements the [**IMediaPosition::put\_CurrentPosition**](/windows/desktop/api/Control/nf-control-imediaposition-put_currentposition) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fdc2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1fdc2-107">Syntax</span></span>


```C++
HRESULT put_CurrentPosition(
   REFTIME llTime
);
```



## <a name="parameters"></a><span data-ttu-id="1fdc2-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1fdc2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fdc2-109">*llTime*</span><span class="sxs-lookup"><span data-stu-id="1fdc2-109">*llTime*</span></span> 
</dt> <dd>

<span data-ttu-id="1fdc2-110">Nouvelle position, en secondes.</span><span class="sxs-lookup"><span data-stu-id="1fdc2-110">New position, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fdc2-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1fdc2-111">Return value</span></span>

<span data-ttu-id="1fdc2-112">Retourne la valeur **HRESULT** de la broche connectée.</span><span class="sxs-lookup"><span data-stu-id="1fdc2-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fdc2-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1fdc2-113">Requirements</span></span>



| <span data-ttu-id="1fdc2-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1fdc2-114">Requirement</span></span> | <span data-ttu-id="1fdc2-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="1fdc2-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fdc2-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="1fdc2-116">Header</span></span><br/>  | <dl> <span data-ttu-id="1fdc2-117"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1fdc2-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1fdc2-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1fdc2-118">Library</span></span><br/> | <dl> <span data-ttu-id="1fdc2-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1fdc2-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fdc2-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1fdc2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fdc2-121">**CPosPassThru, classe**</span><span class="sxs-lookup"><span data-stu-id="1fdc2-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




