---
description: Les États de rendu définissent des États de configuration pour tous les types de traitement des vertex et des pixels.
ms.assetid: 2fd56388-f3bd-409f-876c-ae893840b623
title: Énumération D3DRENDERSTATETYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRENDERSTATETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 2386762eaa45f1eefbccac97723c3ad71c3a76fd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539867"
---
# <a name="d3drenderstatetype-enumeration"></a><span data-ttu-id="a2c35-103">Énumération D3DRENDERSTATETYPE</span><span class="sxs-lookup"><span data-stu-id="a2c35-103">D3DRENDERSTATETYPE enumeration</span></span>

<span data-ttu-id="a2c35-104">Les États de rendu définissent des États de configuration pour tous les types de traitement des vertex et des pixels.</span><span class="sxs-lookup"><span data-stu-id="a2c35-104">Render states define set-up states for all kinds of vertex and pixel processing.</span></span> <span data-ttu-id="a2c35-105">Certains États de rendu configurent le traitement des vertex et un traitement des pixels configuré (voir [États de rendu (Direct3D 9)](render-states.md)).</span><span class="sxs-lookup"><span data-stu-id="a2c35-105">Some render states set up vertex processing, and some set up pixel processing (see [Render States (Direct3D 9)](render-states.md)).</span></span> <span data-ttu-id="a2c35-106">Les États de rendu peuvent être enregistrés et restaurés à l’aide de stateblocks (consultez États de l' [enregistrement et de la restauration des blocs d’État (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span><span class="sxs-lookup"><span data-stu-id="a2c35-106">Render states can be saved and restored using stateblocks (see [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span></span>

## <a name="syntax"></a><span data-ttu-id="a2c35-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a2c35-107">Syntax</span></span>


```C++
typedef enum D3DRENDERSTATETYPE { 
  D3DRS_ZENABLE                     = 7,
  D3DRS_FILLMODE                    = 8,
  D3DRS_SHADEMODE                   = 9,
  D3DRS_ZWRITEENABLE                = 14,
  D3DRS_ALPHATESTENABLE             = 15,
  D3DRS_LASTPIXEL                   = 16,
  D3DRS_SRCBLEND                    = 19,
  D3DRS_DESTBLEND                   = 20,
  D3DRS_CULLMODE                    = 22,
  D3DRS_ZFUNC                       = 23,
  D3DRS_ALPHAREF                    = 24,
  D3DRS_ALPHAFUNC                   = 25,
  D3DRS_DITHERENABLE                = 26,
  D3DRS_ALPHABLENDENABLE            = 27,
  D3DRS_FOGENABLE                   = 28,
  D3DRS_SPECULARENABLE              = 29,
  D3DRS_FOGCOLOR                    = 34,
  D3DRS_FOGTABLEMODE                = 35,
  D3DRS_FOGSTART                    = 36,
  D3DRS_FOGEND                      = 37,
  D3DRS_FOGDENSITY                  = 38,
  D3DRS_RANGEFOGENABLE              = 48,
  D3DRS_STENCILENABLE               = 52,
  D3DRS_STENCILFAIL                 = 53,
  D3DRS_STENCILZFAIL                = 54,
  D3DRS_STENCILPASS                 = 55,
  D3DRS_STENCILFUNC                 = 56,
  D3DRS_STENCILREF                  = 57,
  D3DRS_STENCILMASK                 = 58,
  D3DRS_STENCILWRITEMASK            = 59,
  D3DRS_TEXTUREFACTOR               = 60,
  D3DRS_WRAP0                       = 128,
  D3DRS_WRAP1                       = 129,
  D3DRS_WRAP2                       = 130,
  D3DRS_WRAP3                       = 131,
  D3DRS_WRAP4                       = 132,
  D3DRS_WRAP5                       = 133,
  D3DRS_WRAP6                       = 134,
  D3DRS_WRAP7                       = 135,
  D3DRS_CLIPPING                    = 136,
  D3DRS_LIGHTING                    = 137,
  D3DRS_AMBIENT                     = 139,
  D3DRS_FOGVERTEXMODE               = 140,
  D3DRS_COLORVERTEX                 = 141,
  D3DRS_LOCALVIEWER                 = 142,
  D3DRS_NORMALIZENORMALS            = 143,
  D3DRS_DIFFUSEMATERIALSOURCE       = 145,
  D3DRS_SPECULARMATERIALSOURCE      = 146,
  D3DRS_AMBIENTMATERIALSOURCE       = 147,
  D3DRS_EMISSIVEMATERIALSOURCE      = 148,
  D3DRS_VERTEXBLEND                 = 151,
  D3DRS_CLIPPLANEENABLE             = 152,
  D3DRS_POINTSIZE                   = 154,
  D3DRS_POINTSIZE_MIN               = 155,
  D3DRS_POINTSPRITEENABLE           = 156,
  D3DRS_POINTSCALEENABLE            = 157,
  D3DRS_POINTSCALE_A                = 158,
  D3DRS_POINTSCALE_B                = 159,
  D3DRS_POINTSCALE_C                = 160,
  D3DRS_MULTISAMPLEANTIALIAS        = 161,
  D3DRS_MULTISAMPLEMASK             = 162,
  D3DRS_PATCHEDGESTYLE              = 163,
  D3DRS_DEBUGMONITORTOKEN           = 165,
  D3DRS_POINTSIZE_MAX               = 166,
  D3DRS_INDEXEDVERTEXBLENDENABLE    = 167,
  D3DRS_COLORWRITEENABLE            = 168,
  D3DRS_TWEENFACTOR                 = 170,
  D3DRS_BLENDOP                     = 171,
  D3DRS_POSITIONDEGREE              = 172,
  D3DRS_NORMALDEGREE                = 173,
  D3DRS_SCISSORTESTENABLE           = 174,
  D3DRS_SLOPESCALEDEPTHBIAS         = 175,
  D3DRS_ANTIALIASEDLINEENABLE       = 176,
  D3DRS_MINTESSELLATIONLEVEL        = 178,
  D3DRS_MAXTESSELLATIONLEVEL        = 179,
  D3DRS_ADAPTIVETESS_X              = 180,
  D3DRS_ADAPTIVETESS_Y              = 181,
  D3DRS_ADAPTIVETESS_Z              = 182,
  D3DRS_ADAPTIVETESS_W              = 183,
  D3DRS_ENABLEADAPTIVETESSELLATION  = 184,
  D3DRS_TWOSIDEDSTENCILMODE         = 185,
  D3DRS_CCW_STENCILFAIL             = 186,
  D3DRS_CCW_STENCILZFAIL            = 187,
  D3DRS_CCW_STENCILPASS             = 188,
  D3DRS_CCW_STENCILFUNC             = 189,
  D3DRS_COLORWRITEENABLE1           = 190,
  D3DRS_COLORWRITEENABLE2           = 191,
  D3DRS_COLORWRITEENABLE3           = 192,
  D3DRS_BLENDFACTOR                 = 193,
  D3DRS_SRGBWRITEENABLE             = 194,
  D3DRS_DEPTHBIAS                   = 195,
  D3DRS_WRAP8                       = 198,
  D3DRS_WRAP9                       = 199,
  D3DRS_WRAP10                      = 200,
  D3DRS_WRAP11                      = 201,
  D3DRS_WRAP12                      = 202,
  D3DRS_WRAP13                      = 203,
  D3DRS_WRAP14                      = 204,
  D3DRS_WRAP15                      = 205,
  D3DRS_SEPARATEALPHABLENDENABLE    = 206,
  D3DRS_SRCBLENDALPHA               = 207,
  D3DRS_DESTBLENDALPHA              = 208,
  D3DRS_BLENDOPALPHA                = 209,
  D3DRS_FORCE_DWORD                 = 0x7fffffff
} D3DRENDERSTATETYPE, *LPD3DRENDERSTATETYPE;
```



## <a name="constants"></a><span data-ttu-id="a2c35-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="a2c35-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a2c35-109"><span id="D3DRS_ZENABLE"></span><span id="d3drs_zenable"></span>**D3DRS \_ ZENABLE**</span><span class="sxs-lookup"><span data-stu-id="a2c35-109"><span id="D3DRS_ZENABLE"></span><span id="d3drs_zenable"></span>**D3DRS\_ZENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-110">État de mise en mémoire tampon de profondeur comme un membre du type énuméré [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) .</span><span class="sxs-lookup"><span data-stu-id="a2c35-110">Depth-buffering state as one member of the [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) enumerated type.</span></span> <span data-ttu-id="a2c35-111">Définissez cet État sur D3DZB \_ true pour activer la mise en mémoire tampon z, D3DZB \_ USEW pour activer la mise en mémoire tampon w ou D3DZB \_ false pour désactiver la mise en mémoire tampon de profondeur.</span><span class="sxs-lookup"><span data-stu-id="a2c35-111">Set this state to D3DZB\_TRUE to enable z-buffering, D3DZB\_USEW to enable w-buffering, or D3DZB\_FALSE to disable depth buffering.</span></span>

<span data-ttu-id="a2c35-112">La valeur par défaut de cet état de rendu est D3DZB \_ true si un stencil de profondeur a été créé avec la chaîne de permutation en affectant la valeur **true** au membre EnableAutoDepthStencil de la structure de [**\_ paramètres D3DPRESENT**](d3dpresent-parameters.md) et D3DZB \_ false dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="a2c35-112">The default value for this render state is D3DZB\_TRUE if a depth stencil was created along with the swap chain by setting the EnableAutoDepthStencil member of the [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md) structure to **TRUE**, and D3DZB\_FALSE otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-113"><span id="D3DRS_FILLMODE"></span><span id="d3drs_fillmode"></span>**D3DRS \_ FillMode**</span><span class="sxs-lookup"><span data-stu-id="a2c35-113"><span id="D3DRS_FILLMODE"></span><span id="d3drs_fillmode"></span>**D3DRS\_FILLMODE**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-114">Un ou plusieurs membres du type énuméré [**D3DFILLMODE**](./d3dfillmode.md) .</span><span class="sxs-lookup"><span data-stu-id="a2c35-114">One or more members of the [**D3DFILLMODE**](./d3dfillmode.md) enumerated type.</span></span> <span data-ttu-id="a2c35-115">La valeur par défaut est D3DFILL \_ Solid.</span><span class="sxs-lookup"><span data-stu-id="a2c35-115">The default value is D3DFILL\_SOLID.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-116"><span id="D3DRS_SHADEMODE"></span><span id="d3drs_shademode"></span>**D3DRS \_ SHADEMODE**</span><span class="sxs-lookup"><span data-stu-id="a2c35-116"><span id="D3DRS_SHADEMODE"></span><span id="d3drs_shademode"></span>**D3DRS\_SHADEMODE**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-117">Un ou plusieurs membres du type énuméré [**D3DSHADEMODE**](./d3dshademode.md) .</span><span class="sxs-lookup"><span data-stu-id="a2c35-117">One or more members of the [**D3DSHADEMODE**](./d3dshademode.md) enumerated type.</span></span> <span data-ttu-id="a2c35-118">La valeur par défaut est D3DSHADE \_ Gouraud.</span><span class="sxs-lookup"><span data-stu-id="a2c35-118">The default value is D3DSHADE\_GOURAUD.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-119"><span id="D3DRS_ZWRITEENABLE"></span><span id="d3drs_zwriteenable"></span>**D3DRS \_ ZWRITEENABLE**</span><span class="sxs-lookup"><span data-stu-id="a2c35-119"><span id="D3DRS_ZWRITEENABLE"></span><span id="d3drs_zwriteenable"></span>**D3DRS\_ZWRITEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-120">**True** pour permettre à l’application d’écrire dans le tampon de profondeur.</span><span class="sxs-lookup"><span data-stu-id="a2c35-120">**TRUE** to enable the application to write to the depth buffer.</span></span> <span data-ttu-id="a2c35-121">La valeur par défaut est **true**.</span><span class="sxs-lookup"><span data-stu-id="a2c35-121">The default value is **TRUE**.</span></span> <span data-ttu-id="a2c35-122">Ce membre permet à une application d’empêcher le système de mettre à jour la mémoire tampon de profondeur avec de nouvelles valeurs de profondeur.</span><span class="sxs-lookup"><span data-stu-id="a2c35-122">This member enables an application to prevent the system from updating the depth buffer with new depth values.</span></span> <span data-ttu-id="a2c35-123">Si la **valeur est false**, les comparaisons de profondeur sont toujours effectuées en fonction de l’état de rendu D3DRS \_ ZFUNC, en supposant que la mise en mémoire tampon de profondeur a lieu, mais que les valeurs de profondeur ne sont pas écrites dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="a2c35-123">If **FALSE**, depth comparisons are still made according to the render state D3DRS\_ZFUNC, assuming that depth buffering is taking place, but depth values are not written to the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-124"><span id="D3DRS_ALPHATESTENABLE"></span><span id="d3drs_alphatestenable"></span>**D3DRS \_ ALPHATESTENABLE**</span><span class="sxs-lookup"><span data-stu-id="a2c35-124"><span id="D3DRS_ALPHATESTENABLE"></span><span id="d3drs_alphatestenable"></span>**D3DRS\_ALPHATESTENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-125">**True** pour activer le test alpha par pixel.</span><span class="sxs-lookup"><span data-stu-id="a2c35-125">**TRUE** to enable per pixel alpha testing.</span></span> <span data-ttu-id="a2c35-126">Si le test réussit, le pixel est traité par la mémoire tampon de trame.</span><span class="sxs-lookup"><span data-stu-id="a2c35-126">If the test passes, the pixel is processed by the frame buffer.</span></span> <span data-ttu-id="a2c35-127">Dans le cas contraire, tout le traitement de la mémoire tampon de trame est ignoré pour le pixel.</span><span class="sxs-lookup"><span data-stu-id="a2c35-127">Otherwise, all frame-buffer processing is skipped for the pixel.</span></span>

<span data-ttu-id="a2c35-128">Le test est effectué en comparant la valeur alpha entrante avec la valeur alpha de référence, à l’aide de la fonction de comparaison fournie par l' \_ État de rendu D3DRS ALPHAFUNC.</span><span class="sxs-lookup"><span data-stu-id="a2c35-128">The test is done by comparing the incoming alpha value with the reference alpha value, using the comparison function provided by the D3DRS\_ALPHAFUNC render state.</span></span> <span data-ttu-id="a2c35-129">La valeur alpha de référence est déterminée par la valeur définie pour D3DRS \_ ALPHAREF.</span><span class="sxs-lookup"><span data-stu-id="a2c35-129">The reference alpha value is determined by the value set for D3DRS\_ALPHAREF.</span></span> <span data-ttu-id="a2c35-130">Pour plus d’informations, consultez [État des tests alpha (Direct3D 9)](alpha-testing-state.md).</span><span class="sxs-lookup"><span data-stu-id="a2c35-130">For more information, see [Alpha Testing State (Direct3D 9)](alpha-testing-state.md).</span></span>

<span data-ttu-id="a2c35-131">La valeur par défaut de ce paramètre est **false**.</span><span class="sxs-lookup"><span data-stu-id="a2c35-131">The default value of this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-132"><span id="D3DRS_LASTPIXEL"></span><span id="d3drs_lastpixel"></span>**D3DRS \_ LASTPIXEL**</span><span class="sxs-lookup"><span data-stu-id="a2c35-132"><span id="D3DRS_LASTPIXEL"></span><span id="d3drs_lastpixel"></span>**D3DRS\_LASTPIXEL**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-133">La valeur par défaut est **true**, ce qui permet de dessiner le dernier pixel d’une ligne.</span><span class="sxs-lookup"><span data-stu-id="a2c35-133">The default value is **TRUE**, which enables drawing of the last pixel in a line.</span></span> <span data-ttu-id="a2c35-134">Pour empêcher le dessin du dernier pixel, définissez cette valeur sur **false**.</span><span class="sxs-lookup"><span data-stu-id="a2c35-134">To prevent drawing of the last pixel, set this value to **FALSE**.</span></span> <span data-ttu-id="a2c35-135">Pour plus d’informations, consultez état de la [structure et du remplissage (Direct3D 9)](outline-and-fill-state.md).</span><span class="sxs-lookup"><span data-stu-id="a2c35-135">For more information, see [Outline and Fill State (Direct3D 9)](outline-and-fill-state.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-136"><span id="D3DRS_SRCBLEND"></span><span id="d3drs_srcblend"></span>**D3DRS \_ SRCBLEND**</span><span class="sxs-lookup"><span data-stu-id="a2c35-136"><span id="D3DRS_SRCBLEND"></span><span id="d3drs_srcblend"></span>**D3DRS\_SRCBLEND**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-137">Un membre du type énuméré [**D3DBLEND**](./d3dblend.md) .</span><span class="sxs-lookup"><span data-stu-id="a2c35-137">One member of the [**D3DBLEND**](./d3dblend.md) enumerated type.</span></span> <span data-ttu-id="a2c35-138">La valeur par défaut est D3DBLEND \_ .</span><span class="sxs-lookup"><span data-stu-id="a2c35-138">The default value is D3DBLEND\_ONE.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-139"><span id="D3DRS_DESTBLEND"></span><span id="d3drs_destblend"></span>**D3DRS \_ DESTBLEND**</span><span class="sxs-lookup"><span data-stu-id="a2c35-139"><span id="D3DRS_DESTBLEND"></span><span id="d3drs_destblend"></span>**D3DRS\_DESTBLEND**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-140">Un membre du type énuméré [**D3DBLEND**](./d3dblend.md) .</span><span class="sxs-lookup"><span data-stu-id="a2c35-140">One member of the [**D3DBLEND**](./d3dblend.md) enumerated type.</span></span> <span data-ttu-id="a2c35-141">La valeur par défaut est D3DBLEND \_ zéro.</span><span class="sxs-lookup"><span data-stu-id="a2c35-141">The default value is D3DBLEND\_ZERO.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-142"><span id="D3DRS_CULLMODE"></span><span id="d3drs_cullmode"></span>**D3DRS \_ CULLMODE**</span><span class="sxs-lookup"><span data-stu-id="a2c35-142"><span id="D3DRS_CULLMODE"></span><span id="d3drs_cullmode"></span>**D3DRS\_CULLMODE**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-143">Spécifie la manière dont les triangles d’arrière-plan sont éliminés, si ce n’est pas le cas.</span><span class="sxs-lookup"><span data-stu-id="a2c35-143">Specifies how back-facing triangles are culled, if at all.</span></span> <span data-ttu-id="a2c35-144">Peut être défini sur un membre du type énuméré [**D3DCULL**](./d3dcull.md) .</span><span class="sxs-lookup"><span data-stu-id="a2c35-144">This can be set to one member of the [**D3DCULL**](./d3dcull.md) enumerated type.</span></span> <span data-ttu-id="a2c35-145">La valeur par défaut est D3DCULL \_ CCW.</span><span class="sxs-lookup"><span data-stu-id="a2c35-145">The default value is D3DCULL\_CCW.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-146"><span id="D3DRS_ZFUNC"></span><span id="d3drs_zfunc"></span>**D3DRS \_ ZFUNC**</span><span class="sxs-lookup"><span data-stu-id="a2c35-146"><span id="D3DRS_ZFUNC"></span><span id="d3drs_zfunc"></span>**D3DRS\_ZFUNC**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-147">Un membre du type énuméré [**D3DCMPFUNC**](./d3dcmpfunc.md) .</span><span class="sxs-lookup"><span data-stu-id="a2c35-147">One member of the [**D3DCMPFUNC**](./d3dcmpfunc.md) enumerated type.</span></span> <span data-ttu-id="a2c35-148">La valeur par défaut est D3DCMP \_ LESSEQUAL.</span><span class="sxs-lookup"><span data-stu-id="a2c35-148">The default value is D3DCMP\_LESSEQUAL.</span></span> <span data-ttu-id="a2c35-149">Ce membre permet à une application d’accepter ou de rejeter un pixel, en fonction de sa distance par rapport à l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="a2c35-149">This member enables an application to accept or reject a pixel, based on its distance from the camera.</span></span>

<span data-ttu-id="a2c35-150">La valeur de profondeur du pixel est comparée à la valeur de la mémoire tampon de profondeur.</span><span class="sxs-lookup"><span data-stu-id="a2c35-150">The depth value of the pixel is compared with the depth-buffer value.</span></span> <span data-ttu-id="a2c35-151">Si la valeur de profondeur du pixel passe la fonction de comparaison, le pixel est écrit.</span><span class="sxs-lookup"><span data-stu-id="a2c35-151">If the depth value of the pixel passes the comparison function, the pixel is written.</span></span>

<span data-ttu-id="a2c35-152">La valeur de profondeur est écrite dans le tampon de profondeur uniquement si l’état de rendu est **true**.</span><span class="sxs-lookup"><span data-stu-id="a2c35-152">The depth value is written to the depth buffer only if the render state is **TRUE**.</span></span>

<span data-ttu-id="a2c35-153">Les rastériseurs de logiciels et de nombreux accélérateurs de matériel fonctionnent plus rapidement si le test de profondeur échoue, car il n’est pas nécessaire de filtrer et de moduler la texture si le pixel n’est pas rendu.</span><span class="sxs-lookup"><span data-stu-id="a2c35-153">Software rasterizers and many hardware accelerators work faster if the depth test fails, because there is no need to filter and modulate the texture if the pixel is not going to be rendered.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-154"><span id="D3DRS_ALPHAREF"></span><span id="d3drs_alpharef"></span>**D3DRS \_ ALPHAREF**</span><span class="sxs-lookup"><span data-stu-id="a2c35-154"><span id="D3DRS_ALPHAREF"></span><span id="d3drs_alpharef"></span>**D3DRS\_ALPHAREF**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-155">Valeur qui spécifie une valeur alpha de référence par rapport à laquelle les pixels sont testés lorsque le test alpha est activé.</span><span class="sxs-lookup"><span data-stu-id="a2c35-155">Value that specifies a reference alpha value against which pixels are tested when alpha testing is enabled.</span></span> <span data-ttu-id="a2c35-156">Il s’agit d’une valeur de 8 bits placée dans les 8 bits de poids faible de la valeur de l’état de rendu DWORD.</span><span class="sxs-lookup"><span data-stu-id="a2c35-156">This is an 8-bit value placed in the low 8 bits of the DWORD render-state value.</span></span> <span data-ttu-id="a2c35-157">Les valeurs peuvent être comprises entre 0x00000000 et 0x000000FF.</span><span class="sxs-lookup"><span data-stu-id="a2c35-157">Values can range from 0x00000000 through 0x000000FF.</span></span> <span data-ttu-id="a2c35-158">La valeur par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="a2c35-158">The default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-159"><span id="D3DRS_ALPHAFUNC"></span><span id="d3drs_alphafunc"></span>**D3DRS \_ ALPHAFUNC**</span><span class="sxs-lookup"><span data-stu-id="a2c35-159"><span id="D3DRS_ALPHAFUNC"></span><span id="d3drs_alphafunc"></span>**D3DRS\_ALPHAFUNC**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-160">Un membre du type énuméré [**D3DCMPFUNC**](./d3dcmpfunc.md) .</span><span class="sxs-lookup"><span data-stu-id="a2c35-160">One member of the [**D3DCMPFUNC**](./d3dcmpfunc.md) enumerated type.</span></span> <span data-ttu-id="a2c35-161">La valeur par défaut est D3DCMP \_ Always.</span><span class="sxs-lookup"><span data-stu-id="a2c35-161">The default value is D3DCMP\_ALWAYS.</span></span> <span data-ttu-id="a2c35-162">Ce membre permet à une application d’accepter ou de rejeter un pixel, en fonction de sa valeur alpha.</span><span class="sxs-lookup"><span data-stu-id="a2c35-162">This member enables an application to accept or reject a pixel, based on its alpha value.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-163"><span id="D3DRS_DITHERENABLE"></span><span id="d3drs_ditherenable"></span>**D3DRS \_ DITHERENABLE**</span><span class="sxs-lookup"><span data-stu-id="a2c35-163"><span id="D3DRS_DITHERENABLE"></span><span id="d3drs_ditherenable"></span>**D3DRS\_DITHERENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-164">**True** pour activer le tramage.</span><span class="sxs-lookup"><span data-stu-id="a2c35-164">**TRUE** to enable dithering.</span></span> <span data-ttu-id="a2c35-165">La valeur par défaut est **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="a2c35-165">The default value is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-166"><span id="D3DRS_ALPHABLENDENABLE"></span><span id="d3drs_alphablendenable"></span>**D3DRS \_ ALPHABLENDENABLE**</span><span class="sxs-lookup"><span data-stu-id="a2c35-166"><span id="D3DRS_ALPHABLENDENABLE"></span><span id="d3drs_alphablendenable"></span>**D3DRS\_ALPHABLENDENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-167">**True** pour activer la transparence à contrôle alpha.</span><span class="sxs-lookup"><span data-stu-id="a2c35-167">**TRUE** to enable alpha-blended transparency.</span></span> <span data-ttu-id="a2c35-168">La valeur par défaut est **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="a2c35-168">The default value is **FALSE**.</span></span>

<span data-ttu-id="a2c35-169">Le type de fusion alpha est déterminé par les États de \_ rendu D3DRS SRCBLEND et D3DRS \_ DESTBLEND.</span><span class="sxs-lookup"><span data-stu-id="a2c35-169">The type of alpha blending is determined by the D3DRS\_SRCBLEND and D3DRS\_DESTBLEND render states.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-170"><span id="D3DRS_FOGENABLE"></span><span id="d3drs_fogenable"></span>**D3DRS \_ FOGENABLE**</span><span class="sxs-lookup"><span data-stu-id="a2c35-170"><span id="D3DRS_FOGENABLE"></span><span id="d3drs_fogenable"></span>**D3DRS\_FOGENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-171">**True** pour activer la fusion de brouillard.</span><span class="sxs-lookup"><span data-stu-id="a2c35-171">**TRUE** to enable fog blending.</span></span> <span data-ttu-id="a2c35-172">La valeur par défaut est **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="a2c35-172">The default value is **FALSE**.</span></span> <span data-ttu-id="a2c35-173">Pour plus d’informations sur l’utilisation de la fusion de brouillard, consultez [brouillard](fog.md).</span><span class="sxs-lookup"><span data-stu-id="a2c35-173">For more information about using fog blending, see [Fog](fog.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-174"><span id="D3DRS_SPECULARENABLE"></span><span id="d3drs_specularenable"></span>**D3DRS \_ SpecularEnable**</span><span class="sxs-lookup"><span data-stu-id="a2c35-174"><span id="D3DRS_SPECULARENABLE"></span><span id="d3drs_specularenable"></span>**D3DRS\_SPECULARENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-175">**True** pour activer les surbrillances spéculaires.</span><span class="sxs-lookup"><span data-stu-id="a2c35-175">**TRUE** to enable specular highlights.</span></span> <span data-ttu-id="a2c35-176">La valeur par défaut est **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="a2c35-176">The default value is **FALSE**.</span></span>

<span data-ttu-id="a2c35-177">Les surbrillances spéculaires sont calculées comme si chaque vertex de l’objet allumé se trouve à l’origine de l’objet.</span><span class="sxs-lookup"><span data-stu-id="a2c35-177">Specular highlights are calculated as though every vertex in the object being lit is at the object's origin.</span></span> <span data-ttu-id="a2c35-178">Cela donne les résultats attendus tant que l’objet est modélisé autour de l’origine et que la distance entre la lumière et l’objet est relativement importante.</span><span class="sxs-lookup"><span data-stu-id="a2c35-178">This gives the expected results as long as the object is modeled around the origin and the distance from the light to the object is relatively large.</span></span> <span data-ttu-id="a2c35-179">Dans d’autres cas, les résultats ne sont pas définis.</span><span class="sxs-lookup"><span data-stu-id="a2c35-179">In other cases, the results as undefined.</span></span>

<span data-ttu-id="a2c35-180">Lorsque ce membre a la valeur **true**, la couleur spéculaire est ajoutée à la couleur de base après la cascade de texture, mais avant la fusion alpha.</span><span class="sxs-lookup"><span data-stu-id="a2c35-180">When this member is set to **TRUE**, the specular color is added to the base color after the texture cascade but before alpha blending.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-181"><span id="D3DRS_FOGCOLOR"></span><span id="d3drs_fogcolor"></span>**D3DRS \_ FOGCOLOR**</span><span class="sxs-lookup"><span data-stu-id="a2c35-181"><span id="D3DRS_FOGCOLOR"></span><span id="d3drs_fogcolor"></span>**D3DRS\_FOGCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-182">Valeur dont le type est [**D3DCOLOR**](d3dcolor.md).</span><span class="sxs-lookup"><span data-stu-id="a2c35-182">Value whose type is [**D3DCOLOR**](d3dcolor.md).</span></span> <span data-ttu-id="a2c35-183">La valeur par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="a2c35-183">The default value is 0.</span></span> <span data-ttu-id="a2c35-184">Pour plus d’informations sur la couleur de brouillard, consultez [couleur de brouillard (Direct3D 9)](fog-color.md).</span><span class="sxs-lookup"><span data-stu-id="a2c35-184">For more information about fog color, see [Fog Color (Direct3D 9)](fog-color.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-185"><span id="D3DRS_FOGTABLEMODE"></span><span id="d3drs_fogtablemode"></span>**D3DRS \_ FOGTABLEMODE**</span><span class="sxs-lookup"><span data-stu-id="a2c35-185"><span id="D3DRS_FOGTABLEMODE"></span><span id="d3drs_fogtablemode"></span>**D3DRS\_FOGTABLEMODE**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-186">Formule de brouillard à utiliser pour le brouillard de pixel.</span><span class="sxs-lookup"><span data-stu-id="a2c35-186">The fog formula to be used for pixel fog.</span></span> <span data-ttu-id="a2c35-187">Défini sur l’un des membres du type énuméré [**D3DFOGMODE**](./d3dfogmode.md) .</span><span class="sxs-lookup"><span data-stu-id="a2c35-187">Set to one of the members of the [**D3DFOGMODE**](./d3dfogmode.md) enumerated type.</span></span> <span data-ttu-id="a2c35-188">La valeur par défaut est D3DFOG \_ None.</span><span class="sxs-lookup"><span data-stu-id="a2c35-188">The default value is D3DFOG\_NONE.</span></span> <span data-ttu-id="a2c35-189">Pour plus d’informations sur le brouillard de pixel, consultez la rubrique [brouillard de pixel (Direct3D 9)](pixel-fog.md).</span><span class="sxs-lookup"><span data-stu-id="a2c35-189">For more information about pixel fog, see [Pixel Fog (Direct3D 9)](pixel-fog.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-190"><span id="D3DRS_FOGSTART"></span><span id="d3drs_fogstart"></span>**D3DRS \_ FOGSTART**</span><span class="sxs-lookup"><span data-stu-id="a2c35-190"><span id="D3DRS_FOGSTART"></span><span id="d3drs_fogstart"></span>**D3DRS\_FOGSTART**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-191">Profondeur à laquelle les effets de brouillard de pixel ou de vertex commencent pour le mode de brouillard linéaire.</span><span class="sxs-lookup"><span data-stu-id="a2c35-191">Depth at which pixel or vertex fog effects begin for linear fog mode.</span></span> <span data-ttu-id="a2c35-192">La valeur par défaut est 0.0 f.</span><span class="sxs-lookup"><span data-stu-id="a2c35-192">The default value is 0.0f.</span></span> <span data-ttu-id="a2c35-193">La profondeur est spécifiée dans l’espace universel pour le brouillard de vertex et l’espace \[ de périphérique 0,0, 1,0 \] ou l’espace universel pour le brouillard de pixel.</span><span class="sxs-lookup"><span data-stu-id="a2c35-193">Depth is specified in world space for vertex fog and either device space \[0.0, 1.0\] or world space for pixel fog.</span></span> <span data-ttu-id="a2c35-194">Pour le brouillard de pixel, ces valeurs se trouvent dans l’espace de l’appareil lorsque le système utilise z pour les calculs de brouillard et l’espace universel lorsque le système utilise le brouillard relatif à l’oeil (w-brouillard).</span><span class="sxs-lookup"><span data-stu-id="a2c35-194">For pixel fog, these values are in device space when the system uses z for fog calculations and world-world space when the system is using eye-relative fog (w-fog).</span></span> <span data-ttu-id="a2c35-195">Pour plus d’informations, consultez [paramètres de brouillard (Direct3D 9)](fog-parameters.md) et [profondeur oculaire ou Z](pixel-fog.md).</span><span class="sxs-lookup"><span data-stu-id="a2c35-195">For more information, see [Fog Parameters (Direct3D 9)](fog-parameters.md) and [Eye-Relative vs. Z-based Depth](pixel-fog.md).</span></span>

<span data-ttu-id="a2c35-196">Les valeurs de cet état de rendu sont des valeurs à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="a2c35-196">Values for this render state are floating-point values.</span></span> <span data-ttu-id="a2c35-197">Étant donné que la méthode [**IDirect3DDevice9 :: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accepte les valeurs DWORD, votre application doit effectuer un cast d’une variable qui contient la valeur, comme indiqué dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="a2c35-197">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
pDevice9->SetRenderState(D3DRS_FOGSTART, 
                         *((DWORD*) (&fFogStart)));
```



</dd> <dt>

<span data-ttu-id="a2c35-198"><span id="D3DRS_FOGEND"></span><span id="d3drs_fogend"></span>**D3DRS \_ FOGEND**</span><span class="sxs-lookup"><span data-stu-id="a2c35-198"><span id="D3DRS_FOGEND"></span><span id="d3drs_fogend"></span>**D3DRS\_FOGEND**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-199">Profondeur à laquelle les effets de brouillard de pixel ou de vertex se terminent pour le mode de brouillard linéaire.</span><span class="sxs-lookup"><span data-stu-id="a2c35-199">Depth at which pixel or vertex fog effects end for linear fog mode.</span></span> <span data-ttu-id="a2c35-200">La valeur par défaut est 1,0 f.</span><span class="sxs-lookup"><span data-stu-id="a2c35-200">The default value is 1.0f.</span></span> <span data-ttu-id="a2c35-201">La profondeur est spécifiée dans l’espace universel pour le brouillard de vertex et l’espace \[ de périphérique 0,0, 1,0 \] ou l’espace universel pour le brouillard de pixel.</span><span class="sxs-lookup"><span data-stu-id="a2c35-201">Depth is specified in world space for vertex fog and either device space \[0.0, 1.0\] or world space for pixel fog.</span></span> <span data-ttu-id="a2c35-202">Pour le brouillard de pixel, ces valeurs se trouvent dans l’espace de l’appareil lorsque le système utilise z pour les calculs de brouillard et dans l’espace universel quand le système utilise le brouillard relatif à l’oeil (w-brouillard).</span><span class="sxs-lookup"><span data-stu-id="a2c35-202">For pixel fog, these values are in device space when the system uses z for fog calculations and in world space when the system is using eye-relative fog (w-fog).</span></span> <span data-ttu-id="a2c35-203">Pour plus d’informations, consultez [paramètres de brouillard (Direct3D 9)](fog-parameters.md) et [profondeur oculaire ou Z](pixel-fog.md).</span><span class="sxs-lookup"><span data-stu-id="a2c35-203">For more information, see [Fog Parameters (Direct3D 9)](fog-parameters.md) and [Eye-Relative vs. Z-based Depth](pixel-fog.md).</span></span>

<span data-ttu-id="a2c35-204">Les valeurs de cet état de rendu sont des valeurs à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="a2c35-204">Values for this render state are floating-point values.</span></span> <span data-ttu-id="a2c35-205">Étant donné que la méthode [**IDirect3DDevice9 :: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accepte les valeurs DWORD, votre application doit effectuer un cast d’une variable qui contient la valeur, comme indiqué dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="a2c35-205">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_FOGEND, *((DWORD*) (&fFogEnd)));
```



</dd> <dt>

<span data-ttu-id="a2c35-206"><span id="D3DRS_FOGDENSITY"></span><span id="d3drs_fogdensity"></span>**D3DRS \_ FOGDENSITY**</span><span class="sxs-lookup"><span data-stu-id="a2c35-206"><span id="D3DRS_FOGDENSITY"></span><span id="d3drs_fogdensity"></span>**D3DRS\_FOGDENSITY**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-207">Densité de brouillard pour le brouillard de pixel ou vertex utilisé dans les modes de brouillard exponentiels (D3DFOG \_ exp et D3DFOG \_ EXP2).</span><span class="sxs-lookup"><span data-stu-id="a2c35-207">Fog density for pixel or vertex fog used in the exponential fog modes (D3DFOG\_EXP and D3DFOG\_EXP2).</span></span> <span data-ttu-id="a2c35-208">Les valeurs de densité valides sont comprises entre 0,0 et 1,0.</span><span class="sxs-lookup"><span data-stu-id="a2c35-208">Valid density values range from 0.0 through 1.0.</span></span> <span data-ttu-id="a2c35-209">La valeur par défaut est 1,0.</span><span class="sxs-lookup"><span data-stu-id="a2c35-209">The default value is 1.0.</span></span> <span data-ttu-id="a2c35-210">Pour plus d’informations, consultez [paramètres de brouillard (Direct3D 9)](fog-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a2c35-210">For more information, see [Fog Parameters (Direct3D 9)](fog-parameters.md).</span></span>

<span data-ttu-id="a2c35-211">Les valeurs de cet état de rendu sont des valeurs à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="a2c35-211">Values for this render state are floating-point values.</span></span> <span data-ttu-id="a2c35-212">Étant donné que la méthode [**IDirect3DDevice9 :: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accepte les valeurs DWORD, votre application doit effectuer un cast d’une variable qui contient la valeur, comme indiqué dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="a2c35-212">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
    m_pDevice9->SetRenderState(D3DRS_FOGDENSITY, *((DWORD*) (&fFogDensity)));
```



</dd> <dt>

<span data-ttu-id="a2c35-213"><span id="D3DRS_RANGEFOGENABLE"></span><span id="d3drs_rangefogenable"></span>**D3DRS \_ RANGEFOGENABLE**</span><span class="sxs-lookup"><span data-stu-id="a2c35-213"><span id="D3DRS_RANGEFOGENABLE"></span><span id="d3drs_rangefogenable"></span>**D3DRS\_RANGEFOGENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-214">**True** pour activer le brouillard de vertex basé sur une plage.</span><span class="sxs-lookup"><span data-stu-id="a2c35-214">**TRUE** to enable range-based vertex fog.</span></span> <span data-ttu-id="a2c35-215">La valeur par défaut est **false**, auquel cas le système utilise le brouillard basé sur la profondeur.</span><span class="sxs-lookup"><span data-stu-id="a2c35-215">The default value is **FALSE**, in which case the system uses depth-based fog.</span></span> <span data-ttu-id="a2c35-216">Dans le brouillard basé sur une plage, la distance d’un objet à partir de la visionneuse est utilisée pour calculer les effets de brouillard, et non la profondeur de l’objet (autrement dit, la coordonnée z) dans la scène.</span><span class="sxs-lookup"><span data-stu-id="a2c35-216">In range-based fog, the distance of an object from the viewer is used to compute fog effects, not the depth of the object (that is, the z-coordinate) in the scene.</span></span> <span data-ttu-id="a2c35-217">Dans le brouillard basé sur une plage, toutes les méthodes de brouillard fonctionnent comme d’habitude, sauf qu’elles utilisent la plage au lieu de la profondeur dans les calculs.</span><span class="sxs-lookup"><span data-stu-id="a2c35-217">In range-based fog, all fog methods work as usual, except that they use range instead of depth in the computations.</span></span>

<span data-ttu-id="a2c35-218">La plage est le facteur approprié à utiliser pour les calculs de brouillard, mais la profondeur est couramment utilisée à la place, car la plage prend du temps pour calculer et la profondeur est généralement déjà disponible.</span><span class="sxs-lookup"><span data-stu-id="a2c35-218">Range is the correct factor to use for fog computations, but depth is commonly used instead because range is time-consuming to compute and depth is generally already available.</span></span> <span data-ttu-id="a2c35-219">L’utilisation de Depth pour calculer le brouillard a l’effet indésirable que le fogginess des objets périphériques change à mesure que l’œil de la visionneuse se déplace. dans ce cas, les modifications de profondeur et la plage restent constantes.</span><span class="sxs-lookup"><span data-stu-id="a2c35-219">Using depth to calculate fog has the undesirable effect of having the fogginess of peripheral objects change as the viewer's eye moves - in this case, the depth changes and the range remains constant.</span></span>

<span data-ttu-id="a2c35-220">Étant donné qu’aucun matériel ne prend actuellement en charge le brouillard basé sur une plage par pixel, la correction de plage est proposée uniquement pour le brouillard de vertex.</span><span class="sxs-lookup"><span data-stu-id="a2c35-220">Because no hardware currently supports per-pixel range-based fog, range correction is offered only for vertex fog.</span></span>

<span data-ttu-id="a2c35-221">Pour plus d’informations, consultez la rubrique [brouillard de vertex (Direct3D 9)](vertex-fog.md).</span><span class="sxs-lookup"><span data-stu-id="a2c35-221">For more information, see [Vertex Fog (Direct3D 9)](vertex-fog.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-222"><span id="D3DRS_STENCILENABLE"></span><span id="d3drs_stencilenable"></span>**D3DRS \_ STENCILENABLE**</span><span class="sxs-lookup"><span data-stu-id="a2c35-222"><span id="D3DRS_STENCILENABLE"></span><span id="d3drs_stencilenable"></span>**D3DRS\_STENCILENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-223">**True** pour activer le stencil, ou **false** pour désactiver le stencil.</span><span class="sxs-lookup"><span data-stu-id="a2c35-223">**TRUE** to enable stenciling, or **FALSE** to disable stenciling.</span></span> <span data-ttu-id="a2c35-224">La valeur par défaut est **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="a2c35-224">The default value is **FALSE**.</span></span> <span data-ttu-id="a2c35-225">Pour plus d’informations, consultez [techniques de tampon de stencil (Direct3D 9)](stencil-buffer-techniques.md).</span><span class="sxs-lookup"><span data-stu-id="a2c35-225">For more information, see [Stencil Buffer Techniques (Direct3D 9)](stencil-buffer-techniques.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-226"><span id="D3DRS_STENCILFAIL"></span><span id="d3drs_stencilfail"></span>**D3DRS \_ STENCILFAIL**</span><span class="sxs-lookup"><span data-stu-id="a2c35-226"><span id="D3DRS_STENCILFAIL"></span><span id="d3drs_stencilfail"></span>**D3DRS\_STENCILFAIL**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-227">Opération de stencil à effectuer en cas d’échec du test du stencil.</span><span class="sxs-lookup"><span data-stu-id="a2c35-227">Stencil operation to perform if the stencil test fails.</span></span> <span data-ttu-id="a2c35-228">Les valeurs proviennent du type énuméré [**D3DSTENCILOP**](./d3dstencilop.md) .</span><span class="sxs-lookup"><span data-stu-id="a2c35-228">Values are from the [**D3DSTENCILOP**](./d3dstencilop.md) enumerated type.</span></span> <span data-ttu-id="a2c35-229">La valeur par défaut est D3DSTENCILOP \_ Keep.</span><span class="sxs-lookup"><span data-stu-id="a2c35-229">The default value is D3DSTENCILOP\_KEEP.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-230"><span id="D3DRS_STENCILZFAIL"></span><span id="d3drs_stencilzfail"></span>**D3DRS \_ STENCILZFAIL**</span><span class="sxs-lookup"><span data-stu-id="a2c35-230"><span id="D3DRS_STENCILZFAIL"></span><span id="d3drs_stencilzfail"></span>**D3DRS\_STENCILZFAIL**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-231">Opération de stencil à effectuer si le test de stencil réussit et que le test de profondeur (z-test) échoue.</span><span class="sxs-lookup"><span data-stu-id="a2c35-231">Stencil operation to perform if the stencil test passes and the depth test (z-test) fails.</span></span> <span data-ttu-id="a2c35-232">Les valeurs proviennent du type énuméré [**D3DSTENCILOP**](./d3dstencilop.md) .</span><span class="sxs-lookup"><span data-stu-id="a2c35-232">Values are from the [**D3DSTENCILOP**](./d3dstencilop.md) enumerated type.</span></span> <span data-ttu-id="a2c35-233">La valeur par défaut est D3DSTENCILOP \_ Keep.</span><span class="sxs-lookup"><span data-stu-id="a2c35-233">The default value is D3DSTENCILOP\_KEEP.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-234"><span id="D3DRS_STENCILPASS"></span><span id="d3drs_stencilpass"></span>**D3DRS \_ STENCILPASS**</span><span class="sxs-lookup"><span data-stu-id="a2c35-234"><span id="D3DRS_STENCILPASS"></span><span id="d3drs_stencilpass"></span>**D3DRS\_STENCILPASS**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-235">Opération de stencil à effectuer si le stencil et les tests de profondeur (z) réussissent.</span><span class="sxs-lookup"><span data-stu-id="a2c35-235">Stencil operation to perform if both the stencil and the depth (z) tests pass.</span></span> <span data-ttu-id="a2c35-236">Les valeurs proviennent du type énuméré [**D3DSTENCILOP**](./d3dstencilop.md) .</span><span class="sxs-lookup"><span data-stu-id="a2c35-236">Values are from the [**D3DSTENCILOP**](./d3dstencilop.md) enumerated type.</span></span> <span data-ttu-id="a2c35-237">La valeur par défaut est D3DSTENCILOP \_ Keep.</span><span class="sxs-lookup"><span data-stu-id="a2c35-237">The default value is D3DSTENCILOP\_KEEP.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-238"><span id="D3DRS_STENCILFUNC"></span><span id="d3drs_stencilfunc"></span>**D3DRS \_ STENCILFUNC**</span><span class="sxs-lookup"><span data-stu-id="a2c35-238"><span id="D3DRS_STENCILFUNC"></span><span id="d3drs_stencilfunc"></span>**D3DRS\_STENCILFUNC**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-239">Fonction de comparaison pour le test de stencil.</span><span class="sxs-lookup"><span data-stu-id="a2c35-239">Comparison function for the stencil test.</span></span> <span data-ttu-id="a2c35-240">Les valeurs proviennent du type énuméré [**D3DCMPFUNC**](./d3dcmpfunc.md) .</span><span class="sxs-lookup"><span data-stu-id="a2c35-240">Values are from the [**D3DCMPFUNC**](./d3dcmpfunc.md) enumerated type.</span></span> <span data-ttu-id="a2c35-241">La valeur par défaut est D3DCMP \_ Always.</span><span class="sxs-lookup"><span data-stu-id="a2c35-241">The default value is D3DCMP\_ALWAYS.</span></span>

<span data-ttu-id="a2c35-242">La fonction de comparaison est utilisée pour comparer la valeur de référence à une entrée de tampon de stencil.</span><span class="sxs-lookup"><span data-stu-id="a2c35-242">The comparison function is used to compare the reference value to a stencil buffer entry.</span></span> <span data-ttu-id="a2c35-243">Cette comparaison s’applique uniquement aux bits dans la valeur de référence et à l’entrée de mémoire tampon de stencil qui sont définis dans le masque de stencil (défini par l' \_ État de rendu D3DRS STENCILMASK).</span><span class="sxs-lookup"><span data-stu-id="a2c35-243">This comparison applies only to the bits in the reference value and stencil buffer entry that are set in the stencil mask (set by the D3DRS\_STENCILMASK render state).</span></span> <span data-ttu-id="a2c35-244">Si la **valeur est true**, le test du stencil réussit.</span><span class="sxs-lookup"><span data-stu-id="a2c35-244">If **TRUE**, the stencil test passes.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-245"><span id="D3DRS_STENCILREF"></span><span id="d3drs_stencilref"></span>**D3DRS \_ STENCILREF**</span><span class="sxs-lookup"><span data-stu-id="a2c35-245"><span id="D3DRS_STENCILREF"></span><span id="d3drs_stencilref"></span>**D3DRS\_STENCILREF**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-246">Valeur de référence int pour le test de stencil.</span><span class="sxs-lookup"><span data-stu-id="a2c35-246">An int reference value for the stencil test.</span></span> <span data-ttu-id="a2c35-247">La valeur par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="a2c35-247">The default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-248"><span id="D3DRS_STENCILMASK"></span><span id="d3drs_stencilmask"></span>**D3DRS \_ STENCILMASK**</span><span class="sxs-lookup"><span data-stu-id="a2c35-248"><span id="D3DRS_STENCILMASK"></span><span id="d3drs_stencilmask"></span>**D3DRS\_STENCILMASK**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-249">Masque appliqué à la valeur de référence et à chaque entrée de tampon de stencil pour déterminer les bits significatifs pour le test de stencil.</span><span class="sxs-lookup"><span data-stu-id="a2c35-249">Mask applied to the reference value and each stencil buffer entry to determine the significant bits for the stencil test.</span></span> <span data-ttu-id="a2c35-250">Le masque par défaut est 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="a2c35-250">The default mask is 0xFFFFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-251"><span id="D3DRS_STENCILWRITEMASK"></span><span id="d3drs_stencilwritemask"></span>**D3DRS \_ STENCILWRITEMASK**</span><span class="sxs-lookup"><span data-stu-id="a2c35-251"><span id="D3DRS_STENCILWRITEMASK"></span><span id="d3drs_stencilwritemask"></span>**D3DRS\_STENCILWRITEMASK**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-252">Masque d’écriture appliqué aux valeurs écrites dans la mémoire tampon du stencil.</span><span class="sxs-lookup"><span data-stu-id="a2c35-252">Write mask applied to values written into the stencil buffer.</span></span> <span data-ttu-id="a2c35-253">Le masque par défaut est 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="a2c35-253">The default mask is 0xFFFFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-254"><span id="D3DRS_TEXTUREFACTOR"></span><span id="d3drs_texturefactor"></span>**D3DRS \_ TEXTUREFACTOR**</span><span class="sxs-lookup"><span data-stu-id="a2c35-254"><span id="D3DRS_TEXTUREFACTOR"></span><span id="d3drs_texturefactor"></span>**D3DRS\_TEXTUREFACTOR**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-255">Couleur utilisée pour la fusion de textures multiples avec l' \_ argument D3DTA TFACTOR texture-Blending ou l' \_ opération de fusion de texture D3DTOP BLENDFACTORALPHA.</span><span class="sxs-lookup"><span data-stu-id="a2c35-255">Color used for multiple-texture blending with the D3DTA\_TFACTOR texture-blending argument or the D3DTOP\_BLENDFACTORALPHA texture-blending operation.</span></span> <span data-ttu-id="a2c35-256">La valeur associée est une variable [**D3DCOLOR**](d3dcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="a2c35-256">The associated value is a [**D3DCOLOR**](d3dcolor.md) variable.</span></span> <span data-ttu-id="a2c35-257">La valeur par défaut est opaque white (0xFFFFFFFF).</span><span class="sxs-lookup"><span data-stu-id="a2c35-257">The default value is opaque white (0xFFFFFFFF).</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-258"><span id="D3DRS_WRAP0"></span><span id="d3drs_wrap0"></span>**D3DRS \_ WRAP0**</span><span class="sxs-lookup"><span data-stu-id="a2c35-258"><span id="D3DRS_WRAP0"></span><span id="d3drs_wrap0"></span>**D3DRS\_WRAP0**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-259">Comportement d’habillage de texture pour plusieurs jeux de coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="a2c35-259">Texture-wrapping behavior for multiple sets of texture coordinates.</span></span> <span data-ttu-id="a2c35-260">Les valeurs valides pour cet état de rendu peuvent être n’importe quelle combinaison des D3DWRAPCOORD \_ 0 (ou D3DWRAP \_ U), D3DWRAPCOORD \_ 1 (ou D3DWRAP \_ V), D3DWRAPCOORD \_ 2 (ou D3DWRAP \_ W) et D3DWRAPCOORD \_ 3 indicateurs.</span><span class="sxs-lookup"><span data-stu-id="a2c35-260">Valid values for this render state can be any combination of the D3DWRAPCOORD\_0 (or D3DWRAP\_U), D3DWRAPCOORD\_1 (or D3DWRAP\_V), D3DWRAPCOORD\_2 (or D3DWRAP\_W), and D3DWRAPCOORD\_3 flags.</span></span> <span data-ttu-id="a2c35-261">Cela amène le système à encapsuler dans le sens des premières, deuxième, troisième et quatrième dimensions, parfois appelées directions s, t, r et q, pour une texture donnée.</span><span class="sxs-lookup"><span data-stu-id="a2c35-261">These cause the system to wrap in the direction of the first, second, third, and fourth dimensions, sometimes referred to as the s, t, r, and q directions, for a given texture.</span></span> <span data-ttu-id="a2c35-262">La valeur par défaut de cet état de rendu est 0 (encapsulation désactivée dans toutes les directions).</span><span class="sxs-lookup"><span data-stu-id="a2c35-262">The default value for this render state is 0 (wrapping disabled in all directions).</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-263"><span id="D3DRS_WRAP1"></span><span id="d3drs_wrap1"></span>**D3DRS \_ WRAP1**</span><span class="sxs-lookup"><span data-stu-id="a2c35-263"><span id="D3DRS_WRAP1"></span><span id="d3drs_wrap1"></span>**D3DRS\_WRAP1**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-264">Consultez D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="a2c35-264">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-265"><span id="D3DRS_WRAP2"></span><span id="d3drs_wrap2"></span>**D3DRS \_ WRAP2**</span><span class="sxs-lookup"><span data-stu-id="a2c35-265"><span id="D3DRS_WRAP2"></span><span id="d3drs_wrap2"></span>**D3DRS\_WRAP2**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-266">Consultez D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="a2c35-266">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-267"><span id="D3DRS_WRAP3"></span><span id="d3drs_wrap3"></span>**D3DRS \_ WRAP3**</span><span class="sxs-lookup"><span data-stu-id="a2c35-267"><span id="D3DRS_WRAP3"></span><span id="d3drs_wrap3"></span>**D3DRS\_WRAP3**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-268">Consultez D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="a2c35-268">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-269"><span id="D3DRS_WRAP4"></span><span id="d3drs_wrap4"></span>**D3DRS \_ WRAP4**</span><span class="sxs-lookup"><span data-stu-id="a2c35-269"><span id="D3DRS_WRAP4"></span><span id="d3drs_wrap4"></span>**D3DRS\_WRAP4**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-270">Consultez D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="a2c35-270">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-271"><span id="D3DRS_WRAP5"></span><span id="d3drs_wrap5"></span>**D3DRS \_ WRAP5**</span><span class="sxs-lookup"><span data-stu-id="a2c35-271"><span id="D3DRS_WRAP5"></span><span id="d3drs_wrap5"></span>**D3DRS\_WRAP5**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-272">Consultez D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="a2c35-272">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-273"><span id="D3DRS_WRAP6"></span><span id="d3drs_wrap6"></span>**D3DRS \_ WRAP6**</span><span class="sxs-lookup"><span data-stu-id="a2c35-273"><span id="D3DRS_WRAP6"></span><span id="d3drs_wrap6"></span>**D3DRS\_WRAP6**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-274">Consultez D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="a2c35-274">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-275"><span id="D3DRS_WRAP7"></span><span id="d3drs_wrap7"></span>**D3DRS \_ WRAP7**</span><span class="sxs-lookup"><span data-stu-id="a2c35-275"><span id="D3DRS_WRAP7"></span><span id="d3drs_wrap7"></span>**D3DRS\_WRAP7**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-276">Consultez D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="a2c35-276">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-277"><span id="D3DRS_CLIPPING"></span><span id="d3drs_clipping"></span>**\_Découpage D3DRS**</span><span class="sxs-lookup"><span data-stu-id="a2c35-277"><span id="D3DRS_CLIPPING"></span><span id="d3drs_clipping"></span>**D3DRS\_CLIPPING**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-278">**True** pour activer le découpage primitif par Direct3D, ou **false** pour le désactiver.</span><span class="sxs-lookup"><span data-stu-id="a2c35-278">**TRUE** to enable primitive clipping by Direct3D, or **FALSE** to disable it.</span></span> <span data-ttu-id="a2c35-279">La valeur par défaut est **true**.</span><span class="sxs-lookup"><span data-stu-id="a2c35-279">The default value is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-280"><span id="D3DRS_LIGHTING"></span><span id="d3drs_lighting"></span>**\_Éclairage D3DRS**</span><span class="sxs-lookup"><span data-stu-id="a2c35-280"><span id="D3DRS_LIGHTING"></span><span id="d3drs_lighting"></span>**D3DRS\_LIGHTING**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-281">**True** pour activer l’éclairage Direct3D, ou **false** pour le désactiver.</span><span class="sxs-lookup"><span data-stu-id="a2c35-281">**TRUE** to enable Direct3D lighting, or **FALSE** to disable it.</span></span> <span data-ttu-id="a2c35-282">La valeur par défaut est **true**.</span><span class="sxs-lookup"><span data-stu-id="a2c35-282">The default value is **TRUE**.</span></span> <span data-ttu-id="a2c35-283">Seuls les vertex qui incluent un sommet normal sont correctement allumés ; les vertex qui ne contiennent pas de normales utilisent un produit scalaire de 0 dans tous les calculs d’éclairage.</span><span class="sxs-lookup"><span data-stu-id="a2c35-283">Only vertices that include a vertex normal are properly lit; vertices that do not contain a normal employ a dot product of 0 in all lighting calculations.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-284"><span id="D3DRS_AMBIENT"></span><span id="d3drs_ambient"></span>**D3DRS \_ ambiant**</span><span class="sxs-lookup"><span data-stu-id="a2c35-284"><span id="D3DRS_AMBIENT"></span><span id="d3drs_ambient"></span>**D3DRS\_AMBIENT**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-285">Couleur de l’éclairage ambiant.</span><span class="sxs-lookup"><span data-stu-id="a2c35-285">Ambient light color.</span></span> <span data-ttu-id="a2c35-286">Cette valeur est de type [**D3DCOLOR**](d3dcolor.md).</span><span class="sxs-lookup"><span data-stu-id="a2c35-286">This value is of type [**D3DCOLOR**](d3dcolor.md).</span></span> <span data-ttu-id="a2c35-287">La valeur par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="a2c35-287">The default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-288"><span id="D3DRS_FOGVERTEXMODE"></span><span id="d3drs_fogvertexmode"></span>**D3DRS \_ FOGVERTEXMODE**</span><span class="sxs-lookup"><span data-stu-id="a2c35-288"><span id="D3DRS_FOGVERTEXMODE"></span><span id="d3drs_fogvertexmode"></span>**D3DRS\_FOGVERTEXMODE**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-289">Formule de brouillard à utiliser pour le brouillard de vertex.</span><span class="sxs-lookup"><span data-stu-id="a2c35-289">Fog formula to be used for vertex fog.</span></span> <span data-ttu-id="a2c35-290">Défini sur un membre du type énuméré [**D3DFOGMODE**](./d3dfogmode.md) .</span><span class="sxs-lookup"><span data-stu-id="a2c35-290">Set to one member of the [**D3DFOGMODE**](./d3dfogmode.md) enumerated type.</span></span> <span data-ttu-id="a2c35-291">La valeur par défaut est D3DFOG \_ None.</span><span class="sxs-lookup"><span data-stu-id="a2c35-291">The default value is D3DFOG\_NONE.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-292"><span id="D3DRS_COLORVERTEX"></span><span id="d3drs_colorvertex"></span>**D3DRS \_ COLORVERTEX**</span><span class="sxs-lookup"><span data-stu-id="a2c35-292"><span id="D3DRS_COLORVERTEX"></span><span id="d3drs_colorvertex"></span>**D3DRS\_COLORVERTEX**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-293">**True** pour activer la couleur par vertex ou **false** pour la désactiver.</span><span class="sxs-lookup"><span data-stu-id="a2c35-293">**TRUE** to enable per-vertex color or **FALSE** to disable it.</span></span> <span data-ttu-id="a2c35-294">La valeur par défaut est **true**.</span><span class="sxs-lookup"><span data-stu-id="a2c35-294">The default value is **TRUE**.</span></span> <span data-ttu-id="a2c35-295">L’activation de la couleur par vertex permet au système d’inclure la couleur définie pour les vertex individuels dans ses calculs d’éclairage.</span><span class="sxs-lookup"><span data-stu-id="a2c35-295">Enabling per-vertex color allows the system to include the color defined for individual vertices in its lighting calculations.</span></span>

<span data-ttu-id="a2c35-296">Pour plus d’informations, consultez les États de rendu suivants :</span><span class="sxs-lookup"><span data-stu-id="a2c35-296">For more information, see the following render states:</span></span>

-   <span data-ttu-id="a2c35-297">D3DRS \_ DIFFUSEMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="a2c35-297">D3DRS\_DIFFUSEMATERIALSOURCE</span></span>
-   <span data-ttu-id="a2c35-298">D3DRS \_ SPECULARMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="a2c35-298">D3DRS\_SPECULARMATERIALSOURCE</span></span>
-   <span data-ttu-id="a2c35-299">D3DRS \_ AMBIENTMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="a2c35-299">D3DRS\_AMBIENTMATERIALSOURCE</span></span>
-   <span data-ttu-id="a2c35-300">D3DRS \_ EMISSIVEMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="a2c35-300">D3DRS\_EMISSIVEMATERIALSOURCE</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-301"><span id="D3DRS_LOCALVIEWER"></span><span id="d3drs_localviewer"></span>**D3DRS \_ LOCALVIEWER**</span><span class="sxs-lookup"><span data-stu-id="a2c35-301"><span id="D3DRS_LOCALVIEWER"></span><span id="d3drs_localviewer"></span>**D3DRS\_LOCALVIEWER**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-302">**True** pour activer les surbrillances spéculaires relatives à l’appareil photo, ou **false** pour utiliser les surbrillances spéculaires orthogonales.</span><span class="sxs-lookup"><span data-stu-id="a2c35-302">**TRUE** to enable camera-relative specular highlights, or **FALSE** to use orthogonal specular highlights.</span></span> <span data-ttu-id="a2c35-303">La valeur par défaut est **true**.</span><span class="sxs-lookup"><span data-stu-id="a2c35-303">The default value is **TRUE**.</span></span> <span data-ttu-id="a2c35-304">Les applications qui utilisent la projection orthogonale doivent spécifier **false**.</span><span class="sxs-lookup"><span data-stu-id="a2c35-304">Applications that use orthogonal projection should specify **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-305"><span id="D3DRS_NORMALIZENORMALS"></span><span id="d3drs_normalizenormals"></span>**D3DRS \_ NORMALIZENORMALS**</span><span class="sxs-lookup"><span data-stu-id="a2c35-305"><span id="D3DRS_NORMALIZENORMALS"></span><span id="d3drs_normalizenormals"></span>**D3DRS\_NORMALIZENORMALS**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-306">**True** pour activer la normalisation automatique des normales des sommets, ou **false** pour la désactiver.</span><span class="sxs-lookup"><span data-stu-id="a2c35-306">**TRUE** to enable automatic normalization of vertex normals, or **FALSE** to disable it.</span></span> <span data-ttu-id="a2c35-307">La valeur par défaut est **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="a2c35-307">The default value is **FALSE**.</span></span> <span data-ttu-id="a2c35-308">L’activation de cette fonctionnalité amène le système à normaliser les normales des vertex pour les vertex après les avoir transformées en espace de caméra, ce qui peut prendre du temps.</span><span class="sxs-lookup"><span data-stu-id="a2c35-308">Enabling this feature causes the system to normalize the vertex normals for vertices after transforming them to camera space, which can be computationally time-consuming.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-309"><span id="D3DRS_DIFFUSEMATERIALSOURCE"></span><span id="d3drs_diffusematerialsource"></span>**D3DRS \_ DIFFUSEMATERIALSOURCE**</span><span class="sxs-lookup"><span data-stu-id="a2c35-309"><span id="D3DRS_DIFFUSEMATERIALSOURCE"></span><span id="d3drs_diffusematerialsource"></span>**D3DRS\_DIFFUSEMATERIALSOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-310">Source de couleur diffuse pour les calculs d’éclairage.</span><span class="sxs-lookup"><span data-stu-id="a2c35-310">Diffuse color source for lighting calculations.</span></span> <span data-ttu-id="a2c35-311">Les valeurs valides sont les membres du type énuméré [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) .</span><span class="sxs-lookup"><span data-stu-id="a2c35-311">Valid values are members of the [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) enumerated type.</span></span> <span data-ttu-id="a2c35-312">La valeur par défaut est D3DMCS \_ COLOR1.</span><span class="sxs-lookup"><span data-stu-id="a2c35-312">The default value is D3DMCS\_COLOR1.</span></span> <span data-ttu-id="a2c35-313">La valeur de cet état de rendu est utilisée uniquement si l' \_ État de rendu D3DRS COLORVERTEX est défini sur **true**.</span><span class="sxs-lookup"><span data-stu-id="a2c35-313">The value for this render state is used only if the D3DRS\_COLORVERTEX render state is set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-314"><span id="D3DRS_SPECULARMATERIALSOURCE"></span><span id="d3drs_specularmaterialsource"></span>**D3DRS \_ SPECULARMATERIALSOURCE**</span><span class="sxs-lookup"><span data-stu-id="a2c35-314"><span id="D3DRS_SPECULARMATERIALSOURCE"></span><span id="d3drs_specularmaterialsource"></span>**D3DRS\_SPECULARMATERIALSOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-315">Source de couleur spéculaire pour les calculs d’éclairage.</span><span class="sxs-lookup"><span data-stu-id="a2c35-315">Specular color source for lighting calculations.</span></span> <span data-ttu-id="a2c35-316">Les valeurs valides sont les membres du type énuméré [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) .</span><span class="sxs-lookup"><span data-stu-id="a2c35-316">Valid values are members of the [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) enumerated type.</span></span> <span data-ttu-id="a2c35-317">La valeur par défaut est D3DMCS \_ COLOR2.</span><span class="sxs-lookup"><span data-stu-id="a2c35-317">The default value is D3DMCS\_COLOR2.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-318"><span id="D3DRS_AMBIENTMATERIALSOURCE"></span><span id="d3drs_ambientmaterialsource"></span>**D3DRS \_ AMBIENTMATERIALSOURCE**</span><span class="sxs-lookup"><span data-stu-id="a2c35-318"><span id="D3DRS_AMBIENTMATERIALSOURCE"></span><span id="d3drs_ambientmaterialsource"></span>**D3DRS\_AMBIENTMATERIALSOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-319">Source de couleur ambiante pour les calculs d’éclairage.</span><span class="sxs-lookup"><span data-stu-id="a2c35-319">Ambient color source for lighting calculations.</span></span> <span data-ttu-id="a2c35-320">Les valeurs valides sont les membres du type énuméré [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) .</span><span class="sxs-lookup"><span data-stu-id="a2c35-320">Valid values are members of the [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) enumerated type.</span></span> <span data-ttu-id="a2c35-321">La valeur par défaut est D3DMCS \_ Material.</span><span class="sxs-lookup"><span data-stu-id="a2c35-321">The default value is D3DMCS\_MATERIAL.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-322"><span id="D3DRS_EMISSIVEMATERIALSOURCE"></span><span id="d3drs_emissivematerialsource"></span>**D3DRS \_ EMISSIVEMATERIALSOURCE**</span><span class="sxs-lookup"><span data-stu-id="a2c35-322"><span id="D3DRS_EMISSIVEMATERIALSOURCE"></span><span id="d3drs_emissivematerialsource"></span>**D3DRS\_EMISSIVEMATERIALSOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-323">Source de couleur émissif pour les calculs d’éclairage.</span><span class="sxs-lookup"><span data-stu-id="a2c35-323">Emissive color source for lighting calculations.</span></span> <span data-ttu-id="a2c35-324">Les valeurs valides sont les membres du type énuméré [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) .</span><span class="sxs-lookup"><span data-stu-id="a2c35-324">Valid values are members of the [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) enumerated type.</span></span> <span data-ttu-id="a2c35-325">La valeur par défaut est D3DMCS \_ Material.</span><span class="sxs-lookup"><span data-stu-id="a2c35-325">The default value is D3DMCS\_MATERIAL.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-326"><span id="D3DRS_VERTEXBLEND"></span><span id="d3drs_vertexblend"></span>**D3DRS \_ VERTEXBLEND**</span><span class="sxs-lookup"><span data-stu-id="a2c35-326"><span id="D3DRS_VERTEXBLEND"></span><span id="d3drs_vertexblend"></span>**D3DRS\_VERTEXBLEND**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-327">Nombre de matrices à utiliser pour effectuer la fusion géométrique, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="a2c35-327">Number of matrices to use to perform geometry blending, if any.</span></span> <span data-ttu-id="a2c35-328">Les valeurs valides sont les membres du type énuméré [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) .</span><span class="sxs-lookup"><span data-stu-id="a2c35-328">Valid values are members of the [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) enumerated type.</span></span> <span data-ttu-id="a2c35-329">La valeur par défaut est D3DVBF \_ Disable.</span><span class="sxs-lookup"><span data-stu-id="a2c35-329">The default value is D3DVBF\_DISABLE.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-330"><span id="D3DRS_CLIPPLANEENABLE"></span><span id="d3drs_clipplaneenable"></span>**D3DRS \_ CLIPPLANEENABLE**</span><span class="sxs-lookup"><span data-stu-id="a2c35-330"><span id="D3DRS_CLIPPLANEENABLE"></span><span id="d3drs_clipplaneenable"></span>**D3DRS\_CLIPPLANEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-331">Active ou désactive les plans de découpage définis par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a2c35-331">Enables or disables user-defined clipping planes.</span></span> <span data-ttu-id="a2c35-332">Les valeurs valides sont n’importe quelle valeur DWORD dans laquelle l’état de chaque bit (défini ou non défini) active ou désactive l’état d’activation d’un plan de découpage défini par l’utilisateur correspondant.</span><span class="sxs-lookup"><span data-stu-id="a2c35-332">Valid values are any DWORD in which the status of each bit (set or not set) toggles the activation state of a corresponding user-defined clipping plane.</span></span> <span data-ttu-id="a2c35-333">Le bit le moins significatif (bit 0) contrôle le premier plan de découpage à l’index 0, et les bits suivants contrôlent l’activation des plans de découpage à des index plus élevés.</span><span class="sxs-lookup"><span data-stu-id="a2c35-333">The least significant bit (bit 0) controls the first clipping plane at index 0, and subsequent bits control the activation of clipping planes at higher indexes.</span></span> <span data-ttu-id="a2c35-334">Si un bit est défini, le système applique le plan de découpage approprié pendant le rendu de la scène.</span><span class="sxs-lookup"><span data-stu-id="a2c35-334">If a bit is set, the system applies the appropriate clipping plane during scene rendering.</span></span> <span data-ttu-id="a2c35-335">La valeur par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="a2c35-335">The default value is 0.</span></span>

<span data-ttu-id="a2c35-336">Les macros [**D3DCLIPPLANEn**](d3dclipplanen.md) sont définies pour fournir un moyen pratique d’activer les plans de découpage.</span><span class="sxs-lookup"><span data-stu-id="a2c35-336">The [**D3DCLIPPLANEn**](d3dclipplanen.md) macros are defined to provide a convenient way to enable clipping planes.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-337"><span id="D3DRS_POINTSIZE"></span><span id="d3drs_pointsize"></span>**D3DRS \_ pointe**</span><span class="sxs-lookup"><span data-stu-id="a2c35-337"><span id="D3DRS_POINTSIZE"></span><span id="d3drs_pointsize"></span>**D3DRS\_POINTSIZE**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-338">Valeur flottante qui spécifie la taille à utiliser pour le calcul de la taille du point dans les cas où la taille du point n’est pas spécifiée pour chaque vertex.</span><span class="sxs-lookup"><span data-stu-id="a2c35-338">A float value that specifies the size to use for point size computation in cases where point size is not specified for each vertex.</span></span> <span data-ttu-id="a2c35-339">Cette valeur n’est pas utilisée lorsque le vertex contient une taille de point.</span><span class="sxs-lookup"><span data-stu-id="a2c35-339">This value is not used when the vertex contains point size.</span></span> <span data-ttu-id="a2c35-340">Cette valeur est en unités d’espace d’écran si D3DRS \_ POINTSCALEENABLE a la valeur **false**; sinon, cette valeur est dans les unités d’espace universel.</span><span class="sxs-lookup"><span data-stu-id="a2c35-340">This value is in screen space units if D3DRS\_POINTSCALEENABLE is **FALSE**; otherwise this value is in world space units.</span></span> <span data-ttu-id="a2c35-341">La valeur par défaut est la valeur retournée par un pilote.</span><span class="sxs-lookup"><span data-stu-id="a2c35-341">The default value is the value a driver returns.</span></span> <span data-ttu-id="a2c35-342">Si un pilote retourne 0 ou 1, la valeur par défaut est 64, ce qui permet l’émulation de la taille du point logiciel.</span><span class="sxs-lookup"><span data-stu-id="a2c35-342">If a driver returns 0 or 1, the default value is 64, which allows software point size emulation.</span></span> <span data-ttu-id="a2c35-343">Étant donné que la méthode [**IDirect3DDevice9 :: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accepte les valeurs DWORD, votre application doit effectuer un cast d’une variable qui contient la valeur, comme indiqué dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="a2c35-343">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_POINTSIZE, *((DWORD*)&pointSize));
```



</dd> <dt>

<span data-ttu-id="a2c35-344"><span id="D3DRS_POINTSIZE_MIN"></span><span id="d3drs_pointsize_min"></span>**D3DRS \_ pointe \_ min.**</span><span class="sxs-lookup"><span data-stu-id="a2c35-344"><span id="D3DRS_POINTSIZE_MIN"></span><span id="d3drs_pointsize_min"></span>**D3DRS\_POINTSIZE\_MIN**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-345">Valeur flottante qui spécifie la taille minimale des primitives de point.</span><span class="sxs-lookup"><span data-stu-id="a2c35-345">A float value that specifies the minimum size of point primitives.</span></span> <span data-ttu-id="a2c35-346">Les primitives de point sont ancrées à cette taille pendant le rendu.</span><span class="sxs-lookup"><span data-stu-id="a2c35-346">Point primitives are clamped to this size during rendering.</span></span> <span data-ttu-id="a2c35-347">Si vous définissez cette valeur sur des valeurs inférieures à 1,0, les points qui chutent lorsque le point ne couvre pas un centre de pixels et l’anticrénelage sont désactivés ou rendus avec une intensité réduite lorsque l’anticrénelage est activé.</span><span class="sxs-lookup"><span data-stu-id="a2c35-347">Setting this to values smaller than 1.0 results in points dropping out when the point does not cover a pixel center and antialiasing is disabled or being rendered with reduced intensity when antialiasing is enabled.</span></span> <span data-ttu-id="a2c35-348">La valeur par défaut est 1,0 f.</span><span class="sxs-lookup"><span data-stu-id="a2c35-348">The default value is 1.0f.</span></span> <span data-ttu-id="a2c35-349">La plage de cette valeur est supérieure ou égale à 0.0 f.</span><span class="sxs-lookup"><span data-stu-id="a2c35-349">The range for this value is greater than or equal to 0.0f.</span></span> <span data-ttu-id="a2c35-350">Étant donné que la méthode [**IDirect3DDevice9 :: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accepte les valeurs DWORD, votre application doit effectuer un cast d’une variable qui contient la valeur, comme indiqué dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="a2c35-350">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_POINTSIZE_MIN, *((DWORD*)&pointSizeMin));
```



</dd> <dt>

<span data-ttu-id="a2c35-351"><span id="D3DRS_POINTSPRITEENABLE"></span><span id="d3drs_pointspriteenable"></span>**D3DRS \_ POINTSPRITEENABLE**</span><span class="sxs-lookup"><span data-stu-id="a2c35-351"><span id="D3DRS_POINTSPRITEENABLE"></span><span id="d3drs_pointspriteenable"></span>**D3DRS\_POINTSPRITEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-352">valeur bool.</span><span class="sxs-lookup"><span data-stu-id="a2c35-352">bool value.</span></span> <span data-ttu-id="a2c35-353">Lorsque la **valeur est true**, les coordonnées de texture des primitives de point sont définies de sorte que les textures complètes soient mappées sur chaque point.</span><span class="sxs-lookup"><span data-stu-id="a2c35-353">When **TRUE**, texture coordinates of point primitives are set so that full textures are mapped on each point.</span></span> <span data-ttu-id="a2c35-354">Quand la **valeur est false**, les coordonnées de texture de vertex sont utilisées pour le point entier.</span><span class="sxs-lookup"><span data-stu-id="a2c35-354">When **FALSE**, the vertex texture coordinates are used for the entire point.</span></span> <span data-ttu-id="a2c35-355">La valeur par défaut est **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="a2c35-355">The default value is **FALSE**.</span></span> <span data-ttu-id="a2c35-356">Vous pouvez obtenir des points à un seul pixel de style DirectX 7 en affectant \_ à D3DRS POINTSCALEENABLE la **valeur false** et à D3DRS \_ la valeur 1,0, qui sont les valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="a2c35-356">You can achieve DirectX 7 style single-pixel points by setting D3DRS\_POINTSCALEENABLE to **FALSE** and D3DRS\_POINTSIZE to 1.0, which are the default values.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-357"><span id="D3DRS_POINTSCALEENABLE"></span><span id="d3drs_pointscaleenable"></span>**D3DRS \_ POINTSCALEENABLE**</span><span class="sxs-lookup"><span data-stu-id="a2c35-357"><span id="D3DRS_POINTSCALEENABLE"></span><span id="d3drs_pointscaleenable"></span>**D3DRS\_POINTSCALEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-358">valeur bool qui contrôle le calcul de la taille pour les primitives de point.</span><span class="sxs-lookup"><span data-stu-id="a2c35-358">bool value that controls computation of size for point primitives.</span></span> <span data-ttu-id="a2c35-359">Lorsque la valeur est **true**, la taille du point est interprétée comme une valeur d’espace de caméra et est mise à l’échelle par la fonction distance et la frustum à la mise à l’échelle de l’axe y pour calculer la taille finale du point d’espace d’écran.</span><span class="sxs-lookup"><span data-stu-id="a2c35-359">When **TRUE**, the point size is interpreted as a camera space value and is scaled by the distance function and the frustum to viewport y-axis scaling to compute the final screen-space point size.</span></span> <span data-ttu-id="a2c35-360">Quand la **valeur est false**, la taille du point est interprétée comme un espace à l’écran et utilisée directement.</span><span class="sxs-lookup"><span data-stu-id="a2c35-360">When **FALSE**, the point size is interpreted as screen space and used directly.</span></span> <span data-ttu-id="a2c35-361">La valeur par défaut est **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="a2c35-361">The default value is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-362"><span id="D3DRS_POINTSCALE_A"></span><span id="d3drs_pointscale_a"></span>**D3DRS \_ POINTSCALE \_ A**</span><span class="sxs-lookup"><span data-stu-id="a2c35-362"><span id="D3DRS_POINTSCALE_A"></span><span id="d3drs_pointscale_a"></span>**D3DRS\_POINTSCALE\_A**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-363">Valeur float qui contrôle l’atténuation de la taille basée sur la distance pour les primitives de point.</span><span class="sxs-lookup"><span data-stu-id="a2c35-363">A float value that controls for distance-based size attenuation for point primitives.</span></span> <span data-ttu-id="a2c35-364">Actif uniquement lorsque D3DRS \_ POINTSCALEENABLE a la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="a2c35-364">Active only when D3DRS\_POINTSCALEENABLE is **TRUE**.</span></span> <span data-ttu-id="a2c35-365">La valeur par défaut est 1,0 f.</span><span class="sxs-lookup"><span data-stu-id="a2c35-365">The default value is 1.0f.</span></span> <span data-ttu-id="a2c35-366">La plage de cette valeur est supérieure ou égale à 0.0 f.</span><span class="sxs-lookup"><span data-stu-id="a2c35-366">The range for this value is greater than or equal to 0.0f.</span></span> <span data-ttu-id="a2c35-367">Étant donné que la méthode [**IDirect3DDevice9 :: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accepte les valeurs DWORD, votre application doit effectuer un cast d’une variable qui contient la valeur, comme indiqué dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="a2c35-367">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_POINTSCALE_A, *((DWORD*)&pointScaleA));
```



</dd> <dt>

<span data-ttu-id="a2c35-368"><span id="D3DRS_POINTSCALE_B"></span><span id="d3drs_pointscale_b"></span>**D3DRS \_ POINTSCALE \_ B**</span><span class="sxs-lookup"><span data-stu-id="a2c35-368"><span id="D3DRS_POINTSCALE_B"></span><span id="d3drs_pointscale_b"></span>**D3DRS\_POINTSCALE\_B**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-369">Valeur float qui contrôle l’atténuation de la taille basée sur la distance pour les primitives de point.</span><span class="sxs-lookup"><span data-stu-id="a2c35-369">A float value that controls for distance-based size attenuation for point primitives.</span></span> <span data-ttu-id="a2c35-370">Actif uniquement lorsque D3DRS \_ POINTSCALEENABLE a la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="a2c35-370">Active only when D3DRS\_POINTSCALEENABLE is **TRUE**.</span></span> <span data-ttu-id="a2c35-371">La valeur par défaut est 0.0 f.</span><span class="sxs-lookup"><span data-stu-id="a2c35-371">The default value is 0.0f.</span></span> <span data-ttu-id="a2c35-372">La plage de cette valeur est supérieure ou égale à 0.0 f.</span><span class="sxs-lookup"><span data-stu-id="a2c35-372">The range for this value is greater than or equal to 0.0f.</span></span> <span data-ttu-id="a2c35-373">Étant donné que la méthode [**IDirect3DDevice9 :: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accepte les valeurs DWORD, votre application doit effectuer un cast d’une variable qui contient la valeur, comme indiqué dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="a2c35-373">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_POINTSCALE_B, *((DWORD*)&pointScaleB));
```



</dd> <dt>

<span data-ttu-id="a2c35-374"><span id="D3DRS_POINTSCALE_C"></span><span id="d3drs_pointscale_c"></span>**D3DRS \_ POINTSCALE \_ C**</span><span class="sxs-lookup"><span data-stu-id="a2c35-374"><span id="D3DRS_POINTSCALE_C"></span><span id="d3drs_pointscale_c"></span>**D3DRS\_POINTSCALE\_C**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-375">Valeur float qui contrôle l’atténuation de la taille basée sur la distance pour les primitives de point.</span><span class="sxs-lookup"><span data-stu-id="a2c35-375">A float value that controls for distance-based size attenuation for point primitives.</span></span> <span data-ttu-id="a2c35-376">Actif uniquement lorsque D3DRS \_ POINTSCALEENABLE a la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="a2c35-376">Active only when D3DRS\_POINTSCALEENABLE is **TRUE**.</span></span> <span data-ttu-id="a2c35-377">La valeur par défaut est 0.0 f.</span><span class="sxs-lookup"><span data-stu-id="a2c35-377">The default value is 0.0f.</span></span> <span data-ttu-id="a2c35-378">La plage de cette valeur est supérieure ou égale à 0.0 f.</span><span class="sxs-lookup"><span data-stu-id="a2c35-378">The range for this value is greater than or equal to 0.0f.</span></span> <span data-ttu-id="a2c35-379">Étant donné que la méthode [**IDirect3DDevice9 :: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accepte les valeurs DWORD, votre application doit effectuer un cast d’une variable qui contient la valeur, comme indiqué dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="a2c35-379">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_POINTSCALE_C, *((DWORD*)&pointScaleC));
```



</dd> <dt>

<span data-ttu-id="a2c35-380"><span id="D3DRS_MULTISAMPLEANTIALIAS"></span><span id="d3drs_multisampleantialias"></span>**D3DRS \_ MULTISAMPLEANTIALIAS**</span><span class="sxs-lookup"><span data-stu-id="a2c35-380"><span id="D3DRS_MULTISAMPLEANTIALIAS"></span><span id="d3drs_multisampleantialias"></span>**D3DRS\_MULTISAMPLEANTIALIAS**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-381">valeur booléenne qui détermine la façon dont les échantillons individuels sont calculés lors de l’utilisation d’un tampon de cible de rendu à plusieurs échantillons.</span><span class="sxs-lookup"><span data-stu-id="a2c35-381">bool value that determines how individual samples are computed when using a multisample render-target buffer.</span></span> <span data-ttu-id="a2c35-382">Quand la valeur est **true**, les différents échantillons sont calculés de manière à ce que l’anticrénelage complet soit effectué par échantillonnage à différentes positions d’échantillonnage pour chaque échantillon multiple.</span><span class="sxs-lookup"><span data-stu-id="a2c35-382">When set to **TRUE**, the multiple samples are computed so that full-scene antialiasing is performed by sampling at different sample positions for each multiple sample.</span></span> <span data-ttu-id="a2c35-383">Quand la valeur est **false**, les exemples multiples sont tous écrits avec la même valeur d’échantillon, échantillonnés au centre de pixels, ce qui permet un rendu non-sans alias dans une mémoire tampon d’échantillonnage multiple.</span><span class="sxs-lookup"><span data-stu-id="a2c35-383">When set to **FALSE**, the multiple samples are all written with the same sample value, sampled at the pixel center, which allows non-antialiased rendering to a multisample buffer.</span></span> <span data-ttu-id="a2c35-384">Cet état de rendu n’a aucun effet lors du rendu d’une mémoire tampon d’exemple unique.</span><span class="sxs-lookup"><span data-stu-id="a2c35-384">This render state has no effect when rendering to a single sample buffer.</span></span> <span data-ttu-id="a2c35-385">La valeur par défaut est **true**.</span><span class="sxs-lookup"><span data-stu-id="a2c35-385">The default value is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-386"><span id="D3DRS_MULTISAMPLEMASK"></span><span id="d3drs_multisamplemask"></span>**D3DRS \_ MULTISAMPLEMASK**</span><span class="sxs-lookup"><span data-stu-id="a2c35-386"><span id="D3DRS_MULTISAMPLEMASK"></span><span id="d3drs_multisamplemask"></span>**D3DRS\_MULTISAMPLEMASK**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-387">Chaque bit de ce masque, à partir du bit le moins significatif (LSB), contrôle la modification de l’un des exemples dans une cible de rendu à plusieurs échantillons.</span><span class="sxs-lookup"><span data-stu-id="a2c35-387">Each bit in this mask, starting at the least significant bit (LSB), controls modification of one of the samples in a multisample render target.</span></span> <span data-ttu-id="a2c35-388">Par conséquent, pour une cible de rendu à 8 échantillons, l’octet de poids faible contient les huit exemples d’écriture pour chacun des huit échantillons.</span><span class="sxs-lookup"><span data-stu-id="a2c35-388">Thus, for an 8-sample render target, the low byte contains the eight write enables for each of the eight samples.</span></span> <span data-ttu-id="a2c35-389">Cet état de rendu n’a aucun effet lors du rendu d’une mémoire tampon d’exemple unique.</span><span class="sxs-lookup"><span data-stu-id="a2c35-389">This render state has no effect when rendering to a single sample buffer.</span></span> <span data-ttu-id="a2c35-390">La valeur par défaut est 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="a2c35-390">The default value is 0xFFFFFFFF.</span></span>

<span data-ttu-id="a2c35-391">Cet état de rendu permet l’utilisation d’une mémoire tampon d’exemples en tant que mémoire tampon d’accumulation, en procédant à un rendu multipasse de Geometry où chaque passe met à jour un sous-ensemble d’échantillons.</span><span class="sxs-lookup"><span data-stu-id="a2c35-391">This render state enables use of a multisample buffer as an accumulation buffer, doing multipass rendering of geometry where each pass updates a subset of samples.</span></span>

<span data-ttu-id="a2c35-392">S’il existe n exemples d’échantillonnages et k, l’intensité résultante de l’image rendue doit être k/n.</span><span class="sxs-lookup"><span data-stu-id="a2c35-392">If there are n multisamples and k enabled samples, the resulting intensity of the rendered image should be k/n.</span></span> <span data-ttu-id="a2c35-393">Chaque composant RVB de chaque pixel est pondéré par k/n.</span><span class="sxs-lookup"><span data-stu-id="a2c35-393">Each component RGB of every pixel is factored by k/n.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-394"><span id="D3DRS_PATCHEDGESTYLE"></span><span id="d3drs_patchedgestyle"></span>**D3DRS \_ PATCHEDGESTYLE**</span><span class="sxs-lookup"><span data-stu-id="a2c35-394"><span id="D3DRS_PATCHEDGESTYLE"></span><span id="d3drs_patchedgestyle"></span>**D3DRS\_PATCHEDGESTYLE**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-395">Définit si les bords des correctifs utilisent le pavage de style flottant.</span><span class="sxs-lookup"><span data-stu-id="a2c35-395">Sets whether patch edges will use float style tessellation.</span></span> <span data-ttu-id="a2c35-396">Les valeurs possibles sont définies par le type énuméré [**D3DPATCHEDGESTYLE**](./d3dpatchedgestyle.md) .</span><span class="sxs-lookup"><span data-stu-id="a2c35-396">Possible values are defined by the [**D3DPATCHEDGESTYLE**](./d3dpatchedgestyle.md) enumerated type.</span></span> <span data-ttu-id="a2c35-397">La valeur par défaut est D3DPATCHEDGE \_ discrète.</span><span class="sxs-lookup"><span data-stu-id="a2c35-397">The default value is D3DPATCHEDGE\_DISCRETE.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-398"><span id="D3DRS_DEBUGMONITORTOKEN"></span><span id="d3drs_debugmonitortoken"></span>**D3DRS \_ DEBUGMONITORTOKEN**</span><span class="sxs-lookup"><span data-stu-id="a2c35-398"><span id="D3DRS_DEBUGMONITORTOKEN"></span><span id="d3drs_debugmonitortoken"></span>**D3DRS\_DEBUGMONITORTOKEN**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-399">Défini uniquement pour le débogage de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="a2c35-399">Set only for debugging the monitor.</span></span> <span data-ttu-id="a2c35-400">Les valeurs possibles sont définies par le type énuméré [**D3DDEBUGMONITORTOKENS**](./d3ddebugmonitortokens.md) .</span><span class="sxs-lookup"><span data-stu-id="a2c35-400">Possible values are defined by the [**D3DDEBUGMONITORTOKENS**](./d3ddebugmonitortokens.md) enumerated type.</span></span> <span data-ttu-id="a2c35-401">Notez que si D3DRS \_ DEBUGMONITORTOKEN est défini, l’appel est traité comme la transmission d’un jeton à l’analyse de débogage.</span><span class="sxs-lookup"><span data-stu-id="a2c35-401">Note that if D3DRS\_DEBUGMONITORTOKEN is set, the call is treated as passing a token to the debug monitor.</span></span> <span data-ttu-id="a2c35-402">Par exemple, si-après passage de D3DDMT \_ Enable ou D3DDMT \_ Disable à D3DRS \_ DEBUGMONITORTOKEN-les autres valeurs de jeton sont transmises, l’État (activé ou désactivé) de l’analyse de débogage est toujours conservé.</span><span class="sxs-lookup"><span data-stu-id="a2c35-402">For example, if - after passing D3DDMT\_ENABLE or D3DDMT\_DISABLE to D3DRS\_DEBUGMONITORTOKEN - other token values are passed in, the state (enabled or disabled) of the debug monitor will still persist.</span></span>

<span data-ttu-id="a2c35-403">Cet État est utile uniquement pour les versions Debug.</span><span class="sxs-lookup"><span data-stu-id="a2c35-403">This state is only useful for debug builds.</span></span> <span data-ttu-id="a2c35-404">La valeur par défaut de l’analyse de débogage est D3DDMT \_ activer.</span><span class="sxs-lookup"><span data-stu-id="a2c35-404">The debug monitor defaults to D3DDMT\_ENABLE.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-405"><span id="D3DRS_POINTSIZE_MAX"></span><span id="d3drs_pointsize_max"></span>**D3DRS \_ pointe \_ Max.**</span><span class="sxs-lookup"><span data-stu-id="a2c35-405"><span id="D3DRS_POINTSIZE_MAX"></span><span id="d3drs_pointsize_max"></span>**D3DRS\_POINTSIZE\_MAX**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-406">Valeur flottante qui spécifie la taille maximale à laquelle les points de sprite seront fixés.</span><span class="sxs-lookup"><span data-stu-id="a2c35-406">A float value that specifies the maximum size to which point sprites will be clamped.</span></span> <span data-ttu-id="a2c35-407">La valeur doit être inférieure ou égale au membre MaxPointSize de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) et supérieur ou égal à D3DRS \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="a2c35-407">The value must be less than or equal to the MaxPointSize member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) and greater than or equal to D3DRS\_POINTSIZE\_MIN.</span></span> <span data-ttu-id="a2c35-408">La valeur par défaut est 64,0.</span><span class="sxs-lookup"><span data-stu-id="a2c35-408">The default value is 64.0.</span></span> <span data-ttu-id="a2c35-409">Étant donné que la méthode [**IDirect3DDevice9 :: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accepte les valeurs DWORD, votre application doit effectuer un cast d’une variable qui contient la valeur, comme indiqué dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="a2c35-409">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_PONTSIZE_MAX, *((DWORD*)&pointSizeMax));
```



</dd> <dt>

<span data-ttu-id="a2c35-410"><span id="D3DRS_INDEXEDVERTEXBLENDENABLE"></span><span id="d3drs_indexedvertexblendenable"></span>**D3DRS \_ INDEXEDVERTEXBLENDENABLE**</span><span class="sxs-lookup"><span data-stu-id="a2c35-410"><span id="D3DRS_INDEXEDVERTEXBLENDENABLE"></span><span id="d3drs_indexedvertexblendenable"></span>**D3DRS\_INDEXEDVERTEXBLENDENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-411">valeur booléenne qui active ou désactive la fusion de vertex indexée.</span><span class="sxs-lookup"><span data-stu-id="a2c35-411">bool value that enables or disables indexed vertex blending.</span></span> <span data-ttu-id="a2c35-412">La valeur par défaut est **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="a2c35-412">The default value is **FALSE**.</span></span> <span data-ttu-id="a2c35-413">Lorsque la valeur est **true**, la fusion des vertex indexée est activée.</span><span class="sxs-lookup"><span data-stu-id="a2c35-413">When set to **TRUE**, indexed vertex blending is enabled.</span></span> <span data-ttu-id="a2c35-414">Quand la valeur est **false**, la fusion des vertex indexés est désactivée.</span><span class="sxs-lookup"><span data-stu-id="a2c35-414">When set to **FALSE**, indexed vertex blending is disabled.</span></span> <span data-ttu-id="a2c35-415">Si cet état de rendu est activé, l’utilisateur doit passer des index de matrice comme un DWORDwith compressé tous les vertex.</span><span class="sxs-lookup"><span data-stu-id="a2c35-415">If this render state is enabled, the user must pass matrix indices as a packed DWORDwith every vertex.</span></span> <span data-ttu-id="a2c35-416">Lorsque l’état de rendu est désactivé et que la fusion de vertex est activée par le biais de l' \_ État D3DRS VERTEXBLEND, cela équivaut à avoir des index de matrice 0, 1, 2, 3 dans chaque vertex.</span><span class="sxs-lookup"><span data-stu-id="a2c35-416">When the render state is disabled and vertex blending is enabled through the D3DRS\_VERTEXBLEND state, it is equivalent to having matrix indices 0, 1, 2, 3 in every vertex.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-417"><span id="D3DRS_COLORWRITEENABLE"></span><span id="d3drs_colorwriteenable"></span>**D3DRS \_ COLORWRITEENABLE**</span><span class="sxs-lookup"><span data-stu-id="a2c35-417"><span id="D3DRS_COLORWRITEENABLE"></span><span id="d3drs_colorwriteenable"></span>**D3DRS\_COLORWRITEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-418">Valeur UINT qui active une écriture par canal pour la mémoire tampon de couleur de rendu cible.</span><span class="sxs-lookup"><span data-stu-id="a2c35-418">UINT value that enables a per-channel write for the render-target color buffer.</span></span> <span data-ttu-id="a2c35-419">Un bit de jeu entraîne la mise à jour du canal de couleur pendant le rendu 3D.</span><span class="sxs-lookup"><span data-stu-id="a2c35-419">A set bit results in the color channel being updated during 3D rendering.</span></span> <span data-ttu-id="a2c35-420">Un bit clair entraîne l’inaffectation du canal de couleur.</span><span class="sxs-lookup"><span data-stu-id="a2c35-420">A clear bit results in the color channel being unaffected.</span></span> <span data-ttu-id="a2c35-421">Cette fonctionnalité est disponible si le \_ bit des fonctionnalités D3DPMISCCAPS COLORWRITEENABLE est défini dans le membre PrimitiveMiscCaps de la structure [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a2c35-421">This functionality is available if the D3DPMISCCAPS\_COLORWRITEENABLE capabilities bit is set in the PrimitiveMiscCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure for the device.</span></span> <span data-ttu-id="a2c35-422">Cet état de rendu n’affecte pas l’opération d’effacement.</span><span class="sxs-lookup"><span data-stu-id="a2c35-422">This render state does not affect the clear operation.</span></span> <span data-ttu-id="a2c35-423">La valeur par défaut est 0x0000000F.</span><span class="sxs-lookup"><span data-stu-id="a2c35-423">The default value is 0x0000000F.</span></span>

<span data-ttu-id="a2c35-424">Les valeurs valides pour cet état de rendu peuvent être n’importe quelle combinaison des \_ indicateurs D3DCOLORWRITEENABLE alpha, D3DCOLORWRITEENABLE \_ Blue, D3DCOLORWRITEENABLE \_ vert ou D3DCOLORWRITEENABLE \_ Red.</span><span class="sxs-lookup"><span data-stu-id="a2c35-424">Valid values for this render state can be any combination of the D3DCOLORWRITEENABLE\_ALPHA, D3DCOLORWRITEENABLE\_BLUE, D3DCOLORWRITEENABLE\_GREEN, or D3DCOLORWRITEENABLE\_RED flags.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-425"><span id="D3DRS_TWEENFACTOR"></span><span id="d3drs_tweenfactor"></span>**D3DRS \_ TWEENFACTOR**</span><span class="sxs-lookup"><span data-stu-id="a2c35-425"><span id="D3DRS_TWEENFACTOR"></span><span id="d3drs_tweenfactor"></span>**D3DRS\_TWEENFACTOR**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-426">Valeur flottante qui contrôle le facteur d’interpolation.</span><span class="sxs-lookup"><span data-stu-id="a2c35-426">A float value that controls the tween factor.</span></span> <span data-ttu-id="a2c35-427">La valeur par défaut est 0.0 f.</span><span class="sxs-lookup"><span data-stu-id="a2c35-427">The default value is 0.0f.</span></span> <span data-ttu-id="a2c35-428">Étant donné que la méthode [**IDirect3DDevice9 :: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accepte les valeurs DWORD, votre application doit effectuer un cast d’une variable qui contient la valeur, comme indiqué dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="a2c35-428">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_TWEENFACTOR, *((DWORD*)&TweenFactor));
```



</dd> <dt>

<span data-ttu-id="a2c35-429"><span id="D3DRS_BLENDOP"></span><span id="d3drs_blendop"></span>**D3DRS \_ BLENDOP**</span><span class="sxs-lookup"><span data-stu-id="a2c35-429"><span id="D3DRS_BLENDOP"></span><span id="d3drs_blendop"></span>**D3DRS\_BLENDOP**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-430">Valeur utilisée pour sélectionner l’opération arithmétique appliquée lorsque l’état de rendu de la fusion alpha, D3DRS \_ ALPHABLENDENABLE, a la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="a2c35-430">Value used to select the arithmetic operation applied when the alpha blending render state, D3DRS\_ALPHABLENDENABLE, is set to **TRUE**.</span></span> <span data-ttu-id="a2c35-431">Les valeurs valides sont définies par le type énuméré [**D3DBLENDOP**](./d3dblendop.md) .</span><span class="sxs-lookup"><span data-stu-id="a2c35-431">Valid values are defined by the [**D3DBLENDOP**](./d3dblendop.md) enumerated type.</span></span> <span data-ttu-id="a2c35-432">La valeur par défaut est D3DBLENDOP \_ Add.</span><span class="sxs-lookup"><span data-stu-id="a2c35-432">The default value is D3DBLENDOP\_ADD.</span></span>

<span data-ttu-id="a2c35-433">Si la fonctionnalité de l' \_ appareil D3DPMISCCAPS BLENDOP n’est pas prise en charge, l’ajout de D3DBLENDOP \_ est effectué.</span><span class="sxs-lookup"><span data-stu-id="a2c35-433">If the D3DPMISCCAPS\_BLENDOP device capability is not supported, then D3DBLENDOP\_ADD is performed.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-434"><span id="D3DRS_POSITIONDEGREE"></span><span id="d3drs_positiondegree"></span>**D3DRS \_ POSITIONDEGREE**</span><span class="sxs-lookup"><span data-stu-id="a2c35-434"><span id="D3DRS_POSITIONDEGREE"></span><span id="d3drs_positiondegree"></span>**D3DRS\_POSITIONDEGREE**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-435">Degré d’interpolation de la position N-patch.</span><span class="sxs-lookup"><span data-stu-id="a2c35-435">N-patch position interpolation degree.</span></span> <span data-ttu-id="a2c35-436">Les valeurs peuvent être D3DDEGREE \_ cubique (par défaut) ou D3DDEGREE \_ Linear.</span><span class="sxs-lookup"><span data-stu-id="a2c35-436">The values can be D3DDEGREE\_CUBIC (default) or D3DDEGREE\_LINEAR.</span></span> <span data-ttu-id="a2c35-437">Pour plus d’informations, consultez [**D3DDEGREETYPE**](./d3ddegreetype.md).</span><span class="sxs-lookup"><span data-stu-id="a2c35-437">For more information, see [**D3DDEGREETYPE**](./d3ddegreetype.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-438"><span id="D3DRS_NORMALDEGREE"></span><span id="d3drs_normaldegree"></span>**D3DRS \_ NORMALDEGREE**</span><span class="sxs-lookup"><span data-stu-id="a2c35-438"><span id="D3DRS_NORMALDEGREE"></span><span id="d3drs_normaldegree"></span>**D3DRS\_NORMALDEGREE**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-439">Degré d’interpolation normale N-patch.</span><span class="sxs-lookup"><span data-stu-id="a2c35-439">N-patch normal interpolation degree.</span></span> <span data-ttu-id="a2c35-440">Les valeurs peuvent être D3DDEGREE \_ Linear (par défaut) ou D3DDEGREE \_ quadratique.</span><span class="sxs-lookup"><span data-stu-id="a2c35-440">The values can be D3DDEGREE\_LINEAR (default) or D3DDEGREE\_QUADRATIC.</span></span> <span data-ttu-id="a2c35-441">Pour plus d’informations, consultez [**D3DDEGREETYPE**](./d3ddegreetype.md).</span><span class="sxs-lookup"><span data-stu-id="a2c35-441">For more information, see [**D3DDEGREETYPE**](./d3ddegreetype.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-442"><span id="D3DRS_SCISSORTESTENABLE"></span><span id="d3drs_scissortestenable"></span>**D3DRS \_ SCISSORTESTENABLE**</span><span class="sxs-lookup"><span data-stu-id="a2c35-442"><span id="D3DRS_SCISSORTESTENABLE"></span><span id="d3drs_scissortestenable"></span>**D3DRS\_SCISSORTESTENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-443">**True** pour activer le test de ciseaux et **false** pour le désactiver.</span><span class="sxs-lookup"><span data-stu-id="a2c35-443">**TRUE** to enable scissor testing and **FALSE** to disable it.</span></span> <span data-ttu-id="a2c35-444">La valeur par défaut est **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="a2c35-444">The default value is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-445"><span id="D3DRS_SLOPESCALEDEPTHBIAS"></span><span id="d3drs_slopescaledepthbias"></span>**D3DRS \_ SLOPESCALEDEPTHBIAS**</span><span class="sxs-lookup"><span data-stu-id="a2c35-445"><span id="D3DRS_SLOPESCALEDEPTHBIAS"></span><span id="d3drs_slopescaledepthbias"></span>**D3DRS\_SLOPESCALEDEPTHBIAS**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-446">Utilisé pour déterminer la quantité d’écart pouvant être appliquée aux primitives coplanaires pour réduire la lutte z.</span><span class="sxs-lookup"><span data-stu-id="a2c35-446">Used to determine how much bias can be applied to co-planar primitives to reduce z-fighting.</span></span> <span data-ttu-id="a2c35-447">La valeur par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="a2c35-447">The default value is 0.</span></span>

<span data-ttu-id="a2c35-448">Bias = (Max \* D3DRS \_ SLOPESCALEDEPTHBIAS) + D3DRS \_ DEPTHBIAS.</span><span class="sxs-lookup"><span data-stu-id="a2c35-448">bias = (max \* D3DRS\_SLOPESCALEDEPTHBIAS) + D3DRS\_DEPTHBIAS.</span></span>

<span data-ttu-id="a2c35-449">où Max est la pente de profondeur maximale du triangle rendu.</span><span class="sxs-lookup"><span data-stu-id="a2c35-449">where max is the maximum depth slope of the triangle being rendered.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-450"><span id="D3DRS_ANTIALIASEDLINEENABLE"></span><span id="d3drs_antialiasedlineenable"></span>**D3DRS \_ ANTIALIASEDLINEENABLE**</span><span class="sxs-lookup"><span data-stu-id="a2c35-450"><span id="D3DRS_ANTIALIASEDLINEENABLE"></span><span id="d3drs_antialiasedlineenable"></span>**D3DRS\_ANTIALIASEDLINEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-451">**True** pour activer l’anticrénelage de ligne, **false** pour désactiver l’anticrénelage de ligne.</span><span class="sxs-lookup"><span data-stu-id="a2c35-451">**TRUE** to enable line antialiasing, **FALSE** to disable line antialiasing.</span></span> <span data-ttu-id="a2c35-452">La valeur par défaut est **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="a2c35-452">The default value is **FALSE**.</span></span>

<span data-ttu-id="a2c35-453">Lors du rendu sur une cible de rendu d’échantillonnage, D3DRS \_ ANTIALIASEDLINEENABLE est ignoré et toutes les lignes sont associées à un alias.</span><span class="sxs-lookup"><span data-stu-id="a2c35-453">When rendering to a multisample render target, D3DRS\_ANTIALIASEDLINEENABLE is ignored and all lines are rendered aliased.</span></span> <span data-ttu-id="a2c35-454">Utilisez [**ID3DXLine**](id3dxline.md) pour le rendu de ligne avec anticrénelage dans une cible de rendu multiéchantillon.</span><span class="sxs-lookup"><span data-stu-id="a2c35-454">Use [**ID3DXLine**](id3dxline.md) for antialiased line rendering in a multisample render target.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-455"><span id="D3DRS_MINTESSELLATIONLEVEL"></span><span id="d3drs_mintessellationlevel"></span>**D3DRS \_ MINTESSELLATIONLEVEL**</span><span class="sxs-lookup"><span data-stu-id="a2c35-455"><span id="D3DRS_MINTESSELLATIONLEVEL"></span><span id="d3drs_mintessellationlevel"></span>**D3DRS\_MINTESSELLATIONLEVEL**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-456">Niveau de pavage minimal.</span><span class="sxs-lookup"><span data-stu-id="a2c35-456">Minimum tessellation level.</span></span> <span data-ttu-id="a2c35-457">La valeur par défaut est 1,0 f.</span><span class="sxs-lookup"><span data-stu-id="a2c35-457">The default value is 1.0f.</span></span> <span data-ttu-id="a2c35-458">Voir [pavage (Direct3D 9)](tessellation.md).</span><span class="sxs-lookup"><span data-stu-id="a2c35-458">See [Tessellation (Direct3D 9)](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-459"><span id="D3DRS_MAXTESSELLATIONLEVEL"></span><span id="d3drs_maxtessellationlevel"></span>**D3DRS \_ MAXTESSELLATIONLEVEL**</span><span class="sxs-lookup"><span data-stu-id="a2c35-459"><span id="D3DRS_MAXTESSELLATIONLEVEL"></span><span id="d3drs_maxtessellationlevel"></span>**D3DRS\_MAXTESSELLATIONLEVEL**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-460">Niveau de pavage maximal.</span><span class="sxs-lookup"><span data-stu-id="a2c35-460">Maximum tessellation level.</span></span> <span data-ttu-id="a2c35-461">La valeur par défaut est 1,0 f.</span><span class="sxs-lookup"><span data-stu-id="a2c35-461">The default value is 1.0f.</span></span> <span data-ttu-id="a2c35-462">Voir [pavage (Direct3D 9)](tessellation.md).</span><span class="sxs-lookup"><span data-stu-id="a2c35-462">See [Tessellation (Direct3D 9)](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-463"><span id="D3DRS_ADAPTIVETESS_X"></span><span id="d3drs_adaptivetess_x"></span>**D3DRS \_ ADAPTIVETESS \_ X**</span><span class="sxs-lookup"><span data-stu-id="a2c35-463"><span id="D3DRS_ADAPTIVETESS_X"></span><span id="d3drs_adaptivetess_x"></span>**D3DRS\_ADAPTIVETESS\_X**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-464">Valeur de paver de manière adaptative, sur l’axe x.</span><span class="sxs-lookup"><span data-stu-id="a2c35-464">Amount to adaptively tessellate, in the x direction.</span></span> <span data-ttu-id="a2c35-465">La valeur par défaut est 0.0 f.</span><span class="sxs-lookup"><span data-stu-id="a2c35-465">Default value is 0.0f.</span></span> <span data-ttu-id="a2c35-466">Consultez [pavage adaptative](tessellation.md).</span><span class="sxs-lookup"><span data-stu-id="a2c35-466">See [Adaptive Tessellation](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-467"><span id="D3DRS_ADAPTIVETESS_Y"></span><span id="d3drs_adaptivetess_y"></span>**D3DRS \_ ADAPTIVETESS \_ Y**</span><span class="sxs-lookup"><span data-stu-id="a2c35-467"><span id="D3DRS_ADAPTIVETESS_Y"></span><span id="d3drs_adaptivetess_y"></span>**D3DRS\_ADAPTIVETESS\_Y**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-468">Valeur de paver adaptative, sur l’axe y.</span><span class="sxs-lookup"><span data-stu-id="a2c35-468">Amount to adaptively tessellate, in the y direction.</span></span> <span data-ttu-id="a2c35-469">La valeur par défaut est 0.0 f.</span><span class="sxs-lookup"><span data-stu-id="a2c35-469">Default value is 0.0f.</span></span> <span data-ttu-id="a2c35-470">Consultez [ \_ pavage adaptative](tessellation.md).</span><span class="sxs-lookup"><span data-stu-id="a2c35-470">See [Adaptive\_Tessellation](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-471"><span id="D3DRS_ADAPTIVETESS_Z"></span><span id="d3drs_adaptivetess_z"></span>**D3DRS \_ ADAPTIVETESS \_ Z**</span><span class="sxs-lookup"><span data-stu-id="a2c35-471"><span id="D3DRS_ADAPTIVETESS_Z"></span><span id="d3drs_adaptivetess_z"></span>**D3DRS\_ADAPTIVETESS\_Z**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-472">Valeur de paver de manière adaptative, en z.</span><span class="sxs-lookup"><span data-stu-id="a2c35-472">Amount to adaptively tessellate, in the z direction.</span></span> <span data-ttu-id="a2c35-473">La valeur par défaut est 1,0 f.</span><span class="sxs-lookup"><span data-stu-id="a2c35-473">Default value is 1.0f.</span></span> <span data-ttu-id="a2c35-474">Consultez [ \_ pavage adaptative](tessellation.md).</span><span class="sxs-lookup"><span data-stu-id="a2c35-474">See [Adaptive\_Tessellation](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-475"><span id="D3DRS_ADAPTIVETESS_W"></span><span id="d3drs_adaptivetess_w"></span>**D3DRS \_ ADAPTIVETESS \_ W**</span><span class="sxs-lookup"><span data-stu-id="a2c35-475"><span id="D3DRS_ADAPTIVETESS_W"></span><span id="d3drs_adaptivetess_w"></span>**D3DRS\_ADAPTIVETESS\_W**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-476">Valeur de paver adaptative, dans la direction w.</span><span class="sxs-lookup"><span data-stu-id="a2c35-476">Amount to adaptively tessellate, in the w direction.</span></span> <span data-ttu-id="a2c35-477">La valeur par défaut est 0.0 f.</span><span class="sxs-lookup"><span data-stu-id="a2c35-477">Default value is 0.0f.</span></span> <span data-ttu-id="a2c35-478">Consultez [ \_ pavage adaptative](tessellation.md).</span><span class="sxs-lookup"><span data-stu-id="a2c35-478">See [Adaptive\_Tessellation](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-479"><span id="D3DRS_ENABLEADAPTIVETESSELLATION"></span><span id="d3drs_enableadaptivetessellation"></span>**D3DRS \_ ENABLEADAPTIVETESSELLATION**</span><span class="sxs-lookup"><span data-stu-id="a2c35-479"><span id="D3DRS_ENABLEADAPTIVETESSELLATION"></span><span id="d3drs_enableadaptivetessellation"></span>**D3DRS\_ENABLEADAPTIVETESSELLATION**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-480">**True** pour activer le pavage adaptative, **false** pour le désactiver.</span><span class="sxs-lookup"><span data-stu-id="a2c35-480">**TRUE** to enable adaptive tessellation, **FALSE** to disable it.</span></span> <span data-ttu-id="a2c35-481">La valeur par défaut est **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="a2c35-481">The default value is **FALSE**.</span></span> <span data-ttu-id="a2c35-482">Consultez [ \_ pavage adaptative](tessellation.md).</span><span class="sxs-lookup"><span data-stu-id="a2c35-482">See [Adaptive\_Tessellation](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-483"><span id="D3DRS_TWOSIDEDSTENCILMODE"></span><span id="d3drs_twosidedstencilmode"></span>**D3DRS \_ TWOSIDEDSTENCILMODE**</span><span class="sxs-lookup"><span data-stu-id="a2c35-483"><span id="D3DRS_TWOSIDEDSTENCILMODE"></span><span id="d3drs_twosidedstencilmode"></span>**D3DRS\_TWOSIDEDSTENCILMODE**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-484">**True** active le stencil à deux côtés, **false** le désactive.</span><span class="sxs-lookup"><span data-stu-id="a2c35-484">**TRUE** enables two-sided stenciling, **FALSE** disables it.</span></span> <span data-ttu-id="a2c35-485">La valeur par défaut est **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="a2c35-485">The default value is **FALSE**.</span></span> <span data-ttu-id="a2c35-486">L’application doit définir D3DRS \_ CULLMODE sur D3DCULL \_ None pour activer le mode stencil à deux côtés.</span><span class="sxs-lookup"><span data-stu-id="a2c35-486">The application should set D3DRS\_CULLMODE to D3DCULL\_NONE to enable two-sided stencil mode.</span></span> <span data-ttu-id="a2c35-487">Si l’ordre d’enroulement du triangle est dans le sens des aiguilles d’une montre, les \_ opérations du stencil D3DRS \* sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="a2c35-487">If the triangle winding order is clockwise, the D3DRS\_STENCIL\* operations will be used.</span></span> <span data-ttu-id="a2c35-488">Si l’ordre d’enroulement est dans le sens inverse des aiguilles d' \_ une passe, les opérations du stencil D3DRS CCW \_ \* sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="a2c35-488">If the winding order is counterclockwise, the D3DRS\_CCW\_STENCIL\* operations will be used.</span></span>

<span data-ttu-id="a2c35-489">Pour voir si le stencil à deux côtés est pris en charge, consultez le membre StencilCaps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) pour D3DSTENCILCAPS \_ TWOSIDED.</span><span class="sxs-lookup"><span data-stu-id="a2c35-489">To see if two-sided stencil is supported, check the StencilCaps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) for D3DSTENCILCAPS\_TWOSIDED.</span></span> <span data-ttu-id="a2c35-490">Voir aussi [D3DSTENCILCAPS](d3dstencilcaps.md).</span><span class="sxs-lookup"><span data-stu-id="a2c35-490">See also [D3DSTENCILCAPS](d3dstencilcaps.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-491"><span id="D3DRS_CCW_STENCILFAIL"></span><span id="d3drs_ccw_stencilfail"></span>**D3DRS \_ CCW \_ STENCILFAIL**</span><span class="sxs-lookup"><span data-stu-id="a2c35-491"><span id="D3DRS_CCW_STENCILFAIL"></span><span id="d3drs_ccw_stencilfail"></span>**D3DRS\_CCW\_STENCILFAIL**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-492">Opération de stencil à effectuer si le test du stencil CCW échoue.</span><span class="sxs-lookup"><span data-stu-id="a2c35-492">Stencil operation to perform if CCW stencil test fails.</span></span> <span data-ttu-id="a2c35-493">Les valeurs proviennent du type énuméré [**D3DSTENCILOP**](./d3dstencilop.md) .</span><span class="sxs-lookup"><span data-stu-id="a2c35-493">Values are from the [**D3DSTENCILOP**](./d3dstencilop.md) enumerated type.</span></span> <span data-ttu-id="a2c35-494">La valeur par défaut est D3DSTENCILOP \_ Keep.</span><span class="sxs-lookup"><span data-stu-id="a2c35-494">The default value is D3DSTENCILOP\_KEEP.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-495"><span id="D3DRS_CCW_STENCILZFAIL"></span><span id="d3drs_ccw_stencilzfail"></span>**D3DRS \_ CCW \_ STENCILZFAIL**</span><span class="sxs-lookup"><span data-stu-id="a2c35-495"><span id="D3DRS_CCW_STENCILZFAIL"></span><span id="d3drs_ccw_stencilzfail"></span>**D3DRS\_CCW\_STENCILZFAIL**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-496">Opération de stencil à exécuter si le test de stencil CCW réussit et que le test z échoue.</span><span class="sxs-lookup"><span data-stu-id="a2c35-496">Stencil operation to perform if CCW stencil test passes and z-test fails.</span></span> <span data-ttu-id="a2c35-497">Les valeurs proviennent du type énuméré [**D3DSTENCILOP**](./d3dstencilop.md) .</span><span class="sxs-lookup"><span data-stu-id="a2c35-497">Values are from the [**D3DSTENCILOP**](./d3dstencilop.md) enumerated type.</span></span> <span data-ttu-id="a2c35-498">La valeur par défaut est D3DSTENCILOP \_ Keep.</span><span class="sxs-lookup"><span data-stu-id="a2c35-498">The default value is D3DSTENCILOP\_KEEP.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-499"><span id="D3DRS_CCW_STENCILPASS"></span><span id="d3drs_ccw_stencilpass"></span>**D3DRS \_ CCW \_ STENCILPASS**</span><span class="sxs-lookup"><span data-stu-id="a2c35-499"><span id="D3DRS_CCW_STENCILPASS"></span><span id="d3drs_ccw_stencilpass"></span>**D3DRS\_CCW\_STENCILPASS**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-500">Opération de stencil à effectuer si les deux stencils CCW et z-tests réussissent.</span><span class="sxs-lookup"><span data-stu-id="a2c35-500">Stencil operation to perform if both CCW stencil and z-tests pass.</span></span> <span data-ttu-id="a2c35-501">Les valeurs proviennent du type énuméré [**D3DSTENCILOP**](./d3dstencilop.md) .</span><span class="sxs-lookup"><span data-stu-id="a2c35-501">Values are from the [**D3DSTENCILOP**](./d3dstencilop.md) enumerated type.</span></span> <span data-ttu-id="a2c35-502">La valeur par défaut est D3DSTENCILOP \_ Keep.</span><span class="sxs-lookup"><span data-stu-id="a2c35-502">The default value is D3DSTENCILOP\_KEEP.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-503"><span id="D3DRS_CCW_STENCILFUNC"></span><span id="d3drs_ccw_stencilfunc"></span>**D3DRS \_ CCW \_ STENCILFUNC**</span><span class="sxs-lookup"><span data-stu-id="a2c35-503"><span id="D3DRS_CCW_STENCILFUNC"></span><span id="d3drs_ccw_stencilfunc"></span>**D3DRS\_CCW\_STENCILFUNC**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-504">Fonction de comparaison.</span><span class="sxs-lookup"><span data-stu-id="a2c35-504">The comparison function.</span></span> <span data-ttu-id="a2c35-505">Le test du stencil CCW réussit si la fonction de stencil ((Ref & Mask) (gabarit & Mask)) a la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="a2c35-505">CCW stencil test passes if ((ref & mask) stencil function (stencil & mask)) is **TRUE**.</span></span> <span data-ttu-id="a2c35-506">Les valeurs proviennent du type énuméré [**D3DCMPFUNC**](./d3dcmpfunc.md) .</span><span class="sxs-lookup"><span data-stu-id="a2c35-506">Values are from the [**D3DCMPFUNC**](./d3dcmpfunc.md) enumerated type.</span></span> <span data-ttu-id="a2c35-507">La valeur par défaut est D3DCMP \_ Always.</span><span class="sxs-lookup"><span data-stu-id="a2c35-507">The default value is D3DCMP\_ALWAYS.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-508"><span id="D3DRS_COLORWRITEENABLE1"></span><span id="d3drs_colorwriteenable1"></span>**D3DRS \_ COLORWRITEENABLE1**</span><span class="sxs-lookup"><span data-stu-id="a2c35-508"><span id="D3DRS_COLORWRITEENABLE1"></span><span id="d3drs_colorwriteenable1"></span>**D3DRS\_COLORWRITEENABLE1**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-509">Valeurs ColorWriteEnable supplémentaires pour les appareils.</span><span class="sxs-lookup"><span data-stu-id="a2c35-509">Additional ColorWriteEnable values for the devices.</span></span> <span data-ttu-id="a2c35-510">Consultez D3DRS \_ COLORWRITEENABLE.</span><span class="sxs-lookup"><span data-stu-id="a2c35-510">See D3DRS\_COLORWRITEENABLE.</span></span> <span data-ttu-id="a2c35-511">Cette fonctionnalité est disponible si le \_ bit des fonctionnalités D3DPMISCCAPS INDEPENDENTWRITEMASKS est défini dans le membre PrimitiveMiscCaps de la structure [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a2c35-511">This functionality is available if the D3DPMISCCAPS\_INDEPENDENTWRITEMASKS capabilities bit is set in the PrimitiveMiscCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure for the device.</span></span> <span data-ttu-id="a2c35-512">La valeur par défaut est 0x0000000f.</span><span class="sxs-lookup"><span data-stu-id="a2c35-512">The default value is 0x0000000f.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-513"><span id="D3DRS_COLORWRITEENABLE2"></span><span id="d3drs_colorwriteenable2"></span>**D3DRS \_ COLORWRITEENABLE2**</span><span class="sxs-lookup"><span data-stu-id="a2c35-513"><span id="D3DRS_COLORWRITEENABLE2"></span><span id="d3drs_colorwriteenable2"></span>**D3DRS\_COLORWRITEENABLE2**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-514">Valeurs ColorWriteEnable supplémentaires pour les appareils.</span><span class="sxs-lookup"><span data-stu-id="a2c35-514">Additional ColorWriteEnable values for the devices.</span></span> <span data-ttu-id="a2c35-515">Consultez D3DRS \_ COLORWRITEENABLE.</span><span class="sxs-lookup"><span data-stu-id="a2c35-515">See D3DRS\_COLORWRITEENABLE.</span></span> <span data-ttu-id="a2c35-516">Cette fonctionnalité est disponible si le \_ bit des fonctionnalités D3DPMISCCAPS INDEPENDENTWRITEMASKS est défini dans le membre PrimitiveMiscCaps de la structure [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a2c35-516">This functionality is available if the D3DPMISCCAPS\_INDEPENDENTWRITEMASKS capabilities bit is set in the PrimitiveMiscCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure for the device.</span></span> <span data-ttu-id="a2c35-517">La valeur par défaut est 0x0000000f.</span><span class="sxs-lookup"><span data-stu-id="a2c35-517">The default value is 0x0000000f.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-518"><span id="D3DRS_COLORWRITEENABLE3"></span><span id="d3drs_colorwriteenable3"></span>**D3DRS \_ COLORWRITEENABLE3**</span><span class="sxs-lookup"><span data-stu-id="a2c35-518"><span id="D3DRS_COLORWRITEENABLE3"></span><span id="d3drs_colorwriteenable3"></span>**D3DRS\_COLORWRITEENABLE3**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-519">Valeurs ColorWriteEnable supplémentaires pour les appareils.</span><span class="sxs-lookup"><span data-stu-id="a2c35-519">Additional ColorWriteEnable values for the devices.</span></span> <span data-ttu-id="a2c35-520">Consultez D3DRS \_ COLORWRITEENABLE.</span><span class="sxs-lookup"><span data-stu-id="a2c35-520">See D3DRS\_COLORWRITEENABLE.</span></span> <span data-ttu-id="a2c35-521">Cette fonctionnalité est disponible si le \_ bit des fonctionnalités D3DPMISCCAPS INDEPENDENTWRITEMASKS est défini dans le membre PrimitiveMiscCaps de la structure [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a2c35-521">This functionality is available if the D3DPMISCCAPS\_INDEPENDENTWRITEMASKS capabilities bit is set in the PrimitiveMiscCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure for the device.</span></span> <span data-ttu-id="a2c35-522">La valeur par défaut est 0x0000000f.</span><span class="sxs-lookup"><span data-stu-id="a2c35-522">The default value is 0x0000000f.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-523"><span id="D3DRS_BLENDFACTOR"></span><span id="d3drs_blendfactor"></span>**D3DRS \_ BLENDFACTOR**</span><span class="sxs-lookup"><span data-stu-id="a2c35-523"><span id="D3DRS_BLENDFACTOR"></span><span id="d3drs_blendfactor"></span>**D3DRS\_BLENDFACTOR**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-524">[**D3DCOLOR**](d3dcolor.md) utilisé pour une constante Blend-Factor pendant la fusion alpha.</span><span class="sxs-lookup"><span data-stu-id="a2c35-524">[**D3DCOLOR**](d3dcolor.md) used for a constant blend-factor during alpha blending.</span></span> <span data-ttu-id="a2c35-525">Cette fonctionnalité est disponible si le \_ bit des fonctionnalités D3DPBLENDCAPS BLENDFACTOR est défini dans le membre SrcBlendCaps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) ou le membre DestBlendCaps de **D3DCAPS9**.</span><span class="sxs-lookup"><span data-stu-id="a2c35-525">This functionality is available if the D3DPBLENDCAPS\_BLENDFACTOR capabilities bit is set in the SrcBlendCaps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) or the DestBlendCaps member of **D3DCAPS9**.</span></span> <span data-ttu-id="a2c35-526">Consultez [**D3DRENDERSTATETYPE**]().</span><span class="sxs-lookup"><span data-stu-id="a2c35-526">See [**D3DRENDERSTATETYPE**]().</span></span> <span data-ttu-id="a2c35-527">La valeur par défaut est 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="a2c35-527">The default value is 0xffffffff.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-528"><span id="D3DRS_SRGBWRITEENABLE"></span><span id="d3drs_srgbwriteenable"></span>**D3DRS \_ SRGBWRITEENABLE**</span><span class="sxs-lookup"><span data-stu-id="a2c35-528"><span id="D3DRS_SRGBWRITEENABLE"></span><span id="d3drs_srgbwriteenable"></span>**D3DRS\_SRGBWRITEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-529">Activez la valeur gamma des écritures de la cible de rendu pour qu’elles soient corrigées en sRVB.</span><span class="sxs-lookup"><span data-stu-id="a2c35-529">Enable render-target writes to be gamma corrected to sRGB.</span></span> <span data-ttu-id="a2c35-530">Le format doit exposer D3DUSAGE \_ SRGBWRITE.</span><span class="sxs-lookup"><span data-stu-id="a2c35-530">The format must expose D3DUSAGE\_SRGBWRITE.</span></span> <span data-ttu-id="a2c35-531">La valeur par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="a2c35-531">The default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-532"><span id="D3DRS_DEPTHBIAS"></span><span id="d3drs_depthbias"></span>**D3DRS \_ DEPTHBIAS**</span><span class="sxs-lookup"><span data-stu-id="a2c35-532"><span id="D3DRS_DEPTHBIAS"></span><span id="d3drs_depthbias"></span>**D3DRS\_DEPTHBIAS**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-533">Valeur à virgule flottante utilisée pour la comparaison des valeurs de profondeur.</span><span class="sxs-lookup"><span data-stu-id="a2c35-533">A floating-point value that is used for comparison of depth values.</span></span> <span data-ttu-id="a2c35-534">Consultez [décalage de profondeur (Direct3D 9)](depth-bias.md).</span><span class="sxs-lookup"><span data-stu-id="a2c35-534">See [Depth Bias (Direct3D 9)](depth-bias.md).</span></span> <span data-ttu-id="a2c35-535">La valeur par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="a2c35-535">The default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-536"><span id="D3DRS_WRAP8"></span><span id="d3drs_wrap8"></span>**D3DRS \_ WRAP8**</span><span class="sxs-lookup"><span data-stu-id="a2c35-536"><span id="D3DRS_WRAP8"></span><span id="d3drs_wrap8"></span>**D3DRS\_WRAP8**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-537">Consultez D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="a2c35-537">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-538"><span id="D3DRS_WRAP9"></span><span id="d3drs_wrap9"></span>**D3DRS \_ WRAP9**</span><span class="sxs-lookup"><span data-stu-id="a2c35-538"><span id="D3DRS_WRAP9"></span><span id="d3drs_wrap9"></span>**D3DRS\_WRAP9**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-539">Consultez D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="a2c35-539">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-540"><span id="D3DRS_WRAP10"></span><span id="d3drs_wrap10"></span>**D3DRS \_ WRAP10**</span><span class="sxs-lookup"><span data-stu-id="a2c35-540"><span id="D3DRS_WRAP10"></span><span id="d3drs_wrap10"></span>**D3DRS\_WRAP10**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-541">Consultez D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="a2c35-541">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-542"><span id="D3DRS_WRAP11"></span><span id="d3drs_wrap11"></span>**D3DRS \_ WRAP11**</span><span class="sxs-lookup"><span data-stu-id="a2c35-542"><span id="D3DRS_WRAP11"></span><span id="d3drs_wrap11"></span>**D3DRS\_WRAP11**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-543">Consultez D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="a2c35-543">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-544"><span id="D3DRS_WRAP12"></span><span id="d3drs_wrap12"></span>**D3DRS \_ WRAP12**</span><span class="sxs-lookup"><span data-stu-id="a2c35-544"><span id="D3DRS_WRAP12"></span><span id="d3drs_wrap12"></span>**D3DRS\_WRAP12**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-545">Consultez D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="a2c35-545">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-546"><span id="D3DRS_WRAP13"></span><span id="d3drs_wrap13"></span>**D3DRS \_ WRAP13**</span><span class="sxs-lookup"><span data-stu-id="a2c35-546"><span id="D3DRS_WRAP13"></span><span id="d3drs_wrap13"></span>**D3DRS\_WRAP13**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-547">Consultez D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="a2c35-547">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-548"><span id="D3DRS_WRAP14"></span><span id="d3drs_wrap14"></span>**D3DRS \_ WRAP14**</span><span class="sxs-lookup"><span data-stu-id="a2c35-548"><span id="D3DRS_WRAP14"></span><span id="d3drs_wrap14"></span>**D3DRS\_WRAP14**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-549">Consultez D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="a2c35-549">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-550"><span id="D3DRS_WRAP15"></span><span id="d3drs_wrap15"></span>**D3DRS \_ WRAP15**</span><span class="sxs-lookup"><span data-stu-id="a2c35-550"><span id="D3DRS_WRAP15"></span><span id="d3drs_wrap15"></span>**D3DRS\_WRAP15**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-551">Consultez D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="a2c35-551">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-552"><span id="D3DRS_SEPARATEALPHABLENDENABLE"></span><span id="d3drs_separatealphablendenable"></span>**D3DRS \_ SEPARATEALPHABLENDENABLE**</span><span class="sxs-lookup"><span data-stu-id="a2c35-552"><span id="D3DRS_SEPARATEALPHABLENDENABLE"></span><span id="d3drs_separatealphablendenable"></span>**D3DRS\_SEPARATEALPHABLENDENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-553">**True** active le mode de fondu distinct pour le canal alpha.</span><span class="sxs-lookup"><span data-stu-id="a2c35-553">**TRUE** enables the separate blend mode for the alpha channel.</span></span> <span data-ttu-id="a2c35-554">La valeur par défaut est **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="a2c35-554">The default value is **FALSE**.</span></span>

<span data-ttu-id="a2c35-555">Quand la valeur est **false**, les facteurs et les opérations de fusion de cible de rendu appliqués à alpha sont forcés à être les mêmes que ceux définis pour la couleur.</span><span class="sxs-lookup"><span data-stu-id="a2c35-555">When set to **FALSE**, the render-target blending factors and operations applied to alpha are forced to be the same as those defined for color.</span></span> <span data-ttu-id="a2c35-556">Ce mode est effectivement câblé à **false** sur les implémentations qui ne définissent pas le SEPARATEALPHABLEND Cap D3DPMISCCAPS \_ .</span><span class="sxs-lookup"><span data-stu-id="a2c35-556">This mode is effectively hardwired to **FALSE** on implementations that don't set the cap D3DPMISCCAPS\_SEPARATEALPHABLEND.</span></span> <span data-ttu-id="a2c35-557">Consultez [D3DPMISCCAPS](d3dpmisccaps.md).</span><span class="sxs-lookup"><span data-stu-id="a2c35-557">See [D3DPMISCCAPS](d3dpmisccaps.md).</span></span>

<span data-ttu-id="a2c35-558">Le type de fusion alpha distincte est déterminé par les États de \_ rendu D3DRS SRCBLENDALPHA et D3DRS \_ DESTBLENDALPHA.</span><span class="sxs-lookup"><span data-stu-id="a2c35-558">The type of separate alpha blending is determined by the D3DRS\_SRCBLENDALPHA and D3DRS\_DESTBLENDALPHA render states.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-559"><span id="D3DRS_SRCBLENDALPHA"></span><span id="d3drs_srcblendalpha"></span>**D3DRS \_ SRCBLENDALPHA**</span><span class="sxs-lookup"><span data-stu-id="a2c35-559"><span id="D3DRS_SRCBLENDALPHA"></span><span id="d3drs_srcblendalpha"></span>**D3DRS\_SRCBLENDALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-560">Un membre du type énuméré [**D3DBLEND**](./d3dblend.md) .</span><span class="sxs-lookup"><span data-stu-id="a2c35-560">One member of the [**D3DBLEND**](./d3dblend.md) enumerated type.</span></span> <span data-ttu-id="a2c35-561">Cette valeur est ignorée, sauf si D3DRS \_ SEPARATEALPHABLENDENABLE a la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="a2c35-561">This value is ignored unless D3DRS\_SEPARATEALPHABLENDENABLE is **TRUE**.</span></span> <span data-ttu-id="a2c35-562">La valeur par défaut est D3DBLEND \_ .</span><span class="sxs-lookup"><span data-stu-id="a2c35-562">The default value is D3DBLEND\_ONE.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-563"><span id="D3DRS_DESTBLENDALPHA"></span><span id="d3drs_destblendalpha"></span>**D3DRS \_ DESTBLENDALPHA**</span><span class="sxs-lookup"><span data-stu-id="a2c35-563"><span id="D3DRS_DESTBLENDALPHA"></span><span id="d3drs_destblendalpha"></span>**D3DRS\_DESTBLENDALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-564">Un membre du type énuméré [**D3DBLEND**](./d3dblend.md) .</span><span class="sxs-lookup"><span data-stu-id="a2c35-564">One member of the [**D3DBLEND**](./d3dblend.md) enumerated type.</span></span> <span data-ttu-id="a2c35-565">Cette valeur est ignorée, sauf si D3DRS \_ SEPARATEALPHABLENDENABLE a la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="a2c35-565">This value is ignored unless D3DRS\_SEPARATEALPHABLENDENABLE is **TRUE**.</span></span> <span data-ttu-id="a2c35-566">La valeur par défaut est D3DBLEND \_ zéro.</span><span class="sxs-lookup"><span data-stu-id="a2c35-566">The default value is D3DBLEND\_ZERO.</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-567"><span id="D3DRS_BLENDOPALPHA"></span><span id="d3drs_blendopalpha"></span>**D3DRS \_ BLENDOPALPHA**</span><span class="sxs-lookup"><span data-stu-id="a2c35-567"><span id="D3DRS_BLENDOPALPHA"></span><span id="d3drs_blendopalpha"></span>**D3DRS\_BLENDOPALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-568">Valeur utilisée pour sélectionner l’opération arithmétique appliquée à la fusion alpha distincte lorsque l’état de rendu D3DRS \_ SEPARATEALPHABLENDENABLE est défini sur **true**.</span><span class="sxs-lookup"><span data-stu-id="a2c35-568">Value used to select the arithmetic operation applied to separate alpha blending when the render state, D3DRS\_SEPARATEALPHABLENDENABLE, is set to **TRUE**.</span></span>

<span data-ttu-id="a2c35-569">Les valeurs valides sont définies par le type énuméré [**D3DBLENDOP**](./d3dblendop.md) .</span><span class="sxs-lookup"><span data-stu-id="a2c35-569">Valid values are defined by the [**D3DBLENDOP**](./d3dblendop.md) enumerated type.</span></span> <span data-ttu-id="a2c35-570">La valeur par défaut est D3DBLENDOP \_ Add.</span><span class="sxs-lookup"><span data-stu-id="a2c35-570">The default value is D3DBLENDOP\_ADD.</span></span>

<span data-ttu-id="a2c35-571">Si la fonctionnalité de l' \_ appareil D3DPMISCCAPS BLENDOP n’est pas prise en charge, l’ajout de D3DBLENDOP \_ est effectué.</span><span class="sxs-lookup"><span data-stu-id="a2c35-571">If the D3DPMISCCAPS\_BLENDOP device capability is not supported, then D3DBLENDOP\_ADD is performed.</span></span> <span data-ttu-id="a2c35-572">Consultez [D3DPMISCCAPS](d3dpmisccaps.md).</span><span class="sxs-lookup"><span data-stu-id="a2c35-572">See [D3DPMISCCAPS](d3dpmisccaps.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2c35-573"><span id="D3DRS_FORCE_DWORD"></span><span id="d3drs_force_dword"></span>**D3DRS \_ forcer \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="a2c35-573"><span id="D3DRS_FORCE_DWORD"></span><span id="d3drs_force_dword"></span>**D3DRS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="a2c35-574">Force cette énumération à se compiler à 32 bits de taille.</span><span class="sxs-lookup"><span data-stu-id="a2c35-574">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="a2c35-575">Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits.</span><span class="sxs-lookup"><span data-stu-id="a2c35-575">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="a2c35-576">Cette valeur n'est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="a2c35-576">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a2c35-577">Notes</span><span class="sxs-lookup"><span data-stu-id="a2c35-577">Remarks</span></span>



| <span data-ttu-id="a2c35-578">États de rendu</span><span class="sxs-lookup"><span data-stu-id="a2c35-578">Render States</span></span>        |                    |
|----------------------|--------------------|
| <span data-ttu-id="a2c35-579">PS \_ 1 \_ 1 à PS \_ 1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="a2c35-579">ps\_1\_1 to ps\_1\_3</span></span> | <span data-ttu-id="a2c35-580">4 échantillonneurs de texture</span><span class="sxs-lookup"><span data-stu-id="a2c35-580">4 texture samplers</span></span> |



 

<span data-ttu-id="a2c35-581">Direct3D définit la \_ constante WRAPBIAS D3DRENDERSTATE comme un moyen pratique pour les applications d’activer ou de désactiver le renvoi à la ligne, en fonction de l’entier de base zéro d’un jeu de coordonnées de texture (plutôt que d’utiliser explicitement l’une des \_ valeurs d’État n de retour de D3DRS).</span><span class="sxs-lookup"><span data-stu-id="a2c35-581">Direct3D defines the D3DRENDERSTATE\_WRAPBIAS constant as a convenience for applications to enable or disable texture wrapping, based on the zero-based integer of a texture coordinate set (rather than explicitly using one of the D3DRS\_WRAP n state values).</span></span> <span data-ttu-id="a2c35-582">Ajoutez la \_ valeur WRAPBIAS D3DRENDERSTATE à l’index de base zéro d’un jeu de coordonnées de texture pour calculer la \_ valeur n Wrap D3DRS correspondant à cet index, comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="a2c35-582">Add the D3DRENDERSTATE\_WRAPBIAS value to the zero-based index of a texture coordinate set to calculate the D3DRS\_WRAP n value that corresponds to that index, as shown in the following example.</span></span>


```
// Enable U/V wrapping for textures that use the texture 
// coordinate set at the index within the dwIndex variable
    
HRESULT hr = pd3dDevice->SetRenderState(
dwIndex + D3DRENDERSTATE_WRAPBIAS,  
D3DWRAPCOORD_0 | D3DWRAPCOORD_1);
     
// If dwIndex is 3, the value that results from 
// the addition equals D3DRS_WRAP3 (131)
```



## <a name="requirements"></a><span data-ttu-id="a2c35-583">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a2c35-583">Requirements</span></span>



| <span data-ttu-id="a2c35-584">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a2c35-584">Requirement</span></span> | <span data-ttu-id="a2c35-585">Valeur</span><span class="sxs-lookup"><span data-stu-id="a2c35-585">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a2c35-586">En-tête</span><span class="sxs-lookup"><span data-stu-id="a2c35-586">Header</span></span><br/> | <dl> <span data-ttu-id="a2c35-587"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2c35-587"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2c35-588">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a2c35-588">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2c35-589">Énumérations Direct3D</span><span class="sxs-lookup"><span data-stu-id="a2c35-589">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="a2c35-590">**IDirect3DDevice9::GetRenderState**</span><span class="sxs-lookup"><span data-stu-id="a2c35-590">**IDirect3DDevice9::GetRenderState**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrenderstate)
</dt> <dt>

[<span data-ttu-id="a2c35-591">**IDirect3DDevice9::SetRenderState**</span><span class="sxs-lookup"><span data-stu-id="a2c35-591">**IDirect3DDevice9::SetRenderState**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)
</dt> </dl>

 

 
