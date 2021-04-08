---
description: Validez toutes les modifications apportées à un maillage sur l’appareil afin que les modifications puissent être rendues. Cela doit être appelé après la modification des données d’un maillage et avant son rendu. Un maillage ne peut pas être rendu, sauf s’il est validé sur l’appareil. Consultez la section Remarques.
ms.assetid: 26927553-d1d8-4745-85ad-a8a6fe949306
title: 'ID3DX10Mesh :: CommitToDevice, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.CommitToDevice
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 160f97a3a00ddc7bbf69989991b2794ab3d6e5e8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104043112"
---
# <a name="id3dx10meshcommittodevice-method"></a><span data-ttu-id="86ff5-106">ID3DX10Mesh :: CommitToDevice, méthode</span><span class="sxs-lookup"><span data-stu-id="86ff5-106">ID3DX10Mesh::CommitToDevice method</span></span>

<span data-ttu-id="86ff5-107">Validez toutes les modifications apportées à un maillage sur l’appareil afin que les modifications puissent être rendues.</span><span class="sxs-lookup"><span data-stu-id="86ff5-107">Commit any changes made to a mesh to the device so that the changes can be rendered.</span></span> <span data-ttu-id="86ff5-108">Cela doit être appelé après la modification des données d’un maillage et avant son rendu.</span><span class="sxs-lookup"><span data-stu-id="86ff5-108">This should be called after a mesh's data is altered and before it is rendered.</span></span> <span data-ttu-id="86ff5-109">Un maillage ne peut pas être rendu, sauf s’il est validé sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="86ff5-109">A mesh cannot be rendered unless it is committed to the device.</span></span> <span data-ttu-id="86ff5-110">Consultez la section Remarques.</span><span class="sxs-lookup"><span data-stu-id="86ff5-110">See remarks.</span></span>

## <a name="syntax"></a><span data-ttu-id="86ff5-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="86ff5-111">Syntax</span></span>


```C++
HRESULT CommitToDevice();
```



## <a name="parameters"></a><span data-ttu-id="86ff5-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="86ff5-112">Parameters</span></span>

<span data-ttu-id="86ff5-113">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="86ff5-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="86ff5-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="86ff5-114">Return value</span></span>

<span data-ttu-id="86ff5-115">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="86ff5-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="86ff5-116">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="86ff5-116">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="86ff5-117">Notes</span><span class="sxs-lookup"><span data-stu-id="86ff5-117">Remarks</span></span>

<span data-ttu-id="86ff5-118">Lorsqu’un maillage est chargé, ses données sont chargées dans des ressources intermédiaires, ce qui signifie que les données peuvent être modifiées mais pas rendues.</span><span class="sxs-lookup"><span data-stu-id="86ff5-118">When a mesh is loaded, it's data is loaded into staging resources, meaning the data can be altered but not rendered.</span></span> <span data-ttu-id="86ff5-119">Quand CommitToDevice est appelé, les données des ressources de mise en lots sont copiées dans les ressources de l’appareil afin qu’elles puissent être rendues.</span><span class="sxs-lookup"><span data-stu-id="86ff5-119">When CommitToDevice is called, the data from the staging resources are copied into device resources so that they can be rendered.</span></span> <span data-ttu-id="86ff5-120">Bien que les données soient validées sur l’appareil, les ressources de mise en lots restent et peuvent être modifiées.</span><span class="sxs-lookup"><span data-stu-id="86ff5-120">Although the data is committed to the device, the staging resources remain and can be modified.</span></span> <span data-ttu-id="86ff5-121">Si des modifications sont apportées aux ressources intermédiaires, celles-ci doivent être réactivées sur l’appareil afin que ces modifications soient rendues à l’écran.</span><span class="sxs-lookup"><span data-stu-id="86ff5-121">If any modifications are made to the staging resources, the staging resources must be committed to the device again in order for those changes to be rendered on screen.</span></span>

## <a name="requirements"></a><span data-ttu-id="86ff5-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="86ff5-122">Requirements</span></span>



| <span data-ttu-id="86ff5-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="86ff5-123">Requirement</span></span> | <span data-ttu-id="86ff5-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="86ff5-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="86ff5-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="86ff5-125">Header</span></span><br/>  | <dl> <span data-ttu-id="86ff5-126"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="86ff5-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="86ff5-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="86ff5-127">Library</span></span><br/> | <dl> <span data-ttu-id="86ff5-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="86ff5-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86ff5-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="86ff5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86ff5-130">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="86ff5-130">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="86ff5-131">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="86ff5-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




