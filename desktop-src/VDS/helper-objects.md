---
description: 'VDS fournit deux objets d’assistance : l’objet d’énumération et l’objet Async. Cette rubrique décrit chacun de ces objets et fournit des liens vers des exemples de la façon dont les appelants fonctionnent avec chacun d’eux.'
ms.assetid: 0f809c71-a3bd-4c62-8086-9651ea1a3400
title: Objets d’assistance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac5193003abd10d9fa2c311b250272d9ad5847a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210749"
---
# <a name="helper-objects"></a>Objets d’assistance

\[À compter de Windows 8 et de Windows Server 2012, l’interface com du [service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion de stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

VDS fournit deux objets d’assistance : l’objet d’énumération et l’objet Async. Cette rubrique décrit chacun de ces objets et fournit des liens vers des exemples de la façon dont les appelants fonctionnent avec chacun d’eux.

## <a name="enumeration-object"></a>Objet d’énumération

Un objet d’énumération énumère un ensemble d’objets VDS d’un type donné. Les objets peuvent être des fournisseurs, des sous-systèmes, des contrôleurs, des numéros d’unités logiques, des plex LUN, des lecteurs, des disques, des disques, des volumes ou des plex de volume. Les appelants peuvent obtenir un pointeur vers un objet spécifique en sélectionnant l’objet souhaité à partir de l’énumération retournée par la méthode appropriée. Pour obtenir un exemple de code, consultez [utilisation des objets d’énumération](working-with-enumeration-objects.md).

Le tableau suivant répertorie les interfaces, énumérations et structures associées. 

| Type                                              | Élément                                  |
|---------------------------------------------------|------------------------------------------|
| Interfaces toujours exposées par cet objet | [**IEnumVdsObject**](/windows/desktop/api/Vds/nn-vds-ienumvdsobject) |
| Énumérations associées                           | Aucun                                    |
| Structures associées                             | Aucun                                    |



 

## <a name="async-object"></a>Objet Async

Un objet Async gère les opérations asynchrones. Les méthodes qui lancent des opérations asynchrones retournent un pointeur vers une interface [**IVdsAsync**](/windows/desktop/api/Vds/nn-vds-ivdsasync) , qui permet à l’appelant d’annuler, d’attendre et de demander l’état de l’opération asynchrone.

Les opérations VDS de longue durée ont tendance à être implémentées de manière asynchrone. Les programmes de base et dynamiques du fournisseur de logiciels implémentent des méthodes asynchrones de manière cohérente pour les opérations de volume, de partition et de disque. Les fournisseurs de matériel implémentent éventuellement des méthodes asynchrones asynchrones. Quelle que soit la façon dont le fournisseur implémente la méthode, l’opération doit retourner un pointeur vers une interface [**IVdsAsync**](/windows/desktop/api/Vds/nn-vds-ivdsasync) à l’appelant. Pour obtenir un exemple de code, consultez [gestion des opérations asynchrones](managing-asynchronous-operations.md).

Les opérations asynchrones sont les suivantes :

-   Création d’un numéro d’unité logique (LUN), d’un volume ou d’une partition.
-   Formatage d’un volume ou d’une partition.
-   Ajout ou suppression d’un numéro d’unité logique ou d’un plex de volume.
-   Interruption d’un plex de volume.
-   Extension ou réduction d’un numéro d’unité logique ou d’un volume.
-   Récupération d’un numéro d’unité logique ou d’un volume.
-   Nettoyage d’un disque.
-   Remplacement d’un disque.

Le tableau suivant répertorie les interfaces, énumérations et structures associées. 

| Type                                              | Élément                        |
|---------------------------------------------------|--------------------------------|
| Interfaces toujours exposées par cet objet | [**IVdsAsync**](/windows/desktop/api/Vds/nn-vds-ivdsasync) |
| Énumérations associées                           | Aucun                          |
| Structures associées                             | Aucun                          |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Modèle d’objet VDS](vds-object-model.md)
</dt> <dt>

[**IVdsAsync**](/windows/desktop/api/Vds/nn-vds-ivdsasync)
</dt> <dt>

[Utilisation d’objets d’énumération](working-with-enumeration-objects.md)
</dt> <dt>

[Gestion des opérations asynchrones](managing-asynchronous-operations.md)
</dt> </dl>

 

 
