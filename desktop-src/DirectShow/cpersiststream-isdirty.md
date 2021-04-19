---
description: Indique si l’objet a été modifié depuis son dernier enregistrement dans son flux actuel.
ms.assetid: 69840be6-062e-4505-8381-ea04e822c660
title: CPersistStream. IsDirty, méthode (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.IsDirty
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f3bc57998b63ece5ca32543fc00d1d3b5b4389b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535247"
---
# <a name="cpersiststreamisdirty-method"></a><span data-ttu-id="25635-103">CPersistStream. IsDirty, méthode</span><span class="sxs-lookup"><span data-stu-id="25635-103">CPersistStream.IsDirty method</span></span>

<span data-ttu-id="25635-104">Indique si l’objet a été modifié depuis son dernier enregistrement dans son flux actuel.</span><span class="sxs-lookup"><span data-stu-id="25635-104">Indicates whether the object has changed since it was last saved to its current stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="25635-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="25635-105">Syntax</span></span>


```C++
HRESULT IsDirty();
```



## <a name="parameters"></a><span data-ttu-id="25635-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="25635-106">Parameters</span></span>

<span data-ttu-id="25635-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="25635-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="25635-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="25635-108">Return value</span></span>

<span data-ttu-id="25635-109">Retourne S \_ OK si le filtre a besoin d’être enregistré et S \_ false s’il n’a pas besoin d’être enregistré.</span><span class="sxs-lookup"><span data-stu-id="25635-109">Returns S\_OK if the filter needs saving and S\_FALSE if it does not need saving.</span></span>

## <a name="remarks"></a><span data-ttu-id="25635-110">Notes</span><span class="sxs-lookup"><span data-stu-id="25635-110">Remarks</span></span>

<span data-ttu-id="25635-111">Cette fonction membre implémente la méthode **IPersistStream :: IsDirty** .</span><span class="sxs-lookup"><span data-stu-id="25635-111">This member function implements the **IPersistStream::IsDirty** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="25635-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="25635-112">Requirements</span></span>



| <span data-ttu-id="25635-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="25635-113">Requirement</span></span> | <span data-ttu-id="25635-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="25635-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25635-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="25635-115">Header</span></span><br/>  | <dl> <span data-ttu-id="25635-116"><dt>PStream. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="25635-116"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="25635-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="25635-117">Library</span></span><br/> | <dl> <span data-ttu-id="25635-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="25635-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25635-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25635-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25635-120">**CPersistStream, classe**</span><span class="sxs-lookup"><span data-stu-id="25635-120">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




