---
description: Une fois qu’un effet a été créé, la première étape consiste à compiler le code pour vérifier les problèmes de syntaxe.
ms.assetid: b8d8a0b7-b520-44e4-8691-6eb46202c092
title: Compiler un effet (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab6183f2f71b07c482fa24efc4f9fed199216d75
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104200922"
---
# <a name="compile-an-effect-direct3d-10"></a>Compiler un effet (Direct3D 10)

Une fois qu’un effet a été créé, la première étape consiste à compiler le code pour vérifier les problèmes de syntaxe. Pour ce faire, appelez l’une des API de compilation (comme D3DX10CompileEffectFromFile, D3DX10CompileEffectFromResource, D3DX10CompileEffectFromMemory). Ces API appellent le compilateur Effect fxc.exe qui est le compilateur utilisé pour compiler le code HLSL. C’est pour cette raison que la syntaxe du code dans un effet ressemble beaucoup à du code HLSL (il existe quelques exceptions qui seront gérées ultérieurement). Au fait, le compilateur/HLSL Effects (fxc.exe) se trouve dans le kit de développement logiciel (SDK) dans le dossier Utilities afin que vous puissiez compiler vos nuanceurs (ou effets) hors connexion si vous le souhaitez. Consultez la documentation pour exécuter le compilateur à partir de la ligne de commande.

-   [Includes](#includes)
-   [Macros](#macros)
-   [Indicateurs de nuanceur HLSL](#hlsl-shader-flags)
-   [Indicateurs FX](#fx-flags)
-   [Vérification des erreurs](#checking-errors)
-   [Rubriques connexes](#related-topics)

Voici un exemple de compilation d’un fichier Effect (à partir de l’exemple BasicHLSL10).


```
WCHAR str[MAX_PATH];
DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );

hr = D3DX10CompileEffectFromFile( str, NULL, NULL, "fx_4_0", 
    D3D10_SHADER_ENABLE_STRICTNESS, 0, pd3dDevice, NULL, NULL, 
    &l_pBlob_Effect, &l_pBlob_Errors, NULL );
```



## <a name="includes"></a>Includes

Un paramètre est une interface include. Générez l’une d’entre elles si vous souhaitez inclure un comportement personnalisé lors de la lecture d’un fichier include. Ce comportement personnalisé est exécuté chaque fois qu’un effet (qui utilise le pointeur include) est créé ou qu’un effet (qui utilise le pointeur include) est compilé. Pour implémenter un comportement include personnalisé, dérivez une classe de l’interface include. Cela fournit vos méthodes de classe deux : Open et Close. Implémentez le comportement personnalisé dans les méthodes Open et Close.

## <a name="macros"></a>Macros

La compilation des effets peut également prendre un pointeur vers les macros définies ailleurs. Par exemple, supposons que vous deviez modifier l’effet dans BasicHLSL10 pour utiliser deux macros : zéro et un. Le code d’effet qui utilise les deux macros est présenté ici.


```
if( bAnimate )
    vAnimatedPos += float4(vNormal, zero) *  
        (sin(g_fTime+5.5)+0.5)*5;
        
    Output.Diffuse.a = one;         
```



Voici la déclaration pour les deux macros.


```
D3D_SHADER_MACRO Shader_Macros[3] = { "zero", "0", "one", "1.0f", NULL, NULL };
```



Les macros sont un tableau de macros terminé par un caractère NULL ; où chaque macro est définie avec un struct de [**\_ \_ macro de nuanceur D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) .

Enfin, modifiez l’appel de l’effet de compilation pour prendre un pointeur vers les macros.


```
D3DX10CreateEffectFromFile( str, Shader_Macros, NULL, 
    D3D10_SHADER_ENABLE_STRICTNESS, 0, pd3dDevice, NULL, NULL, 
    &g_pEffect10, NULL );
```



## <a name="hlsl-shader-flags"></a>Indicateurs de nuanceur HLSL

Les indicateurs de nuanceur spécifient des contraintes de nuanceur pour le compilateur HLSL. Ces indicateurs ont un impact sur le code généré par le compilateur du nuanceur, y compris :

-   Considérations relatives à la taille : optimisez le code.
-   Considérations relatives au débogage : ajout d’informations de débogage, prévention du contrôle de Flow.
-   Considérations matérielles : la cible de compilation et si un nuanceur peut ou non s’exécuter sur du matériel hérité.

En général, ces indicateurs peuvent être combinés de manière logique, en supposant que vous n’avez pas spécifié deux caractéristiques conflictuelles. Pour obtenir la liste des indicateurs [, consultez constantes d’effet (Direct3D 10)](d3d10-graphics-reference-effect-constants.md).

## <a name="fx-flags"></a>Indicateurs FX

Ces indicateurs sont utilisés lors de la création d’un effet pour définir le comportement de compilation ou le comportement d’un effet d’exécution. Pour obtenir la liste des indicateurs [, consultez constantes d’effet (Direct3D 10)](d3d10-graphics-reference-effect-constants.md).

## <a name="checking-errors"></a>Vérification des erreurs

Si, au cours de la compilation, une erreur se produit, l’API retourne une interface qui contient les erreurs retournées par le compilateur d’effet. Cette interface est appelée ID3D10Blob. Toutefois, il n’est pas directement lisible en retournant un pointeur vers la mémoire tampon qui contient les données (qui est une chaîne), vous pouvez voir toutes les erreurs de compilation.

Dans cet exemple, une erreur a été introduite dans l’effet BasicHLSL. FX en copiant deux fois la première déclaration de variable.


```
//-------------------------------------------------------------------
// Global variables
//-------------------------------------------------------------------
float4 g_MaterialAmbientColor;      // Material's ambient color

// Declare the same variable twice
float4 g_MaterialAmbientColor;      // Material's ambient color
```



Cette erreur a empêché le compilateur de retourner l’erreur suivante, comme illustré dans la capture d’écran suivante de la fenêtre Espion dans Microsoft Visual Studio.

![capture d’écran de la fenêtre Espion de Visual Studio](images/effect-compile-errors-2.jpg)

Étant donné que l’erreur est retournée dans un pointeur LPVOID, effectuez un cast de celle-ci en une chaîne de caractères dans la fenêtre Espion.

Voici le code utilisé pour retourner l’erreur de la compilation qui a échoué.


```
// Read the D3DX effect file
WCHAR str[MAX_PATH];
ID3D10Blob* l_pBlob_Effect = NULL;
ID3D10Blob* l_pBlob_Errors = NULL;
hr = DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );
hr = D3DX10CompileEffectFromFile( str, NULL, NULL, 
    D3D10_SHADER_ENABLE_STRICTNESS, 0, NULL, 
    &l_pBlob_Effect, &l_pBlob_Errors );

LPVOID l_pError = NULL;
if( l_pBlob_Errors )
{
    l_pError = l_pBlob_Errors->GetBufferPointer();
    // then cast to a char* to see it in the locals window
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Rendu d’un effet (Direct3D 10)](d3d10-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 



