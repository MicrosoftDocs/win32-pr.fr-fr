---
title: Nouveautés de Direct3D 12
description: Cette rubrique décrit la nouvelle documentation Direct3D 12 la plus significative disponible pour les différentes versions.
ms.assetid: 38F41E05-FECB-41DE-8D30-09733FBEAC48
ms.localizationpriority: high
ms.topic: article
ms.date: 12/05/2019
ms.openlocfilehash: ec3ecc9e68fc4711def2c364793eca32804d8d04
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548485"
---
# <a name="whats-new-in-direct3d-12"></a>Nouveautés de Direct3D 12

Cette rubrique décrit la nouvelle documentation Direct3D 12 la plus significative disponible pour les différentes versions.

Pour plus d’informations sur l’obtention et l’installation de Direct3D, consultez Configuration de l' [environnement de programmation Direct3D 12](./directx-12-programming-environment-set-up.md).

## <a name="direct3d-12-on-windows-7"></a>Direct3D 12 sur Windows 7

- [Direct3D 12 sur Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/) est désormais disponible pour les développeurs.

## <a name="windows-10-may-2019-update"></a>Mise à jour de Windows 10 de mai 2019

Ces fonctionnalités et API ont été ajoutées ou mises à jour pour Windows 10, version 1903 (10,0 ; Build 18362) &mdash; également connu sous le nom de Windows 10 mai 2019 Update.

