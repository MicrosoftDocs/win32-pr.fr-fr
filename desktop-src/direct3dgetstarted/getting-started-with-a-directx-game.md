---
title: Prise en main de DirectX pour Windows
description: La création d’un jeu Microsoft DirectX pour Windows est un défi pour un nouveau développeur. Ici, nous examinons rapidement les concepts impliqués et les étapes que vous devez suivre pour commencer à développer un jeu à l’aide de DirectX et C++.
ms.assetid: fd460c52-9854-4ffe-b89e-5219be2e11f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae09cd127a30401ae0493f5dd770fe1e67607b45
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106511696"
---
# <a name="get-started-with-directx-for-windows"></a>Prise en main de DirectX pour Windows

La création d’un jeu Microsoft DirectX pour Windows est un défi pour un nouveau développeur. Ici, nous examinons rapidement les concepts impliqués et les étapes que vous devez suivre pour commencer à développer un jeu à l’aide de DirectX et C++.

Commençons.

## <a name="what-skills-do-you-need"></a>Quelles sont les compétences dont vous avez besoin ?

Pour développer un jeu dans DirectX pour Windows, vous devez avoir quelques compétences de base. Plus précisément, vous devez être en mesure d’effectuer les opérations suivantes :

-   Lisez et écrivez du code C++ moderne (C++ 11 vous aide le plus) et familiarisez-vous avec les principes et modèles de conception C++ de base tels que les modèles et le modèle de fabrique. Vous devez également être familiarisé avec les bibliothèques C++ courantes, telles que la bibliothèque STL (Standard Template Library), et plus particulièrement avec les opérateurs de conversion, les types pointeur et les structures de données de bibliothèque de modèles standard (telles que STD :: Vector).
-   Comprenez la géométrie de base, la trigonométrie et l’algèbre linéaire. La majeure partie du code que vous trouverez dans les exemples suppose que vous comprenez ces formes de mathématiques et leurs règles communes.
-   Familiarisez-vous avec COM, en particulier [**Microsoft :: WRL :: ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) (pointeur intelligent).
-   Découvrez les bases de la technologie Graphics and Graphics, en particulier les graphiques 3D. Bien que DirectX ait sa propre terminologie, il s’appuie toujours sur une compréhension bien établie des principes graphiques 3D généraux.
-   Comprendre le concept d’une boucle de message, car vous allez implémenter une boucle qui écoute le système d’exploitation Windows.

## <a name="and-were-off"></a>Et nous sommes inactifs !

Prêt à commencer ? Nous allons nous pencher sur. Vous avez :

-   Une installation mise à jour et opérationnelle de Windows 8.1.
-   Installation de [Microsoft Visual Studio](https://visualstudio.microsoft.com/downloads/download-visual-studio-vs).
-   Un esprit intrépide et un désir d’en savoir plus sur le développement de jeux DirectX !

## <a name="next-steps"></a>Étapes suivantes



|                                                                                                    |                                                                                                           |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [Utiliser les ressources de l’appareil DirectX](work-with-dxgi.md)                                           | Découvrez comment utiliser DXGI pour créer un appareil graphique virtualisé et créer et configurer une chaîne de permutation.     |
| [Comprendre le pipeline de rendu Direct3D 11](understand-the-directx-11-2-graphics-pipeline.md) | Découvrez comment raccorder la classe de ressources de l’appareil DirectX et dessiner à l’aide du pipeline de graphiques Direct3D. |
| [Utiliser des nuanceurs et des ressources de nuanceur](work-with-shaders-and-shader-resources.md)               | Découvrez comment écrire des programmes nuanceurs HLSL pour les étapes de pipeline de graphiques Direct3D.                            |



 

 

 