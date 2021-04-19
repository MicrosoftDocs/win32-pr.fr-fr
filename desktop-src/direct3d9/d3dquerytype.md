---
description: Identifie le type de requête.
ms.assetid: 575c4e71-3cab-4123-a2a5-d23b53e87111
title: Énumération D3DQUERYTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DQUERYTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 21cb3e2f2254d54caacd4217d3e0023446a0c6f1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531553"
---
# <a name="d3dquerytype-enumeration"></a><span data-ttu-id="59f8e-103">Énumération D3DQUERYTYPE</span><span class="sxs-lookup"><span data-stu-id="59f8e-103">D3DQUERYTYPE enumeration</span></span>

<span data-ttu-id="59f8e-104">Identifie le type de requête.</span><span class="sxs-lookup"><span data-stu-id="59f8e-104">Identifies the query type.</span></span> <span data-ttu-id="59f8e-105">Pour plus d’informations sur les requêtes, consultez [requêtes (Direct3D 9)](queries.md) .</span><span class="sxs-lookup"><span data-stu-id="59f8e-105">For information about queries, see [Queries (Direct3D 9)](queries.md)</span></span>

## <a name="syntax"></a><span data-ttu-id="59f8e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="59f8e-106">Syntax</span></span>


```C++
typedef enum D3DQUERYTYPE { 
  D3DQUERYTYPE_VCACHE             = 4,
  D3DQUERYTYPE_ResourceManager    = 5,
  D3DQUERYTYPE_VERTEXSTATS        = 6,
  D3DQUERYTYPE_EVENT              = 8,
  D3DQUERYTYPE_OCCLUSION          = 9,
  D3DQUERYTYPE_TIMESTAMP          = 10,
  D3DQUERYTYPE_TIMESTAMPDISJOINT  = 11,
  D3DQUERYTYPE_TIMESTAMPFREQ      = 12,
  D3DQUERYTYPE_PIPELINETIMINGS    = 13,
  D3DQUERYTYPE_INTERFACETIMINGS   = 14,
  D3DQUERYTYPE_VERTEXTIMINGS      = 15,
  D3DQUERYTYPE_PIXELTIMINGS       = 16,
  D3DQUERYTYPE_BANDWIDTHTIMINGS   = 17,
  D3DQUERYTYPE_CACHEUTILIZATION   = 18,
  D3DQUERYTYPE_MEMORYPRESSURE     = 19
} D3DQUERYTYPE, *LPD3DQUERYTYPE;
```



## <a name="constants"></a><span data-ttu-id="59f8e-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="59f8e-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="59f8e-108"><span id="D3DQUERYTYPE_VCACHE"></span><span id="d3dquerytype_vcache"></span>**D3DQUERYTYPE \_ Vcache**</span><span class="sxs-lookup"><span data-stu-id="59f8e-108"><span id="D3DQUERYTYPE_VCACHE"></span><span id="d3dquerytype_vcache"></span>**D3DQUERYTYPE\_VCACHE**</span></span>
</dt> <dd>

<span data-ttu-id="59f8e-109">Recherchez des indications de pilote sur la disposition des données pour la mise en cache des vertex.</span><span class="sxs-lookup"><span data-stu-id="59f8e-109">Query for driver hints about data layout for vertex caching.</span></span>

</dd> <dt>

<span data-ttu-id="59f8e-110"><span id="D3DQUERYTYPE_ResourceManager"></span><span id="d3dquerytype_resourcemanager"></span><span id="D3DQUERYTYPE_RESOURCEMANAGER"></span>**D3DQUERYTYPE \_ ResourceManager**</span><span class="sxs-lookup"><span data-stu-id="59f8e-110"><span id="D3DQUERYTYPE_ResourceManager"></span><span id="d3dquerytype_resourcemanager"></span><span id="D3DQUERYTYPE_RESOURCEMANAGER"></span>**D3DQUERYTYPE\_ResourceManager**</span></span>
</dt> <dd>

<span data-ttu-id="59f8e-111">Interrogez le gestionnaire des ressources.</span><span class="sxs-lookup"><span data-stu-id="59f8e-111">Query the resource manager.</span></span> <span data-ttu-id="59f8e-112">Pour cette requête, les indicateurs de comportement de l’appareil doivent inclure la [ \_ gestion des \_ pilotes \_ D3DCREATE Disable](d3dcreate.md).</span><span class="sxs-lookup"><span data-stu-id="59f8e-112">For this query, the device behavior flags must include [D3DCREATE\_DISABLE\_DRIVER\_MANAGEMENT](d3dcreate.md).</span></span>

