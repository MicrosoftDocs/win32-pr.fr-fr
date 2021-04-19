---
description: Verrou pour protéger la création d’objets à l’intérieur du filtre.
ms.assetid: ad1d2584-0d9e-42a8-83ea-0c1907ddcf33
title: 'Membre CBaseRenderer :: m_ObjectCreationLock (Renbase. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_ObjectCreationLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e344b20b4924ac26ebe6253f5388136b350abefe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534863"
---
# <a name="cbaserendererm_objectcreationlock-member"></a><span data-ttu-id="f9d44-103">CBaseRenderer :: m \_ ObjectCreationLock, membre</span><span class="sxs-lookup"><span data-stu-id="f9d44-103">CBaseRenderer::m\_ObjectCreationLock member</span></span>

<span data-ttu-id="f9d44-104">Verrou pour protéger la création d’objets à l’intérieur du filtre.</span><span class="sxs-lookup"><span data-stu-id="f9d44-104">Lock to protect the creation of objects inside the filter.</span></span> <span data-ttu-id="f9d44-105">Le filtre maintient ce verrou lorsqu’il crée la broche d’entrée ([**CBaseRenderer :: m \_ pInputPin**](cbaserenderer-m-pinputpin.md)) ou l’objet [**CRendererPosPassThru**](crendererpospassthru.md) ([**CBaseRenderer :: m \_ pPosition**](cbaserenderer-m-pposition.md)).</span><span class="sxs-lookup"><span data-stu-id="f9d44-105">The filter holds this lock when it creates the input pin ([**CBaseRenderer::m\_pInputPin**](cbaserenderer-m-pinputpin.md)) or the [**CRendererPosPassThru**](crendererpospassthru.md) object ([**CBaseRenderer::m\_pPosition**](cbaserenderer-m-pposition.md)).</span></span> <span data-ttu-id="f9d44-106">Ce verrou empêche plusieurs threads de tenter de créer l’un de ces objets en même temps.</span><span class="sxs-lookup"><span data-stu-id="f9d44-106">This lock prevents multiple threads from attempting to create one of these objects at the same time.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9d44-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f9d44-107">Syntax</span></span>


```C++
CCritSec m_ObjectCreationLock;
```



## <a name="requirements"></a><span data-ttu-id="f9d44-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f9d44-108">Requirements</span></span>



| <span data-ttu-id="f9d44-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f9d44-109">Requirement</span></span> | <span data-ttu-id="f9d44-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9d44-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9d44-111">En-tête</span><span class="sxs-lookup"><span data-stu-id="f9d44-111">Header</span></span><br/>  | <dl> <span data-ttu-id="f9d44-112"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f9d44-112"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f9d44-113">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f9d44-113">Library</span></span><br/> | <dl> <span data-ttu-id="f9d44-114"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f9d44-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9d44-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f9d44-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9d44-116">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="f9d44-116">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




