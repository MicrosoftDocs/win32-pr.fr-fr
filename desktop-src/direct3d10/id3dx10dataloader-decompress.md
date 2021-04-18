---
description: Utilisé pour décompresser des données encodées. En général, cette valeur est utilisée pour charger des ressources à partir de systèmes de fichiers, tels que des fichiers ZIP. Lors du chargement à partir d’une ressource non compressée, l’étape de décompression n’a pas besoin d’effectuer de travail.
ms.assetid: 7f7e3ffd-8dac-403f-813b-d6d21d146fa7
title: ID3DX10DataLoader ::D méthode eComPress (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataLoader.Decompress
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e6f711722852cba4b671cc84416055d279fd7cc6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523189"
---
# <a name="id3dx10dataloaderdecompress-method"></a><span data-ttu-id="d1ada-105">ID3DX10DataLoader ::D méthode eComPress</span><span class="sxs-lookup"><span data-stu-id="d1ada-105">ID3DX10DataLoader::Decompress method</span></span>

<span data-ttu-id="d1ada-106">Utilisé pour décompresser des données encodées.</span><span class="sxs-lookup"><span data-stu-id="d1ada-106">Used to decompress encoded data.</span></span> <span data-ttu-id="d1ada-107">En général, cette valeur est utilisée pour charger des ressources à partir de systèmes de fichiers, tels que des fichiers ZIP.</span><span class="sxs-lookup"><span data-stu-id="d1ada-107">Typically this would be used to load resources from file systems, such as ZIP files.</span></span> <span data-ttu-id="d1ada-108">Lors du chargement à partir d’une ressource non compressée, l’étape de décompression n’a pas besoin d’effectuer de travail.</span><span class="sxs-lookup"><span data-stu-id="d1ada-108">When loading from an uncompressed resource, the decompression stage does not have to do any work.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1ada-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d1ada-109">Syntax</span></span>


```C++
HRESULT Decompress(
  [out] void   **ppData,
  [in]  SIZE_T *pcBytes
);
```



## <a name="parameters"></a><span data-ttu-id="d1ada-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d1ada-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1ada-111">*ppData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d1ada-111">*ppData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d1ada-112">Type : **void \* \***</span><span class="sxs-lookup"><span data-stu-id="d1ada-112">Type: **void\*\***</span></span>

<span data-ttu-id="d1ada-113">Pointeur vers les données brutes à décompresser.</span><span class="sxs-lookup"><span data-stu-id="d1ada-113">Pointer to the raw data to decompress.</span></span>

</dd> <dt>

<span data-ttu-id="d1ada-114">*pcBytes* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d1ada-114">*pcBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1ada-115">Type : **[ **taille \_ T**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d1ada-115">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d1ada-116">Taille des données vers lesquelles pointe ppData.</span><span class="sxs-lookup"><span data-stu-id="d1ada-116">The size of the data pointed to by ppData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1ada-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d1ada-117">Return value</span></span>

<span data-ttu-id="d1ada-118">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d1ada-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d1ada-119">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="d1ada-119">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d1ada-120">Notes</span><span class="sxs-lookup"><span data-stu-id="d1ada-120">Remarks</span></span>

<span data-ttu-id="d1ada-121">L' [**interface ID3DX10DataLoader**](id3dx10dataloader.md) peut être héritée et ses membres redéfinis.</span><span class="sxs-lookup"><span data-stu-id="d1ada-121">[**ID3DX10DataLoader Interface**](id3dx10dataloader.md) can be inherited and its members redefined.</span></span> <span data-ttu-id="d1ada-122">La décompression peut être redéfinie pour prendre en charge vos propres formats de fichier personnalisés.</span><span class="sxs-lookup"><span data-stu-id="d1ada-122">Decompress could be redefined to support your own custom file formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1ada-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d1ada-123">Requirements</span></span>



| <span data-ttu-id="d1ada-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d1ada-124">Requirement</span></span> | <span data-ttu-id="d1ada-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1ada-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d1ada-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="d1ada-126">Header</span></span><br/>  | <dl> <span data-ttu-id="d1ada-127"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1ada-127"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="d1ada-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d1ada-128">Library</span></span><br/> | <dl> <span data-ttu-id="d1ada-129"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d1ada-129"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1ada-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1ada-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1ada-131">ID3DX10DataLoader</span><span class="sxs-lookup"><span data-stu-id="d1ada-131">ID3DX10DataLoader</span></span>](id3dx10dataloader.md)
</dt> <dt>

[<span data-ttu-id="d1ada-132">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="d1ada-132">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
