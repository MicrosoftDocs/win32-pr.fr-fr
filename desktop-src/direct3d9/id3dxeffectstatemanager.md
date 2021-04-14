---
description: Il s’agit d’une interface implémentée par l’utilisateur qui permet à un utilisateur de définir l’état de l’appareil à partir d’un effet.
ms.assetid: ccd3e456-e27b-4128-b20b-99ff8dafcbe1
title: Interface ID3DXEffectStateManager (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: fad9df739634625800c0a21fd9ba2a2823d70f8e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323069"
---
# <a name="id3dxeffectstatemanager-interface"></a><span data-ttu-id="adb60-103">Interface ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="adb60-103">ID3DXEffectStateManager interface</span></span>

<span data-ttu-id="adb60-104">Il s’agit d’une interface implémentée par l’utilisateur qui permet à un utilisateur de définir l’état de l’appareil à partir d’un effet.</span><span class="sxs-lookup"><span data-stu-id="adb60-104">This is a user-implemented interface that allows a user to set the device state from an effect.</span></span> <span data-ttu-id="adb60-105">Chacune des méthodes dans cette interface doit être implémentée par l’utilisateur et sera ensuite utilisée comme rappels de l’application lorsque l’une ou l’autre des conditions suivantes se présente :</span><span class="sxs-lookup"><span data-stu-id="adb60-105">Each of the methods in this interface must be implemented by the user and will then be used as callbacks to the application when either of the following occur:</span></span>

-   <span data-ttu-id="adb60-106">Un effet appelle [**ID3DXEffect :: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="adb60-106">An effect calls [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="adb60-107">L’état de l’effet est mis à jour de manière dynamique en appelant l’API de modification d’État appropriée.</span><span class="sxs-lookup"><span data-stu-id="adb60-107">Effect state is dynamically updated by calling the appropriate state change API.</span></span> <span data-ttu-id="adb60-108">Pour plus d’informations, consultez les pages de méthode individuelles.</span><span class="sxs-lookup"><span data-stu-id="adb60-108">See individual method pages for details.</span></span>

<span data-ttu-id="adb60-109">Quand une application utilise le gestionnaire d’État pour implémenter des rappels personnalisés, un effet n’enregistre et ne restaure plus automatiquement l’état lors de l’appel de [**ID3DXEffect :: BeginPass**](id3dxeffect--beginpass.md) et de [**ID3DXEffect :: EndPass**](id3dxeffect--endpass.md).</span><span class="sxs-lookup"><span data-stu-id="adb60-109">When an application uses the state manager to implement custom callbacks, an effect no longer automatically saves and restores state when calling [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md) and [**ID3DXEffect::EndPass**](id3dxeffect--endpass.md).</span></span> <span data-ttu-id="adb60-110">Étant donné que l’application a implémenté un comportement personnalisé d’enregistrement et de restauration dans les rappels, ce comportement automatique est contourné.</span><span class="sxs-lookup"><span data-stu-id="adb60-110">Because the application has implemented a custom save and restore behavior in the callbacks, this automatic behavior is bypassed.</span></span>

## <a name="members"></a><span data-ttu-id="adb60-111">Membres</span><span class="sxs-lookup"><span data-stu-id="adb60-111">Members</span></span>

<span data-ttu-id="adb60-112">L’interface **ID3DXEffectStateManager** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="adb60-112">The **ID3DXEffectStateManager** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="adb60-113">**ID3DXEffectStateManager** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="adb60-113">**ID3DXEffectStateManager** also has these types of members:</span></span>

-   [<span data-ttu-id="adb60-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="adb60-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="adb60-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="adb60-115">Methods</span></span>

<span data-ttu-id="adb60-116">L’interface **ID3DXEffectStateManager** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="adb60-116">The **ID3DXEffectStateManager** interface has these methods.</span></span>



| <span data-ttu-id="adb60-117">Méthode</span><span class="sxs-lookup"><span data-stu-id="adb60-117">Method</span></span>                                                                                | <span data-ttu-id="adb60-118">Description</span><span class="sxs-lookup"><span data-stu-id="adb60-118">Description</span></span>                                                                                                                  |
|:--------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="adb60-119">**Éclaircie**</span><span class="sxs-lookup"><span data-stu-id="adb60-119">**LightEnable**</span></span>](id3dxeffectstatemanager--lightenable.md)                           | <span data-ttu-id="adb60-120">Fonction de rappel qui doit être implémentée par un utilisateur pour activer/désactiver une lumière.</span><span class="sxs-lookup"><span data-stu-id="adb60-120">A callback function that must be implemented by a user to enable/disable a light.</span></span><br/>                                 |
| [<span data-ttu-id="adb60-121">**SetFVF**</span><span class="sxs-lookup"><span data-stu-id="adb60-121">**SetFVF**</span></span>](id3dxeffectstatemanager--setfvf.md)                                     | <span data-ttu-id="adb60-122">Fonction de rappel qui doit être implémentée par un utilisateur pour définir un code de Commission.</span><span class="sxs-lookup"><span data-stu-id="adb60-122">A callback function that must be implemented by a user to set a FVF code.</span></span><br/>                                         |
| [<span data-ttu-id="adb60-123">**SetLight**</span><span class="sxs-lookup"><span data-stu-id="adb60-123">**SetLight**</span></span>](id3dxeffectstatemanager--setlight.md)                                 | <span data-ttu-id="adb60-124">Fonction de rappel qui doit être implémentée par un utilisateur pour définir une lumière.</span><span class="sxs-lookup"><span data-stu-id="adb60-124">A callback function that must be implemented by a user to set a light.</span></span><br/>                                            |
| [<span data-ttu-id="adb60-125">**SetMaterial**</span><span class="sxs-lookup"><span data-stu-id="adb60-125">**SetMaterial**</span></span>](id3dxeffectstatemanager--setmaterial.md)                           | <span data-ttu-id="adb60-126">Fonction de rappel qui doit être implémentée par un utilisateur pour définir l’état du matériau.</span><span class="sxs-lookup"><span data-stu-id="adb60-126">A callback function that must be implemented by a user to set material state.</span></span><br/>                                     |
| [<span data-ttu-id="adb60-127">**SetNPatchMode**</span><span class="sxs-lookup"><span data-stu-id="adb60-127">**SetNPatchMode**</span></span>](id3dxeffectstatemanager--setnpatchmode.md)                       | <span data-ttu-id="adb60-128">Fonction de rappel qui doit être implémentée par un utilisateur pour définir le nombre de segments de la sous-division pour N-patchs.</span><span class="sxs-lookup"><span data-stu-id="adb60-128">A callback function that must be implemented by a user to set the number of subdivision segments for N-patches.</span></span><br/>   |
| [<span data-ttu-id="adb60-129">**SetPixelShader**</span><span class="sxs-lookup"><span data-stu-id="adb60-129">**SetPixelShader**</span></span>](id3dxeffectstatemanager--setpixelshader.md)                     | <span data-ttu-id="adb60-130">Fonction de rappel qui doit être implémentée par un utilisateur pour définir un nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="adb60-130">A callback function that must be implemented by a user to set a pixel shader.</span></span><br/>                                     |
| [<span data-ttu-id="adb60-131">**SetPixelShaderConstantB**</span><span class="sxs-lookup"><span data-stu-id="adb60-131">**SetPixelShaderConstantB**</span></span>](id3dxeffectstatemanager--setpixelshaderconstantb.md)   | <span data-ttu-id="adb60-132">Fonction de rappel qui doit être implémentée par un utilisateur pour définir un tableau de constantes booléennes de nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="adb60-132">A callback function that must be implemented by a user to set an array of vertex shader Boolean constants.</span></span><br/>        |
| [<span data-ttu-id="adb60-133">**SetPixelShaderConstantF**</span><span class="sxs-lookup"><span data-stu-id="adb60-133">**SetPixelShaderConstantF**</span></span>](id3dxeffectstatemanager--setpixelshaderconstantf.md)   | <span data-ttu-id="adb60-134">Fonction de rappel qui doit être implémentée par un utilisateur pour définir un tableau de constantes à virgule flottante de vertex shader.</span><span class="sxs-lookup"><span data-stu-id="adb60-134">A callback function that must be implemented by a user to set an array of vertex shader floating-point constants.</span></span><br/> |
| [<span data-ttu-id="adb60-135">**SetPixelShaderConstantI**</span><span class="sxs-lookup"><span data-stu-id="adb60-135">**SetPixelShaderConstantI**</span></span>](id3dxeffectstatemanager--setpixelshaderconstanti.md)   | <span data-ttu-id="adb60-136">Fonction de rappel qui doit être implémentée par un utilisateur pour définir un tableau de constantes entières de nuanceur de vertex.</span><span class="sxs-lookup"><span data-stu-id="adb60-136">A callback function that must be implemented by a user to set an array of vertex shader integer constants.</span></span><br/>        |
| [<span data-ttu-id="adb60-137">**SetRenderState**</span><span class="sxs-lookup"><span data-stu-id="adb60-137">**SetRenderState**</span></span>](id3dxeffectstatemanager--setrenderstate.md)                     | <span data-ttu-id="adb60-138">Fonction de rappel qui doit être implémentée par un utilisateur pour définir l’état de rendu.</span><span class="sxs-lookup"><span data-stu-id="adb60-138">A callback function that must be implemented by a user to set render state.</span></span><br/>                                       |
| [<span data-ttu-id="adb60-139">**SetSamplerState**</span><span class="sxs-lookup"><span data-stu-id="adb60-139">**SetSamplerState**</span></span>](id3dxeffectstatemanager--setsamplerstate.md)                   | <span data-ttu-id="adb60-140">Fonction de rappel qui doit être implémentée par un utilisateur pour définir un échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="adb60-140">A callback function that must be implemented by a user to set a sampler.</span></span><br/>                                          |
| [<span data-ttu-id="adb60-141">**SetTexture**</span><span class="sxs-lookup"><span data-stu-id="adb60-141">**SetTexture**</span></span>](id3dxeffectstatemanager--settexture.md)                             | <span data-ttu-id="adb60-142">Fonction de rappel qui doit être implémentée par un utilisateur pour définir une texture.</span><span class="sxs-lookup"><span data-stu-id="adb60-142">A callback function that must be implemented by a user to set a texture.</span></span><br/>                                          |
| [<span data-ttu-id="adb60-143">**SetTextureStageState**</span><span class="sxs-lookup"><span data-stu-id="adb60-143">**SetTextureStageState**</span></span>](id3dxeffectstatemanager--settexturestagestate.md)         | <span data-ttu-id="adb60-144">Fonction de rappel qui doit être implémentée par un utilisateur pour définir l’état de l’étape de texture.</span><span class="sxs-lookup"><span data-stu-id="adb60-144">A callback function that must be implemented by a user to set the texture stage state.</span></span><br/>                            |
| [<span data-ttu-id="adb60-145">**SetTransform**</span><span class="sxs-lookup"><span data-stu-id="adb60-145">**SetTransform**</span></span>](id3dxeffectstatemanager--settransform.md)                         | <span data-ttu-id="adb60-146">Fonction de rappel qui doit être implémentée par un utilisateur pour définir une transformation.</span><span class="sxs-lookup"><span data-stu-id="adb60-146">A callback function that must be implemented by a user to set a transform.</span></span><br/>                                        |
| [<span data-ttu-id="adb60-147">**SetVertexShader**</span><span class="sxs-lookup"><span data-stu-id="adb60-147">**SetVertexShader**</span></span>](id3dxeffectstatemanager--setvertexshader.md)                   | <span data-ttu-id="adb60-148">Fonction de rappel qui doit être implémentée par un utilisateur pour définir un nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="adb60-148">A callback function that must be implemented by a user to set a vertex shader.</span></span><br/>                                    |
| [<span data-ttu-id="adb60-149">**SetVertexShaderConstantB**</span><span class="sxs-lookup"><span data-stu-id="adb60-149">**SetVertexShaderConstantB**</span></span>](id3dxeffectstatemanager--setvertexshaderconstantb.md) | <span data-ttu-id="adb60-150">Fonction de rappel qui doit être implémentée par un utilisateur pour définir un tableau de constantes booléennes de nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="adb60-150">A callback function that must be implemented by a user to set an array of vertex shader Boolean constants.</span></span><br/>        |
| [<span data-ttu-id="adb60-151">**SetVertexShaderConstantF**</span><span class="sxs-lookup"><span data-stu-id="adb60-151">**SetVertexShaderConstantF**</span></span>](id3dxeffectstatemanager--setvertexshaderconstantf.md) | <span data-ttu-id="adb60-152">Fonction de rappel qui doit être implémentée par un utilisateur pour définir un tableau de constantes à virgule flottante de vertex shader.</span><span class="sxs-lookup"><span data-stu-id="adb60-152">A callback function that must be implemented by a user to set an array of vertex shader floating-point constants.</span></span><br/> |
| [<span data-ttu-id="adb60-153">**SetVertexShaderConstantI**</span><span class="sxs-lookup"><span data-stu-id="adb60-153">**SetVertexShaderConstantI**</span></span>](id3dxeffectstatemanager--setvertexshaderconstanti.md) | <span data-ttu-id="adb60-154">Fonction de rappel qui doit être implémentée par un utilisateur pour définir un tableau de constantes entières de nuanceur de vertex.</span><span class="sxs-lookup"><span data-stu-id="adb60-154">A callback function that must be implemented by a user to set an array of vertex shader integer constants.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="adb60-155">Notes</span><span class="sxs-lookup"><span data-stu-id="adb60-155">Remarks</span></span>

<span data-ttu-id="adb60-156">Un utilisateur crée une interface ID3DXEffectStateManager en implémentant une classe qui dérive de cette interface et en implémentant toutes les méthodes d’interface.</span><span class="sxs-lookup"><span data-stu-id="adb60-156">A user creates an ID3DXEffectStateManager interface by implementing a class that derives from this interface, and implementing all the interface methods.</span></span> <span data-ttu-id="adb60-157">Une fois l’interface créée, vous pouvez récupérer ou définir le gestionnaire d’État dans un effet à l’aide de [**ID3DXEffect :: GetStateManager**](id3dxeffect--getstatemanager.md) et [**ID3DXEffect :: SetStateManager**](id3dxeffect--setstatemanager.md).</span><span class="sxs-lookup"><span data-stu-id="adb60-157">Once the interface is created, you can get or set the state manager within an effect using [**ID3DXEffect::GetStateManager**](id3dxeffect--getstatemanager.md) and [**ID3DXEffect::SetStateManager**](id3dxeffect--setstatemanager.md).</span></span>

<span data-ttu-id="adb60-158">Le type LPD3DXEFFECTSTATEMANAGER est défini en tant que pointeur vers cette interface.</span><span class="sxs-lookup"><span data-stu-id="adb60-158">The LPD3DXEFFECTSTATEMANAGER type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXEffectStateManager ID3DXEffectStateManager;
typedef interface ID3DXEffectStateManager *LPD3DXEFFECTSTATEMANAGER;
```



## <a name="requirements"></a><span data-ttu-id="adb60-159">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="adb60-159">Requirements</span></span>



| <span data-ttu-id="adb60-160">Condition requise</span><span class="sxs-lookup"><span data-stu-id="adb60-160">Requirement</span></span> | <span data-ttu-id="adb60-161">Valeur</span><span class="sxs-lookup"><span data-stu-id="adb60-161">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="adb60-162">En-tête</span><span class="sxs-lookup"><span data-stu-id="adb60-162">Header</span></span><br/>  | <dl> <span data-ttu-id="adb60-163"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="adb60-163"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="adb60-164">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="adb60-164">Library</span></span><br/> | <dl> <span data-ttu-id="adb60-165"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="adb60-165"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="adb60-166">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="adb60-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adb60-167">Interfaces d’effet</span><span class="sxs-lookup"><span data-stu-id="adb60-167">Effect Interfaces</span></span>](dx9-graphics-reference-effects-interfaces.md)
</dt> </dl>

 

 
