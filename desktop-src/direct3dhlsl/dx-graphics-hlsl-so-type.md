---
title: Objet Stream-Output
description: Un objet de sortie de flux est un objet basé sur un modèle qui diffuse en continu des données à partir de l’étape Geometry-Shader. Utilisez la syntaxe suivante pour déclarer un objet de sortie de flux.
ms.assetid: 07a5489c-c238-4466-9282-5b168448aff7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 79e0247b424ebb6f72622565845c17b622ab715cd8860a83ce24ae58ac7420c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789479"
---
# <a name="stream-output-object"></a>Objet Stream-Output

Un objet de sortie de flux est un objet basé sur un modèle qui diffuse en continu des données à partir de l' [étape Geometry-Shader](/previous-versions//bb205146(v=vs.85)). Utilisez la syntaxe suivante pour déclarer un objet de sortie de flux.



| INOUT *StreamOutputObject* < nom de *type de données* >  *;* |
|------------------------------------------------------|



 

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="StreamOutputObject___________________________DataType_________________________________________Name"></span><span id="streamoutputobject___________________________datatype_________________________________________name"></span><span id="STREAMOUTPUTOBJECT___________________________DATATYPE_________________________________________NAME"></span>*StreamOutputObject*  <  *Type de données*  >    *Nom*
</dt> <dd>

Déclaration de l’objet de sortie de flux (SO).



| Types d’objets Stream-Output | Description                       |
|----------------------------|-----------------------------------|
| *PointStream*              | Séquence de primitives de point    |
| *LineStream*               | Séquence de primitives de ligne     |
| *TriangleStream*           | Une séquence de primitives de triangle |



 

Type de données *DataType* -output ; peut être n’importe quel [type de données HLSL](dx-graphics-hlsl-data-types.md). Doit être entouré des crochets pointus.

*Nom-nom* de la variable ; chaîne ASCII qui identifie l’objet de façon unique.

</dd> </dl>

## <a name="example"></a>Exemple

Il s’agit d’un exemple de déclaration d’objet de sortie de flux qui diffuse en continu des primitives de triangle dont les données sont définies par l' \_ carte cubique PS \_ dans la structure. Le nuanceur Geometry est limité à la génération de 18 vertex.


```
struct PS_CUBEMAP_IN
{
    float4 Pos : SV_POSITION;     // Projection coord
    float2 Tex : TEXCOORD0;       // Texture coord
    uint RTIndex : SV_RenderTargetArrayIndex;
};

[maxvertexcount(18)]
void main( inout TriangleStream<PS_CUBEMAP_IN> CubeMapStream, triangle PS_CUBEMAP_INT[3] )
{
    ...
}
```



Il s’agit d’un extrait de code de l' [exemple CubeMapGS](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx).

## <a name="stream-output-object-methods"></a>Méthodes d’objet Stream-Output

Utilisez la syntaxe suivante pour appeler des méthodes d’objet de sortie de flux.


```
Object.Method
```



Les méthodes suivantes sont implémentées.



| Méthodes                                              | Description                                                      |
|------------------------------------------------------|------------------------------------------------------------------|
| [Append](dx-graphics-hlsl-so-append.md)             | Ajoute des données de sortie à un flux existant.                        |
| [RestartStrip](dx-graphics-hlsl-so-restartstrip.md) | Mettez fin à la bande primitive actuelle et démarrez une nouvelle bande primitive. |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cet objet est pris en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                        | Pris en charge |
|---------------------------------------------------------------------|-----------|
| [Nuancier modèle 4](dx-graphics-hlsl-sm4.md) et modèles de nuanceur supérieurs | oui       |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 