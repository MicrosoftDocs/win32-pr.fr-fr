---
title: Exceptions
description: Cette rubrique décrit les exceptions lors de l’utilisation de Direct3D 11 sur du matériel de niveau inférieur.
ms.assetid: b3f85036-8572-40ee-b522-3b677443b840
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97920ae42347cf618b22df82abc3b6e06bd5200d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316272"
---
# <a name="exceptions"></a>Exceptions

Certaines fonctionnalités de Direct3D 11 ne sont pas entièrement spécifiées par les niveaux de fonctionnalité. Cette rubrique décrit les exceptions lors de l’utilisation de Direct3D 11 sur du matériel de niveau inférieur. Une fonctionnalité a peut-être été ajoutée après que le niveau de fonctionnalité a été défini (et nécessite un pilote mis à jour), ou peut-être que des GPU différents implémentent des implémentations très différentes. Les exceptions au niveau des fonctionnalités peuvent être regroupées dans les groupes suivants :

-   [Formats étendus](#extended-formats)
-   [Anticrénelage d’échantillonnage](#multisample-anti-aliasing)
-   [Tailles de Texture2D](#texture2d-sizes)
-   [Comportement spécial des adaptateurs pour le niveau de fonctionnalité 9](#special-behavior-of-adapters-for-feature-level-9)
-   [Rubriques connexes](#related-topics)

La section de [référence 10Level9](d3d11-graphics-reference-10level9.md) répertorie les différences entre la façon dont les différentes méthodes [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) et [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) se comportent à différents niveaux de fonctionnalités 10Level9.

## <a name="extended-formats"></a>Formats étendus

Un format étendu est un format de pixel ajouté à Direct3D 10,1 et Direct3D 11 pour les niveaux de fonctionnalité 10 \_ 0 et 10 \_ 1. Un format étendu nécessite un pilote mis à jour (pour Direct3D 10 \_ 1 ou versions antérieures). Utilisez [**ID3D11Device :: CheckFormatSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkformatsupport) et [**ID3D11Device :: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) pour demander la prise en charge de ces formats étendus.

Un format étendu :

-   Ajoute la prise en charge de l’ordre BGRA des ressources par composant de 8 bits.
-   Autorise la conversion d’une mémoire tampon d’échange de valeur entière. Cela permet à une application d’ajouter ou de supprimer le \_ suffixe ou le rendu sRVB à une \_ chaîne d’échange de biais XR.
-   Ajoute la prise en charge facultative pour le \_ format dxgi \_ R10G10B10 \_ XR \_ Bias \_ a2 \_ UNORM.
-   Garantit qu’une \_ chaîne de \_ permutation R16G16B16A16 de format dxgi \_ est présentée comme si les données contenues ne sont pas encodées en sRVB.

Le jeu complet de formats étendus est entièrement pris en charge ou n’est pas pris en charge, à l’exception du \_ format de biais XR. Le \_ format de biais XR est le suivant :

-   Non pris en charge dans 9 niveaux
-   Facultatif dans le niveau 10 \_ 0 ou 10 \_ 1
-   Garantie au niveau du 11 \_ 0

## <a name="multisample-anti-aliasing"></a>Anticrénelage d’échantillonnage

Les implémentations MSAA ont peu de choses en commun entre les implémentations GPU. Le niveau de fonctionnalité 10,1 a ajouté des minima bien définis, mais à des niveaux de fonctionnalités inférieurs, MSAA doit être testé explicitement à l’aide de [**ID3D11Device :: CheckMultisampleQualityLevels**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkmultisamplequalitylevels).

## <a name="texture2d-sizes"></a>Tailles de Texture2D

Un niveau de fonctionnalité garantit qu’une taille minimale peut être créée. Toutefois, une application peut créer des textures plus volumineuses jusqu’à la taille maximale prise en charge par le GPU. Une application doit attendre l’échec d’une méthode telle que [**ID3D11Device :: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) si un maximum est dépassé.

## <a name="special-behavior-of-adapters-for-feature-level-9"></a>Comportement spécial des adaptateurs pour le niveau de fonctionnalité 9

Les trois niveaux de fonctionnalité les plus bas \_ \_ niveau de fonctionnalité D3D \_ 9 \_ 1, \_ niveau de fonctionnalité D3D \_ \_ 9 \_ 2 et \_ \_ niveau de fonctionnalité D3D \_ 9 \_ 3, partagent une DLL d’implémentation commune et traitent l’argument [**IDXGIAdapter**](/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter) pour D3D11CreateDevice \[ AndSwapchain \] en tant qu’adaptateur de modèle et créent leur propre adaptateur dans le cadre de la création de l’appareil. Cela signifie que le **IDXGIAdapter** passé dans la routine de création ne sera pas le même que celui récupéré à partir de l’appareil via IDXGIDevice :: GetAdapter. Cela est dû au fait que les **IDXGIOutputs** énumérées à partir de l’adaptateur transmis ne peuvent pas être utilisés pour entrer du plein écran à l’aide de n’importe quel appareil de niveau 9, puisque ces sorties ne sont pas détenues par l’adaptateur de l’appareil. Il est conseillé de supprimer l’adaptateur de modèle passé et de récupérer l’adaptateur créé de l’appareil à l’aide de IDXGIDevice :: GetAdapter, où [**IDXGIDevice**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) peut être récupéré à l’aide de QueryInterface à partir de l’interface de périphérique Direct3D.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Direct3D 11 sur du matériel de niveau inférieur](overviews-direct3d-11-devices-downlevel.md)
</dt> </dl>

 

 