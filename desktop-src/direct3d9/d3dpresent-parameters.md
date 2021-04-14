---
description: Décrit les paramètres de présentation.
ms.assetid: d677aeb7-a188-4ddc-b8c9-48e13676e9c8
title: Structure D3DPRESENT_PARAMETERS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPRESENT_PARAMETERS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: f83ab03773356a01c8c6ac490bb099c6e7508be2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323001"
---
# <a name="d3dpresent_parameters-structure"></a><span data-ttu-id="ec546-103">D3DPRESENT, \_ structure de paramètres</span><span class="sxs-lookup"><span data-stu-id="ec546-103">D3DPRESENT\_PARAMETERS structure</span></span>

<span data-ttu-id="ec546-104">Décrit les paramètres de présentation.</span><span class="sxs-lookup"><span data-stu-id="ec546-104">Describes the presentation parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec546-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ec546-105">Syntax</span></span>


```C++
typedef struct D3DPRESENT_PARAMETERS {
  UINT                BackBufferWidth;
  UINT                BackBufferHeight;
  D3DFORMAT           BackBufferFormat;
  UINT                BackBufferCount;
  D3DMULTISAMPLE_TYPE MultiSampleType;
  DWORD               MultiSampleQuality;
  D3DSWAPEFFECT       SwapEffect;
  HWND                hDeviceWindow;
  BOOL                Windowed;
  BOOL                EnableAutoDepthStencil;
  D3DFORMAT           AutoDepthStencilFormat;
  DWORD               Flags;
  UINT                FullScreen_RefreshRateInHz;
  UINT                PresentationInterval;
} D3DPRESENT_PARAMETERS, *LPD3DPRESENT_PARAMETERS;
```



## <a name="members"></a><span data-ttu-id="ec546-106">Membres</span><span class="sxs-lookup"><span data-stu-id="ec546-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ec546-107">**BackBufferWidth**</span><span class="sxs-lookup"><span data-stu-id="ec546-107">**BackBufferWidth**</span></span>
</dt> <dd>

<span data-ttu-id="ec546-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ec546-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ec546-109">Largeur des mémoires tampons d’arrière-plan de la nouvelle chaîne d’échange, en pixels.</span><span class="sxs-lookup"><span data-stu-id="ec546-109">Width of the new swap chain's back buffers, in pixels.</span></span> <span data-ttu-id="ec546-110">Si **Windowed** a la valeur **false** (la présentation est pleine d’écran), cette valeur doit être égale à la largeur de l’un des modes d’affichage énumérés trouvés par le biais de [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).</span><span class="sxs-lookup"><span data-stu-id="ec546-110">If **Windowed** is **FALSE** (the presentation is full-screen), this value must equal the width of one of the enumerated display modes found through [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).</span></span> <span data-ttu-id="ec546-111">Si **Windowed** a la **valeur true** et que **BackBufferWidth** ou **BackBufferHeight** est égal à zéro, la dimension correspondante de la zone cliente de **HDeviceWindow** (ou la fenêtre de focus, si **hDeviceWindow** est **null**) est prise.</span><span class="sxs-lookup"><span data-stu-id="ec546-111">If **Windowed** is **TRUE** and either **BackBufferWidth** or **BackBufferHeight** is zero, the corresponding dimension of the client area of the **hDeviceWindow** (or the focus window, if **hDeviceWindow** is **NULL**) is taken.</span></span>

</dd> <dt>

<span data-ttu-id="ec546-112">**BackBufferHeight**</span><span class="sxs-lookup"><span data-stu-id="ec546-112">**BackBufferHeight**</span></span>
</dt> <dd>

