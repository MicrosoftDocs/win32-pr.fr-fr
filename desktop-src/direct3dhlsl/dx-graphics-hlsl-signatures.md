---
title: Signatures
description: Une signature de nuanceur est une liste des paramètres qui sont des entrées ou des sorties d’une fonction de nuanceur.
ms.assetid: c73a4f3e-e6fa-4e49-9ee8-4e200269dba7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 37906222ec674c2c1bb5e1cdfea1cb2de2e1df3d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104990652"
---
# <a name="signatures"></a>Signatures

Une signature de nuanceur est une liste des paramètres qui sont des entrées ou des sorties d’une fonction de nuanceur. Dans Direct3D 10, les étapes adjacentes partagent efficacement un tableau de registres, où le nuanceur de sortie (ou étape de pipeline) écrit des données à des emplacements spécifiques dans le tableau des registres et le nuanceur d’entrée doit lire les mêmes emplacements. L’API utilise des signatures de nuanceur pour lier les sorties de nuanceur avec des entrées sans la surcharge de la résolution sémantique.

Dans Direct3D 10, les signatures d’entrée sont générées à partir d’une déclaration d’entrée de nuanceur et la signature de sortie est générée à partir d’une déclaration de nuanceur-sortie. Une signature d’entrée est dite compatible avec une signature de sortie lorsque la signature de sortie est un sous-ensemble strict (type d’argument et correspondance d’ordre) de la signature d’entrée. La méthode la plus simple pour y parvenir consiste à lier les entrées et sorties de nuanceur correspondantes par le même type de structure.

Voici un exemple de signatures compatibles.


```
// Vertex Shader Output Signature
Struct VSOut
{
  float4 Pos: SV_Position;
  float3 MyNormal: Normal;
  float2 MyTex : Texcoord0;
}

// Pixel Shader Input Signature
Struct PSInWorks
{
  float4 Pos: SV_Position;
  float3 MyNormal: Normal;
}
```



Voici un exemple de signatures incompatibles ; l’ordre des paramètres dans la signature d’entrée ne correspond pas à l’ordre dans la signature de sortie.


```
// Vertex Shader Output Signature
Struct VSOut
{
  float4 Pos: SV_Position;
  float3 MyNormal: Normal;
  float2 MyTex : Texcoord0;
}

// Pixel Shader Input Signature
Struct PSInFails
{
  float3 MyNormal: Normal;
  float4 Pos: SV_Position;
}
```



PSInWorks est un sous-ensemble compatible de VSOut (les deux premières entrées correspondent à la fois à type et à commande avec les deux premières entrées dans VSOut). Toutefois, PSInFails est incompatible, car le classement ne correspond pas à VSOut.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fonctions](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 




