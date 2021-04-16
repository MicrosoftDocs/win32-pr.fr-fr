---
description: Rappel qui avertit l’hôte des informations de maillage des étapes de pipeline retournées par la requête dans.
MS-HAID: vspixengine.IPipeLineStagesCallback\_MeshDataVertCallback\_UINT\_UINT\_MeshDataBufferLayoutEntry\_arr\_UINT\_UINT\_BYTE\_arr\_UINT\_BYTE\_arr\_UINT\_UINT\_UINT\_UINT\_BOOL\_UINT\_UINT
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPipeLineStagesCallback :: MeshDataVertCallback, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E75EDE35-AC8E-4452-B79B-860C39B156F0
api_name:
- IPipeLineStagesCallback.MeshDataVertCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3c878851b0c3cfe32128d766f4dcb35a7437579d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521388"
---
# <a name="span-idvspixengineipipelinestagescallback_meshdatavertcallback_uint_uint_meshdatabufferlayoutentry_arr_uint_uint_byte_arr_uint_byte_arr_uint_uint_uint_uint_bool_uint_uintspanipipelinestagescallbackmeshdatavertcallback-method"></a><span data-ttu-id="867eb-103"><span id="vspixengine.ipipelinestagescallback_meshdatavertcallback_uint_uint_meshdatabufferlayoutentry_arr_uint_uint_byte_arr_uint_byte_arr_uint_uint_uint_uint_bool_uint_uint"></span>IPipeLineStagesCallback :: MeshDataVertCallback, méthode</span><span class="sxs-lookup"><span data-stu-id="867eb-103"><span id="vspixengine.ipipelinestagescallback_meshdatavertcallback_uint_uint_meshdatabufferlayoutentry_arr_uint_uint_byte_arr_uint_byte_arr_uint_uint_uint_uint_bool_uint_uint"></span>IPipeLineStagesCallback::MeshDataVertCallback method</span></span>

<span data-ttu-id="867eb-104">Rappel qui avertit l’hôte des informations de maillage des étapes de pipeline retournées par la requête dans.</span><span class="sxs-lookup"><span data-stu-id="867eb-104">A callback that notifies the host of pipeline stages mesh information returned by the assocaited request.</span></span>

## <a name="syntax"></a><span data-ttu-id="867eb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="867eb-105">Syntax</span></span>


```C++
HRESULT MeshDataVertCallback(
   UINT                         numVertices,
   UINT                         numBufferLayoutEntries,
   MeshDataBufferLayoutEntry [] count1_entries,
   UINT                         stride,
   UINT                         numVBBytes,
   BYTE []                      count4_pVBData,
   UINT                         numIBBytes,
   BYTE []                      count6_pIBData,
   UINT                         indexSize,
   UINT                         IBOffset,
   UINT                         baseVertex,
   UINT                         minVertex,
   BOOL                         IBIndexesVB,
   UINT                         numIndices,
   UINT                         topology
);
```

## <a name="parameters"></a><span data-ttu-id="867eb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="867eb-106">Parameters</span></span>

<span data-ttu-id="867eb-107">*numVertices* </span><span class="sxs-lookup"><span data-stu-id="867eb-107">*numVertices* </span></span>  
<span data-ttu-id="867eb-108">Nombre de vertex dans les résultats.</span><span class="sxs-lookup"><span data-stu-id="867eb-108">The number of vertices in the results.</span></span>

<span data-ttu-id="867eb-109">*numBufferLayoutEntries* </span><span class="sxs-lookup"><span data-stu-id="867eb-109">*numBufferLayoutEntries* </span></span>  
<span data-ttu-id="867eb-110">Nombre d’entrées de disposition de mémoire tampon dans les résultats.</span><span class="sxs-lookup"><span data-stu-id="867eb-110">The number of buffer layout entries in the results.</span></span>

<span data-ttu-id="867eb-111">*\_entrées count1* </span><span class="sxs-lookup"><span data-stu-id="867eb-111">*count1\_entries* </span></span>  
<span data-ttu-id="867eb-112">La disposition de la mémoire tampon entière.</span><span class="sxs-lookup"><span data-stu-id="867eb-112">The buffer layout entires.</span></span> <span data-ttu-id="867eb-113">Ils décrivent la signature de sortie du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="867eb-113">These describe the shader output signature.</span></span>

<span data-ttu-id="867eb-114">*progrès* </span><span class="sxs-lookup"><span data-stu-id="867eb-114">*stride* </span></span>  
<span data-ttu-id="867eb-115">Taille (Stride) d’un bloc de sortie entier.</span><span class="sxs-lookup"><span data-stu-id="867eb-115">The size (stride) of an entire output chunk.</span></span>

