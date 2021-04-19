---
description: Objet Port du contrôleur
ms.assetid: 5f94bcdc-93ab-4522-88bd-009a049b5dc9
title: Objet Port du contrôleur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7547581358bd79212b1093384ce1589e331f6ee0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516439"
---
# <a name="controller-port-object"></a>Objet Port du contrôleur

\[À compter de Windows 8 et de Windows Server 2012, l’interface com du [service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion de stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un objet Port de contrôleur modélise un port de contrôleur dans un sous-système. Les ordinateurs hôtes peuvent écrire et lire des numéros d’unités logiques via des ports de contrôleur. Les ports de contrôleur sont contenus par les contrôleurs dans un sous-système. Dans VDS 1,1 et VDS 2.0, chacun des ports de contrôleur d’un sous-système est défini comme actif ou inactif par rapport à chacun des numéros d’unités logiques que le sous-système couvre. Un seul port de contrôleur, alors, peut être défini simultanément sur actif pour un numéro d’unité logique et inactif pour d’autres. Un port de contrôleur actif pour un numéro d’unité logique donné est responsable de la gestion des entrées et sorties de l’unité logique.

Les ports de contrôleur actifs servent l’un des points de terminaison des chemins d’accès MPIO dans Fibre Channel fournisseurs de matériel, sur lesquels des stratégies d’équilibrage de charge peuvent être imposées.

Utilisez la méthode [**IVdsControllerControllerPort :: QueryControllerPorts**](/windows/desktop/api/Vds/nf-vds-ivdscontrollercontrollerport-querycontrollerports) pour déterminer les ports de contrôleur contenus dans un contrôleur spécifique. Les appelants peuvent obtenir un pointeur vers un port de contrôleur spécifique en sélectionnant l’objet de port de contrôleur souhaité dans l’énumération retournée par la méthode **QueryControllerPorts** . Avec un objet contrôleur, un appelant peut définir l’état du port du contrôleur et la requête pour les numéros d’unités logiques qui lui sont associés.

Les propriétés de l’objet contrôleur incluent un identificateur d’objet, un nom, un numéro de série et l’état du port du contrôleur.

Le tableau suivant répertorie les interfaces, énumérations et structures associées.



| Type                                                                                              | Élément                                                                                               |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| Interfaces toujours exposées par cet objet dans les fournisseurs de Fibre Channel VDS 1,1 et 2,0 uniquement | [**IVdsControllerPort**](/windows/desktop/api/Vds/nn-vds-ivdscontrollerport)                                                      |
| Énumérations associées                                                                           | [**\_État du port VDS \_**](/windows/desktop/api/Vds/ne-vds-vds_port_status)                                                          |
| Structures associées                                                                             | [**VDS \_ PORT \_ prop**](/windows/desktop/api/Vds/ns-vds-vds_port_prop) et [ **\_ \_ notification de port VDS**](/windows/desktop/api/Vds/ns-vds-vds_port_notification) |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Objets de fournisseur de matériel](hardware-provider-objects.md)
</dt> <dt>

[**IVdsControllerControllerPort::QueryControllerPorts**](/windows/desktop/api/Vds/nf-vds-ivdscontrollercontrollerport-querycontrollerports)
</dt> </dl>

 

 
