---
description: 'La méthode IsFormatSupported détermine si un format d’heure spécifié est pris en charge. Cette méthode implémente la méthode IMediaSeeking :: IsFormatSupported.'
ms.assetid: dd8751d6-8439-4155-bdaf-b152a7c6cad4
title: Méthode CPosPassThru. IsFormatSupported (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.IsFormatSupported
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 85bdbef2315bd2c9e2bc92f639a7d328f1f17ce0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540685"
---
# <a name="cpospassthruisformatsupported-method"></a><span data-ttu-id="c3bfd-104">Méthode CPosPassThru. IsFormatSupported</span><span class="sxs-lookup"><span data-stu-id="c3bfd-104">CPosPassThru.IsFormatSupported method</span></span>

<span data-ttu-id="c3bfd-105">La `IsFormatSupported` méthode détermine si un format d’heure spécifié est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c3bfd-105">The `IsFormatSupported` method determines whether a specified time format is supported.</span></span> <span data-ttu-id="c3bfd-106">Cette méthode implémente la méthode [**IMediaSeeking :: IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) .</span><span class="sxs-lookup"><span data-stu-id="c3bfd-106">This method implements the [**IMediaSeeking::IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3bfd-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c3bfd-107">Syntax</span></span>


```C++
HRESULT IsFormatSupported(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="c3bfd-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c3bfd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3bfd-109">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="c3bfd-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="c3bfd-110">Pointeur vers un GUID de format d’heure.</span><span class="sxs-lookup"><span data-stu-id="c3bfd-110">Pointer to a time format GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3bfd-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c3bfd-111">Return value</span></span>

<span data-ttu-id="c3bfd-112">Retourne la valeur **HRESULT** de la broche connectée.</span><span class="sxs-lookup"><span data-stu-id="c3bfd-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3bfd-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c3bfd-113">Requirements</span></span>



| <span data-ttu-id="c3bfd-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c3bfd-114">Requirement</span></span> | <span data-ttu-id="c3bfd-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3bfd-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3bfd-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="c3bfd-116">Header</span></span><br/>  | <dl> <span data-ttu-id="c3bfd-117"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c3bfd-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c3bfd-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c3bfd-118">Library</span></span><br/> | <dl> <span data-ttu-id="c3bfd-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c3bfd-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3bfd-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c3bfd-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3bfd-121">**CPosPassThru, classe**</span><span class="sxs-lookup"><span data-stu-id="c3bfd-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> <dt>

[<span data-ttu-id="c3bfd-122">**GUID de format d’heure**</span><span class="sxs-lookup"><span data-stu-id="c3bfd-122">**Time Format GUIDs**</span></span>](time-format-guids.md)
</dt> </dl>

 

 




