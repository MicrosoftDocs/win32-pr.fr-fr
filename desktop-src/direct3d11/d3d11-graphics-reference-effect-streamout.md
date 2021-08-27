---
title: Syntaxe du flux de sortie
description: Un nuanceur Geometry avec flux sortant est déclaré avec une syntaxe particulière.
ms.assetid: 58cf6503-0dde-4c88-837d-ae0e0eda17d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43980d79d9c338a965d7ab2f2ceb008411d9713dec935d953dd5a1854c40465b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096389"
---
# <a name="stream-out-syntax"></a>Syntaxe du flux de sortie

Un nuanceur Geometry avec flux sortant est déclaré avec une syntaxe particulière. Cette rubrique décrit la syntaxe. Dans le runtime Effect, cette syntaxe est convertie en un appel à [**ID3D11Device :: CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput).

## <a name="construct-syntax"></a>Syntaxe de construction


```
[ StreamingShaderVar = ] ConstructGSWithSO( ShaderVar, "OutputDecl0" )
```





| Nom                   | Description                                                                                                                                                                                                                |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **StreamingShaderVar** | Facultatif. Chaîne ASCI qui identifie de façon unique le nom d’une variable de nuanceur Geometry avec un flux sortant. Cela est facultatif, car ConstructGSWithSO peut être placé directement dans un appel SetGeometryShader ou BindInterfaces. |
| **ShaderVar**          | Une variable de nuanceur Geometry ou vertex.                                                                                                                                                                               |
| **OutputDecl0**        | Une chaîne qui définit les sorties de nuanceur dans le flux 0 sont transmises en continu. Voir ci-dessous pour connaître la syntaxe.                                                                                                                                 |



 

Il s’agit de la syntaxe définie dans \_ les \_ fichiers FX 4 0. Notez que dans \_ \_ les nuanciers GS 4 0 et vs \_ x, il n’y a qu’un seul flux de données. Le nuanceur résultant produira un flux à la fois dans l’unité de diffusion en continu et l’unité de rastérisation.


```
[ StreamingShaderVar = ] ConstructGSWithSO( ShaderVar, "OutputDecl0", "OutputDecl1", "OutputDecl2", 
"OutputDecl3", RasterizedStream )
```





| Nom                   | Description                                                                                                                                                                                                                |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **StreamingShaderVar** | Facultatif. Chaîne ASCI qui identifie de façon unique le nom d’une variable de nuanceur Geometry avec un flux sortant. Cela est facultatif, car ConstructGSWithSO peut être placé directement dans un appel SetGeometryShader ou BindInterfaces. |
| **ShaderVar**          | Une variable de nuanceur Geometry ou vertex.                                                                                                                                                                               |
| **OutputDecl0**        | Une chaîne qui définit les sorties de nuanceur dans le flux 0 sont transmises en continu. Voir ci-dessous pour connaître la syntaxe.                                                                                                                                 |
| **OutputDecl1**        | Une chaîne qui définit les sorties de nuanceur dans le flux 1 sont transmises en continu. Voir ci-dessous pour connaître la syntaxe.                                                                                                                                 |
| **OutputDecl2**        | Une chaîne qui définit les sorties de nuanceur dans le flux 2 sont transmises en continu. Voir ci-dessous pour connaître la syntaxe.                                                                                                                                 |
| **OutputDecl3**        | Une chaîne qui définit les sorties de nuanceur dans le flux 3 sont transmises en continu. Voir ci-dessous pour connaître la syntaxe.                                                                                                                                 |
| **RasterizedStream**   | Entier spécifiant le flux qui sera envoyé au rastériseur.                                                                                                                                                         |



 

Notez que \_ \_ les nuanceurs GS 5 0 peuvent définir jusqu’à quatre flux de données. Le nuanceur résultant produira un flux de sortie vers l’unité d’extraction de flux pour chaque déclaration de sortie non **null** et un flux de l’unité de rastérisation.

## <a name="stream-out-declaration-syntax"></a>Syntaxe de déclaration de flux de sortie


```
" [ Buffer: ] Semantic[ SemanticIndex ] [ .Mask ]; [ ... ; ] ... [ ... ;]"
```





| Nom              | Description                                                                                           |
|-------------------|-------------------------------------------------------------------------------------------------------|
| **Buffer**        | Facultatif. Un entier, 0 <= buffer < 4, spécifiant la mémoire tampon de sortie de flux vers laquelle la valeur doit être redirigée. |
| **Équivalent**      | Chaîne, avec SemanticIndex, spécifiant la valeur à générer.                                 |
| **SemanticIndex** | Facultatif. Index associé à la sémantique.                                                         |
| **Mask**          | Facultatif. Masque de composant indiquant les composants de la valeur à générer.                       |



 

Il existe une sémantique spéciale, nommée « $SKIP », qui indique une sémantique vide, laissant la mémoire correspondante dans le flux sans toucher. La sémantique $SKIP ne peut pas avoir de SemanticIndex, mais peut avoir un masque.

La déclaration out du flux entier peut avoir la **valeur null**.

## <a name="example"></a>Exemple


```
struct GSOutput
{
int4 Pos : Position;
int4 Color : Color;
int4 Texcoord : Texcoord;
};

[maxvertexcount(1)]
void gsBase (inout PointStream<GSOutput> OutputStream, inout PointStream<GSOutput> OutputStream1)
{
GSOutput output;
output.Pos = int4(1,2,3,4);
output.Color = int4(5,6,7,8);
output.Texcoord = int4(9,10,11,12);
OutputStream.Append(output);

output.Pos = int4(1,2,3,4);
    output.Color = int4(5,6,7,8);
output.Texcoord = int4(9,10,11,12);
OutputStream1.Append(output);
};


GeometryShader pGSComp = CompileShader(gs_5_0, gsBase());
GeometryShader pGSwSO = ConstructGSWithSO(pGSComp, "0:Position.xy; 1:Position.zw; 2:Color.xy", 
                                                   "3:Texcoord.xyzw; 3:$SKIP.x;", NULL, NULL, 1);

// The following two passes perform the same operation
technique11 SOPoints
{
    pass 
    {
        SetGeometryShader(ConstructGSWithSO(pGSComp, "0:Position.xy; 1:Position.zw; 2:Color.xy", 
                                                     "3:Texcoord.xyzw; 3:$SKIP.x;", NULL, NULL, 1));
    }
    pass 
    {
        SetGeometryShader(pGSwSO);
    }
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Effets (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 




