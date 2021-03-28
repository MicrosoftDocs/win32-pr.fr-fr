---
title: Méthode ID3DX11Effect IsOptimized (D3dx11effect. h)
description: Testez un effet pour voir si les métadonnées de réflexion ont été supprimées de la mémoire.
ms.assetid: fb0a876b-7419-45b7-97fe-8352dd97d8c5
keywords:
- Méthode IsOptimized Direct3D 11
- Méthode IsOptimized Direct3D 11, interface ID3DX11Effect
- Interface ID3DX11Effect Direct3D 11, méthode IsOptimized
topic_type:
- apiref
api_name:
- ID3DX11Effect.IsOptimized
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18be8901a58715e3bd8aaaa49ae40be07e7e9dc8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323193"
---
# <a name="id3dx11effectisoptimized-method"></a><span data-ttu-id="81292-106">ID3DX11Effect :: IsOptimized, méthode</span><span class="sxs-lookup"><span data-stu-id="81292-106">ID3DX11Effect::IsOptimized method</span></span>

<span data-ttu-id="81292-107">Testez un effet pour voir si les métadonnées de réflexion ont été supprimées de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="81292-107">Test an effect to see if the reflection metadata has been removed from memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="81292-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="81292-108">Syntax</span></span>


```C++
BOOL IsOptimized();
```



## <a name="parameters"></a><span data-ttu-id="81292-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="81292-109">Parameters</span></span>

<span data-ttu-id="81292-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="81292-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="81292-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="81292-111">Return value</span></span>

<span data-ttu-id="81292-112">Type : **[ **bool**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="81292-112">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="81292-113">**True** si l’effet est optimisé ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="81292-113">**TRUE** if the effect is optimized; otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="81292-114">Notes</span><span class="sxs-lookup"><span data-stu-id="81292-114">Remarks</span></span>

<span data-ttu-id="81292-115">Un effet utilise l’espace mémoire de deux façons différentes : pour stocker les informations requises par le runtime pour exécuter un effet, et pour stocker les métadonnées requises pour répercuter les informations dans une application à l’aide de l’API.</span><span class="sxs-lookup"><span data-stu-id="81292-115">An effect uses memory space two different ways: to store the information required by the runtime to execute an effect, and to store the metadata required to reflect information back to an application using the API.</span></span> <span data-ttu-id="81292-116">Vous pouvez réduire la quantité de mémoire requise par un effet en appelant [**ID3DX11Effect :: Optimize**](id3dx11effect-optimize.md) , qui supprime les métadonnées de réflexion de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="81292-116">You can minimize the amount of memory required by an effect by calling [**ID3DX11Effect::Optimize**](id3dx11effect-optimize.md) which removes the reflection metadata from memory.</span></span> <span data-ttu-id="81292-117">Bien entendu, les méthodes d’API pour lire des variables ne fonctionnent plus une fois que les données de réflexion ont été supprimées.</span><span class="sxs-lookup"><span data-stu-id="81292-117">Of course, API methods to read variables will no longer work once reflection data has been removed.</span></span>

> [!Note]  
> <span data-ttu-id="81292-118">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="81292-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="81292-119">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="81292-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="81292-120">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="81292-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="81292-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="81292-121">Requirements</span></span>



| <span data-ttu-id="81292-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="81292-122">Requirement</span></span> | <span data-ttu-id="81292-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="81292-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81292-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="81292-124">Header</span></span><br/>  | <dl> <span data-ttu-id="81292-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="81292-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="81292-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="81292-126">Library</span></span><br/> | <dl> <span data-ttu-id="81292-127"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="81292-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81292-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81292-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81292-129">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="81292-129">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

