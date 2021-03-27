---
title: Interfaces de ressource (graphiques Direct3D 11)
description: Il existe plusieurs interfaces pour les deux types de mémoire tampons et textures de ressources.
ms.assetid: 8e40573a-b186-41ec-b2ff-81279d77bd3a
keywords:
- interfaces, ressource Direct3D 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4d8f01e8d485fcdf575e8aea1a5beeb2184946b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739613"
---
# <a name="resource-interfaces-direct3d-11-graphics"></a>Interfaces de ressource (graphiques Direct3D 11)

Il existe plusieurs interfaces pour les deux types de ressources de base : les tampons et les textures. Il existe également des interfaces pour les vues des ressources.

Une application utilise une vue pour lier une ressource à une étape de pipeline. La vue définit comment la ressource est accessible pendant le rendu. Cette section décrit les interfaces de vue.


## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                       | Description                                                                                                                                                                                            |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)<br/>                             | Une interface de mémoire tampon accède à une ressource de mémoire tampon, qui est une mémoire non structurée. Les mémoires tampons stockent généralement des données de vertex ou d’index.<br/>                                                                  |
| [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)<br/>         | Une interface Depth-View-View accède à une ressource de texture pendant un test de stencil de profondeur.<br/>                                                                                                    |
| [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)<br/>         | Une interface Render-Target-View identifie les sous-ressources de la cible de rendu qui sont accessibles pendant le rendu.<br/>                                                                             |
| [**ID3D11RenderTargetView1**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11rendertargetview1)<br/>       | Une interface Render-Target-View représente les sous-ressources de la cible de rendu qui sont accessibles pendant le rendu.<br/>                                                                             |
| [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)<br/>                         | Une interface de ressource fournit des actions courantes sur toutes les ressources.<br/>                                                                                                                              |
| [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)<br/>     | Une interface Shader-Resource-View spécifie les sous-ressources auxquelles un nuanceur peut accéder pendant le rendu. Les exemples de ressources de nuanceur incluent une mémoire tampon constante, une mémoire tampon de texture et une texture.<br/>  |
| [**ID3D11ShaderResourceView1**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11shaderresourceview1)<br/>   | Une interface Shader-Resource-View représente les sous-ressources auxquelles un nuanceur peut accéder pendant le rendu. Les exemples de ressources de nuanceur incluent une mémoire tampon constante, une mémoire tampon de texture et une texture.<br/> |
| [**ID3D11Texture1D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture1d)<br/>                       | Une interface de texture 1D accède aux données texels, qui est une mémoire structurée.<br/>                                                                                                                     |
| [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)<br/>                       | Une interface de texture 2D gère les données texels, qui est une mémoire structurée.<br/>                                                                                                                      |
| [**ID3D11Texture2D1**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11texture2d1)<br/>                     | Une interface de texture 2D représente des données texels, qui est une mémoire structurée.<br/>                                                                                                                   |
| [**ID3D11Texture3D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture3d)<br/>                       | Une interface de texture 3D accède aux données texels, qui est une mémoire structurée.<br/>                                                                                                                     |
| [**ID3D11Texture3D1**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11texture3d1)<br/>                     | Une interface de texture 3D représente des données texels, qui est une mémoire structurée.<br/>                                                                                                                   |
| [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)<br/>   | Une interface de vue spécifie les parties d’une ressource auxquelles le pipeline peut accéder pendant le rendu.<br/>                                                                                                |
| [**ID3D11UnorderedAccessView1**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11unorderedaccessview1)<br/> | Une interface d’affichage d’accès non ordonnée représente les parties d’une ressource auxquelles le pipeline peut accéder pendant le rendu.<br/>                                                                             |
| [**ID3D11View**](/windows/desktop/api/D3D11/nn-d3d11-id3d11view)<br/>                                 | Une interface de vue spécifie les parties d’une ressource auxquelles le pipeline peut accéder pendant le rendu.<br/>                                                                                                |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence de ressource](d3d11-graphics-reference-resource.md)
</dt> </dl>

 

 





