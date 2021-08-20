---
description: Présentation de la configuration
ms.assetid: 5cdc21a1-ff55-4c36-8106-b045256778ce
title: Présentation de la configuration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b742cb5ca2f287cd8b50b9f248d0ebec1174bfd71b59f0630bd9fb98864309c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007949"
---
# <a name="configuration-overview"></a>Présentation de la configuration

\[à partir de Windows 8 et Windows Server 2012, l’interface COM du [Service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion des Stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Si vous n’êtes pas familiarisé avec les objets définis par VDS, consultez le [modèle d’objet VDS](vds-object-model.md).

La complexité de la configuration d’un disque virtuel peut aller de très simple à affiné. Les disques virtuels sans souci, Free-of-Care et Enterprise définissent trois perspectives de configuration standard. Chaque perspective présente des exigences différentes :

-   Les disques virtuels sans prudence sont peu configurés, peut-être uniquement pour automatiser le partitionnement et la mise en forme de nouveaux disques, ou pour créer temporairement un volume en miroir pour la migration des données d’un disque vers un autre sans temps d’arrêt. Ces disques sont corrects pour les ordinateurs portables et les autres systèmes avec un ou plusieurs disques.
-   Les disques virtuels Free-of-Care offrent un stockage qui s’affiche, autorépare, auto-réparable et disponible ; utilise des volumes agrégés par bandes et des numéros d’unités logiques pour obtenir de meilleures performances. utilise des volumes et des numéros d’unités logiques en miroir pour obtenir une meilleure disponibilité. et utilise des packs pour que les modes d’échec soient propres et contenus. Ce niveau de configuration est idéal pour remplacer les anciens disques système lents par les nouveaux disques rapides, de grande taille. Il est également idéal pour la mise en miroir de données avec le remplacement à chaud automatique. une seule pile de rechange peut protéger de nombreux axes. Pour plus d’informations, consultez [remplacement à chaud](hot-sparing.md).

    les san à petite échelle dépendent de la flexibilité et de l’automatisation offertes par ce niveau de configuration, comme les appliances NAS (Network attached Stockage). les disques virtuels libres de soins simplifient la tâche de consolidation du stockage des applications (par exemple, le stockage pour les SQL et les Exchange) sans la consolidation des serveurs.

-   Enterprise les disques virtuels contiennent des configurations d’entreprise très volumineuses ou complexes avec des exigences supplémentaires spécifiques au site ou à l’application. Les administrateurs règlent le sous-système de stockage pour une seule application qui peut s’exécuter rarement, par exemple un travail de création de rapports par lots mensuel sur un système de transaction de commande. Enterprise disques virtuels doivent être mis à l’échelle, afficher l’activité en temps réel du sous-système de stockage et répondre aux exigences des administrateurs pratiques.

Pour plus d’informations sur les miroirs, les bandes et les autres options de configuration dans VDS, consultez [liaison de volume et de LUN](volume-and-lun-binding.md). Une technique de configuration avancée, appelée empilement, vous permet de combiner les configurations associées aux volumes et LUN existants. Pour plus d’informations, consultez [pile de configurations](configuration-stacking.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Service Disque virtuel](virtual-disk-service-portal.md)
</dt> <dt>

[Modèle d’objet VDS](vds-object-model.md)
</dt> <dt>

[Remplacement à chaud](hot-sparing.md)
</dt> <dt>

[Liaison de volume et de numéro d’unité logique](volume-and-lun-binding.md)
</dt> <dt>

[Empilement de configurations](configuration-stacking.md)
</dt> </dl>

 

 
