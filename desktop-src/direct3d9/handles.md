---
description: Les handles offrent un moyen efficace pour faire référence aux techniques, aux passes, aux annotations et aux paramètres avec ID3DXEffectCompiler ou ID3DXEffect.
ms.assetid: 2494ecf9-88a7-43dc-a75b-ed743b11993a
title: Handles (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9e0dbbcbbc38685cae7c89b334bfb5458bc8386
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521428"
---
# <a name="handles-direct3d-9"></a>Handles (Direct3D 9)

Les handles offrent un moyen efficace pour faire référence aux techniques, aux passes, aux annotations et aux paramètres avec [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) ou [**ID3DXEffect**](id3dxeffect.md). Elles sont générées dynamiquement lorsque vous appelez des fonctions de la technique de la fonction d’annotation de paramètre d’extraction de formulaire \[ \| \| \| \| Pass \] \[ byname \| BySemantic \| \] .

Lors de l’exécution d’un programme, la génération répétée d’un handle vers le même objet retourne à nouveau le même handle à chaque fois. Mais ne vous fiez pas à la poignée qui reste constante lorsque vous exécutez votre programme plusieurs fois. Sachez également que les descripteurs générés par différentes instances de [**ID3DXEffect**](id3dxeffect.md) et [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) seront différents.

Si vous affichez les fichiers d’en-tête, vous remarquerez que les handles (D3DXHANDLEs) sont techniquement des pointeurs de chaîne.

Les descripteurs que vous transmettez dans des fonctions telles que GetParameter \[ byname \| Element \| BySemantic \] ou GetAnnotation \[ byname \] peuvent se présenter sous trois formes comme suit :

1.  Handles retournés par des fonctions telles que GetParameter \[ byname \| Element \| BySemantic \] .
2.  Chaînes telles que NomVariable, MyTechniqueName ou MyArray \[ 0 \] .
3.  Handle = **null**. Il y a quatre cas.
    -   S’il s’agit d’une valeur de retour de méthode, la méthode n’a pas pu trouver le descripteur.
    -   Si un descripteur **null** est transmis comme premier paramètre de l' \[ élément GetParameter byname \| \| BySemantic \] , la fonction retourne un paramètre de niveau supérieur. À l’inverse, si le handle n’est pas **null**, la fonction retourne un membre de structure ou un élément identifié par le handle.
    -   Si un handle **null** est passé comme premier argument de ValidateTechnique ou le deuxième argument de IsParameterUsed, la technique actuelle est validée.
    -   Si un handle **null** est passé comme premier argument de FindNextValidTechnique, la recherche d’une technique valide commence à la première technique dans l’effet.

Conseil sur les performances au début de votre application, effectuez une étape d’initialisation pour générer des handles à partir des chaînes. À partir de là, utilisez uniquement des handles. Le passage de chaînes au lieu de handles générés est plus lent.

## <a name="examples"></a>Exemples

Voici quelques exemples qui illustrent l’utilisation de la technique de la \[ \| \| fonction \| d’annotation de paramètre \| Pass \] \[ byname \| BySemantic \| \] pour générer des handles.


```
// Gets handle of second top-level parameter handle in the effect file
h1 = GetParameter(NULL, 1);    

// Gets handle of the third struct member of MyStruct
h2 = GetParameter("MyStruct", 2); 

// Gets handle of the third array element handle of MyArray
h3 = GetParameterElement("MyArray", 2); 

// Gets handle of first member of h1 (that is, the second top-level param)
h4 = GetParameter(h1, 0);    

// Gets handle of MyStruct.Data
h5 = GetParameterByName("MyStruct", "Data");    
// or 
h6 = GetParameterByName(NULL, "MyStruct.Data");    

// Gets handle of MyStruct.Data.SubData
h7 = GetParameterByName("MyStruct.Data", "SubData"); 
// or 
h8 = GetParameterByName(NULL, "MyStruct.Data.SubData");

// Gets handle of fifth annotation of h1 (that is, second top-level param)
h9 = GetAnnotation(h1, 4);    

// Gets handle of MyStruct's annotation, called Author
h10 = GetAnnotationByName("MyStruct", "Author");  
// or
h11 = GetParameterByName(NULL, "MyStruct@Author"); 
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Format d’effet](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



