---
title: Méthode de décompression ID3DX11DataLoader (D3DX11core. h)
description: 'Remarque : la bibliothèque de l’utilitaire D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store. Décompresse les données encodées.'
ms.assetid: 68579c86-9f77-444b-86b3-746cff745be8
keywords:
- Méthode de décompression Direct3D 11
- Méthode de décompression Direct3D 11, interface ID3DX11DataLoader
- ID3DX11DataLoader interface, méthode de décompression Direct3D 11
topic_type:
- apiref
api_name:
- ID3DX11DataLoader.Decompress
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b515eb38fb70fc31f0bbd0d02e20dcfb9f66ea5b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103954008"
---
# <a name="id3dx11dataloaderdecompress-method"></a><span data-ttu-id="7706a-107">ID3DX11DataLoader ::D méthode eComPress</span><span class="sxs-lookup"><span data-stu-id="7706a-107">ID3DX11DataLoader::Decompress method</span></span>

> [!Note]  
> <span data-ttu-id="7706a-108">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="7706a-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="7706a-109">Décompresse les données encodées.</span><span class="sxs-lookup"><span data-stu-id="7706a-109">Decompresses encoded data.</span></span>

## <a name="syntax"></a><span data-ttu-id="7706a-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7706a-110">Syntax</span></span>


```C++
HRESULT Decompress(
  [out] void   **ppData,
  [in]  SIZE_T *pcBytes
);
```



## <a name="parameters"></a><span data-ttu-id="7706a-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7706a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7706a-112">*ppData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7706a-112">*ppData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7706a-113">Type : **void \* \***</span><span class="sxs-lookup"><span data-stu-id="7706a-113">Type: **void\*\***</span></span>

<span data-ttu-id="7706a-114">Pointeur vers les données brutes à décompresser.</span><span class="sxs-lookup"><span data-stu-id="7706a-114">Pointer to the raw data to decompress.</span></span>

</dd> <dt>

<span data-ttu-id="7706a-115">*pcBytes* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7706a-115">*pcBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7706a-116">Type : **[ **taille \_ T**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="7706a-116">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="7706a-117">Taille des données vers lesquelles pointe ppData.</span><span class="sxs-lookup"><span data-stu-id="7706a-117">The size of the data pointed to by ppData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7706a-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7706a-118">Return value</span></span>

<span data-ttu-id="7706a-119">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7706a-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7706a-120">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="7706a-120">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7706a-121">Notes</span><span class="sxs-lookup"><span data-stu-id="7706a-121">Remarks</span></span>

<span data-ttu-id="7706a-122">Utilisez cette méthode pour charger des ressources à partir de systèmes de fichiers, tels que des fichiers ZIP.</span><span class="sxs-lookup"><span data-stu-id="7706a-122">Use this method to load resources from file systems, such as ZIP files.</span></span> <span data-ttu-id="7706a-123">Lors du chargement à partir d’une ressource non compressée, l’étape de décompression n’a pas besoin d’effectuer de travail.</span><span class="sxs-lookup"><span data-stu-id="7706a-123">When loading from an uncompressed resource, the decompression stage does not have to do any work.</span></span>

<span data-ttu-id="7706a-124">L' [**interface ID3DX11DataLoader**](id3dx11dataloader.md) peut être héritée et ses membres redéfinis pour prendre en charge des formats de fichier personnalisés.</span><span class="sxs-lookup"><span data-stu-id="7706a-124">[**ID3DX11DataLoader Interface**](id3dx11dataloader.md) can be inherited and its members redefined to support custom file formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="7706a-125">Spécifications</span><span class="sxs-lookup"><span data-stu-id="7706a-125">Requirements</span></span>



| <span data-ttu-id="7706a-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7706a-126">Requirement</span></span> | <span data-ttu-id="7706a-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="7706a-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7706a-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="7706a-128">Header</span></span><br/>  | <dl> <span data-ttu-id="7706a-129"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="7706a-129"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="7706a-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7706a-130">Library</span></span><br/> | <dl> <span data-ttu-id="7706a-131"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7706a-131"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7706a-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7706a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7706a-133">ID3DX11DataLoader</span><span class="sxs-lookup"><span data-stu-id="7706a-133">ID3DX11DataLoader</span></span>](id3dx11dataloader.md)
</dt> <dt>

[<span data-ttu-id="7706a-134">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="7706a-134">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