</dd> <dt>

<span data-ttu-id="59f8e-113"><span id="D3DQUERYTYPE_VERTEXSTATS"></span><span id="d3dquerytype_vertexstats"></span>**D3DQUERYTYPE \_ VERTEXSTATS**</span><span class="sxs-lookup"><span data-stu-id="59f8e-113"><span id="D3DQUERYTYPE_VERTEXSTATS"></span><span id="d3dquerytype_vertexstats"></span>**D3DQUERYTYPE\_VERTEXSTATS**</span></span>
</dt> <dd>

<span data-ttu-id="59f8e-114">Statistiques des vertex de la requête.</span><span class="sxs-lookup"><span data-stu-id="59f8e-114">Query vertex statistics.</span></span>

</dd> <dt>

<span data-ttu-id="59f8e-115"><span id="D3DQUERYTYPE_EVENT"></span><span id="d3dquerytype_event"></span>**\_Événement D3DQUERYTYPE**</span><span class="sxs-lookup"><span data-stu-id="59f8e-115"><span id="D3DQUERYTYPE_EVENT"></span><span id="d3dquerytype_event"></span>**D3DQUERYTYPE\_EVENT**</span></span>
</dt> <dd>

<span data-ttu-id="59f8e-116">Recherchez tous les événements asynchrones émis à partir d’appels d’API et tous les événements asynchrones.</span><span class="sxs-lookup"><span data-stu-id="59f8e-116">Query for any and all asynchronous events that have been issued from API calls.</span></span>

</dd> <dt>

<span data-ttu-id="59f8e-117"><span id="D3DQUERYTYPE_OCCLUSION"></span><span id="d3dquerytype_occlusion"></span>**\_Occlusion D3DQUERYTYPE**</span><span class="sxs-lookup"><span data-stu-id="59f8e-117"><span id="D3DQUERYTYPE_OCCLUSION"></span><span id="d3dquerytype_occlusion"></span>**D3DQUERYTYPE\_OCCLUSION**</span></span>
</dt> <dd>

<span data-ttu-id="59f8e-118">Une requête d’occlusion retourne le nombre de pixels qui passent le test z.</span><span class="sxs-lookup"><span data-stu-id="59f8e-118">An occlusion query returns the number of pixels that pass z-testing.</span></span> <span data-ttu-id="59f8e-119">Ces pixels sont destinés aux primitives dessinées entre le problème de [**D3DISSUE \_ Begin**](d3dissue-begin.md) et [**D3DISSUE \_ end**](d3dissue-end.md).</span><span class="sxs-lookup"><span data-stu-id="59f8e-119">These pixels are for primitives drawn between the issue of [**D3DISSUE\_BEGIN**](d3dissue-begin.md) and [**D3DISSUE\_END**](d3dissue-end.md).</span></span> <span data-ttu-id="59f8e-120">Cela permet à une application de vérifier le résultat d’occlusion par rapport à 0.</span><span class="sxs-lookup"><span data-stu-id="59f8e-120">This enables an application to check the occlusion result against 0.</span></span> <span data-ttu-id="59f8e-121">Zéro est entièrement bloqués, ce qui signifie que les pixels ne sont pas visibles à partir de la position actuelle de la caméra.</span><span class="sxs-lookup"><span data-stu-id="59f8e-121">Zero is fully occluded, which means the pixels are not visible from the current camera position.</span></span>

</dd> <dt>

<span data-ttu-id="59f8e-122"><span id="D3DQUERYTYPE_TIMESTAMP"></span><span id="d3dquerytype_timestamp"></span>**\_Horodateur D3DQUERYTYPE**</span><span class="sxs-lookup"><span data-stu-id="59f8e-122"><span id="D3DQUERYTYPE_TIMESTAMP"></span><span id="d3dquerytype_timestamp"></span>**D3DQUERYTYPE\_TIMESTAMP**</span></span>
</dt> <dd>

<span data-ttu-id="59f8e-123">Retourne un horodateur 64 bits.</span><span class="sxs-lookup"><span data-stu-id="59f8e-123">Returns a 64-bit timestamp.</span></span>

</dd> <dt>

<span data-ttu-id="59f8e-124"><span id="D3DQUERYTYPE_TIMESTAMPDISJOINT"></span><span id="d3dquerytype_timestampdisjoint"></span>**D3DQUERYTYPE \_ TIMESTAMPDISJOINT**</span><span class="sxs-lookup"><span data-stu-id="59f8e-124"><span id="D3DQUERYTYPE_TIMESTAMPDISJOINT"></span><span id="d3dquerytype_timestampdisjoint"></span>**D3DQUERYTYPE\_TIMESTAMPDISJOINT**</span></span>
</dt> <dd>

