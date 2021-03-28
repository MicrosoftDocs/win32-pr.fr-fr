---
title: MultiThreading
description: Direct3D 11 implémente la prise en charge de la création et du rendu d’objets à l’aide de plusieurs threads.
ms.assetid: 1bf50927-268b-4471-b059-819adf2189a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a4de7ca3e7e00ffba0c728aef334f21efc18899
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197093"
---
# <a name="multithreading"></a>MultiThreading

Direct3D 11 implémente la prise en charge de la création et du rendu d’objets à l’aide de plusieurs threads.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                                                   | Description                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Introduction au multithreading dans Direct3D 11](overviews-direct3d-11-render-multi-thread-intro.md)<br/>         | Le multithreading est conçu pour améliorer les performances en effectuant un travail à l’aide d’un ou plusieurs threads en même temps. <br/>                                                                                                         |
| [Création d’objets avec multithread](overviews-direct3d-11-render-multi-thread-create.md)<br/>                  | Utilisez l’interface [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) pour créer des ressources et des objets, utilisez le [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) pour le [rendu](overviews-direct3d-11-render-multi-thread-render.md).<br/> |
| [Rendu immédiat et différé](overviews-direct3d-11-render-multi-thread-render.md)<br/>                     | Direct3D 11 prend en charge deux types de rendu : immédiat et différé. Les deux sont implémentés à l’aide de l’interface [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .<br/>                                                      |
| [Liste des commandes](overviews-direct3d-11-render-multi-thread-command-list.md)<br/>                                   | Une liste de commandes est une séquence de commandes GPU qui peut être enregistrée et lue. Une liste de commandes peut améliorer les performances en réduisant la quantité de surcharge générée par le Runtime.<br/>                                    |
| [Différences de threads entre les versions Direct3D](overviews-direct3d-11-render-multi-thread-differences.md)<br/> | De nombreux modèles de programmation multithread utilisent des primitives de synchronisation (telles que des mutex) pour créer des sections critiques et empêcher l’accès à du code par plusieurs threads à la fois.<br/>                       |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Procédure : vérifier la prise en charge des pilotes](overviews-direct3d-11-render-multi-thread-support.md)
</dt> <dt>

[Rendu](overviews-direct3d-11-render.md)
</dt> </dl>

 

 





