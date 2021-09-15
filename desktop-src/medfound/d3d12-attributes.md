---
description: Attributs Direct3D 12
title: Attributs Direct3D 12
ms.topic: article
ms.date: 08/13/2021
ms.openlocfilehash: 646d2cea8923286714982a3e083eade65f664be7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127523716"
---
# <a name="direct3d-12-attributes"></a>Attributs Direct3D 12

Les attributs suivants peuvent être utilisés pour configurer les ressources de Media Foundation Direct3D 12.



| Attribut                                                                                                         | Description                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [MF_MT_D3D_RESOURCE_VERSION](mf-mt-d3d-resource-version.md) | Spécifie la version Direct3D des ressources stockées dans le flux de données associé au type de média. |
| [MF_MT_D3D12_CPU_READBACK](mf-mt-d3d12-cpu-readback.md) | Indique si l’accès au processeur est requis pour les ressources Direct3D associées. |
| [MF_MT_D3D12_RESOURCE_FLAG_ALLOW_CROSS_ADAPTER](mf-mt-d3d12-resource-flag-allow-cross-adapter.md) | Indique si les ressources du flux peuvent être utilisées pour les données entre les adaptateurs.  |
| [MF_MT_D3D12_RESOURCE_FLAG_ALLOW_DEPTH_STENCIL](mf-mt-d3d12-resource-flag-allow-depth-stencil.md) | Indique si la vue du stencil de profondeur peut être créée pour les ressources Direct3D dans le flux associé au type de média. |
| [MF_MT_D3D12_RESOURCE_FLAG_ALLOW_RENDER_TARGET](mf-mt-d3d12-resource-flag-allow-render-target.md) | Indique si une vue de cible de rendu peut être créée pour les ressources Direct3D dans le flux associé au type de média.  |
| [MF_MT_D3D12_RESOURCE_FLAG_ALLOW_SIMULTANEOUS_ACCESS](mf-mt-d3d12-resource-flag-allow-simultaneous-access.md) | Indique si les ressources Direct3D dans le flux peuvent être accessibles simultanément par plusieurs files d’attente de commandes différentes.  |
| [MF_MT_D3D12_RESOURCE_FLAG_ALLOW_UNORDERED_ACCESS](mf-mt-d3d12-resource-flag-allow-unordered-access.md) | Indique si une vue d’accès non ordonnée peut être créée pour les ressources Direct3D dans le flux associé au type de média. |
| [MF_MT_D3D12_RESOURCE_FLAG_DENY_SHADER_RESOURCE](mf-mt-d3d12-resource-flag-deny-shader-resource.md) | Indique si la création d’une vue de ressource de nuanceur n’est pas autorisée pour les ressources Direct3D dans le flux associé au type de média.  |
| [MF_MT_D3D12_TEXTURE_LAYOUT](mf-mt-d3d12-texture-layout.md) | Indique les options de mise en page de texture qui ont été utilisées pour créer les ressources Direct3D associées.  |
| [MF_SA_D3D12_CLEAR_VALUE](mf-sa-d3d12-clear-value.md) | Contient un objet BLOB avec les informations utilisées pour optimiser les opérations d’effacement des ressources Direct3D dans le flux. |
| [MF_SA_D3D12_HEAP_FLAGS](mf-sa-d3d12-heap-flags.md) | Contient une valeur qui spécifie les options de tas utilisées pour les ressources Direct3D dans le flux. |
| [MF_SA_D3D12_HEAP_TYPE](mf-sa-d3d12-heap-type.md)  | Contient une valeur qui spécifie le type de tas utilisé pour les ressources Direct3D dans le flux. |




 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Attributs Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[Convertisseur vidéo amélioré](enhanced-video-renderer.md)
</dt> </dl>

 

 



