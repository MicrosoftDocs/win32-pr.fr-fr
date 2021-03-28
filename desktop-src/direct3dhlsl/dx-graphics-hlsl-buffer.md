---
title: Type de mémoire tampon
description: Pour déclarer une variable de mémoire tampon, utilisez la syntaxe ci-après.
ms.assetid: f21f0de5-58e3-466b-97bb-e4e7efa9cc1c
keywords:
- Type de mémoire tampon HLSL
topic_type:
- apiref
api_name:
- Buffer Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e36030f3dd31f1bdada238e89c1048e4971cd45c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031440"
---
# <a name="buffer-type"></a>Type de mémoire tampon

Pour déclarer une variable de mémoire tampon, utilisez la syntaxe ci-après.



| Buffer< >  *nom* du type ; |
|------------------------------|



 

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>**Mémoire tampon**
</dt> <dd>

Mot clé requis.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>*Entrer*
</dt> <dd>

L’un des types HLSL [scalaires](dx-graphics-hlsl-scalar.md), de [vecteur](dx-graphics-hlsl-vector.md)et de [matrice](dx-graphics-hlsl-matrix.md) . Vous pouvez déclarer une variable de mémoire tampon avec une matrice tant qu’elle s’adapte aux quantités de 4 32 bits. Vous pouvez donc écrire `Buffer<float2x2>` . Mais `Buffer<float4x4>` est trop grand et le compilateur génère une erreur.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nomme*
</dt> <dd>

Chaîne ASCII qui identifie de façon unique le nom de la variable.

</dd> </dl>

## <a name="example"></a>Exemple

Voici un exemple de déclaration de mémoire tampon du fichier PipesGS. fx dans l' [exemple PipesGS](https://msdn.microsoft.com/library/Ee416423(v=VS.85).aspx).


```
Buffer<float4> g_Buffer;
```



Les données sont lues à partir d’une mémoire tampon à l’aide d’une version surchargée de la fonction intrinsèque [**Load**](dx-graphics-hlsl-to-load.md) HLSL qui accepte un paramètre d’entrée (un index d’entiers). Une mémoire tampon est accessible comme un tableau d’éléments ; par conséquent, cet exemple lit le deuxième élément.


```
float4 bufferData = g_Buffer.Load( 1 );
```



Utilisez l' [étape flux-sortie](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-stream-stage) pour sortir des données dans une mémoire tampon.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Types de données (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 