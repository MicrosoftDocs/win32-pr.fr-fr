---
description: La méthode IsValid détermine si un type principal a été assigné à cet objet.
ms.assetid: 22d28019-f360-4b93-972c-d1dfe83938f0
title: CMediaType. IsValid, méthode (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.IsValid
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7d8e1731060021b61eb5037e1baeeda95021e8f5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534802"
---
# <a name="cmediatypeisvalid-method"></a><span data-ttu-id="02192-103">CMediaType. IsValid, méthode</span><span class="sxs-lookup"><span data-stu-id="02192-103">CMediaType.IsValid method</span></span>

<span data-ttu-id="02192-104">La `IsValid` méthode détermine si un type principal a été assigné à cet objet.</span><span class="sxs-lookup"><span data-stu-id="02192-104">The `IsValid` method determines whether a major type has been assigned to this object.</span></span>

## <a name="syntax"></a><span data-ttu-id="02192-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="02192-105">Syntax</span></span>


```C++
BOOL IsValid() const;
```



## <a name="parameters"></a><span data-ttu-id="02192-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="02192-106">Parameters</span></span>

<span data-ttu-id="02192-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="02192-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="02192-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="02192-108">Return value</span></span>

<span data-ttu-id="02192-109">Retourne la **valeur true** si un type principal a été assigné à cet objet.</span><span class="sxs-lookup"><span data-stu-id="02192-109">Returns **TRUE** if a major type has been assigned to this object.</span></span> <span data-ttu-id="02192-110">Sinon, retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="02192-110">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="02192-111">Notes</span><span class="sxs-lookup"><span data-stu-id="02192-111">Remarks</span></span>

<span data-ttu-id="02192-112">Par défaut, les objets [**CMediaType**](cmediatype.md) sont initialisés avec un type majeur de GUID \_ null.</span><span class="sxs-lookup"><span data-stu-id="02192-112">By default, [**CMediaType**](cmediatype.md) objects are initialized with a major type of GUID\_NULL.</span></span> <span data-ttu-id="02192-113">Appelez cette méthode pour déterminer si l’objet a été correctement initialisé.</span><span class="sxs-lookup"><span data-stu-id="02192-113">Call this method to determine whether the object has been correctly initialized.</span></span>

## <a name="requirements"></a><span data-ttu-id="02192-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="02192-114">Requirements</span></span>



| <span data-ttu-id="02192-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="02192-115">Requirement</span></span> | <span data-ttu-id="02192-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="02192-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02192-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="02192-117">Header</span></span><br/>  | <dl> <span data-ttu-id="02192-118"><dt>Mtype. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="02192-118"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="02192-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="02192-119">Library</span></span><br/> | <dl> <span data-ttu-id="02192-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="02192-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02192-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="02192-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02192-122">**CMediaType, classe**</span><span class="sxs-lookup"><span data-stu-id="02192-122">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




