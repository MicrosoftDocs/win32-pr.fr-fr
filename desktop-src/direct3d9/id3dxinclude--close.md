---
description: Méthode implémentée par l’utilisateur pour la fermeture d’un \# fichier include de nuanceur.
ms.assetid: de54ce56-3884-443a-9879-4e7290bcfb8d
title: 'ID3DXInclude :: Close, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXInclude.Close
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b60d01d59a4e54fa0d50c16a3fc845ea4e316792
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106525300"
---
# <a name="id3dxincludeclose-method"></a><span data-ttu-id="e7d34-103">ID3DXInclude :: Close, méthode</span><span class="sxs-lookup"><span data-stu-id="e7d34-103">ID3DXInclude::Close method</span></span>

<span data-ttu-id="e7d34-104">Méthode implémentée par l’utilisateur pour la fermeture d’un \# fichier include de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="e7d34-104">A user-implemented method for closing a shader \#include file.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7d34-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e7d34-105">Syntax</span></span>


```C++
HRESULT Close(
  [in] LPCVOID pData
);
```



## <a name="parameters"></a><span data-ttu-id="e7d34-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e7d34-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7d34-107">*pData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e7d34-107">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7d34-108">Type : **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e7d34-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e7d34-109">Pointeur vers la mémoire tampon retournée qui contient les directives include.</span><span class="sxs-lookup"><span data-stu-id="e7d34-109">Pointer to the returned buffer that contains the include directives.</span></span> <span data-ttu-id="e7d34-110">Il s’agit du pointeur qui a été retourné par l’appel [**ID3DXInclude :: Open**](id3dxinclude--open.md) correspondant.</span><span class="sxs-lookup"><span data-stu-id="e7d34-110">This is the pointer that was returned by the corresponding [**ID3DXInclude::Open**](id3dxinclude--open.md) call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7d34-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e7d34-111">Return value</span></span>

<span data-ttu-id="e7d34-112">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e7d34-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e7d34-113">La méthode implémentée par l’utilisateur doit retourner S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e7d34-113">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="e7d34-114">Si le rappel échoue lors de la lecture du \# fichier include, l’API qui a provoqué l’appel du rappel échoue.</span><span class="sxs-lookup"><span data-stu-id="e7d34-114">If the callback fails when reading the \#include file, the API that caused the callback to be called will fail.</span></span> <span data-ttu-id="e7d34-115">Il s’agit de l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="e7d34-115">This is one of the following:</span></span>

-   <span data-ttu-id="e7d34-116">Le nuanceur HLSL échouera à l’une des \* \* \* fonctions D3DXCompileShader.</span><span class="sxs-lookup"><span data-stu-id="e7d34-116">The HLSL shader will fail one of the D3DXCompileShader\*\*\* functions.</span></span>
-   <span data-ttu-id="e7d34-117">Le nuanceur d’assembly échouera à l’une des \* \* \* fonctions D3DXAssembleShader.</span><span class="sxs-lookup"><span data-stu-id="e7d34-117">The assembly shader will fail one of the D3DXAssembleShader\*\*\* functions.</span></span>
-   <span data-ttu-id="e7d34-118">L’effet échouera à l’une des \* \* \* fonctions D3DXCreateEffect ou D3DXCreateEffectCompiler \* \* \* .</span><span class="sxs-lookup"><span data-stu-id="e7d34-118">The effect will fail one of the D3DXCreateEffect\*\*\* or D3DXCreateEffectCompiler\*\*\* functions.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7d34-119">Notes</span><span class="sxs-lookup"><span data-stu-id="e7d34-119">Remarks</span></span>

<span data-ttu-id="e7d34-120">Si [**ID3DXInclude :: Open**](id3dxinclude--open.md) a réussi, l’appel de **ID3DXInclude :: Close** est garanti avant que l’API utilisant cette interface retourne.</span><span class="sxs-lookup"><span data-stu-id="e7d34-120">If [**ID3DXInclude::Open**](id3dxinclude--open.md) was successful, **ID3DXInclude::Close** is guaranteed to be called before the API using this interface returns.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7d34-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e7d34-121">Requirements</span></span>



| <span data-ttu-id="e7d34-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e7d34-122">Requirement</span></span> | <span data-ttu-id="e7d34-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="e7d34-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7d34-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="e7d34-124">Header</span></span><br/>  | <dl> <span data-ttu-id="e7d34-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7d34-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="e7d34-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e7d34-126">Library</span></span><br/> | <dl> <span data-ttu-id="e7d34-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e7d34-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e7d34-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7d34-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7d34-129">ID3DXInclude</span><span class="sxs-lookup"><span data-stu-id="e7d34-129">ID3DXInclude</span></span>](id3dxinclude.md)
</dt> <dt>

[<span data-ttu-id="e7d34-130">**ID3DXInclude :: Open**</span><span class="sxs-lookup"><span data-stu-id="e7d34-130">**ID3DXInclude::Open**</span></span>](id3dxinclude--open.md)
</dt> </dl>

 

 
