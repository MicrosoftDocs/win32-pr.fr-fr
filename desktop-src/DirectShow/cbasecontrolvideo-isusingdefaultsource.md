---
description: La méthode IsUsingDefaultSource détermine si le convertisseur utilise la fenêtre source par défaut.
ms.assetid: f68d47e7-6602-4321-8e9e-373d354077a1
title: Méthode CBaseControlVideo. IsUsingDefaultSource (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.IsUsingDefaultSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94768cb098183654b7a0fa9464221989b407d880
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545689"
---
# <a name="cbasecontrolvideoisusingdefaultsource-method"></a><span data-ttu-id="ef589-103">Méthode CBaseControlVideo. IsUsingDefaultSource</span><span class="sxs-lookup"><span data-stu-id="ef589-103">CBaseControlVideo.IsUsingDefaultSource method</span></span>

<span data-ttu-id="ef589-104">La `IsUsingDefaultSource` méthode détermine si le convertisseur utilise la fenêtre source par défaut.</span><span class="sxs-lookup"><span data-stu-id="ef589-104">The `IsUsingDefaultSource` method determines if the renderer is using the default source window.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef589-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ef589-105">Syntax</span></span>


```C++
virtual HRESULT IsUsingDefaultSource() = 0;
```



## <a name="parameters"></a><span data-ttu-id="ef589-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ef589-106">Parameters</span></span>

<span data-ttu-id="ef589-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="ef589-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ef589-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ef589-108">Return value</span></span>

<span data-ttu-id="ef589-109">Retourne S \_ OK si le convertisseur utilise la source par défaut ; sinon, retourne s \_ false.</span><span class="sxs-lookup"><span data-stu-id="ef589-109">Returns S\_OK if the renderer is using the default source; otherwise, returns S\_FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef589-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ef589-110">Requirements</span></span>



| <span data-ttu-id="ef589-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ef589-111">Requirement</span></span> | <span data-ttu-id="ef589-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef589-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef589-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="ef589-113">Header</span></span><br/>  | <dl> <span data-ttu-id="ef589-114"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ef589-114"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ef589-115">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ef589-115">Library</span></span><br/> | <dl> <span data-ttu-id="ef589-116"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ef589-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef589-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef589-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef589-118">**CBaseControlVideo, classe**</span><span class="sxs-lookup"><span data-stu-id="ef589-118">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




