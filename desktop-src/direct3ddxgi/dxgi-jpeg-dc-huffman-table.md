---
description: Décrit une table de Huffmans de la table de contrôle d’images JPEG.
ms.assetid: 9D6C18C3-F75C-41E0-9EFA-E882E89DE713
title: Structure DXGI_JPEG_DC_HUFFMAN_TABLE (Dxgitype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXGI_JPEG_DC_HUFFMAN_TABLE
api_type:
- HeaderDef
api_location:
- dxgitype.h
ms.openlocfilehash: b2f5f73f7c6def745b987818b9ec30fb3e2752e2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211735"
---
# <a name="dxgi_jpeg_dc_huffman_table-structure"></a><span data-ttu-id="44ef1-103">\_Structure de \_ \_ table Huffman \_ dxgi JPEG DC</span><span class="sxs-lookup"><span data-stu-id="44ef1-103">DXGI\_JPEG\_DC\_HUFFMAN\_TABLE structure</span></span>

<span data-ttu-id="44ef1-104">Décrit une table de Huffmans de la table de contrôle d’images JPEG.</span><span class="sxs-lookup"><span data-stu-id="44ef1-104">Describes a JPEG DC huffman table.</span></span>

## <a name="syntax"></a><span data-ttu-id="44ef1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="44ef1-105">Syntax</span></span>


```C++
typedef struct DXGI_JPEG_DC_HUFFMAN_TABLE {
  BYTE CodeCounts[12];
  BYTE CodeValues[12];
} DXGI_JPEG_DC_HUFFMAN_TABLE;
```



## <a name="members"></a><span data-ttu-id="44ef1-106">Membres</span><span class="sxs-lookup"><span data-stu-id="44ef1-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="44ef1-107">**CodeCounts**</span><span class="sxs-lookup"><span data-stu-id="44ef1-107">**CodeCounts**</span></span>
</dt> <dd>

<span data-ttu-id="44ef1-108">Nombre de codes pour chaque longueur de code.</span><span class="sxs-lookup"><span data-stu-id="44ef1-108">The number of codes for each code length.</span></span>

</dd> <dt>

<span data-ttu-id="44ef1-109">**CodeValues**</span><span class="sxs-lookup"><span data-stu-id="44ef1-109">**CodeValues**</span></span>
</dt> <dd>

<span data-ttu-id="44ef1-110">Valeurs de code Huffman, par ordre de croissance de la longueur de code.</span><span class="sxs-lookup"><span data-stu-id="44ef1-110">The Huffman code values, in order of increasing code length.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="44ef1-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="44ef1-111">Requirements</span></span>



| <span data-ttu-id="44ef1-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="44ef1-112">Requirement</span></span> | <span data-ttu-id="44ef1-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="44ef1-113">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="44ef1-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="44ef1-114">Header</span></span><br/> | <dl> <span data-ttu-id="44ef1-115"><dt>Dxgitype. h</dt></span><span class="sxs-lookup"><span data-stu-id="44ef1-115"><dt>Dxgitype.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44ef1-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="44ef1-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44ef1-117">Structures DXGI</span><span class="sxs-lookup"><span data-stu-id="44ef1-117">DXGI Structures</span></span>](d3d10-graphics-reference-dxgi-structures.md)
</dt> </dl>

 

 




