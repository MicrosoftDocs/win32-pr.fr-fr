---
title: Objet Geometry-Shader
description: Un objet de nuanceur Geometry traite les primitives entières. Pour déclarer un objet Geometry-Shader, utilisez la syntaxe ci-après.
ms.assetid: d5c1c22b-6fa6-40a8-900f-6d74f74468c1
keywords:
- maxvertexcount (DirectX HLSL)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e06bbc184a4b5f82d5edaaf7fdbfbd55f1906f12
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120614"
---
# <a name="geometry-shader-object"></a>Objet Geometry-Shader

Un objet de nuanceur Geometry traite les primitives entières. Pour déclarer un objet Geometry-Shader, utilisez la syntaxe ci-après.

\[maxvertexcount (*NumVerts*) \] void *ShaderName* ( *PrimitiveType nom du type de données \[ \] NumElements*, INOUT *StreamOutputObject* );



 

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="_maxvertexcount_NumVerts__"></span><span id="_maxvertexcount_numverts__"></span><span id="_MAXVERTEXCOUNT_NUMVERTS__"></span>\[maxvertexcount (*NumVerts*)\]
</dt> <dd>

\[dans une \] déclaration pour le nombre maximal de vertex à créer.

-   \[maxvertexcount () \] -mot clé required ; les crochets et les parenthèses sont des caractères requis pour une syntaxe correcte.
-   *NumVerts* : nombre entier représentant le nombre de vertex.

</dd> <dt>

<span id="ShaderName"></span><span id="shadername"></span><span id="SHADERNAME"></span>*ShaderName*
</dt> <dd>

\[dans \] une chaîne ASCII qui contient un nom unique pour la fonction Geometry-Shader.

</dd> <dt>

<span id="PrimitiveType_DataType_Name___NumElements__"></span><span id="primitivetype_datatype_name___numelements__"></span><span id="PRIMITIVETYPE_DATATYPE_NAME___NUMELEMENTS__"></span>*Nom de type de données PrimitiveType \[ NumElements \]*
</dt> <dd>

*PrimitiveType* -type primitif, qui détermine l’ordre des données Primitives.



| Type primitif | Description                                                   |
|----------------|---------------------------------------------------------------|
| *point*        | Liste des points                                                    |
| *spline*         | Liste de lignes ou de lignes                                       |
| *placé*     | Liste de triangles ou bande triangulaire                               |
| *lineadj*      | Liste des lignes avec contiguïté ou frange avec contiguïté         |
| *triangleadj*  | Liste de triangles avec contiguïté ou bande triangulaire avec contiguïté |



 

*Type de données*  -  \[ dans \] un type de données d’entrée, peut être n’importe quel [type de données HLSL](dx-graphics-hlsl-data-types.md).

*Nom* -argument Name ; Il s’agit d’une chaîne ASCII.

*NumElements* : taille du tableau de l’entrée, qui dépend du *PrimitiveType* , comme indiqué dans le tableau suivant.

| Type primitif | NumElements                                                                                                  |
|----------------|--------------------------------------------------------------------------------------------------------------|
| *point*        | \[1\]<br/> Vous ne pouvez utiliser qu’un seul point à la fois.<br/>                                         |
| *spline*         | \[2\]<br/> Une ligne requiert deux vertex.<br/>                                                    |
| *placé*     | \[3\]<br/> Un triangle requiert trois vertex.<br/>                                              |
| *lineadj*      | \[4\]<br/> Un lineadj a deux extrémités ; par conséquent, il requiert quatre vertex.<br/>                    |
| *triangleadj*  | \[6\]<br/> Une bordure triangleadj trois triangles supplémentaires ; par conséquent, il requiert six vertex.<br/> |



 

</dd> <dt>

<span id="StreamOutputObject"></span><span id="streamoutputobject"></span><span id="STREAMOUTPUTOBJECT"></span>*StreamOutputObject*
</dt> <dd>

Déclaration de l' [objet de sortie de flux](dx-graphics-hlsl-so-type.md).

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

None

## <a name="remarks"></a>Remarques

Le diagramme suivant montre les différents types primitifs pour un objet de nuanceur Geometry.

![illustration des différents types primitifs pour un objet de nuanceur Geometry](images/d3d11-gsinputs1.png)

Le diagramme suivant illustre les appels de nuanceur Geometry.

![illustration des appels de nuanceur Geometry](images/d3d11-gsinputs2.png)

## <a name="examples"></a>Exemples

Cet exemple est issu de l’exercice 1 de l' [atelier 4,0 de l’atelier du modèle de nuanceur Direct3D 10](https://msdn.microsoft.com/library/Ee416554(v=VS.85).aspx).


```
[maxvertexcount(3)]
void GSScene( triangleadj GSSceneIn input[6], inout TriangleStream<PSSceneIn> OutputStream )
{   
    PSSceneIn output = (PSSceneIn)0;

    for( uint i=0; i<6; i+=2 )
    {
        output.Pos = input[i].Pos;
        output.Norm = input[i].Norm;
        output.Tex = input[i].Tex;
        
        OutputStream.Append( output );
    }
    
    OutputStream.RestartStrip();
}
```



## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cet objet est pris en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                        | Prise en charge |
|---------------------------------------------------------------------|-----------|
| [Nuancier modèle 4](dx-graphics-hlsl-sm4.md) et modèles de nuanceur supérieurs | yes       |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 





