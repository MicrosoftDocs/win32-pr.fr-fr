---
title: Compiler un effet (Direct3D 11)
description: Une fois qu’un effet a été créé, l’étape suivante consiste à compiler le code pour vérifier les problèmes de syntaxe.
ms.assetid: 7624d55e-6466-4156-8f31-30f0d25a2883
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3df304a7b657af19984008bd90a1be4bfe5219c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941108"
---
# <a name="compile-an-effect-direct3d-11"></a>Compiler un effet (Direct3D 11)

Une fois qu’un effet a été créé, l’étape suivante consiste à compiler le code pour vérifier les problèmes de syntaxe.

Pour ce faire, appelez l’une des API de compilation ([**D3DX11CompileFromFile**](d3dx11compilefromfile.md), [**D3DX11CompileFromMemory**](d3dx11compilefrommemory.md)ou [**D3DX11CompileFromResource**](d3dx11compilefromresource.md) ). Ces API appellent le compilateur Effect fxc.exe, qui compile le code HLSL. C’est pour cette raison que la syntaxe du code dans un effet ressemble beaucoup à du code HLSL. (Il existe quelques exceptions qui seront gérées ultérieurement). Le compilateur Effect/compilateur HLSL, fxc.exe, est disponible dans le kit de développement logiciel (SDK) dans le dossier Utilities afin que les nuanceurs (ou effets) puissent être compilés hors connexion si vous le souhaitez. Consultez la documentation pour exécuter le compilateur à partir de la ligne de commande.

