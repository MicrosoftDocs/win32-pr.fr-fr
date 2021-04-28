---
description: 'Méthode CTransformOutputPin. CurrentMediaType : la méthode CurrentMediaType récupère le type de média pour la connexion de code confidentiel actuelle.'
ms.assetid: 1c42664d-160a-4f76-9d7a-40414c5c1704
title: Méthode CTransformOutputPin. CurrentMediaType (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CurrentMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0cb40310afb1c22d00a5394c0a0667fc8d22eb03
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094907"
---
# <a name="ctransformoutputpincurrentmediatype-method"></a><span data-ttu-id="dcecb-103">Méthode CTransformOutputPin. CurrentMediaType</span><span class="sxs-lookup"><span data-stu-id="dcecb-103">CTransformOutputPin.CurrentMediaType method</span></span>

<span data-ttu-id="dcecb-104">La `CurrentMediaType` méthode récupère le type de média pour la connexion de code confidentiel actuelle.</span><span class="sxs-lookup"><span data-stu-id="dcecb-104">The `CurrentMediaType` method retrieves the media type for the current pin connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcecb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dcecb-105">Syntax</span></span>


```C++
CMediaType& CurrentMediaType();
```



## <a name="parameters"></a><span data-ttu-id="dcecb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dcecb-106">Parameters</span></span>

<span data-ttu-id="dcecb-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="dcecb-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dcecb-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="dcecb-108">Return value</span></span>

<span data-ttu-id="dcecb-109">Retourne une référence à la variable de membre [**CBasePin :: m \_ MT**](cbasepin-m-mt.md) .</span><span class="sxs-lookup"><span data-stu-id="dcecb-109">Returns a reference to the [**CBasePin::m\_mt**](cbasepin-m-mt.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcecb-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dcecb-110">Requirements</span></span>



| <span data-ttu-id="dcecb-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dcecb-111">Requirement</span></span> | <span data-ttu-id="dcecb-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="dcecb-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcecb-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="dcecb-113">Header</span></span><br/>  | <dl> <span data-ttu-id="dcecb-114"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dcecb-114"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="dcecb-115">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="dcecb-115">Library</span></span><br/> | <dl> <span data-ttu-id="dcecb-116"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="dcecb-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




