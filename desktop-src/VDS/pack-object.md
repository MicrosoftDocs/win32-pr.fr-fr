---
description: Objet Pack
ms.assetid: e84a05a0-ea12-4bc1-83e1-1eb0dd291dc9
title: Objet Pack
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaa8c565c45b802258b9d8b9955a2d28adc13c73c989805ce6b2663bc3006d7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058021"
---
# <a name="pack-object"></a>Objet Pack

\[à partir de Windows 8 et Windows Server 2012, l’interface COM du [Service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion des Stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un objet Pack modélise un groupe de disques, un ensemble de disques et de volumes gérés par le fournisseur de logiciels de base ou dynamique. Un fournisseur peut contenir plusieurs objets Pack.

À l’aide de l’API, les applications peuvent diriger VDS pour ajouter un ou plusieurs disques à un Pack, lier les disques à des volumes et éventuellement déplacer les disques en tant qu’unité entre les ordinateurs hôtes. Vous ne pouvez pas importer un volume existant dans un Pack.

> [!Note]  
> L’appartenance à un Pack n’implique pas la cohérence entre les disques en ce qui concerne les performances, les médias, le protocole d’interconnexion ou d’autres caractéristiques.

 

Les objets disque ne sont pas alloués et gérés par VDS, ou ils sont membres d’un seul Pack. Le fournisseur de logiciels de base peut comporter zéro, un ou plusieurs packs, chacun contenant un seul disque de base. Le fournisseur n’impose aucune limite au nombre de volumes sur un disque de base. Le fournisseur dynamique peut avoir zéro, un ou plusieurs packs avec plusieurs disques dynamiques dans chaque Pack. Ce fournisseur limite le nombre de volumes sur un disque, en fonction de la taille d’un mégaoctet de la base de données du gestionnaire de disque logique (LDM). Étant donné qu’un volume a au moins un plex et une extension de disque, le nombre maximal de volumes pour un Pack est d’environ 1000. Le nombre maximal de disques tombe en panne.

En plus des objets disque, un pack peut contenir un ou plusieurs objets LUN implémentés par un ou plusieurs fournisseurs de matériel. pour le noyau Windows, un numéro d’unité logique est simplement un autre disque. (Les objets LUN doivent être démasqués sur l’ordinateur qui exécute le programme fournisseur.) Lorsque le disque est un numéro d’unité logique (LUN), l’objet LUN expose les interfaces [**IVdsLun**](/windows/desktop/api/Vds/nn-vds-ivdslun) et [**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk) . Un objet Pack utilise **IVdsDisk**, au lieu de **IVdsLun**, pour énumérer les numéros d’unités logiques dans un Pack. Pour obtenir une description plus détaillée d’un numéro d’unité logique, consultez l' [objet lun](lun-object.md).

L’illustration suivante montre un pack avec deux membres : un disque et un numéro d’unité logique (LUN). Une application peut ajouter ces objets à un Pack en ligne et créer un volume à partir du disque sous-jacent et des étendues de lecteur représentées par des piles de disques.

![Diagramme montrant un « pack » avec un disque et un LUN ajouté par une application pour créer un volume représenté par un « lecteur » et un « axe ».](images/vdsdisksareluns.png)

Utilisez la méthode [**IVdsSwProvider :: CreatePack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack) pour créer un nouvel objet Pack. Les appelants peuvent obtenir un pointeur vers un pack spécifique en sélectionnant l’objet Pack souhaité dans l’énumération retournée par la méthode [**IVdsSwProvider :: QueryPacks**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-querypacks) . Avec un objet Pack, vous pouvez ajouter, supprimer ou remplacer les membres d’un Pack. Lorsque vous ajoutez un objet disque à un Pack, VDS Initialise un disque pour dissocier tous les volumes existants. En revanche, un numéro d’unité logique conserve tous les détails de liaison lorsqu’il est ajouté à un Pack. Si vous supprimez le dernier disque d’un Pack, VDS supprime l’objet Pack lorsque l’appelant libère la dernière référence à l’objet.

Les propriétés d’objet incluent un identificateur d’objet, un nom, un état de Pack et des indicateurs. Un Pack en ligne est disponible pour la configuration et l’utilisation, un pack hors connexion n’est pas disponible. VDS prend en charge un nombre quelconque de packs en ligne et hors connexion.

**Windows Server 2003 :** Ne prend en charge qu’un seul Pack en ligne à la fois.

VDS applique un quorum de disques en ligne au sein d’un Pack. Le quorum détermine si un pack peut avoir un État en ligne et empêche plusieurs hôtes d’accorder un État en ligne au même Pack. Si le nombre de disques en ligne d’un pack se situe sous le quorum (n/2 + 1), VDS met le Pack en ligne hors connexion.

Le tableau suivant répertorie les interfaces, énumérations et structures associées.



| Type                                              | Élément                                                                                                |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| Interfaces toujours exposées par cet objet | [**IVdsPack**](/windows/desktop/api/Vds/nn-vds-ivdspack) et [**IVdsPack2**](/windows/desktop/api/Vds/nn-vds-ivdspack2) \* .                                     |
| Énumérations associées                           | [**VDS \_ \_**](/windows/desktop/api/Vds/ne-vds-vds_pack_flag) État de l’indicateur de Pack et du [**\_ Pack \_ VDS**](/windows/desktop/api/Vds/ne-vds-vds_pack_status).             |
| Structures associées                             | [**VDS \_ NOTIFICATION PACK \_ prop**](/windows/desktop/api/Vds/ns-vds-vds_pack_prop) et [**VDS \_ Pack \_**](/windows/desktop/api/Vds/ns-vds-vds_pack_notification). |



 

**\* Windows Server 2003 :** cette interface n’est pas prise en charge tant que Windows Vista.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Objets de fournisseur de logiciels](software-provider-objects.md)
</dt> <dt>

[LUN (objet)](lun-object.md)
</dt> <dt>

[**IVdsLun**](/windows/desktop/api/Vds/nn-vds-ivdslun)
</dt> <dt>

[**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk)
</dt> </dl>

 

 
