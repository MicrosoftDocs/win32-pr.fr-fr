---
description: Méthode de destructeur.
ms.assetid: 92375e95-adfb-414b-abbb-e827db2186ac
title: CMediaType. ~ CMediaType, destructeur (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.~CMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 26efde8fe7d3c3efd0f29c77945011cef5834829
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535223"
---
# <a name="cmediatypecmediatype-destructor"></a><span data-ttu-id="34537-103">CMediaType. ~ CMediaType, destructeur</span><span class="sxs-lookup"><span data-stu-id="34537-103">CMediaType.~CMediaType destructor</span></span>

<span data-ttu-id="34537-104">Méthode de destructeur.</span><span class="sxs-lookup"><span data-stu-id="34537-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="34537-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="34537-105">Syntax</span></span>


```C++
~CMediaType();
```



## <a name="remarks"></a><span data-ttu-id="34537-106">Notes</span><span class="sxs-lookup"><span data-stu-id="34537-106">Remarks</span></span>

<span data-ttu-id="34537-107">Le destructeur appelle la fonction [**FreeMediaType**](freemediatype.md) sur lui-même.</span><span class="sxs-lookup"><span data-stu-id="34537-107">The destructor calls the [**FreeMediaType**](freemediatype.md) function on itself.</span></span>

## <a name="requirements"></a><span data-ttu-id="34537-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="34537-108">Requirements</span></span>



| <span data-ttu-id="34537-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="34537-109">Requirement</span></span> | <span data-ttu-id="34537-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="34537-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34537-111">En-tête</span><span class="sxs-lookup"><span data-stu-id="34537-111">Header</span></span><br/>  | <dl> <span data-ttu-id="34537-112"><dt>Mtype. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="34537-112"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="34537-113">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="34537-113">Library</span></span><br/> | <dl> <span data-ttu-id="34537-114"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="34537-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34537-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="34537-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34537-116">**CMediaType, classe**</span><span class="sxs-lookup"><span data-stu-id="34537-116">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




