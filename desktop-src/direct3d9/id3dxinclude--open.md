---
description: Méthode implémentée par l’utilisateur pour ouvrir et lire le contenu d’un \# fichier include de nuanceur.
ms.assetid: ad0105f7-042d-4e96-ad4a-1ece08e519af
title: 'ID3DXInclude :: Open, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXInclude.Open
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 313b3f4845f9a46f758a40b6b315cc5b5eeecb29
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106527953"
---
# <a name="id3dxincludeopen-method"></a><span data-ttu-id="c558b-103">ID3DXInclude :: Open, méthode</span><span class="sxs-lookup"><span data-stu-id="c558b-103">ID3DXInclude::Open method</span></span>

<span data-ttu-id="c558b-104">Méthode implémentée par l’utilisateur pour ouvrir et lire le contenu d’un \# fichier include de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="c558b-104">A user-implemented method for opening and reading the contents of a shader \#include file.</span></span>

## <a name="syntax"></a><span data-ttu-id="c558b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c558b-105">Syntax</span></span>


```C++
HRESULT Open(
  [in]  D3DXINCLUDE_TYPE IncludeType,
  [in]  LPCSTR           pFileName,
  [in]  LPCVOID          pParentData,
  [out] LPCVOID          *ppData,
  [out] UINT             *pBytes
);
```



## <a name="parameters"></a><span data-ttu-id="c558b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c558b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c558b-107">*IncludeType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c558b-107">*IncludeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c558b-108">Type : **[ **D3DXINCLUDE \_**](./d3dxinclude-type.md)**</span><span class="sxs-lookup"><span data-stu-id="c558b-108">Type: **[**D3DXINCLUDE\_TYPE**](./d3dxinclude-type.md)**</span></span>

<span data-ttu-id="c558b-109">Emplacement du \# fichier include.</span><span class="sxs-lookup"><span data-stu-id="c558b-109">The location of the \#include file.</span></span> <span data-ttu-id="c558b-110">Consultez [**\_ type D3DXINCLUDE**](./d3dxinclude-type.md).</span><span class="sxs-lookup"><span data-stu-id="c558b-110">See [**D3DXINCLUDE\_TYPE**](./d3dxinclude-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="c558b-111">*pFileName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c558b-111">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c558b-112">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c558b-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c558b-113">Nom du \# fichier include.</span><span class="sxs-lookup"><span data-stu-id="c558b-113">Name of the \#include file.</span></span>

</dd> <dt>

<span data-ttu-id="c558b-114">*pParentData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c558b-114">*pParentData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c558b-115">Type : **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c558b-115">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c558b-116">Pointeur vers le conteneur qui inclut le \# fichier include.</span><span class="sxs-lookup"><span data-stu-id="c558b-116">Pointer to the container that includes the \#include file.</span></span> <span data-ttu-id="c558b-117">Le compilateur peut passer NULL dans *pParentData*.</span><span class="sxs-lookup"><span data-stu-id="c558b-117">The compiler might pass NULL in *pParentData*.</span></span> <span data-ttu-id="c558b-118">Pour plus d’informations, consultez la section « recherche de fichiers include » dans [compiler un effet (Direct3D 11)](../direct3d11/d3d11-graphics-programming-guide-effects-compile.md).</span><span class="sxs-lookup"><span data-stu-id="c558b-118">For more information, see the "Searching for Include Files" section in [Compile an Effect (Direct3D 11)](../direct3d11/d3d11-graphics-programming-guide-effects-compile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c558b-119">*ppData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c558b-119">*ppData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c558b-120">Type : **[ **LPCVOID**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c558b-120">Type: **[**LPCVOID**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c558b-121">Pointeur vers la mémoire tampon retournée qui contient les directives include.</span><span class="sxs-lookup"><span data-stu-id="c558b-121">Pointer to the returned buffer that contains the include directives.</span></span> <span data-ttu-id="c558b-122">Ce pointeur reste valide jusqu’à ce que [**ID3DXInclude :: Close**](id3dxinclude--close.md) soit appelé.</span><span class="sxs-lookup"><span data-stu-id="c558b-122">This pointer remains valid until [**ID3DXInclude::Close**](id3dxinclude--close.md) is called.</span></span>

</dd> <dt>

<span data-ttu-id="c558b-123">*pBytes* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c558b-123">*pBytes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c558b-124">Type : **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c558b-124">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c558b-125">Nombre d’octets retournés dans ppData.</span><span class="sxs-lookup"><span data-stu-id="c558b-125">Number of bytes returned in ppData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c558b-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c558b-126">Return value</span></span>

<span data-ttu-id="c558b-127">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c558b-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c558b-128">La méthode implémentée par l’utilisateur doit retourner S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c558b-128">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="c558b-129">Si le rappel échoue lors de la lecture du \# fichier include, l’API qui a provoqué l’appel du rappel échoue.</span><span class="sxs-lookup"><span data-stu-id="c558b-129">If the callback fails when reading the \#include file, the API that caused the callback to be called will fail.</span></span> <span data-ttu-id="c558b-130">Il s’agit de l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="c558b-130">This is one of the following:</span></span>

-   <span data-ttu-id="c558b-131">Le nuanceur HLSL échouera à l’une des \* \* \* fonctions D3DXCompileShader.</span><span class="sxs-lookup"><span data-stu-id="c558b-131">The HLSL shader will fail one of the D3DXCompileShader\*\*\* functions.</span></span>
-   <span data-ttu-id="c558b-132">Le nuanceur d’assembly échouera à l’une des \* \* \* fonctions D3DXAssembleShader.</span><span class="sxs-lookup"><span data-stu-id="c558b-132">The assembly shader will fail one of the D3DXAssembleShader\*\*\* functions.</span></span>
-   <span data-ttu-id="c558b-133">L’effet échouera à l’une des \* \* \* fonctions D3DXCreateEffect ou D3DXCreateEffectCompiler \* \* \* .</span><span class="sxs-lookup"><span data-stu-id="c558b-133">The effect will fail one of the D3DXCreateEffect\*\*\* or D3DXCreateEffectCompiler\*\*\* functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="c558b-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c558b-134">Requirements</span></span>



| <span data-ttu-id="c558b-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c558b-135">Requirement</span></span> | <span data-ttu-id="c558b-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="c558b-136">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c558b-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="c558b-137">Header</span></span><br/>  | <dl> <span data-ttu-id="c558b-138"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="c558b-138"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="c558b-139">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c558b-139">Library</span></span><br/> | <dl> <span data-ttu-id="c558b-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c558b-140"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c558b-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c558b-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c558b-142">ID3DXInclude</span><span class="sxs-lookup"><span data-stu-id="c558b-142">ID3DXInclude</span></span>](id3dxinclude.md)
</dt> <dt>

[<span data-ttu-id="c558b-143">**ID3DXInclude :: Close**</span><span class="sxs-lookup"><span data-stu-id="c558b-143">**ID3DXInclude::Close**</span></span>](id3dxinclude--close.md)
</dt> </dl>

 

 
