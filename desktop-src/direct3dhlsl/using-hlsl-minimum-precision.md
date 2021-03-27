---
title: Utilisation de la précision minimale HLSL
description: À compter de Windows 8, les pilotes graphiques peuvent implémenter des types de données scalaires HLSL de précision minimale à l’aide d’une précision supérieure ou égale à la précision de bit spécifiée.
ms.assetid: 422B0C45-5CEB-4235-AD05-62D36C36CFC6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7f66f35aef3e870edb4e8564a280be89ce34be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728165"
---
# <a name="using-hlsl-minimum-precision"></a>Utilisation de la précision minimale HLSL

À compter de Windows 8, les pilotes graphiques peuvent implémenter des [types de données scalaires HLSL](dx-graphics-hlsl-scalar.md) de précision minimale à l’aide d’une précision supérieure ou égale à la précision de bit spécifiée. Lorsque votre code de nuanceur de précision minimale HLSL est utilisé sur le matériel qui implémente la précision minimale HLSL, vous utilisez moins de bande passante de mémoire et vous utilisez donc moins de puissance système.

Vous pouvez interroger la prise en charge de précision minimale que le pilote Graphics fournit en appelant [**ID3D11Device :: CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) avec la valeur de [**\_ \_ \_ \_ \_ prise en charge de l’outil nuanceur min précision de la fonctionnalité d3d11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature) . Pour plus d’informations, consultez [prise en charge de la précision minimale HLSL](/windows/desktop/direct3d11/direct3d-11-1-features).

-   [Déclarer des variables avec des types de données de précision minimale](#declare-variables-with-minimum-precision-data-types)
-   [Test de votre code de nuanceur de précision minimal](#testing-your-minimum-precision-shader-code)
-   [Rubriques connexes](#related-topics)

## <a name="declare-variables-with-minimum-precision-data-types"></a>Déclarer des variables avec des types de données de précision minimale

Pour utiliser la précision minimale dans le code du nuanceur HLSL, déclarez des variables individuelles avec des types tels que **min16float** (**min16float4** pour un vecteur), **min16int**, **min10float**, et ainsi de suite. Avec ces variables, votre code de nuanceur indique qu’il n’a pas besoin de plus de précision que ce que les variables indiquent. Mais le matériel peut ignorer les indicateurs de précision minimale et s’exécuter avec une précision de 32 bits. Lorsque votre code de nuanceur est utilisé sur du matériel qui tire parti de la précision minimale, vous utilisez moins de bande passante de mémoire et, par conséquent, vous utilisez moins de puissance système tant que votre code de nuanceur n’attend pas une précision supérieure à celle spécifiée.

Vous n’avez pas besoin de créer plusieurs nuanceurs qui n’utilisent pas la précision minimale. Au lieu de cela, créez des nuanceurs avec une précision minimale, et les variables de précision minimale se comportent à une précision de 32 bits complète si le pilote graphique signale qu’il ne prend pas en charge de précision minimale. Les nuanceurs de précision minimale HLSL ne fonctionnent pas sur les systèmes d’exploitation antérieurs à Windows 8. par conséquent, si vous envisagez de cibler des systèmes d’exploitation antérieurs, vous devez créer plusieurs nuanceurs, certains d’entre eux et d’autres qui n’utilisent pas la précision minimale.

> [!Note]  
> N’effectuez pas de commutations de données entre différents niveaux de précision au sein d’un nuanceur, car ces types de conversions sont inutiles et réduisent les performances. L’exception est que les constantes de nuanceur sont toujours 32 bits, mais les fournisseurs peuvent concevoir du matériel graphique qui peut librement passer à la plus basse précision que la lecture des instructions HLSL peut utiliser.

 

À l’aide de la précision minimale, vous pouvez contrôler la précision des calculs dans différentes parties de votre code de nuanceur.

Les règles de précision minimale HLSL sont similaires à C/C++, où les types dans une expression déterminent la précision de l’opération, et non le type dans lequel les types sont finalement écrits.

## <a name="testing-your-minimum-precision-shader-code"></a>Test de votre code de nuanceur de précision minimal

Le rastériseur de référence ([**\_ référence de \_ type \_ de pilote D3D**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_driver_type)) vous donne une idée approximative de la façon dont la précision minimale de votre code de nuanceur HLSL se comporte en quantifiant chaque instruction HLSL sur la précision spécifiée. Cela vous permet de découvrir du code qui peut accidentellement reposer sur une précision supérieure à la précision minimale. Le rastériseur de référence ne s’exécute pas plus rapidement lorsque votre code de nuanceur HLSL utilise une précision minimale, mais vous pouvez l’utiliser pour vérifier l’exactitude de votre code. [Warp](/windows/desktop/direct3d11/overviews-direct3d-11-devices-create-warp) ([**\_ type de pilote D3D \_ \_ Warp**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_driver_type)) ne prend pas en charge l’utilisation de la précision minimale dans le code du nuanceur HLSL. WARP s’exécute uniquement avec une précision de 32 bits.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de programmation pour HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 