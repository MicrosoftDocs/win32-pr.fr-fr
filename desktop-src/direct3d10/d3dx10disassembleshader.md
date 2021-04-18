---
description: Notez qu’au lieu d’utiliser cette fonction héritée, nous vous recommandons d’utiliser l’API D3DDisassemble. Cette fonction, qui Désassemble un nuanceur compilé en une chaîne de texte qui contient des instructions d’assembly et des affectations de registres, n’existe plus.
ms.assetid: f94264f8-121a-4bb7-bf1f-cc5d2cac6cd2
title: D3DX10DisassembleShader, fonction (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10DisassembleShader
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 13716fd5d25e2e8602379ea3864c516fa5388475
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106520302"
---
# <a name="d3dx10disassembleshader-function"></a><span data-ttu-id="02dcb-104">D3DX10DisassembleShader fonction)</span><span class="sxs-lookup"><span data-stu-id="02dcb-104">D3DX10DisassembleShader function</span></span>

> [!Note]  
> <span data-ttu-id="02dcb-105">Au lieu d’utiliser cette fonction héritée, nous vous recommandons d’utiliser l’API [**D3DDisassemble**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble) .</span><span class="sxs-lookup"><span data-stu-id="02dcb-105">Instead of using this legacy function, we recommend that you use the [**D3DDisassemble**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble) API.</span></span>

 

<span data-ttu-id="02dcb-106">Cette fonction, qui Désassemble un nuanceur compilé en une chaîne de texte qui contient des instructions d’assembly et des affectations de registres, n’existe plus.</span><span class="sxs-lookup"><span data-stu-id="02dcb-106">This function -- which disassembles a compiled shader into a text string that contains assembly instructions and register assignments -- no longer exists.</span></span> <span data-ttu-id="02dcb-107">Utilisez plutôt [**D3DDisassemble10Effect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect).</span><span class="sxs-lookup"><span data-stu-id="02dcb-107">Instead, use [**D3DDisassemble10Effect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect).</span></span>

## <a name="syntax"></a><span data-ttu-id="02dcb-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="02dcb-108">Syntax</span></span>


```C++
HRESULT D3DX10DisassembleShader(
  _In_  const void       *pShader,
  _In_        SIZE_T     BytecodeLength,
  _In_        BOOL       EnableColorCode,
  _In_        LPCSTR     pComments,
  _Out_       ID3D10Blob **ppDisassembly
);
```



## <a name="parameters"></a><span data-ttu-id="02dcb-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="02dcb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02dcb-110">*pShader* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="02dcb-110">*pShader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02dcb-111">Type : **const void \***</span><span class="sxs-lookup"><span data-stu-id="02dcb-111">Type: **const void\***</span></span>

<span data-ttu-id="02dcb-112">Pointeur vers le [**nuanceur compilé**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout).</span><span class="sxs-lookup"><span data-stu-id="02dcb-112">A pointer to the [**compiled shader**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout).</span></span>

</dd> <dt>

<span data-ttu-id="02dcb-113">*BytecodeLength* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="02dcb-113">*BytecodeLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02dcb-114">Type : **[ **taille \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="02dcb-114">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="02dcb-115">Taille de pShader.</span><span class="sxs-lookup"><span data-stu-id="02dcb-115">The size of pShader.</span></span>

</dd> <dt>

<span data-ttu-id="02dcb-116">*EnableColorCode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="02dcb-116">*EnableColorCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02dcb-117">Type : **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="02dcb-117">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="02dcb-118">Incluez des balises HTML dans la sortie pour coder en couleur le résultat.</span><span class="sxs-lookup"><span data-stu-id="02dcb-118">Include HTML tags in the output to color code the result.</span></span>

</dd> <dt>

<span data-ttu-id="02dcb-119">*pComments* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="02dcb-119">*pComments* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02dcb-120">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="02dcb-120">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="02dcb-121">Chaîne de commentaire en haut du nuanceur qui identifie les constantes et les variables de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="02dcb-121">The comment string at the top of the shader that identifies the shader constants and variables.</span></span>

</dd> <dt>

<span data-ttu-id="02dcb-122">*ppDisassembly* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="02dcb-122">*ppDisassembly* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="02dcb-123">Type : **[ **ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="02dcb-123">Type: **[**ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="02dcb-124">Adresse d’une mémoire tampon (voir [**interface ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)) qui contient le nuanceur désassemblé.</span><span class="sxs-lookup"><span data-stu-id="02dcb-124">Address of a buffer (see [**ID3D10Blob Interface**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)) which contains the disassembled shader.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02dcb-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="02dcb-125">Return value</span></span>

<span data-ttu-id="02dcb-126">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="02dcb-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="02dcb-127">Retourne l’un des [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="02dcb-127">Returns one of the following [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="02dcb-128">Notes</span><span class="sxs-lookup"><span data-stu-id="02dcb-128">Remarks</span></span>

<span data-ttu-id="02dcb-129">Ce texte retourné comprend un en-tête avec la version du compilateur HLSL utilisée pour générer cet objet, des commentaires décrivant la disposition mémoire des mémoires tampons constantes utilisées par le nuanceur, les signatures d’entrée et de sortie et les points de liaison de ressources.</span><span class="sxs-lookup"><span data-stu-id="02dcb-129">This returned text includes a header with the version of the HLSL compiler used to generate this object, comments describing the memory layout of the constant buffers used by the shader, input and output signatures, and resource binding points.</span></span>

<span data-ttu-id="02dcb-130">Voici un exemple de désassemblage d’un nuanceur compilé.</span><span class="sxs-lookup"><span data-stu-id="02dcb-130">Here is an example of disassembling a compiled shader.</span></span> <span data-ttu-id="02dcb-131">L’exemple suppose que vous démarrez avec un nuanceur compilé (représenté sous la forme *pVSBuf* , que vous pouvez voir dans l' [exemple HLSLWithoutFX10](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)).</span><span class="sxs-lookup"><span data-stu-id="02dcb-131">The example assumes you start with a compiled shader (shown as *pVSBuf* which you can see in [HLSLWithoutFX10 Sample](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)).</span></span>


```
LPCSTR commentString = NULL;
ID3D10Blob* pIDisassembly = NULL;
char* pDisassembly = NULL;
if( pVSBuf )
{
    D3D10DisassembleShader( (UINT*) pVSBuf->GetBufferPointer(), 
        pVSBuf->GetBufferSize(), TRUE, commentString, &pIDisassembly );
    if( pIDisassembly )
    {
        FILE* pFile = fopen( "shader.htm", "w" );
        if( pFile)
        {
            fputs( (char*)pIDisassembly->GetBufferPointer(), pFile );
            fclose( pFile );
        }
    }
}
```



## <a name="requirements"></a><span data-ttu-id="02dcb-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="02dcb-132">Requirements</span></span>



| <span data-ttu-id="02dcb-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="02dcb-133">Requirement</span></span> | <span data-ttu-id="02dcb-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="02dcb-134">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="02dcb-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="02dcb-135">Header</span></span><br/> | <dl> <span data-ttu-id="02dcb-136"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="02dcb-136"><dt>D3DX10Core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02dcb-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="02dcb-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02dcb-138">Fonctions usage général</span><span class="sxs-lookup"><span data-stu-id="02dcb-138">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
