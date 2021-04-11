---
description: Les États de l’étape de texture définissent des opérations de texture à plusieurs fusions.
ms.assetid: 87a5a1bb-e748-4c72-8320-ea82250dcc0e
title: Énumération D3DTEXTURESTAGESTATETYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTURESTAGESTATETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 0530f428c9ebf89607fa89509c65ddd336fee293
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211727"
---
# <a name="d3dtexturestagestatetype-enumeration"></a><span data-ttu-id="056b0-103">Énumération D3DTEXTURESTAGESTATETYPE</span><span class="sxs-lookup"><span data-stu-id="056b0-103">D3DTEXTURESTAGESTATETYPE enumeration</span></span>

<span data-ttu-id="056b0-104">Les États de l’étape de texture définissent des opérations de texture à plusieurs fusions.</span><span class="sxs-lookup"><span data-stu-id="056b0-104">Texture stage states define multi-blender texture operations.</span></span> <span data-ttu-id="056b0-105">Certains États de l’échantillonneur configurent le traitement des vertex et un traitement des pixels configuré.</span><span class="sxs-lookup"><span data-stu-id="056b0-105">Some sampler states set up vertex processing, and some set up pixel processing.</span></span> <span data-ttu-id="056b0-106">Les États de l’étape de texture peuvent être enregistrés et restaurés à l’aide de stateblocks (consultez États d' [enregistrement et de restauration des blocs d’État (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span><span class="sxs-lookup"><span data-stu-id="056b0-106">Texture stage states can be saved and restored using stateblocks (see [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span></span>

## <a name="syntax"></a><span data-ttu-id="056b0-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="056b0-107">Syntax</span></span>


```C++
typedef enum D3DTEXTURESTAGESTATETYPE { 
  D3DTSS_COLOROP                = 1,
  D3DTSS_COLORARG1              = 2,
  D3DTSS_COLORARG2              = 3,
  D3DTSS_ALPHAOP                = 4,
  D3DTSS_ALPHAARG1              = 5,
  D3DTSS_ALPHAARG2              = 6,
  D3DTSS_BUMPENVMAT00           = 7,
  D3DTSS_BUMPENVMAT01           = 8,
  D3DTSS_BUMPENVMAT10           = 9,
  D3DTSS_BUMPENVMAT11           = 10,
  D3DTSS_TEXCOORDINDEX          = 11,
  D3DTSS_BUMPENVLSCALE          = 22,
  D3DTSS_BUMPENVLOFFSET         = 23,
  D3DTSS_TEXTURETRANSFORMFLAGS  = 24,
  D3DTSS_COLORARG0              = 26,
  D3DTSS_ALPHAARG0              = 27,
  D3DTSS_RESULTARG              = 28,
  D3DTSS_CONSTANT               = 32,
  D3DTSS_FORCE_DWORD            = 0x7fffffff
} D3DTEXTURESTAGESTATETYPE, *LPD3DTEXTURESTAGESTATETYPE;
```



## <a name="constants"></a><span data-ttu-id="056b0-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="056b0-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="056b0-109"><span id="D3DTSS_COLOROP"></span><span id="d3dtss_colorop"></span>**D3DTSS \_ COLOROP**</span><span class="sxs-lookup"><span data-stu-id="056b0-109"><span id="D3DTSS_COLOROP"></span><span id="d3dtss_colorop"></span>**D3DTSS\_COLOROP**</span></span>
</dt> <dd>

<span data-ttu-id="056b0-110">L’état de la texture-étape est une opération de fusion des couleurs de texture identifiée par un membre du type énuméré [**D3DTEXTUREOP**](./d3dtextureop.md) .</span><span class="sxs-lookup"><span data-stu-id="056b0-110">Texture-stage state is a texture color blending operation identified by one member of the [**D3DTEXTUREOP**](./d3dtextureop.md) enumerated type.</span></span> <span data-ttu-id="056b0-111">La valeur par défaut de la première étape de texture (étape 0) est D3DTOP \_ module. pour toutes les autres étapes, la valeur par défaut est D3DTOP \_ Désactiver.</span><span class="sxs-lookup"><span data-stu-id="056b0-111">The default value for the first texture stage (stage 0) is D3DTOP\_MODULATE; for all other stages the default is D3DTOP\_DISABLE.</span></span>

</dd> <dt>

<span data-ttu-id="056b0-112"><span id="D3DTSS_COLORARG1"></span><span id="d3dtss_colorarg1"></span>**D3DTSS \_ COLORARG1**</span><span class="sxs-lookup"><span data-stu-id="056b0-112"><span id="D3DTSS_COLORARG1"></span><span id="d3dtss_colorarg1"></span>**D3DTSS\_COLORARG1**</span></span>
</dt> <dd>

<span data-ttu-id="056b0-113">L’état de la texture-étape est le premier argument de couleur pour l’étape, identifié par l’un des [D3DTA](d3dta.md).</span><span class="sxs-lookup"><span data-stu-id="056b0-113">Texture-stage state is the first color argument for the stage, identified by one of the [D3DTA](d3dta.md).</span></span> <span data-ttu-id="056b0-114">L’argument par défaut est D3DTA \_ texture.</span><span class="sxs-lookup"><span data-stu-id="056b0-114">The default argument is D3DTA\_TEXTURE.</span></span>

<span data-ttu-id="056b0-115">Spécifiez D3DTA \_ temp pour sélectionner une couleur de registre temporaire pour la lecture ou l’écriture.</span><span class="sxs-lookup"><span data-stu-id="056b0-115">Specify D3DTA\_TEMP to select a temporary register color for read or write.</span></span> <span data-ttu-id="056b0-116">D3DTA \_ temp est pris en charge si la fonctionnalité de l' \_ appareil D3DPMISCCAPS TSSARGTEMP est présente.</span><span class="sxs-lookup"><span data-stu-id="056b0-116">D3DTA\_TEMP is supported if the D3DPMISCCAPS\_TSSARGTEMP device capability is present.</span></span> <span data-ttu-id="056b0-117">La valeur par défaut du Registre est (0,0, 0,0, 0,0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="056b0-117">The default value for the register is (0.0, 0.0, 0.0, 0.0).</span></span>

</dd> <dt>

<span data-ttu-id="056b0-118"><span id="D3DTSS_COLORARG2"></span><span id="d3dtss_colorarg2"></span>**D3DTSS \_ COLORARG2**</span><span class="sxs-lookup"><span data-stu-id="056b0-118"><span id="D3DTSS_COLORARG2"></span><span id="d3dtss_colorarg2"></span>**D3DTSS\_COLORARG2**</span></span>
</dt> <dd>

<span data-ttu-id="056b0-119">L’état de la texture-étape est le deuxième argument de couleur pour l’étape, identifié par [D3DTA](d3dta.md).</span><span class="sxs-lookup"><span data-stu-id="056b0-119">Texture-stage state is the second color argument for the stage, identified by [D3DTA](d3dta.md).</span></span> <span data-ttu-id="056b0-120">L’argument par défaut est D3DTA \_ Current.</span><span class="sxs-lookup"><span data-stu-id="056b0-120">The default argument is D3DTA\_CURRENT.</span></span> <span data-ttu-id="056b0-121">Spécifiez D3DTA \_ temp pour sélectionner une couleur de registre temporaire pour la lecture ou l’écriture.</span><span class="sxs-lookup"><span data-stu-id="056b0-121">Specify D3DTA\_TEMP to select a temporary register color for read or write.</span></span> <span data-ttu-id="056b0-122">D3DTA \_ temp est pris en charge si la fonctionnalité de l' \_ appareil D3DPMISCCAPS TSSARGTEMP est présente.</span><span class="sxs-lookup"><span data-stu-id="056b0-122">D3DTA\_TEMP is supported if the D3DPMISCCAPS\_TSSARGTEMP device capability is present.</span></span> <span data-ttu-id="056b0-123">La valeur par défaut du Registre est (0,0, 0,0, 0,0, 0,0)</span><span class="sxs-lookup"><span data-stu-id="056b0-123">The default value for the register is (0.0, 0.0, 0.0, 0.0)</span></span>

</dd> <dt>

<span data-ttu-id="056b0-124"><span id="D3DTSS_ALPHAOP"></span><span id="d3dtss_alphaop"></span>**D3DTSS \_ ALPHAOP**</span><span class="sxs-lookup"><span data-stu-id="056b0-124"><span id="D3DTSS_ALPHAOP"></span><span id="d3dtss_alphaop"></span>**D3DTSS\_ALPHAOP**</span></span>
</dt> <dd>

<span data-ttu-id="056b0-125">L’état de la texture-étape est une opération de fusion alpha de texture identifiée par un membre du type énuméré [**D3DTEXTUREOP**](./d3dtextureop.md) .</span><span class="sxs-lookup"><span data-stu-id="056b0-125">Texture-stage state is a texture alpha blending operation identified by one member of the [**D3DTEXTUREOP**](./d3dtextureop.md) enumerated type.</span></span> <span data-ttu-id="056b0-126">La valeur par défaut de la première étape de texture (étape 0) est D3DTOP \_ SELECTARG1, et pour toutes les autres étapes, la valeur par défaut est D3DTOP \_ Disable.</span><span class="sxs-lookup"><span data-stu-id="056b0-126">The default value for the first texture stage (stage 0) is D3DTOP\_SELECTARG1, and for all other stages the default is D3DTOP\_DISABLE.</span></span>

</dd> <dt>

<span data-ttu-id="056b0-127"><span id="D3DTSS_ALPHAARG1"></span><span id="d3dtss_alphaarg1"></span>**D3DTSS \_ ALPHAARG1**</span><span class="sxs-lookup"><span data-stu-id="056b0-127"><span id="D3DTSS_ALPHAARG1"></span><span id="d3dtss_alphaarg1"></span>**D3DTSS\_ALPHAARG1**</span></span>
</dt> <dd>

<span data-ttu-id="056b0-128">L’état de la texture-étape est le premier argument alpha pour l’étape, identifié par par [D3DTA](d3dta.md).</span><span class="sxs-lookup"><span data-stu-id="056b0-128">Texture-stage state is the first alpha argument for the stage, identified by by [D3DTA](d3dta.md).</span></span> <span data-ttu-id="056b0-129">L’argument par défaut est D3DTA \_ texture.</span><span class="sxs-lookup"><span data-stu-id="056b0-129">The default argument is D3DTA\_TEXTURE.</span></span> <span data-ttu-id="056b0-130">Si aucune texture n’est définie pour cette étape, l’argument par défaut est D3DTA \_ diffus.</span><span class="sxs-lookup"><span data-stu-id="056b0-130">If no texture is set for this stage, the default argument is D3DTA\_DIFFUSE.</span></span> <span data-ttu-id="056b0-131">Spécifiez D3DTA \_ temp pour sélectionner une couleur de registre temporaire pour la lecture ou l’écriture.</span><span class="sxs-lookup"><span data-stu-id="056b0-131">Specify D3DTA\_TEMP to select a temporary register color for read or write.</span></span> <span data-ttu-id="056b0-132">D3DTA \_ temp est pris en charge si la fonctionnalité de l' \_ appareil D3DPMISCCAPS TSSARGTEMP est présente.</span><span class="sxs-lookup"><span data-stu-id="056b0-132">D3DTA\_TEMP is supported if the D3DPMISCCAPS\_TSSARGTEMP device capability is present.</span></span> <span data-ttu-id="056b0-133">La valeur par défaut du Registre est (0,0, 0,0, 0,0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="056b0-133">The default value for the register is (0.0, 0.0, 0.0, 0.0).</span></span>

</dd> <dt>

<span data-ttu-id="056b0-134"><span id="D3DTSS_ALPHAARG2"></span><span id="d3dtss_alphaarg2"></span>**D3DTSS \_ ALPHAARG2**</span><span class="sxs-lookup"><span data-stu-id="056b0-134"><span id="D3DTSS_ALPHAARG2"></span><span id="d3dtss_alphaarg2"></span>**D3DTSS\_ALPHAARG2**</span></span>
</dt> <dd>

<span data-ttu-id="056b0-135">L’état de la texture-étape est le deuxième argument alpha pour l’étape, identifié par par [D3DTA](d3dta.md).</span><span class="sxs-lookup"><span data-stu-id="056b0-135">Texture-stage state is the second alpha argument for the stage, identified by by [D3DTA](d3dta.md).</span></span> <span data-ttu-id="056b0-136">L’argument par défaut est D3DTA \_ Current.</span><span class="sxs-lookup"><span data-stu-id="056b0-136">The default argument is D3DTA\_CURRENT.</span></span> <span data-ttu-id="056b0-137">Spécifiez D3DTA \_ temp pour sélectionner une couleur de registre temporaire pour la lecture ou l’écriture.</span><span class="sxs-lookup"><span data-stu-id="056b0-137">Specify D3DTA\_TEMP to select a temporary register color for read or write.</span></span> <span data-ttu-id="056b0-138">D3DTA \_ temp est pris en charge si la fonctionnalité de l' \_ appareil D3DPMISCCAPS TSSARGTEMP est présente.</span><span class="sxs-lookup"><span data-stu-id="056b0-138">D3DTA\_TEMP is supported if the D3DPMISCCAPS\_TSSARGTEMP device capability is present.</span></span> <span data-ttu-id="056b0-139">La valeur par défaut du Registre est (0,0, 0,0, 0,0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="056b0-139">The default value for the register is (0.0, 0.0, 0.0, 0.0).</span></span>

</dd> <dt>

<span data-ttu-id="056b0-140"><span id="D3DTSS_BUMPENVMAT00"></span><span id="d3dtss_bumpenvmat00"></span>**D3DTSS \_ BUMPENVMAT00**</span><span class="sxs-lookup"><span data-stu-id="056b0-140"><span id="D3DTSS_BUMPENVMAT00"></span><span id="d3dtss_bumpenvmat00"></span>**D3DTSS\_BUMPENVMAT00**</span></span>
</dt> <dd>

<span data-ttu-id="056b0-141">L’état de la texture-étape est une valeur à virgule flottante pour le \[ \] \[ \] coefficient 0 0 dans une matrice de mappage de relief.</span><span class="sxs-lookup"><span data-stu-id="056b0-141">Texture-stage state is a floating-point value for the \[0\]\[0\] coefficient in a bump-mapping matrix.</span></span> <span data-ttu-id="056b0-142">La valeur par défaut est 0.0.</span><span class="sxs-lookup"><span data-stu-id="056b0-142">The default value is 0.0.</span></span>

</dd> <dt>

<span data-ttu-id="056b0-143"><span id="D3DTSS_BUMPENVMAT01"></span><span id="d3dtss_bumpenvmat01"></span>**D3DTSS \_ BUMPENVMAT01**</span><span class="sxs-lookup"><span data-stu-id="056b0-143"><span id="D3DTSS_BUMPENVMAT01"></span><span id="d3dtss_bumpenvmat01"></span>**D3DTSS\_BUMPENVMAT01**</span></span>
</dt> <dd>

<span data-ttu-id="056b0-144">L’état de la texture-étape est une valeur à virgule flottante pour le \[ \] \[ \] coefficient 0 1 dans une matrice de mappage de relief.</span><span class="sxs-lookup"><span data-stu-id="056b0-144">Texture-stage state is a floating-point value for the \[0\]\[1\] coefficient in a bump-mapping matrix.</span></span> <span data-ttu-id="056b0-145">La valeur par défaut est 0.0.</span><span class="sxs-lookup"><span data-stu-id="056b0-145">The default value is 0.0.</span></span>

</dd> <dt>

<span data-ttu-id="056b0-146"><span id="D3DTSS_BUMPENVMAT10"></span><span id="d3dtss_bumpenvmat10"></span>**D3DTSS \_ BUMPENVMAT10**</span><span class="sxs-lookup"><span data-stu-id="056b0-146"><span id="D3DTSS_BUMPENVMAT10"></span><span id="d3dtss_bumpenvmat10"></span>**D3DTSS\_BUMPENVMAT10**</span></span>
</dt> <dd>

<span data-ttu-id="056b0-147">L’état de la texture-étape est une valeur à virgule flottante pour le \[ \] \[ \] coefficient 1 0 dans une matrice de mappage de relief.</span><span class="sxs-lookup"><span data-stu-id="056b0-147">Texture-stage state is a floating-point value for the \[1\]\[0\] coefficient in a bump-mapping matrix.</span></span> <span data-ttu-id="056b0-148">La valeur par défaut est 0.0.</span><span class="sxs-lookup"><span data-stu-id="056b0-148">The default value is 0.0.</span></span>

</dd> <dt>

<span data-ttu-id="056b0-149"><span id="D3DTSS_BUMPENVMAT11"></span><span id="d3dtss_bumpenvmat11"></span>**D3DTSS \_ BUMPENVMAT11**</span><span class="sxs-lookup"><span data-stu-id="056b0-149"><span id="D3DTSS_BUMPENVMAT11"></span><span id="d3dtss_bumpenvmat11"></span>**D3DTSS\_BUMPENVMAT11**</span></span>
</dt> <dd>

<span data-ttu-id="056b0-150">L’état de la texture-étape est une valeur à virgule flottante pour le \[ \] \[ \] coefficient 1 1 dans une matrice de mappage de relief.</span><span class="sxs-lookup"><span data-stu-id="056b0-150">Texture-stage state is a floating-point value for the \[1\]\[1\] coefficient in a bump-mapping matrix.</span></span> <span data-ttu-id="056b0-151">La valeur par défaut est 0.0.</span><span class="sxs-lookup"><span data-stu-id="056b0-151">The default value is 0.0.</span></span>

</dd> <dt>

<span data-ttu-id="056b0-152"><span id="D3DTSS_TEXCOORDINDEX"></span><span id="d3dtss_texcoordindex"></span>**D3DTSS \_ TEXCOORDINDEX**</span><span class="sxs-lookup"><span data-stu-id="056b0-152"><span id="D3DTSS_TEXCOORDINDEX"></span><span id="d3dtss_texcoordindex"></span>**D3DTSS\_TEXCOORDINDEX**</span></span>
</dt> <dd>

<span data-ttu-id="056b0-153">Index du jeu de coordonnées de texture à utiliser avec cette étape de texture.</span><span class="sxs-lookup"><span data-stu-id="056b0-153">Index of the texture coordinate set to use with this texture stage.</span></span> <span data-ttu-id="056b0-154">Vous pouvez spécifier jusqu’à huit jeux de coordonnées de texture par vertex.</span><span class="sxs-lookup"><span data-stu-id="056b0-154">You can specify up to eight sets of texture coordinates per vertex.</span></span> <span data-ttu-id="056b0-155">Si un vertex n’inclut pas un jeu de coordonnées de texture à l’index spécifié, le système utilise par défaut les coordonnées v et v (0,0).</span><span class="sxs-lookup"><span data-stu-id="056b0-155">If a vertex does not include a set of texture coordinates at the specified index, the system defaults to the u and v coordinates (0,0).</span></span>

<span data-ttu-id="056b0-156">Lors du rendu à l’aide de nuanceurs vertex, l’index des coordonnées de texture de chaque étape doit être défini sur sa valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="056b0-156">When rendering using vertex shaders, each stage's texture coordinate index must be set to its default value.</span></span> <span data-ttu-id="056b0-157">L’index par défaut de chaque étape est égal à l’index de la phase.</span><span class="sxs-lookup"><span data-stu-id="056b0-157">The default index for each stage is equal to the stage index.</span></span> <span data-ttu-id="056b0-158">Définissez cet État sur l’index de base zéro de l’ensemble de coordonnées pour chaque vertex utilisé par cette étape de texture.</span><span class="sxs-lookup"><span data-stu-id="056b0-158">Set this state to the zero-based index of the coordinate set for each vertex that this texture stage uses.</span></span>

<span data-ttu-id="056b0-159">En outre, les applications peuvent inclure, comme logique ou avec l’index en cours de définition, l’une des constantes pour demander que Direct3D génère automatiquement les coordonnées de texture d’entrée pour une transformation de texture.</span><span class="sxs-lookup"><span data-stu-id="056b0-159">Additionally, applications can include, as logical OR with the index being set, one of the constants to request that Direct3D automatically generate the input texture coordinates for a texture transformation.</span></span> <span data-ttu-id="056b0-160">Pour obtenir la liste de toutes les constantes, consultez [D3DTSS \_ TCI](d3dtss-tci.md).</span><span class="sxs-lookup"><span data-stu-id="056b0-160">For a list of all the constants, see [D3DTSS\_TCI](d3dtss-tci.md).</span></span>

<span data-ttu-id="056b0-161">À l’exception de D3DTSS \_ TCI \_ PASSTHRU, qui correspond à zéro, si l’une des valeurs suivantes est incluse avec l’index en cours de définition, le système utilise l’index strictement pour déterminer le mode d’habillage de texture.</span><span class="sxs-lookup"><span data-stu-id="056b0-161">With the exception of D3DTSS\_TCI\_PASSTHRU, which resolves to zero, if any of the following values is included with the index being set, the system uses the index strictly to determine texture wrapping mode.</span></span> <span data-ttu-id="056b0-162">Ces indicateurs sont particulièrement utiles lors de l’exécution d’un mappage d’environnement.</span><span class="sxs-lookup"><span data-stu-id="056b0-162">These flags are most useful when performing environment mapping.</span></span>

</dd> <dt>

<span data-ttu-id="056b0-163"><span id="D3DTSS_BUMPENVLSCALE"></span><span id="d3dtss_bumpenvlscale"></span>**D3DTSS \_ BUMPENVLSCALE**</span><span class="sxs-lookup"><span data-stu-id="056b0-163"><span id="D3DTSS_BUMPENVLSCALE"></span><span id="d3dtss_bumpenvlscale"></span>**D3DTSS\_BUMPENVLSCALE**</span></span>
</dt> <dd>

<span data-ttu-id="056b0-164">Valeur de mise à l’échelle à virgule flottante pour la luminance de la carte de relief.</span><span class="sxs-lookup"><span data-stu-id="056b0-164">Floating-point scale value for bump-map luminance.</span></span> <span data-ttu-id="056b0-165">La valeur par défaut est 0.0.</span><span class="sxs-lookup"><span data-stu-id="056b0-165">The default value is 0.0.</span></span>

</dd> <dt>

<span data-ttu-id="056b0-166"><span id="D3DTSS_BUMPENVLOFFSET"></span><span id="d3dtss_bumpenvloffset"></span>**D3DTSS \_ BUMPENVLOFFSET**</span><span class="sxs-lookup"><span data-stu-id="056b0-166"><span id="D3DTSS_BUMPENVLOFFSET"></span><span id="d3dtss_bumpenvloffset"></span>**D3DTSS\_BUMPENVLOFFSET**</span></span>
</dt> <dd>

<span data-ttu-id="056b0-167">Valeur de décalage à virgule flottante pour la luminance de la carte de relief.</span><span class="sxs-lookup"><span data-stu-id="056b0-167">Floating-point offset value for bump-map luminance.</span></span> <span data-ttu-id="056b0-168">La valeur par défaut est 0.0.</span><span class="sxs-lookup"><span data-stu-id="056b0-168">The default value is 0.0.</span></span>

</dd> <dt>

<span data-ttu-id="056b0-169"><span id="D3DTSS_TEXTURETRANSFORMFLAGS"></span><span id="d3dtss_texturetransformflags"></span>**D3DTSS \_ TEXTURETRANSFORMFLAGS**</span><span class="sxs-lookup"><span data-stu-id="056b0-169"><span id="D3DTSS_TEXTURETRANSFORMFLAGS"></span><span id="d3dtss_texturetransformflags"></span>**D3DTSS\_TEXTURETRANSFORMFLAGS**</span></span>
</dt> <dd>

<span data-ttu-id="056b0-170">Membre du type énuméré [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) qui contrôle la transformation des coordonnées de texture pour cette étape de texture.</span><span class="sxs-lookup"><span data-stu-id="056b0-170">Member of the [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) enumerated type that controls the transformation of texture coordinates for this texture stage.</span></span> <span data-ttu-id="056b0-171">La valeur par défaut est D3DTTFF \_ Disable.</span><span class="sxs-lookup"><span data-stu-id="056b0-171">The default value is D3DTTFF\_DISABLE.</span></span>

</dd> <dt>

<span data-ttu-id="056b0-172"><span id="D3DTSS_COLORARG0"></span><span id="d3dtss_colorarg0"></span>**D3DTSS \_ COLORARG0**</span><span class="sxs-lookup"><span data-stu-id="056b0-172"><span id="D3DTSS_COLORARG0"></span><span id="d3dtss_colorarg0"></span>**D3DTSS\_COLORARG0**</span></span>
</dt> <dd>

<span data-ttu-id="056b0-173">Paramètres du troisième opérande de couleur pour les opérations tripliées (multiplication, ajout et interpolation linéaire), identifiées par [D3DTA](d3dta.md).</span><span class="sxs-lookup"><span data-stu-id="056b0-173">Settings for the third color operand for triadic operations (multiply, add, and linearly interpolate), identified by [D3DTA](d3dta.md).</span></span> <span data-ttu-id="056b0-174">Ce paramètre est pris en charge si les fonctionnalités de l' \_ appareil D3DTEXOPCAPS MULTIPLYADD ou D3DTEXOPCAPS \_ LERP sont présentes.</span><span class="sxs-lookup"><span data-stu-id="056b0-174">This setting is supported if the D3DTEXOPCAPS\_MULTIPLYADD or D3DTEXOPCAPS\_LERP device capabilities are present.</span></span> <span data-ttu-id="056b0-175">L’argument par défaut est D3DTA \_ Current.</span><span class="sxs-lookup"><span data-stu-id="056b0-175">The default argument is D3DTA\_CURRENT.</span></span> <span data-ttu-id="056b0-176">Spécifiez D3DTA \_ temp pour sélectionner une couleur de registre temporaire pour la lecture ou l’écriture.</span><span class="sxs-lookup"><span data-stu-id="056b0-176">Specify D3DTA\_TEMP to select a temporary register color for read or write.</span></span> <span data-ttu-id="056b0-177">D3DTA \_ temp est pris en charge si la fonctionnalité de l' \_ appareil D3DPMISCCAPS TSSARGTEMP est présente.</span><span class="sxs-lookup"><span data-stu-id="056b0-177">D3DTA\_TEMP is supported if the D3DPMISCCAPS\_TSSARGTEMP device capability is present.</span></span> <span data-ttu-id="056b0-178">La valeur par défaut du Registre est (0,0, 0,0, 0,0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="056b0-178">The default value for the register is (0.0, 0.0, 0.0, 0.0).</span></span>

</dd> <dt>

<span data-ttu-id="056b0-179"><span id="D3DTSS_ALPHAARG0"></span><span id="d3dtss_alphaarg0"></span>**D3DTSS \_ ALPHAARG0**</span><span class="sxs-lookup"><span data-stu-id="056b0-179"><span id="D3DTSS_ALPHAARG0"></span><span id="d3dtss_alphaarg0"></span>**D3DTSS\_ALPHAARG0**</span></span>
</dt> <dd>

<span data-ttu-id="056b0-180">Paramètres de l’opérande du sélecteur de canal alpha pour les opérations tripliées (multiplication, ajout et interpolation linéaire), identifiées par [D3DTA](d3dta.md).</span><span class="sxs-lookup"><span data-stu-id="056b0-180">Settings for the alpha channel selector operand for triadic operations (multiply, add, and linearly interpolate), identified by [D3DTA](d3dta.md).</span></span> <span data-ttu-id="056b0-181">Ce paramètre est pris en charge si les fonctionnalités de l' \_ appareil D3DTEXOPCAPS MULTIPLYADD ou D3DTEXOPCAPS \_ LERP sont présentes.</span><span class="sxs-lookup"><span data-stu-id="056b0-181">This setting is supported if the D3DTEXOPCAPS\_MULTIPLYADD or D3DTEXOPCAPS\_LERP device capabilities are present.</span></span> <span data-ttu-id="056b0-182">L’argument par défaut est D3DTA \_ Current.</span><span class="sxs-lookup"><span data-stu-id="056b0-182">The default argument is D3DTA\_CURRENT.</span></span> <span data-ttu-id="056b0-183">Spécifiez D3DTA \_ temp pour sélectionner une couleur de registre temporaire pour la lecture ou l’écriture.</span><span class="sxs-lookup"><span data-stu-id="056b0-183">Specify D3DTA\_TEMP to select a temporary register color for read or write.</span></span> <span data-ttu-id="056b0-184">D3DTA \_ temp est pris en charge si la fonctionnalité de l' \_ appareil D3DPMISCCAPS TSSARGTEMP est présente.</span><span class="sxs-lookup"><span data-stu-id="056b0-184">D3DTA\_TEMP is supported if the D3DPMISCCAPS\_TSSARGTEMP device capability is present.</span></span> <span data-ttu-id="056b0-185">L’argument par défaut est (0,0, 0,0, 0,0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="056b0-185">The default argument is (0.0, 0.0, 0.0, 0.0).</span></span>

</dd> <dt>

<span data-ttu-id="056b0-186"><span id="D3DTSS_RESULTARG"></span><span id="d3dtss_resultarg"></span>**D3DTSS \_ RESULTARG**</span><span class="sxs-lookup"><span data-stu-id="056b0-186"><span id="D3DTSS_RESULTARG"></span><span id="d3dtss_resultarg"></span>**D3DTSS\_RESULTARG**</span></span>
</dt> <dd>

<span data-ttu-id="056b0-187">Paramètre permettant de sélectionner le registre de destination pour le résultat de cette étape, identifié par [D3DTA](d3dta.md).</span><span class="sxs-lookup"><span data-stu-id="056b0-187">Setting to select destination register for the result of this stage, identified by [D3DTA](d3dta.md).</span></span> <span data-ttu-id="056b0-188">Cette valeur peut être définie sur D3DTA \_ Current (valeur par défaut) ou sur D3DTA \_ temp, qui est un registre temporaire unique qui peut être lu dans les étapes suivantes sous forme d’argument d’entrée.</span><span class="sxs-lookup"><span data-stu-id="056b0-188">This value can be set to D3DTA\_CURRENT (the default value) or to D3DTA\_TEMP, which is a single temporary register that can be read into subsequent stages as an input argument.</span></span> <span data-ttu-id="056b0-189">La couleur finale transmise au mélangeur de brouillard et à la mémoire tampon de trame est extraite de D3DTA \_ actuel, de sorte que l’état de la dernière étape de texture active doit être défini pour écrire dans le en cours.</span><span class="sxs-lookup"><span data-stu-id="056b0-189">The final color passed to the fog blender and frame buffer is taken from D3DTA\_CURRENT, so the last active texture stage state must be set to write to current.</span></span> <span data-ttu-id="056b0-190">Ce paramètre est pris en charge si la fonctionnalité de l' \_ appareil D3DPMISCCAPS TSSARGTEMP est présente.</span><span class="sxs-lookup"><span data-stu-id="056b0-190">This setting is supported if the D3DPMISCCAPS\_TSSARGTEMP device capability is present.</span></span>

</dd> <dt>

<span data-ttu-id="056b0-191"><span id="D3DTSS_CONSTANT"></span><span id="d3dtss_constant"></span>**D3DTSS \_ constante)**</span><span class="sxs-lookup"><span data-stu-id="056b0-191"><span id="D3DTSS_CONSTANT"></span><span id="d3dtss_constant"></span>**D3DTSS\_CONSTANT**</span></span>
</dt> <dd>

<span data-ttu-id="056b0-192">Couleur constante par étape.</span><span class="sxs-lookup"><span data-stu-id="056b0-192">Per-stage constant color.</span></span> <span data-ttu-id="056b0-193">Pour savoir si un appareil prend en charge une couleur constante par étape, consultez la \_ constante D3DPMISCCAPS PERSTAGECONSTANT dans [D3DPMISCCAPS](d3dpmisccaps.md).</span><span class="sxs-lookup"><span data-stu-id="056b0-193">To see if a device supports a per-stage constant color, see the D3DPMISCCAPS\_PERSTAGECONSTANT constant in [D3DPMISCCAPS](d3dpmisccaps.md).</span></span> <span data-ttu-id="056b0-194">La \_ constante D3DTSS est utilisée par la \_ constante D3DTA.</span><span class="sxs-lookup"><span data-stu-id="056b0-194">D3DTSS\_CONSTANT is used by D3DTA\_CONSTANT.</span></span> <span data-ttu-id="056b0-195">Consultez [D3DTA](d3dta.md).</span><span class="sxs-lookup"><span data-stu-id="056b0-195">See [D3DTA](d3dta.md).</span></span>

</dd> <dt>

<span data-ttu-id="056b0-196"><span id="D3DTSS_FORCE_DWORD"></span><span id="d3dtss_force_dword"></span>**D3DTSS \_ forcer \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="056b0-196"><span id="D3DTSS_FORCE_DWORD"></span><span id="d3dtss_force_dword"></span>**D3DTSS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="056b0-197">Force cette énumération à se compiler à 32 bits de taille.</span><span class="sxs-lookup"><span data-stu-id="056b0-197">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="056b0-198">Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits.</span><span class="sxs-lookup"><span data-stu-id="056b0-198">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="056b0-199">Cette valeur n'est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="056b0-199">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="056b0-200">Notes</span><span class="sxs-lookup"><span data-stu-id="056b0-200">Remarks</span></span>

<span data-ttu-id="056b0-201">Les membres de ce type énuméré sont utilisés avec les méthodes [**IDirect3DDevice9 :: GetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate) et [**IDirect3DDevice9 :: SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) pour récupérer et définir des valeurs d’état de texture.</span><span class="sxs-lookup"><span data-stu-id="056b0-201">Members of this enumerated type are used with the [**IDirect3DDevice9::GetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate) and [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) methods to retrieve and set texture state values.</span></span>

<span data-ttu-id="056b0-202">La plage de valeurs valide pour les \_ coefficients de matrice de mappage D3DTSS BUMPENVMAT00, D3DTSS \_ BUMPENVMAT01, D3DTSS \_ BUMPENVMAT10 et D3DTSS BUMPENVMAT11 \_ est supérieure ou égale à-8,0 et inférieure à 8,0.</span><span class="sxs-lookup"><span data-stu-id="056b0-202">The valid range of values for the D3DTSS\_BUMPENVMAT00, D3DTSS\_BUMPENVMAT01, D3DTSS\_BUMPENVMAT10, and D3DTSS\_BUMPENVMAT11 bump-mapping matrix coefficients is greater than or equal to -8.0 and less than 8.0.</span></span> <span data-ttu-id="056b0-203">Cette plage, exprimée en notation mathématique, est (-8.0, 8.0).</span><span class="sxs-lookup"><span data-stu-id="056b0-203">This range, expressed in mathematical notation is (-8.0,8.0).</span></span>

## <a name="requirements"></a><span data-ttu-id="056b0-204">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="056b0-204">Requirements</span></span>



| <span data-ttu-id="056b0-205">Condition requise</span><span class="sxs-lookup"><span data-stu-id="056b0-205">Requirement</span></span> | <span data-ttu-id="056b0-206">Valeur</span><span class="sxs-lookup"><span data-stu-id="056b0-206">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="056b0-207">En-tête</span><span class="sxs-lookup"><span data-stu-id="056b0-207">Header</span></span><br/> | <dl> <span data-ttu-id="056b0-208"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="056b0-208"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="056b0-209">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="056b0-209">See also</span></span>

<dl> <dt>

[<span data-ttu-id="056b0-210">Énumérations Direct3D</span><span class="sxs-lookup"><span data-stu-id="056b0-210">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="056b0-211">**IDirect3DDevice9::GetTextureStageState**</span><span class="sxs-lookup"><span data-stu-id="056b0-211">**IDirect3DDevice9::GetTextureStageState**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate)
</dt> <dt>

[<span data-ttu-id="056b0-212">**IDirect3DDevice9::SetTextureStageState**</span><span class="sxs-lookup"><span data-stu-id="056b0-212">**IDirect3DDevice9::SetTextureStageState**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate)
</dt> </dl>

 

 
