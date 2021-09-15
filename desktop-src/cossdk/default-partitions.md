---
description: Partitions par défaut
ms.assetid: ce6ad7c1-d4a1-4573-860e-f7859c588773
title: Partitions par défaut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5115b6b2480958c78a53c264804eb1f292808545
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127411263"
---
# <a name="default-partitions"></a>Partitions par défaut

Lorsqu’une partition par défaut est affectée à un utilisateur, COM+ tente d’abord d’activer les composants de cette partition. Si l’activation échoue, COM+ recherche le composant à activer dans la partition globale. L’exception à ce processus se produit lorsque le composant COM+ comprend un moniker de partition qui spécifie explicitement la partition dans laquelle le composant se trouve. Dans ce cas, le moniker de la partition a la priorité sur toute configuration de partition par défaut.

Lorsque vous utilisez des partitions locales, la partition par défaut est affectée aux utilisateurs à l’aide du dossier **com+ partition Users** dans l’outil d’administration Services de composants sur le serveur d’applications. Lorsque vous utilisez des jeux de partitions dans le Active Directory, la partition par défaut de l’utilisateur est déterminée par le jeu de partitions de l’utilisateur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Partitions locales](local-partitions.md)
</dt> <dt>

[Propriétés de partition](partition-properties.md)
</dt> <dt>

[Partitions et Active Directory](partitions-and-active-directory.md)
</dt> <dt>

[Partition globale](the-global-partition.md)
</dt> </dl>

 

 



