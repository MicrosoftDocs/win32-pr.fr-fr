---
description: 'Décrémente le décompte de références sur l’objet. Cette méthode implémente la méthode INonDelegatingUnknown :: NonDelegatingRelease.'
ms.assetid: 58610f7d-5524-450f-a0f8-b299944abc78
title: Méthode CUnknown. NonDelegatingRelease (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.NonDelegatingRelease
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ec709d4b636eea6a145f9a24a868ad5c495e4477
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533179"
---
# <a name="cunknownnondelegatingrelease-method"></a><span data-ttu-id="547f6-104">Méthode CUnknown. NonDelegatingRelease</span><span class="sxs-lookup"><span data-stu-id="547f6-104">CUnknown.NonDelegatingRelease method</span></span>

<span data-ttu-id="547f6-105">Décrémente le décompte de références sur l’objet.</span><span class="sxs-lookup"><span data-stu-id="547f6-105">Decrements the reference count on the object.</span></span> <span data-ttu-id="547f6-106">Cette méthode implémente la méthode **INonDelegatingUnknown :: NonDelegatingRelease** .</span><span class="sxs-lookup"><span data-stu-id="547f6-106">This method implements the **INonDelegatingUnknown::NonDelegatingRelease** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="547f6-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="547f6-107">Syntax</span></span>


```C++
ULONG NonDelegatingRelease();
```



## <a name="parameters"></a><span data-ttu-id="547f6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="547f6-108">Parameters</span></span>

<span data-ttu-id="547f6-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="547f6-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="547f6-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="547f6-110">Return value</span></span>

<span data-ttu-id="547f6-111">Retourne le nombre de références.</span><span class="sxs-lookup"><span data-stu-id="547f6-111">Returns the reference count.</span></span>

## <a name="remarks"></a><span data-ttu-id="547f6-112">Notes</span><span class="sxs-lookup"><span data-stu-id="547f6-112">Remarks</span></span>

<span data-ttu-id="547f6-113">Lorsque le nombre de références atteint zéro, l’objet se supprime lui-même.</span><span class="sxs-lookup"><span data-stu-id="547f6-113">When the reference count reaches zero, the object deletes itself.</span></span>

## <a name="requirements"></a><span data-ttu-id="547f6-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="547f6-114">Requirements</span></span>



| <span data-ttu-id="547f6-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="547f6-115">Requirement</span></span> | <span data-ttu-id="547f6-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="547f6-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="547f6-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="547f6-117">Header</span></span><br/>  | <dl> <span data-ttu-id="547f6-118"><dt>ComBase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="547f6-118"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="547f6-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="547f6-119">Library</span></span><br/> | <dl> <span data-ttu-id="547f6-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="547f6-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