<span data-ttu-id="59f8e-125">Utilisez cette requête pour notifier une application si la fréquence du compteur est modifiée par rapport à l' \_ horodateur D3DQUERYTYPE.</span><span class="sxs-lookup"><span data-stu-id="59f8e-125">Use this query to notify an application if the counter frequency has changed from the D3DQUERYTYPE\_TIMESTAMP.</span></span>

</dd> <dt>

<span data-ttu-id="59f8e-126"><span id="D3DQUERYTYPE_TIMESTAMPFREQ"></span><span id="d3dquerytype_timestampfreq"></span>**D3DQUERYTYPE \_ TIMESTAMPFREQ**</span><span class="sxs-lookup"><span data-stu-id="59f8e-126"><span id="D3DQUERYTYPE_TIMESTAMPFREQ"></span><span id="d3dquerytype_timestampfreq"></span>**D3DQUERYTYPE\_TIMESTAMPFREQ**</span></span>
</dt> <dd>

<span data-ttu-id="59f8e-127">Ce résultat de requête est **true** si les valeurs des \_ requêtes d’horodatage D3DQUERYTYPE ne peuvent pas être garanties en continu pendant toute la durée de la \_ requête de TIMESTAMPDISJOINT D3DQUERYTYPE.</span><span class="sxs-lookup"><span data-stu-id="59f8e-127">This query result is **TRUE** if the values from D3DQUERYTYPE\_TIMESTAMP queries cannot be guaranteed to be continuous throughout the duration of the D3DQUERYTYPE\_TIMESTAMPDISJOINT query.</span></span> <span data-ttu-id="59f8e-128">Dans le cas contraire, le résultat de la requête est **false**.</span><span class="sxs-lookup"><span data-stu-id="59f8e-128">Otherwise, the query result is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="59f8e-129"><span id="D3DQUERYTYPE_PIPELINETIMINGS"></span><span id="d3dquerytype_pipelinetimings"></span>**D3DQUERYTYPE \_ PIPELINETIMINGS**</span><span class="sxs-lookup"><span data-stu-id="59f8e-129"><span id="D3DQUERYTYPE_PIPELINETIMINGS"></span><span id="d3dquerytype_pipelinetimings"></span>**D3DQUERYTYPE\_PIPELINETIMINGS**</span></span>
</dt> <dd>

<span data-ttu-id="59f8e-130">Pourcentage de temps de traitement des données de pipeline.</span><span class="sxs-lookup"><span data-stu-id="59f8e-130">Percent of time processing pipeline data.</span></span>

</dd> <dt>

<span data-ttu-id="59f8e-131"><span id="D3DQUERYTYPE_INTERFACETIMINGS"></span><span id="d3dquerytype_interfacetimings"></span>**D3DQUERYTYPE \_ INTERFACETIMINGS**</span><span class="sxs-lookup"><span data-stu-id="59f8e-131"><span id="D3DQUERYTYPE_INTERFACETIMINGS"></span><span id="d3dquerytype_interfacetimings"></span>**D3DQUERYTYPE\_INTERFACETIMINGS**</span></span>
</dt> <dd>

<span data-ttu-id="59f8e-132">Pourcentage de temps de traitement des données dans le pilote.</span><span class="sxs-lookup"><span data-stu-id="59f8e-132">Percent of time processing data in the driver.</span></span>

</dd> <dt>

<span data-ttu-id="59f8e-133"><span id="D3DQUERYTYPE_VERTEXTIMINGS"></span><span id="d3dquerytype_vertextimings"></span>**D3DQUERYTYPE \_ VERTEXTIMINGS**</span><span class="sxs-lookup"><span data-stu-id="59f8e-133"><span id="D3DQUERYTYPE_VERTEXTIMINGS"></span><span id="d3dquerytype_vertextimings"></span>**D3DQUERYTYPE\_VERTEXTIMINGS**</span></span>
</dt> <dd>

<span data-ttu-id="59f8e-134">Pourcentage de temps de traitement des données de nuanceur de vertex.</span><span class="sxs-lookup"><span data-stu-id="59f8e-134">Percent of time processing vertex shader data.</span></span>

</dd> <dt>

