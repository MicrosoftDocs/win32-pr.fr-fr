---
description: La méthode GetOwner récupère un pointeur vers l’interface IUnknown du composant propriétaire. Pour un composant agrégé, le propriétaire est le composant externe. Dans le cas contraire, le composant se trouve lui-même.
ms.assetid: 7d8af9d1-52c0-4f2b-9d05-6ddff85ab508
title: Méthode CUnknown. GetOwner (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.GetOwner
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e3cb1cd1d5b183857b6d75db79ee0fcdc6cb2d30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540013"
---
# <a name="cunknowngetowner-method"></a><span data-ttu-id="de5f8-105">Méthode CUnknown. GetOwner</span><span class="sxs-lookup"><span data-stu-id="de5f8-105">CUnknown.GetOwner method</span></span>

<span data-ttu-id="de5f8-106">La `GetOwner` méthode récupère un pointeur vers l’interface **IUnknown** du composant propriétaire.</span><span class="sxs-lookup"><span data-stu-id="de5f8-106">The `GetOwner` method retrieves a pointer to the **IUnknown** interface of the owning component.</span></span> <span data-ttu-id="de5f8-107">Pour un composant agrégé, le propriétaire est le composant externe.</span><span class="sxs-lookup"><span data-stu-id="de5f8-107">For an aggregated component, the owner is the outer component.</span></span> <span data-ttu-id="de5f8-108">Dans le cas contraire, le composant se trouve lui-même.</span><span class="sxs-lookup"><span data-stu-id="de5f8-108">Otherwise, the component owns itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="de5f8-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="de5f8-109">Syntax</span></span>


```C++
LPUNKNOWN GetOwner();
```



## <a name="parameters"></a><span data-ttu-id="de5f8-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="de5f8-110">Parameters</span></span>

<span data-ttu-id="de5f8-111">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="de5f8-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="de5f8-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="de5f8-112">Return value</span></span>

<span data-ttu-id="de5f8-113">Retourne un pointeur vers l’interface de contrôle **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="de5f8-113">Returns a pointer to the controlling **IUnknown** interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="de5f8-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="de5f8-114">Requirements</span></span>



| <span data-ttu-id="de5f8-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="de5f8-115">Requirement</span></span> | <span data-ttu-id="de5f8-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="de5f8-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de5f8-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="de5f8-117">Header</span></span><br/>  | <dl> <span data-ttu-id="de5f8-118"><dt>ComBase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="de5f8-118"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="de5f8-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="de5f8-119">Library</span></span><br/> | <dl> <span data-ttu-id="de5f8-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="de5f8-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