- [VRS (variable-rate Shading)](./vrs.md). Vous permet d’allouer des performances de rendu/puissance à des vitesses qui varient d’un rendu à l’autre.
- [Modèle de nuanceur HLSL 6,4](../direct3dhlsl/hlsl-shader-model-6-4-features-for-direct3d-12.md). Décrit les Machine Learning intrinsèques ajoutés au modèle de nuanceur HLSL 6,4.
- Énumération [**D3D12_DRED_VERSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dred_version) . Définit des constantes qui spécifient une version des données étendues supprimées par l’appareil (ordinateur).
- Structure [**D3D12_FEATURE_DATA_D3D12_OPTIONS6**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options6) . Indique le niveau de prise en charge fourni par l’adaptateur pour les commandes de commande.
- Structure [**D3D12_FEATURE_DATA_QUERY_META_COMMAND**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_query_meta_command) . Indique le niveau de prise en charge fourni par l’adaptateur pour les commandes de commande.
- Énumération [**D3D12_VARIABLE_SHADING_RATE_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier) . Définit des constantes qui spécifient un niveau de taux d’ombrage (pour l’ombrage à taux variable ou VRS).
- Interface [**ID3D12Device6**](/windows/win32/api/d3d12/nn-d3d12-id3d12device6) et ses méthodes. Utilisé pour définir le mode des optimisations du traitement en arrière-plan du pilote. Voir aussi [optimisations du nuanceur d’arrière-plan](https://devblogs.microsoft.com/directx/background-shader-optimizations/).
- Interface [**ID3D12DeviceRemovedExtendedData**](/windows/win32/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddata) et ses méthodes. Fournit l’accès au moment de l’exécution aux données de données étendues supprimées (ordinateur) de l’appareil.
- Interface [**ID3D12DeviceRemovedExtendedDataSettings**](/windows/win32/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddatasettings) et ses méthodes. Contrôle les paramètres de données étendus (ordinateur) supprimés du périphérique.
- Interface [**D3D12GraphicsCommandList5**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist5) et ses méthodes. Prise en charge de l’ombrage à taux variable (VRS).

L’énumération [**D3D_SHADER_MODEL**](/windows/win32/api/d3d12/ne-d3d12-d3d_shader_model) a été mise à jour avec l’ajout de la constante **D3D_SHADER_MODEL_6_5** (fonctionnalité de niveau expérimental).

L’énumération [**D3D12_COMMAND_LIST_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) a été mise à jour avec l’ajout de la constante **D3D12_COMMAND_LIST_TYPE_VIDEO_ENCODE** .

L’énumération [**D3D12_FEATURE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_feature) a été mise à jour avec l’ajout des constantes **D3D12_FEATURE_D3D12_OPTIONS6** et **D3D12_FEATURE_QUERY_META_COMMAND** .

L’énumération [**D3D12_RESOURCE_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) a été mise à jour avec l’ajout de la constante **D3D12_RESOURCE_STATE_SHADING_RATE_SOURCE** .

## <a name="windows-10-version-1809"></a>Windows 10, version 1809

Ces fonctionnalités et API ont été ajoutées ou mises à jour pour Windows 10, version 1809 (10,0 ; Build 17763) &mdash; également connu sous le nom de Windows 10 octobre 2018 Update.

- [Direct3D 12 Raytracing](./direct3d-12-raytracing.md)
- [Passes de rendu Direct3D 12](./direct3d-12-render-passes.md)

## <a name="windows-10-version-1709"></a>Windows 10, version 1709

Ces interfaces ont été ajoutées à la documentation Direct3D pour Windows 10, version 1709.

-   [**ID3D12Fence1**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence1) étend les fonctionnalités de création de clôtures en prenant en charge la récupération des indicateurs passés pour créer la clôture.
-   [**ID3D12GraphicsCommandList2**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist2) étend la liste des commandes graphiques disponibles en prenant en charge l’écriture directe de valeurs immédiates dans une mémoire tampon.
-   [**ID3D12Device3**](/windows/win32/api/d3d12/nn-d3d12-id3d12device3) étend la fonctionnalité de carte virtuelle en créant des tas de diagnostic à usage spécial dans la mémoire système qui persistent même en cas de défaillance du GPU ou de l’appareil.

L’énumération du [**\_ \_ modèle de nuanceur D3D**](/windows/win32/api/d3d12/ne-d3d12-d3d_shader_model) a une nouvelle valeur de **modèle de \_ nuanceur D3D \_ \_ 6 \_ 1** ajoutée pour décrire le modèle de nuanceur 6,1.

L’énumération des [**\_ fonctionnalités D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_feature) a également les nouvelles **\_ fonctionnalités D3D12 \_ D3D12 \_ OPTIONS3** et **D3D12 \_ Feature des \_ \_ tas existants** . Comme leur nom l’indique, ces valeurs vous permettent de vérifier d’autres options directement Direct3D 12 et de vérifier la prise en charge des tas existants.

## <a name="windows-10-version-1703"></a>Windows 10 version 1703

Ces rubriques ont été ajoutées à la documentation Direct3D pour Windows 10, version 1703.

-   La méthode [**ID3D12Device2 :: CreatePipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device2-createpipelinestate) et la structure DESC du flux d' [**\_ \_ état \_ \_ du pipeline D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc) représentent une méthode nouvelle et plus fiable pour créer des objets PSO et unifie les inteface pour la création de graphiques et de pipelines de calcul.
-   La méthode [**ID3D12Device1 :: CreatePipelineLibrary1**](https://www.bing.com/search?q=**ID3D12Device1::CreatePipelineLibrary1**) développe l’interface de la bibliothèque de pipelines pour accepter les objets PSO créées avec la nouvelle structure d' [**État de \_ \_ \_ flux \_ de pipeline D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc) unifiée.
-   La fonction [**D3D12EnableExperimentalFeatures**](/windows/win32/api/d3d12/nf-d3d12-d3d12enableexperimentalfeatures) permet aux développeurs d’expérimenter certaines fonctionnalités de développement à l’aide d’un ordinateur en mode développeur.
-   Il existe cinq nouvelles interfaces (reportez-vous à la [hiérarchie d’interface](interface-hierarchy.md)) :
    -   [**ID3D12GraphicsCommandList1**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist1)
    -   [**ID3D12PipelineLibrary1**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinelibrary1)
    -   [**ID3D12Device2**](/windows/win32/api/d3d12/nn-d3d12-id3d12device2)
    -   [**ID3D12Debug2**](/windows/win32/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug2)
    -   [**ID3D12Tools**](/windows/win32/api/d3d12/nn-d3d12-id3d12tools)
-   Reportez-vous à la [vue d’ensemble du nuancier HLSL Model 6,0](../direct3dhlsl/hlsl-shader-model-6-0-features-for-direct3d-12.md), qui décrit les opérations intrinsèques Wave pour les nuanceurs de calcul et de pixel multithread.
-   L’utilisation de [**ID3D12Device :: SetStablePowerState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate) a changé.
-   Certaines nouvelles fonctionnalités de Direct3D 11 sont décrites dans [fonctionnalités direct3d 11,4](../direct3d11/direct3d-11-4-features.md).
-   [**AtomicCopyBufferUINT**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint) et [**AtomicCopyBufferUINT64**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint64) activent **le verrouillage** à la fin pour réduire la latence pervieved.
-   [**ID3D12Device2 :: CreatePipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device2-createpipelinestate) et [**OMSetDepthBounds**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-omsetdepthbounds) permettent **un test des limites de profondeur** sur le matériel pris en charge.
-   [**ResolveSubresourceRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-resolvesubresourceregion) permet une **résolution partielle** des sous-ressources afin d’optimiser les performances.
-   [**SetSamplePositions**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-setsamplepositions) permet d’avoir des **exemples de positions à programmer** sur le matériel pris en charge.

## <a name="november-2016-documentation-update"></a>Mise à jour de la documentation de novembre 2016

-   Révision des notes pour [**ID3D12GraphicsCommandList ::D iscardresource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource).
-   Clarification de « l’état d’atténuation à commun » (voir [utilisation de barrières de ressources pour synchroniser les États des ressources dans Direct3D 12](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md)).
-   Le fichier d’en-tête D3dx12. h, référencé dans les [structures et fonctions d’assistance pour D3D12](helper-structures-and-functions-for-d3d12.md), peut être téléchargé directement à partir de [la bibliothèque d’assistance D3D12](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Libraries/D3DX12).

## <a name="august-2016-documentation-update-2"></a>Documentation de 2016 août Update 2

-   Une nouvelle section de guide intitulée [compréhension de la couche de débogage D3D12](understanding-the-d3d12-debug-layer.md).

    Trois nouvelles interfaces de couche de débogage (en mode Aperçu) sont décrites : [**ID3D12Debug1**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug1), [**ID3D12DebugCommandList1**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist1), [**ID3D12DebugDevice1**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice1).

## <a name="august-2016-documentation-update-1"></a>Mise à jour 1 de la documentation d’août 2016

-   Révision de [l’utilisation de barrières de ressources pour synchroniser les États des ressources dans Direct3D 12](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md).
-   Révision de [l’accès aux ressources de plusieurs files d’attente](./user-mode-heap-synchronization.md#multi-queue-resource-access).

## <a name="windows-10-version-1607"></a>Windows 10, version 1607

Ces rubriques ont été ajoutées à la documentation Direct3D pour Windows 10, version 1607.

-   [Signature racine Version 1,1](root-signature-version-1-1.md) : vue d’ensemble des signatures racines mises à jour, ce qui permet aux applications de spécifier la façon dont les descripteurs statiques ou volatiles et les données sont, ce qui peut aider les optimisations des pilotes graphiques.
-   La méthode [**ID3D12Device1 :: CreatePipelineLibrary**](/windows/win32/api/d3d12/nf-d3d12-id3d12device1-createpipelinelibrary) décrit les avantages de la création d’une bibliothèque de pipeline.
-   Il existe trois nouvelles interfaces (reportez-vous à la [hiérarchie d’interface](interface-hierarchy.md)) :
    -   [**ID3D12PipelineLibrary**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinelibrary)
    -   [**ID3D12Device1**](/windows/win32/api/d3d12/nn-d3d12-id3d12device1)
    -   [**ID3D12VersionedRootSignatureDeserializer**](/windows/win32/api/d3d12/nn-d3d12-id3d12versionedrootsignaturedeserializer)
-   Reportez-vous à la [vue d’ensemble du nuancier HLSL Model 6,0](../direct3dhlsl/hlsl-shader-model-6-0-features-for-direct3d-12.md), qui décrit les opérations intrinsèques Wave pour les nuanceurs de calcul et de pixel multithread.
-   L’utilisation de [**ID3D12Device :: SetStablePowerState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate) a changé.
-   Certaines nouvelles fonctionnalités de Direct3D 11 sont décrites dans [fonctionnalités direct3d 11,4](../direct3d11/direct3d-11-4-features.md).
-   La plage des bibliothèques prises en charge pour Direct3D 12 a été mise à jour, reportez-vous à la section **Outils et bibliothèques pris en charge** de la configuration de l' [environnement de programmation Direct3D 12](directx-12-programming-environment-set-up.md).
-   [Utilisation de DirectX avec des écrans à haute gamme dynamique et une couleur avancée](../direct3darticles/high-dynamic-range.md)
-   [Affichage du taux d’actualisation des variables](../direct3ddxgi/variable-refresh-rate-displays.md)
-   [Améliorations de DXGI 1,5](../direct3ddxgi/dxgi-1-5-improvements.md)

## <a name="related-topics"></a>Rubriques connexes

* [Guide de programmation Direct3D 12](directx-12-programming-guide.md)