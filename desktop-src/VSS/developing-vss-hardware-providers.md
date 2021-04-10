---
description: Les fournisseurs de matériel implémentent les interfaces IVssProviderCreateSnapshotSet et IVssHardwareSnapshotProvider.
ms.assetid: 9f40f1d1-a63a-4edc-aa8d-b3998ecb2716
title: Développement de fournisseurs de matériel VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca6e9775eb6ee4ee5f16451f51f29cc1c87b300
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210571"
---
# <a name="developing-vss-hardware-providers"></a>Développement de fournisseurs de matériel VSS

Les fournisseurs de matériel implémentent les interfaces [**IVssProviderCreateSnapshotSet**](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidercreatesnapshotset) et [**IVssHardwareSnapshotProvider**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotprovider) . **IVssProviderCreateSnapshotSet** implémente le séquencement d’état de cliché instantané. **IVssHardwareSnapshotProvider** opère sur une abstraction de LUN. Les fournisseurs doivent être implémentés en tant que serveur COM hors processus. Les fournisseurs utilisent des mécanismes spécifiques au fournisseur (souvent des IOCTL privées) pour communiquer avec le sous-système de stockage qui instancie les numéros d’unités logiques de clichés instantanés.

-   [Inscription et chargement du fournisseur de clichés instantanés](shadow-copy-provider-registration-and-loading.md)
-   [Création de clichés instantanés pour les fournisseurs](shadow-copy-creation-for-providers.md)
-   [Interactions et comportements des fournisseurs de matériel](hardware-provider-interactions-and-behaviors.md)

 

 



