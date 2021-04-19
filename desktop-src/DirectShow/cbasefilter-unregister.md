---
description: La méthode unregister Supprime le filtre du Registre.
ms.assetid: 2eb70e9f-1acf-433e-972f-24fb32eaeb13
title: CBaseFilter. Unregister, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Unregister
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8b46e74e4009f6767788fa120984eca0e89fb551
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530957"
---
# <a name="cbasefilterunregister-method"></a><span data-ttu-id="4d150-103">CBaseFilter. Unregister, méthode</span><span class="sxs-lookup"><span data-stu-id="4d150-103">CBaseFilter.Unregister method</span></span>

<span data-ttu-id="4d150-104">La `Unregister` méthode supprime le filtre du Registre.</span><span class="sxs-lookup"><span data-stu-id="4d150-104">The `Unregister` method removes the filter from the registry.</span></span>

> [!Note]  
> <span data-ttu-id="4d150-105">Cette méthode est obsolète.</span><span class="sxs-lookup"><span data-stu-id="4d150-105">This method is obsolete.</span></span> <span data-ttu-id="4d150-106">Les nouveaux filtres doivent être désinscrits à l’aide de la fonction [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) .</span><span class="sxs-lookup"><span data-stu-id="4d150-106">New filters should be unregistered using the [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) function.</span></span> <span data-ttu-id="4d150-107">Pour plus d’informations, consultez [comment inscrire des filtres DirectShow](how-to-register-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="4d150-107">For more information, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="4d150-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4d150-108">Syntax</span></span>


```C++
HRESULT Unregister();
```



## <a name="parameters"></a><span data-ttu-id="4d150-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4d150-109">Parameters</span></span>

<span data-ttu-id="4d150-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="4d150-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4d150-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4d150-111">Return value</span></span>

<span data-ttu-id="4d150-112">Retourne S \_ OK en cas de réussite, ou une valeur **HRESULT** indiquant la cause de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="4d150-112">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d150-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4d150-113">Requirements</span></span>



| <span data-ttu-id="4d150-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4d150-114">Requirement</span></span> | <span data-ttu-id="4d150-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="4d150-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d150-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="4d150-116">Header</span></span><br/>  | <dl> <span data-ttu-id="4d150-117"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4d150-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4d150-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4d150-118">Library</span></span><br/> | <dl> <span data-ttu-id="4d150-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4d150-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d150-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4d150-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d150-121">**CBaseFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="4d150-121">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




