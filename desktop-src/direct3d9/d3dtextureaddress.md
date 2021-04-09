---
description: Définit des constantes qui décrivent les modes d’adressage de texture pris en charge.
ms.assetid: 5c03c55f-4a74-4b0e-ba05-e4a6582ff47c
title: Énumération D3DTEXTUREADDRESS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTUREADDRESS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 2cb1893541f80efb9bf85ea444b27bebba5dea29
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104043090"
---
# <a name="d3dtextureaddress-enumeration"></a><span data-ttu-id="e1ed8-103">Énumération D3DTEXTUREADDRESS</span><span class="sxs-lookup"><span data-stu-id="e1ed8-103">D3DTEXTUREADDRESS enumeration</span></span>

<span data-ttu-id="e1ed8-104">Définit des constantes qui décrivent les modes d’adressage de texture pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e1ed8-104">Defines constants that describe the supported texture-addressing modes.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1ed8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e1ed8-105">Syntax</span></span>


```C++
typedef enum D3DTEXTUREADDRESS { 
  D3DTADDRESS_WRAP         = 1,
  D3DTADDRESS_MIRROR       = 2,
  D3DTADDRESS_CLAMP        = 3,
  D3DTADDRESS_BORDER       = 4,
  D3DTADDRESS_MIRRORONCE   = 5,
  D3DTADDRESS_FORCE_DWORD  = 0x7fffffff
} D3DTEXTUREADDRESS, *LPD3DTEXTUREADDRESS;
```



## <a name="constants"></a><span data-ttu-id="e1ed8-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="e1ed8-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e1ed8-107"><span id="D3DTADDRESS_WRAP"></span><span id="d3dtaddress_wrap"></span>**\_Retour à la ligne D3DTADDRESS**</span><span class="sxs-lookup"><span data-stu-id="e1ed8-107"><span id="D3DTADDRESS_WRAP"></span><span id="d3dtaddress_wrap"></span>**D3DTADDRESS\_WRAP**</span></span>
</dt> <dd>

<span data-ttu-id="e1ed8-108">Juxtaposer la texture à chaque jonction d’entier.</span><span class="sxs-lookup"><span data-stu-id="e1ed8-108">Tile the texture at every integer junction.</span></span> <span data-ttu-id="e1ed8-109">Par exemple, pour vos valeurs comprises entre 0 et 3, la texture est répétée trois fois. aucune mise en miroir n’est effectuée.</span><span class="sxs-lookup"><span data-stu-id="e1ed8-109">For example, for u values between 0 and 3, the texture is repeated three times; no mirroring is performed.</span></span>

</dd> <dt>

<span data-ttu-id="e1ed8-110"><span id="D3DTADDRESS_MIRROR"></span><span id="d3dtaddress_mirror"></span>**\_Miroir D3DTADDRESS**</span><span class="sxs-lookup"><span data-stu-id="e1ed8-110"><span id="D3DTADDRESS_MIRROR"></span><span id="d3dtaddress_mirror"></span>**D3DTADDRESS\_MIRROR**</span></span>
</dt> <dd>

<span data-ttu-id="e1ed8-111">Semblable à D3DTADDRESS \_ Wrap, sauf que la texture est retournée à chaque jonction d’entier.</span><span class="sxs-lookup"><span data-stu-id="e1ed8-111">Similar to D3DTADDRESS\_WRAP, except that the texture is flipped at every integer junction.</span></span> <span data-ttu-id="e1ed8-112">pour vos valeurs comprises entre 0 et 1, par exemple, la texture est traitée normalement ; entre 1 et 2, la texture est retournée (en miroir); entre 2 et 3, la texture est à nouveau normale ; et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="e1ed8-112">For u values between 0 and 1, for example, the texture is addressed normally; between 1 and 2, the texture is flipped (mirrored); between 2 and 3, the texture is normal again; and so on.</span></span>

</dd> <dt>

<span data-ttu-id="e1ed8-113"><span id="D3DTADDRESS_CLAMP"></span><span id="d3dtaddress_clamp"></span>**D3DTADDRESS \_ clamp**</span><span class="sxs-lookup"><span data-stu-id="e1ed8-113"><span id="D3DTADDRESS_CLAMP"></span><span id="d3dtaddress_clamp"></span>**D3DTADDRESS\_CLAMP**</span></span>
</dt> <dd>

