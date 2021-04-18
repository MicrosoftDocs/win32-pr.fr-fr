---
description: Charge les données du filtre à partir d’un flux donné.
ms.assetid: c2bfd379-2916-4698-bc41-653161723706
title: CPersistStream. Load, méthode (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.Load
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 83b16c3fe7bf905d1ade6b7f38cf27c61b44e4d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540316"
---
# <a name="cpersiststreamload-method"></a><span data-ttu-id="d45f7-103">CPersistStream. Load, méthode</span><span class="sxs-lookup"><span data-stu-id="d45f7-103">CPersistStream.Load method</span></span>

<span data-ttu-id="d45f7-104">Charge les données du filtre à partir d’un flux donné.</span><span class="sxs-lookup"><span data-stu-id="d45f7-104">Loads the filter's data from a given stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="d45f7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d45f7-105">Syntax</span></span>


```C++
HRESULT Load(
   LPSTREAM pStm
);
```



## <a name="parameters"></a><span data-ttu-id="d45f7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d45f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d45f7-107">*pStm*</span><span class="sxs-lookup"><span data-stu-id="d45f7-107">*pStm*</span></span> 
</dt> <dd>

<span data-ttu-id="d45f7-108">Pointeur vers le flux à partir duquel le chargement doit être effectué.</span><span class="sxs-lookup"><span data-stu-id="d45f7-108">Pointer to the stream from which to be loaded.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d45f7-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d45f7-109">Return value</span></span>

<span data-ttu-id="d45f7-110">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d45f7-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d45f7-111">Notes</span><span class="sxs-lookup"><span data-stu-id="d45f7-111">Remarks</span></span>

<span data-ttu-id="d45f7-112">Cette fonction membre implémente la méthode **IPersistStream :: Load** .</span><span class="sxs-lookup"><span data-stu-id="d45f7-112">This member function implements the **IPersistStream::Load** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d45f7-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d45f7-113">Requirements</span></span>



| <span data-ttu-id="d45f7-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d45f7-114">Requirement</span></span> | <span data-ttu-id="d45f7-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="d45f7-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d45f7-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="d45f7-116">Header</span></span><br/>  | <dl> <span data-ttu-id="d45f7-117"><dt>PStream. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d45f7-117"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d45f7-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d45f7-118">Library</span></span><br/> | <dl> <span data-ttu-id="d45f7-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d45f7-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d45f7-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d45f7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d45f7-121">**CPersistStream, classe**</span><span class="sxs-lookup"><span data-stu-id="d45f7-121">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




