---
description: Définit les types de texture de l’échantillonneur pour les nuanceurs de vertex.
ms.assetid: 8e9923f9-6f30-45e5-a557-f26d441a534d
title: Énumération D3DSAMPLER_TEXTURE_TYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSAMPLER_TEXTURE_TYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 337e8b25a8ec8389a6252fb48582128c601730ca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394063"
---
# <a name="d3dsampler_texture_type-enumeration"></a><span data-ttu-id="50edc-103">\_Énumération de type de texture D3DSAMPLER \_</span><span class="sxs-lookup"><span data-stu-id="50edc-103">D3DSAMPLER\_TEXTURE\_TYPE enumeration</span></span>

<span data-ttu-id="50edc-104">Définit les types de texture de l’échantillonneur pour les nuanceurs de vertex.</span><span class="sxs-lookup"><span data-stu-id="50edc-104">Defines the sampler texture types for vertex shaders.</span></span>

## <a name="syntax"></a><span data-ttu-id="50edc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="50edc-105">Syntax</span></span>


```C++
typedef enum D3DSAMPLER_TEXTURE_TYPE { 
  D3DSTT_UNKNOWN,
  D3DSTT_2D,
  D3DSTT_CUBE,
  D3DSTT_VOLUME,
  D3DSTT_FORCE_DWORD
} D3DSAMPLER_TEXTURE_TYPE, *LPD3DSAMPLER_TEXTURE_TYPE;
```



## <a name="constants"></a><span data-ttu-id="50edc-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="50edc-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="50edc-107"><span id="D3DSTT_UNKNOWN"></span><span id="d3dstt_unknown"></span>**D3DSTT \_ inconnu**</span><span class="sxs-lookup"><span data-stu-id="50edc-107"><span id="D3DSTT_UNKNOWN"></span><span id="d3dstt_unknown"></span>**D3DSTT\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="50edc-108">Valeur non initialisée.</span><span class="sxs-lookup"><span data-stu-id="50edc-108">Uninitialized value.</span></span> <span data-ttu-id="50edc-109">La valeur de cet élément est 0 &lt; &lt; D3DSP \_ TEXTURETYPE \_ Shift.</span><span class="sxs-lookup"><span data-stu-id="50edc-109">The value of this element is 0 &lt;&lt; D3DSP\_TEXTURETYPE\_SHIFT.</span></span>

</dd> <dt>

<span data-ttu-id="50edc-110"><span id="D3DSTT_2D"></span><span id="d3dstt_2d"></span>**D3DSTT \_ 2D**</span><span class="sxs-lookup"><span data-stu-id="50edc-110"><span id="D3DSTT_2D"></span><span id="d3dstt_2d"></span>**D3DSTT\_2D**</span></span>
</dt> <dd>

<span data-ttu-id="50edc-111">Déclaration d’une texture 2D.</span><span class="sxs-lookup"><span data-stu-id="50edc-111">Declaring a 2D texture.</span></span> <span data-ttu-id="50edc-112">La valeur de cet élément est 2 &lt; &lt; D3DSP \_ TEXTURETYPE \_ Shift.</span><span class="sxs-lookup"><span data-stu-id="50edc-112">The value of this element is 2 &lt;&lt; D3DSP\_TEXTURETYPE\_SHIFT.</span></span>

</dd> <dt>

<span data-ttu-id="50edc-113"><span id="D3DSTT_CUBE"></span><span id="d3dstt_cube"></span>**\_Cube D3DSTT**</span><span class="sxs-lookup"><span data-stu-id="50edc-113"><span id="D3DSTT_CUBE"></span><span id="d3dstt_cube"></span>**D3DSTT\_CUBE**</span></span>
</dt> <dd>

<span data-ttu-id="50edc-114">Déclaration d’une texture de cube.</span><span class="sxs-lookup"><span data-stu-id="50edc-114">Declaring a cube texture.</span></span> <span data-ttu-id="50edc-115">La valeur de cet élément est 3 &lt; &lt; D3DSP \_ TEXTURETYPE \_ Shift.</span><span class="sxs-lookup"><span data-stu-id="50edc-115">The value of this element is 3 &lt;&lt; D3DSP\_TEXTURETYPE\_SHIFT.</span></span>

</dd> <dt>

<span data-ttu-id="50edc-116"><span id="D3DSTT_VOLUME"></span><span id="d3dstt_volume"></span>**\_Volume D3DSTT**</span><span class="sxs-lookup"><span data-stu-id="50edc-116"><span id="D3DSTT_VOLUME"></span><span id="d3dstt_volume"></span>**D3DSTT\_VOLUME**</span></span>
</dt> <dd>

<span data-ttu-id="50edc-117">Déclaration d’une texture de volume.</span><span class="sxs-lookup"><span data-stu-id="50edc-117">Declaring a volume texture.</span></span> <span data-ttu-id="50edc-118">La valeur de cet élément est 4 &lt; &lt; D3DSP \_ TEXTURETYPE \_ Shift.</span><span class="sxs-lookup"><span data-stu-id="50edc-118">The value of this element is 4 &lt;&lt; D3DSP\_TEXTURETYPE\_SHIFT.</span></span>

</dd> <dt>

<span data-ttu-id="50edc-119"><span id="D3DSTT_FORCE_DWORD"></span><span id="d3dstt_force_dword"></span>**D3DSTT \_ forcer \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="50edc-119"><span id="D3DSTT_FORCE_DWORD"></span><span id="d3dstt_force_dword"></span>**D3DSTT\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="50edc-120">Force cette énumération à se compiler à 32 bits de taille.</span><span class="sxs-lookup"><span data-stu-id="50edc-120">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="50edc-121">Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits.</span><span class="sxs-lookup"><span data-stu-id="50edc-121">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="50edc-122">Cette valeur n'est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="50edc-122">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="50edc-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="50edc-123">Requirements</span></span>



| <span data-ttu-id="50edc-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="50edc-124">Requirement</span></span> | <span data-ttu-id="50edc-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="50edc-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="50edc-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="50edc-126">Header</span></span><br/> | <dl> <span data-ttu-id="50edc-127"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="50edc-127"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50edc-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50edc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50edc-129">Énumérations Direct3D</span><span class="sxs-lookup"><span data-stu-id="50edc-129">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




