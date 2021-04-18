---
description: Fonctionnalités Direct3D 10,1
ms.assetid: e60c6116-e2f9-46b7-aed8-13e3e5ae2b90
title: Fonctionnalités Direct3D 10,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99935941f60a984407c688e4ae67f0a125b0130d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515931"
---
# <a name="direct3d-101-features"></a>Fonctionnalités Direct3D 10,1

Direct3D 10,1 étend l’ensemble des fonctionnalités de Direct3D 10,0 avec les nouvelles fonctionnalités suivantes :

-   Blend modes : mode de fusion indépendant par cible de rendu à l’aide de la nouvelle interface d’état de fusion (voir [**interface ID3D10BlendState1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10blendstate1)). Les opérations de fusion à deux sources sont limitées à l’emplacement cible de rendu 0 ; vous ne pouvez pas écrire dans d’autres sorties ou n’avoir aucune cible de rendu liée à des emplacements autres que l’emplacement 0.
-   Comportement d’élimination-les faces de zone zéro sont automatiquement éliminées ; Cela affecte le rendu filaire uniquement.
-   Règles à virgule flottante : utilise les mêmes règles IEEE-754 pour la virgule flottante, sauf que les opérations à virgule flottante 32 bits ont été renforcées pour produire un résultat dans 0,5 unité-Last-place (0,5 ULP) du résultat infini. Cela s’applique à l’addition, à la soustraction et à la multiplication. (précision à 0,5 ULP pour multiplier, 1,0 ULP pour réciproquement).
-   Formats : la précision de la fusion float16 est passée à 0,5 ULP. La fusion est également requise pour les formats UNORM16/SNORM16/SNORM8.
-   Anticrénelage à plusieurs échantillons-l’échantillonnage multiple a été amélioré pour généraliser la transparence basée sur la couverture et rendre le travail d’échantillonnage multiple plus efficace avec un rendu multipasse. Pour ce faire, toute la sémantique d’échantillonnage est définie comme si le nuanceur de pixels s’exécute toujours une fois par échantillon (fréquence d’échantillonnage), en calculant une couleur distincte par échantillon. Si un nuanceur de pixels n’utilise pas d’attributs par échantillon, il calcule la même valeur pour chaque échantillon couvert dans un pixel. Dans ce cas, il est équivalent au matériel exécutant le nuanceur une fois par pixel (fréquence de pixel), en répliquant le résultat sur tous les exemples couverts. Naturellement, l’exécution à la fréquence de pixel produit toujours les mêmes résultats que l’exécution du même nuanceur à la fréquence d’échantillonnage, lorsque les attributs sont échantillonnés à une fréquence de pixel. La statistique de pipeline PSInvocations s’incrémente à la fréquence d’échantillonnage, sauf si le nuanceur s’exécute à la fréquence de pixel.
-   Bande passante d’étape de pipeline : augmentation de la quantité de données pouvant être transmises entre les étapes du nuanceur : 

    | Ressource                        | limites                    |
    |---------------------------------|---------------------------|
    | Registres entre les étapes du nuanceur | 32 (32 bits x 4-composant) |
    | Registres d’entrée du nuanceur de sommets   | 32                        |
    | Emplacements d’entrée de l’assembleur d’entrée     | 32                        |

    

     

-   Règles de pixellisation : les règles de pixellisation ont été modifiées pour les lignes. de plus, de nouvelles fonctionnalités ont été ajoutées.
    -   MultisampleEnable affecte uniquement la pixellisation des lignes (les points et triangles ne sont pas affectés) et est utilisé pour choisir un algorithme de dessin de ligne. Cela signifie que certains exemples de pixellisation de Direct3D 10 ne sont plus pris en charge.
    -   Nouvelle exécution de nuanceur de pixels de fréquence d’échantillonnage avec pixellisation primitive.
-   Ressources-CopyResource est activé dans deux nouveaux scénarios :
    -   Les surfaces MSAA de couleur et de profondeur/stencil peuvent désormais être utilisées avec CopyResource en tant que source ou destination
    -   Conversion de format lors de la copie entre certaines ressources typées préstructurées 32/64/128 bits et les représentations compressées des mêmes largeurs de bits.
