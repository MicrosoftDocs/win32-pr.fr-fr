---
description: Notifications VDS
ms.assetid: a0841215-3eb0-4769-b320-4da25b535362
title: Notifications VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa99751912f110a77b061d50134135413baf2894
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2021
ms.locfileid: "104551477"
---
# <a name="vds-notifications"></a>Notifications VDS

\[À compter de Windows 8 et de Windows Server 2012, l’interface com du [service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion de stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un fournisseur peut envoyer une notification d’événements à VDS, et VDS peut à son tour transférer la notification aux applications. Le modèle de notification utilisé par VDS ressemble au modèle de point de connexion utilisé par les objets COM.

VDS génère des notifications de service pour les événements tels que l’affectation d’une lettre de lecteur ou l’arrivée d’un disque non alloué. Une fois que VDS alloue un disque à un fournisseur, le fournisseur est responsable de la génération des notifications associées. L’illustration qui suit montre les interfaces et les méthodes utilisées dans le modèle de notification VDS.

![Diagramme qui montre l’interface et les méthodes (Advise, OnLoad et OnNotify) entre les applications, le service de disque virtuel et les fournisseurs V D S.](images/vdsnotification.png)

Pour recevoir des notifications, VDS inscrit son interface [**IVdsAdviseSink**](/windows/desktop/api/Vds/nn-vds-ivdsadvisesink) auprès de l’objet Provider en appelant la méthode [**IVdsProviderPrivate :: OnLoad**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsproviderprivate-onload) et en passant un pointeur vers l’interface. Lorsqu’un événement de notification se produit, tel que l’arrivée d’un nouveau volume ou lecteur, le fournisseur transmet la structure de notification appropriée à VDS en tant que paramètre de méthode [**IVdsAdviseSink :: OnNotify**](/windows/desktop/api/Vds/nf-vds-ivdsadvisesink-onnotify) .

Le processus est similaire entre une application et VDS. Plus précisément, pour recevoir des notifications, une application inscrit son interface [**IVdsAdviseSink**](/windows/desktop/api/Vds/nn-vds-ivdsadvisesink) auprès de VDS en appelant la méthode [**IVdsService :: Advise**](/windows/desktop/api/Vds/nf-vds-ivdsservice-advise) et en passant un pointeur vers l’interface. Lorsque VDS reçoit une notification de la part d’un fournisseur, il transmet la structure de notification appropriée aux applications inscrites en tant que paramètre de méthode [**IVdsAdviseSink :: OnNotify**](/windows/desktop/api/Vds/nf-vds-ivdsadvisesink-onnotify) .

> [!Note]  
> Une application qui appelle [**Advise**](/windows/desktop/api/Vds/nf-vds-ivdsservice-advise) doit finalement appeler la méthode [**IVdsService :: Unadvise**](/windows/desktop/api/Vds/nf-vds-ivdsservice-unadvise) . Dans l’idéal, il doit appeler **Unadvise** dès qu’il n’a plus besoin de recevoir des notifications.

 

Le tableau suivant répertorie les notifications générées par le fournisseur par type d’objet.



| Object     | Notification                              | Valeur | Lien vers la description de l’événement                                             |
|------------|-------------------------------------------|-------|-----------------------------------------------------------------------|
| Pack       | **l' \_ arrivée du VDS NF \_ Pack \_**                 | 1     | [**\_notification du Pack VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_pack_notification)              |
| Pack       | **VDS \_ - \_ Pack \_ NF**                 | 2     | [**\_notification du Pack VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_pack_notification)              |
| Pack       | **VDS \_ NF \_ Pack \_ Modify**                 | 3     | [**\_notification du Pack VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_pack_notification)              |
| Volume     | **\_réception du \_ volume du NF de VDS \_**               | 4     | [**\_notification du volume VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_volume_notification)          |
| Volume     | **VOLUME VDS du \_ NF \_ \_**               | 5     | [**\_notification du volume VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_volume_notification)          |
| Volume     | **modification du volume de VDS \_ NF \_ \_**               | 6     | [**\_notification du volume VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_volume_notification)          |
| Volume     | **progression de la reconstruction du volume VDS \_ NF \_ \_ \_** | 7     | [**\_notification du volume VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_volume_notification)          |
| Disque       | **\_réception du \_ disque VDS NF \_**                 | 8     | [**\_notification de disque VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)              |
| Disque       | **\_disque VDS NF- \_ \_ composant**                 | 9     | [**\_notification de disque VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)              |
| Disque       | **\_modification du \_ disque VDS NF \_**                 | 10    | [**\_notification de disque VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)              |
| Partition  | **réception de la \_ partition VDS NF \_ \_**            | 11    | [**\_notification de partition VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_partition_notification)    |
| Partition  | **\_partition VDS \_ NF \_**            | 12    | [**\_notification de partition VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_partition_notification)    |
| Partition  | **modification de la partition du VDS \_ NF \_ \_**            | 13    | [**\_notification de partition VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_partition_notification)    |
| Subsystem  | **le \_ \_ sous-système VDS NF est \_ \_ arrivé**          | 101   | [**\_notification du sous \_ -système VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_notification) |
| Subsystem  | **\_ \_ sous \_ -système VDS \_ NF**          | 102   | [**\_notification du sous \_ -système VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_notification) |
| Subsystem  | **\_ \_ sous \_ -système VDS \_ NF**          | 151   | [**\_notification du sous \_ -système VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_notification) |
| Contrôleur | **\_réception du \_ contrôleur VDS NF \_**           | 103   | [**\_notification du contrôleur VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification)  |
| Contrôleur | **\_contrôleur VDS \_ NF \_**           | 104   | [**\_notification du contrôleur VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification)  |
| Contrôleur | **modification du contrôleur de VDS \_ NF \_ \_**           | 350   | [**\_notification du contrôleur VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification)  |
| Contrôleur | **VDS \_ NF \_ Controller \_ supprimé**          | 351   | [**\_notification du contrôleur VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification)  |
| Port       | **\_modification du \_ port VDS NF \_**                 | 352   | [**\_notification de port VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_port_notification)              |
| Port       | **\_port VDS \_ NF \_ supprimé**                | 353   | [**\_notification de port VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_port_notification)              |
| Lecteur      | **\_réception du lecteur du NF NF \_ \_**                | 105   | [**\_notification de lecteur VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification)            |
| Lecteur      | **\_lecteur du NF NF \_ \_**                | 106   | [**\_notification de lecteur VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification)            |
| Lecteur      | **modification du lecteur de VDS \_ NF \_ \_**                | 107   | [**\_notification de lecteur VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification)            |
| Lecteur      | **\_lecteur NF \_ NF \_ supprimé**               | 354   | [**\_notification de lecteur VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification)            |
| Numéro d'unité logique        | **\_réception du \_ numéro d’unité logique VDS NF \_**                  | 108   | [**\_notification de LUN VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_lun_notification)                |
| Numéro d'unité logique        | **\_numéro d' \_ unité logique VDS NF \_**                  | 109   | [**\_notification de LUN VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_lun_notification)                |
| Numéro d'unité logique        | **\_modification du \_ numéro d’unité logique VDS \_**                  | 110   | [**\_notification de LUN VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_lun_notification)                |



 

VDS génère les notifications restantes. Le tableau suivant répertorie les constantes de notification basées sur les services par catégorie.



| Category     | Notification                                | Valeur | Lien vers la description de l’événement                                                 |
|--------------|---------------------------------------------|-------|---------------------------------------------------------------------------|
| Disque         | **\_réception du \_ disque VDS NF \_**                   | 8     | [**\_notification de disque VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)                  |
| Disque         | **\_disque VDS NF- \_ \_ composant**                   | 9     | [**\_notification de disque VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)                  |
| Disque         | **\_modification du \_ disque VDS NF \_**                   | 10    | [**\_notification de disque VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)                  |
| Lettre de lecteur | **\_lettre de lecteur du NF NF \_ \_ \_ gratuite**            | 201   | [**\_notification de \_ lettre de lecteur VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_drive_letter_notification) |
| Lettre de lecteur | **\_lettre de lecteur du NF NF \_ \_ \_**          | 202   | [**\_notification de \_ lettre de lecteur VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_drive_letter_notification) |
| Système de fichiers  | **\_modification du \_ système de fichiers NF NF \_ \_**           | 203   | [**\_notification du \_ système de fichiers VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_file_system_notification)   |
| Système de fichiers  | **progression de la mise en forme du système de fichiers de VDS \_ NF \_ \_ \_ \_** | 204   | [**\_notification du \_ système de fichiers VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_file_system_notification)   |
| Volume       | **\_changement des \_ points de montage VDS NF \_ \_**          | 205   | [**\_notification de \_ point de montage VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_mount_point_notification)   |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Modèle d’objet VDS](vds-object-model.md)
</dt> <dt>

[**IVdsAdviseSink**](/windows/desktop/api/Vds/nn-vds-ivdsadvisesink)
</dt> <dt>

[**IVdsAdviseSink :: OnNotify**](/windows/desktop/api/Vds/nf-vds-ivdsadvisesink-onnotify)
</dt> <dt>

[**IVdsProviderPrivate :: OnLoad**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsproviderprivate-onload)
</dt> <dt>

[**IVdsService :: Advise**](/windows/desktop/api/Vds/nf-vds-ivdsservice-advise)
</dt> </dl>

 

 
