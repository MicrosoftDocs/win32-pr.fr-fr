---
title: Utilisation de la liaison de nuanceur
description: Nous montrons comment créer des fonctions HLSL précompilées, les empaqueter dans des bibliothèques et les lier à des nuanceurs complets au moment de l’exécution.
ms.assetid: 3A1597FF-F848-415E-BDF8-199C69C05C3B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7528415f1bedb0364a9c4b09126a983222fc42b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729916"
---
# <a name="using-shader-linking"></a>Utilisation de la liaison de nuanceur

Nous montrons comment créer des fonctions HLSL précompilées, les empaqueter dans des bibliothèques et les lier à des nuanceurs complets au moment de l’exécution. La liaison de nuanceur est prise en charge à partir de Windows 8.1.

**Objectif :** Découvrez comment utiliser la liaison de nuanceur.

## <a name="prerequisites"></a>Prérequis

Nous partons du principe que vous êtes familiarisé avec C++. Vous avez également besoin d’une expérience de base dans les concepts de programmation graphique.

**Durée totale :** 60 minutes.

## <a name="where-to-go-from-here"></a>Où aller à partir d’ici

Consultez également [API HLSL compiler](dx-graphics-d3dcompiler-reference.md).

Les opérations suivantes sont abordées :

-   Compiler le code de votre nuanceur
-   Charger le code compilé dans une bibliothèque de nuanceur
-   Lier les ressources des emplacements sources aux emplacements de destination
-   Construire une fonction-liaison-graphiques (FLGs) pour les nuanceurs
-   Lier des graphiques de nuanceur à une bibliothèque de nuanceur pour produire un objet blob de nuanceur que le runtime Direct3D peut utiliser

Nous allons ensuite créer une bibliothèque de nuanceur et lier les ressources des emplacements sources aux emplacements de destination.

[Empaquetage d’une bibliothèque de nuanceur](pachaging-a-shader-library.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de programmation pour HLSL](dx-graphics-hlsl-pguide.md)
</dt> <dt>

[Graphismes Direct3D 11](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11)
</dt> <dt>

[DXGI](/windows/desktop/direct3ddxgi/dx-graphics-dxgi)
</dt> </dl>

 

 