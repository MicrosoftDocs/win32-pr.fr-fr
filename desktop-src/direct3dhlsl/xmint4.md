---
title: XMINT4, structure
description: Décrit un vecteur d’entiers 4D.
ms.assetid: 1f21727d-fcb4-4514-b30e-d8ef0e36c256
keywords:
- XMINT4 structure HLSL
topic_type:
- apiref
api_name:
- XMINT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 302d820428fafb1561bd38850c4f75240ce9094f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323129"
---
# <a name="xmint4-structure"></a><span data-ttu-id="1ed12-104">XMINT4, structure</span><span class="sxs-lookup"><span data-stu-id="1ed12-104">XMINT4 structure</span></span>

<span data-ttu-id="1ed12-105">Décrit un vecteur d’entiers 4D.</span><span class="sxs-lookup"><span data-stu-id="1ed12-105">Describes an 4D integer vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ed12-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1ed12-106">Syntax</span></span>


``` syntax
typedef struct _XMINT4 {
  INT x;
  INT {
    INT {
      INT w;
    }z;
  }y;
} XMINT4;
```



## <a name="members"></a><span data-ttu-id="1ed12-107">Membres</span><span class="sxs-lookup"><span data-stu-id="1ed12-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="1ed12-108">**x**</span><span class="sxs-lookup"><span data-stu-id="1ed12-108">**x**</span></span>
</dt> <dd>

<span data-ttu-id="1ed12-109">composant x du vecteur.</span><span class="sxs-lookup"><span data-stu-id="1ed12-109">x-component of the vector.</span></span>

</dd> <dt>

<span data-ttu-id="1ed12-110">**y**</span><span class="sxs-lookup"><span data-stu-id="1ed12-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="1ed12-111">composant y du vecteur.</span><span class="sxs-lookup"><span data-stu-id="1ed12-111">y-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="1ed12-112">**Lettre**</span><span class="sxs-lookup"><span data-stu-id="1ed12-112">**z**</span></span>
</dt> <dd>

<span data-ttu-id="1ed12-113">composant z du vecteur.</span><span class="sxs-lookup"><span data-stu-id="1ed12-113">z-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="1ed12-114">**w**</span><span class="sxs-lookup"><span data-stu-id="1ed12-114">**w**</span></span>
</dt> <dd>

<span data-ttu-id="1ed12-115">composant w du vecteur.</span><span class="sxs-lookup"><span data-stu-id="1ed12-115">w-component of the vector.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1ed12-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1ed12-116">Requirements</span></span>



| <span data-ttu-id="1ed12-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1ed12-117">Requirement</span></span> | <span data-ttu-id="1ed12-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="1ed12-118">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ed12-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="1ed12-119">Header</span></span><br/> | <dl> <span data-ttu-id="1ed12-120"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="1ed12-120"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ed12-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ed12-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ed12-122">Structures</span><span class="sxs-lookup"><span data-stu-id="1ed12-122">Structures</span></span>](format-conversion-structures.md)
</dt> <dt>

[<span data-ttu-id="1ed12-123">Décompresser et compresser le \_ format DXGI pour la modification des images In-Place</span><span class="sxs-lookup"><span data-stu-id="1ed12-123">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





