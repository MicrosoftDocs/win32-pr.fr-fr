---
description: Indicateur qui spécifie si le code PIN tente ses propres types de média préférés avant ceux du code confidentiel de réception.
ms.assetid: 50462ee4-4a61-472f-9a7e-9cdb39be4dea
title: 'Membre CBasePin :: m_bTryMyTypesFirst (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bTryMyTypesFirst
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 72f98021b6ba97d32974f26ac4e76ca31fa54e5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543887"
---
# <a name="cbasepinm_btrymytypesfirst-member"></a><span data-ttu-id="81e87-103">CBasePin :: m \_ bTryMyTypesFirst, membre</span><span class="sxs-lookup"><span data-stu-id="81e87-103">CBasePin::m\_bTryMyTypesFirst member</span></span>

<span data-ttu-id="81e87-104">Indicateur qui spécifie si le code PIN tente ses propres types de média préférés avant ceux du code confidentiel de réception.</span><span class="sxs-lookup"><span data-stu-id="81e87-104">Flag that indicates whether the pin tries its own preferred media types before those of the receiving pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="81e87-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="81e87-105">Syntax</span></span>


```C++
bool m_bTryMyTypesFirst;
```



## <a name="remarks"></a><span data-ttu-id="81e87-106">Notes</span><span class="sxs-lookup"><span data-stu-id="81e87-106">Remarks</span></span>

<span data-ttu-id="81e87-107">Par défaut, cet indicateur est défini sur **false**.</span><span class="sxs-lookup"><span data-stu-id="81e87-107">This flag defaults to **FALSE**.</span></span> <span data-ttu-id="81e87-108">Si l’indicateur a la **valeur true**, la méthode [**CBasePin :: AgreeMediaType**](cbasepin-agreemediatype.md) inverse l’ordre dans lequel elle essaie les types de média.</span><span class="sxs-lookup"><span data-stu-id="81e87-108">If the flag is **TRUE**, the [**CBasePin::AgreeMediaType**](cbasepin-agreemediatype.md) method reverses the order in which it tries media types.</span></span>

## <a name="requirements"></a><span data-ttu-id="81e87-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="81e87-109">Requirements</span></span>



| <span data-ttu-id="81e87-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="81e87-110">Requirement</span></span> | <span data-ttu-id="81e87-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="81e87-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81e87-112">En-tête</span><span class="sxs-lookup"><span data-stu-id="81e87-112">Header</span></span><br/>  | <dl> <span data-ttu-id="81e87-113"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="81e87-113"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="81e87-114">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="81e87-114">Library</span></span><br/> | <dl> <span data-ttu-id="81e87-115"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="81e87-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81e87-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81e87-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81e87-117">**CBasePin, classe**</span><span class="sxs-lookup"><span data-stu-id="81e87-117">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




