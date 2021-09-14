---
description: D3DX est une bibliothèque d’outils conçue pour fournir des fonctionnalités graphiques supplémentaires par-dessus Direct3D. D3DX est fourni sous la forme d’une bibliothèque de liens dynamiques (DLL).
ms.assetid: d7b8c6ba-5c4f-494c-a24f-3b81a176725f
title: D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 397a2164349b761cd7ff2ccca5e2158abc22bd64
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127237006"
---
# <a name="d3dx-direct3d-9"></a>D3DX (Direct3D 9)

> [!NOTE]
> La bibliothèque D3DX est déconseillée. si vous n’avez pas la possibilité de procéder à une mise à niveau vers une version plus récente de Direct3D et du code de l’utilitaire associé, vous pouvez utiliser le package de NuGet [Microsoft. DXSDK. D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) au lieu de vous appuyer sur le SDK DirectX hérité ou DirectSetup.

D3DX est une bibliothèque d’outils conçue pour fournir des fonctionnalités graphiques supplémentaires par-dessus Direct3D. D3DX est fourni sous la forme d’une bibliothèque de liens dynamiques (DLL).

Une seule version de D3DX est fournie dans cette version du kit de développement logiciel (SDK) DirectX. La DLL de la version commerciale D3DX est incluse dans le redistribuable fourni dans le kit de développement logiciel (SDK) et est automatiquement installée dans le cadre de l' **installation de DirectX avec DirectSetup**. La bibliothèque D3DX incluse dans cette version dépend des runtimes Direct3D fournis avec ce kit de développement logiciel (SDK). Les applications qui sont liées à la version de D3DX dans cette version doivent également redistribuer le runtime à partir de ce kit de développement logiciel (SDK).

Plusieurs versions de D3DX peuvent résider indépendamment sur un même système simultanément. En liant de manière statique une application à D3dx9. lib, l’application est liée de manière dynamique à la DLL de la version commerciale D3DX correspondante au moment de l’exécution. Cette DLL correspond aux en-têtes D3DX avec lesquels l’application est compilée (nommée avec la \_ constante de version du kit de développement logiciel D3DX \_ dans D3dx9core. h). À mesure que de nouvelles versions de D3DX sont fournies dans les futures versions du SDK DirectX, les applications qui sont liées à des bibliothèques D3DX antérieures ne seront pas affectées.

La bibliothèque D3DX résout ces problèmes généraux de fonctionnalités :

-   [Prise en charge des dessins en ligne dans D3DX (Direct3D 9)](line-drawing-support-in-d3dx.md)
-   [Prise en charge des maillages dans D3DX (Direct3D 9)](mesh-support-in-d3dx.md)
-   [Prise en charge des fonctions mathématiques dans D3DX (Direct3D 9)](math-function-support-in-d3dx.md)
-   [Prise en charge de la texture dans D3DX (Direct3D 9)](texture-support-in-d3dx.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en main](getting-started.md)
</dt> </dl>

 

 