<span data-ttu-id="59f8e-135"><span id="D3DQUERYTYPE_PIXELTIMINGS"></span><span id="d3dquerytype_pixeltimings"></span>**D3DQUERYTYPE \_ PIXELTIMINGS**</span><span class="sxs-lookup"><span data-stu-id="59f8e-135"><span id="D3DQUERYTYPE_PIXELTIMINGS"></span><span id="d3dquerytype_pixeltimings"></span>**D3DQUERYTYPE\_PIXELTIMINGS**</span></span>
</dt> <dd>

<span data-ttu-id="59f8e-136">Pourcentage de temps de traitement des données de nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="59f8e-136">Percent of time processing pixel shader data.</span></span>

</dd> <dt>

<span data-ttu-id="59f8e-137"><span id="D3DQUERYTYPE_BANDWIDTHTIMINGS"></span><span id="d3dquerytype_bandwidthtimings"></span>**D3DQUERYTYPE \_ BANDWIDTHTIMINGS**</span><span class="sxs-lookup"><span data-stu-id="59f8e-137"><span id="D3DQUERYTYPE_BANDWIDTHTIMINGS"></span><span id="d3dquerytype_bandwidthtimings"></span>**D3DQUERYTYPE\_BANDWIDTHTIMINGS**</span></span>
</dt> <dd>

<span data-ttu-id="59f8e-138">Les comparaisons de mesure du débit pour vous aider à comprendre les performances d’une application.</span><span class="sxs-lookup"><span data-stu-id="59f8e-138">Throughput measurement comparisons for help in understanding the performance of an application.</span></span>

</dd> <dt>

<span data-ttu-id="59f8e-139"><span id="D3DQUERYTYPE_CACHEUTILIZATION"></span><span id="d3dquerytype_cacheutilization"></span>**D3DQUERYTYPE \_ CACHEUTILIZATION**</span><span class="sxs-lookup"><span data-stu-id="59f8e-139"><span id="D3DQUERYTYPE_CACHEUTILIZATION"></span><span id="d3dquerytype_cacheutilization"></span>**D3DQUERYTYPE\_CACHEUTILIZATION**</span></span>
</dt> <dd>

<span data-ttu-id="59f8e-140">Mesurez les performances du taux d’accès au cache pour les textures et les vertex indexés.</span><span class="sxs-lookup"><span data-stu-id="59f8e-140">Measure the cache hit-rate performance for textures and indexed vertices.</span></span>

</dd> <dt>

<span data-ttu-id="59f8e-141"><span id="D3DQUERYTYPE_MEMORYPRESSURE"></span><span id="d3dquerytype_memorypressure"></span>**D3DQUERYTYPE \_ MEMORYPRESSURE**</span><span class="sxs-lookup"><span data-stu-id="59f8e-141"><span id="D3DQUERYTYPE_MEMORYPRESSURE"></span><span id="d3dquerytype_memorypressure"></span>**D3DQUERYTYPE\_MEMORYPRESSURE**</span></span>
</dt> <dd>

<span data-ttu-id="59f8e-142">Efficacité de l’allocation de mémoire contenue dans une structure [**D3DMEMORYPRESSURE**](d3dmemorypressure.md) .</span><span class="sxs-lookup"><span data-stu-id="59f8e-142">Efficiency of memory allocation contained in a [**D3DMEMORYPRESSURE**](d3dmemorypressure.md) structure.</span></span>



|                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59f8e-143">Différences entre Direct3D 9 et Direct3D 9Ex :</span><span class="sxs-lookup"><span data-stu-id="59f8e-143">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="59f8e-144">D3DQUERYTYPE \_ MEMORYPRESSURE est disponible uniquement dans Direct3D9Ex qui s’exécute sur Windows 7 (ou plus le système d’exploitation actuel).</span><span class="sxs-lookup"><span data-stu-id="59f8e-144">D3DQUERYTYPE\_MEMORYPRESSURE is only available in Direct3D9Ex running on Windows 7 (or more current operating system).</span></span><br/> |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="59f8e-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="59f8e-145">Requirements</span></span>



| <span data-ttu-id="59f8e-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="59f8e-146">Requirement</span></span> | <span data-ttu-id="59f8e-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="59f8e-147">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="59f8e-148">En-tête</span><span class="sxs-lookup"><span data-stu-id="59f8e-148">Header</span></span><br/> | <dl> <span data-ttu-id="59f8e-149"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="59f8e-149"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59f8e-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59f8e-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59f8e-151">Énumérations Direct3D</span><span class="sxs-lookup"><span data-stu-id="59f8e-151">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="59f8e-152">**IDirect3DDevice9 :: CreateQuery**</span><span class="sxs-lookup"><span data-stu-id="59f8e-152">**IDirect3DDevice9::CreateQuery**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery)
</dt> </dl>

 

 
