---
description: 'La méthode NonDelegatingAddRef incrémente le décompte de références sur l’objet. Cette méthode implémente la méthode INonDelegatingUnknown :: NonDelegatingAddRef.'
ms.assetid: abb6ee51-8fb8-4307-b127-b3667260e35a
title: Méthode CUnknown. NonDelegatingAddRef (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.NonDelegatingAddRef
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2f97260c03f0931e94e8ce6de8b7816789b2fe66
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543291"
---
# <a name="cunknownnondelegatingaddref-method"></a><span data-ttu-id="eb2d7-104">Méthode CUnknown. NonDelegatingAddRef</span><span class="sxs-lookup"><span data-stu-id="eb2d7-104">CUnknown.NonDelegatingAddRef method</span></span>

<span data-ttu-id="eb2d7-105">La `NonDelegatingAddRef` méthode incrémente le décompte de références sur l’objet.</span><span class="sxs-lookup"><span data-stu-id="eb2d7-105">The `NonDelegatingAddRef` method increments the reference count on the object.</span></span> <span data-ttu-id="eb2d7-106">Cette méthode implémente la méthode **INonDelegatingUnknown :: NonDelegatingAddRef** .</span><span class="sxs-lookup"><span data-stu-id="eb2d7-106">This method implements the **INonDelegatingUnknown::NonDelegatingAddRef** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb2d7-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eb2d7-107">Syntax</span></span>


```C++
ULONG NonDelegatingAddRef();
```



## <a name="parameters"></a><span data-ttu-id="eb2d7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eb2d7-108">Parameters</span></span>

<span data-ttu-id="eb2d7-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="eb2d7-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="eb2d7-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="eb2d7-110">Return value</span></span>

<span data-ttu-id="eb2d7-111">Retourne le nombre de références.</span><span class="sxs-lookup"><span data-stu-id="eb2d7-111">Returns the reference count.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb2d7-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eb2d7-112">Requirements</span></span>



| <span data-ttu-id="eb2d7-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eb2d7-113">Requirement</span></span> | <span data-ttu-id="eb2d7-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="eb2d7-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb2d7-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="eb2d7-115">Header</span></span><br/>  | <dl> <span data-ttu-id="eb2d7-116"><dt>ComBase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eb2d7-116"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="eb2d7-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="eb2d7-117">Library</span></span><br/> | <dl> <span data-ttu-id="eb2d7-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="eb2d7-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




