---
description: Objets de fournisseur de logiciels
ms.assetid: 0d415238-7558-4d90-a122-e65ae7760344
title: Objets de fournisseur de logiciels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 507abb00b67b51ad68eb0592ff4fa7b5201cff5be0587b7170662556238feb50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137155"
---
# <a name="software-provider-objects"></a>Objets de fournisseur de logiciels

\[à partir de Windows 8 et Windows Server 2012, l’interface COM du [Service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion des Stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Les objets de fournisseur de logiciels modélisent des appareils physiques, tels que des disques IDE et des CD-ROM, et des éléments virtuels tels que des packs, des volumes et des plex de volume. L’illustration suivante montre la relation entre l’objet de fournisseur et le jeu d’objets de fournisseur de logiciels, ainsi que la relation entre les différents objets de fournisseur de logiciels eux-mêmes.

![Diagramme qui montre la relation entre un « fournisseur » et des objets de fournisseur de logiciels, tels que « Pack » et « volume ».](images/vdsswobjects.png)

Un objet fournisseur peut contenir zéro ou plusieurs packs. Un objet Pack peut contenir zéro, un ou plusieurs disques et volumes. Un volume comprend au moins un plex de volume et chaque plex de volume peut être mappé à un ou plusieurs disques, selon le type de plex. VDS gère directement les disques non alloués, sans conteneur de packs. Les autres rubriques de cette section décrivent les objets Pack, disque, volume et Plex volume.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Modèle d’objet VDS](vds-object-model.md)
</dt> </dl>

 

 
