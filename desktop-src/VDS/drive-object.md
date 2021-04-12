---
description: Objet Drive
ms.assetid: c1c17a97-cf4b-45b7-bc32-4bad94c3ddb2
title: Objet Drive
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7df8501c79f9381dba80a1fe0276014dccdf7a34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203015"
---
# <a name="drive-object"></a>Objet Drive

\[À compter de Windows 8 et de Windows Server 2012, l’interface com du [service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion de stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un objet lecteur modélise un lecteur de disque physique qui est contenu dans un sous-système. Chaque lecteur se connecte à un bus, occupe un emplacement et contient un ensemble d’étendues de lecteurs. Chaque lecteur peut fournir des étendues à n’importe quel nombre de numéros d’unités logiques. Un lecteur peut également être désigné comme disque de rechange à chaud.

Utilisez la méthode [**IVdsSubSystem :: QueryDrives**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querydrives) pour déterminer les lecteurs contenus dans un sous-système spécifique. Les appelants peuvent obtenir un pointeur vers un lecteur spécifique en sélectionnant l’objet lecteur souhaité dans l’énumération retournée par la méthode **QueryDrives** , ou en appelant la méthode [**IVdsSubSystem :: GetDrive**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-getdrive) et en passant le bus et le numéro d’emplacement souhaités. Avec un objet lecteur, vous pouvez définir l’état du lecteur et la requête pour les propriétés du lecteur, les étendues de lecteur associées et le sous-système contenant le lecteur.

En plus de l’identificateur d’objet, d’un nom et d’un numéro de série, les propriétés de l’objet lecteur incluent l’état du lecteur, l’intégrité et les indicateurs ; taille en octets ; et un numéro de bus et d’emplacement.

Le tableau suivant répertorie les interfaces, énumérations et structures associées.



| Type                                              | Élément                                                                                                                                         |
|---------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces toujours exposées par cet objet | [**IVdsDrive**](/windows/desktop/api/Vds/nn-vds-ivdsdrive)                                                                                                                  |
| Interfaces qui peuvent être exposées par cet objet     | [**IVdsMaintenance**](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance)                                                                                                      |
| Énumérations associées                           | [**VDS \_ \_Indicateur de lecteur**](/windows/desktop/api/Vds/ne-vds-vds_drive_flag), [**\_ \_ État du lecteur VDS**](/windows/desktop/api/Vds/ne-vds-vds_drive_status)et [**\_ \_ étendue du lecteur VDS**](/windows/desktop/api/Vds/ns-vds-vds_drive_extent). |
| Structures associées                             | [**VDS \_ La \_ prop**](/windows/desktop/api/Vds/ns-vds-vds_drive_prop) . du lecteur et la [**\_ \_ notification du lecteur VDS**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification).                                      |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Objets de fournisseur de matériel](hardware-provider-objects.md)
</dt> <dt>

[**IVdsSubSystem::QueryDrives**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querydrives)
</dt> <dt>

[**IVdsSubSystem::GetDrive**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-getdrive)
</dt> </dl>

 

 
