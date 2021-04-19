---
title: Interface ID3DX11Effect (D3dx11effect. h)
description: Une interface ID3DX11Effect gère un ensemble d’objets d’État, de ressources et de nuanceurs pour l’implémentation d’un effet de rendu.
ms.assetid: 34429d51-6b45-4a62-bce1-50c4da02edac
keywords:
- Interface ID3DX11Effect Direct3D 11
- Interface ID3DX11Effect Direct3D 11, Description
topic_type:
- apiref
api_name:
- ID3DX11Effect
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51c9b945f09ad0424ecd6b546aefe68bea276ffc
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314452"
---
# <a name="id3dx11effect-interface"></a><span data-ttu-id="46c9c-105">Interface ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="46c9c-105">ID3DX11Effect interface</span></span>

<span data-ttu-id="46c9c-106">Une interface **ID3DX11Effect** gère un ensemble d’objets d’État, de ressources et de nuanceurs pour l’implémentation d’un effet de rendu.</span><span class="sxs-lookup"><span data-stu-id="46c9c-106">An **ID3DX11Effect** interface manages a set of state objects, resources, and shaders for implementing a rendering effect.</span></span>

## <a name="members"></a><span data-ttu-id="46c9c-107">Membres</span><span class="sxs-lookup"><span data-stu-id="46c9c-107">Members</span></span>

<span data-ttu-id="46c9c-108">L’interface **ID3DX11Effect** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="46c9c-108">The **ID3DX11Effect** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="46c9c-109">**ID3DX11Effect** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="46c9c-109">**ID3DX11Effect** also has these types of members:</span></span>

