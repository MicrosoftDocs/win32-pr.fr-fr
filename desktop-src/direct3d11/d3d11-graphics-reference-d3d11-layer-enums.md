---
title: Énumérations de couche
description: Cette section contient des informations sur les énumérations de couche.
ms.assetid: 0fd0456b-2638-4b4c-8a34-a3e104a1a034
keywords:
- énumérations, couche Direct3D 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1e1cca3fa500a529930c8d0c39005697045d18b
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104971831"
---
# <a name="layer-enumerations"></a>Énumérations de couche

Cette section contient des informations sur les énumérations de couche.


## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                             | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Catégorie de message d3d11 \_**](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_message_category)<br/>                             | Catégories de messages de débogage. Cela permet d’identifier la catégorie d’un message lors de l’extraction d’un message avec [**ID3D11InfoQueue :: GetMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-getmessage) et lors de l’ajout d’un message avec [**ID3D11InfoQueue :: AddMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-addmessage). Lors de la création d’un [**filtre de file d’attente d’informations**](/windows/desktop/api/D3D11SDKLayers/ns-d3d11sdklayers-d3d11_info_queue_filter), ces valeurs peuvent être utilisées pour autoriser ou refuser les catégories de messages à traverser les filtres de stockage et de récupération.<br/> |
| [**\_ID de message d3d11 \_**](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_message_id)<br/>                                         | Déboguez les messages pour la configuration d’un filtre de file d’attente d’informations (consultez [**d3d11 \_ info \_ Queue \_ Filter**](/windows/desktop/api/D3D11SDKLayers/ns-d3d11sdklayers-d3d11_info_queue_filter)); Utilisez ces messages pour autoriser ou refuser les catégories de message à traverser les filtres de stockage et de récupération. Ces ID sont utilisés par des méthodes telles que [**ID3D11InfoQueue :: GetMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-getmessage) ou [**ID3D11InfoQueue :: AddMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-addmessage). <br/>                                                             |
| [**\_Gravité du message d3d11 \_**](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_message_severity)<br/>                             | Déboguez les niveaux de gravité des messages pour une file d’attente d’informations.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**\_Indicateurs d3d11 RLDO \_**](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_rldo_flags)<br/>                                         | Options de la quantité d’informations à signaler sur la durée de vie d’un objet appareil.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| [**\_Options de suivi du nuanceur d3d11 \_ \_**](/windows/win32/api/d3d11sdklayers/ne-d3d11sdklayers-d3d11_shader_tracking_options)<br/>              | Options qui spécifient comment effectuer le suivi du débogage du nuanceur.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**\_Type de \_ ressource de suivi du NUANCEur d3d11 \_ \_**](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_shader_tracking_resource_type)<br/> | Indique les types de ressources à suivre.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence de couche](d3d11-graphics-reference-d3d11-layer.md)
</dt> </dl>

 

 





