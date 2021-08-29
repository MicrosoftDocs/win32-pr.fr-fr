---
description: 'Au cours d’une opération de restauration, le demandeur peut utiliser la méthode IVssBackupComponents :: SetRestoreState pour définir le type d’opération de restauration en cours.'
ms.assetid: f6bf1979-7604-450f-8988-2a17da6b82d7
title: État de restauration VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e45e3be9863904440c295ed8e32dd9d5a288226c5ab850a46556eff5953a7236
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986549"
---
# <a name="vss-restore-state"></a>État de restauration VSS

Au cours d’une opération de restauration, le demandeur peut utiliser la méthode [**IVssBackupComponents :: SetRestoreState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestorestate) pour définir le type d’opération de restauration en cours. Toutefois, la plupart des opérations de restauration n’ont pas besoin de remplacer le type de restauration par défaut (VSS \_ RTYPE non \_ défini). Les enregistreurs doivent traiter ce type de restauration comme s’il s’agissait \_ de RTYPE VSS \_ par \_ copie. Pour plus d’informations sur les valeurs de type de restauration, consultez l’énumération du [**\_ \_ type de restauration VSS**](/windows/desktop/api/Vss/ne-vss-vss_restore_type) .

 

 



