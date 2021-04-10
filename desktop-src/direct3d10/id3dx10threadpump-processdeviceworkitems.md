---
description: Définissez les éléments de travail sur l’appareil une fois qu’ils ont terminé le chargement et le traitement.
ms.assetid: 67a9fcb2-3513-413d-ac3d-9988ef7b5a1f
title: ID3DX10ThreadPump ::P méthode rocessDeviceWorkItems (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10ThreadPump.ProcessDeviceWorkItems
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 88b98d68e4e0e47b2c8e7f9a2e095565c53e2561
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116299"
---
# <a name="id3dx10threadpumpprocessdeviceworkitems-method"></a><span data-ttu-id="c37a2-103">ID3DX10ThreadPump ::P méthode rocessDeviceWorkItems</span><span class="sxs-lookup"><span data-stu-id="c37a2-103">ID3DX10ThreadPump::ProcessDeviceWorkItems method</span></span>

<span data-ttu-id="c37a2-104">Définissez les éléments de travail sur l’appareil une fois qu’ils ont terminé le chargement et le traitement.</span><span class="sxs-lookup"><span data-stu-id="c37a2-104">Set work items to the device after they have finished loading and processing.</span></span> <span data-ttu-id="c37a2-105">Lorsque la pompe de thread a terminé le chargement et le traitement d’une ressource ou d’un nuanceur, elle le contiendra dans une file d’attente jusqu’à ce que cette API soit appelée, auquel cas les éléments traités seront définis sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c37a2-105">When the thread pump has finished loading and processing a resource or shader, it will hold it in a queue until this API is called, at which point the processed items will be set to the device.</span></span> <span data-ttu-id="c37a2-106">Cela est utile pour contrôler la quantité de traitement consacrée à la liaison de ressources à l’appareil pour chaque trame.</span><span class="sxs-lookup"><span data-stu-id="c37a2-106">This is useful for controlling the amount of processing that is spent on binding resources to the device for each frame.</span></span> <span data-ttu-id="c37a2-107">Consultez la section Remarques.</span><span class="sxs-lookup"><span data-stu-id="c37a2-107">See remarks.</span></span>

## <a name="syntax"></a><span data-ttu-id="c37a2-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c37a2-108">Syntax</span></span>


```C++
HRESULT ProcessDeviceWorkItems(
  [in] UINT iWorkItemCount
);
```



## <a name="parameters"></a><span data-ttu-id="c37a2-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c37a2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c37a2-110">*iWorkItemCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c37a2-110">*iWorkItemCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c37a2-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c37a2-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c37a2-112">Nombre d’éléments de travail à définir sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c37a2-112">The number of work items to set to the device.</span></span> <span data-ttu-id="c37a2-113">ProcessDeviceObjectCreation va créer au maximum objets iWorkItemCount.</span><span class="sxs-lookup"><span data-stu-id="c37a2-113">ProcessDeviceObjectCreation will create at most iWorkItemCount objects.</span></span> <span data-ttu-id="c37a2-114">S’il n’y a pas assez d’éléments de travail dans la file d’attente pour traiter les objets iWorkItemCount, ProcessDeviceObjectCreation créera autant d’objets d’appareil qu’il y a d’éléments dans la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="c37a2-114">If there are not enough work items in the queue to process iWorkItemCount objects, ProcessDeviceObjectCreation will create as many device objects as there are items in the queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c37a2-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c37a2-115">Return value</span></span>

<span data-ttu-id="c37a2-116">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c37a2-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c37a2-117">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="c37a2-117">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c37a2-118">Notes</span><span class="sxs-lookup"><span data-stu-id="c37a2-118">Remarks</span></span>

<span data-ttu-id="c37a2-119">En guise d’exemple de l’utilisation de cette API, imaginons que vous approchez de la fin d’un niveau de votre jeu et que vous souhaitez commencer à précharger les textures, les nuanceurs et les autres ressources pour le niveau suivant.</span><span class="sxs-lookup"><span data-stu-id="c37a2-119">As an example of how one might use this API, say you are nearing the end of one level in your game and you want to begin preloading the textures, shaders, and other resources for the next level.</span></span> <span data-ttu-id="c37a2-120">La pompe de threads démarre le chargement, la décompression et le traitement des ressources et des nuanceurs sur un thread séparé jusqu’à ce qu’ils soient prêts à être définis sur l’appareil. à partir de là, il les laisse dans une file d’attente.</span><span class="sxs-lookup"><span data-stu-id="c37a2-120">The thread pump will begin loading, decompressing, and processing the resources and shaders on a separate thread until they are ready to be set to the device, at which point it will leave them in a queue.</span></span> <span data-ttu-id="c37a2-121">Il se peut que vous ne souhaitiez pas définir toutes les ressources et tous les nuanceurs sur l’appareil en même temps, car cela peut entraîner un ralentissement temporaire pouvant être remarqué dans les performances du jeu.</span><span class="sxs-lookup"><span data-stu-id="c37a2-121">One may not want to set all the resources and shaders to the device at once because this may cause a noticable temporary slow down in the game's performance.</span></span> <span data-ttu-id="c37a2-122">Par conséquent, cette API peut être appelée une fois par frame afin que seuls les petits éléments de travail soient définis sur le périphérique de chaque trame, répartissant ainsi la charge de travail des ressources de liaison sur l’appareil sur plusieurs trames et minimisant la probabilité d’un ralentissement des performances du jeu.</span><span class="sxs-lookup"><span data-stu-id="c37a2-122">So, this API could be called once per frame so that only a small number work items would be set to the device on each frame, thereby spreading the work load of binding resources to the device over several frames and minimizing the possibility of a noticable slow down in the game's performance.</span></span>

## <a name="requirements"></a><span data-ttu-id="c37a2-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c37a2-123">Requirements</span></span>



| <span data-ttu-id="c37a2-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c37a2-124">Requirement</span></span> | <span data-ttu-id="c37a2-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="c37a2-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c37a2-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="c37a2-126">Header</span></span><br/>  | <dl> <span data-ttu-id="c37a2-127"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="c37a2-127"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="c37a2-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c37a2-128">Library</span></span><br/> | <dl> <span data-ttu-id="c37a2-129"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c37a2-129"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c37a2-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c37a2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c37a2-131">ID3DX10ThreadPump</span><span class="sxs-lookup"><span data-stu-id="c37a2-131">ID3DX10ThreadPump</span></span>](id3dx10threadpump.md)
</dt> <dt>

[<span data-ttu-id="c37a2-132">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="c37a2-132">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
