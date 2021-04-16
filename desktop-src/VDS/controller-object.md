---
description: Objet contrôleur
ms.assetid: ae2c4d47-15a6-4b9d-9165-4ee04a6ff3a8
title: Objet contrôleur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7db9468c1ca4c8f07c5498724333bdad9fc53bf
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2021
ms.locfileid: "104570941"
---
# <a name="controller-object"></a>Objet contrôleur

\[À compter de Windows 8 et de Windows Server 2012, l’interface com du [service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion de stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un objet de contrôleur modélise un contrôleur dans un sous-système. Les contrôleurs sont contenus dans les sous-systèmes, et chaque contrôleur possède un ou plusieurs ports de contrôleur via lesquels l’ordinateur hôte peut écrire et lire des numéros d’unités logiques. Un seul contrôleur peut être défini simultanément sur actif pour un numéro d’unité logique et inactif pour d’autres. Un contrôleur actif pour un numéro d’unité logique spécifié assume la responsabilité de la gestion des entrées et sorties de l’unité logique. La figure suivante illustre cette idée.

![Diagramme montrant un « contrôleur » avec un numéro d’unité logique actif sur la gauche et deux numéros d’unités logiques actifs à droite.](images/vdscontroller.png)

**VDS 1,0 :** Chacun des contrôleurs d’un sous-système est défini sur actif ou inactif par rapport à chacun des numéros d’unités logiques que le sous-système couvre.

Les applications VDS utilisent la méthode [**IVdsSubSystem :: QueryControllers**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querycontrollers) pour déterminer les contrôleurs contenus dans un sous-système spécifique. Les appelants peuvent obtenir un pointeur vers un contrôleur spécifique en sélectionnant l’objet contrôleur souhaité dans l’énumération retournée par la méthode **QueryControllers** . Avec un objet contrôleur, un appelant peut définir l’état du contrôleur, interroger les numéros d’unités logiques associés, interroger ses ports de contrôleur et vider et invalider le cache.

En plus de l’identificateur d’objet, d’un nom et d’un numéro de série, les propriétés de l’objet contrôleur incluent l’État et l’intégrité du contrôleur, ainsi que le nombre de ports.

Le tableau suivant répertorie les interfaces, énumérations et structures associées.



| Type                                                                                              | Élément                                                                                                                        |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| Interfaces toujours exposées par cet objet                                                 | [**IVdsController**](/windows/desktop/api/Vds/nn-vds-ivdscontroller)                                                                                       |
| Interfaces toujours exposées par cet objet dans les fournisseurs de Fibre Channel VDS 1,1 et 2,0 uniquement | [**IVdsControllerControllerPort**](/windows/desktop/api/Vds/nn-vds-ivdscontrollercontrollerport)                                                           |
| Interfaces qui peuvent être exposées par cet objet                                                     | [**IVdsMaintenance**](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance)                                                                                     |
| Énumérations associées                                                                           | [**VDS \_ \_État du contrôleur**](/windows/desktop/api/Vds/ne-vds-vds_controller_status).                                                                      |
| Structures associées                                                                             | [**VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_controller_prop) Notification du contrôleur prop et du [**\_ contrôleur \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification). |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Objets de fournisseur de matériel](hardware-provider-objects.md)
</dt> <dt>

[**IVdsSubSystem::QueryControllers**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querycontrollers)
</dt> </dl>

 

 
