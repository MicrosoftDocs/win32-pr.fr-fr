---
description: La fonction GetInterface récupère un pointeur d’interface.
ms.assetid: 75fe8849-c779-4d47-a5ff-5a23308c8a21
title: GetInterface, fonction (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetInterface
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 317f08af2a4ff0e9410c61da8b19d14735a14f6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539995"
---
# <a name="getinterface-function"></a><span data-ttu-id="da198-103">GetInterface, fonction</span><span class="sxs-lookup"><span data-stu-id="da198-103">GetInterface function</span></span>

<span data-ttu-id="da198-104">La `GetInterface` fonction récupère un pointeur d’interface.</span><span class="sxs-lookup"><span data-stu-id="da198-104">The `GetInterface` function retrieves an interface pointer.</span></span>

## <a name="syntax"></a><span data-ttu-id="da198-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="da198-105">Syntax</span></span>


```C++
HRESULT GetInterface(
   LPUNKNOWN pUnk,
   void      **ppv
);
```



## <a name="parameters"></a><span data-ttu-id="da198-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="da198-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da198-107">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="da198-107">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="da198-108">Pointeur vers l’interface **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="da198-108">Pointer to the **IUnknown** interface.</span></span>

</dd> <dt>

<span data-ttu-id="da198-109">*ppv*</span><span class="sxs-lookup"><span data-stu-id="da198-109">*ppv*</span></span> 
</dt> <dd>

<span data-ttu-id="da198-110">Adresse d’un pointeur vers l’interface récupérée.</span><span class="sxs-lookup"><span data-stu-id="da198-110">Address of a pointer to the retrieved interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da198-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="da198-111">Return value</span></span>

<span data-ttu-id="da198-112">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="da198-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="da198-113">Notes</span><span class="sxs-lookup"><span data-stu-id="da198-113">Remarks</span></span>

<span data-ttu-id="da198-114">Cette fonction membre effectue un incrément thread-safe du décompte de références.</span><span class="sxs-lookup"><span data-stu-id="da198-114">This member function performs a thread-safe increment of the reference count.</span></span> <span data-ttu-id="da198-115">Pour récupérer l’interface et ajouter une référence, appelez cette fonction à partir de votre implémentation de substitution de la méthode **INonDelegatingUnknown :: NonDelegatingQueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="da198-115">To retrieve the interface and add a reference, call this function from your overriding implementation of the **INonDelegatingUnknown::NonDelegatingQueryInterface** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="da198-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="da198-116">Requirements</span></span>



| <span data-ttu-id="da198-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="da198-117">Requirement</span></span> | <span data-ttu-id="da198-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="da198-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da198-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="da198-119">Header</span></span><br/>  | <dl> <span data-ttu-id="da198-120"><dt>ComBase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="da198-120"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="da198-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="da198-121">Library</span></span><br/> | <dl> <span data-ttu-id="da198-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="da198-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da198-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da198-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da198-124">**Fonctions d’assistance COM**</span><span class="sxs-lookup"><span data-stu-id="da198-124">**COM Helper Functions**</span></span>](com-helper-functions.md)
</dt> <dt>

[<span data-ttu-id="da198-125">**INonDelegatingUnknown**</span><span class="sxs-lookup"><span data-stu-id="da198-125">**INonDelegatingUnknown**</span></span>](inondelegatingunknown.md)
</dt> </dl>

 

 




