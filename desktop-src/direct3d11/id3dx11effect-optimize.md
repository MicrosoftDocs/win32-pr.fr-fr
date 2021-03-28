---
title: ID3DX11Effect Optimize, méthode (D3dx11effect. h)
description: Réduisez la quantité de mémoire requise pour un effet.
ms.assetid: fa1d0769-6746-44f6-9979-31a534646884
keywords:
- Optimiser la méthode Direct3D 11
- Optimiser la méthode Direct3D 11, interface ID3DX11Effect
- Interface ID3DX11Effect Direct3D 11, méthode Optimize
topic_type:
- apiref
api_name:
- ID3DX11Effect.Optimize
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33fd6d200f6b22af46e648040e8299f40ec9ebae
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992332"
---
# <a name="id3dx11effectoptimize-method"></a><span data-ttu-id="73bd9-106">ID3DX11Effect :: Optimize, méthode</span><span class="sxs-lookup"><span data-stu-id="73bd9-106">ID3DX11Effect::Optimize method</span></span>

<span data-ttu-id="73bd9-107">Réduisez la quantité de mémoire requise pour un effet.</span><span class="sxs-lookup"><span data-stu-id="73bd9-107">Minimize the amount of memory required for an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="73bd9-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="73bd9-108">Syntax</span></span>


```C++
HRESULT Optimize();
```



## <a name="parameters"></a><span data-ttu-id="73bd9-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="73bd9-109">Parameters</span></span>

<span data-ttu-id="73bd9-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="73bd9-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="73bd9-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="73bd9-111">Return value</span></span>

<span data-ttu-id="73bd9-112">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="73bd9-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="73bd9-113">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="73bd9-113">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="73bd9-114">Notes</span><span class="sxs-lookup"><span data-stu-id="73bd9-114">Remarks</span></span>

<span data-ttu-id="73bd9-115">Un effet utilise l’espace mémoire de deux façons différentes : pour stocker les informations requises par le runtime pour exécuter un effet, et pour stocker les métadonnées requises pour répercuter les informations dans une application à l’aide de l’API.</span><span class="sxs-lookup"><span data-stu-id="73bd9-115">An effect uses memory space two different ways: to store the information required by the runtime to execute an effect, and to store the metadata required to reflect information back to an application using the API.</span></span> <span data-ttu-id="73bd9-116">Vous pouvez réduire la quantité de mémoire requise par un effet en appelant **ID3DX11Effect :: Optimize** , qui supprime les métadonnées de réflexion de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="73bd9-116">You can minimize the amount of memory required by an effect by calling **ID3DX11Effect::Optimize** which removes the reflection metadata from memory.</span></span> <span data-ttu-id="73bd9-117">Les méthodes d’API pour lire des variables ne fonctionnent plus une fois que les données de réflexion ont été supprimées.</span><span class="sxs-lookup"><span data-stu-id="73bd9-117">API methods to read variables will no longer work once reflection data has been removed.</span></span>

<span data-ttu-id="73bd9-118">Les méthodes suivantes échouent après l’appel de la méthode Optimize sur un effet.</span><span class="sxs-lookup"><span data-stu-id="73bd9-118">The following methods will fail after Optimize has been called on an effect.</span></span>

-   [<span data-ttu-id="73bd9-119">**ID3DX11Effect::GetConstantBufferByIndex**</span><span class="sxs-lookup"><span data-stu-id="73bd9-119">**ID3DX11Effect::GetConstantBufferByIndex**</span></span>](id3dx11effect-getconstantbufferbyindex.md)
-   [<span data-ttu-id="73bd9-120">**ID3DX11Effect::GetConstantBufferByName**</span><span class="sxs-lookup"><span data-stu-id="73bd9-120">**ID3DX11Effect::GetConstantBufferByName**</span></span>](id3dx11effect-getconstantbufferbyname.md)
-   [<span data-ttu-id="73bd9-121">**ID3DX11Effect::GetDesc**</span><span class="sxs-lookup"><span data-stu-id="73bd9-121">**ID3DX11Effect::GetDesc**</span></span>](id3dx11effect-getdesc.md)
-   [<span data-ttu-id="73bd9-122">**ID3DX11Effect::GetDevice**</span><span class="sxs-lookup"><span data-stu-id="73bd9-122">**ID3DX11Effect::GetDevice**</span></span>](id3dx11effect-getdevice.md)
-   [<span data-ttu-id="73bd9-123">**ID3DX11Effect::GetTechniqueByIndex**</span><span class="sxs-lookup"><span data-stu-id="73bd9-123">**ID3DX11Effect::GetTechniqueByIndex**</span></span>](id3dx11effect-gettechniquebyindex.md)
-   [<span data-ttu-id="73bd9-124">**ID3DX11Effect::GetTechniqueByName**</span><span class="sxs-lookup"><span data-stu-id="73bd9-124">**ID3DX11Effect::GetTechniqueByName**</span></span>](id3dx11effect-gettechniquebyname.md)
-   [<span data-ttu-id="73bd9-125">**ID3DX11Effect::GetVariableByIndex**</span><span class="sxs-lookup"><span data-stu-id="73bd9-125">**ID3DX11Effect::GetVariableByIndex**</span></span>](id3dx11effect-getvariablebyindex.md)
-   [<span data-ttu-id="73bd9-126">**ID3DX11Effect::GetVariableByName**</span><span class="sxs-lookup"><span data-stu-id="73bd9-126">**ID3DX11Effect::GetVariableByName**</span></span>](id3dx11effect-getvariablebyname.md)
-   [<span data-ttu-id="73bd9-127">**ID3DX11Effect::GetVariableBySemantic**</span><span class="sxs-lookup"><span data-stu-id="73bd9-127">**ID3DX11Effect::GetVariableBySemantic**</span></span>](id3dx11effect-getvariablebysemantic.md)

> [!Note]  
> <span data-ttu-id="73bd9-128">Les références récupérées avec ces méthodes avant d’appeler **ID3DX11Effect :: Optimize** sont toujours valides après l’appel de **ID3DX11Effect :: Optimize** .</span><span class="sxs-lookup"><span data-stu-id="73bd9-128">References retrieved with these methods before calling **ID3DX11Effect::Optimize** are still valid after **ID3DX11Effect::Optimize** is called.</span></span> <span data-ttu-id="73bd9-129">Cela permet à l’application d’accéder à toutes les variables, techniques et passes qu’elle utilise, d’appeler Optimize, puis d’utiliser l’effet.</span><span class="sxs-lookup"><span data-stu-id="73bd9-129">This allows the application to get all the variables, techniques, and passes it will use, call Optimize, and then use the effect.</span></span>

 

> [!Note]  
> <span data-ttu-id="73bd9-130">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="73bd9-130">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="73bd9-131">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="73bd9-131">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="73bd9-132">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="73bd9-132">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="73bd9-133">Spécifications</span><span class="sxs-lookup"><span data-stu-id="73bd9-133">Requirements</span></span>



| <span data-ttu-id="73bd9-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="73bd9-134">Requirement</span></span> | <span data-ttu-id="73bd9-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="73bd9-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73bd9-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="73bd9-136">Header</span></span><br/>  | <dl> <span data-ttu-id="73bd9-137"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="73bd9-137"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="73bd9-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="73bd9-138">Library</span></span><br/> | <dl> <span data-ttu-id="73bd9-139"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="73bd9-139"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73bd9-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="73bd9-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73bd9-141">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="73bd9-141">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

 





