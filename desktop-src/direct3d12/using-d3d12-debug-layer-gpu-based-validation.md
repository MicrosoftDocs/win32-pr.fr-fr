---
title: Validation basée sur GPU et couche de débogage Direct3D 12
description: Cette rubrique explique comment tirer le meilleur parti de la couche de débogage Direct3D 12. La validation basée sur GPU (GBV) active des scénarios de validation sur la chronologie GPU qui ne sont pas possibles lors des appels d’API sur le processeur.
ms.assetid: 01D1F94F-4DD4-4781-86EF-6C639E8B1069
ms.localizationpriority: high
ms.topic: article
ms.date: 02/12/2019
ms.openlocfilehash: 3160df3faf994df2abf9cf878088e84564bb5fe1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012844"
---
# <a name="gpu-based-validation-and-the-direct3d-12-debug-layer"></a>Validation basée sur GPU et couche de débogage Direct3D 12

Cette rubrique explique comment tirer le meilleur parti de la couche de débogage Direct3D 12. La validation basée sur GPU (GBV) active des scénarios de validation sur la chronologie GPU qui ne sont pas possibles lors des appels d’API sur le processeur. GBV est disponible à partir de la mise à jour anniversaire des outils graphics pour Windows 10.

## <a name="purpose-of-gpu-based-validation"></a>Objectif de la validation basée sur GPU

La validation basée sur GPU permet d’identifier les erreurs suivantes :

- Utilisation de descripteurs non initialisés ou incompatibles dans un nuanceur.
- Utilisation de descripteurs référençant les ressources supprimées dans un nuanceur.
- Validation des États des ressources promues et de la dégradation de l’état des ressources.
- Indexation au-delà de la fin du tas du descripteur dans un nuanceur.
- Accès du nuanceur des ressources dans un État incompatible.
- Utilisation d’échantillonneurs non initialisés ou incompatibles dans un nuanceur.

GBV fonctionne en créant des nuanceurs corrigés qui ont une validation ajoutée directement au nuanceur. Les nuanceurs corrigés inspectent les arguments racine et les ressources accessibles pendant l’exécution du nuanceur et signalent les erreurs dans un tampon de journal. GBV injecte également des opérations supplémentaires et des appels de répartition dans les listes de commandes de l’application pour valider et suivre les modifications apportées à l’état des ressources imposées par la liste de commandes sur la chronologie du GPU.

Comme GBV nécessite la possibilité d’exécuter des nuanceurs, les listes de commandes de copie sont émulées par une liste de commandes de calcul. Cela peut modifier la manière dont le matériel effectue des copies même si le résultat final ne doit pas être modifié. L’application percevra toujours qu’il s’agit de listes de commandes de copie et que la couche de débogage les validera comme telle.

## <a name="turning-on-gpu-based-validation"></a>Activation de la validation basée sur GPU

GBV peut être forcé à l’aide du panneau de configuration DirectX (DXCPL) en forçant la couche de débogage Direct3D 12 et en forçant en outre la validation basée sur GPU (nouvel onglet dans le panneau de configuration). Une fois activé, GBV reste activé jusqu’à la sortie de l’appareil Direct3D 12. Sinon, GBV peut être activé par programme avant de créer l’appareil Direct3D 12 :

```cpp
void EnableShaderBasedValidation()
{
    CComPtr<ID3D12Debug> spDebugController0;
    CComPtr<ID3D12Debug1> spDebugController1;
    VERIFY(D3D12GetDebugInterface(IID_PPV_ARGS(&spDebugController0)));
    VERIFY(spDebugController0->QueryInterface(IID_PPV_ARGS(&spDebugController1)));
    spDebugController1->SetEnableGPUBasedValidation(true);
}
```

## <a name="recommended-usage"></a>Utilisation recommandée

En règle générale, vous devez exécuter votre code avec la couche de débogage activée la plupart du temps. Toutefois, GBV peut ralentir considérablement les choses. Les développeurs peuvent envisager d’activer GBV avec des jeux de données plus petits (par exemple, des démonstrations de moteur ou des petits niveaux de jeu avec moins d’PSO et des ressources) ou lors de la mise en place d’une application précoce pour réduire les problèmes de performances. Avec un contenu de plus grande taille, envisagez d’activer GBV sur une ou deux machines de test dans un test nocturne.

