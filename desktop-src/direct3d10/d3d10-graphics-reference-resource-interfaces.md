---
description: 'Direct3D 10 définit un certain nombre d’interfaces pour les deux types de ressources de base : les mémoires tampons et les textures.'
ms.assetid: e53ca7ab-6ca5-4774-8a52-825b10c1a2ce
title: Interfaces de ressource (graphiques Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94eb7a0f2ce0b6792ccb98b95605f00504fbf239ee0cecf0846814d84566de9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119282819"
---
# <a name="resource-interfaces-direct3d-10-graphics"></a>Interfaces de ressource (graphiques Direct3D 10)

Direct3D 10 définit un certain nombre d’interfaces pour les deux types de ressources de base : les [mémoires tampons](d3d10-graphics-programming-guide-resources-types.md) et les textures.



| Interfaces                                           | Description                                          |
|------------------------------------------------------|------------------------------------------------------|
| [**Interface ID3D10Buffer**](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)       | Accède aux données de mémoire tampon.                                |
| [**Interface ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)   | Classe de base pour une ressource.                           |
| [**Interface ID3D10Texture1D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture1d) | Accède aux données dans une texture 1D ou un tableau de texture 1D. |
| [**Interface ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d) | Accède aux données dans une texture 2D ou un tableau de texture 2D  |
| [**Interface ID3D10Texture3D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture3d) | Accède aux données dans une texture 3D ou un tableau de texture 3D. |



 

Une application utilise une vue pour lier une ressource à une [étape de pipeline](d3d10-graphics-programming-guide-pipeline-stages.md). La [vue](d3d10-graphics-programming-guide-resources-access-views.md) définit comment la ressource est accessible pendant le rendu. L’API contient ces interfaces d’affichage.



| Interfaces                                                               | Description                                                                                                  |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**Interface ID3D10DepthStencilView**](/windows/desktop/api/D3D10/nn-d3d10-id3d10depthstencilview)       | Accède aux données dans une texture de [stencil de profondeur](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md) . |
| [**Interface ID3D10RenderTargetView**](/windows/desktop/api/D3D10/nn-d3d10-id3d10rendertargetview)       | Accède aux données d’une [cible de rendu](d3d10-graphics-programming-guide-resources-creating-textures.md).        |
| [**Interface ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)   | Accède aux données d’une ressource Shader dans Direct3D 10,0.                                                         |
| [**Interface ID3D10ShaderResourceView1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10shaderresourceview1) | Accède aux données d’une ressource Shader dans Direct3D 10,1.                                                         |
| [**Interface ID3D10View**](/windows/desktop/api/D3D10/nn-d3d10-id3d10view)                               | Classe de base pour une vue.                                                                                       |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence de ressource](d3d10-graphics-reference-resource.md)
</dt> </dl>

 

 
