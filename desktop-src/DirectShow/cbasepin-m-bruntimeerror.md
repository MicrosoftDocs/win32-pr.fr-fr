---
description: Indicateur qui signale si une erreur d’exécution s’est produite.
ms.assetid: 917bcb21-a11e-4ac5-af96-565f61c155cd
title: 'Membre CBasePin :: m_bRunTimeError (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bRunTimeError
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5e8b0c5548d3089a6e619f88db5e4eed19b12be8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537882"
---
# <a name="cbasepinm_bruntimeerror-member"></a><span data-ttu-id="10cf3-103">CBasePin :: m \_ bRunTimeError, membre</span><span class="sxs-lookup"><span data-stu-id="10cf3-103">CBasePin::m\_bRunTimeError member</span></span>

<span data-ttu-id="10cf3-104">Indicateur qui signale si une erreur d’exécution s’est produite.</span><span class="sxs-lookup"><span data-stu-id="10cf3-104">Flag that indicates whether a run-time error has occurred.</span></span>

## <a name="syntax"></a><span data-ttu-id="10cf3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="10cf3-105">Syntax</span></span>


```C++
bool m_bRunTimeError;
```



## <a name="remarks"></a><span data-ttu-id="10cf3-106">Notes</span><span class="sxs-lookup"><span data-stu-id="10cf3-106">Remarks</span></span>

<span data-ttu-id="10cf3-107">Par défaut, cet indicateur est défini sur **false**.</span><span class="sxs-lookup"><span data-stu-id="10cf3-107">This flag defaults to **FALSE**.</span></span> <span data-ttu-id="10cf3-108">Affectez la **valeur true** à l’indicateur si une erreur d’exécution se produit pendant la diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="10cf3-108">Set the flag to **TRUE** if a run-time error occurs during streaming.</span></span> <span data-ttu-id="10cf3-109">La méthode [**CBasePin :: inactive**](cbasepin-inactive.md) réinitialise l’indicateur à **false**.</span><span class="sxs-lookup"><span data-stu-id="10cf3-109">The [**CBasePin::Inactive**](cbasepin-inactive.md) method resets the flag to **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="10cf3-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="10cf3-110">Requirements</span></span>



| <span data-ttu-id="10cf3-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="10cf3-111">Requirement</span></span> | <span data-ttu-id="10cf3-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="10cf3-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10cf3-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="10cf3-113">Header</span></span><br/>  | <dl> <span data-ttu-id="10cf3-114"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="10cf3-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="10cf3-115">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="10cf3-115">Library</span></span><br/> | <dl> <span data-ttu-id="10cf3-116"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="10cf3-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10cf3-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="10cf3-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10cf3-118">**CBasePin, classe**</span><span class="sxs-lookup"><span data-stu-id="10cf3-118">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




