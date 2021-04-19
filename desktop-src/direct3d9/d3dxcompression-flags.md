---
description: Définit le mode de compression utilisé pour le stockage des données de jeu d’animations compressées.
ms.assetid: 41592b71-52ba-4727-a885-fb10fc23c5f8
title: Énumération D3DXCOMPRESSION_FLAGS (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCOMPRESSION_FLAGS
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 6f912c44659d418d543194ba82a9d82f31e7ef08
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523835"
---
# <a name="d3dxcompression_flags-enumeration"></a><span data-ttu-id="88dea-103">\_Énumération d’indicateurs D3DXCOMPRESSION</span><span class="sxs-lookup"><span data-stu-id="88dea-103">D3DXCOMPRESSION\_FLAGS enumeration</span></span>

<span data-ttu-id="88dea-104">Définit le mode de compression utilisé pour le stockage des données de jeu d’animations compressées.</span><span class="sxs-lookup"><span data-stu-id="88dea-104">Defines the compression mode used for storing compressed animation set data.</span></span>

## <a name="syntax"></a><span data-ttu-id="88dea-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="88dea-105">Syntax</span></span>


```C++
typedef enum D3DXCOMPRESSION_FLAGS { 
  D3DXCOMPRESS_DEFAULT      = 0,
  D3DXCOMPRESS_STRONG       = 1,
  D3DXCOMPRESS_FORCE_DWORD  = 0x7fffffff
} D3DXCOMPRESSION_FLAGS, *LPD3DXCOMPRESSION_FLAGS;
```



## <a name="constants"></a><span data-ttu-id="88dea-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="88dea-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="88dea-107"><span id="D3DXCOMPRESS_DEFAULT"></span><span id="d3dxcompress_default"></span>**D3DXCOMPRESS \_ par défaut**</span><span class="sxs-lookup"><span data-stu-id="88dea-107"><span id="D3DXCOMPRESS_DEFAULT"></span><span id="d3dxcompress_default"></span>**D3DXCOMPRESS\_DEFAULT**</span></span>
</dt> <dd>

<span data-ttu-id="88dea-108">Implémente la compression rapide.</span><span class="sxs-lookup"><span data-stu-id="88dea-108">Implements fast compression.</span></span>

</dd> <dt>

<span data-ttu-id="88dea-109"><span id="D3DXCOMPRESS_STRONG"></span><span id="d3dxcompress_strong"></span>**D3DXCOMPRESS \_ Strong**</span><span class="sxs-lookup"><span data-stu-id="88dea-109"><span id="D3DXCOMPRESS_STRONG"></span><span id="d3dxcompress_strong"></span>**D3DXCOMPRESS\_STRONG**</span></span>
</dt> <dd>

<span data-ttu-id="88dea-110">Implémente la compression lente.</span><span class="sxs-lookup"><span data-stu-id="88dea-110">Implements slow compression.</span></span> <span data-ttu-id="88dea-111">Produit généralement une meilleure qualité d’animation compressée que si D3DXCOMPRESS \_ est utilisé par défaut.</span><span class="sxs-lookup"><span data-stu-id="88dea-111">Typically results in a better quality compressed animation set than if D3DXCOMPRESS\_DEFAULT is used.</span></span>

</dd> <dt>

<span data-ttu-id="88dea-112"><span id="D3DXCOMPRESS_FORCE_DWORD"></span><span id="d3dxcompress_force_dword"></span>**D3DXCOMPRESS \_ forcer \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="88dea-112"><span id="D3DXCOMPRESS_FORCE_DWORD"></span><span id="d3dxcompress_force_dword"></span>**D3DXCOMPRESS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="88dea-113">Force cette énumération à se compiler à 32 bits de taille.</span><span class="sxs-lookup"><span data-stu-id="88dea-113">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="88dea-114">Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits.</span><span class="sxs-lookup"><span data-stu-id="88dea-114">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="88dea-115">Cette valeur n'est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="88dea-115">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="88dea-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="88dea-116">Requirements</span></span>



| <span data-ttu-id="88dea-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="88dea-117">Requirement</span></span> | <span data-ttu-id="88dea-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="88dea-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="88dea-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="88dea-119">Header</span></span><br/> | <dl> <span data-ttu-id="88dea-120"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="88dea-120"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88dea-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="88dea-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88dea-122">Énumérations D3DX</span><span class="sxs-lookup"><span data-stu-id="88dea-122">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




