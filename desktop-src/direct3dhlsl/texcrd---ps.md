---
title: texcrd-PS
description: Copie les données de coordonnée de texture du registre d’itérateur de coordonnées de texture source en tant que données de couleur dans le registre de destination.
ms.assetid: b3330d70-6e18-4494-a01c-51f0a282e305
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e1b7bda7ab06c4af43eaa40393d2c5d64b09d9f4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104990924"
---
# <a name="texcrd---ps"></a><span data-ttu-id="1f8cb-103">texcrd-PS</span><span class="sxs-lookup"><span data-stu-id="1f8cb-103">texcrd - ps</span></span>

<span data-ttu-id="1f8cb-104">Copie les données de coordonnée de texture du registre d’itérateur de coordonnées de texture source en tant que données de couleur dans le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="1f8cb-104">Copies texture coordinate data from the source texture coordinate iterator register as color data in the destination register.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f8cb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1f8cb-105">Syntax</span></span>



| <span data-ttu-id="1f8cb-106">texcrd DST, SRC</span><span class="sxs-lookup"><span data-stu-id="1f8cb-106">texcrd dst, src</span></span> |
|-----------------|



 

<span data-ttu-id="1f8cb-107">where</span><span class="sxs-lookup"><span data-stu-id="1f8cb-107">where</span></span>

-   <span data-ttu-id="1f8cb-108">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="1f8cb-108">dst is the destination register.</span></span>
-   <span data-ttu-id="1f8cb-109">SRC est un registre source.</span><span class="sxs-lookup"><span data-stu-id="1f8cb-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f8cb-110">Notes</span><span class="sxs-lookup"><span data-stu-id="1f8cb-110">Remarks</span></span>



| <span data-ttu-id="1f8cb-111">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="1f8cb-111">Pixel shader versions</span></span> | <span data-ttu-id="1f8cb-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="1f8cb-112">1\_1</span></span> | <span data-ttu-id="1f8cb-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="1f8cb-113">1\_2</span></span> | <span data-ttu-id="1f8cb-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="1f8cb-114">1\_3</span></span> | <span data-ttu-id="1f8cb-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="1f8cb-115">1\_4</span></span> | <span data-ttu-id="1f8cb-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="1f8cb-116">2\_0</span></span> | <span data-ttu-id="1f8cb-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="1f8cb-117">2\_x</span></span> | <span data-ttu-id="1f8cb-118">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="1f8cb-118">2\_sw</span></span> | <span data-ttu-id="1f8cb-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="1f8cb-119">3\_0</span></span> | <span data-ttu-id="1f8cb-120">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="1f8cb-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="1f8cb-121">texcrd</span><span class="sxs-lookup"><span data-stu-id="1f8cb-121">texcrd</span></span>                |      |      |      | <span data-ttu-id="1f8cb-122">x</span><span class="sxs-lookup"><span data-stu-id="1f8cb-122">x</span></span>    |      |      |       |      |       |



 

<span data-ttu-id="1f8cb-123">Cette instruction interprète les données de coordonnée comme des données de couleur (RVBA).</span><span class="sxs-lookup"><span data-stu-id="1f8cb-123">This instruction interprets coordinate data as color data (RGBA).</span></span>

<span data-ttu-id="1f8cb-124">Aucune texture n’est échantillonnée par cette instruction.</span><span class="sxs-lookup"><span data-stu-id="1f8cb-124">No texture is sampled by this instruction.</span></span> <span data-ttu-id="1f8cb-125">Seules les coordonnées de texture définies pour cette étape de texture sont pertinentes.</span><span class="sxs-lookup"><span data-stu-id="1f8cb-125">Only texture coordinates set on this texture stage are relevant.</span></span>

