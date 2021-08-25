---
title: Appareils (graphiques Direct3D 11)
description: Cette section décrit les objets de contexte d’appareil et de périphérique Direct3D 11.
ms.assetid: 61d1ea92-e657-4931-8475-74a3123c72f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e77cfd255c43cc902f2583fe22575bef2567609f43b6f893984e99dec713532
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119851119"
---
# <a name="devices-direct3d-11-graphics"></a>Appareils (graphiques Direct3D 11)

Un appareil Direct3D alloue et détruit des objets, restitue des primitives et communique avec un pilote graphique et le matériel. Dans Direct3D 11, un appareil est séparé en objet d’appareil pour la création de ressources et d’un objet de contexte d’appareil, qui effectue le rendu. Cette section décrit les objets de contexte d’appareil et de périphérique Direct3D 11.

Les objets créés à partir d’un appareil ne peuvent pas être utilisés directement avec d’autres appareils. Utilisez une ressource partagée pour partager des données entre plusieurs appareils, avec la contrainte qu’un objet partagé ne peut être utilisé que par l’appareil qui l’a créé.


## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                                                                                         | Description                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Présentation d’un appareil dans Direct3D 11](overviews-direct3d-11-devices-intro.md)<br/>                                                                 | Le modèle objet Direct3D 11 sépare les fonctionnalités de création et de rendu des ressources dans un appareil et un ou plusieurs contextes. Cette séparation est conçue pour faciliter le multithread.<br/>                                                  |
| [Couches logicielles](overviews-direct3d-11-devices-layers.md)<br/>                                                                                        | Le runtime Direct3D 11 est construit avec des couches, en commençant par les fonctionnalités de base au cœur et en créant des fonctionnalités facultatives et d’assistance aux développeurs dans les couches externes. Cette section décrit les fonctionnalités de chaque couche.<br/> |
| [Limitations de la création d’appareils de déformation et de référence](overviews-direct3d-11-devices-limitations.md)<br/>                                                   | Certaines limitations existent pour la création de périphériques de déformation et de référence dans Direct3D 10,1 et Direct3D 11,0. Cette rubrique présente ces limitations.<br/>                                                                                              |
| [Direct3D 11 sur du matériel de niveau inférieur](overviews-direct3d-11-devices-downlevel.md)<br/>                                                                   | Cette section explique comment Direct3D 11 est conçu pour prendre en charge le matériel nouveau ou existant, de DirectX 9 à DirectX 11.<br/>                                                                                                             |
| [Utilisation des données de fonctionnalités Direct3D 11 pour compléter les niveaux de fonctionnalité Direct3D](using-direct3d-optional-features-to-supplement-direct3d-feature-levels.md)<br/> | Découvrez comment vérifier la prise en charge d’appareils pour les fonctionnalités facultatives, notamment les fonctionnalités qui ont été ajoutées dans les versions récentes de Windows.<br/>                                                                                                           |



 

## <a name="how-to-topics-about-devices"></a>Rubriques relatives aux appareils



| Rubrique                                                                                                                                                                                                                                                                                                    | Description                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <span id="How_To__Create_a_Reference_Device"></span><span id="how_to__create_a_reference_device"></span><span id="HOW_TO__CREATE_A_REFERENCE_DEVICE"></span>[Comment : créer un appareil de référence](overviews-direct3d-11-devices-create-ref.md)<br/>                                                 | Décrit comment créer un appareil de référence.<br/>                            |
| <span id="How_To__Create_a_WARP_Device"></span><span id="how_to__create_a_warp_device"></span><span id="HOW_TO__CREATE_A_WARP_DEVICE"></span>[Comment : créer un appareil WARP](overviews-direct3d-11-devices-create-warp.md)<br/>                                                                    | Décrit comment créer un appareil WARP.<br/>                                 |
| <span id="How_To__Create_a_Swap_Chain"></span><span id="how_to__create_a_swap_chain"></span><span id="HOW_TO__CREATE_A_SWAP_CHAIN"></span>[Comment : créer une chaîne de permutation](overviews-direct3d-11-devices-create-swap-chain.md)<br/>                                                                  | Décrit comment créer une chaîne de permutation.<br/>                                  |
| <span id="How_To__Enumerate_Adapters"></span><span id="how_to__enumerate_adapters"></span><span id="HOW_TO__ENUMERATE_ADAPTERS"></span>[Comment : énumérer des adaptateurs](overviews-direct3d-11-devices-enum.md)<br/>                                                                                   | Décrit comment énumérer les adaptateurs d’affichage physiques.<br/>              |
| <span id="How_To__Get_Adapter_Display_Modes"></span><span id="how_to__get_adapter_display_modes"></span><span id="HOW_TO__GET_ADAPTER_DISPLAY_MODES"></span>[Comment : obtenir les modes d’affichage de l’adaptateur](overviews-direct3d-11-devices-get-adapter-info.md)<br/>                                           | Décrit comment obtenir les fonctionnalités d’affichage prises en charge d’un adaptateur.<br/> |
| <span id="How_To__Create_a_Device_and_Immediate_Context"></span><span id="how_to__create_a_device_and_immediate_context"></span><span id="HOW_TO__CREATE_A_DEVICE_AND_IMMEDIATE_CONTEXT"></span>[Comment : créer un appareil et un contexte immédiat](overviews-direct3d-11-devices-initialize.md)<br/> | Décrit comment initialiser un appareil.<br/>                                  |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de programmation pour Direct3D 11](dx-graphics-overviews.md)
</dt> </dl>

 

 





