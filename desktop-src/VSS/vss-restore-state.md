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
# <a name="vss-restore-state"></a><span data-ttu-id="29bd2-103">État de restauration VSS</span><span class="sxs-lookup"><span data-stu-id="29bd2-103">VSS Restore State</span></span>

<span data-ttu-id="29bd2-104">Au cours d’une opération de restauration, le demandeur peut utiliser la méthode [**IVssBackupComponents :: SetRestoreState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestorestate) pour définir le type d’opération de restauration en cours.</span><span class="sxs-lookup"><span data-stu-id="29bd2-104">During a restore operation, the requester can use the [**IVssBackupComponents::SetRestoreState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestorestate) method to define the type of restore operation in progress.</span></span> <span data-ttu-id="29bd2-105">Toutefois, la plupart des opérations de restauration n’ont pas besoin de remplacer le type de restauration par défaut (VSS \_ RTYPE non \_ défini).</span><span class="sxs-lookup"><span data-stu-id="29bd2-105">However, most restore operations will not need to override the default restore type (VSS\_RTYPE\_UNDEFINED).</span></span> <span data-ttu-id="29bd2-106">Les enregistreurs doivent traiter ce type de restauration comme s’il s’agissait \_ de RTYPE VSS \_ par \_ copie.</span><span class="sxs-lookup"><span data-stu-id="29bd2-106">Writers should treat this restore type as if it were VSS\_RTYPE\_BY\_COPY.</span></span> <span data-ttu-id="29bd2-107">Pour plus d’informations sur les valeurs de type de restauration, consultez l’énumération du [**\_ \_ type de restauration VSS**](/windows/desktop/api/Vss/ne-vss-vss_restore_type) .</span><span class="sxs-lookup"><span data-stu-id="29bd2-107">For more information about restore type values, see the [**VSS\_RESTORE\_TYPE**](/windows/desktop/api/Vss/ne-vss-vss_restore_type) enumeration.</span></span>

 

 



