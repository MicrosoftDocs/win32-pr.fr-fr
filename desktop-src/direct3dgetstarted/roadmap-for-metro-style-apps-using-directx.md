---
title: Feuille de route pour les applications de bureau DirectX
description: Voici des ressources clés pour vous aider à utiliser DirectX et C++ pour développer des applications de bureau riches en graphiques, comme les jeux.
ms.assetid: d7921f38-e384-4a83-b458-ee71f7044468
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eca95e1fe281253705620136afdced3cb705fe02
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/18/2020
ms.locfileid: "104032135"
---
# <a name="roadmap-for-desktop-directx-apps"></a>Feuille de route pour les applications de bureau DirectX

Voici des ressources clés pour vous aider à utiliser DirectX et C++ pour développer des applications de bureau gourmandes en graphiques, telles que des jeux. Il ne s’agit pas d’une liste exhaustive de toutes les fonctionnalités ou ressources disponibles.

## <a name="get-started"></a>Bien démarrer

Voici quelques rubriques clés. Configuration de votre projet DirectX, en acclimatant des applications Windows et des exemples d’applications.

| Rubrique | Description |
|-|-|
| [Créer votre première application Windows à l’aide de DirectX](building-your-first-directx-app.md) | Utilisez ce didacticiel de base pour commencer à utiliser le développement d’applications DirectX, puis utilisez la feuille de route pour poursuivre l’exploration de DirectX. |
| [Prise en main de DirectX pour Windows](getting-started-with-a-directx-game.md) | Passez en revue les étapes que vous devez suivre pour commencer à développer un jeu à l’aide de DirectX et C++. |
| [Code complet pour une infrastructure DirectX](complete-code-sample-for-using-a-corewindow-with-directx.md) | Obtenir le code d’un Framework de rendu DirectX de base. |
| [Comment utiliser Direct3D 11](/windows/desktop/direct3d11/how-to-use-direct3d-11) | Cette section montre comment utiliser l’API Microsoft Direct3D 11 pour accomplir plusieurs tâches courantes. |
| [Guide de programmation pour Direct3D 11](/windows/desktop/direct3d11/dx-graphics-overviews) | Le Guide de programmation contient des informations sur l’utilisation du pipeline programmable Microsoft Direct3D 11 pour créer des graphiques 3D en temps réel pour les applications de bureau. |
| [Outils pour DirectX Graphics](/windows/desktop/direct3dtools/dx-graphics-tools) | Documentation pour les outils utilisés pour prendre en charge le développement DirectX. |
| [Nouveautés de Direct3D 11](/windows/desktop/direct3d11/dx-graphics-overviews-introduction) | La répartition de toutes les fonctionnalités ajoutées dans les versions les plus récentes de DirectX et Direct3D (actuellement 11,2). |
| [Télécharger Visual Studio 2013](https://msdn.microsoft.com/windows/apps/br229516.aspx) | Vous devez disposer de Visual Studio Express 2013 pour Windows Desktop pour créer des jeux Windows Store. Pour une visite guidée de Visual Studio, consultez [développer des applications du Windows Store à l’aide de Visual studio 2012](/previous-versions/windows/apps/br211384(v=win.10)). Pour plus d’informations sur les nouvelles fonctionnalités de Visual Studio, consultez [les points importants pour Visual Studio 2013](/previous-versions/visualstudio/visual-studio-2013/bb386063(v=vs.120)). |
| [Où est le kit SDK DirectX ?](../directx-sdk--august-2009-.md) | Contient des conseils pour les développeurs qui souhaitent intégrer leurs projets DirectX dans Microsoft Visual Studio. |

## <a name="sample-applications"></a>Exemples d’applications

| Rubrique | Description |
|-|-|
| [Didacticiel Direct3D-exemple Win32](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample) | Exemple de didacticiel de base sur le Direct3D Desktop Direct3D. |
| [Exemple de rendu vidéo DirectX](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DirectX%20video%20rendering%20sample) | Exemple illustrant un rendu vidéo personnalisé avec Direct3D. |

## <a name="review-key-direct3d-11-concepts"></a>Passer en revue les principaux concepts de Direct3D 11

| Rubrique | Description |
|-|-|
| [Pipeline graphique](/windows/desktop/direct3d11/overviews-direct3d-11-graphics-pipeline) | Aborde le pipeline de base des graphiques Direct3D 11. |
| [Rendu](/windows/desktop/direct3d11/overviews-direct3d-11-render) | Décrit les modèles de rendu Direct3D, les composants, les nuanceurs et le workflow d’appel d’API. |
| [Ressources](/windows/desktop/direct3d11/overviews-direct3d-11-resources) | Traite des « ressources » Direct3D, telles que les mémoires tampons et les autres types de ressources GPU. |
| [Effets](/windows/desktop/direct3d11/d3d11-graphics-programming-guide-effects) | Aborde les effets et l’instanciation de plusieurs nuanceurs Direct3D.  |
| [Comment : créer une chaîne de permutation](/windows/desktop/direct3d11/overviews-direct3d-11-devices-create-swap-chain) | Comment créer la chaîne de permutation utilisée pour dessiner des pixels dans une zone de l’écran. |
| [Comment : créer un appareil et un contexte immédiat](/windows/desktop/direct3d11/overviews-direct3d-11-devices-initialize) | Comment créer une abstraction de périphérique Direct3D et un contexte immédiat pour le dessin. |
| [Comment : créer une mémoire tampon de vertex](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-vertex-how-to) | Comment créer une liste simple de vertex de maillage à traiter par le GPU. |
| [Comment : créer un tampon d’index](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-index-how-to) | Comment créer un tampon d’index permettant au nuanceur de sommets de parcourir l’ordre des vertex dans une maille. |
| [Comment : créer une mémoire tampon constante](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to) | Comment passer des données constantes (uniformes) entre l’UC et le GPU pendant le rendu. |
| [Comment : créer une texture](/windows/desktop/direct3d11/overviews-direct3d-11-resources-textures-create) | Comment créer une texture ou une autre ressource tampon pouvant être échantillonnée par le GPU. |
| [Comment : initialiser une texture à partir d’un fichier](/windows/desktop/direct3d11/overviews-direct3d-11-resources-textures-how-to) | Comment charger une texture à partir d’un fichier et la traiter pour une utilisation par le pipeline du nuanceur. |
| [Comment : compiler un nuanceur](../direct3d11/how-to--compile-a-shader.md) | Comment compiler un nuanceur pour l’utiliser dans votre application Graphics. |

## <a name="graphics-apis"></a>API graphiques

| Rubrique | Description |
|-|-|
| [Direct3D 11](/windows/desktop/direct3d11/d3d11-graphics-reference) | Documentation des API principales pour la virtualisation du GPU et de ses ressources, et pour dessiner des graphiques à l’aide d’un modèle de nuanceur unifié. |
| [Langage HLSL Direct3D](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) | Documentation de référence pour High-Level Language Shader, la syntaxe et les règles utilisées pour définir les programmes de nuanceur exécutés dans le cadre du pipeline Graphics dans un modèle de nuanceur unifié. |
| [Interface DirectX Graphics (DXGI)](/windows/desktop/direct3ddxgi/dx-graphics-dxgi) | Documentation des API de bas niveau utilisées pour acquérir l’interface GPU et les ressources système. |
| [Direct2D](/windows/desktop/Direct2D/direct2d-portal) | Documentation pour les API Direct2D, qui prennent en charge le dessin de primitives 2D. En règle générale, Direct2D est utilisé pour les interfaces utilisateur personnalisées, le traitement d’images et le traitement par lot, et les jeux simples. |
| [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) | Documentation pour les API DirectWrite, qui prennent en charge le rendu et la mise à l’échelle personnalisés des polices. |
| [Composant Imagerie Windows (WIC)](/windows/desktop/wic/-wic-api) | Documentation sur les API WIC, qui sont utilisées pour lire et gérer différents formats d’image bitmap. |
| [Surfaces DirectDraw (DDS)](/windows/desktop/direct3ddds/dx-graphics-dds) pour les textures | Documentation pour les API DDS, qui sont utilisées pour la compression et la décompression de texture 2D conjointement avec les API WIC. |
| [DirectXMath](/windows/desktop/dxmath/directxmath-portal) | Documentation pour les API DirectXMath, qui prennent en charge Direct3D avec un ensemble de types et de fonctions adaptées au développement de graphiques en temps réel 3D. (Anciennement XNAMath.) |
| [DirectCompute](https://walbourn.github.io/) | Documentation pour les API DirectCompute, utilisée pour la fonctionnalité de nuanceur de calcul ou d’utilisation générale. |

## <a name="audio-media-and-input-apis"></a>API audio, multimédia et d’entrée

| Rubrique | Description |
|-|-|
| [Guide de programmation XAudio2](/windows/desktop/xaudio2/programming-guide) | Nœud de niveau supérieur pour la documentation conceptuelle de l’API audio XAudio2. |
| [Référence de programmation XAudio2](/windows/desktop/xaudio2/programming-reference) | Nœud de niveau supérieur pour la documentation de référence sur l’API audio XAudio2. |
| [Guide de programmation XInput](/windows/desktop/xinput/programming-guide) | Nœud de niveau supérieur pour la documentation conceptuelle de l’API du contrôleur XInput. |
| [Informations de référence sur la programmation XInput](/windows/desktop/xinput/programming-reference) | Nœud de niveau supérieur pour la documentation de référence sur l’API du contrôleur XInput. |
| [Media Foundation](/windows/desktop/medfound/about-the-media-foundation-sdk) | Nœud de niveau supérieur pour la documentation de l’API de lecture (audio/vidéo) du support Media Foundation (MF). En règle générale, MF est utilisé dans les jeux pour la lecture de la bande-son, tandis que XAudio2 est utilisé pour le son dynamique. |

## <a name="port-to-directx-11"></a>Port vers DirectX 11

| Rubrique | Description |
|-|-|
| [Migration vers Direct3D 11](/windows/desktop/direct3d11/d3d11-programming-guide-migrating) | Conseils de base pour déplacer votre code base DirectX 9 vers DirectX 11. |
| [Techniques de codage à double utilisation pour les jeux](https://walbourn.github.io/) | Billet de Blog détaillé sur le développement pour les niveaux de fonctionnalité DirectX 9 \_ \* et DirectX 11 \_ \* dans une même application. |
| [Implémentation de mémoires tampons secondaires pour le niveau de fonctionnalité Direct3D 9](/previous-versions/windows/apps/jj262110(v=win.10)) | Conseils pour l’implémentation des clichés instantanés sous DirectX Feature Level 9 \_ \* . |

## <a name="work-with-c"></a>Utiliser C++

Si vous êtes un vieil avec C++ sur les plateformes Windows, les choses peuvent être légèrement différentes. Voici quelques pointeurs vers des rubriques qui peuvent vous aider à obtenir un descripteur sur la différence.

> [!NOTE]
> Certaines de ces rubriques existent pour vous aider à gérer votre application C++/CX. Toutefois, nous vous recommandons d’utiliser [C++/WinRT](/windows/uwp/cpp-and-winrt-apis/intro-to-using-cpp-with-winrt) pour les nouvelles applications. C++/WinRT est une projection de langage C++17 moderne entièrement standard pour les API Windows Runtime (WinRT), implémentée en tant que bibliothèque basée sur un fichier d’en-tête et conçue pour vous fournir un accès de première classe à l’API Windows moderne.

| Rubrique | Description |
|-|-|
| [**Informations de référence sur le langage Visual C++ (C++/CX)**](/cpp/cppcx/visual-c-language-reference-c-cx?view=vs-2019) | Page de niveau supérieur qui établit un lien vers du contenu relatif à C++. |
| [**Référence rapide (Windows Runtime et Visual C++)**](/cpp/cppcx/quick-reference-c-cx?view=vs-2019) | Table qui fournit des informations Express sur Visual C++ les opérateurs et les mots clés des extensions de composant (C++/CX). |
| [**Système de type (C++/CX)**](/cpp/cppcx/type-system-c-cx?view=vs-2019) | Contenu de référence pour les types pris en charge par C++/CX. |
| [**Espaces de noms (C++/CX)**](/cpp/cppcx/namespaces-reference-c-cx?view=vs-2019) | Contenu de référence pour les espaces de noms qui contiennent des types spécifiques à C++ qui peuvent être utilisés dans les applications du Windows Store. |

| | |
|-|-|
| [Programmation asynchrone (DirectX et C++)](/previous-versions/windows/apps/hh994919(v=win.10)) | En savoir plus sur la programmation asynchrone et multithread pour les jeux et les applications DirectX. |
| [Programmation asynchrone en C++](/previous-versions/windows/apps/hh780559(v=win.10)) | Décrit les méthodes de base pour utiliser la classe de tâche afin de consommer Windows Runtime méthodes asynchrones. |
| [**Classe de tâche (runtime d’accès concurrentiel)**](/previous-versions/visualstudio/visual-studio-2012/hh750113(v=vs.110)) | Documentation de référence pour la classe Task. |
| [Parallélisme des tâches (runtime d’accès concurrentiel)](/previous-versions/visualstudio/visual-studio-2010/dd492427(v=vs.100)) | Présentation détaillée de la classe de tâche et de son utilisation. |

## <a name="additional-useful-libraries-for-windows-c-programming"></a>Bibliothèques utiles supplémentaires pour la programmation Windows C++

| | |
|-|-|
| [Bibliothèque STL (C++ Standard Template Library)](https://msdn.microsoft.com/library/c191tb28(v=VS.71).aspx) | Les types de Windows Runtime jouent un mal avec les types de bibliothèques de modèles standard. La plupart des applications du Windows Store C++ utilisent des algorithmes et des collections STL (Standard Template Library), à l’exception de la limite ABI. |
| [bibliothèque de modèles parallèles](/previous-versions/visualstudio/visual-studio-2010/dd492418(v=vs.100)) | La bibliothèque de modèles parallèles fournit des algorithmes et des types qui simplifient le parallélisme des tâches et le parallélisme des données sur le processeur.  |
| [C++ Accelerated Massive Parallelism (C++ AMP)](/previous-versions/visualstudio/visual-studio-2012/hh265137(v=vs.110)) | C++ AMP permet d’accéder au GPU pour le parallélisme des données à usage général sur les cartes vidéo qui prennent en charge DirectX 11. |

## <a name="blogs-and-other-resources"></a>Blogs et autres ressources

| Rubrique | Description |
|-|-|
| [Blog sur les jeux pour Windows et DirectX](https://walbourn.github.io/) | Blog régulièrement mis à jour à partir d’un contributeur principal DirectX, et une ressource remarquable pour les développements DirectX. |
| [Blog du développeur Windows DirectX](https://devblogs.microsoft.com/directx/) | Blog officiel de Windows DirectX. |
| [Blog DirectX de Shawn Hargreave](https://www.shawnhargreaves.com/blogindex.html)) | Blog de développement d’un autre contributeur de développement Windows DirectX bien respecté. |
| [Kit de ressources DirectX](https://directxtk.codeplex.com/) | Site CodePlex pour DirectX Tool Kit (DxTK), qui contient un certain nombre d’API de prise en charge utiles pour le chargement des maillages, la diffusion de sons et d’autres comportements courants. |
| [Bibliothèque de traitement des textures DirectXTex](https://directxtex.codeplex.com/) | Site de code plex pour la bibliothèque de traitement de texture DirectX (DxTEX), qui contient les API de prise en charge pour le traitement de la texture et la compression/décompression. |