## <a name="debug-output"></a>Sortie de débogage

GBV produit une sortie de débogage après qu’un appel à [**ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) termine l’exécution sur le GPU. Étant donné qu’il s’agit de la chronologie du GPU, la sortie de débogage peut être asynchrone avec une autre validation de la chronologie de l’UC. Les développeurs d’applications peuvent souhaiter injecter leur propre attente-après-exécution pour synchroniser la sortie de débogage.

La sortie de GBV identifie l’endroit où une erreur s’est produite dans un nuanceur, ainsi que le nombre actuel de dessins/dispatchs et les identités des objets associés (par exemple, liste de commandes, file d’attente, PSO, etc.).

## <a name="example-debug-message"></a>Exemple de message de débogage

Le message d’erreur suivant indique qu’une ressource nommée « main Color buffer » a été accédée dans un nuanceur en tant que ressource de nuanceur, mais qu’elle était dans l’état d’accès non ordonné lorsque le nuanceur s’exécutait sur le GPU. Des informations supplémentaires, telles que l’emplacement dans la source du nuanceur, le nom de la liste de commandes et le nombre de dessins (index de dessin), ainsi que les noms des objets d’interface D3D associés sont également fournis.

```cmd
D3D12 ERROR: Incompatible resource state: Resource: 0x0000016F61A6EA80:'Main Color Buffer', 
Subresource Index: [0], 
Descriptor heap index: [0], 
Binding Type In Descriptor: SRV, 
Resource State: D3D12_RESOURCE_STATE_UNORDERED_ACCESS(0x8), 
Shader Stage: PIXEL, 
Root Parameter Index: [0], 
Draw Index: [0], 
Shader Code: E:\FileShare\MiniEngine_GitHub_160128\MiniEngine_GitHub\Core\Shaders\SharpeningUpsamplePS.hlsl(37,2-59), 
Asm Instruction Range: [0x138-0x16b], 
Asm Operand Index: [3], 
Command List: 0x0000016F6F75F740:'CommandList', SRV/UAV/CBV Descriptor Heap: 0x0000016F6F76F280:'Unnamed ID3D12DescriptorHeap Object', 
Sampler Descriptor Heap: <not set>, 
Pipeline State: 0x0000016F572C89F0:'Unnamed ID3D12PipelineState Object',  
[ EXECUTION ERROR #942: GPU_BASED_VALIDATION_INCOMPATIBLE_RESOURCE_STATE]
```

## <a name="debug-layer-apis"></a>API de couche de débogage

Pour activer la couche de débogage, appelez [**EnableDebugLayer**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug-enabledebuglayer).

Pour activer la validation basée sur GPU, appelez [**SetEnableGPUBasedValidation**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug1-setenablegpubasedvalidation)et reportez-vous aux méthodes des interfaces suivantes :

- [**ID3D12Debug1**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug1)
- [**ID3D12DebugCommandList1**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist1)
- [**ID3D12DebugDevice1**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice1)

Reportez-vous aux énumérations et structures suivantes :

- [**\_Type de \_ \_ paramètre de liste de commandes de débogage D3D12 \_ \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_command_list_parameter_type)
- [**TYPE de paramètre de l' \_ appareil de débogage D3D12 \_ \_ \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_device_parameter_type)
- [**Indicateurs de création de l' \_ \_ \_ État du \_ pipeline de validation \_ basé \_ sur \_ GPU D3D12**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_pipeline_state_create_flags)
- [**\_Mode de \_ \_ Correction du \_ nuanceur de validation basé \_ sur GPU D3D12 \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_shader_patch_mode)
- [**\_Liste de commandes de débogage D3D12 \_ \_ \_ \_ \_ paramètres de validation basés sur GPU \_**](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_command_list_gpu_based_validation_settings)
- [**D3D12 \_ déboguer les \_ \_ \_ paramètres de validation basés sur GPU \_ \_**](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_device_gpu_based_validation_settings)

## <a name="related-topics"></a>Rubriques connexes

* [Fonctionnement de la couche de débogage Direct3D 12](understanding-the-d3d12-debug-layer.md)
