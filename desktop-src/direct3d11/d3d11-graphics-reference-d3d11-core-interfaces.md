---
title: Interfaces principales Direct3D 11
description: Cette section contient des informations sur les interfaces de base.
ms.assetid: e96804db-0987-49ca-b1b1-321f36c13024
keywords:
- interfaces, Direct3D 11 Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2485e633158d3eb1f8448249812eb6699b37a6ea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127526144"
---
# <a name="direct3d-11-core-interfaces"></a>Interfaces principales Direct3D 11

Cette section contient des informations sur les interfaces de base.

## <a name="in-this-section"></a>Contenu de cette section




| Rubrique | Description | 
|-------|-------------|
| <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11asynchronous"><strong>ID3D11Asynchronous</strong></a><br /> | Cette interface encapsule les méthodes de récupération des données du GPU de manière asynchrone.<br /> | 
| <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate"><strong>ID3D11BlendState</strong></a><br /> | L’interface d’état de fusion contient une description de l’état de fusion que vous pouvez lier à l' <a href="d3d10-graphics-programming-guide-output-merger-stage.md">étape de fusion de sortie</a>.<br /> | 
| <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11blendstate1"><strong>ID3D11BlendState1</strong></a><br /> | L’interface d’état de fusion contient une description de l’état de fusion que vous pouvez lier à l' <a href="d3d10-graphics-programming-guide-output-merger-stage.md">étape de fusion de sortie</a>. Cette interface d’état de fusion prend en charge les opérations logiques, ainsi que les opérations de fusion.<br /> | 
| <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist"><strong>ID3D11CommandList</strong></a><br /> | L’interface <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist"><strong>ID3D11CommandList</strong></a> encapsule une liste de commandes Graphics pour la lecture.<br /> | 
| <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11counter"><strong>ID3D11Counter</strong></a><br /> | Cette interface encapsule des méthodes pour mesurer les performances du GPU.<br /> | 
| <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate"><strong>ID3D11DepthStencilState</strong></a><br /> | L’interface Depth-stencil-State contient une description de l’état du gabarit de profondeur que vous pouvez lier à l' <a href="d3d10-graphics-programming-guide-output-merger-stage.md">étape de fusion de sortie</a>.<br /> | 
| <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a><br /> | L’interface d’appareil représente un adaptateur virtuel ; Il est utilisé pour créer des ressources.<br /> | 
| <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a><br /> | L’interface d’appareil représente un adaptateur virtuel ; Il est utilisé pour créer des ressources. <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a> ajoute de nouvelles méthodes à celles de <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a>.<br /> | 
| <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a><br /> | L’interface d’appareil représente un adaptateur virtuel ; Il est utilisé pour créer des ressources. <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a> ajoute de nouvelles méthodes à celles de <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a>.<br /> | 
| <a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a><br /> | L’interface d’appareil représente un adaptateur virtuel ; Il est utilisé pour créer des ressources. <a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a> ajoute de nouvelles méthodes à celles de <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a>.<br /> | 
| <a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a><br /> | L’interface d’appareil représente un adaptateur virtuel ; Il est utilisé pour créer des ressources. <a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a> ajoute de nouvelles méthodes à celles de <a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a>, telles que <strong>RegisterDeviceRemovedEvent</strong> et <strong>UnregisterDeviceRemoved</strong>. <br /> | 
| <a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5"><strong>ID3D11Device5</strong></a><br /> | L’interface d’appareil représente un adaptateur virtuel ; Il est utilisé pour créer des ressources. <a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5"><strong>ID3D11Device5</strong></a> ajoute de nouvelles méthodes à celles de <a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a>.<br /> | 
| <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a><br /> | Une interface enfant d’appareil accède aux données utilisées par un appareil.<br /> | 
| <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a><br /> | L’interface <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a> représente un contexte de périphérique qui génère des commandes de rendu.<br /><blockquote>[!Note]<br />La dernière version de cette interface est <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceContext4</strong></a> introduite dans le Windows 10 Creators Update. les Applications ciblant Windows 10 Creators Update doivent utiliser l’interface <strong>ID3D11DeviceContext4</strong> au lieu de <strong>ID3D11Device</strong>.</blockquote><br /> | 
| <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a><br /> | L’interface de contexte de périphérique représente un contexte de périphérique (Device Context). Il est utilisé pour restituer des commandes. <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a> ajoute de nouvelles méthodes à celles de <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a>.<br /> | 
| <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2</strong></a><br /> | L’interface de contexte de périphérique représente un contexte de périphérique (Device Context). Il est utilisé pour restituer des commandes. <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2</strong></a> ajoute de nouvelles méthodes à celles de <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a>.<br /> | 
| <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceContext3</strong></a><br /> | L’interface de contexte de périphérique représente un contexte de périphérique (Device Context). Il est utilisé pour restituer des commandes. <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceContext3</strong></a> ajoute de nouvelles méthodes à celles de <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2</strong></a>. <br /> | 
| <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceContext4</strong></a><br /> | L’interface de contexte de périphérique représente un contexte de périphérique (Device Context). Il est utilisé pour restituer des commandes. <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceContext4</strong></a> ajoute de nouvelles méthodes à celles de <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceContext3</strong></a>.<br /> | 
| <a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate"><strong>ID3DDeviceContextState</strong></a><br /> | L’interface <a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate"><strong>ID3DDeviceContextState</strong></a> représente un objet d’état de contexte qui contient les informations sur l’État et le comportement d’un périphérique Microsoft Direct3D.<br /> | 
| <a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11fence"><strong>ID3D11Fence</strong></a><br /> | Représente une clôture, un objet utilisé pour la synchronisation de l’UC et un ou plusieurs GPU.<br /> | 
| <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11inputlayout"><strong>ID3D11InputLayout</strong></a><br /> | Une interface de disposition d’entrée contient une définition de la façon d’alimenter les données de vertex disposées en mémoire dans l' <a href="d3d10-graphics-programming-guide-input-assembler-stage.md">étape assembleur d’entrée</a> du <a href="overviews-direct3d-11-graphics-pipeline.md">pipeline Graphics</a>.<br /> | 
| <a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11multithread"><strong>ID3D11Multithread</strong></a><br /> | Fournit une protection de thread pour les sections critiques d’une application multithread.<br /> | 
| <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11predicate"><strong>ID3D11Predicate</strong></a><br /> | Une interface de prédicat détermine si la géométrie doit être traitée en fonction des résultats d’un appel de dessin précédent.<br /> | 
| <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11query"><strong>ID3D11Query</strong></a><br /> | Une interface de requête interroge les informations du GPU.<br /> | 
| <a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11query1"><strong>ID3D11Query1</strong></a><br /> | Représente un objet de requête pour interroger des informations à partir de l’unité de traitement graphique (GPU).<br /> | 
| <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate"><strong>ID3D11RasterizerState</strong></a><br /> | L’interface d’État du rastériseur contient une description de l’état du rastériseur que vous pouvez lier à l' <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">étape de rastérisation</a>.<br /> | 
| <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11rasterizerstate1"><strong>ID3D11RasterizerState1</strong></a><br /> | L’interface d’État du rastériseur contient une description de l’état du rastériseur que vous pouvez lier à l' <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">étape de rastérisation</a>. Cette interface de l’état de rastériseur prend en charge le nombre d’échantillons forcés.<br /> | 
| <a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11rasterizerstate2"><strong>ID3D11RasterizerState2</strong></a><br /> | L’interface d’État du rastériseur contient une description de l’état du rastériseur que vous pouvez lier à l' <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">étape de rastérisation</a>. Cette interface d’État du rastériseur prend en charge le nombre d’échantillons forcés et le mode de pixellisation conservateur.<br /> | 
| <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate"><strong>ID3D11SamplerState</strong></a><br /> | L’interface d’échantillonnage-état contient une description de l’état de l’échantillonneur que vous pouvez lier à toute étape de nuanceur du <a href="overviews-direct3d-11-graphics-pipeline.md">pipeline</a> pour référencer les opérations d’exemple de texture.<br /> | 




 

Direct3D 11 implémente des interfaces pour :

-   [Ressources](d3d11-graphics-reference-resource-interfaces.md)
-   [Nuanceurs](d3d11-graphics-reference-d3d11-shader-interfaces.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence principale](d3d11-graphics-reference-d3d11-core.md)
</dt> </dl>

