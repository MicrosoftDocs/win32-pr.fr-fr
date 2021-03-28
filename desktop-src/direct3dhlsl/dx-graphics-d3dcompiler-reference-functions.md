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
# <a name="compiler-functions-hlsl-reference"></a>Fonctions du compilateur (référence HLSL)

Cette section contient des informations sur les fonctions de compilateur HLSL Direct3D suivantes :

## <a name="in-this-section"></a>Contenu de cette section



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Rubrique</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="d3d11reflect.md"><strong>D3D11Reflect</strong></a><br/></td>
<td>Obtient un pointeur vers une interface de réflexion.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile"><strong>D3DCompile</strong></a><br/></td>
<td>Compilez le code HLSL ou un fichier d’effet en bytecode pour une cible donnée.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2"><strong>D3DCompile2</strong></a><br/></td>
<td>Compile le code HLSL (High Level Shader Language) de Microsoft en bytecode pour une cible donnée.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile"><strong>D3DCompileFromFile</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Vous pouvez utiliser cette API pour développer vos applications du Windows Store, mais vous ne pouvez pas l’utiliser dans les applications que vous envoyez au Windows Store. Reportez-vous à la section &quot; compilation des nuanceurs pour UWP &quot; dans les notes pour <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2"><strong>D3DCompile2</strong></a>.
</blockquote>
<br/> Compile le code HLSL en bytecode pour une cible donnée.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompressshaders"><strong>D3DCompressShaders</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Vous pouvez utiliser cette API pour développer vos applications du Windows Store, mais vous ne pouvez pas l’utiliser dans les applications que vous envoyez au Windows Store.
</blockquote>
<br/> Compresse un ensemble de nuanceurs dans une forme plus compacte. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcreateblob"><strong>D3DCreateBlob</strong></a><br/></td>
<td>Crée une mémoire tampon.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph"><strong>D3DCreateFunctionLinkingGraph</strong></a><br/></td>
<td>Crée une interface de graphe de liaison de fonction. <br/>
<blockquote>
[!Note]<br />
Cette fonction fait partie de la technologie de liaison de nuanceur HLSL que vous pouvez utiliser sur toutes les plateformes Direct3D 11 pour créer des fonctions HLSL précompilées, les empaqueter dans des bibliothèques et les lier à des nuanceurs complets au moment de l’exécution.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker"><strong>D3DCreateLinker</strong></a><br/></td>
<td>Crée une interface de l’éditeur de liens. <br/>
<blockquote>
[!Note]<br />
Cette fonction fait partie de la technologie de liaison de nuanceur HLSL que vous pouvez utiliser sur toutes les plateformes Direct3D 11 pour créer des fonctions HLSL précompilées, les empaqueter dans des bibliothèques et les lier à des nuanceurs complets au moment de l’exécution.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddecompressshaders"><strong>D3DDecompressShaders</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Vous pouvez utiliser cette API pour développer vos applications du Windows Store, mais vous ne pouvez pas l’utiliser dans les applications que vous envoyez au Windows Store.
</blockquote>
<br/> Décompresse un ou plusieurs nuanceurs d’un jeu compressé. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble"><strong>D3DDisassemble</strong></a><br/></td>
<td>Désassemble le code HLSL compilé.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect"><strong>D3DDisassemble10Effect</strong></a><br/></td>
<td>Désassemble le code HLSL compilé à partir d’un effet Direct3D10.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/d3d11shadertracing/nf-d3d11shadertracing-d3ddisassemble11trace"><strong>D3DDisassemble11Trace</strong></a><br/></td>
<td>Désassemble une section du code HLSL compilé qui est spécifiée par les étapes de trace du nuanceur.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassembleregion"><strong>D3DDisassembleRegion</strong></a><br/></td>
<td>Désassemble une région spécifique de code HLSL compilé.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a><br/></td>
<td>Récupère une partie spécifique d’un résultat de compilation.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetdebuginfo"><strong>D3DGetDebugInfo</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Vous pouvez utiliser cette API pour développer vos applications du Windows Store, mais vous ne pouvez pas l’utiliser dans les applications que vous envoyez au Windows Store.
</blockquote>
<br/> Obtient les informations de débogage du nuanceur.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputandoutputsignatureblob"><strong>D3DGetInputAndOutputSignatureBlob</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
<a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputandoutputsignatureblob"><strong>D3DGetInputAndOutputSignatureBlob</strong></a> peut être modifié ou non disponible pour les mises en production après Windows 8.1. Utilisez plutôt <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a> avec la valeur <a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_INPUT_AND_OUTPUT_SIGNATURE_BLOB</strong></a> .
</blockquote>
<br/> Obtient les signatures d’entrée et de sortie à partir d’un résultat de compilation.<br/></td>
</tr>
<tr class="odd">
<td>[<strong>D3DGetInputSignatureBlob</strong>] (/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputsignatureblob)<br/></td>
<td><blockquote>
[!Note]<br />
<a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputsignatureblob"><strong>D3DGetInputSignatureBlob</strong></a> peut être modifié ou non disponible pour les mises en production après Windows 8.1. Utilisez plutôt <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a> avec la valeur <a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_INPUT_SIGNATURE_BLOB</strong></a> .
</blockquote>
<br/> Obtient la signature d’entrée à partir d’un résultat de compilation.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetoutputsignatureblob"><strong>D3DGetOutputSignatureBlob</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
<a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetoutputsignatureblob"><strong>D3DGetOutputSignatureBlob</strong></a> peut être modifié ou non disponible pour les mises en production après Windows 8.1. Utilisez plutôt <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a> avec la valeur <a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_OUTPUT_SIGNATURE_BLOB</strong></a> .
</blockquote>
<br/> Obtient la signature de sortie à partir d’un résultat de compilation.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgettraceinstructionoffsets"><strong>D3DGetTraceInstructionOffsets</strong></a><br/></td>
<td>Récupère les décalages d’octets pour les instructions dans une section du code du nuanceur.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dloadmodule"><strong>D3DLoadModule</strong></a><br/></td>
<td>Crée une interface de module Shader à partir des données sources pour le module Shader. <br/>
<blockquote>
[!Note]<br />
Cette fonction fait partie de la technologie de liaison de nuanceur HLSL que vous pouvez utiliser sur toutes les plateformes Direct3D 11 pour créer des fonctions HLSL précompilées, les empaqueter dans des bibliothèques et les lier à des nuanceurs complets au moment de l’exécution.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess"><strong>D3DPreprocess</strong></a><br/></td>
<td>Prétraite le code HLSL non compilé.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreadfiletoblob"><strong>D3DReadFileToBlob</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Vous pouvez utiliser cette API pour développer vos applications du Windows Store, mais vous ne pouvez pas l’utiliser dans les applications que vous envoyez au Windows Store.
</blockquote>
<br/> Lit un fichier qui se trouve sur le disque en mémoire.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect"><strong>D3DReflect</strong></a><br/></td>
<td>Obtient un pointeur vers une interface de réflexion.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dreflectlibrary"><strong>D3DReflectLibrary</strong></a><br/></td>
<td>Crée une interface de réflexion de bibliothèque à partir de données sources qui contient une bibliothèque de fonctions HLSL. <br/>
<blockquote>
[!Note]<br />
Cette fonction fait partie de la technologie de liaison de nuanceur HLSL que vous pouvez utiliser sur toutes les plateformes Direct3D 11 pour créer des fonctions HLSL précompilées, les empaqueter dans des bibliothèques et les lier à des nuanceurs complets au moment de l’exécution.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dsetblobpart"><strong>D3DSetBlobPart</strong></a><br/></td>
<td>Définit des informations dans un résultat de compilation.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dstripshader"><strong>D3DStripShader</strong></a><br/></td>
<td>Supprime les objets BLOB indésirables d’un résultat de compilation.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dwriteblobtofile"><strong>D3DWriteBlobToFile</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Vous pouvez utiliser cette API pour développer vos applications du Windows Store, mais vous ne pouvez pas l’utiliser dans les applications que vous envoyez au Windows Store.
</blockquote>
<br/> Écrit un objet blob de mémoire dans un fichier sur le disque.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence D3DCompiler](dx-graphics-d3dcompiler-reference.md)
</dt> </dl>

