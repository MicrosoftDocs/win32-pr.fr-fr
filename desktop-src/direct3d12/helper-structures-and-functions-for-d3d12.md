---
title: Structures et fonctions d’assistance pour Direct3D 12
description: Ces structures d’assistance et fonctions d’assistance sont déclarées dans `d3dx12.h` .
ms.assetid: 095958A9-345B-45AE-8363-B353534044B2
keywords:
- Fonctions d’assistance
- Structures d’assistance
- d3dx12. h
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b42bc9ae73f3537cc786a465feba596b3392401
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812176"
---
# <a name="helper-structures-and-functions-for-direct3d-12"></a>Structures et fonctions d’assistance pour Direct3D 12

Ces structures d’assistance et fonctions d’assistance sont déclarées dans `d3dx12.h` .

`d3dx12.h` est disponible séparément des en-têtes Direct3D 12. Vous pouvez télécharger `d3dx12.h` à partir de [la bibliothèque d’assistance D3D12](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h).

Vous pouvez utiliser ces structures d’assistance pour créer et initialiser des structures Direct3D. Ces structures d’assistance se comportent comme des classes C++. Chaque structure d’assistance a généralement un constructeur par défaut, un constructeur explicite, un destructeur et un opérateur de cast pour la structure D3D12 associée. Chaque structure d’assistance a un préfixe « C » et est associée à une structure D3D12 qui ne possède pas le préfixe « C ». La plupart des structures d’assistance contiennent des méthodes membres d’initialisation, certaines contiennent des fonctions de comparaison.

## <a name="in-this-section"></a>Contenu de cette section

| Rubrique | Description |
|-|-|
| [Interfaces d’assistance pour D3D12](helper-interfaces-for-d3d12.md) | Ces interfaces d’assistance sont particulièrement utiles pour gérer les sous-ressources et sont déclarées dans `d3dx12.h` .  |
| [Structures d’assistance pour D3D12](helper-structures-for-d3d12.md) | Ces structures d’assistance permettent d’initialiser un grand nombre des structures Direct3D 12 et sont déclarées dans `d3dx12.h` . |
| [Fonctions d’assistance pour D3D12](helper-functions-for-d3d12.md) | Ces fonctions d’assistance permettent notamment de gérer des sous-ressources et sont déclarées dans `d3dx12.h` .  |

## <a name="related-topics"></a>Rubriques connexes

* [Référence de Direct3D 12](direct3d-12-reference.md)
