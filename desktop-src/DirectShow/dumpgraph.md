---
description: La fonction DumpGraph envoie les informations relatives à un graphique de filtre à l’emplacement de sortie de débogage. Ignoré dans les builds de vente au détail.
ms.assetid: c78f86bb-44d0-4904-b7f8-e756bda0151d
title: DumpGraph, fonction (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DumpGraph
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 55c3adf793982b7b00ab44e26e7c34e08a1ac42b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526321"
---
# <a name="dumpgraph-function"></a><span data-ttu-id="6ccda-104">DumpGraph fonction)</span><span class="sxs-lookup"><span data-stu-id="6ccda-104">DumpGraph function</span></span>

<span data-ttu-id="6ccda-105">La `DumpGraph` fonction envoie des informations sur un graphique de filtre à l’emplacement de sortie de débogage.</span><span class="sxs-lookup"><span data-stu-id="6ccda-105">The `DumpGraph` function sends information about a filter graph to the debug output location.</span></span> <span data-ttu-id="6ccda-106">Ignoré dans les builds de vente au détail.</span><span class="sxs-lookup"><span data-stu-id="6ccda-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ccda-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6ccda-107">Syntax</span></span>


```C++
void DumpGraph(
   IFilterGraph *pGraph,
   DWORD        dwLevel
);
```



## <a name="parameters"></a><span data-ttu-id="6ccda-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6ccda-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ccda-109">*pGraph*</span><span class="sxs-lookup"><span data-stu-id="6ccda-109">*pGraph*</span></span> 
</dt> <dd>

<span data-ttu-id="6ccda-110">Pointeur vers l’interface [**IFilterGraph**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph) sur le gestionnaire de graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="6ccda-110">Pointer to the [**IFilterGraph**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph) interface on the filter graph manager.</span></span>

</dd> <dt>

<span data-ttu-id="6ccda-111">*dwLevel*</span><span class="sxs-lookup"><span data-stu-id="6ccda-111">*dwLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="6ccda-112">Niveau de journalisation.</span><span class="sxs-lookup"><span data-stu-id="6ccda-112">Logging level.</span></span> <span data-ttu-id="6ccda-113">La fonction génère un \_ message de trace du journal avec le niveau de journalisation spécifié.</span><span class="sxs-lookup"><span data-stu-id="6ccda-113">The function generates a LOG\_TRACE message with the specified logging level.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ccda-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6ccda-114">Return value</span></span>

<span data-ttu-id="6ccda-115">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="6ccda-115">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ccda-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6ccda-116">Requirements</span></span>



| <span data-ttu-id="6ccda-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6ccda-117">Requirement</span></span> | <span data-ttu-id="6ccda-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="6ccda-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ccda-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="6ccda-119">Header</span></span><br/>  | <dl> <span data-ttu-id="6ccda-120"><dt>Wxdebug. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6ccda-120"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6ccda-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6ccda-121">Library</span></span><br/> | <dl> <span data-ttu-id="6ccda-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="6ccda-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ccda-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6ccda-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ccda-124">Fonctions de sortie de débogage</span><span class="sxs-lookup"><span data-stu-id="6ccda-124">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




