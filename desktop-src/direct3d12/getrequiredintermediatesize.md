---
title: GetRequiredIntermediateSize, fonction (D3dx12. h)
description: Retourne la taille requise d’une mémoire tampon à utiliser pour le téléchargement de données.
ms.assetid: 424B52E9-DE52-40D2-B8B0-C27FD3D3C298
keywords:
- GetRequiredIntermediateSize fonction)
topic_type:
- apiref
api_name:
- GetRequiredIntermediateSize
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15293ce1588704d55f41c364c35db57cbf4c869d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106537267"
---
# <a name="getrequiredintermediatesize-function"></a><span data-ttu-id="c6486-104">GetRequiredIntermediateSize fonction)</span><span class="sxs-lookup"><span data-stu-id="c6486-104">GetRequiredIntermediateSize function</span></span>

<span data-ttu-id="c6486-105">Retourne la taille requise d’une mémoire tampon à utiliser pour le téléchargement de données.</span><span class="sxs-lookup"><span data-stu-id="c6486-105">Returns the required size of a buffer to be used for data upload.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6486-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c6486-106">Syntax</span></span>


```C++
UINT64 inline GetRequiredIntermediateSize(
  _In_ ID3D12Resource *pDestinationResource,
  _In_ UINT           FirstSubresource,
  _In_ UINT           NumSubresources
);
```



## <a name="parameters"></a><span data-ttu-id="c6486-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c6486-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6486-108">*pDestinationResource* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c6486-108">*pDestinationResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6486-109">Type : **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span><span class="sxs-lookup"><span data-stu-id="c6486-109">Type: **[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span></span>

<span data-ttu-id="c6486-110">Pointeur vers l’interface [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) qui représente la ressource de destination.</span><span class="sxs-lookup"><span data-stu-id="c6486-110">A pointer to the [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) interface that represents the destination resource.</span></span>

</dd> <dt>

<span data-ttu-id="c6486-111">*FirstSubresource* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c6486-111">*FirstSubresource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6486-112">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c6486-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c6486-113">Index de la première sous-ressource dans la ressource.</span><span class="sxs-lookup"><span data-stu-id="c6486-113">The index of the first subresource in the resource.</span></span> <span data-ttu-id="c6486-114">La plage de valeurs valides est comprise entre 0 et des sous- \_ ressources D3D12 req \_ .</span><span class="sxs-lookup"><span data-stu-id="c6486-114">The range of valid values is 0 to D3D12\_REQ\_SUBRESOURCES.</span></span>

</dd> <dt>

<span data-ttu-id="c6486-115">*NumSubresources* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c6486-115">*NumSubresources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6486-116">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c6486-116">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c6486-117">Nombre de sous-ressources dans la ressource.</span><span class="sxs-lookup"><span data-stu-id="c6486-117">The number of subresources in the resource.</span></span> <span data-ttu-id="c6486-118">La plage de valeurs valides est comprise entre 0 et (D3D12 \_ req \_ Resources- *FirstSubresource*).</span><span class="sxs-lookup"><span data-stu-id="c6486-118">The range of valid values is 0 to (D3D12\_REQ\_SUBRESOURCES - *FirstSubresource*).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6486-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c6486-119">Return value</span></span>

<span data-ttu-id="c6486-120">Type : **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c6486-120">Type: **[**UINT64**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c6486-121">Taille de la mémoire tampon, en octets.</span><span class="sxs-lookup"><span data-stu-id="c6486-121">The size of the buffer, in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6486-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c6486-122">Requirements</span></span>



| <span data-ttu-id="c6486-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c6486-123">Requirement</span></span> | <span data-ttu-id="c6486-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="c6486-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c6486-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="c6486-125">Header</span></span><br/>  | <dl> <span data-ttu-id="c6486-126"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6486-126"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="c6486-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c6486-127">Library</span></span><br/> | <dl> <span data-ttu-id="c6486-128"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c6486-128"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="c6486-129">DLL</span><span class="sxs-lookup"><span data-stu-id="c6486-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="c6486-130"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6486-130"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6486-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c6486-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6486-132">Fonctions d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="c6486-132">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> </dl>

 