<span data-ttu-id="e1ed8-114">Les coordonnées de texture en dehors de la plage \[ 0,0, 1,0 \] sont définies sur la couleur de texture à 0,0 ou 1,0, respectivement.</span><span class="sxs-lookup"><span data-stu-id="e1ed8-114">Texture coordinates outside the range \[0.0, 1.0\] are set to the texture color at 0.0 or 1.0, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="e1ed8-115"><span id="D3DTADDRESS_BORDER"></span><span id="d3dtaddress_border"></span>**\_Bordure D3DTADDRESS**</span><span class="sxs-lookup"><span data-stu-id="e1ed8-115"><span id="D3DTADDRESS_BORDER"></span><span id="d3dtaddress_border"></span>**D3DTADDRESS\_BORDER**</span></span>
</dt> <dd>

<span data-ttu-id="e1ed8-116">Les coordonnées de texture en dehors de la plage \[ 0,0, 1,0 \] sont définies sur la couleur de la bordure.</span><span class="sxs-lookup"><span data-stu-id="e1ed8-116">Texture coordinates outside the range \[0.0, 1.0\] are set to the border color.</span></span>

</dd> <dt>

<span data-ttu-id="e1ed8-117"><span id="D3DTADDRESS_MIRRORONCE"></span><span id="d3dtaddress_mirroronce"></span>**D3DTADDRESS \_ MIRRORONCE**</span><span class="sxs-lookup"><span data-stu-id="e1ed8-117"><span id="D3DTADDRESS_MIRRORONCE"></span><span id="d3dtaddress_mirroronce"></span>**D3DTADDRESS\_MIRRORONCE**</span></span>
</dt> <dd>

<span data-ttu-id="e1ed8-118">Semblable à D3DTADDRESS \_ Mirror et D3DTADDRESS \_ clamp.</span><span class="sxs-lookup"><span data-stu-id="e1ed8-118">Similar to D3DTADDRESS\_MIRROR and D3DTADDRESS\_CLAMP.</span></span> <span data-ttu-id="e1ed8-119">Prend la valeur absolue de la coordonnée de texture (par conséquent, la mise en miroir autour de 0), puis attache à la valeur maximale.</span><span class="sxs-lookup"><span data-stu-id="e1ed8-119">Takes the absolute value of the texture coordinate (thus, mirroring around 0), and then clamps to the maximum value.</span></span> <span data-ttu-id="e1ed8-120">L’utilisation la plus courante concerne les textures de volume, où la prise en charge du \_ mode d’adressage de texture MIRRORONCE D3DTADDRESS complet n’est pas nécessaire, mais les données sont symétriques autour de l’axe.</span><span class="sxs-lookup"><span data-stu-id="e1ed8-120">The most common usage is for volume textures, where support for the full D3DTADDRESS\_MIRRORONCE texture-addressing mode is not necessary, but the data is symmetric around the one axis.</span></span>

</dd> <dt>

<span data-ttu-id="e1ed8-121"><span id="D3DTADDRESS_FORCE_DWORD"></span><span id="d3dtaddress_force_dword"></span>**D3DTADDRESS \_ forcer \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="e1ed8-121"><span id="D3DTADDRESS_FORCE_DWORD"></span><span id="d3dtaddress_force_dword"></span>**D3DTADDRESS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="e1ed8-122">Force cette énumération à se compiler à 32 bits de taille.</span><span class="sxs-lookup"><span data-stu-id="e1ed8-122">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="e1ed8-123">Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits.</span><span class="sxs-lookup"><span data-stu-id="e1ed8-123">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="e1ed8-124">Cette valeur n'est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="e1ed8-124">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e1ed8-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e1ed8-125">Requirements</span></span>



| <span data-ttu-id="e1ed8-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e1ed8-126">Requirement</span></span> | <span data-ttu-id="e1ed8-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1ed8-127">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e1ed8-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="e1ed8-128">Header</span></span><br/> | <dl> <span data-ttu-id="e1ed8-129"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1ed8-129"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1ed8-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1ed8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1ed8-131">Énumérations Direct3D</span><span class="sxs-lookup"><span data-stu-id="e1ed8-131">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="e1ed8-132">**D3DSAMPLERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="e1ed8-132">**D3DSAMPLERSTATETYPE**</span></span>](./d3dsamplerstatetype.md)
</dt> </dl>

 

 
