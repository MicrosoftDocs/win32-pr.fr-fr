---
title: Arguments de fonction
description: Une fonction accepte un ou plusieurs arguments d’entrée ; pour déclarer chaque argument, utilisez la syntaxe ci-après.
ms.assetid: 80e0dbc8-26b7-4250-bb01-6856fc70f6b8
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bcc89d3e4be22dcf56cf0d7d7966311f79954d48
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122631571"
---
# <a name="function-arguments"></a>Arguments de fonction

Une fonction accepte un ou plusieurs arguments d’entrée ; pour déclarer chaque argument, utilisez la syntaxe ci-après.



|                                                                                             |
|---------------------------------------------------------------------------------------------|
| **\[\]Nom du type InputModifier \[ : sémantique \] \[ InterpolationModifier \] \[ = initialiseurs\]** |



 

\[Nom du type de modificateur \] \[ : sémantique \] \[ : modificateur d’interpolation \] \[ = initialiseur (s)\]

S’il existe plusieurs arguments de fonction, ils sont séparés par des virgules.

## <a name="parameters"></a>Paramètres



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Élément</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="InputModifier"></span><span id="inputmodifier"></span><span id="INPUTMODIFIER"></span><strong>InputModifier</strong><br/></td>
<td>Terme facultatif qui identifie un argument comme une entrée, une sortie ou les deux.<br/> 
<table>
<tbody>
<tr class="odd">
<td>Valeur</td>
<td>Description</td>
</tr>
<tr class="even">
<td><strong>in</strong></td>
<td>Entrée uniquement</td>
</tr>
<tr class="odd">
<td><strong>INOUT</strong></td>
<td>Entrée et sortie</td>
</tr>
<tr class="even">
<td><strong>out</strong></td>
<td>Sortie uniquement</td>
</tr>
<tr class="odd">
<td><strong>uniforme</strong></td>
<td>Données de constante en entrée uniquement</td>
</tr>
</tbody>
</table>

<p> </p>
<p>Les paramètres sont toujours passés par valeur. dans indique que la valeur du paramètre doit être copiée à partir de l’application appelante avant le début de la fonction. out indique que la dernière valeur du paramètre doit être copiée et retournée à l’application appelante lorsque la fonction retourne. INOUT est un raccourci permettant de spécifier les deux.</p>
<p>Une valeur uniforme provient d’un registre de constantes ; chaque appel de nuanceur de sommet ou de nuanceur de pixels affiche la même valeur initiale pour une variable uniforme. Les variables globales sont traitées comme si elles étaient déclarées comme uniformes. Pour les fonctions non de niveau supérieur, Uniform est synonyme de <strong>dans</strong>. Si aucune utilisation de paramètre n’est spécifiée, l’utilisation des paramètres est supposée être <strong>dans</strong>.</p></td>
</tr>
<tr class="even">
<td><p><span id="Type"></span><span id="type"></span><span id="TYPE"></span><strong>Entrer</strong></p></td>
<td><p>Type d’argument ; peut être n’importe quel <a href="dx-graphics-hlsl-data-types.md">type</a>HLSL valide.</p></td>
</tr>
<tr class="odd">
<td><p><span id="Name"></span><span id="name"></span><span id="NAME"></span><strong>Nomme</strong></p></td>
<td><p>Chaîne ASCII qui identifie de façon unique le nom de la fonction de nuanceur.</p></td>
</tr>
<tr class="even">
<td><p><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span><strong>Équivalent</strong></p></td>
<td><p>Chaîne facultative qui identifie l’utilisation prévue des données (voir <a href="dx-graphics-hlsl-semantics.md">sémantique (DirectX HLSL)</a>).</p></td>
</tr>
<tr class="odd">
<td><p><span id="InterpolationModifier"></span><span id="interpolationmodifier"></span><span id="INTERPOLATIONMODIFIER"></span><strong>InterpolationModifier</strong></p></td>
<td><p><a href="dx-graphics-hlsl-struct.md">Modificateur d’interpolation</a> facultatif qui permet à un nuanceur de déterminer la méthode d’interpolation. Un modificateur d’interpolation sur un argument de fonction s’applique uniquement à un argument utilisé comme entrée d’une fonction de nuanceur de pixels.</p></td>
</tr>
<tr class="even">
<td><p><span id="Initializers"></span><span id="initializers"></span><span id="INITIALIZERS"></span><strong>Initialiseurs</strong></p></td>
<td><p>Valeurs facultatives pour l’initialisation ; plusieurs valeurs sont requises pour initialiser des types de données à plusieurs composants.</p></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Remarques

Les arguments de fonction sont répertoriés dans une liste d’arguments séparés par des virgules dans une déclaration de fonction. Comme dans les fonctions C, chaque argument doit avoir un nom de paramètre et un type déclarés ; un argument d’une fonction HLSL peut éventuellement inclure une sémantique, une valeur initiale et une entrée de nuanceur de pixels peut inclure un type d’interpolation.

Le *type* d’un argument de fonction peut être une structure, qui peut inclure un modificateur d’interpolation par membre. Si l’argument de fonction a également un modificateur d’interpolation, le modificateur d’argument de fonction remplace les modificateurs d’interpolation déclarés dans le type.

## <a name="examples"></a>Exemples

Cet exemple (à partir de l' [exemple BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)) illustre des entrées uniformes et non uniformes dans une fonction de nuanceur de sommets.


```
VS_OUTPUT RenderSceneVS( 
  float4 vPos : POSITION,
  float3 vNormal : NORMAL,
  float2 vTexCoord0 : TEXCOORD,
  uniform int nNumLights,
  uniform bool bTexture,
  uniform bool bAnimate )
{
  ...
}
```



Cet exemple (à partir de l' [exemple ContentStreaming](https://msdn.microsoft.com/library/Ee416397(v=VS.85).aspx)) utilise une structure d’entrée pour passer des arguments à une fonction de nuanceur de pixels.


```
VSBasicIn input
struct VSBasicIn
{
  float4 Pos    : POSITION;
  float3 Norm   : NORMAL;
  float2 Tex    : TEXCOORD0;
};

PSBasicIn VSBasic(VSBasicIn input)
{
  ...
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fonctions (DirectX HLSL)](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 





