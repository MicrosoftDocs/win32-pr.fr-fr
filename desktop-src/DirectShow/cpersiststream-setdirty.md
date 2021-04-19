---
description: Modifie l’indicateur de modification pour le flux actuel.
ms.assetid: 65fa7fbe-4fa7-45a3-91a4-4a3547b035b9
title: CPersistStream. SetDirty, méthode (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.SetDirty
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 382b74f6314beb586b1e51c02a257cad8904c188
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541150"
---
# <a name="cpersiststreamsetdirty-method"></a><span data-ttu-id="bc094-103">CPersistStream. SetDirty, méthode</span><span class="sxs-lookup"><span data-stu-id="bc094-103">CPersistStream.SetDirty method</span></span>

<span data-ttu-id="bc094-104">Modifie l’indicateur de modification pour le flux actuel.</span><span class="sxs-lookup"><span data-stu-id="bc094-104">Changes the dirty flag for the current stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc094-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bc094-105">Syntax</span></span>


```C++
HRESULT SetDirty(
   BOOL fDirty
);
```



## <a name="parameters"></a><span data-ttu-id="bc094-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bc094-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc094-107">*fDirty*</span><span class="sxs-lookup"><span data-stu-id="bc094-107">*fDirty*</span></span> 
</dt> <dd>

<span data-ttu-id="bc094-108">Nouvel indicateur de changement pour ce flux.</span><span class="sxs-lookup"><span data-stu-id="bc094-108">New dirty flag for this stream.</span></span> <span data-ttu-id="bc094-109">**True** signifie que les données n’ont pas été enregistrées.</span><span class="sxs-lookup"><span data-stu-id="bc094-109">**TRUE** means that the data has not been saved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc094-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bc094-110">Return value</span></span>

<span data-ttu-id="bc094-111">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bc094-111">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc094-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bc094-112">Requirements</span></span>



| <span data-ttu-id="bc094-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bc094-113">Requirement</span></span> | <span data-ttu-id="bc094-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="bc094-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc094-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="bc094-115">Header</span></span><br/>  | <dl> <span data-ttu-id="bc094-116"><dt>PStream. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bc094-116"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bc094-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bc094-117">Library</span></span><br/> | <dl> <span data-ttu-id="bc094-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="bc094-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc094-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bc094-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc094-120">**CPersistStream, classe**</span><span class="sxs-lookup"><span data-stu-id="bc094-120">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




