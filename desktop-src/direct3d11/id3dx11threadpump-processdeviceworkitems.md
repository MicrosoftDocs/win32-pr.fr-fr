---
title: Méthode ID3DX11ThreadPump ProcessDeviceWorkItems (D3DX11core. h)
description: 'Remarque : la bibliothèque de l’utilitaire D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store. Définit les éléments de travail sur l’appareil une fois qu’ils ont terminé le chargement et le traitement.'
ms.assetid: 154e6ea5-0a88-4c8a-9c20-e7fbf95f1946
keywords:
- Méthode ProcessDeviceWorkItems Direct3D 11
- Méthode ProcessDeviceWorkItems Direct3D 11, interface ID3DX11ThreadPump
- Interface ID3DX11ThreadPump Direct3D 11, méthode ProcessDeviceWorkItems
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump.ProcessDeviceWorkItems
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ad570785ac7dc36fb5dd9d464e97ef46f52ca93
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974527"
---
# <a name="id3dx11threadpumpprocessdeviceworkitems-method"></a><span data-ttu-id="1bb58-107">ID3DX11ThreadPump ::P méthode rocessDeviceWorkItems</span><span class="sxs-lookup"><span data-stu-id="1bb58-107">ID3DX11ThreadPump::ProcessDeviceWorkItems method</span></span>

> [!Note]  
> <span data-ttu-id="1bb58-108">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="1bb58-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="1bb58-109">Définit les éléments de travail sur l’appareil une fois qu’ils ont terminé le chargement et le traitement.</span><span class="sxs-lookup"><span data-stu-id="1bb58-109">Sets work items to the device after they have finished loading and processing.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bb58-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1bb58-110">Syntax</span></span>


```C++
HRESULT ProcessDeviceWorkItems(
  [in] UINT iWorkItemCount
);
```



## <a name="parameters"></a><span data-ttu-id="1bb58-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1bb58-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1bb58-112">*iWorkItemCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1bb58-112">*iWorkItemCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bb58-113">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="1bb58-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="1bb58-114">Nombre d’éléments de travail à définir sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="1bb58-114">The number of work items to set to the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1bb58-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1bb58-115">Return value</span></span>

<span data-ttu-id="1bb58-116">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1bb58-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1bb58-117">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="1bb58-117">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1bb58-118">Notes</span><span class="sxs-lookup"><span data-stu-id="1bb58-118">Remarks</span></span>

<span data-ttu-id="1bb58-119">Lorsque la pompe de thread a terminé le chargement et le traitement d’une ressource ou d’un nuanceur, elle le contiendra dans une file d’attente jusqu’à ce que cette API soit appelée, auquel cas les éléments traités seront définis sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="1bb58-119">When the thread pump has finished loading and processing a resource or shader, it will hold it in a queue until this API is called, at which point the processed items will be set to the device.</span></span> <span data-ttu-id="1bb58-120">Cela est utile pour contrôler la quantité de traitement consacrée à la liaison de ressources à l’appareil pour chaque trame.</span><span class="sxs-lookup"><span data-stu-id="1bb58-120">This is useful for controlling the amount of processing that is spent on binding resources to the device for each frame.</span></span>

<span data-ttu-id="1bb58-121">En guise d’exemple de l’utilisation de cette API, imaginons que vous approchez de la fin d’un niveau de votre jeu et que vous souhaitez commencer à précharger les textures, les nuanceurs et les autres ressources pour le niveau suivant.</span><span class="sxs-lookup"><span data-stu-id="1bb58-121">As an example of how one might use this API, say you are nearing the end of one level in your game and you want to begin preloading the textures, shaders, and other resources for the next level.</span></span> <span data-ttu-id="1bb58-122">La pompe de threads démarre le chargement, la décompression et le traitement des ressources et des nuanceurs sur un thread séparé jusqu’à ce qu’ils soient prêts à être définis sur l’appareil. à partir de là, il les laisse dans une file d’attente.</span><span class="sxs-lookup"><span data-stu-id="1bb58-122">The thread pump will begin loading, decompressing, and processing the resources and shaders on a separate thread until they are ready to be set to the device, at which point it will leave them in a queue.</span></span> <span data-ttu-id="1bb58-123">Il se peut que vous ne souhaitiez pas définir l’ensemble des ressources et des nuanceurs sur l’appareil en une seule fois, car cela peut entraîner un ralentissement de la vitesse d’exécution d’un jeu.</span><span class="sxs-lookup"><span data-stu-id="1bb58-123">One may not want to set all the resources and shaders to the device at once because this may cause a noticeable temporary slow down in the game's performance.</span></span> <span data-ttu-id="1bb58-124">Par conséquent, cette API peut être appelée une fois par frame afin que seuls les petits éléments de travail soient définis sur le périphérique de chaque trame, répartissant ainsi la charge de travail des ressources de liaison sur le périphérique sur plusieurs frames.</span><span class="sxs-lookup"><span data-stu-id="1bb58-124">So, this API could be called once per frame so that only a small number work items would be set to the device on each frame, thereby spreading the work load of binding resources to the device over several frames.</span></span>

## <a name="requirements"></a><span data-ttu-id="1bb58-125">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1bb58-125">Requirements</span></span>



| <span data-ttu-id="1bb58-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1bb58-126">Requirement</span></span> | <span data-ttu-id="1bb58-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="1bb58-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1bb58-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="1bb58-128">Header</span></span><br/>  | <dl> <span data-ttu-id="1bb58-129"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="1bb58-129"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="1bb58-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1bb58-130">Library</span></span><br/> | <dl> <span data-ttu-id="1bb58-131"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1bb58-131"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1bb58-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1bb58-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bb58-133">ID3DX11ThreadPump</span><span class="sxs-lookup"><span data-stu-id="1bb58-133">ID3DX11ThreadPump</span></span>](id3dx11threadpump.md)
</dt> <dt>

[<span data-ttu-id="1bb58-134">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="1bb58-134">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

