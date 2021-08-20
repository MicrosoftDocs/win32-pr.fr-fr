---
title: HLSL (High-Level Shader Language)
description: Le langage HLSL est le langage de nuanceur de haut niveau de type C que vous utilisez avec les nuanceurs programmables dans DirectX.
ms.assetid: 09cdd8d6-0cf5-4f7e-b480-f748d2fa9ca9
ms.topic: article
ms.date: 01/11/2021
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.custom: contperf-fy21q3
ms.openlocfilehash: 9f518102b7b3305103ed85231a791c542418a04c
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812895"
---
# <a name="high-level-shader-language-hlsl"></a>HLSL (High-Level Shader Language)

Le langage HLSL est le langage de nuanceur de haut niveau de type C que vous utilisez avec les nuanceurs programmables dans DirectX.

Par exemple, vous pouvez utiliser le langage HLSL pour écrire un [nuanceur de sommets](../direct3d11/vertex-shader-stage.md)ou un [nuanceur de pixels](../direct3d11/pixel-shader-stage.md), et utiliser ces nuanceurs dans l’implémentation du convertisseur dans votre application [Direct3D](../direct3d12/directx-12-programming-guide.md) .

Vous pouvez aussi utiliser le langage HLSL pour écrire un nuanceur de calcul, par exemple pour implémenter une simulation physique. toutefois, si, par exemple, vous allez écrire votre propre opérateur de convolution (pour le traitement d’image) en langage HLSL dans un nuanceur de calcul, vous obtiendrez de meilleures performances dans ce scénario si vous utilisez [Direct Machine Learning (DirectML)](/windows/ai/directml/dml) .

Le langage HLSL a été créé (à partir de DirectX 9) pour configurer le [pipeline](../direct3d11/overviews-direct3d-11-graphics-pipeline.md)3D programmable. Vous pouvez programmer l’intégralité du pipeline avec des instructions HLSL.

## <a name="where-to-go-next"></a>Emplacement suivant

* [Guide de programmation pour le HLSL](./dx-graphics-hlsl-pguide.md)
* [Référence pour le langage HLSL](./dx-graphics-hlsl-reference.md)

### <a name="programming-guide-for-hlsl"></a>Guide de programmation pour le HLSL

Pour une présentation conceptuelle du langage HLSL, consultez le [Guide de programmation pour le langage HLSL](./dx-graphics-hlsl-pguide.md).

Le Guide de programmation aborde les différents types de phases de nuanceur et explique comment créer, compiler, optimiser, lier et lier des nuanceurs.

Vous y trouverez également des présentations et des notes de publication sur, les générations successives de la version du modèle de nuanceur qui ont été publiées, en remontant en ce qui concerne le nuancier HLSL Model 5.

### <a name="reference-for-hlsl"></a>Référence pour le langage HLSL

Pour obtenir de la documentation de référence sur HLSL, consultez la [référence pour HLSL](./dx-graphics-hlsl-reference.md).

La section de référence contient une liste complète de la syntaxe du langage et des fonctions intrinsèques qui sont intégrées en HLSL afin de simplifier vos exigences de codage.

Vous y trouverez également une discussion sur les modèles de nuanceur et les profils, et le contenu de référence du modèle de nuanceur en retour en tant que nuanceur HLSL modèle 1. Il y a également du contenu qui couvre des instructions d’assembly, l’outil D3DCompiler et des informations sur les erreurs et avertissements qu’un nuanceur peut retourner.