---
description: La méthode CurrentMediaType récupère le type de média pour la connexion de code confidentiel actuelle.
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
ms.openlocfilehash: ee9ee15c3cda2baf8ab8d6e9cb0ec3c797e91a1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528929"
---
# <a name="ctransformoutputpincurrentmediatype-method"></a><span data-ttu-id="f2a7b-103">Méthode CTransformOutputPin. CurrentMediaType</span><span class="sxs-lookup"><span data-stu-id="f2a7b-103">CTransformOutputPin.CurrentMediaType method</span></span>

<span data-ttu-id="f2a7b-104">La `CurrentMediaType` méthode récupère le type de média pour la connexion de code confidentiel actuelle.</span><span class="sxs-lookup"><span data-stu-id="f2a7b-104">The `CurrentMediaType` method retrieves the media type for the current pin connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2a7b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f2a7b-105">Syntax</span></span>


```C++
CMediaType& CurrentMediaType();
```



## <a name="parameters"></a><span data-ttu-id="f2a7b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f2a7b-106">Parameters</span></span>

<span data-ttu-id="f2a7b-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="f2a7b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f2a7b-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f2a7b-108">Return value</span></span>

<span data-ttu-id="f2a7b-109">Retourne une référence à la variable de membre [**CBasePin :: m \_ MT**](cbasepin-m-mt.md) .</span><span class="sxs-lookup"><span data-stu-id="f2a7b-109">Returns a reference to the [**CBasePin::m\_mt**](cbasepin-m-mt.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2a7b-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f2a7b-110">Requirements</span></span>



| <span data-ttu-id="f2a7b-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f2a7b-111">Requirement</span></span> | <span data-ttu-id="f2a7b-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="f2a7b-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2a7b-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="f2a7b-113">Header</span></span><br/>  | <dl> <span data-ttu-id="f2a7b-114"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f2a7b-114"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f2a7b-115">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f2a7b-115">Library</span></span><br/> | <dl> <span data-ttu-id="f2a7b-116"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f2a7b-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