-   Échantillonnage de texture-exemple \_ c et \_ exemples \_ d’instructions c LZ sont définis pour fonctionner avec Texture2DArrays et TextureCubeArrays, utilisez le membre location (le composant alpha) pour spécifier un index de tableau.
-   Les vues-TextureCube et le nouveau TextureCubeArray (consultez [**D3D10 \_ TEXCUBE \_ array \_ SRV1**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_texcube_array_srv1)) ne sont pas des ressources réelles, mais sont de nouvelles vues sur une ressource Texture2DArray. Créer un affichage des ressources à partir d’une ressource Texture2DArray avec un nouvel indicateur d’utilisation (D3D10 \_ Resource \_ misc \_ TEXTURECUBE), utilisez la nouvelle interface d' [**interface ID3D10ShaderResourceView1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10shaderresourceview1) pour lier une vue de texture de cube au pipeline.

Les nouvelles fonctionnalités requièrent un type d’appareil 10,1 (voir [**interface ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1)) qui peut être créée en appelant [**D3D10CreateDevice1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdevice1), ou vous pouvez créer l’appareil et la chaîne de permutation en même temps en appelant [**D3D10CreateDeviceAndSwapChain1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdeviceandswapchain1).

Dans Windows Vista Service Pack 1, les dll Direct3D 10,0 et Direct3D 10,1 existent côte à côte sur le système. Pour accéder aux fonctionnalités 10,1, effectuez l’une des opérations suivantes :

## <a name="accessing-101-features-on-vista-gold-and-vista-service-pack-1"></a>Accès aux fonctionnalités 10,1 sur Vista Gold et Vista Service Pack 1

Les développeurs qui souhaitent prendre en charge Vista Gold et SP1 doivent tenir compte de l’absence des nouvelles extensions d’API 10,1 sur Vista Gold. DXUT et D3DX10 fournissent des fonctions pratiques pour créer l’appareil approprié, en fonction des dll disponibles sur le système et du matériel disponible (10,0 ou 10,1). L’appareil 10,1 hérite de l’appareil 10,0 et peut être récupéré à l’aide de QueryInterface (). Il est recommandé que chaque application effectue le suivi du type d’appareil et conserve un pointeur vers l’appareil 10,1 (le cas échéant) pour éviter des appels QueryInterface fréquents lorsque la fonctionnalité 10,1 est souhaitée. De même, là où 10,1 les vues de ressources et les objets d’État sont associés à la classe personnalisée d’une application, il est recommandé que l’application détermine si l’objet est un type 10,0 ou 10,1 pour éviter les appels QueryInterface () redondants. D3DX10 comprend un ensemble de fonctions utilitaires permettant de simplifier ce processus (voir [**D3DX10CreateDevice**](d3dx10createdevice.md) et [**D3DX10CreateDeviceAndSwapChain**](d3dx10createdeviceandswapchain.md)).

## <a name="accessing-101-features-on-vista-service-pack-1-exclusively"></a>Accès exclusif aux fonctionnalités 10,1 sur Vista Service Pack 1

Certains développeurs peuvent choisir d’exiger Vista Service Pack 1, qui sera distribué à grande échelle pour les utilisateurs finaux et comprend une série d’améliorations en dehors de Direct3D 10,1. Ces développeurs peuvent utiliser les en-têtes et les bibliothèques Direct3D 10,1 exclusivement, en prenant une dépendance sur les dll Direct3D 10,1 qui prennent en charge à la fois le matériel 10,0 et 10,1 (certains appels peuvent échouer sur les appareils 10,0 où la nouvelle fonctionnalité n’est pas prise en charge).

Remarques supplémentaires :

-   Les API exposées dans le D3DX10.dll acceptent les deux appareils 10,0 et 10,1, et tirent parti des fonctionnalités 10,1 lorsqu’elles sont disponibles.
-   D3D10SDKLayers.dll prend en charge un appareil 10,1 et peut générer le spew de débogage approprié pour les fonctionnalités 10,1.
-   D3D10Ref.dll implémente un périphérique logiciel 10,0 et 10,1.
-   D3DX10 et FXC prennent en charge le modèle de nuanceur 10,1 mis à jour avec les cibles suivantes : vs \_ 4 \_ 1, GS \_ 4 \_ 1, PS \_ 4 \_ 1 et FX \_ 4 \_ 1 qui peuvent être liées à un appareil 10,1. Un appareil 10,1 prend en charge les nuanceurs de modèle de nuanceur 4,0 et 4,1.
-   L’environnement d’effet Direct3D 10,0 prend en charge les appareils 10,0 et 10,1. Toutefois, toute technique qui comprend des nuanceurs de modèle de nuanceur 4,1 ou les nouvelles fonctionnalités 10,1 doit utiliser un appareil 10,1.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de programmation pour Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 