-   [<span data-ttu-id="46c9c-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="46c9c-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="46c9c-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="46c9c-111">Methods</span></span>

<span data-ttu-id="46c9c-112">L’interface **ID3DX11Effect** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="46c9c-112">The **ID3DX11Effect** interface has these methods.</span></span>



| <span data-ttu-id="46c9c-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="46c9c-113">Method</span></span>                                                                     | <span data-ttu-id="46c9c-114">Description</span><span class="sxs-lookup"><span data-stu-id="46c9c-114">Description</span></span>                                                                               |
|:---------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="46c9c-115">**CloneEffect**</span><span class="sxs-lookup"><span data-stu-id="46c9c-115">**CloneEffect**</span></span>](id3dx11effect-cloneeffect.md)                           | <span data-ttu-id="46c9c-116">Crée une copie d’une interface d’effet.</span><span class="sxs-lookup"><span data-stu-id="46c9c-116">Creates a copy of an effect interface.</span></span><br/>                                         |
| [<span data-ttu-id="46c9c-117">**GetClassLinkage**</span><span class="sxs-lookup"><span data-stu-id="46c9c-117">**GetClassLinkage**</span></span>](id3dx11effect-getclasslinkage.md)                   | <span data-ttu-id="46c9c-118">Obtient une interface de liaison de classe.</span><span class="sxs-lookup"><span data-stu-id="46c9c-118">Gets a class linkage interface.</span></span><br/>                                                |
| [<span data-ttu-id="46c9c-119">**GetConstantBufferByIndex**</span><span class="sxs-lookup"><span data-stu-id="46c9c-119">**GetConstantBufferByIndex**</span></span>](id3dx11effect-getconstantbufferbyindex.md) | <span data-ttu-id="46c9c-120">Obtient une mémoire tampon constante par index.</span><span class="sxs-lookup"><span data-stu-id="46c9c-120">Get a constant buffer by index.</span></span><br/>                                                |
| [<span data-ttu-id="46c9c-121">**GetConstantBufferByName**</span><span class="sxs-lookup"><span data-stu-id="46c9c-121">**GetConstantBufferByName**</span></span>](id3dx11effect-getconstantbufferbyname.md)   | <span data-ttu-id="46c9c-122">Obtient une mémoire tampon constante par nom.</span><span class="sxs-lookup"><span data-stu-id="46c9c-122">Get a constant buffer by name.</span></span><br/>                                                 |
| [<span data-ttu-id="46c9c-123">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="46c9c-123">**GetDesc**</span></span>](id3dx11effect-getdesc.md)                                   | <span data-ttu-id="46c9c-124">Obtient une description de l’effet.</span><span class="sxs-lookup"><span data-stu-id="46c9c-124">Get an effect description.</span></span><br/>                                                     |
| [<span data-ttu-id="46c9c-125">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="46c9c-125">**GetDevice**</span></span>](id3dx11effect-getdevice.md)                               | <span data-ttu-id="46c9c-126">Récupérez l’appareil qui a créé l’effet.</span><span class="sxs-lookup"><span data-stu-id="46c9c-126">Get the device that created the effect.</span></span><br/>                                        |
| [<span data-ttu-id="46c9c-127">**GetGroupByIndex**</span><span class="sxs-lookup"><span data-stu-id="46c9c-127">**GetGroupByIndex**</span></span>](id3dx11effect-getgroupbyindex.md)                   | <span data-ttu-id="46c9c-128">Obtient un groupe d’effets par index.</span><span class="sxs-lookup"><span data-stu-id="46c9c-128">Gets an effect group by index.</span></span><br/>                                                 |
| [<span data-ttu-id="46c9c-129">**GetGroupByName**</span><span class="sxs-lookup"><span data-stu-id="46c9c-129">**GetGroupByName**</span></span>](id3dx11effect-getgroupbyname.md)                     | <span data-ttu-id="46c9c-130">Obtient un groupe d’effets par nom.</span><span class="sxs-lookup"><span data-stu-id="46c9c-130">Gets an effect group by name.</span></span><br/>                                                  |
| [<span data-ttu-id="46c9c-131">**GetTechniqueByIndex**</span><span class="sxs-lookup"><span data-stu-id="46c9c-131">**GetTechniqueByIndex**</span></span>](id3dx11effect-gettechniquebyindex.md)           | <span data-ttu-id="46c9c-132">Obtient une technique par index.</span><span class="sxs-lookup"><span data-stu-id="46c9c-132">Get a technique by index.</span></span><br/>                                                      |
| [<span data-ttu-id="46c9c-133">**GetTechniqueByName**</span><span class="sxs-lookup"><span data-stu-id="46c9c-133">**GetTechniqueByName**</span></span>](id3dx11effect-gettechniquebyname.md)             | <span data-ttu-id="46c9c-134">Obtient une technique par nom.</span><span class="sxs-lookup"><span data-stu-id="46c9c-134">Get a technique by name.</span></span><br/>                                                       |
| [<span data-ttu-id="46c9c-135">**GetVariableByIndex**</span><span class="sxs-lookup"><span data-stu-id="46c9c-135">**GetVariableByIndex**</span></span>](id3dx11effect-getvariablebyindex.md)             | <span data-ttu-id="46c9c-136">Obtient une variable par index.</span><span class="sxs-lookup"><span data-stu-id="46c9c-136">Get a variable by index.</span></span><br/>                                                       |
| [<span data-ttu-id="46c9c-137">**GetVariableByName**</span><span class="sxs-lookup"><span data-stu-id="46c9c-137">**GetVariableByName**</span></span>](id3dx11effect-getvariablebyname.md)               | <span data-ttu-id="46c9c-138">Obtient une variable par nom.</span><span class="sxs-lookup"><span data-stu-id="46c9c-138">Get a variable by name.</span></span><br/>                                                        |
| [<span data-ttu-id="46c9c-139">**GetVariableBySemantic**</span><span class="sxs-lookup"><span data-stu-id="46c9c-139">**GetVariableBySemantic**</span></span>](id3dx11effect-getvariablebysemantic.md)       | <span data-ttu-id="46c9c-140">Obtenir une variable par sémantique.</span><span class="sxs-lookup"><span data-stu-id="46c9c-140">Get a variable by semantic.</span></span><br/>                                                    |
| [<span data-ttu-id="46c9c-141">**IsOptimized**</span><span class="sxs-lookup"><span data-stu-id="46c9c-141">**IsOptimized**</span></span>](id3dx11effect-isoptimized.md)                           | <span data-ttu-id="46c9c-142">Testez un effet pour voir si les métadonnées de réflexion ont été supprimées de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="46c9c-142">Test an effect to see if the reflection metadata has been removed from memory.</span></span><br/> |
| [<span data-ttu-id="46c9c-143">**IsValid**</span><span class="sxs-lookup"><span data-stu-id="46c9c-143">**IsValid**</span></span>](id3dx11effect-isvalid.md)                                   | <span data-ttu-id="46c9c-144">Testez un effet pour voir s’il contient une syntaxe valide.</span><span class="sxs-lookup"><span data-stu-id="46c9c-144">Test an effect to see if it contains valid syntax.</span></span><br/>                             |
| [<span data-ttu-id="46c9c-145">**Optimiser**</span><span class="sxs-lookup"><span data-stu-id="46c9c-145">**Optimize**</span></span>](id3dx11effect-optimize.md)                                 | <span data-ttu-id="46c9c-146">Réduisez la quantité de mémoire requise pour un effet.</span><span class="sxs-lookup"><span data-stu-id="46c9c-146">Minimize the amount of memory required for an effect.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="46c9c-147">Notes</span><span class="sxs-lookup"><span data-stu-id="46c9c-147">Remarks</span></span>

