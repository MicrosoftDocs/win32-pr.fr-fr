---
description: Décrit une mémoire tampon d’index.
ms.assetid: 5d45213e-b3c0-4eb7-a4f9-8d8730eb3899
title: Structure D3DINDEXBUFFER_DESC (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DINDEXBUFFER_DESC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 0a0bf63e732541f9394231cd82c23ff71a584b1e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953880"
---
# <a name="d3dindexbuffer_desc-structure"></a><span data-ttu-id="d2f06-103">D3DINDEXBUFFER \_ desc, structure</span><span class="sxs-lookup"><span data-stu-id="d2f06-103">D3DINDEXBUFFER\_DESC structure</span></span>

<span data-ttu-id="d2f06-104">Décrit une mémoire tampon d’index.</span><span class="sxs-lookup"><span data-stu-id="d2f06-104">Describes an index buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2f06-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d2f06-105">Syntax</span></span>


```C++
typedef struct D3DINDEXBUFFER_DESC {
  D3DFORMAT       Format;
  D3DRESOURCETYPE Type;
  DWORD           Usage;
  D3DPOOL         Pool;
  UINT            Size;
} D3DINDEXBUFFER_DESC, *LPD3DINDEXBUFFER_DESC;
```



## <a name="members"></a><span data-ttu-id="d2f06-106">Membres</span><span class="sxs-lookup"><span data-stu-id="d2f06-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d2f06-107">**Format**</span><span class="sxs-lookup"><span data-stu-id="d2f06-107">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="d2f06-108">Type : **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="d2f06-108">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d2f06-109">Membre du type énuméré [D3DFORMAT](d3dformat.md) , décrivant le format de surface des données de la mémoire tampon d’index.</span><span class="sxs-lookup"><span data-stu-id="d2f06-109">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the surface format of the index buffer data.</span></span>

</dd> <dt>

<span data-ttu-id="d2f06-110">**Type**</span><span class="sxs-lookup"><span data-stu-id="d2f06-110">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="d2f06-111">Type : **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**</span><span class="sxs-lookup"><span data-stu-id="d2f06-111">Type: **[**D3DRESOURCETYPE**](./d3dresourcetype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d2f06-112">Membre du type énuméré [**D3DRESOURCETYPE**](./d3dresourcetype.md) , identifiant cette ressource comme une mémoire tampon d’index.</span><span class="sxs-lookup"><span data-stu-id="d2f06-112">Member of the [**D3DRESOURCETYPE**](./d3dresourcetype.md) enumerated type, identifying this resource as an index buffer.</span></span>

</dd> <dt>

<span data-ttu-id="d2f06-113">**Utilisation**</span><span class="sxs-lookup"><span data-stu-id="d2f06-113">**Usage**</span></span>
</dt> <dd>

<span data-ttu-id="d2f06-114">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d2f06-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d2f06-115">Combinaison d’un ou plusieurs des indicateurs suivants, en spécifiant l’utilisation de cette ressource.</span><span class="sxs-lookup"><span data-stu-id="d2f06-115">Combination of one or more of the following flags, specifying the usage for this resource.</span></span>



| <span data-ttu-id="d2f06-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2f06-116">Value</span></span>                                                                                                                                                                                                   | <span data-ttu-id="d2f06-117">Signification</span><span class="sxs-lookup"><span data-stu-id="d2f06-117">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DUSAGE_DONOTCLIP"></span><span id="d3dusage_donotclip"></span><dl> <span data-ttu-id="d2f06-118"><dt>**D3DUSAGE \_ DONOTCLIP**</dt></span><span class="sxs-lookup"><span data-stu-id="d2f06-118"><dt>**D3DUSAGE\_DONOTCLIP**</dt></span></span> </dl>                            | <span data-ttu-id="d2f06-119">Défini pour indiquer que le contenu de la mémoire tampon d’index ne nécessitera jamais de découpage.</span><span class="sxs-lookup"><span data-stu-id="d2f06-119">Set to indicate that the index buffer content will never require clipping.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="D3DUSAGE_DYNAMIC"></span><span id="d3dusage_dynamic"></span><dl> <span data-ttu-id="d2f06-120"><dt>**D3DUSAGE \_ dynamique**</dt></span><span class="sxs-lookup"><span data-stu-id="d2f06-120"><dt>**D3DUSAGE\_DYNAMIC**</dt></span></span> </dl>                                  | <span data-ttu-id="d2f06-121">Défini pour indiquer que la mémoire tampon d’index requiert l’utilisation de la mémoire dynamique.</span><span class="sxs-lookup"><span data-stu-id="d2f06-121">Set to indicate that the index buffer requires dynamic memory use.</span></span> <span data-ttu-id="d2f06-122">Cela est utile pour les pilotes, car cela leur permet de décider où placer la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="d2f06-122">This is useful for drivers because it enables them to decide where to place the buffer.</span></span> <span data-ttu-id="d2f06-123">En général, les mémoires tampons d’index statiques sont placées dans la mémoire vidéo et les mémoires tampons d’index dynamiques sont placées dans la mémoire AGP.</span><span class="sxs-lookup"><span data-stu-id="d2f06-123">In general, static index buffers are placed in video memory and dynamic index buffers are placed in AGP memory.</span></span> <span data-ttu-id="d2f06-124">Notez qu’il n’y a pas d’utilisation statique distincte ; Si vous ne spécifiez pas D3DUSAGE \_ dynamique, le tampon d’index est rendu statique.</span><span class="sxs-lookup"><span data-stu-id="d2f06-124">Note that there is no separate static usage; if you do not specify D3DUSAGE\_DYNAMIC the index buffer is made static.</span></span> <span data-ttu-id="d2f06-125">D3DUSAGE \_ Dynamic est strictement appliqué via les \_ indicateurs de verrouillage D3DLOCK ignore et D3DLOCK \_ NOOVERWRITE.</span><span class="sxs-lookup"><span data-stu-id="d2f06-125">D3DUSAGE\_DYNAMIC is strictly enforced through the D3DLOCK\_DISCARD and D3DLOCK\_NOOVERWRITE locking flags.</span></span> <span data-ttu-id="d2f06-126">Par conséquent, les D3DLOCK \_ ignorés et D3DLOCK \_ NOOVERWRITE sont valides uniquement sur les tampons d’index créés avec D3DUSAGE \_ dynamique ; il ne s’agit pas d’indicateurs valides sur les mémoires tampons de vertex statiques.</span><span class="sxs-lookup"><span data-stu-id="d2f06-126">As a result, D3DLOCK\_DISCARD and D3DLOCK\_NOOVERWRITE are only valid on index buffers created with D3DUSAGE\_DYNAMIC; they are not valid flags on static vertex buffers.</span></span><br/> <span data-ttu-id="d2f06-127">Pour plus d’informations sur l’utilisation des mémoires tampons d’index dynamiques, consultez [utilisation de mémoires tampons de vertex et d’index dynamiques](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="d2f06-127">For more information about using dynamic index buffers, see [Using Dynamic Vertex and Index Buffers](performance-optimizations.md).</span></span><br/> <span data-ttu-id="d2f06-128">Notez que D3DUSAGE \_ Dynamic ne peut pas être spécifié dans les tampons d’index managés.</span><span class="sxs-lookup"><span data-stu-id="d2f06-128">Note that D3DUSAGE\_DYNAMIC cannot be specified on managed index buffers.</span></span> <span data-ttu-id="d2f06-129">Pour plus d’informations, consultez [gestion des ressources (Direct3D 9)](managing-resources.md).</span><span class="sxs-lookup"><span data-stu-id="d2f06-129">For more information, see [Managing Resources (Direct3D 9)](managing-resources.md).</span></span><br/> |
| <span id="D3DUSAGE_RTPATCHES"></span><span id="d3dusage_rtpatches"></span><dl> <span data-ttu-id="d2f06-130"><dt>**D3DUSAGE \_ RTPATCHES**</dt></span><span class="sxs-lookup"><span data-stu-id="d2f06-130"><dt>**D3DUSAGE\_RTPATCHES**</dt></span></span> </dl>                            | <span data-ttu-id="d2f06-131">Défini pour indiquer à quel moment la mémoire tampon d’index doit être utilisée pour le dessin des primitives d’ordre élevé.</span><span class="sxs-lookup"><span data-stu-id="d2f06-131">Set to indicate when the index buffer is to be used for drawing high-order primitives.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="D3DUSAGE_NPATCHES"></span><span id="d3dusage_npatches"></span><dl> <span data-ttu-id="d2f06-132"><dt>**D3DUSAGE \_ NPATCHES**</dt></span><span class="sxs-lookup"><span data-stu-id="d2f06-132"><dt>**D3DUSAGE\_NPATCHES**</dt></span></span> </dl>                               | <span data-ttu-id="d2f06-133">Défini pour indiquer à quel moment la mémoire tampon d’index doit être utilisée pour le dessin des N correctifs.</span><span class="sxs-lookup"><span data-stu-id="d2f06-133">Set to indicate when the index buffer is to be used for drawing N patches.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="D3DUSAGE_POINTS"></span><span id="d3dusage_points"></span><dl> <span data-ttu-id="d2f06-134"><dt>**POINTS de D3DUSAGE \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d2f06-134"><dt>**D3DUSAGE\_POINTS**</dt></span></span> </dl>                                     | <span data-ttu-id="d2f06-135">Défini pour indiquer le moment où le tampon d’index doit être utilisé pour les points de dessin des sprites ou les listes de points indexés.</span><span class="sxs-lookup"><span data-stu-id="d2f06-135">Set to indicate when the index buffer is to be used for drawing point sprites or indexed point lists.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="D3DUSAGE_SOFTWAREPROCESSING"></span><span id="d3dusage_softwareprocessing"></span><dl> <span data-ttu-id="d2f06-136"><dt>**D3DUSAGE \_ SOFTWAREPROCESSING**</dt></span><span class="sxs-lookup"><span data-stu-id="d2f06-136"><dt>**D3DUSAGE\_SOFTWAREPROCESSING**</dt></span></span> </dl> | <span data-ttu-id="d2f06-137">Défini pour indiquer que la mémoire tampon doit être utilisée avec le traitement logiciel.</span><span class="sxs-lookup"><span data-stu-id="d2f06-137">Set to indicate that the buffer is to be used with software processing.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="D3DUSAGE_WRITEONLY"></span><span id="d3dusage_writeonly"></span><dl> <span data-ttu-id="d2f06-138"><dt>**D3DUSAGE \_ WRITEONLY**</dt></span><span class="sxs-lookup"><span data-stu-id="d2f06-138"><dt>**D3DUSAGE\_WRITEONLY**</dt></span></span> </dl>                            | <span data-ttu-id="d2f06-139">Informe le système que l’application écrit uniquement dans la mémoire tampon d’index.</span><span class="sxs-lookup"><span data-stu-id="d2f06-139">Informs the system that the application writes only to the index buffer.</span></span> <span data-ttu-id="d2f06-140">L’utilisation de cet indicateur permet au pilote de choisir le meilleur emplacement de mémoire pour des opérations d’écriture et un rendu efficaces.</span><span class="sxs-lookup"><span data-stu-id="d2f06-140">Using this flag enables the driver to choose the best memory location for efficient write operations and rendering.</span></span> <span data-ttu-id="d2f06-141">Les tentatives de lecture à partir d’un tampon d’index créé avec cette fonctionnalité peuvent entraîner une dégradation des performances.</span><span class="sxs-lookup"><span data-stu-id="d2f06-141">Attempts to read from an index buffer that is created with this capability can result in degraded performance.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

<span data-ttu-id="d2f06-142">**Pool**</span><span class="sxs-lookup"><span data-stu-id="d2f06-142">**Pool**</span></span>
</dt> <dd>

<span data-ttu-id="d2f06-143">Type : **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="d2f06-143">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d2f06-144">Membre du type énuméré [**D3DPOOL**](./d3dpool.md) , spécifiant la classe de mémoire allouée pour cette mémoire tampon d’index.</span><span class="sxs-lookup"><span data-stu-id="d2f06-144">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, specifying the class of memory allocated for this index buffer.</span></span>

</dd> <dt>

<span data-ttu-id="d2f06-145">**Taille**</span><span class="sxs-lookup"><span data-stu-id="d2f06-145">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="d2f06-146">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d2f06-146">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d2f06-147">Taille de la mémoire tampon d’index, en octets.</span><span class="sxs-lookup"><span data-stu-id="d2f06-147">Size of the index buffer, in bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d2f06-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d2f06-148">Requirements</span></span>



| <span data-ttu-id="d2f06-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d2f06-149">Requirement</span></span> | <span data-ttu-id="d2f06-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2f06-150">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2f06-151">En-tête</span><span class="sxs-lookup"><span data-stu-id="d2f06-151">Header</span></span><br/> | <dl> <span data-ttu-id="d2f06-152"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2f06-152"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2f06-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d2f06-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2f06-154">Structures Direct3D</span><span class="sxs-lookup"><span data-stu-id="d2f06-154">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="d2f06-155">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="d2f06-155">**GetDesc**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-getdesc)
</dt> <dt>

[<span data-ttu-id="d2f06-156">Mémoires tampons d’index (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d2f06-156">Index Buffers (Direct3D 9)</span></span>](index-buffers.md)
</dt> </dl>

 

 