<span data-ttu-id="867eb-116">*numVBBytes* </span><span class="sxs-lookup"><span data-stu-id="867eb-116">*numVBBytes* </span></span>  
<span data-ttu-id="867eb-117">Taille de la mémoire tampon de vertex, en octets.</span><span class="sxs-lookup"><span data-stu-id="867eb-117">The size of the vertex buffer in bytes.</span></span>

<span data-ttu-id="867eb-118">*count4 \_ pVBData* </span><span class="sxs-lookup"><span data-stu-id="867eb-118">*count4\_pVBData* </span></span>  
<span data-ttu-id="867eb-119">Mémoire tampon de vertex.</span><span class="sxs-lookup"><span data-stu-id="867eb-119">The vertex buffer.</span></span>

<span data-ttu-id="867eb-120">*numIBBytes* </span><span class="sxs-lookup"><span data-stu-id="867eb-120">*numIBBytes* </span></span>  
<span data-ttu-id="867eb-121">Taille de la mémoire tampon d’index en octets.</span><span class="sxs-lookup"><span data-stu-id="867eb-121">The size of the index buffer in bytes.</span></span>

<span data-ttu-id="867eb-122">*count6 \_ pIBData* </span><span class="sxs-lookup"><span data-stu-id="867eb-122">*count6\_pIBData* </span></span>  
<span data-ttu-id="867eb-123">Mémoire tampon d’index.</span><span class="sxs-lookup"><span data-stu-id="867eb-123">The index buffer.</span></span>

<span data-ttu-id="867eb-124">*indexSize* </span><span class="sxs-lookup"><span data-stu-id="867eb-124">*indexSize* </span></span>  
<span data-ttu-id="867eb-125">Taille de chaque index, en octets.</span><span class="sxs-lookup"><span data-stu-id="867eb-125">The size of each index in bytes.</span></span>

<span data-ttu-id="867eb-126">*IBOffset* </span><span class="sxs-lookup"><span data-stu-id="867eb-126">*IBOffset* </span></span>  
<span data-ttu-id="867eb-127">Offset dans la mémoire tampon d’index qui spécifie où les index doivent commencer à être utilisés.</span><span class="sxs-lookup"><span data-stu-id="867eb-127">An offset into the index buffer that specifies where indices should start being used.</span></span>

<span data-ttu-id="867eb-128">*baseVertex* </span><span class="sxs-lookup"><span data-stu-id="867eb-128">*baseVertex* </span></span>  
<span data-ttu-id="867eb-129">Offset dans la mémoire tampon de vertex qui spécifie l’emplacement où les vertex doivent commencer à être utilisés.</span><span class="sxs-lookup"><span data-stu-id="867eb-129">An offset into the vertex buffer that specifies where vertices should start being used.</span></span>

<span data-ttu-id="867eb-130">*minVertex*</span><span class="sxs-lookup"><span data-stu-id="867eb-130">*minVertex*</span></span>   

<span data-ttu-id="867eb-131">*IBIndexesVB* </span><span class="sxs-lookup"><span data-stu-id="867eb-131">*IBIndexesVB* </span></span>  
<span data-ttu-id="867eb-132">true lorsque la mémoire tampon d’index est utilisée ; Sinon, false.</span><span class="sxs-lookup"><span data-stu-id="867eb-132">true when the index buffer is used; otherwise false.</span></span>

<span data-ttu-id="867eb-133">*numIndices* </span><span class="sxs-lookup"><span data-stu-id="867eb-133">*numIndices* </span></span>  
<span data-ttu-id="867eb-134">Nombre d’index utilisés.</span><span class="sxs-lookup"><span data-stu-id="867eb-134">The number of indices used.</span></span>

<span data-ttu-id="867eb-135">*topologie* </span><span class="sxs-lookup"><span data-stu-id="867eb-135">*topology* </span></span>  
<span data-ttu-id="867eb-136">Topolology du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="867eb-136">The topolology of the shader.</span></span> <span data-ttu-id="867eb-137">Ce n’est pas nécessairement le même que la topologie de l’appel de dessin associé.</span><span class="sxs-lookup"><span data-stu-id="867eb-137">This is not necessarily the same as the topology of the associated draw call.</span></span>

## <a name="return-value"></a><span data-ttu-id="867eb-138">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="867eb-138">Return value</span></span>

<span data-ttu-id="867eb-139">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="867eb-139">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="867eb-140">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="867eb-140">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="867eb-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="867eb-141">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="867eb-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="867eb-142">Header</span></span></p></td><td><span data-ttu-id="867eb-143">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="867eb-143">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="867eb-144"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="867eb-144"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="867eb-145">**IPipeLineStagesCallback**</span><span class="sxs-lookup"><span data-stu-id="867eb-145">**IPipeLineStagesCallback**</span></span>](/windows/desktop/direct3dtools/ipipelinestagescallback)

 

 
