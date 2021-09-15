---
title: Utilisation de nuanceurs dans Direct3D 9
description: Utilisation de nuanceurs dans Direct3D 9
ms.assetid: 8d8f5124-fbf3-4af5-8399-43ba28aa6eb9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6455b47d24c1c83683ce8b85c48990bb32e221ae
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127524613"
---
# <a name="using-shaders-in-direct3d-9"></a>Utilisation de nuanceurs dans Direct3D 9

-   [Compilation d’un nuanceur pour un matériel spécifique](#compiling-a-shader-for-specific-hardware)
-   [Initialisation des constantes de nuanceur](#initializing-shader-constants)
-   [Liaison d’un paramètre Shader à un registre particulier](#binding-a-shader-parameter-to-a-particular-register)
-   [Rendu d’un nuanceur programmable](#rendering-a-programmable-shader)
-   [Débogage des nuanceurs](#debugging-shaders)
-   [Rubriques connexes](#related-topics)

## <a name="compiling-a-shader-for-specific-hardware"></a>Compilation d’un nuanceur pour un matériel spécifique

Des nuanceurs ont été ajoutés pour la première fois à Microsoft DirectX dans DirectX 8,0. À ce moment-là, plusieurs machines-nuanceurs virtuels ont été définies, chacune correspondant approximativement à un processeur graphique particulier produit par les principaux fournisseurs de graphiques 3D. Pour chacun de ces ordinateurs de nuanceur virtuel, un langage assembleur a été conçu. Les programmes écrits dans les modèles de nuanceur (noms vs \_ 1 1 \_ et PS 1 \_ \_ 1-PS \_ 1 \_ 4) étaient relativement courts et étaient généralement écrits par les développeurs directement dans le langage d’assembly approprié. L’application transmet ce code de langage assembleur lisible à la bibliothèque D3DX à l’aide de [**D3DXAssembleShader**](/windows/desktop/direct3d9/d3dxassembleshader) et récupère une représentation binaire du nuanceur qui, à son tour, est passée à l’aide de [**CreateVertexShader**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createvertexshader) ou [**CreatePixelShader**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createpixelshader). Pour plus d’informations, consultez le kit de développement logiciel (SDK).

La situation dans Direct3D 9 est similaire. Une application passe un nuanceur HLSL à D3DX à l’aide de [**D3DXCompileShader**](/windows/desktop/direct3d9/d3dxcompileshader) et récupère une représentation binaire du nuanceur compilé qui, à son tour, est transmise à Microsoft Direct3D à l’aide de [**CreatePixelShader**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createpixelshader) ou [**CreateVertexShader**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createvertexshader). Le runtime ne connaît rien du langage HLSL, mais uniquement les modèles de nuanceur d’assemblys binaires. C’est agréable, car cela signifie que le compilateur HLSL peut être mis à jour indépendamment du runtime Direct3D. Vous pouvez également compiler les nuanceurs hors connexion à l’aide de [fxc](/windows/desktop/direct3dtools/fxc).

En plus du développement du compilateur HLSL, Direct3D 9 introduit également les modèles de nuanceur au niveau de l’assembly pour exposer les fonctionnalités de la dernière génération de matériel graphique. Les développeurs d’applications peuvent travailler en assembly pour ces nouveaux modèles (vs \_ 2 \_ 0, vs \_ 3 \_ 0, PS \_ 2 \_ 0, PS \_ 3 \_ 0), mais nous pensons que la plupart des développeurs se déplaceront en HLSL pour le développement de nuanceur.

Bien entendu, la possibilité d’écrire un programme HLSL pour exprimer un algorithme d’ombrage particulier ne lui permet pas de s’exécuter automatiquement sur un matériel donné. Une application appelle D3DX pour compiler un nuanceur dans du code assembleur binaire avec [**D3DXCompileShader**](/windows/desktop/direct3d9/d3dxcompileshader). L’une des limitations de ce point d’entrée est un paramètre qui définit quels modèles au niveau de l’assembly (ou cibles de compilation) le compilateur HLSL doit utiliser pour exprimer le code du nuanceur final. Si une application exécute la compilation du nuanceur HLSL au moment de l’exécution (par opposition au temps de compilation ou hors connexion), l’application peut examiner les fonctionnalités du périphérique Direct3D et sélectionner la cible de compilation à faire correspondre. Si l’algorithme exprimé dans le nuanceur HLSL est trop complexe pour s’exécuter sur la cible de compilation sélectionnée, la compilation échoue. Cela signifie que bien que le langage HLSL soit un énorme avantage pour le développement de nuanceur, il ne libère pas les développeurs des réalités de l’expédition de jeux à un public cible avec des appareils graphiques de fonctionnalités variables. En tant que développeur de jeux, vous devez toujours gérer une approche à plusieurs niveaux pour vos visuels. Cela signifie l’écriture de meilleurs nuanceurs pour les cartes graphiques plus performantes et l’écriture d’autres versions de base pour les cartes plus anciennes. Toutefois, avec un langage HLSL bien écrit, cette charge peut être considérablement allégée.

Plutôt que de compiler des nuanceurs HLSL à l’aide de D3DX sur l’ordinateur du client au moment du chargement de l’application ou lors de la première utilisation, de nombreux développeurs choisissent de compiler leur nuanceur du langage HLSL en code assembleur binaire avant même d’être expédiés. Cela permet de conserver le code source HLSL à l’écart des regards indiscrets et de s’assurer que tous les nuanceurs de leur application s’exécuteront dans le processus interne d’assurance qualité. Un utilitaire pratique pour la compilation des nuanceurs hors connexion est [fxc](/windows/desktop/direct3dtools/fxc). Cet outil comporte un certain nombre d’options que vous pouvez utiliser pour compiler du code pour la cible de compilation spécifiée. L’étude de la sortie désassemblée peut être très utile lors du développement si vous souhaitez optimiser vos nuanceurs ou simplement connaître les fonctionnalités de l’ordinateur de nuanceur virtuel à un niveau plus détaillé. Ces options sont résumées ci-dessous :

## <a name="initializing-shader-constants"></a>Initialisation des constantes de nuanceur

Les constantes de nuanceur sont contenues dans la table constante. Vous pouvez y accéder à l’aide de l’interface [**ID3DXConstantTable**](/windows/desktop/direct3d9/id3dxconstanttable) . Les variables globales du nuanceur peuvent être initialisées dans le code du nuanceur. Celles-ci sont initialisées au moment de l’exécution en appelant [**SetDefaults**](/windows/desktop/direct3d9/id3dxconstanttable--setdefaults).

## <a name="binding-a-shader-parameter-to-a-particular-register"></a>Liaison d’un paramètre Shader à un registre particulier

Le compilateur assigne automatiquement les registres aux variables globales. Le compilateur assignerait l’environnement au registre de l’échantillonneur S0, SparkleNoise au registre de l’échantillonneur S1 et k \_ s au registre de constante C0 (en supposant qu’aucun autre échantillon ou registre constant n’a déjà été affecté) pour les trois variables globales suivantes :


```
sampler Environment;
sampler SparkleNoise;
float4 k_s;
```



Il est également possible de lier des variables à un registre spécifique. Pour forcer le compilateur à assigner à un registre particulier, utilisez la syntaxe suivante :


```
register(RegisterName)
```



où RegisterName est le nom du Registre spécifique. Les exemples suivants illustrent la syntaxe d’affectation de Registre spécifique, où l’environnement de l’échantillonneur sera lié au registre de l’échantillonneur S1, SparkleNoise sera lié au registre d’échantillonnage S0, et k \_ s sera lié à un registre de C12 constant :


```
sampler Environment : register(s1);
sampler SparkleNoise : register(s0);
float4 k_s : register(c12);
```



## <a name="rendering-a-programmable-shader"></a>Rendu d’un nuanceur programmable

Un nuanceur est rendu en définissant le nuanceur actuel dans l’appareil, en initialisant les constantes du nuanceur, en indiquant l’appareil sur lequel proviennent les données d’entrée variables et enfin en rendant les primitives. Chacun d’entre eux peut être obtenu en appelant les méthodes suivantes, respectivement :

-   [**SetVertexShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader)
-   [**SetVertexShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf)
-   [**SetStreamSource**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource)
-   [**DrawPrimitive**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-drawprimitive)

## <a name="debugging-shaders"></a>Débogage des nuanceurs

l’extension DirectX pour Microsoft Visual Studio .net fournit un débogueur HLSL entièrement intégré au sein de l’environnement de développement intégré (IDE) Visual Studio .net. pour préparer le débogage du nuanceur, vous devez installer les outils appropriés sur votre ordinateur (consultez [débogage des nuanceurs dans Visual Studio (Direct3D 9)](dx-graphics-hlsl-debug-visual-studio.md)).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de programmation pour HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 