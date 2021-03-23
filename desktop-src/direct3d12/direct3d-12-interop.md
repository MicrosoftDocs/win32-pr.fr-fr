---
title: Utilisation de Direct3D 11, Direct3D 10 et Direct2D
description: Cette section traite des techniques d’interopérabilité avec les versions antérieures de Direct3D et Direct2D, de l’API Direct3D 11on12 et des instructions de portage de Direct3D 11 vers Direct3D 12.
ms.assetid: 1AB98335-30B1-4244-B244-F8573524B38C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b200da0708b9b990b102a77867669217318f1d67
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104216"
---
# <a name="working-with-direct3d-11-direct3d-10-and-direct2d"></a>Utilisation de Direct3D 11, Direct3D 10 et Direct2D

Cette section traite des techniques d’interopérabilité avec les versions antérieures de Direct3D et Direct2D, de l’API Direct3D 11on12 et des instructions de portage de Direct3D 11 vers Direct3D 12.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                             | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Interopérabilité Direct3D 12](direct3d-12-with-direct3d-11--direct-2d-and-gdi.md)<br/>             | D3D12 peut être utilisé pour écrire des applications de composants. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [Direct3D 11 sur 12](direct3d-11-on-12.md)<br/>                                             | D3D11On12 est un mécanisme qui permet aux développeurs d’utiliser des interfaces et des objets D3D11 pour piloter l’API D3D12. D3D11on12 permet aux composants écrits à l’aide de D3D11 (par exemple, du texte et de l’interface utilisateur D2D) de fonctionner conjointement avec des composants écrits ciblant l’API D3D12. D3D11on12 permet également le portage incrémentiel d’une application de D3D11 vers D3D12, en permettant aux parties de l’application de continuer à cibler les D3D11 pour plus de simplicité, tandis que d’autres ciblent D3D12 pour les performances, tout en ayant toujours un rendu complet et correct. D3D11On12 simplifie l’utilisation de techniques d’interopérabilité pour partager des ressources et synchroniser le travail entre les deux API. <br/> |
| [Portage de Direct3D 11 sur Direct3D 12](porting-from-direct3d-11-to-direct3d-12.md)<br/> | Cette section fournit des conseils sur le portage d’un moteur graphique Direct3D 11 personnalisé vers Direct3D 12.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de programmation Direct3D 12](directx-12-programming-guide.md)
</dt> </dl>

 

 