<span data-ttu-id="1f8cb-126">Lorsque vous utilisez texcrd, gardez à l’esprit les détails suivants sur la façon dont les données sont copiées du Registre source vers le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="1f8cb-126">When using texcrd, keep in mind the following detail about how data is copied from the source register to the destination register.</span></span> <span data-ttu-id="1f8cb-127">Le registre de coordonnées de texture source (t \# ) contient des données dans la plage \[ D3DCAPS9. MaxTextureRepeat, D3DCAPS9. MaxTextureRepeat \] , tandis que le registre de destination (r \# ) peut contenir des données uniquement dans la plage (probablement plus petite) \[ -D3DCAPS9. PixelShader1xMaxValue, D3DCAPS9. PixelShader1xMaxValue \] .</span><span class="sxs-lookup"><span data-stu-id="1f8cb-127">The source texture coordinate register (t\#) holds data in the range \[-D3DCAPS9.MaxTextureRepeat, D3DCAPS9.MaxTextureRepeat\], while the destination register (r\#) can hold data only in the (likely smaller) range \[-D3DCAPS9.PixelShader1xMaxValue, D3DCAPS9.PixelShader1xMaxValue\].</span></span> <span data-ttu-id="1f8cb-128">Notez que pour le nuanceur de pixels version 1 \_ , D3DCAPS9. PixelShader1xMaxValue doit avoir une valeur minimale de huit.</span><span class="sxs-lookup"><span data-stu-id="1f8cb-128">Note that for pixel shader version 1\_4, D3DCAPS9.PixelShader1xMaxValue must be a minimum of eight.</span></span> <span data-ttu-id="1f8cb-129">L’instruction texcrd, en cours de verrouillage des données sources qui est hors limites du registre de destination, est susceptible de se comporter différemment sur un matériel différent.</span><span class="sxs-lookup"><span data-stu-id="1f8cb-129">The texcrd instruction, in the process of clamping source data that is out of range of the destination register, is likely to behave differently on different hardware.</span></span> <span data-ttu-id="1f8cb-130">Le premier matériel nuanceur de pixels version 1 \_ 4 sur le marché exécutera une bride spéciale pour les valeurs en dehors de la plage.</span><span class="sxs-lookup"><span data-stu-id="1f8cb-130">The first pixel shader version 1\_4 hardware on the market will perform a special clamp for values outside of range.</span></span> <span data-ttu-id="1f8cb-131">Ce collier est conçu pour produire un nombre pouvant tenir dans le registre de destination, mais également pour conserver le comportement d’adressage des textures pour les données hors limites (voir [**D3DTEXTUREADDRESS**](/windows/desktop/direct3d9/d3dtextureaddress)) si les données doivent être utilisées par la suite pour l’échantillonnage de texture.</span><span class="sxs-lookup"><span data-stu-id="1f8cb-131">This clamp is designed to produce a number that can fit into the destination register, but also to preserve texture addressing behavior for out-of-range data (see [**D3DTEXTUREADDRESS**](/windows/desktop/direct3d9/d3dtextureaddress)) if the data were to be subsequently used for texture sampling.</span></span> <span data-ttu-id="1f8cb-132">Toutefois, le nouveau matériel de différents fabricants peut ne pas présenter ce comportement et peut simplement détailler les données en fonction de la plage de registres de destination.</span><span class="sxs-lookup"><span data-stu-id="1f8cb-132">However, new hardware from different manufacturers might not exhibit this behavior and might just chop data to fit the destination register range.</span></span> <span data-ttu-id="1f8cb-133">Par conséquent, le plus sûr en ce qui concerne l’utilisation de nuanceur de pixels version 1 \_ texcrd consiste à fournir des données de coordonnée de texture uniquement dans le nuanceur de pixels qui se trouve déjà dans la plage \[ 8, 8 afin de ne \] pas compter sur la façon dont les brides matérielles s’appuient.</span><span class="sxs-lookup"><span data-stu-id="1f8cb-133">Therefore, the safest course of action when using pixel shader version 1\_4 texcrd is to supply texture coordinate data only into the pixel shader that is already within the range \[-8,8\] so that you do not rely on the way hardware clamps.</span></span>

<span data-ttu-id="1f8cb-134">Contrairement à texcoord \_ , texcrd n’attache pas de valeurs comprises entre 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="1f8cb-134">Unlike texcoord\_, texcrd does not clamp values between 0 and 1.</span></span>

<span data-ttu-id="1f8cb-135">Règles d’utilisation de texcrd :</span><span class="sxs-lookup"><span data-stu-id="1f8cb-135">Rules for using texcrd :</span></span>

1.  <span data-ttu-id="1f8cb-136">Le même modificateur. xyz ou. XYW doit être appliqué à chaque lecture d’un registre t (n) individuel au sein d’une instruction texcrd ou texld.</span><span class="sxs-lookup"><span data-stu-id="1f8cb-136">The same .xyz or .xyw modifier must be applied to every read of an individual t(n) register within a texcrd or texld instruction.</span></span>
2.  <span data-ttu-id="1f8cb-137">Le résultat du quatrième canal de texcrd est unset/non défini dans tous les cas.</span><span class="sxs-lookup"><span data-stu-id="1f8cb-137">The fourth channel result of texcrd is unset/undefined in all cases.</span></span>
3.  <span data-ttu-id="1f8cb-138">Le troisième canal est unset/non défini pour le cas XYW \_ DW.</span><span class="sxs-lookup"><span data-stu-id="1f8cb-138">The third channel is unset/undefined for the xyw\_dw case.</span></span>

## <a name="examples"></a><span data-ttu-id="1f8cb-139">Exemples</span><span class="sxs-lookup"><span data-stu-id="1f8cb-139">Examples</span></span>

<span data-ttu-id="1f8cb-140">L’ensemble complet de syntaxe autorisée pour texcrd, en tenant compte de toutes les combinaisons valides de modificateurs de source/sélecteur et de masque d’écriture de destination, est illustré ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="1f8cb-140">The complete set of allowed syntax for texcrd, taking into account all valid source modifier/selector and destination write mask combinations, is shown below.</span></span> <span data-ttu-id="1f8cb-141">Notez que la notation. RVBA et. XYZW peut être utilisée de façon interchangeable.</span><span class="sxs-lookup"><span data-stu-id="1f8cb-141">Note that the .rgba and .xyzw notation can be used interchangeably.</span></span>

<span data-ttu-id="1f8cb-142">Copie les trois premiers canaux du registre des itérateurs de coordonnées de texture, t (n), dans r (m).</span><span class="sxs-lookup"><span data-stu-id="1f8cb-142">Copies first three channels of texture coordinate iterator register, t(n), into r(m).</span></span> <span data-ttu-id="1f8cb-143">Le quatrième canal de r (m) n’est pas initialisé.</span><span class="sxs-lookup"><span data-stu-id="1f8cb-143">The fourth channel of r(m) is uninitialized.</span></span>


```
texcrd  r(m).rgb, t(n).xyz  

// Produces the same result as the previous instruction
texcrd  r(m).rgb, t(n)
```



<span data-ttu-id="1f8cb-144">Place les premier, deuxième et quatrième composants de t (n) dans les trois premiers canaux de r (m).</span><span class="sxs-lookup"><span data-stu-id="1f8cb-144">Puts first, second, and fourth components of t(n) into first three channels of r(m).</span></span> <span data-ttu-id="1f8cb-145">Le quatrième canal de r (m) n’est pas initialisé.</span><span class="sxs-lookup"><span data-stu-id="1f8cb-145">The fourth channel of r(m) is uninitialized.</span></span>


```
texcrd  r(m).rgb, t(n).xyw
```



<span data-ttu-id="1f8cb-146">Voici un exemple de division projective qui utilise le \_ modificateur DW.</span><span class="sxs-lookup"><span data-stu-id="1f8cb-146">Here is a projective divide example using the \_dw modifier.</span></span>

<span data-ttu-id="1f8cb-147">Cet exemple copie x/w et y/w de t (n) dans les deux premiers canaux de r (m).</span><span class="sxs-lookup"><span data-stu-id="1f8cb-147">This example copies x/w and y/w from t(n) into the first two channels of r(m).</span></span> <span data-ttu-id="1f8cb-148">Les troisième et quatrième canaux de r (m) ne sont pas initialisés.</span><span class="sxs-lookup"><span data-stu-id="1f8cb-148">The third and fourth channels of r(m) are uninitialized.</span></span> <span data-ttu-id="1f8cb-149">Toutes les données précédemment écrites sur le troisième canal de r (m) seront perdues.</span><span class="sxs-lookup"><span data-stu-id="1f8cb-149">Any data previously written to the third channel of r(m) will be lost.</span></span> <span data-ttu-id="1f8cb-150">Les données du quatrième canal r (m) sont perdues en raison du marqueur de phase.</span><span class="sxs-lookup"><span data-stu-id="1f8cb-150">Data in the fourth channel of r(m) is lost due to the phase marker.</span></span> <span data-ttu-id="1f8cb-151">Pour la version 1 \_ 4, l' \_ indicateur D3DTTFF projeté est ignoré.</span><span class="sxs-lookup"><span data-stu-id="1f8cb-151">For version 1\_4, the D3DTTFF\_PROJECTED flag is ignored.</span></span>


```
texcrd  r(m).rg,  t(n)_dw.xyw
```



## <a name="related-topics"></a><span data-ttu-id="1f8cb-152">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1f8cb-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f8cb-153">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="1f8cb-153">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 