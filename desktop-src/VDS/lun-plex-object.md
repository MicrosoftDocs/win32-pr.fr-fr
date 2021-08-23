---
description: LUN, objet Plex
ms.assetid: db6eabaa-1b84-4613-ab2a-8d5904305e08
title: LUN, objet Plex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df52b60bcbd23269d766435749b40b8c636361390359182a38a695ab6252a27f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999440"
---
# <a name="lun-plex-object"></a>LUN, objet Plex

\[à partir de Windows 8 et Windows Server 2012, l’interface COM du [Service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion des Stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un objet de plex LUN modélise un plex LUN qui est contenu dans un numéro d’unité logique. Seul un numéro d’unité logique en miroir peut avoir plusieurs Plex ; tous les autres types de LUN ont un Plex. Chaque Plex contient une copie des données sur le numéro d’unité logique. De nouveaux Plex peuvent être ajoutés à un numéro d’unité logique (LUN) et, à l’exception du Plex d’origine, les plex existants peuvent être supprimés. VDS prend en charge quatre types de plex LUN : simple, fractionné, agrégé par bandes et avec parité. Pour obtenir une description de chacun de ces types de LUN, consultez l' [objet lun](lun-object.md).

Utilisez la méthode [**IVdsLun :: AddPlex**](/windows/desktop/api/Vds/nf-vds-ivdslun-addplex) pour ajouter un Plex à un numéro d’unité logique et la méthode [**IVdsLun :: RemovePlex**](/windows/desktop/api/Vds/nf-vds-ivdslun-removeplex) pour supprimer le plex. Vous pouvez interroger les plex LUN en appelant la méthode [**IVdsLun :: QueryPlexes**](/windows/desktop/api/Vds/nf-vds-ivdslun-queryplexes) . Vous pouvez obtenir un pointeur vers un plex LUN spécifique en sélectionnant l’objet Plex souhaité à partir de l’énumération retournée par la méthode **QueryPlexes** . Avec un objet Plex, vous pouvez rechercher les étendues de lecteur et les indicateurs automagic, et appliquer de nouveaux indicateurs.

En plus de l’identificateur d’objet, d’un nom et d’un numéro de série, les propriétés des objets LUN Plex incluent le type, la taille, l’État, l’intégrité, l’état de transition et les indicateurs du Plex. une liste de démasquage et une taille d’entrelacement ; et un paramètre de priorité de reconstruction.

Le tableau suivant répertorie les interfaces, énumérations et structures associées.



| Type                                              | Élément                                                                                                                                                          |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces toujours exposées par cet objet | [**IVdsLunPlex**](/windows/desktop/api/Vds/nn-vds-ivdslunplex).                                                                                                                              |
| Énumérations associées                           | [**VDS \_ \_ \_ Indicateur de plex LUN**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_flag), [**\_ \_ \_ État du Plex LUN VDS**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_status)et [**\_ \_ \_ type de plex LUN VDS**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_type). |
| Structures associées                             | [**VDS \_ LUN \_ Plex \_ prop**](/windows/desktop/api/Vds/ns-vds-vds_lun_plex_prop).                                                                                                               |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Objets de fournisseur de matériel](hardware-provider-objects.md)
</dt> <dt>

[LUN (objet)](lun-object.md)
</dt> </dl>

 

 
