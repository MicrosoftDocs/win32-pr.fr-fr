---
title: Liaison de nuanceurs d’effet
description: Direct2D utilise une optimisation appelée liaison de nuanceur d’effet qui combine plusieurs passes de rendu de graphique d’effet dans une seule passe.
ms.assetid: 431A5B39-6C84-442D-AC66-0F341E10DF2C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75b6bad2170f2b897a5cf8ac3086a74945efa8bf
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549234"
---
# <a name="effect-shader-linking"></a>Liaison de nuanceurs d’effet

Direct2D utilise une optimisation appelée liaison de nuanceur d’effet qui combine plusieurs passes de rendu de graphique d’effet dans une seule passe.

-   [Vue d’ensemble de la liaison d’effet du nuanceur](#overview-of-effect-shader-linking)
-   [Utilisation de la liaison de nuanceur d’effet](#using-effect-shader-linking)
-   [Création d’un effet personnalisé compatible avec la liaison de nuanceur](#authoring-a-shader-linking-compatible-custom-effect)
-   [Exemple de nuanceur d’effets compatibles avec la liaison](#example-linking-compatible-effect-shader)
-   [Compilation d’un nuanceur compatible avec les liaisons](#compiling-a-linking-compatible-shader)
    -   [Étape 1 : compiler la fonction d’exportation](#step-1-compile-the-export-function)
    -   [Étape 2 : compiler le nuanceur complet et incorporer la fonction d’exportation](#step-2-compile-the-full-shader-and-embed-the-export-function)
-   [Exporter les spécifications de fonction](#export-function-specifications)
-   [Rubriques connexes](#related-topics)

## <a name="overview-of-effect-shader-linking"></a>Vue d’ensemble de la liaison d’effet du nuanceur

L’effet nuanceur de liaison des optimisations s’appuie sur la liaison de nuanceur HLSL, une fonctionnalité Direct3D 11,2 qui permet de générer des nuanceurs de pixels et de vertex au moment de l’exécution en liant des fonctions de nuanceur précompilées. Les figures suivantes illustrent le concept de liaison de nuanceur d’effet dans un graphique d’effet. La première figure montre un graphique d’effet Direct2D classique avec quatre transformations de rendu. Sans liaison de nuanceur, chaque transformation consomme une passe de rendu et requiert une surface intermédiaire. au total, ce graphique nécessite 4 passes et 3 intermédiaires.

![graphique de transformation sans liaison de nuanceur : 4 passes et 3 intermédiaires.](images/shader-transform-graph.png)

La deuxième figure présente le même graphique d’effet où chaque transformation de rendu a été remplacée par une version de fonction qui peut être liée. Direct2D est en mesure de lier l’intégralité du graphique et de l’exécuter en une seule passe sans aucun intermédiaire. Cela peut augmenter considérablement la durée d’exécution du GPU et réduire la consommation de mémoire du GPU.

![graphique de transformation avec liaison de nuanceur : 1 passe, 0 intermédiaire.](images/shader-linking-graph.png)



 

La liaison d’effet du nuanceur opère sur des transformations individuelles dans un effet ; Cela signifie que même un graphique avec un seul effet peut bénéficier d’une liaison de nuanceur si cet effet a plusieurs transformations valides.

## <a name="using-effect-shader-linking"></a>Utilisation de la liaison de nuanceur d’effet

Si vous créez une application Direct2D qui utilise des effets, vous n’avez rien à faire pour tirer parti de la liaison d’effet du nuanceur. Direct2D analyse automatiquement le graphique d’effet pour déterminer la méthode la plus optimale pour lier chaque transformation.

Les auteurs des effets sont responsables de l’implémentation de leur effet de manière à prendre en charge la liaison de nuanceur d’effets ; Pour plus d’informations, consultez la section [création d’un effet personnalisé compatible avec les liaisons de nuanceur-](#authoring-a-shader-linking-compatible-custom-effect) ci-dessous. Tous les effets intégrés prennent en charge la liaison de nuanceur.

Direct2D liera uniquement les transformations de rendu adjacentes dans les situations où il est bénéfique. Il prend en compte plusieurs facteurs pour déterminer s’il faut lier deux transformations. Par exemple, la liaison de nuanceur n’est pas effectuée si l’une des transformations utilise des nuanceurs de vertex ou de calcul, car seuls les nuanceurs de pixels peuvent être liés. En outre, si un effet n’a pas été créé pour être compatible avec la liaison de nuanceur, les transformations environnantes ne sont pas liées.

Dans le cas où un tel risque de liaison existe, Direct2D ne lie pas les transformations adjacentes au risque, mais tente toujours de lier le reste du graphique.

![transformer le graphique avec un risque de liaison : 2 passes, 1 intermédiaire.](images/shader-linking-graph-hazard.png)

## <a name="authoring-a-shader-linking-compatible-custom-effect"></a>Création d’un effet personnalisé compatible avec la liaison de nuanceur

Si vous créez votre propre effet Direct2D personnalisé, vous devez vous assurer que ses transformations prennent en charge la liaison de nuanceur Effects. Cela nécessite des modifications mineures par rapport à la façon dont les effets personnalisés précédents ont été implémentés. Si une transformation dans votre effet personnalisé ne prend pas en charge la liaison de nuanceur, Direct2D ne la lie pas à des transformations adjacentes dans le graphique d’effet.

En tant qu’auteur d’effet personnalisé, vous devez être conscient de plusieurs concepts et exigences clés :

-   **Aucune modification n’est apportée aux implémentations d’interface**

    Vous n’avez pas besoin de modifier le code qui implémente les différentes interfaces Effects, telles que [ID2D1DrawTransform](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform).

-   **Fournir une version de fonction d’exportation et complète des nuanceurs**

    Vous devez fournir une version de fonction d’exportation des nuanceurs de vos effets qui peuvent être liés par Direct2D. En outre, vous devez également continuer à fournir le nuanceur complet original ; en effet, Direct2D sélectionne au moment de l’exécution la version de nuanceur appropriée, selon que la liaison de nuanceur doit être appliquée à un lien particulier dans le graphique.

    Si une transformation fournit uniquement l’objet blob de nuanceur de pixels complet (via [ID2D1EffectContext :: LoadPixelShader](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadpixelshader)), elle ne sera pas liée à des transformations adjacentes.

- **Fonctions d’assistance**

    Direct2D fournit des fonctions et des macros [d’assistance HLSL](hlsl-helpers.md) qui génèrent automatiquement les versions complète et d’exportation des fonctions d’un nuanceur. Ces applications auxiliaires se trouvent dans d2d1effecthelpers. hlsli. En outre, le compilateur HLSL (FXC) vous permet d’insérer le nuanceur de fonction d’exportation dans un champ privé dans le nuanceur complet. De cette façon, il vous suffit de créer un nuanceur une seule fois et de transmettre les deux versions à Direct2D simultanément. D2d1effecthelpers. hlsli et le compilateur FXC sont inclus dans le cadre du SDK Windows.

    Fonctions d’assistance :

  - [D2DGetInput](d2dgetinput.md)  
  - [D2DSampleInput](d2dsampleinput.md)  
  - [D2DSampleInputAtOffset](d2dsampleinputatoffset.md)  
  - [D2DSampleInputAtPosition](d2dsampleinputatposition.md)  
  - [D2DGetInputCoordinate](d2dgetinputcoordinate.md)  
  - [D2DGetScenePosition](d2dgetsceneposition.md)  
  - [Entrée de la \_ PS D2D \_](d2d-ps-entry.md)  

  Vous pouvez également créer manuellement deux versions de chaque nuanceur et les compiler à deux reprises, à condition que les spécifications décrites ci-dessous dans les [spécifications de fonction d’exportation](#export-function-specifications) soient respectées.

-   **Nuanceurs de pixels uniquement**

    Direct2D ne prend pas en charge la liaison des nuanceurs de calcul ou de vertex. Toutefois, si votre effet utilise à la fois un nuanceur de sommets et de pixels, la sortie du nuanceur de pixels peut toujours être liée.

-   **Échantillonnage simple et complexe**

    La liaison de fonction de nuanceur fonctionne en connectant la sortie d’un nuanceur de pixels à l’entrée d’une passe de nuanceur de pixels suivante. Cela est possible uniquement lorsque le nuanceur de pixels consommatrice requiert une seule valeur d’entrée pour effectuer son calcul. Cette valeur provient normalement de l’échantillonnage d’une texture d’entrée au niveau des coordonnées de texture émises par le nuanceur de sommets. Un tel nuanceur de pixels est dit d’effectuer un échantillonnage simple.

    ![la conversion en nuances de gris est un exemple d’échantillonnage simple. la valeur d’un pixel de sortie particulier dépend uniquement de la valeur du pixel d’entrée correspondant.](images/simple-sampling.png)

    Certains nuanceurs de pixels, tels qu’un flou gaussien, calculent leur sortie à partir de plusieurs exemples d’entrée plutôt qu’un seul échantillon. Un tel nuanceur de pixels est dit d’effectuer un échantillonnage complexe.

    

    ![le flou gaussien est un exemple d’échantillonnage complexe. la valeur du pixel de sortie Center dépend de plusieurs pixels d’entrée.](images/complex-sampling.png)

    
    Seules les fonctions de nuanceur avec des entrées simples peuvent avoir leur entrée fournie par une autre fonction de nuanceur. Les fonctions de nuanceur avec des entrées complexes doivent être fournies avec une texture d’entrée pour échantillonner. Cela signifie que Direct2D ne lie pas un nuanceur avec des entrées complexes à son prédécesseur.

    Lorsque vous utilisez les [applications auxiliaires HLSL de Direct2D](hlsl-helpers.md), vous devez indiquer dans le langage HLSL si un nuanceur utilise des entrées complexes ou simples.

## <a name="example-linking-compatible-effect-shader"></a>Exemple de nuanceur d’effets compatibles avec la liaison

À l’aide des applications d’assistance D2D, l’extrait de code suivant représente un nuanceur d’effets compatible avec la liaison simple :

```syntax
#define D2D_INPUT_COUNT 1
#define D2D_INPUT0_SIMPLE
#include “d2d1effecthelpers.hlsli”

D2D_PS_ENTRY(LinkingCompatiblePixelShader)
{
    float4 input = D2DGetInput(0);
    input.rgb *= input.a;
    return input;
}          
```

Dans cet exemple bref, Notez qu’aucun paramètre de fonction n’est déclaré, que le nombre d’entrées et le type de chaque entrée sont déclarés avant la fonction d’entrée, que l’entrée est récupérée en appelant [D2DGetInput](d2dgetinput.md), et que les directives de préprocesseur doivent être définies avant l’inclusion du fichier d’assistance.

Un nuanceur compatible avec la liaison doit fournir un nuanceur de pixels à passage unique standard et une fonction d’exportation de nuanceur. La macro d' [ \_ \_ entrée de la PS D2D](d2d-ps-entry.md) permet de générer chacune d’elles à partir du même code, quand elles sont utilisées conjointement avec le script de compilation du nuanceur.

Lors de la compilation d’un nuanceur complet, les macros sont développées dans le code suivant, qui a une signature d’entrée compatible avec les effets D2D.

```syntax
Texture2D<float4> InputTexture0;
SamplerState InputSampler0;

float4 LinkingCompatiblePixelShader(
    float4 pos   : SV_POSITION,
    float4 posScene : SCENE_POSITION,
    float4 uv0  : TEXCOORD0
    ) : SV_Target
    {
        float4 input = InputTexture0.Sample(InputSampler0, uv0.xy);
        input.rgb *= input.a;
        return input;
    }    
```

Lors de la compilation d’une version de fonction d’exportation du même code, le code suivant est généré :

```syntax
// Shader function version
export float4 LinkingCompatiblePixelShader_Function(
    float4 input0 : INPUT0)
    {
        input.rgb *= input.a;
        return input;
    }      
```

Notez que l’entrée de texture, normalement récupérée par l’échantillonnage d’un Texture2D, a été remplacée par une entrée de fonction (input0).

Pour obtenir une description détaillée de ce que vous devez faire pour écrire un effet compatible avec la liaison, consultez le didacticiel sur les [effets personnalisés](custom-effects.md) et l' [exemple effets d’images personnalisées Direct2D](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).

## <a name="compiling-a-linking-compatible-shader"></a>Compilation d’un nuanceur compatible avec les liaisons

Pour pouvoir être lié, l’objet blob de nuanceur de pixels passé à D2D doit contenir à la fois les versions complète et d’exportation de la fonction du nuanceur. Pour ce faire, incorporez la fonction d’exportation compilée dans la zone de données privées de l' \_ objet BLOB D3D \_ \_ .

Lorsque les nuanceurs sont créés avec les fonctions d’assistance D2D, une cible de compilation D2D doit être définie au moment de la compilation. Les types de cibles de compilation sont le \_ \_ nuanceur complet D2D et la \_ fonction D2D.

La compilation d’un nuanceur d’effets compatible avec la liaison est un processus en deux étapes :

-   [Compiler la fonction d’exportation](#step-1-compile-the-export-function)
-   [Compiler le nuanceur complet et incorporer la fonction d’exportation](#step-2-compile-the-full-shader-and-embed-the-export-function)

> [!Note]  
> Lors de la compilation d’un effet à l’aide de Visual Studio, vous devez créer un fichier de commandes qui exécute les deux commandes FXC et exécuter ce fichier de commandes en tant qu’étape de génération personnalisée qui s’exécute avant l’étape de compilation.

 

### <a name="step-1-compile-the-export-function"></a>Étape 1 : compiler la fonction d’exportation

```syntax
fxc /T <shadermodel> <MyShaderFile>.hlsl /D D2D_FUNCTION /D D2D_ENTRY=<entry> /Fl <MyShaderFile>.fxlib           
```

Pour compiler la version de la fonction d’exportation de votre nuanceur, vous devez passer les indicateurs suivants à FXC.



|    Indicateur                            |    Description                       |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Commutateur <ShaderModel>         | Définissez <ShaderModel> sur le profil de nuanceur de pixels approprié, tel que défini dans la [syntaxe fxc](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax). Il doit s’agir de l’un des profils listés sous « liaison de nuanceur HLSL ». |
| <MyShaderFile>.hlsl      | Définissez <MyShaderFile> sur le nom du fichier HLSL.                                                                                                                                                                                                    |
| /D, \_ fonction D2D               | Cette définition indique à FXC de compiler la version de la fonction d’exportation du nuanceur.                                                                                                                                                                       |
| /D ( \_ entrée D2D) =<entry>    | Définissez <entry> sur le nom du point d’entrée HLSL que vous avez défini dans la macro d' [ \_ \_ entrée](d2d-ps-entry.md) de l’extension de bloc D2D.                                                                                                                                    |
| /FL <MyShaderFile> . fxlib | Affectez <MyShaderfile> la valeur à l’emplacement où vous souhaitez stocker la version de la fonction d’exportation du nuanceur. Notez que l’extension. fxlib est uniquement destinée à faciliter l’identification.                                                                                              |

### <a name="step-2-compile-the-full-shader-and-embed-the-export-function"></a>Étape 2 : compiler le nuanceur complet et incorporer la fonction d’exportation

```syntax
fxc /T ps_<shadermodel> <MyShaderFile>.hlsl /D D2D_FULL_SHADER /D D2D_ENTRY=<entry> /E <entry> /setprivate <MyShaderFile>.fxlib /Fo <MyShader>.cso /Fh <MyShader>.h           
```

Pour compiler la version complète de votre nuanceur avec une version d’exportation incorporée, vous devez passer les indicateurs suivants à FXC.



|    Indicateur                                    |    Description                     |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Commutateur <ShaderModel>                 | Définissez <ShaderModel> sur le profil de nuanceur de pixels approprié, tel que défini dans la [syntaxe fxc](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax). Il doit s’agir du profil de nuanceur de pixels correspondant au profil de liaison spécifié à l’étape 1. |
| <MyShaderFile>.hlsl              | Définissez <MyShaderFile> sur le nom du fichier HLSL.                                                                                                                                                                                                                               |
| /D D2D \_ - \_ nuanceur complet                   | Cette définition indique à FXC de compiler la version complète du nuanceur.                                                                                                                                                                                                             |
| /D ( \_ entrée D2D) =<entry>            | Définissez <entry> sur le nom du point d’entrée HLSL que vous avez défini à l’intérieur de la \_ \_ macro entrée () D2D.                                                                                                                                                                                 |
| /E <entry>                       | Définissez <entry> sur le nom du point d’entrée HLSL que vous avez défini à l’intérieur de la \_ \_ macro entrée () D2D.                                                                                                                                                                                 |
| /SetPrivate <MyShaderFile> . fxlib | Cet argument indique à FXC d’incorporer le nuanceur de fonction d’exportation généré à l’étape 1 dans la \_ zone de données privées de l’objet BLOB D3D \_ \_ .                                                                                                                                                          |
| /FO <MyShader> . CSO               | Affectez <MyShader> la valeur à l’emplacement où vous souhaitez stocker le nuanceur compilé final et combiné.                                                                                                                                                                                                 |
| /FH <MyShader> . h                 | Définissez <MyShader> sur l’emplacement où vous souhaitez stocker l’en-tête combiné final.                                                                                                                                                                                                          |

## <a name="export-function-specifications"></a>Exporter les spécifications de fonction

Il est possible, bien que cela ne soit pas recommandé, de créer un nuanceur d’effets compatible sans utiliser les applications d’assistance fournies par D2D. Vous devez veiller à ce que les signatures de l’entrée de la fonction de nuanceur et de l’exportation complète soient conformes aux spécifications D2D.

Les spécifications des nuanceurs complets sont identiques à celles des versions antérieures de Windows. Brièvement, les paramètres d’entrée de nuanceur de pixels doivent être \_ position de SV, position de scène \_ et une seule texcoord d’entrée par effet.

Pour la fonction d’exportation, la fonction doit retourner un float4 et ses entrées doivent être de l’un des types suivants :

-   Entrée simple

    ```syntax
    float4 d2d_inputN : INPUTN         
    ```

    Pour les entrées simples, D2D insère un exemple de fonction entre la texture d’entrée et la fonction de nuanceur, ou l’entrée est fournie par la sortie d’une autre fonction de nuanceur.

-   Entrée complexe

    ```syntax
    float4 d2d_uvN  : TEXCOORDN                
    ```

    Pour les entrées complexes, D2D passera uniquement une coordonnée de texture comme décrit dans la documentation de Windows 8.

-   Emplacement de sortie

    ```syntax
    float4 d2d_posScene : SCENE_POSITION                
    ```

    Une seule entrée de position de scène \_ peut être définie. Ce paramètre doit être inclus uniquement lorsque cela est nécessaire, car une seule fonction par nuanceur lié peut utiliser ce paramètre.

La sémantique doit être définie comme ci-dessus, car D2D inspectera la sémantique pour décider comment lier des fonctions ensemble. Si une entrée de fonction ne correspond pas à l’un des types ci-dessus, la fonction est rejetée pour la liaison de nuanceur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Applications auxiliaires HLSL](hlsl-helpers.md)
</dt> <dt>

[Interface ID3D11Linker](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)
</dt> <dt>

[Interface ID3D11FunctionLinkingGraph](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)
</dt> </dl>

 

 