<span data-ttu-id="ec546-113">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ec546-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ec546-114">Hauteur des mémoires tampons d’arrière-plan de la nouvelle chaîne d’échange, en pixels.</span><span class="sxs-lookup"><span data-stu-id="ec546-114">Height of the new swap chain's back buffers, in pixels.</span></span> <span data-ttu-id="ec546-115">Si **Windowed** a la valeur **false** (la présentation est pleine d’écran), cette valeur doit être égale à la hauteur de l’un des modes d’affichage énumérés trouvés par le biais de [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).</span><span class="sxs-lookup"><span data-stu-id="ec546-115">If **Windowed** is **FALSE** (the presentation is full-screen), this value must equal the height of one of the enumerated display modes found through [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).</span></span> <span data-ttu-id="ec546-116">Si **Windowed** a la **valeur true** et que **BackBufferWidth** ou **BackBufferHeight** est égal à zéro, la dimension correspondante de la zone cliente de **HDeviceWindow** (ou la fenêtre de focus, si **hDeviceWindow** est **null**) est prise.</span><span class="sxs-lookup"><span data-stu-id="ec546-116">If **Windowed** is **TRUE** and either **BackBufferWidth** or **BackBufferHeight** is zero, the corresponding dimension of the client area of the **hDeviceWindow** (or the focus window, if **hDeviceWindow** is **NULL**) is taken.</span></span>

</dd> <dt>

<span data-ttu-id="ec546-117">**BackBufferFormat**</span><span class="sxs-lookup"><span data-stu-id="ec546-117">**BackBufferFormat**</span></span>
</dt> <dd>

<span data-ttu-id="ec546-118">Type : **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="ec546-118">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ec546-119">Format de la mémoire tampon d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="ec546-119">The back buffer format.</span></span> <span data-ttu-id="ec546-120">Pour plus d’informations sur les formats, consultez [D3DFORMAT](d3dformat.md).</span><span class="sxs-lookup"><span data-stu-id="ec546-120">For more information about formats, see [D3DFORMAT](d3dformat.md).</span></span> <span data-ttu-id="ec546-121">Cette valeur doit être l’un des formats de cible de rendu tels qu’ils sont validés par [**CheckDeviceType**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="ec546-121">This value must be one of the render-target formats as validated by [**CheckDeviceType**](/windows/desktop/api).</span></span> <span data-ttu-id="ec546-122">Vous pouvez utiliser [**GetDisplayMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode) pour obtenir le format actuel.</span><span class="sxs-lookup"><span data-stu-id="ec546-122">You can use [**GetDisplayMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode) to obtain the current format.</span></span>

<span data-ttu-id="ec546-123">En fait, D3DFMT \_ Unknown peut être spécifié pour **backBufferFormat** en mode fenêtre.</span><span class="sxs-lookup"><span data-stu-id="ec546-123">In fact, D3DFMT\_UNKNOWN can be specified for the **BackBufferFormat** while in windowed mode.</span></span> <span data-ttu-id="ec546-124">Cela indique au runtime d’utiliser le format de mode d’affichage actuel et d’éliminer la nécessité d’appeler [**GetDisplayMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode).</span><span class="sxs-lookup"><span data-stu-id="ec546-124">This tells the runtime to use the current display-mode format and eliminates the need to call [**GetDisplayMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode).</span></span>

<span data-ttu-id="ec546-125">Pour les applications Windows, le format de mémoire tampon d’arrière-plan n’a plus besoin de correspondre au format de mode d’affichage, car la conversion de couleur peut désormais être effectuée par le matériel (si le matériel prend en charge la conversion de couleur).</span><span class="sxs-lookup"><span data-stu-id="ec546-125">For windowed applications, the back buffer format no longer needs to match the display-mode format because color conversion can now be done by the hardware (if the hardware supports color conversion).</span></span> <span data-ttu-id="ec546-126">L’ensemble de formats de mémoire tampon d’arrière-plan possibles est restreint, mais le runtime permet de présenter tout format de mémoire tampon d’arrière-plan valide à n’importe quel format de bureau.</span><span class="sxs-lookup"><span data-stu-id="ec546-126">The set of possible back buffer formats is constrained, but the runtime will allow any valid back buffer format to be presented to any desktop format.</span></span> <span data-ttu-id="ec546-127">(Il existe une condition supplémentaire que l’appareil soit utilisable dans le Bureau ; les appareils ne fonctionnent généralement pas dans les modes 8 bits par pixel.)</span><span class="sxs-lookup"><span data-stu-id="ec546-127">(There is the additional requirement that the device be operable in the desktop; devices typically do not operate in 8 bits per pixel modes.)</span></span>

