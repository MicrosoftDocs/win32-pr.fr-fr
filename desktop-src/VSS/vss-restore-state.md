---
description: 'Au cours d’une opération de restauration, le demandeur peut utiliser la méthode IVssBackupComponents :: SetRestoreState pour définir le type d’opération de restauration en cours.'
ms.assetid: f6bf1979-7604-450f-8988-2a17da6b82d7
title: État de restauration VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97581d33f5695890ba83e87c6f6155a9e7f92f78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531661"
---
# <a name="vss-restore-state"></a>État de restauration VSS

Au cours d’une opération de restauration, le demandeur peut utiliser la méthode [**IVssBackupComponents :: SetRestoreState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestorestate) pour définir le type d’opération de restauration en cours. Toutefois, la plupart des opérations de restauration n’ont pas besoin de remplacer le type de restauration par défaut (VSS \_ RTYPE non \_ défini). Les enregistreurs doivent traiter ce type de restauration comme s’il s’agissait \_ de RTYPE VSS \_ par \_ copie. Pour plus d’informations sur les valeurs de type de restauration, consultez l’énumération du [**\_ \_ type de restauration VSS**](/windows/desktop/api/Vss/ne-vss-vss_restore_type) .

 

 



