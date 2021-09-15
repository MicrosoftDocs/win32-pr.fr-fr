---
title: Référence pour le langage HLSL
description: La documentation de référence HLSL spécifie les caractéristiques du langage. Il est divisé en plusieurs sections.
ms.assetid: 1d0e12ff-8559-4e5c-9914-6ed313ea5464
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ce0bb59dd26bd8bb9723bcdff23bbc79ee810253
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127524688"
---
# <a name="reference-for-hlsl"></a>Référence pour le langage HLSL

La documentation de référence HLSL spécifie les caractéristiques du langage. Il est divisé en plusieurs sections.

-   [Syntaxe du langage (DirectX HLSL)](dx-graphics-hlsl-language-syntax.md) -les nuanceurs de programmation en HLSL requièrent que vous compreniez la syntaxe du langage, autrement dit, la façon dont vous écrivez le code HLSL. Cela comprend le code permettant de déclarer et d’initialiser des variables, d’écrire des fonctions de nuanceur définies par l’utilisateur et d’ajouter des instructions de contrôle de Flow pour rendre vos fonctions plus puissantes.
-   [Modèles de nuanceur et profils de nuanceur](dx-graphics-hlsl-models.md) -le compilateur HLSL implémente des règles et des restrictions basées sur les modèles de nuanceur. Le code de chaque nuanceur de sommets, nuanceur de géométrie (si vous utilisez Direct3D 10) et le nuanceur de pixels sont validés par rapport à un modèle de nuanceur, que vous fournissez au moment de la compilation.
-   [**Fonctions intrinsèques (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md) -HLSL possède de nombreuses fonctions intrinsèques. Celles-ci sont implémentées et testées afin que vous puissiez les utiliser, sachant qu’elles sont déjà déboguées et qu’elles fonctionnent correctement. Si vous choisissez d’écrire vos propres fonctions, consultez la section syntaxe de langage pour l’écriture de fonctions définies par l’utilisateur.
-   [Référence du nuanceur asm](dx9-graphics-reference-asm.md) : instructions d’assembly que vous pouvez utiliser pour programmer et déboguer des nuanceurs.
-   [Référence D3DCompiler](dx-graphics-d3dcompiler-reference.md) : compile la source HLSL brute.
-   [Référence de conversion de format Inline](inline-format-conversion-reference.md) : le \_ fichier D3DX DXGIFormatConvert. inl contient des fonctions de conversion de format Inline que vous pouvez utiliser dans le nuanceur de calcul ou le nuanceur de pixels sur du matériel Direct3D 11. Vous pouvez utiliser ces fonctions dans votre application pour lire et écrire simultanément dans une texture. Autrement dit, vous pouvez effectuer une modification d’image sur place. Pour utiliser ces fonctions de conversion de format Inline, incluez le \_ fichier D3DX DXGIFormatConvert. inl dans votre application.
-   [Annexe (DirectX HLSL)](dx-graphics-hlsl-appendix.md) -l’annexe est incluse à des fins d’exhaustivité. Il comprend une liste des mots clés et des mots réservés. ces mots ne peuvent pas être utilisés comme identificateurs dans vos programmes. Il comprend également une liste de la grammaire de la langue à des fins de référence.
-   [**Erreurs et avertissements HLSL**](hlsl-errors-and-warnings.md) -fournit des codes d’erreur et d’avertissement qu’un nuanceur peut retourner.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[HLSL](dx-graphics-hlsl.md)
</dt> <dt>

[Guide de programmation pour HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 