<span data-ttu-id="ec546-128">Les applications plein écran ne peuvent pas effectuer de conversion de couleurs.</span><span class="sxs-lookup"><span data-stu-id="ec546-128">Full-screen applications cannot do color conversion.</span></span>

</dd> <dt>

<span data-ttu-id="ec546-129">**BackBufferCount**</span><span class="sxs-lookup"><span data-stu-id="ec546-129">**BackBufferCount**</span></span>
</dt> <dd>

<span data-ttu-id="ec546-130">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ec546-130">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ec546-131">Cette valeur peut être comprise entre 0 et [D3DPRESENT \_ \_ tampons \_ ](d3dpresent-back-buffers.md) d’arrière-plan Max (ou [D3DPRESENT des \_ \_ mémoires tampons d’arrière-plan \_ Max \_ ](d3dpresent-back-buffers.md) , par exemple lors de l’utilisation de Direct3D 9Ex).</span><span class="sxs-lookup"><span data-stu-id="ec546-131">This value can be between 0 and [D3DPRESENT\_BACK\_BUFFERS\_MAX](d3dpresent-back-buffers.md) (or [D3DPRESENT\_BACK\_BUFFERS\_MAX\_EX](d3dpresent-back-buffers.md) when using Direct3D 9Ex).</span></span> <span data-ttu-id="ec546-132">Les valeurs de 0 sont traitées comme 1.</span><span class="sxs-lookup"><span data-stu-id="ec546-132">Values of 0 are treated as 1.</span></span> <span data-ttu-id="ec546-133">Si le nombre de mémoires tampons d’arrière-plan ne peut pas être créé, le runtime échouera à l’appel de la méthode et remplira cette valeur avec le nombre de mémoires tampons d’arrière-plan qui pourraient être créées.</span><span class="sxs-lookup"><span data-stu-id="ec546-133">If the number of back buffers cannot be created, the runtime will fail the method call and fill this value with the number of back buffers that could be created.</span></span> <span data-ttu-id="ec546-134">Par conséquent, une application peut appeler la méthode deux fois avec la même \_ structure de paramètres D3DPRESENT et s’attendre à ce qu’elle fonctionne la deuxième fois.</span><span class="sxs-lookup"><span data-stu-id="ec546-134">As a result, an application can call the method twice with the same D3DPRESENT\_PARAMETERS structure and expect it to work the second time.</span></span>

<span data-ttu-id="ec546-135">La méthode échoue si une mémoire tampon d’arrière-plan ne peut pas être créée.</span><span class="sxs-lookup"><span data-stu-id="ec546-135">The method fails if one back buffer cannot be created.</span></span> <span data-ttu-id="ec546-136">La valeur de **BackBufferCount** influence le jeu d’effets de permutation autorisés.</span><span class="sxs-lookup"><span data-stu-id="ec546-136">The value of **BackBufferCount** influences what set of swap effects are allowed.</span></span> <span data-ttu-id="ec546-137">Plus précisément, tous les \_ effets d’échange de copie D3DSWAPEFFECT nécessitent une seule mémoire tampon d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="ec546-137">Specifically, any D3DSWAPEFFECT\_COPY swap effect requires that there be exactly one back buffer.</span></span>

</dd> <dt>

<span data-ttu-id="ec546-138">**MultiSampleType**</span><span class="sxs-lookup"><span data-stu-id="ec546-138">**MultiSampleType**</span></span>
</dt> <dd>

