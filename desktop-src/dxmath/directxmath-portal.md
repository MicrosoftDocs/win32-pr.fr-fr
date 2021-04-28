---
description: DirectXMath
ms.assetid: 719954bf-0d7d-f647-2d3f-a77d87df204e
title: DirectXMath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fd35f1faf004bc55a6802da204a6c2fe4e7869b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113007"
---
# <a name="directxmath"></a>DirectXMath

## <a name="purpose"></a>Objectif

L’API DirectXMath fournit des fonctions et des types C++ compatibles SIMD pour les opérations mathématiques de graphiques algébriques et mathématiques courantes communes aux applications DirectX. La bibliothèque fournit des versions optimisées pour Windows 32 bits (x86), Windows 64 bits (x64) et Windows sur ARM/ARM64 via la prise en charge des intrinsèques SSE, AVX et ARM-néon dans le compilateur de Visual C++.

Pour les développeurs qui débutent avec DirectXMath, vous pouvez envisager d’utiliser le wrapper SimpleMath dans le *Kit d’outils DirectX* pour [DirectX 11](https://go.microsoft.com/fwlink/?LinkId=248929)  /  [DirectX12](https://go.microsoft.com/fwlink/?LinkID=615561) comme point de départ.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                     | Description                                                                      |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [Guide de programmation DirectXMath](ovw-xnamath-progguide.md)<br/>     | DirectXMath fournit une solution mathématique optimisée pour Windows.<br/>           |
| [Informations de référence sur la programmation DirectXMath](ovw-xnamath-reference.md)<br/> | Cette section contient des documents de référence pour la bibliothèque DirectXMath.<br/> |



 

## <a name="developer-audience"></a>Développeurs concernés

La bibliothèque DirectXMath est conçue pour les développeurs C++ qui travaillent sur les jeux et les graphiques DirectX dans les applications du Windows Store, les jeux Xbox et les applications de bureau traditionnelles pour Windows.

## <a name="obtaining-directxmath"></a>Obtention de DirectXMath
 
Les en-têtes DirectXMath sont fournis dans le SDK Windows fourni avec Visual Studio 2012 ou version ultérieure, et en tant qu’en-tête en ligne, il n’y a aucune DLL ou bibliothèque statique à lier. Il est également disponible sous la forme d’un package sur [NuGet](https://www.nuget.org/packages/directxmath/).

DirectXMath est open source sous la [licence MIT](https://opensource.org/licenses/MIT) hébergée sur [GitHub](https://github.com/Microsoft/DirectXMath).




