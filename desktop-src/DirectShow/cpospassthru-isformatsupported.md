---
description: 'Méthode CPosPassThru. IsFormatSupported : la méthode IsFormatSupported détermine si un format d’heure spécifié est pris en charge. Cette méthode implémente la méthode IMediaSeeking :: IsFormatSupported.'
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
ms.openlocfilehash: 6bd4b90bbe86e7ba05aa48fb7888c946babd8ed9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095247"
---
# <a name="cpospassthruisformatsupported-method"></a><span data-ttu-id="6ffe9-104">Méthode CPosPassThru. IsFormatSupported</span><span class="sxs-lookup"><span data-stu-id="6ffe9-104">CPosPassThru.IsFormatSupported method</span></span>

<span data-ttu-id="6ffe9-105">La `IsFormatSupported` méthode détermine si un format d’heure spécifié est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="6ffe9-105">The `IsFormatSupported` method determines whether a specified time format is supported.</span></span> <span data-ttu-id="6ffe9-106">Cette méthode implémente la méthode [**IMediaSeeking :: IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) .</span><span class="sxs-lookup"><span data-stu-id="6ffe9-106">This method implements the [**IMediaSeeking::IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ffe9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6ffe9-107">Syntax</span></span>


```C++
HRESULT IsFormatSupported(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="6ffe9-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6ffe9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ffe9-109">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="6ffe9-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="6ffe9-110">Pointeur vers un GUID de format d’heure.</span><span class="sxs-lookup"><span data-stu-id="6ffe9-110">Pointer to a time format GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ffe9-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6ffe9-111">Return value</span></span>

<span data-ttu-id="6ffe9-112">Retourne la valeur **HRESULT** de la broche connectée.</span><span class="sxs-lookup"><span data-stu-id="6ffe9-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ffe9-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6ffe9-113">Requirements</span></span>



| <span data-ttu-id="6ffe9-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6ffe9-114">Requirement</span></span> | <span data-ttu-id="6ffe9-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="6ffe9-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ffe9-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="6ffe9-116">Header</span></span><br/>  | <dl> <span data-ttu-id="6ffe9-117"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6ffe9-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6ffe9-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6ffe9-118">Library</span></span><br/> | <dl> <span data-ttu-id="6ffe9-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="6ffe9-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ffe9-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6ffe9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ffe9-121">**CPosPassThru, classe**</span><span class="sxs-lookup"><span data-stu-id="6ffe9-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> <dt>

[<span data-ttu-id="6ffe9-122">**GUID de format d’heure**</span><span class="sxs-lookup"><span data-stu-id="6ffe9-122">**Time Format GUIDs**</span></span>](time-format-guids.md)
</dt> </dl>

 

 