-   [Exemple](#example)
-   [Includes](#includes)
-   [Recherche de fichiers include](#searching-for-include-files)
-   [Macros](#macros)
-   [Indicateurs de nuanceur HLSL](#hlsl-shader-flags)
-   [Indicateurs FX](#fx-flags)
-   [Vérification des erreurs](#checking-errors)
-   [Rubriques connexes](#related-topics)

## <a name="example"></a>Exemple

Voici un exemple de compilation d’un fichier Effect.


```
WCHAR str[MAX_PATH];
DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );

hr = D3DX11CompileFromFile( str, NULL, NULL, pFunctionName, pProfile, D3D10_SHADER_ENABLE_STRICTNESS, NULL, NULL, &pBlob, &pErrorBlob, NULL );
```



## <a name="includes"></a>Includes

L’un des paramètres des API de compilation est une interface include. Générez l’une de ces si vous souhaitez inclure un comportement personnalisé lorsque le compilateur lit un fichier include. Le compilateur exécute ce comportement personnalisé chaque fois qu’il crée ou compile un effet (qui utilise le pointeur include). Pour implémenter un comportement include personnalisé, dérivez une classe de l’interface [**ID3DInclude**](/windows/desktop/api/D3Dcommon/nn-d3dcommon-id3dinclude) . Cela fournit à votre classe deux méthodes : [**Open**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) et [**Close**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-close). Implémentez le comportement personnalisé dans ces méthodes.

## <a name="searching-for-include-files"></a>Recherche de fichiers include

Le pointeur que le compilateur transmet dans le paramètre *pParentData* à la méthode [**Open**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) de votre gestionnaire include peut ne pas pointer vers le conteneur qui inclut le \# fichier include dont le compilateur a besoin pour compiler le code de votre nuanceur. Autrement dit, le compilateur peut passer **null** dans *pParentData*. Par conséquent, nous recommandons que votre gestionnaire d’inclusion recherche sa propre liste d’emplacements include pour le contenu. Votre gestionnaire include peut ajouter dynamiquement de nouveaux emplacements include lorsqu’il reçoit ces emplacements dans les appels à sa méthode **Open** .

Dans l’exemple suivant, supposons que les fichiers include du code du nuanceur sont tous deux stockés dans le répertoire *somewhereelse* . Lorsque le compilateur appelle la méthode [**Open**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) du gestionnaire include pour ouvrir et lire le contenu de *somewhereelse \\ foo. h*, le gestionnaire include peut enregistrer l’emplacement du répertoire **somewhereelse** . Plus tard, lorsque le compilateur appelle la méthode **Open** du gestionnaire include pour ouvrir et lire le contenu de *bar. h*, le gestionnaire include peut effectuer une recherche automatique dans le répertoire *somewhereelse* pour *bar. h*.


```
Main.hlsl:
#include "somewhereelse\foo.h"

Foo.h:
#include "bar.h"
```



## <a name="macros"></a>Macros

La compilation des effets peut également prendre un pointeur vers les macros définies ailleurs. Par exemple, supposons que vous souhaitiez modifier l’effet dans BasicHLSL10 pour utiliser deux macros : zéro et un. Le code d’effet qui utilise les deux macros est présenté ici.


```
if( bAnimate )
    vAnimatedPos += float4(vNormal, zero) *  
        (sin(g_fTime+5.5)+0.5)*5;
        
    Output.Diffuse.a = one;         
```



Voici la déclaration pour les deux macros.


```
D3D10_SHADER_MACRO Shader_Macros[3] = { "zero", "0", "one", "1.0f", NULL, NULL };
```



Les macros sont un tableau de macros se terminant par un caractère NULL ; où chaque macro est définie à l’aide d’un struct de [**\_ \_ macro de nuanceur D3D10**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) .

Modifiez l’appel de l’effet de compilation pour prendre un pointeur vers les macros.


```
D3DX11CompileFromFile( str, Shader_Macros, NULL, pFunctionName, 
                       pProfile, D3D10_SHADER_ENABLE_STRICTNESS, NULL, 
                       NULL, &pBlob, &pErrorBlob, NULL );    
```



## <a name="hlsl-shader-flags"></a>Indicateurs de nuanceur HLSL

Les indicateurs de nuanceur spécifient des contraintes de nuanceur pour le compilateur HLSL. Ces indicateurs affectent le code généré par le compilateur du nuanceur des manières suivantes :

-   Optimisez la taille du code.
-   Y compris les informations de débogage, qui empêchent le contrôle de Flow.
-   Affecte la cible de compilation et si un nuanceur peut s’exécuter sur du matériel hérité.

Ces indicateurs peuvent être combinés de manière logique si vous n’avez pas spécifié deux caractéristiques conflictuelles. Pour obtenir la liste des indicateurs, [consultez \_ constantes de nuanceur D3D10](/windows/desktop/direct3d10/d3d10-shader).

## <a name="fx-flags"></a>Indicateurs FX

Utilisez ces indicateurs quand vous créez un effet pour définir le comportement de la compilation ou le comportement de l’effet d’exécution. Pour obtenir la liste des indicateurs, [consultez \_ constantes Effect D3D10](/windows/desktop/direct3d10/d3d10-effect).

## <a name="checking-errors"></a>Vérification des erreurs

Si, au cours de la compilation, une erreur se produit, l’API retourne une interface qui contient les erreurs du compilateur d’effet. Cette interface est appelée [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)). Elle n’est pas directement lisible ; Toutefois, en retournant un pointeur vers la mémoire tampon qui contient les données (qui est une chaîne), vous pouvez voir toutes les erreurs de compilation.

Cet exemple contient une erreur dans BasicHLSL. FX, la première déclaration de variable se produit deux fois.


```
//-------------------------------------------------------------------
// Global variables
//-------------------------------------------------------------------
float4 g_MaterialAmbientColor;      // Material's ambient color

// Declare the same variable twice
float4 g_MaterialAmbientColor;      // Material's ambient color
```



Cette erreur force le compilateur à retourner l’erreur suivante, comme illustré dans la capture d’écran suivante du Fenêtre Espion dans Microsoft Visual Studio.

![capture d’écran de la fenêtre Espion de Visual Studio avec une erreur 0x01997fb8](images/effect-compile-errors-2.jpg)

Étant donné que le compilateur retourne l’erreur dans un pointeur LPVOID, effectuez un cast de celui-ci en une chaîne de caractères dans le Fenêtre Espion.

Voici le code qui retourne l’erreur de la compilation ayant échoué.


```
// Read the D3DX effect file
WCHAR str[MAX_PATH];
ID3DBlob*   l_pBlob_Effect = NULL;
ID3DBlob*   l_pBlob_Errors = NULL;
hr = DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );
hr = D3DX11CompileFromFile( str, NULL, NULL, pFunctionName, 
                       pProfile, D3D10_SHADER_ENABLE_STRICTNESS, NULL, 
                       NULL, &pBlob, &pErrorBlob, NULL );      

LPVOID l_pError = NULL;
if( pErrorBlob )
{
    l_pError = pErrorBlob->GetBufferPointer();
    // then cast to a char* to see it in the locals window
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Rendu d’un effet (Direct3D 11)](d3d11-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 