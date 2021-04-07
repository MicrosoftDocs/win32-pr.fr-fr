---
title: Applications auxiliaires HLSL
description: Pour aider les auteurs d’effet à écrire des nuanceurs de pixels pouvant être liés, d2d1effecthelpers. hlsli définit un ensemble d’extensions de langage HLSL sous la forme de méthodes d’assistance et de macros.
ms.assetid: 5D0BB99E-7C77-4D45-82E6-F038E4B752A4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec8f43447c16d93ef9e1839ac319c761b975222a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939730"
---
# <a name="hlsl-helpers"></a>Applications auxiliaires HLSL

Pour aider les auteurs d’effet à écrire des nuanceurs de pixels pouvant être liés, d2d1effecthelpers. hlsli définit un ensemble d’extensions de langage HLSL sous la forme de méthodes d’assistance et de macros.

Pour ajouter d2d1effecthelpers. hlsli à votre projet, ajoutez une \# instruction include dans le fichier HLSL. d2d1effecthelpers. hlsli se trouve au même emplacement que les autres en-têtes Direct2D tels que d2d1. h ; elle peut être référencée à partir de la page de propriétés du fichier HLSL en ajoutant la macro $ (WindowsSDK \_ INCLUDEPATH) à la propriété autres répertoires Include. Notez que l' \# instruction include doit venir après toutes les directives de préprocesseur \_ . ce nombre d’entrées D2D \_ a été défini.

``` syntax
#include <d2d1effecthelpers.hlsli>
```

Direct2D ne prend pas en charge la liaison des nuanceurs de calcul ou de vertex. Toutefois, si votre effet utilise à la fois un nuanceur de sommets et un nuanceur de pixels, la sortie du nuanceur de pixels peut toujours être liée.

## <a name="preprocessor-directives"></a>Directives de préprocesseur

Des directives de préprocesseur sont requises pour communiquer des informations sur l’effet. Cela comprend le nombre d’entrées et le type d’échantillonnage de chaque entrée. Les valeurs suivantes doivent être définies dans le code du nuanceur d’effet au-dessus du point d’entrée du nuanceur approprié, le cas échéant.

-   `D2D_INPUT_COUNT <N>` : Déclare le nombre d’entrées de texture à l’effet. Si l’effet a un nombre variable d’entrées, cette valeur doit être étendue de manière appropriée à chaque point d’entrée du nuanceur. La définition de cette valeur est obligatoire.
-   `D2D_INPUT<N>_SIMPLE` : Déclare la nième entrée pour utiliser l’échantillonnage simple. S’il n’est pas défini, l’entrée nth est par défaut complexe. La définition de cette valeur est facultative.
-   `D2D_INPUT<N>_COMPLEX` : Déclare la nième entrée pour utiliser un échantillonnage complexe. S’il n’est pas défini, l’entrée nth est par défaut complexe. La définition de cette valeur est facultative.
-   `D2D_REQUIRES_SCENE_POSITION` : Indique que la fonction de nuanceur appelle les méthodes d’assistance qui utilisent la valeur de position de la scène (à savoir, la fonction d’assistance [D2DGetScenePosition](d2dgetsceneposition.md) ). Ce paramètre doit être inclus uniquement lorsque cela est nécessaire, car une seule fonction par nuanceur lié peut utiliser ce paramètre. La définition de cette valeur est facultative.
-   `D2D_CUSTOM_ENTRY` : Indique que la fonction de nuanceur de pixels consomme la sortie d’un nuanceur de sommets personnalisé, et déclare donc ses paramètres d’entrée. Toutes les entrées de nuanceur de vertex personnalisées utilisent un échantillonnage complexe et ne peuvent pas consommer la sortie d’une autre fonction de nuanceur (c’est-à-dire qu’elles ne sont qu’après liaison). La définition de cette valeur est facultative.

Par exemple :

``` syntax
#define D2D_INPUT_COUNT 3
#define D2D_INPUT0_SIMPLE
#define D2D_INPUT1_SIMPLE
#define D2D_INPUT2_COMPLEX
#include <d2d1effecthelpers.hlsli>
          
```

## <a name="helper-functions"></a>Fonctions d’assistance

Les fonctions d’assistance sont utilisées comme remplacement pour certaines fonctions intrinsèques HLSL natives. Au moment de la compilation, ces fonctions d’assistance sont redéfinies par Direct2D dans la version appropriée en fonction du type de cible de compilation (nuanceur complet ou fonction d’exportation).

Fonctions d’assistance :

<dl>

[D2DGetInput](d2dgetinput.md)  
[D2DSampleInput](d2dsampleinput.md)  
[D2DSampleInputAtOffset](d2dsampleinputatoffset.md)  
[D2DSampleInputAtPosition](d2dsampleinputatposition.md)  
[D2DGetInputCoordinate](d2dgetinputcoordinate.md)  
[D2DGetScenePosition](d2dgetsceneposition.md)  
[Entrée de la \_ PS D2D \_](d2d-ps-entry.md)  
</dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Liaison de nuanceurs d’effet](effect-shader-linking.md)
</dt> </dl>

 

 




