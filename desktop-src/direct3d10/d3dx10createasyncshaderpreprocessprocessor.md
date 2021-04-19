---
description: Créer un processeur de données pour un nuanceur de manière asynchrone.
ms.assetid: f5521e55-5f20-422d-979e-98b70efd3b13
title: D3DX10CreateAsyncShaderPreprocessProcessor, fonction (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncShaderPreprocessProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 14afdb899d99b7c0278d3042fbc9a108f446c692
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539470"
---
# <a name="d3dx10createasyncshaderpreprocessprocessor-function"></a><span data-ttu-id="831b4-103">D3DX10CreateAsyncShaderPreprocessProcessor fonction)</span><span class="sxs-lookup"><span data-stu-id="831b4-103">D3DX10CreateAsyncShaderPreprocessProcessor function</span></span>

<span data-ttu-id="831b4-104">Créer un processeur de données pour un nuanceur de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="831b4-104">Create a data processor for a shader asynchronously.</span></span>

## <a name="syntax"></a><span data-ttu-id="831b4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="831b4-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncShaderPreprocessProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _Out_       ID3D10Blob           **ppShaderText,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX10DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="831b4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="831b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="831b4-107">*pFileName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="831b4-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="831b4-108">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="831b4-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="831b4-109">Chaîne qui contient le nom de fichier du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="831b4-109">A string that contains the shader filename.</span></span>

</dd> <dt>

<span data-ttu-id="831b4-110">*pDefines* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="831b4-110">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="831b4-111">Type : **\* macro de [**\_ nuanceur \_ D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) const**</span><span class="sxs-lookup"><span data-stu-id="831b4-111">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="831b4-112">Tableau de macros de nuanceur se terminant par un caractère NULL (consultez la [**\_ \_ macro de nuanceur D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); définissez cette valeur sur **null** pour ne spécifier aucune macro.</span><span class="sxs-lookup"><span data-stu-id="831b4-112">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="831b4-113">*pInclude* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="831b4-113">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="831b4-114">Type : **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="831b4-114">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="831b4-115">Pointeur vers une interface include (voir [**interface ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); Affectez-lui la valeur **null** pour spécifier qu’il n’y a aucun fichier include.</span><span class="sxs-lookup"><span data-stu-id="831b4-115">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="831b4-116">*ppShaderText* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="831b4-116">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="831b4-117">Type : **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="831b4-117">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="831b4-118">Adresse d’un pointeur vers une mémoire tampon qui contient le texte ASCII du nuanceur (voir [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span><span class="sxs-lookup"><span data-stu-id="831b4-118">Address of a pointer to a buffer that contains the ASCII text of the shader (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span></span>

</dd> <dt>

<span data-ttu-id="831b4-119">*ppErrorBuffer* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="831b4-119">*ppErrorBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="831b4-120">Type : **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="831b4-120">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="831b4-121">Adresse d’un pointeur vers une mémoire tampon qui contient des erreurs de compilation (voir [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span><span class="sxs-lookup"><span data-stu-id="831b4-121">Address of a pointer to a buffer that contains compile errors (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span></span>

</dd> <dt>

<span data-ttu-id="831b4-122">*ppDataProcessor* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="831b4-122">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="831b4-123">Type : **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="831b4-123">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="831b4-124">Adresse d’un pointeur vers une mémoire tampon qui contient le processeur de données créé (voir [**interface ID3DX10DataProcessor**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="831b4-124">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="831b4-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="831b4-125">Return value</span></span>

<span data-ttu-id="831b4-126">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="831b4-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="831b4-127">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="831b4-127">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="831b4-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="831b4-128">Requirements</span></span>



| <span data-ttu-id="831b4-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="831b4-129">Requirement</span></span> | <span data-ttu-id="831b4-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="831b4-130">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="831b4-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="831b4-131">Header</span></span><br/> | <dl> <span data-ttu-id="831b4-132"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="831b4-132"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="831b4-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="831b4-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="831b4-134">Fonctions usage général</span><span class="sxs-lookup"><span data-stu-id="831b4-134">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
