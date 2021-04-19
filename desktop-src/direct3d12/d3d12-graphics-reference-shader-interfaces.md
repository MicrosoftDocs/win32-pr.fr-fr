---
title: Interfaces du nuanceur (Direct3D 12 Graphics)
description: D3d12shader. h déclare les interfaces suivantes.
ms.assetid: 791d2c91-3791-47fe-b887-8117ecc798ba
keywords:
- interfaces, nuanceur Direct3D 12
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16f111572aacca36f12600b0cf334895684064e5
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "106509491"
---
# <a name="shader-interfaces-direct3d-12-graphics"></a>Interfaces du nuanceur (Direct3D 12 Graphics)

d3d12shader. h déclare les interfaces suivantes.

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
<td><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12functionparameterreflection"><strong>ID3D12FunctionParameterReflection</strong></a><br/></td>
<td>Une interface de fonction-paramètre-Reflection accède aux informations sur les paramètres de fonction. <br/>
<blockquote>
[!Note]<br />
Cette interface fait partie de la technologie de liaison de nuanceur HLSL que vous pouvez utiliser sur toutes les plateformes Direct3D 12 pour créer des fonctions HLSL précompilées, les empaqueter dans des bibliothèques et les lier à des nuanceurs complets au moment de l’exécution.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12functionreflection"><strong>ID3D12FunctionReflection</strong></a><br/></td>
<td>Une interface de réflexion de fonction accède aux informations de la fonction. <br/>
<blockquote>
[!Note]<br />
Cette interface fait partie de la technologie de liaison de nuanceur HLSL que vous pouvez utiliser sur toutes les plateformes Direct3D 12 pour créer des fonctions HLSL précompilées, les empaqueter dans des bibliothèques et les lier à des nuanceurs complets au moment de l’exécution.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12libraryreflection"><strong>ID3D12LibraryReflection</strong></a><br/></td>
<td>Une interface de réflexion de bibliothèque accède aux informations de la bibliothèque. <br/>
<blockquote>
[!Note]<br />
Cette interface fait partie de la technologie de liaison de nuanceur HLSL que vous pouvez utiliser sur toutes les plateformes Direct3D 12 pour créer des fonctions HLSL précompilées, les empaqueter dans des bibliothèques et les lier à des nuanceurs complets au moment de l’exécution.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflection"><strong>ID3D12ShaderReflection</strong></a><br/></td>
<td>Une interface de nuanceur-réflexion accède à des informations de nuanceur. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectionconstantbuffer"><strong>ID3D12ShaderReflectionConstantBuffer</strong></a><br/></td>
<td>Cette interface de nuanceur-réflexion fournit l’accès à une mémoire tampon constante. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectiontype"><strong>ID3D12ShaderReflectionType</strong></a><br/></td>
<td>Cette interface de nuanceur-réflexion donne accès au type de variable. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectionvariable"><strong>ID3D12ShaderReflectionVariable</strong></a><br/></td>
<td>Cette interface de nuanceur-réflexion donne accès à une variable. <br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence de Direct3D 12](direct3d-12-reference.md)
</dt> <dt>

[Référence du nuanceur](d3d12-graphics-reference-shader-reference.md)
</dt> </dl>

 

 





