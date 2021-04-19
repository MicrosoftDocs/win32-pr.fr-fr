---
description: Récupère la \# valeur DWORD FOURCC&160 ; à partir de l’objet FOURCCMap.
ms.assetid: bb382a57-8499-44c0-b287-2d31f5f5d1d0
title: 'FOURCCMap :: GetFOURCC, méthode (FourCC. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FOURCCMap.GetFOURCC
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c76493ff172f7a5611367fd50aa3b7957cf5441b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523519"
---
# <a name="fourccmapgetfourcc-method"></a><span data-ttu-id="50ca5-103">FOURCCMap :: GetFOURCC, méthode</span><span class="sxs-lookup"><span data-stu-id="50ca5-103">FOURCCMap::GetFOURCC method</span></span>

<span data-ttu-id="50ca5-104">Récupère la **valeur DWORD** **FourCC** de l’objet [**FOURCCMap**](fourccmap.md) .</span><span class="sxs-lookup"><span data-stu-id="50ca5-104">Retrieves the **FOURCC** **DWORD** from the [**FOURCCMap**](fourccmap.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="50ca5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="50ca5-105">Syntax</span></span>


```C++
DWORD GetFOURCC();
```



## <a name="parameters"></a><span data-ttu-id="50ca5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="50ca5-106">Parameters</span></span>

<span data-ttu-id="50ca5-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="50ca5-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="50ca5-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="50ca5-108">Return value</span></span>

<span data-ttu-id="50ca5-109">Retourne la valeur **DWORD** **FourCC** .</span><span class="sxs-lookup"><span data-stu-id="50ca5-109">Returns the **FOURCC** **DWORD** value.</span></span> <span data-ttu-id="50ca5-110">Notez que si vous construisez un **GUID** qui n’a pas été dérivé à l’origine d’un **FourCC**, la valeur de retour sera essentiellement aléatoire.</span><span class="sxs-lookup"><span data-stu-id="50ca5-110">Note that if you construct a **GUID** that was not originally derived from a **FOURCC**, the return value will be essentially random.</span></span>

## <a name="requirements"></a><span data-ttu-id="50ca5-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="50ca5-111">Requirements</span></span>



| <span data-ttu-id="50ca5-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="50ca5-112">Requirement</span></span> | <span data-ttu-id="50ca5-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="50ca5-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50ca5-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="50ca5-114">Header</span></span><br/>  | <dl> <span data-ttu-id="50ca5-115"><dt>FourCC. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="50ca5-115"><dt>Fourcc.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="50ca5-116">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="50ca5-116">Library</span></span><br/> | <dl> <span data-ttu-id="50ca5-117"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="50ca5-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50ca5-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50ca5-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50ca5-119">**FOURCCMap, classe**</span><span class="sxs-lookup"><span data-stu-id="50ca5-119">**FOURCCMap Class**</span></span>](fourccmap.md)
</dt> </dl>

 

 




