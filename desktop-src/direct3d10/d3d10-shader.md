---
description: Options de compilation HLSL.
ms.assetid: vs|directx_sdk|~\d3d10_shader.htm
title: Constantes D3D10_SHADER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e965c050d3643e80b493875b27ba5a9b774b351487e191584f40297819758f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118303522"
---
# <a name="d3d10_shader-constants"></a>\_Constantes de nuanceur D3D10

Options de compilation HLSL.



| \#définition                                        | Description                                                                                                                                                                                                                                    |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3D10 \_ Shader \_ - \_ éviter \_ le contrôle de Flow             | Indiquez au compilateur de ne pas autoriser le contrôle de Flow (si possible).                                                                                                                                                                                       |
| Débogage du \_ nuanceur D3D10 \_                            | Insérez les informations de fichier de débogage/ligne/type/symbole.                                                                                                                                                                                                |
| D3D10 \_ Shader \_ Enable \_ strict               | Par défaut, le compilateur HLSL désactive la rigueur sur la syntaxe déconseillée. La spécification de cet indicateur permet une rigueur qui n’autorise pas la syntaxe héritée.                                                                                         |
| Le \_ nuanceur D3D10 \_ active la \_ compatibilité descendante \_ | Cela permet aux nuanceurs antérieurs de compiler sur 4 \_ cibles.                                                                                                                                                                                         |
| \_Application de nuanceur de D3D10 \_ \_ vs \_ logiciel \_ non \_ opt     | Compilez un nuanceur de sommets pour le profil de nuanceur le plus élevé suivant. Cette option active le débogage (et les optimisations désactivées).                                                                                                                           |
| D3D10 \_ Shader \_ force \_ PS \_ logiciel \_ non \_ opt     | Compilez un nuanceur de pixels pour le profil de nuanceur le plus élevé suivant. Cette option active le débogage (et les optimisations désactivées).                                                                                                                            |
| Respect de la \_ \_ norme IEEE du NUANCEur D3D10 \_                 | Active la strictité IEEE.                                                                                                                                                                                                                       |
| \_Nuanceur D3D10 \_ sans \_ prénuanceur                    | Désactive les prénuanceurs. L’utilisation de cet indicateur force le compilateur à ne pas extraire l’expression statique pour l’évaluation.                                                                                                                                 |
| D3D10 \_ du \_ niveau0 d’optimisation de nuanceur \_             | Niveau d’optimisation le plus bas. Peut générer du code plus lentement, mais le fera plus rapidement. Cela peut être utile dans un cycle de développement de nuanceur hautement itératif.                                                                                             |
| \_Optimisation du nuanceur D3D10 \_ \_ niveau1             | Deuxième niveau d’optimisation le plus bas.                                                                                                                                                                                                              |
| D3D10 \_ - \_ d’isolement2 d’optimisation de nuanceur \_             | Deuxième niveau d’optimisation le plus élevé.                                                                                                                                                                                                             |
| D3D10 \_ du \_ niveau3 d’optimisation de nuanceur \_             | Niveau d’optimisation le plus élevé. Produit le meilleur code possible, mais peut prendre beaucoup plus de temps. Cela sera utile pour les versions finales d’une application où les performances sont le facteur le plus important.                                 |
| D3D10 de \_ matrice de nuanceur de nuanceur \_ \_ \_ \_ principal         | Sauf spécification explicite, les matrices sont compressées dans l’ordre ligne-principal de l’entrée et de la sortie du nuanceur.                                                                                                                                   |
| \_ \_ \_ \_ Colonne principale de matrice de nuanceur D3D10 \_      | Sauf spécification explicite, les matrices sont compressées dans l’ordre colonne-principal de l’entrée et de la sortie du nuanceur. Cette opération est généralement plus efficace, car elle permet d’effectuer une multiplication de matrice vectorielle à l’aide d’une série de produits de point. |
| \_Précision partielle du nuanceur D3D10 \_ \_               | Forcer tous les calculs à être effectués avec une précision partielle ; Cela peut s’exécuter plus rapidement sur un matériel.                                                                                                                                                |
| \_Le nuanceur D3D10 \_ préfère \_ \_ le contrôle de Flow            | Indiquez au compilateur d’utiliser Flow-Control (si possible).                                                                                                                                                                                             |
| Optimisation de l' \_ ignorance du nuanceur D3D10 \_ \_               | Ignorer l’optimisation pendant la génération de code ; généralement recommandé pour le débogage uniquement.                                                                                                                                                                |
| \_Ignorer la \_ \_ validation du nuanceur D3D10                 | Ne validez pas le code généré par rapport aux capacités et contraintes connues. Utilisez-le uniquement avec les nuanceurs qui ont été correctement compilés par le passé. Les nuanceurs sont toujours validés par DirectX avant d’être définis sur l’appareil.         |
| \_Les avertissements du nuanceur D3D10 \_ \_ sont des \_ Erreurs            | Informez le compilateur HLSL de traiter tous les avertissements comme des erreurs lors de la compilation du code du nuanceur. Pour le nouveau code de nuanceur, vous devez utiliser cette option afin de pouvoir résoudre tous les avertissements et garantir le moins possible de problèmes difficiles à trouver dans le code.             |



 

Ces constantes sont définies en tant que macros dans d3d10shader. h.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Constantes de nuanceur](d3d10-graphics-reference-d3d10-shader-constants.md)
</dt> </dl>

 

 



