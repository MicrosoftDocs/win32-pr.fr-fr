---
description: 'Le modèle de transition d’état d’un fournisseur de clichés instantanés est simplifié par la sérialisation de la création de clichés instantanés à partir du moment où IVssBackupComponents :: StartSnapshotSet est appelé jusqu’à ce que l’appel à IVssBackupComponents ::D oSnapshotSet retourne.'
ms.assetid: 5dbf0fb3-53cb-4532-9a8f-bd955afe16c4
title: Transitions d’État dans les fournisseurs de clichés instantanés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad6141b9b8f221a1e67e95fde1e6b33ad819c0cbdead57eeb676164e89acc392
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118121599"
---
# <a name="state-transitions-in-shadow-copy-providers"></a>Transitions d’État dans les fournisseurs de clichés instantanés

Le modèle de transition d’état d’un fournisseur de clichés instantanés est simplifié par la sérialisation de la création de clichés instantanés à partir du moment où [**IVssBackupComponents :: StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) est appelé jusqu’à ce que l’appel à [**IVssBackupComponents ::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) retourne. Si un autre demandeur tente de créer un cliché instantané pendant cette période, l’appel à **StartSnapshotSet** échouera avec l’erreur **VSS \_ E \_ snapshot \_ Set \_ en \_ cours**, indiquant que le deuxième demandeur doit attendre et réessayer.

VSS appellera [**IVssProviderCreateSnapshotSet :: AbortSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-abortsnapshots) une fois que le demandeur a appelé [**DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset), même si le cliché instantané échoue ou est abandonné avant ce point. Cela signifie qu’un fournisseur ne recevra pas d’appel à **AbortSnapshots** tant que [**IVssProviderCreateSnapshotSet :: EndPrepareSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-endpreparesnapshots) n’a pas été appelé. Si un cliché instantané est abandonné ou échoue avant ce point, le fournisseur ne reçoit aucune indication tant qu’un nouveau cliché instantané n’a pas démarré. Pour cette raison, le fournisseur doit être prêt à gérer un appel hors séquence à [**IVssHardwareSnapshotProvider :: BeginPrepareSnapshot**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-beginpreparesnapshot) à tout moment. Cet appel hors séquence représente le début d’une nouvelle séquence de clichés instantanés et aura un nouvel ID de jeu de clichés instantanés.

 

 



