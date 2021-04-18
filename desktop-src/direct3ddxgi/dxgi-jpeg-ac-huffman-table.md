---
description: Décrit une table de Huffmans de l’AC JPEG.
ms.assetid: E1923FFA-E7E5-4158-9793-3E7F5A6EA7FA
title: Structure DXGI_JPEG_AC_HUFFMAN_TABLE (Dxgitype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXGI_JPEG_AC_HUFFMAN_TABLE
api_type:
- HeaderDef
api_location:
- dxgitype.h
ms.openlocfilehash: 760840822eb6b9411983c72324bc1e86a3208195
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522584"
---
# <a name="dxgi_jpeg_ac_huffman_table-structure"></a><span data-ttu-id="12876-103">\_Structure de \_ \_ table Huffman \_ dxgi JPEG AC</span><span class="sxs-lookup"><span data-stu-id="12876-103">DXGI\_JPEG\_AC\_HUFFMAN\_TABLE structure</span></span>

<span data-ttu-id="12876-104">Décrit une table de Huffmans de l’AC JPEG.</span><span class="sxs-lookup"><span data-stu-id="12876-104">Describes a JPEG AC huffman table.</span></span>

## <a name="syntax"></a><span data-ttu-id="12876-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="12876-105">Syntax</span></span>


```C++
typedef struct DXGI_JPEG_AC_HUFFMAN_TABLE {
  BYTE CodeCounts[16];
  BYTE CodeValues[162];
} DXGI_JPEG_AC_HUFFMAN_TABLE;
```



## <a name="members"></a><span data-ttu-id="12876-106">Membres</span><span class="sxs-lookup"><span data-stu-id="12876-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="12876-107">**CodeCounts**</span><span class="sxs-lookup"><span data-stu-id="12876-107">**CodeCounts**</span></span>
</dt> <dd>

<span data-ttu-id="12876-108">Nombre de codes pour chaque longueur de code.</span><span class="sxs-lookup"><span data-stu-id="12876-108">The number of codes for each code length.</span></span>

</dd> <dt>

<span data-ttu-id="12876-109">**CodeValues**</span><span class="sxs-lookup"><span data-stu-id="12876-109">**CodeValues**</span></span>
</dt> <dd>

<span data-ttu-id="12876-110">Valeurs de code Huffman, par ordre de croissance de la longueur de code.</span><span class="sxs-lookup"><span data-stu-id="12876-110">The Huffman code values, in order of increasing code length.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="12876-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="12876-111">Requirements</span></span>



| <span data-ttu-id="12876-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="12876-112">Requirement</span></span> | <span data-ttu-id="12876-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="12876-113">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="12876-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="12876-114">Header</span></span><br/> | <dl> <span data-ttu-id="12876-115"><dt>Dxgitype. h</dt></span><span class="sxs-lookup"><span data-stu-id="12876-115"><dt>Dxgitype.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12876-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="12876-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12876-117">Structures DXGI</span><span class="sxs-lookup"><span data-stu-id="12876-117">DXGI Structures</span></span>](d3d10-graphics-reference-dxgi-structures.md)
</dt> </dl>

 

 




