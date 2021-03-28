---
title: Fonctions du compilateur (référence HLSL)
description: Cette section contient des informations sur les fonctions de compilateur HLSL Direct3D suivantes
ms.assetid: aacc5207-3ec8-4031-b5c9-f7c0fb7b7095
keywords:
- fonctions, compilateur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ee63fa17cc9216fdb92f69fed4d77bc65bb49048
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "104982826"
---
# <a name="compiler-functions-hlsl-reference"></a><span data-ttu-id="08985-104">Fonctions du compilateur (référence HLSL)</span><span class="sxs-lookup"><span data-stu-id="08985-104">Compiler functions (HLSL reference)</span></span>

<span data-ttu-id="08985-105">Cette section contient des informations sur les fonctions de compilateur HLSL Direct3D suivantes :</span><span class="sxs-lookup"><span data-stu-id="08985-105">This section contains information about the following Direct3D HLSL compiler functions:</span></span>

## <a name="in-this-section"></a><span data-ttu-id="08985-106">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="08985-106">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="08985-107">Rubrique</span><span class="sxs-lookup"><span data-stu-id="08985-107">Topic</span></span></th>
<th><span data-ttu-id="08985-108">Description</span><span class="sxs-lookup"><span data-stu-id="08985-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="08985-109"><a href="d3d11reflect.md"><strong>D3D11Reflect</strong></a></span><span class="sxs-lookup"><span data-stu-id="08985-109"><a href="d3d11reflect.md"><strong>D3D11Reflect</strong></a></span></span><br/></td>
<td><span data-ttu-id="08985-110">Obtient un pointeur vers une interface de réflexion.</span><span class="sxs-lookup"><span data-stu-id="08985-110">Gets a pointer to a reflection interface.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="08985-111"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile"><strong>D3DCompile</strong></a></span><span class="sxs-lookup"><span data-stu-id="08985-111"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile"><strong>D3DCompile</strong></a></span></span><br/></td>
<td><span data-ttu-id="08985-112">Compilez le code HLSL ou un fichier d’effet en bytecode pour une cible donnée.</span><span class="sxs-lookup"><span data-stu-id="08985-112">Compile HLSL code or an effect file into bytecode for a given target.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="08985-113"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2"><strong>D3DCompile2</strong></a></span><span class="sxs-lookup"><span data-stu-id="08985-113"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2"><strong>D3DCompile2</strong></a></span></span><br/></td>
<td><span data-ttu-id="08985-114">Compile le code HLSL (High Level Shader Language) de Microsoft en bytecode pour une cible donnée.</span><span class="sxs-lookup"><span data-stu-id="08985-114">Compiles Microsoft High Level Shader Language (HLSL) code into bytecode for a given target.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="08985-115"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile"><strong>D3DCompileFromFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="08985-115"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile"><strong>D3DCompileFromFile</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="08985-116">Vous pouvez utiliser cette API pour développer vos applications du Windows Store, mais vous ne pouvez pas l’utiliser dans les applications que vous envoyez au Windows Store.</span><span class="sxs-lookup"><span data-stu-id="08985-116">You can use this API to develop your Windows Store apps, but you can't use it in apps that you submit to the Windows Store.</span></span> <span data-ttu-id="08985-117">Reportez-vous à la section &quot; compilation des nuanceurs pour UWP &quot; dans les notes pour <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2"><strong>D3DCompile2</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="08985-117">Refer to the section, &quot;Compiling shaders for UWP&quot;, in the remarks for <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2"><strong>D3DCompile2</strong></a>.</span></span>
</blockquote>
<br/> <span data-ttu-id="08985-118">Compile le code HLSL en bytecode pour une cible donnée.</span><span class="sxs-lookup"><span data-stu-id="08985-118">Compiles HLSL code into bytecode for a given target.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="08985-119"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompressshaders"><strong>D3DCompressShaders</strong></a></span><span class="sxs-lookup"><span data-stu-id="08985-119"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompressshaders"><strong>D3DCompressShaders</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="08985-120">Vous pouvez utiliser cette API pour développer vos applications du Windows Store, mais vous ne pouvez pas l’utiliser dans les applications que vous envoyez au Windows Store.</span><span class="sxs-lookup"><span data-stu-id="08985-120">You can use this API to develop your Windows Store apps, but you can't use it in apps that you submit to the Windows Store.</span></span>
</blockquote>
<br/> <span data-ttu-id="08985-121">Compresse un ensemble de nuanceurs dans une forme plus compacte.</span><span class="sxs-lookup"><span data-stu-id="08985-121">Compresses a set of shaders into a more compact form.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="08985-122"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcreateblob"><strong>D3DCreateBlob</strong></a></span><span class="sxs-lookup"><span data-stu-id="08985-122"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcreateblob"><strong>D3DCreateBlob</strong></a></span></span><br/></td>
<td><span data-ttu-id="08985-123">Crée une mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="08985-123">Creates a buffer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="08985-124"><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph"><strong>D3DCreateFunctionLinkingGraph</strong></a></span><span class="sxs-lookup"><span data-stu-id="08985-124"><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph"><strong>D3DCreateFunctionLinkingGraph</strong></a></span></span><br/></td>
<td><span data-ttu-id="08985-125">Crée une interface de graphe de liaison de fonction.</span><span class="sxs-lookup"><span data-stu-id="08985-125">Creates a function-linking-graph interface.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="08985-126">Cette fonction fait partie de la technologie de liaison de nuanceur HLSL que vous pouvez utiliser sur toutes les plateformes Direct3D 11 pour créer des fonctions HLSL précompilées, les empaqueter dans des bibliothèques et les lier à des nuanceurs complets au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="08985-126">This function is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="08985-127"><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker"><strong>D3DCreateLinker</strong></a></span><span class="sxs-lookup"><span data-stu-id="08985-127"><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker"><strong>D3DCreateLinker</strong></a></span></span><br/></td>
<td><span data-ttu-id="08985-128">Crée une interface de l’éditeur de liens.</span><span class="sxs-lookup"><span data-stu-id="08985-128">Creates a linker interface.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="08985-129">Cette fonction fait partie de la technologie de liaison de nuanceur HLSL que vous pouvez utiliser sur toutes les plateformes Direct3D 11 pour créer des fonctions HLSL précompilées, les empaqueter dans des bibliothèques et les lier à des nuanceurs complets au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="08985-129">This function is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="08985-130"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddecompressshaders"><strong>D3DDecompressShaders</strong></a></span><span class="sxs-lookup"><span data-stu-id="08985-130"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddecompressshaders"><strong>D3DDecompressShaders</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="08985-131">Vous pouvez utiliser cette API pour développer vos applications du Windows Store, mais vous ne pouvez pas l’utiliser dans les applications que vous envoyez au Windows Store.</span><span class="sxs-lookup"><span data-stu-id="08985-131">You can use this API to develop your Windows Store apps, but you can't use it in apps that you submit to the Windows Store.</span></span>
</blockquote>
<br/> <span data-ttu-id="08985-132">Décompresse un ou plusieurs nuanceurs d’un jeu compressé.</span><span class="sxs-lookup"><span data-stu-id="08985-132">Decompresses one or more shaders from a compressed set.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="08985-133"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble"><strong>D3DDisassemble</strong></a></span><span class="sxs-lookup"><span data-stu-id="08985-133"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble"><strong>D3DDisassemble</strong></a></span></span><br/></td>
<td><span data-ttu-id="08985-134">Désassemble le code HLSL compilé.</span><span class="sxs-lookup"><span data-stu-id="08985-134">Disassembles compiled HLSL code.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="08985-135"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect"><strong>D3DDisassemble10Effect</strong></a></span><span class="sxs-lookup"><span data-stu-id="08985-135"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect"><strong>D3DDisassemble10Effect</strong></a></span></span><br/></td>
<td><span data-ttu-id="08985-136">Désassemble le code HLSL compilé à partir d’un effet Direct3D10.</span><span class="sxs-lookup"><span data-stu-id="08985-136">Disassembles compiled HLSL code from a Direct3D10 effect.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="08985-137"><a href="/windows/win32/api/d3d11shadertracing/nf-d3d11shadertracing-d3ddisassemble11trace"><strong>D3DDisassemble11Trace</strong></a></span><span class="sxs-lookup"><span data-stu-id="08985-137"><a href="/windows/win32/api/d3d11shadertracing/nf-d3d11shadertracing-d3ddisassemble11trace"><strong>D3DDisassemble11Trace</strong></a></span></span><br/></td>
<td><span data-ttu-id="08985-138">Désassemble une section du code HLSL compilé qui est spécifiée par les étapes de trace du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="08985-138">Disassembles a section of compiled HLSL code that is specified by shader trace steps.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="08985-139"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassembleregion"><strong>D3DDisassembleRegion</strong></a></span><span class="sxs-lookup"><span data-stu-id="08985-139"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassembleregion"><strong>D3DDisassembleRegion</strong></a></span></span><br/></td>
<td><span data-ttu-id="08985-140">Désassemble une région spécifique de code HLSL compilé.</span><span class="sxs-lookup"><span data-stu-id="08985-140">Disassembles a specific region of compiled HLSL code.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="08985-141"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a></span><span class="sxs-lookup"><span data-stu-id="08985-141"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a></span></span><br/></td>
<td><span data-ttu-id="08985-142">Récupère une partie spécifique d’un résultat de compilation.</span><span class="sxs-lookup"><span data-stu-id="08985-142">Retrieves a specific part from a compilation result.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="08985-143"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetdebuginfo"><strong>D3DGetDebugInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="08985-143"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetdebuginfo"><strong>D3DGetDebugInfo</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="08985-144">Vous pouvez utiliser cette API pour développer vos applications du Windows Store, mais vous ne pouvez pas l’utiliser dans les applications que vous envoyez au Windows Store.</span><span class="sxs-lookup"><span data-stu-id="08985-144">You can use this API to develop your Windows Store apps, but you can't use it in apps that you submit to the Windows Store.</span></span>
</blockquote>
<br/> <span data-ttu-id="08985-145">Obtient les informations de débogage du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="08985-145">Gets shader debug information.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="08985-146"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputandoutputsignatureblob"><strong>D3DGetInputAndOutputSignatureBlob</strong></a></span><span class="sxs-lookup"><span data-stu-id="08985-146"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputandoutputsignatureblob"><strong>D3DGetInputAndOutputSignatureBlob</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br /><span data-ttu-id="08985-147">
<a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputandoutputsignatureblob"><strong>D3DGetInputAndOutputSignatureBlob</strong></a> peut être modifié ou non disponible pour les mises en production après Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="08985-147">
<a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputandoutputsignatureblob"><strong>D3DGetInputAndOutputSignatureBlob</strong></a> may be altered or unavailable for releases after Windows 8.1.</span></span> <span data-ttu-id="08985-148">Utilisez plutôt <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a> avec la valeur <a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_INPUT_AND_OUTPUT_SIGNATURE_BLOB</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="08985-148">Instead use <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a> with the <a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_INPUT_AND_OUTPUT_SIGNATURE_BLOB</strong></a> value.</span></span>
</blockquote>
<br/> <span data-ttu-id="08985-149">Obtient les signatures d’entrée et de sortie à partir d’un résultat de compilation.</span><span class="sxs-lookup"><span data-stu-id="08985-149">Gets the input and output signatures from a compilation result.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="08985-150">[<strong>D3DGetInputSignatureBlob</strong>] (/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputsignatureblob)</span><span class="sxs-lookup"><span data-stu-id="08985-150">[<strong>D3DGetInputSignatureBlob</strong>](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputsignatureblob)</span></span><br/></td>
<td><blockquote>
[!Note]<br /><span data-ttu-id="08985-151">
<a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputsignatureblob"><strong>D3DGetInputSignatureBlob</strong></a> peut être modifié ou non disponible pour les mises en production après Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="08985-151">
<a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputsignatureblob"><strong>D3DGetInputSignatureBlob</strong></a> may be altered or unavailable for releases after Windows 8.1.</span></span> <span data-ttu-id="08985-152">Utilisez plutôt <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a> avec la valeur <a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_INPUT_SIGNATURE_BLOB</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="08985-152">Instead use <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a> with the <a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_INPUT_SIGNATURE_BLOB</strong></a> value.</span></span>
</blockquote>
<br/> <span data-ttu-id="08985-153">Obtient la signature d’entrée à partir d’un résultat de compilation.</span><span class="sxs-lookup"><span data-stu-id="08985-153">Gets the input signature from a compilation result.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="08985-154"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetoutputsignatureblob"><strong>D3DGetOutputSignatureBlob</strong></a></span><span class="sxs-lookup"><span data-stu-id="08985-154"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetoutputsignatureblob"><strong>D3DGetOutputSignatureBlob</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br /><span data-ttu-id="08985-155">
<a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetoutputsignatureblob"><strong>D3DGetOutputSignatureBlob</strong></a> peut être modifié ou non disponible pour les mises en production après Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="08985-155">
<a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetoutputsignatureblob"><strong>D3DGetOutputSignatureBlob</strong></a> may be altered or unavailable for releases after Windows 8.1.</span></span> <span data-ttu-id="08985-156">Utilisez plutôt <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a> avec la valeur <a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_OUTPUT_SIGNATURE_BLOB</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="08985-156">Instead use <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a> with the <a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_OUTPUT_SIGNATURE_BLOB</strong></a> value.</span></span>
</blockquote>
<br/> <span data-ttu-id="08985-157">Obtient la signature de sortie à partir d’un résultat de compilation.</span><span class="sxs-lookup"><span data-stu-id="08985-157">Gets the output signature from a compilation result.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="08985-158"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgettraceinstructionoffsets"><strong>D3DGetTraceInstructionOffsets</strong></a></span><span class="sxs-lookup"><span data-stu-id="08985-158"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgettraceinstructionoffsets"><strong>D3DGetTraceInstructionOffsets</strong></a></span></span><br/></td>
<td><span data-ttu-id="08985-159">Récupère les décalages d’octets pour les instructions dans une section du code du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="08985-159">Retrieves the byte offsets for instructions within a section of shader code.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="08985-160"><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dloadmodule"><strong>D3DLoadModule</strong></a></span><span class="sxs-lookup"><span data-stu-id="08985-160"><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dloadmodule"><strong>D3DLoadModule</strong></a></span></span><br/></td>
<td><span data-ttu-id="08985-161">Crée une interface de module Shader à partir des données sources pour le module Shader.</span><span class="sxs-lookup"><span data-stu-id="08985-161">Creates a shader module interface from source data for the shader module.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="08985-162">Cette fonction fait partie de la technologie de liaison de nuanceur HLSL que vous pouvez utiliser sur toutes les plateformes Direct3D 11 pour créer des fonctions HLSL précompilées, les empaqueter dans des bibliothèques et les lier à des nuanceurs complets au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="08985-162">This function is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="08985-163"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess"><strong>D3DPreprocess</strong></a></span><span class="sxs-lookup"><span data-stu-id="08985-163"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess"><strong>D3DPreprocess</strong></a></span></span><br/></td>
<td><span data-ttu-id="08985-164">Prétraite le code HLSL non compilé.</span><span class="sxs-lookup"><span data-stu-id="08985-164">Preprocesses uncompiled HLSL code.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="08985-165"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreadfiletoblob"><strong>D3DReadFileToBlob</strong></a></span><span class="sxs-lookup"><span data-stu-id="08985-165"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreadfiletoblob"><strong>D3DReadFileToBlob</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="08985-166">Vous pouvez utiliser cette API pour développer vos applications du Windows Store, mais vous ne pouvez pas l’utiliser dans les applications que vous envoyez au Windows Store.</span><span class="sxs-lookup"><span data-stu-id="08985-166">You can use this API to develop your Windows Store apps, but you can't use it in apps that you submit to the Windows Store.</span></span>
</blockquote>
<br/> <span data-ttu-id="08985-167">Lit un fichier qui se trouve sur le disque en mémoire.</span><span class="sxs-lookup"><span data-stu-id="08985-167">Reads a file that is on disk into memory.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="08985-168"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect"><strong>D3DReflect</strong></a></span><span class="sxs-lookup"><span data-stu-id="08985-168"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect"><strong>D3DReflect</strong></a></span></span><br/></td>
<td><span data-ttu-id="08985-169">Obtient un pointeur vers une interface de réflexion.</span><span class="sxs-lookup"><span data-stu-id="08985-169">Gets a pointer to a reflection interface.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="08985-170"><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dreflectlibrary"><strong>D3DReflectLibrary</strong></a></span><span class="sxs-lookup"><span data-stu-id="08985-170"><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dreflectlibrary"><strong>D3DReflectLibrary</strong></a></span></span><br/></td>
<td><span data-ttu-id="08985-171">Crée une interface de réflexion de bibliothèque à partir de données sources qui contient une bibliothèque de fonctions HLSL.</span><span class="sxs-lookup"><span data-stu-id="08985-171">Creates a library-reflection interface from source data that contains an HLSL library of functions.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="08985-172">Cette fonction fait partie de la technologie de liaison de nuanceur HLSL que vous pouvez utiliser sur toutes les plateformes Direct3D 11 pour créer des fonctions HLSL précompilées, les empaqueter dans des bibliothèques et les lier à des nuanceurs complets au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="08985-172">This function is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="08985-173"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dsetblobpart"><strong>D3DSetBlobPart</strong></a></span><span class="sxs-lookup"><span data-stu-id="08985-173"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dsetblobpart"><strong>D3DSetBlobPart</strong></a></span></span><br/></td>
<td><span data-ttu-id="08985-174">Définit des informations dans un résultat de compilation.</span><span class="sxs-lookup"><span data-stu-id="08985-174">Sets information in a compilation result.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="08985-175"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dstripshader"><strong>D3DStripShader</strong></a></span><span class="sxs-lookup"><span data-stu-id="08985-175"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dstripshader"><strong>D3DStripShader</strong></a></span></span><br/></td>
<td><span data-ttu-id="08985-176">Supprime les objets BLOB indésirables d’un résultat de compilation.</span><span class="sxs-lookup"><span data-stu-id="08985-176">Removes unwanted blobs from a compilation result.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="08985-177"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dwriteblobtofile"><strong>D3DWriteBlobToFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="08985-177"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dwriteblobtofile"><strong>D3DWriteBlobToFile</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="08985-178">Vous pouvez utiliser cette API pour développer vos applications du Windows Store, mais vous ne pouvez pas l’utiliser dans les applications que vous envoyez au Windows Store.</span><span class="sxs-lookup"><span data-stu-id="08985-178">You can use this API to develop your Windows Store apps, but you can't use it in apps that you submit to the Windows Store.</span></span>
</blockquote>
<br/> <span data-ttu-id="08985-179">Écrit un objet blob de mémoire dans un fichier sur le disque.</span><span class="sxs-lookup"><span data-stu-id="08985-179">Writes a memory blob to a file on disk.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="08985-180">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="08985-180">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08985-181">Référence D3DCompiler</span><span class="sxs-lookup"><span data-stu-id="08985-181">D3DCompiler Reference</span></span>](dx-graphics-d3dcompiler-reference.md)
</dt> </dl>

