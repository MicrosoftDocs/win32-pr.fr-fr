---
description: La méthode Register ajoute le filtre au registre.
ms.assetid: 934e421a-25a6-40fa-a48b-6d7331f34b78
title: CBaseFilter. Register, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Register
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1bd7ba5a57d670ef28ffda022c95c7dc5b12df77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540633"
---
# <a name="cbasefilterregister-method"></a><span data-ttu-id="2a462-103">CBaseFilter. Register, méthode</span><span class="sxs-lookup"><span data-stu-id="2a462-103">CBaseFilter.Register method</span></span>

<span data-ttu-id="2a462-104">La `Register` méthode ajoute le filtre au registre.</span><span class="sxs-lookup"><span data-stu-id="2a462-104">The `Register` method adds the filter to the registry.</span></span>

> [!Note]  
> <span data-ttu-id="2a462-105">Cette méthode est obsolète.</span><span class="sxs-lookup"><span data-stu-id="2a462-105">This method is obsolete.</span></span> <span data-ttu-id="2a462-106">Les nouveaux filtres doivent être inscrits à l’aide de la fonction [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) .</span><span class="sxs-lookup"><span data-stu-id="2a462-106">New filters should be registered using the [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) function.</span></span> <span data-ttu-id="2a462-107">Pour plus d’informations, consultez [comment inscrire des filtres DirectShow](how-to-register-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="2a462-107">For more information, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="2a462-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2a462-108">Syntax</span></span>


```C++
HRESULT Register();
```



## <a name="parameters"></a><span data-ttu-id="2a462-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2a462-109">Parameters</span></span>

<span data-ttu-id="2a462-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="2a462-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2a462-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2a462-111">Return value</span></span>

<span data-ttu-id="2a462-112">Retourne l’une des valeurs **HRESULT** listées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="2a462-112">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="2a462-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="2a462-113">Return code</span></span>                                                                             | <span data-ttu-id="2a462-114">Description</span><span class="sxs-lookup"><span data-stu-id="2a462-114">Description</span></span>                                          |
|-----------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="2a462-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2a462-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="2a462-116">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="2a462-116">Success.</span></span><br/>                                  |
| <dl> <span data-ttu-id="2a462-117"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="2a462-117"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="2a462-118">Aucune information d’inscription n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="2a462-118">No registration information is available.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2a462-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2a462-119">Requirements</span></span>



| <span data-ttu-id="2a462-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2a462-120">Requirement</span></span> | <span data-ttu-id="2a462-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a462-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a462-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="2a462-122">Header</span></span><br/>  | <dl> <span data-ttu-id="2a462-123"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2a462-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="2a462-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2a462-124">Library</span></span><br/> | <dl> <span data-ttu-id="2a462-125"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="2a462-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a462-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2a462-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a462-127">**CBaseFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="2a462-127">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




