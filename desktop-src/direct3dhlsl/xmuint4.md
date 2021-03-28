---
title: XMUINT4, structure
description: Décrit un vecteur d’entier non signé 4D.
ms.assetid: 289293e5-882e-479c-886e-82c802f824b5
keywords:
- XMUINT4 structure HLSL
topic_type:
- apiref
api_name:
- XMUINT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f0b02ffe64e7b4c4479723b4e36abd87f6bd03b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974442"
---
# <a name="xmuint4-structure"></a><span data-ttu-id="72013-104">XMUINT4, structure</span><span class="sxs-lookup"><span data-stu-id="72013-104">XMUINT4 structure</span></span>

<span data-ttu-id="72013-105">Décrit un vecteur d’entier non signé 4D.</span><span class="sxs-lookup"><span data-stu-id="72013-105">Describes an 4D unsigned integer vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="72013-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="72013-106">Syntax</span></span>


``` syntax
typedef struct _XMUINT4 {
  UINT x;
  UINT {
    UINT {
      UINT w;
    }z;
  }y;
} XMUINT4;
```



## <a name="members"></a><span data-ttu-id="72013-107">Membres</span><span class="sxs-lookup"><span data-stu-id="72013-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="72013-108">**x**</span><span class="sxs-lookup"><span data-stu-id="72013-108">**x**</span></span>
</dt> <dd>

<span data-ttu-id="72013-109">composant x du vecteur.</span><span class="sxs-lookup"><span data-stu-id="72013-109">x-component of the vector.</span></span>

</dd> <dt>

<span data-ttu-id="72013-110">**y**</span><span class="sxs-lookup"><span data-stu-id="72013-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="72013-111">composant y du vecteur.</span><span class="sxs-lookup"><span data-stu-id="72013-111">y-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="72013-112">**Lettre**</span><span class="sxs-lookup"><span data-stu-id="72013-112">**z**</span></span>
</dt> <dd>

<span data-ttu-id="72013-113">composant z du vecteur.</span><span class="sxs-lookup"><span data-stu-id="72013-113">z-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="72013-114">**w**</span><span class="sxs-lookup"><span data-stu-id="72013-114">**w**</span></span>
</dt> <dd>

<span data-ttu-id="72013-115">composant w du vecteur.</span><span class="sxs-lookup"><span data-stu-id="72013-115">w-component of the vector.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="72013-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="72013-116">Requirements</span></span>



| <span data-ttu-id="72013-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="72013-117">Requirement</span></span> | <span data-ttu-id="72013-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="72013-118">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72013-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="72013-119">Header</span></span><br/> | <dl> <span data-ttu-id="72013-120"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="72013-120"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72013-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="72013-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72013-122">Structures</span><span class="sxs-lookup"><span data-stu-id="72013-122">Structures</span></span>](format-conversion-structures.md)
</dt> <dt>

[<span data-ttu-id="72013-123">Décompresser et compresser le \_ format DXGI pour la modification des images In-Place</span><span class="sxs-lookup"><span data-stu-id="72013-123">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





