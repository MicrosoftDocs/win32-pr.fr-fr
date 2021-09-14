---
title: Descripteurs
description: Les descripteurs sont l’unité principale de liaison pour une seule ressource dans D3D12.
ms.assetid: f35b5776-46b0-4659-9e61-c6ebfdb55f87
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9576a2d40ade89c9c7a342feb6b069ca1321028e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127293606"
---
# <a name="descriptors"></a>Descripteurs

Les descripteurs sont l’unité principale de liaison pour une seule ressource dans D3D12.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                       | Description                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Vue d’ensemble des descripteurs](descriptors-overview.md)<br/> | Les descripteurs sont créés par des appels d’API et identifient les ressources.<br/>                                                                                                                                                                                                                                                                                                                   |
| [Création de descripteurs](creating-descriptors.md)<br/> | Décrit et montre des exemples pour créer des vues de mémoire tampon d’index, de vertex et de constantes ; la ressource de nuanceur, la cible de rendu, l’accès non ordonné, la sortie de flux et les vues de stencil de profondeur ; et les échantillonneurs. Toutes les méthodes de création de descripteurs sont des threads libres.<br/>                                                                                                                             |
| [Copie de descripteurs](copying-descriptors.md)<br/>   | Les méthodes [**ID3D12Device :: CopyDescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) et [**ID3D12Device :: CopyDescriptorsSimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple) sur l’interface de l’appareil utilisent le processeur pour copier immédiatement les descripteurs. Ils peuvent être appelés thread libre, à condition que plusieurs threads sur le processeur ou le GPU n’effectuent pas d’écriture potentiellement conflictuelle.<br/> |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Tas de descripteurs](descriptor-heaps.md)
</dt> <dt>

[Tables de descripteurs](descriptor-tables.md)
</dt> <dt>

[Liaison de ressource](resource-binding.md)
</dt> <dt>

[Signatures racine](root-signatures.md)
</dt> </dl>

 

 





