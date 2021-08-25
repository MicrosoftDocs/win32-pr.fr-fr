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
ms.openlocfilehash: 43d9bf2feb572d7b410d702dbc456af7c18be0ee
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465806"
---
# <a name="compiler-functions-hlsl-reference"></a>Fonctions du compilateur (référence HLSL)

Cette section contient des informations sur les fonctions de compilateur HLSL Direct3D suivantes :

## <a name="in-this-section"></a>Contenu de cette section




| Rubrique | Description | 
|-------|-------------|
| <a href="d3d11reflect.md"><strong>D3D11Reflect</strong></a><br /> | Obtient un pointeur vers une interface de réflexion.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile"><strong>D3DCompile</strong></a><br /> | Compilez le code HLSL ou un fichier d’effet en bytecode pour une cible donnée.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2"><strong>D3DCompile2</strong></a><br /> | Compile le code HLSL (High Level Shader Language) de Microsoft en bytecode pour une cible donnée.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile"><strong>D3DCompileFromFile</strong></a><br /> | <blockquote>[!Note]<br />vous pouvez utiliser cette API pour développer vos applications Windows store, mais vous ne pouvez pas l’utiliser dans les applications que vous envoyez au magasin de Windows. Reportez-vous à la section « compilation des nuanceurs pour UWP » dans les notes de <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2"><strong>D3DCompile2</strong></a>.</blockquote><br /> Compile le code HLSL en bytecode pour une cible donnée.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompressshaders"><strong>D3DCompressShaders</strong></a><br /> | <blockquote>[!Note]<br />vous pouvez utiliser cette API pour développer vos applications Windows store, mais vous ne pouvez pas l’utiliser dans les applications que vous envoyez au magasin de Windows.</blockquote><br /> Compresse un ensemble de nuanceurs dans une forme plus compacte. <br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcreateblob"><strong>D3DCreateBlob</strong></a><br /> | Crée une mémoire tampon.<br /> | 
| <a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph"><strong>D3DCreateFunctionLinkingGraph</strong></a><br /> | Crée une interface de graphe de liaison de fonction. <br /><blockquote>[!Note]<br />Cette fonction fait partie de la technologie de liaison de nuanceur HLSL que vous pouvez utiliser sur toutes les plateformes Direct3D 11 pour créer des fonctions HLSL précompilées, les empaqueter dans des bibliothèques et les lier à des nuanceurs complets au moment de l’exécution.</blockquote><br /> | 
| <a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker"><strong>D3DCreateLinker</strong></a><br /> | Crée une interface de l’éditeur de liens. <br /><blockquote>[!Note]<br />Cette fonction fait partie de la technologie de liaison de nuanceur HLSL que vous pouvez utiliser sur toutes les plateformes Direct3D 11 pour créer des fonctions HLSL précompilées, les empaqueter dans des bibliothèques et les lier à des nuanceurs complets au moment de l’exécution.</blockquote><br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddecompressshaders"><strong>D3DDecompressShaders</strong></a><br /> | <blockquote>[!Note]<br />vous pouvez utiliser cette API pour développer vos applications Windows store, mais vous ne pouvez pas l’utiliser dans les applications que vous envoyez au magasin de Windows.</blockquote><br /> Décompresse un ou plusieurs nuanceurs d’un jeu compressé. <br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble"><strong>D3DDisassemble</strong></a><br /> | Désassemble le code HLSL compilé.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect"><strong>D3DDisassemble10Effect</strong></a><br /> | Désassemble le code HLSL compilé à partir d’un effet Direct3D10.<br /> | 
| <a href="/windows/win32/api/d3d11shadertracing/nf-d3d11shadertracing-d3ddisassemble11trace"><strong>D3DDisassemble11Trace</strong></a><br /> | Désassemble une section du code HLSL compilé qui est spécifiée par les étapes de trace du nuanceur.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassembleregion"><strong>D3DDisassembleRegion</strong></a><br /> | Désassemble une région spécifique de code HLSL compilé.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a><br /> | Récupère une partie spécifique d’un résultat de compilation.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetdebuginfo"><strong>D3DGetDebugInfo</strong></a><br /> | <blockquote>[!Note]<br />vous pouvez utiliser cette API pour développer vos applications Windows store, mais vous ne pouvez pas l’utiliser dans les applications que vous envoyez au magasin de Windows.</blockquote><br /> Obtient les informations de débogage du nuanceur.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputandoutputsignatureblob"><strong>D3DGetInputAndOutputSignatureBlob</strong></a><br /> | <blockquote>[!Note]<br /><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputandoutputsignatureblob"><strong>D3DGetInputAndOutputSignatureBlob</strong></a> peut être modifié ou non disponible pour les mises en production après Windows 8.1. Utilisez plutôt <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a> avec la valeur <a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_INPUT_AND_OUTPUT_SIGNATURE_BLOB</strong></a> .</blockquote><br /> Obtient les signatures d’entrée et de sortie à partir d’un résultat de compilation.<br /> | 
| [<strong>D3DGetInputSignatureBlob</strong>](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputsignatureblob)<br /> | <blockquote>[!Note]<br /><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputsignatureblob"><strong>D3DGetInputSignatureBlob</strong></a> peut être modifié ou non disponible pour les mises en production après Windows 8.1. Utilisez plutôt <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a> avec la valeur <a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_INPUT_SIGNATURE_BLOB</strong></a> .</blockquote><br /> Obtient la signature d’entrée à partir d’un résultat de compilation.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetoutputsignatureblob"><strong>D3DGetOutputSignatureBlob</strong></a><br /> | <blockquote>[!Note]<br /><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetoutputsignatureblob"><strong>D3DGetOutputSignatureBlob</strong></a> peut être modifié ou non disponible pour les mises en production après Windows 8.1. Utilisez plutôt <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a> avec la valeur <a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_OUTPUT_SIGNATURE_BLOB</strong></a> .</blockquote><br /> Obtient la signature de sortie à partir d’un résultat de compilation.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgettraceinstructionoffsets"><strong>D3DGetTraceInstructionOffsets</strong></a><br /> | Récupère les décalages d’octets pour les instructions dans une section du code du nuanceur.<br /> | 
| <a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dloadmodule"><strong>D3DLoadModule</strong></a><br /> | Crée une interface de module Shader à partir des données sources pour le module Shader. <br /><blockquote>[!Note]<br />Cette fonction fait partie de la technologie de liaison de nuanceur HLSL que vous pouvez utiliser sur toutes les plateformes Direct3D 11 pour créer des fonctions HLSL précompilées, les empaqueter dans des bibliothèques et les lier à des nuanceurs complets au moment de l’exécution.</blockquote><br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess"><strong>D3DPreprocess</strong></a><br /> | Prétraite le code HLSL non compilé.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreadfiletoblob"><strong>D3DReadFileToBlob</strong></a><br /> | <blockquote>[!Note]<br />vous pouvez utiliser cette API pour développer vos applications Windows store, mais vous ne pouvez pas l’utiliser dans les applications que vous envoyez au magasin de Windows.</blockquote><br /> Lit un fichier qui se trouve sur le disque en mémoire.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect"><strong>D3DReflect</strong></a><br /> | Obtient un pointeur vers une interface de réflexion.<br /> | 
| <a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dreflectlibrary"><strong>D3DReflectLibrary</strong></a><br /> | Crée une interface de réflexion de bibliothèque à partir de données sources qui contient une bibliothèque de fonctions HLSL. <br /><blockquote>[!Note]<br />Cette fonction fait partie de la technologie de liaison de nuanceur HLSL que vous pouvez utiliser sur toutes les plateformes Direct3D 11 pour créer des fonctions HLSL précompilées, les empaqueter dans des bibliothèques et les lier à des nuanceurs complets au moment de l’exécution.</blockquote><br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dsetblobpart"><strong>D3DSetBlobPart</strong></a><br /> | Définit des informations dans un résultat de compilation.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dstripshader"><strong>D3DStripShader</strong></a><br /> | Supprime les objets BLOB indésirables d’un résultat de compilation.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dwriteblobtofile"><strong>D3DWriteBlobToFile</strong></a><br /> | <blockquote>[!Note]<br />vous pouvez utiliser cette API pour développer vos applications Windows store, mais vous ne pouvez pas l’utiliser dans les applications que vous envoyez au magasin de Windows.</blockquote><br /> Écrit un objet blob de mémoire dans un fichier sur le disque.<br /> | 




 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence D3DCompiler](dx-graphics-d3dcompiler-reference.md)
</dt> </dl>

