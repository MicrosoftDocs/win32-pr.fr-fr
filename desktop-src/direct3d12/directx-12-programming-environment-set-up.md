---
title: Configuration de l’environnement de programmation Direct3D 12
description: Décrit l’installation, les outils et les bibliothèques prises en charge qui constituent un environnement de développement Direct3D 12 productif.
ms.assetid: B2288866-E95F-46B8-A7A1-19888F029C03
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ee39dc1f99f2c99f911a52b211075b7d210b698
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404321"
---
# <a name="direct3d-12-programming-environment-setup"></a>Configuration de l’environnement de programmation Direct3D 12

Décrit l’installation, les outils et les bibliothèques prises en charge qui constituent un environnement de développement Direct3D 12 productif.

-   [Environnement de développement](#development-environment)
-   [Langues prises en charge](#supported-languages)
-   [Structures d’assistance](#helper-structures)
-   [Bibliothèque de gestion de la mémoire](#memory-management-library)
-   [Outils et bibliothèques pris en charge](#supported-tools-and-libraries)
-   [Exemples](#samples)
-   [Couche de débogage](#debug-layer)
-   [Vidéos pédagogiques](#educational-videos)
-   [Rubriques connexes](#related-topics)

## <a name="development-environment"></a>Environnement de développement

les en-têtes et les bibliothèques Direct3D 12 font partie du kit de développement logiciel (SDK) Windows 10. Aucun téléchargement ou installation distinct n’est requis pour utiliser Direct3D 12.

une fois que vous avez installé le logiciel Windows 10 SDK et Visual Studio, la configuration de votre environnement de programmation Direct3D 12 est terminée. Visual Studio 2019 est recommandé, car il inclut les outils de débogage D3D12 graphics, mais les versions antérieures de Visual Studio fonctionnent pour le développement de programmes.

Pour utiliser l' [API Direct3D 12](direct3d-12-reference.md), incluez D3d12. h et liez-la à D3d12. lib, ou interrogez les points d’entrée directement dans D3d12.dll.

Les en-têtes et les bibliothèques suivants sont disponibles. l’emplacement des bibliothèques statiques dépend de la version (32-bit ou 64 bits) de Windows 10 qui s’exécute sur votre ordinateur.



| Nom du fichier d’en-tête ou de bibliothèque | Description                         | Emplacement d’exploration      |
|-----------------------------|-------------------------------------|-----------------------|
| D3d12. h                     | En-tête de l’API Direct3D 12              | % WindowsSdkDir d' \\ inclure le \% WindowsSDKVersion% \\ \um |
| D3d12. lib                   | Bibliothèque stub de l’API Direct3D 12 statique | % WindowsSdkDir \\ lib \% WindowsSDKVersion% \\ \um\arch |
| D3d12.dll                   | Bibliothèque dynamique Direct3D 12 API     | % WINDIR% \\ system32    |
| D3d12SDKLayers. h            | En-tête de débogage Direct3D 12            | % WindowsSdkDir d' \\ inclure le \% WindowsSDKVersion% \\ \um |
| D3d12SDKLayers.dll          | Bibliothèque de débogage Direct3D 12 dynamique   | % WINDIR% \\ system32    |



## <a name="supported-languages"></a>Langues prises en charge

C++ est le seul langage pris en charge pour le développement Direct3D 12, C# et d’autres langages .NET ne sont pas pris en charge.

## <a name="helper-structures"></a>Structures d’assistance

Il existe un certain nombre de structures d’assistance qui, en particulier, facilitent l’initialisation d’un certain nombre de structures D3D12. Ces structures, ainsi que certaines fonctions utilitaires, se trouvent dans l’en-tête D3dx12. h. Cet en-tête est open source et peut être modifié par un développeur en fonction des besoins, téléchargez-le à partir de [la bibliothèque d’assistance D3D12](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) et reportez-vous aux [structures et fonctions d’assistance pour D3D12](helper-structures-and-functions-for-d3d12.md).

## <a name="memory-management-library"></a>Bibliothèque de gestion de la mémoire

Une bibliothèque d’assistance de gestion de la mémoire est disponible au téléchargement et peut être intégrée à votre application pour mieux correspondre au comportement de la gestion de mémoire D3D11. En tant que bibliothèque de gestion de style D3D11, elle est plus efficace avec les applications qui utilisent encore une stratégie d’allocation de style de *ressource validée* . En particulier, la bibliothèque doit être considérée comme une partie pas à pas qui vous permettra de revenir à la gestion de la mémoire D3D11 performante dans les scénarios de mémoire limité (par exemple, les cartes mémoire bas de gamme, 4k, ultra Settings, etc.). Les API D3D12 permettent d’améliorer l’efficacité de la mémoire par rapport à D3D11, bien que ces techniques puissent être difficiles à implémenter et prendre beaucoup de temps.

Notez que cette bibliothèque est un travail en cours et peut changer au fil du temps. Utilisez les liens ci-dessous pour accéder à la bibliothèque et à des exemples.

-   [Bibliothèque Starter de la résidence D3D12](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Libraries)

## <a name="supported-tools-and-libraries"></a>Outils et bibliothèques pris en charge

Les bibliothèques suivantes peuvent toutes être utilisées avec Direct3D 12.



| Bibliothèque                                                                                 |  Objectif                                                                                                                                                                                                                                                                      | Documentation                                                                                                           |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [Kit d’outils DirectX pour DirectX 12](https://github.com/Microsoft/DirectXTK12) | une collection importante de classes d’assistance pour l’écriture de code C++ de Direct3D 12 pour les applications plateforme Windows universelle (UWP), les applications de bureau Win32 pour les Windows 10 et les applications Xbox One exclusives.                                                                         | [Wiki DirectX12TK](https://github.com/Microsoft/DirectXTK12/wiki)                                          |
| [DirectXTex](https://github.com/Microsoft/DirectXTex)                      | Utilisez cette fonction pour lire et écrire des fichiers DDS et effectuer diverses opérations de traitement de contenu de texture, y compris le redimensionnement, la conversion de format, la génération de mappage MIP, la compression de bloc pour les ressources de texture Runtime Direct3D et la conversion de mappage de hauteur en carte normale. | [Wiki DirectXTex](https://github.com/Microsoft/DirectXTex/wiki)                                            |
| [DirectXMesh](https://github.com/Microsoft/DirectXMesh)                   | À utiliser pour effectuer diverses opérations de traitement de contenu Geometry, notamment la génération de normales et de frames tangentes, les calculs d’adjacence de triangle et l’optimisation du cache de vertex.                                                                                | [Wiki DirectXMesh](https://github.com/Microsoft/DirectXMesh/wiki)                                          |
| [DirectXMath](https://github.com/Microsoft/DirectXMath)                     | Un grand nombre de classes et de méthodes d’assistance pour prendre en charge les vecteurs, les scalaires, les matrices, les quaternions et de nombreuses autres opérations mathématiques.                                                                                                                               | [Documentation DirectXMath sur MSDN](/windows/desktop/dxmath/ovw-xnamath-progguide) |
| [UVAtlas](https://github.com/Microsoft/UVAtlas)                         | À utiliser pour la création et l’empaquetage d’un Atlas de texture isochart.                                                                                                                                                                                                           | [Wiki UVAtlas](https://github.com/Microsoft/UVAtlas/wiki)                                                  |



 

## <a name="samples"></a>Exemples

Pour obtenir la liste des exemples de D3D12 de travail et comment les localiser et les exécuter, reportez-vous à la rubrique [exemples fonctionnels](working-samples.md).

Pour obtenir des procédures pas à pas sur l’ajout de code pour activer des fonctionnalités particulières, reportez-vous à la procédure pas à pas sur le [code D3D12](d3d12-code-walk-throughs.md).

## <a name="debug-layer"></a>Couche de débogage

La couche de débogage fournit une validation de paramètres et de cohérence étendues supplémentaires (par exemple, la validation de la liaison de nuanceur et la liaison de ressources, la validation de la cohérence des paramètres et la création de rapports sur les erreurs).

> [!Note]  
> par Windows 10, pour créer un appareil qui prend en charge la couche de débogage, activez la fonctionnalité facultative « outils graphiques ». accédez au panneau Paramètres, sous système, applications & fonctionnalités, gérer les fonctionnalités facultatives, ajouter une fonctionnalité, puis rechercher « outils graphics ».

L’en-tête requis pour prendre en charge la couche de débogage, D3D12SDKLayers. h, est inclus par défaut dans d3d12. h.

Lorsque la couche de débogage répertorie les fuites de mémoire, elle génère une liste de pointeurs d’interface d’objet avec leurs noms conviviaux. Le nom convivial par défaut est « sans &lt; nom &gt; ». Vous pouvez définir le nom convivial à l’aide de la méthode [**ID3D12Object :: SetName**](/windows/desktop/api/d3d12/nf-d3d12-id3d12object-setname) . En règle générale, vous devez compiler ces appels en dehors de votre version de production.

Nous vous recommandons d’utiliser la couche de débogage pour déboguer vos applications et vous assurer qu’il ne s’agit pas d’erreurs et d’avertissements. La couche de débogage vous aide à écrire du code Direct3D 12. En outre, votre productivité peut augmenter lorsque vous utilisez la couche de débogage, car vous pouvez voir immédiatement les causes d’erreurs de rendu obscures ou même d’écrans noirs à leur source. La couche de débogage fournit des avertissements pour de nombreux problèmes. Par exemple :

-   Vous avez oublié de définir une texture, mais de la lire dans votre nuanceur de pixels.
-   Profondeur de sortie, mais n’ont pas de limite d’État du gabarit de profondeur.
-   Échec de la création de la texture avec INVALIDARG.

Définissez le compilateur définir le \_ débogage D3DCOMPILE pour indiquer au compilateur HLSL d’inclure les informations de débogage dans l’objet blob de nuanceur.

``` syntax
#define D3DCOMPILE_DEBUG 1
```

Pour plus d’informations sur toutes les méthodes et les interfaces de débogage, reportez-vous à la [référence de couche de débogage](direct3d-12-sdklayers-reference.md).

Pour obtenir des informations générales sur l’utilisation de la couche de débogage, consultez [Présentation de la couche de débogage D3D12](understanding-the-d3d12-debug-layer.md).

## <a name="educational-videos"></a>Vidéos pédagogiques

il existe un certain nombre de vidéos Direct3D 12 et Windows 10 associées dans [DirectX advanced learning didacticiels vidéo](https://www.youtube.com/channel/UCiaX2B8XiXR70jaN7NK-FpA), y compris des vidéos sur les outils de débogage graphique et rapports de bogues graphiques.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Comprendre Direct3D 12](directx-12-getting-started.md)
</dt> </dl>

 

 