<span data-ttu-id="46c9c-148">Un effet est créé en appelant [**D3DX11CreateEffectFromMemory**](d3dx11createeffectfrommemory.md).</span><span class="sxs-lookup"><span data-stu-id="46c9c-148">An effect is created by calling [**D3DX11CreateEffectFromMemory**](d3dx11createeffectfrommemory.md).</span></span>

<span data-ttu-id="46c9c-149">Le système d’effet regroupe les informations requises pour le rendu dans un effet qui contient : les objets d’État pour l’affectation des modifications d’État dans les groupes, les ressources pour fournir des données d’entrée et le stockage des données de sortie, ainsi que les programmes qui contrôlent la façon dont le rendu est effectué appelé nuanceurs.</span><span class="sxs-lookup"><span data-stu-id="46c9c-149">The effect system groups the information required for rendering into an effect which contains: state objects for assigning state changes in groups, resources for supplying input data and storing output data, and programs that control how the rendering is done called shaders.</span></span>

> [!Note]  
> <span data-ttu-id="46c9c-150">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="46c9c-150">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="46c9c-151">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="46c9c-151">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="46c9c-152">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="46c9c-152">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

> [!Note]
>
> <span data-ttu-id="46c9c-153">Si vous appelez [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur un objet **ID3DX11Effect** pour récupérer l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , **QueryInterface** retourne E \_ nointerface.</span><span class="sxs-lookup"><span data-stu-id="46c9c-153">If you call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on an **ID3DX11Effect** object to retrieve the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface, **QueryInterface** returns E\_NOINTERFACE.</span></span> <span data-ttu-id="46c9c-154">Pour contourner ce problème, utilisez le code suivant :</span><span class="sxs-lookup"><span data-stu-id="46c9c-154">To work around this issue, use the following code:</span></span>
>
> <span codelanguage=""></span>
>
> <table>
> <colgroup>
> <col style="width: 100%" />
> </colgroup>
> <tbody>
> <tr class="odd">
> <td><pre><code>    IUnknown* pIUnknown = (IUnknown*)pEffect;
>     pIUnknown->AddRef();</code></pre></td>
> </tr>
> </tbody>
> </table>>
>  

## <a name="requirements"></a><span data-ttu-id="46c9c-155">Spécifications</span><span class="sxs-lookup"><span data-stu-id="46c9c-155">Requirements</span></span>

| <span data-ttu-id="46c9c-156">Condition requise</span><span class="sxs-lookup"><span data-stu-id="46c9c-156">Requirement</span></span> | <span data-ttu-id="46c9c-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="46c9c-157">Value</span></span> |
|-------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="46c9c-158">En-tête</span><span class="sxs-lookup"><span data-stu-id="46c9c-158">Header</span></span><br/>  | <dl> <span data-ttu-id="46c9c-159"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="46c9c-159"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="46c9c-160">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="46c9c-160">Library</span></span><br/> | <dl> <span data-ttu-id="46c9c-161"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="46c9c-161"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="46c9c-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="46c9c-162">See also</span></span>

[<span data-ttu-id="46c9c-163">Effets 11 interfaces</span><span class="sxs-lookup"><span data-stu-id="46c9c-163">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)

[<span data-ttu-id="46c9c-164">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="46c9c-164">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
