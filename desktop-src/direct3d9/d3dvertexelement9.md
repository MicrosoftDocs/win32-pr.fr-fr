---
description: Définit la disposition des données de vertex. Chaque vertex peut contenir un ou plusieurs types de données, et chaque type de données est décrit par un élément vertex.
ms.assetid: 6f3c40a0-b28e-48d6-acad-ef80a919c5d7
title: D3DVERTEXELEMENT9, structure (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVERTEXELEMENT9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: e6c5e9508185124673ca7464b31d741cdf8035c8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106537265"
---
# <a name="d3dvertexelement9-structure"></a><span data-ttu-id="84843-104">D3DVERTEXELEMENT9, structure</span><span class="sxs-lookup"><span data-stu-id="84843-104">D3DVERTEXELEMENT9 structure</span></span>

<span data-ttu-id="84843-105">Définit la disposition des données de vertex.</span><span class="sxs-lookup"><span data-stu-id="84843-105">Defines the vertex data layout.</span></span> <span data-ttu-id="84843-106">Chaque vertex peut contenir un ou plusieurs types de données, et chaque type de données est décrit par un élément vertex.</span><span class="sxs-lookup"><span data-stu-id="84843-106">Each vertex can contain one or more data types, and each data type is described by a vertex element.</span></span>

## <a name="syntax"></a><span data-ttu-id="84843-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="84843-107">Syntax</span></span>


```C++
typedef struct D3DVERTEXELEMENT9 {
  WORD Stream;
  WORD Offset;
  BYTE Type;
  BYTE Method;
  BYTE Usage;
  BYTE UsageIndex;
} D3DVERTEXELEMENT9, *LPD3DVERTEXELEMENT9;
```



## <a name="members"></a><span data-ttu-id="84843-108">Membres</span><span class="sxs-lookup"><span data-stu-id="84843-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="84843-109">**Stream**</span><span class="sxs-lookup"><span data-stu-id="84843-109">**Stream**</span></span>
</dt> <dd>

<span data-ttu-id="84843-110">Type : **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="84843-110">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="84843-111">Numéro de flux.</span><span class="sxs-lookup"><span data-stu-id="84843-111">Stream number.</span></span>

</dd> <dt>

<span data-ttu-id="84843-112">**Offset**</span><span class="sxs-lookup"><span data-stu-id="84843-112">**Offset**</span></span>
</dt> <dd>

<span data-ttu-id="84843-113">Type : **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="84843-113">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="84843-114">Décalage entre le début des données de vertex et les données associées au type de données particulier.</span><span class="sxs-lookup"><span data-stu-id="84843-114">Offset from the beginning of the vertex data to the data associated with the particular data type.</span></span>

</dd> <dt>

<span data-ttu-id="84843-115">**Type**</span><span class="sxs-lookup"><span data-stu-id="84843-115">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="84843-116">Type : **[ **Byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="84843-116">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="84843-117">Type de données spécifié en tant que [**D3DDECLTYPE**](./d3ddecltype.md).</span><span class="sxs-lookup"><span data-stu-id="84843-117">The data type, specified as a [**D3DDECLTYPE**](./d3ddecltype.md).</span></span> <span data-ttu-id="84843-118">Un des nombreux types prédéfinis qui définissent la taille des données.</span><span class="sxs-lookup"><span data-stu-id="84843-118">One of several predefined types that define the data size.</span></span> <span data-ttu-id="84843-119">Certaines méthodes ont un type implicite.</span><span class="sxs-lookup"><span data-stu-id="84843-119">Some methods have an implied type.</span></span>

</dd> <dt>

<span data-ttu-id="84843-120">**Méthode**</span><span class="sxs-lookup"><span data-stu-id="84843-120">**Method**</span></span>
</dt> <dd>

<span data-ttu-id="84843-121">Type : **[ **Byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="84843-121">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="84843-122">La méthode spécifie le traitement du paveur, qui détermine comment le du paveur interprète (ou fonctionne) les données de vertex.</span><span class="sxs-lookup"><span data-stu-id="84843-122">The method specifies the tessellator processing, which determines how the tessellator interprets (or operates on) the vertex data.</span></span> <span data-ttu-id="84843-123">Pour plus d’informations, consultez [**D3DDECLMETHOD**](./d3ddeclmethod.md).</span><span class="sxs-lookup"><span data-stu-id="84843-123">For more information, see [**D3DDECLMETHOD**](./d3ddeclmethod.md).</span></span>

</dd> <dt>

<span data-ttu-id="84843-124">**Utilisation**</span><span class="sxs-lookup"><span data-stu-id="84843-124">**Usage**</span></span>
</dt> <dd>

<span data-ttu-id="84843-125">Type : **[ **Byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="84843-125">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="84843-126">Définit ce à quoi les données seront utilisées ; autrement dit, l’interopérabilité entre la disposition des données de vertex et les nuanceurs de sommets.</span><span class="sxs-lookup"><span data-stu-id="84843-126">Defines what the data will be used for; that is, the interoperability between vertex data layouts and vertex shaders.</span></span> <span data-ttu-id="84843-127">Chaque utilisation agit pour lier une déclaration de vertex à un nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="84843-127">Each usage acts to bind a vertex declaration to a vertex shader.</span></span> <span data-ttu-id="84843-128">Dans certains cas, ils ont une interprétation spéciale.</span><span class="sxs-lookup"><span data-stu-id="84843-128">In some cases, they have a special interpretation.</span></span> <span data-ttu-id="84843-129">Par exemple, un élément qui spécifie D3DDECLUSAGE \_ normal ou \_ la position D3DDECLUSAGE est utilisé par le du paveur de patch N pour configurer le pavage.</span><span class="sxs-lookup"><span data-stu-id="84843-129">For example, an element that specifies D3DDECLUSAGE\_NORMAL or D3DDECLUSAGE\_POSITION is used by the N-patch tessellator to set up tessellation.</span></span> <span data-ttu-id="84843-130">Pour obtenir la liste des sémantiques disponibles, consultez [**D3DDECLUSAGE**](./d3ddeclusage.md) .</span><span class="sxs-lookup"><span data-stu-id="84843-130">See [**D3DDECLUSAGE**](./d3ddeclusage.md) for a list of the available semantics.</span></span> <span data-ttu-id="84843-131">D3DDECLUSAGE \_ texcoord peut être utilisé pour les champs définis par l’utilisateur (qui n’ont pas d’utilisation existante définie).</span><span class="sxs-lookup"><span data-stu-id="84843-131">D3DDECLUSAGE\_TEXCOORD can be used for user-defined fields (which don't have an existing usage defined).</span></span>

</dd> <dt>

<span data-ttu-id="84843-132">**UsageIndex**</span><span class="sxs-lookup"><span data-stu-id="84843-132">**UsageIndex**</span></span>
</dt> <dd>

<span data-ttu-id="84843-133">Type : **[ **Byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="84843-133">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="84843-134">Modifie les données d’utilisation pour permettre à l’utilisateur de spécifier plusieurs types d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="84843-134">Modifies the usage data to allow the user to specify multiple usage types.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="84843-135">Notes</span><span class="sxs-lookup"><span data-stu-id="84843-135">Remarks</span></span>

<span data-ttu-id="84843-136">Les données de vertex sont définies à l’aide d’un tableau de structures **D3DVERTEXELEMENT9** .</span><span class="sxs-lookup"><span data-stu-id="84843-136">Vertex data is defined using an array of **D3DVERTEXELEMENT9** structures.</span></span> <span data-ttu-id="84843-137">Utilisez [**D3DDECL \_ end**](d3ddecl-end.md) pour déclarer le dernier élément de la déclaration.</span><span class="sxs-lookup"><span data-stu-id="84843-137">Use [**D3DDECL\_END**](d3ddecl-end.md) to declare the last element in the declaration.</span></span>

## <a name="requirements"></a><span data-ttu-id="84843-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="84843-138">Requirements</span></span>



| <span data-ttu-id="84843-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="84843-139">Requirement</span></span> | <span data-ttu-id="84843-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="84843-140">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="84843-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="84843-141">Header</span></span><br/> | <dl> <span data-ttu-id="84843-142"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="84843-142"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84843-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="84843-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84843-144">Structures Direct3D</span><span class="sxs-lookup"><span data-stu-id="84843-144">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="84843-145">Déclaration de vertex (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="84843-145">Vertex Declaration (Direct3D 9)</span></span>](vertex-declaration.md)
</dt> </dl>

 

 
