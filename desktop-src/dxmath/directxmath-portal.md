---
description: DirectXMath
ms.assetid: 719954bf-0d7d-f647-2d3f-a77d87df204e
title: DirectXMath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a041696daf5d5cad8467d01f8ef7912d177ba63a7193945b4cb52a430f4afc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118501766"
---
# <a name="directxmath"></a>DirectXMath

## <a name="purpose"></a>Objectif

L’API DirectXMath fournit des fonctions et des types C++ compatibles SIMD pour les opérations mathématiques de graphiques algébriques et mathématiques courantes communes aux applications DirectX. la bibliothèque fournit des versions optimisées pour Windows 32 bits (x86), Windows 64 bits (x64) et Windows sur ARM/ARM64 par le biais de la prise en charge des intrinsèques SSE, AVX et arm-néon dans le compilateur de Visual C++.

Pour les développeurs qui débutent avec DirectXMath, vous pouvez envisager d’utiliser le wrapper SimpleMath dans le *Kit d’outils DirectX* pour [DirectX 11](https://go.microsoft.com/fwlink/?LinkId=248929)  /  [DirectX12](https://go.microsoft.com/fwlink/?LinkID=615561) comme point de départ.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                     | Description                                                                      |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [Guide de programmation DirectXMath](ovw-xnamath-progguide.md)<br/>     | DirectXMath fournit une solution mathématique optimisée pour Windows.<br/>           |
| [Informations de référence sur la programmation DirectXMath](ovw-xnamath-reference.md)<br/> | Cette section contient des documents de référence pour la bibliothèque DirectXMath.<br/> |



 

## <a name="developer-audience"></a>Développeurs concernés

la bibliothèque DirectXMath est conçue pour les développeurs C++ qui travaillent sur des jeux et des graphiques DirectX dans Windows applications du windows Store, des jeux Xbox et des applications de bureau traditionnelles pour Windows.

## <a name="obtaining-directxmath"></a>Obtention de DirectXMath
 
les en-têtes DirectXMath sont fournis dans le SDK Windows fourni avec Visual Studio 2012 ou version ultérieure, et en tant qu’en-tête en ligne, il n’y a aucune DLL ou bibliothèque statique à lier. Il est également disponible sous forme de package sur [NuGet](https://www.nuget.org/packages/directxmath/).

DirectXMath est open source sous la [licence MIT](https://opensource.org/licenses/MIT) hébergée sur [GitHub](https://github.com/Microsoft/DirectXMath).