<span data-ttu-id="ec546-139">Type : **[ **D3DMULTISAMPLE \_**](./d3dmultisample-type.md)**</span><span class="sxs-lookup"><span data-stu-id="ec546-139">Type: **[**D3DMULTISAMPLE\_TYPE**](./d3dmultisample-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ec546-140">Membre du type énuméré de [**\_ type D3DMULTISAMPLE**](./d3dmultisample-type.md) .</span><span class="sxs-lookup"><span data-stu-id="ec546-140">Member of the [**D3DMULTISAMPLE\_TYPE**](./d3dmultisample-type.md) enumerated type.</span></span> <span data-ttu-id="ec546-141">La valeur doit être D3DMULTISAMPLE \_ None, sauf si **SwapEffect** a été défini sur D3DSWAPEFFECT \_ Discard.</span><span class="sxs-lookup"><span data-stu-id="ec546-141">The value must be D3DMULTISAMPLE\_NONE unless **SwapEffect** has been set to D3DSWAPEFFECT\_DISCARD.</span></span> <span data-ttu-id="ec546-142">L’échantillonnage multiple est pris en charge uniquement si l’effet d’échange est D3DSWAPEFFECT \_ ignore.</span><span class="sxs-lookup"><span data-stu-id="ec546-142">Multisampling is supported only if the swap effect is D3DSWAPEFFECT\_DISCARD.</span></span>

</dd> <dt>

<span data-ttu-id="ec546-143">**MultiSampleQuality**</span><span class="sxs-lookup"><span data-stu-id="ec546-143">**MultiSampleQuality**</span></span>
</dt> <dd>

<span data-ttu-id="ec546-144">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ec546-144">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ec546-145">Niveau de qualité.</span><span class="sxs-lookup"><span data-stu-id="ec546-145">Quality level.</span></span> <span data-ttu-id="ec546-146">La plage valide est comprise entre zéro et un de moins que le niveau retourné par pQualityLevels utilisé par [**CheckDeviceMultiSampleType**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="ec546-146">The valid range is between zero and one less than the level returned by pQualityLevels used by [**CheckDeviceMultiSampleType**](/windows/desktop/api).</span></span> <span data-ttu-id="ec546-147">La transmission d’une valeur supérieure retourne l’erreur D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="ec546-147">Passing a larger value returns the error D3DERR\_INVALIDCALL.</span></span> <span data-ttu-id="ec546-148">Les valeurs jumelées des cibles de rendu ou des surfaces du stencil de profondeur et du [**\_ type de D3DMULTISAMPLE**](./d3dmultisample-type.md) doivent correspondre.</span><span class="sxs-lookup"><span data-stu-id="ec546-148">Paired values of render targets or of depth stencil surfaces and [**D3DMULTISAMPLE\_TYPE**](./d3dmultisample-type.md) must match.</span></span>

</dd> <dt>

<span data-ttu-id="ec546-149">**SwapEffect**</span><span class="sxs-lookup"><span data-stu-id="ec546-149">**SwapEffect**</span></span>
</dt> <dd>

<span data-ttu-id="ec546-150">Type : **[ **D3DSWAPEFFECT**](./d3dswapeffect.md)**</span><span class="sxs-lookup"><span data-stu-id="ec546-150">Type: **[**D3DSWAPEFFECT**](./d3dswapeffect.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ec546-151">Membre du type énuméré [**D3DSWAPEFFECT**](./d3dswapeffect.md) .</span><span class="sxs-lookup"><span data-stu-id="ec546-151">Member of the [**D3DSWAPEFFECT**](./d3dswapeffect.md) enumerated type.</span></span> <span data-ttu-id="ec546-152">Le runtime garantit la sémantique implicite concernant le comportement de l’échange de mémoire tampon ; par conséquent, si **Windowed** a la **valeur true** et que **SwapEffect** a la valeur D3DSWAPEFFECT \_ Flip, le runtime crée une mémoire tampon d’arrière-plan supplémentaire et copie celle qui devient la mémoire tampon d’arrière-plan au moment de la présentation.</span><span class="sxs-lookup"><span data-stu-id="ec546-152">The runtime will guarantee the implied semantics concerning buffer swap behavior; therefore, if **Windowed** is **TRUE** and **SwapEffect** is set to D3DSWAPEFFECT\_FLIP, the runtime will create one extra back buffer and copy whichever becomes the front buffer at presentation time.</span></span>

<span data-ttu-id="ec546-153">D3DSWAPEFFECT \_ Copy requiert que **BackBufferCount** soit défini sur 1.</span><span class="sxs-lookup"><span data-stu-id="ec546-153">D3DSWAPEFFECT\_COPY requires that **BackBufferCount** be set to 1.</span></span>

<span data-ttu-id="ec546-154">D3DSWAPEFFECT \_ Discard sera appliqué dans le runtime de débogage en remplissant toute mémoire tampon avec un bruit après sa présentation.</span><span class="sxs-lookup"><span data-stu-id="ec546-154">D3DSWAPEFFECT\_DISCARD will be enforced in the debug runtime by filling any buffer with noise after it is presented.</span></span>



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec546-155">Différences entre Direct3D9 et Direct3D9Ex</span><span class="sxs-lookup"><span data-stu-id="ec546-155">Differences between Direct3D9 and Direct3D9Ex</span></span><br/> <span data-ttu-id="ec546-156">Dans Direct3D9Ex, D3DSWAPEFFECT \_ FLIPEX est ajouté pour désigner le moment où une application adopte le mode Flip.</span><span class="sxs-lookup"><span data-stu-id="ec546-156">In Direct3D9Ex, D3DSWAPEFFECT\_FLIPEX is added to designate when an application is adopting flip mode.</span></span> <span data-ttu-id="ec546-157">Autrement dit, Whan le frame d’une application est passé en mode de fenêtre (au lieu d’être copié) au Gestionnaire de fenêtrage (DWM) pour la composition.</span><span class="sxs-lookup"><span data-stu-id="ec546-157">That is, whan an application's frame is passed in window's mode (instead of copied) to the Desktop Window Manager(DWM) for composition.</span></span> <span data-ttu-id="ec546-158">Le mode Flip fournit une bande passante de mémoire plus efficace et permet à une application de tirer parti des statistiques de présentation plein écran.</span><span class="sxs-lookup"><span data-stu-id="ec546-158">Flip mode provides more efficient memory bandwidth and enables an application to take advantage of full-screen-present statistics.</span></span> <span data-ttu-id="ec546-159">Elle ne modifie pas le comportement plein écran.</span><span class="sxs-lookup"><span data-stu-id="ec546-159">It does not change full screen behavior.</span></span> <span data-ttu-id="ec546-160">Le comportement en mode Flip est disponible à partir de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ec546-160">Flip mode behavior is available beginning with Windows 7.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ec546-161">**hDeviceWindow**</span><span class="sxs-lookup"><span data-stu-id="ec546-161">**hDeviceWindow**</span></span>
</dt> <dd>

<span data-ttu-id="ec546-162">Type : **[ **HWND**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ec546-162">Type: **[**HWND**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ec546-163">La fenêtre de l’appareil détermine l’emplacement et la taille de la mémoire tampon d’arrière-plan sur l’écran.</span><span class="sxs-lookup"><span data-stu-id="ec546-163">The device window determines the location and size of the back buffer on screen.</span></span> <span data-ttu-id="ec546-164">Utilisé par Direct3D lorsque le contenu de la mémoire tampon d’arrière-plan est copié dans le tampon d’avant pendant la [**présente**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).</span><span class="sxs-lookup"><span data-stu-id="ec546-164">This is used by Direct3D when the back buffer contents are copied to the front buffer during [**Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).</span></span>

-   <span data-ttu-id="ec546-165">Pour une application en plein écran, il s’agit d’un handle vers la fenêtre supérieure (qui est la fenêtre de focus).</span><span class="sxs-lookup"><span data-stu-id="ec546-165">For a full-screen application, this is a handle to the top window (which is the focus window).</span></span>

    <span data-ttu-id="ec546-166">Pour les applications qui utilisent plusieurs appareils plein écran (par exemple, un système multimoniteur), un seul périphérique peut utiliser la fenêtre de focus comme fenêtre d’appareil.</span><span class="sxs-lookup"><span data-stu-id="ec546-166">For applications that use multiple full-screen devices (such as a multimonitor system), exactly one device can use the focus window as the device window.</span></span> <span data-ttu-id="ec546-167">Tous les autres appareils doivent avoir des fenêtres d’appareil uniques.</span><span class="sxs-lookup"><span data-stu-id="ec546-167">All other devices must have unique device windows.</span></span>

-   <span data-ttu-id="ec546-168">Pour une application en mode fenêtre, ce descripteur est la fenêtre cible par défaut pour le [**présent**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).</span><span class="sxs-lookup"><span data-stu-id="ec546-168">For a windowed-mode application, this handle will be the default target window for [**Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).</span></span> <span data-ttu-id="ec546-169">Si ce handle est **null**, la fenêtre de focus est prise.</span><span class="sxs-lookup"><span data-stu-id="ec546-169">If this handle is **NULL**, the focus window will be taken.</span></span>

<span data-ttu-id="ec546-170">Notez qu’aucune tentative n’est effectuée par le runtime pour refléter les modifications apportées par l’utilisateur dans la taille de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="ec546-170">Note that no attempt is made by the runtime to reflect user changes in window size.</span></span> <span data-ttu-id="ec546-171">La mémoire tampon d’arrière-plan n’est pas réinitialisée implicitement lorsque cette fenêtre est réinitialisée.</span><span class="sxs-lookup"><span data-stu-id="ec546-171">The back buffer is not implicitly reset when this window is reset.</span></span> <span data-ttu-id="ec546-172">Toutefois, la méthode [**présente**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) effectue automatiquement le suivi des modifications de position de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="ec546-172">However, the [**Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) method does automatically track window position changes.</span></span>

</dd> <dt>

<span data-ttu-id="ec546-173">**Fenêtrées**</span><span class="sxs-lookup"><span data-stu-id="ec546-173">**Windowed**</span></span>
</dt> <dd>

<span data-ttu-id="ec546-174">Type : **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ec546-174">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ec546-175">**True** si l’application s’exécute sous la fenêtre ; **False** si l’application s’exécute en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="ec546-175">**TRUE** if the application runs windowed; **FALSE** if the application runs full-screen.</span></span>

</dd> <dt>

<span data-ttu-id="ec546-176">**EnableAutoDepthStencil**</span><span class="sxs-lookup"><span data-stu-id="ec546-176">**EnableAutoDepthStencil**</span></span>
</dt> <dd>

<span data-ttu-id="ec546-177">Type : **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ec546-177">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ec546-178">Si cette valeur est **true**, Direct3D gère les tampons de profondeur pour l’application.</span><span class="sxs-lookup"><span data-stu-id="ec546-178">If this value is **TRUE**, Direct3D will manage depth buffers for the application.</span></span> <span data-ttu-id="ec546-179">L’appareil crée une mémoire tampon de stencil de profondeur lors de sa création.</span><span class="sxs-lookup"><span data-stu-id="ec546-179">The device will create a depth-stencil buffer when it is created.</span></span> <span data-ttu-id="ec546-180">La mémoire tampon du stencil de profondeur est définie automatiquement en tant que cible de rendu de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ec546-180">The depth-stencil buffer will be automatically set as the render target of the device.</span></span> <span data-ttu-id="ec546-181">Lorsque l’appareil est réinitialisé, la mémoire tampon du stencil de profondeur est automatiquement détruite et recréée dans la nouvelle taille.</span><span class="sxs-lookup"><span data-stu-id="ec546-181">When the device is reset, the depth-stencil buffer will be automatically destroyed and recreated in the new size.</span></span>

<span data-ttu-id="ec546-182">Si EnableAutoDepthStencil a la **valeur true**, AutoDepthStencilFormat doit être un format de stencil de profondeur valide.</span><span class="sxs-lookup"><span data-stu-id="ec546-182">If EnableAutoDepthStencil is **TRUE**, then AutoDepthStencilFormat must be a valid depth-stencil format.</span></span>

</dd> <dt>

<span data-ttu-id="ec546-183">**AutoDepthStencilFormat**</span><span class="sxs-lookup"><span data-stu-id="ec546-183">**AutoDepthStencilFormat**</span></span>
</dt> <dd>

<span data-ttu-id="ec546-184">Type : **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="ec546-184">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ec546-185">Membre du type énuméré [D3DFORMAT](d3dformat.md) .</span><span class="sxs-lookup"><span data-stu-id="ec546-185">Member of the [D3DFORMAT](d3dformat.md) enumerated type.</span></span> <span data-ttu-id="ec546-186">Format de la surface de stencil de profondeur automatique que l’appareil va créer.</span><span class="sxs-lookup"><span data-stu-id="ec546-186">The format of the automatic depth-stencil surface that the device will create.</span></span> <span data-ttu-id="ec546-187">Ce membre est ignoré, sauf si **EnableAutoDepthStencil** a la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="ec546-187">This member is ignored unless **EnableAutoDepthStencil** is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="ec546-188">**Indicateurs**</span><span class="sxs-lookup"><span data-stu-id="ec546-188">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="ec546-189">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ec546-189">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ec546-190">Une des constantes [D3DPRESENTFLAG](d3dpresentflag.md) .</span><span class="sxs-lookup"><span data-stu-id="ec546-190">One of the [D3DPRESENTFLAG](d3dpresentflag.md) constants.</span></span>

</dd> <dt>

<span data-ttu-id="ec546-191">**RefreshRateInHz plein écran \_**</span><span class="sxs-lookup"><span data-stu-id="ec546-191">**FullScreen\_RefreshRateInHz**</span></span>
</dt> <dd>

<span data-ttu-id="ec546-192">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ec546-192">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ec546-193">Vitesse à laquelle la carte d’affichage actualise l’écran.</span><span class="sxs-lookup"><span data-stu-id="ec546-193">The rate at which the display adapter refreshes the screen.</span></span> <span data-ttu-id="ec546-194">La valeur dépend du mode dans lequel l’application s’exécute :</span><span class="sxs-lookup"><span data-stu-id="ec546-194">The value depends on the mode in which the application is running:</span></span>

-   <span data-ttu-id="ec546-195">Pour le mode fenêtre, la fréquence d’actualisation doit être 0.</span><span class="sxs-lookup"><span data-stu-id="ec546-195">For windowed mode, the refresh rate must be 0.</span></span>
-   <span data-ttu-id="ec546-196">Pour le mode plein écran, la fréquence d’actualisation est l’un des taux d’actualisation retournés par [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).</span><span class="sxs-lookup"><span data-stu-id="ec546-196">For full-screen mode, the refresh rate is one of the refresh rates returned by [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).</span></span>

</dd> <dt>

<span data-ttu-id="ec546-197">**PresentationInterval**</span><span class="sxs-lookup"><span data-stu-id="ec546-197">**PresentationInterval**</span></span>
</dt> <dd>

<span data-ttu-id="ec546-198">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ec546-198">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ec546-199">Vitesse maximale à laquelle les mémoires tampons d’arrière-plan de la chaîne de permutation peuvent être présentées au tampon d’avant.</span><span class="sxs-lookup"><span data-stu-id="ec546-199">The maximum rate at which the swap chain's back buffers can be presented to the front buffer.</span></span> <span data-ttu-id="ec546-200">Pour obtenir une explication détaillée des modes et des intervalles pris en charge, consultez [D3DPRESENT](d3dpresent.md).</span><span class="sxs-lookup"><span data-stu-id="ec546-200">For a detailed explanation of the modes and the intervals that are supported, see [D3DPRESENT](d3dpresent.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ec546-201">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ec546-201">Requirements</span></span>



| <span data-ttu-id="ec546-202">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ec546-202">Requirement</span></span> | <span data-ttu-id="ec546-203">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec546-203">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec546-204">En-tête</span><span class="sxs-lookup"><span data-stu-id="ec546-204">Header</span></span><br/> | <dl> <span data-ttu-id="ec546-205"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec546-205"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec546-206">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec546-206">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec546-207">Structures Direct3D</span><span class="sxs-lookup"><span data-stu-id="ec546-207">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="ec546-208">**CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="ec546-208">**CreateDevice**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)
</dt> <dt>

[<span data-ttu-id="ec546-209">**CreateAdditionalSwapChain**</span><span class="sxs-lookup"><span data-stu-id="ec546-209">**CreateAdditionalSwapChain**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain)
</dt> <dt>

[<span data-ttu-id="ec546-210">**Présent**</span><span class="sxs-lookup"><span data-stu-id="ec546-210">**Present**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)
</dt> <dt>

[<span data-ttu-id="ec546-211">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="ec546-211">**Reset**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)
</dt> </dl>

 

 
