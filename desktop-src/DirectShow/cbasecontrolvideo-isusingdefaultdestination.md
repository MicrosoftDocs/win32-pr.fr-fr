---
description: La méthode IsUsingDefaultDestination détermine si le convertisseur utilise la fenêtre de destination par défaut.
ms.assetid: 0b956575-4cf0-4f1f-9223-bb1ec3ae8b10
title: Méthode CBaseControlVideo. IsUsingDefaultDestination (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.IsUsingDefaultDestination
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 88168442cf741e5997c2b66fc4b83bf8205e694f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542657"
---
# <a name="cbasecontrolvideoisusingdefaultdestination-method"></a><span data-ttu-id="346ff-103">Méthode CBaseControlVideo. IsUsingDefaultDestination</span><span class="sxs-lookup"><span data-stu-id="346ff-103">CBaseControlVideo.IsUsingDefaultDestination method</span></span>

<span data-ttu-id="346ff-104">La `IsUsingDefaultDestination` méthode détermine si le convertisseur utilise la fenêtre de destination par défaut.</span><span class="sxs-lookup"><span data-stu-id="346ff-104">The `IsUsingDefaultDestination` method determines if the renderer is using the default destination window.</span></span>

## <a name="syntax"></a><span data-ttu-id="346ff-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="346ff-105">Syntax</span></span>


```C++
virtual HRESULT IsUsingDefaultDestination() = 0;
```



## <a name="parameters"></a><span data-ttu-id="346ff-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="346ff-106">Parameters</span></span>

<span data-ttu-id="346ff-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="346ff-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="346ff-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="346ff-108">Return value</span></span>

<span data-ttu-id="346ff-109">Retourne S \_ OK si vous utilisez la destination par défaut ; sinon, retourne s \_ false.</span><span class="sxs-lookup"><span data-stu-id="346ff-109">Returns S\_OK if using the default destination; otherwise, returns S\_FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="346ff-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="346ff-110">Requirements</span></span>



| <span data-ttu-id="346ff-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="346ff-111">Requirement</span></span> | <span data-ttu-id="346ff-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="346ff-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="346ff-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="346ff-113">Header</span></span><br/>  | <dl> <span data-ttu-id="346ff-114"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="346ff-114"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="346ff-115">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="346ff-115">Library</span></span><br/> | <dl> <span data-ttu-id="346ff-116"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="346ff-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="346ff-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="346ff-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="346ff-118">**CBaseControlVideo, classe**</span><span class="sxs-lookup"><span data-stu-id="346ff-118">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




