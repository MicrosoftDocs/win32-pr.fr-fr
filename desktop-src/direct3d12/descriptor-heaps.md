---
title: Tas de descripteurs
description: Un tas de descripteur est une collection d’allocations contiguës de descripteurs, une allocation pour chaque descripteur.
ms.assetid: 04d3facf-21ec-45ca-ad9b-78fdcddc7136
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f19821cff5e8730c376e5c80fef07e67974d31d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127521725"
---
# <a name="descriptor-heaps"></a>Tas de descripteurs

Un tas de descripteur est une collection d’allocations contiguës de descripteurs, une allocation pour chaque descripteur.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                             | Description                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Vue d’ensemble des tas de descripteurs](descriptor-heaps-overview.md)<br/>                             | Les tas de descripteurs contiennent de nombreux types d’objets qui ne font pas partie d’un objet d’État du pipeline (PSO), tels que les vues des ressources de nuanceur (SRVs), les vues d’accès non ordonnées (UAVs), les vues de mémoire tampon constante (CBVs) et les échantillonneurs. <br/>                |
| [Niveaux matériels](hardware-support.md)<br/>                                                 | Les niveaux de matériel du niveau 1 au niveau 3 ont des ressources accrues disponibles pour le pipeline. <br/>                                                                                                                              |
| [Tas du descripteur visible par le nuanceur](shader-visible-descriptor-heaps.md)<br/>                 | Les tas de descripteurs visibles du nuanceur, sont des tas de descripteurs qui peuvent être référencés par des nuanceurs par le biais de tables de descripteurs.<br/>                                                                                                              |
| [Tas du descripteur non visible par le nuanceur](non-shader-visible-descriptor-heaps.md)<br/>         | Certains tas de descripteurs ne peuvent pas être référencés par des nuanceurs par le biais de tables de descripteurs, mais ils existent pour aider l’application à mettre en attente les descripteurs avant l’enregistrement d’une liste de commandes ou parce qu’aucun tas visible par le nuanceur n’est requis.<br/> |
| [Création de tas de descripteurs](creating-descriptor-heaps.md)<br/>                             | Pour créer et configurer un tas de descripteur, vous devez sélectionner un type de tas de descripteur, déterminer le nombre de descripteurs qu’il contient et définir des indicateurs qui indiquent s’il est visible par l’UC et/ou nuanceur visible. <br/>                    |
| [Définition et remplissage des tas de descripteurs](setting-descriptor-heaps.md)<br/>                | Les types de tas de descripteur qui peuvent être définis sur une liste de commandes sont ceux qui contiennent des descripteurs pour lesquels les tables de descripteurs peuvent être utilisées (au plus une de chacune à la fois). <br/>                                                        |
| [Résumé de la configuration du tas de descripteurs](descriptor-heap-configurability-summary.md)<br/> | Le tableau suivant récapitule les informations sur la prise en charge des tas et des tas visibles non-nuanceur.<br/>                                                                                                                                    |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Descripteurs](descriptors.md)
</dt> <dt>

[Tables de descripteurs](descriptor-tables.md)
</dt> <dt>

[**ID3D12DescriptorHeap**](/windows/desktop/api/d3d12/nn-d3d12-id3d12descriptorheap)
</dt> <dt>

[Liaison de ressource](resource-binding.md)
</dt> <dt>

[Signatures racine](root-signatures.md)
</dt> </dl>

 

 





