---
description: Windows Server 2008 R2 et Windows 7 présentent les modifications suivantes apportées au Service VSS.
ms.assetid: 1287f175-29e4-40be-804b-d78542e76efc
title: 'Nouveautés : VSS dans Windows Server 2008 R2 & Windows 7'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3677f89517a770a4519369ae11f2eed7e7985414
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516666"
---
# <a name="whats-new-vss-in-windows-server-2008-r2--windows-7"></a>Nouveautés : VSS dans Windows Server 2008 R2 & Windows 7

Windows Server 2008 R2 et Windows 7 présentent les modifications suivantes apportées au Service VSS.

## <a name="new-vss-interfaces"></a>Nouvelles interfaces VSS

<dl>

[**IVssBackupComponentsEx3**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex3)  
[**IVssComponentEx2**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponentex2)  
[**IVssCreateExpressWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreateexpresswritermetadata)  
[**IVssExpressWriter**](/windows/desktop/api/VsWriter/nl-vswriter-ivssexpresswriter)  
</dl>

## <a name="new-vss-classes"></a>Nouvelles classes VSS

<dl>

[**CVssWriterEx2**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriterex2)  
</dl>

## <a name="new-vss-enumerations"></a>Nouvelles énumérations VSS

<dl>

[**\_options de récupération VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_recovery_options)  
</dl>

## <a name="new-vss-functions"></a>Nouvelles fonctions VSS

<dl>

[**CreateVssExpressWriter**](/windows/desktop/api/VsWriter/nf-vswriter-createvssexpresswriter)  
</dl>

## <a name="existing-vss-interface-modifications"></a>Modifications existantes de l’interface VSS

<dl>

Interface [**IVssHardwareSnapshotProviderEx**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotproviderex)<dl> Méthode ajoutée : [ **ResyncLuns**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotproviderex-resyncluns)  
</dl> </dd> </dl>

## <a name="vss-event-tracing-and-logging"></a>Suivi et journalisation des événements VSS

À compter de Windows Server 2008 R2 et Windows 7, vous pouvez utiliser l’outil VssTrace, l’outil Logman ou l’outil tracelog pour collecter des informations de traçage pour l’infrastructure VSS. Pour plus d’informations, consultez [utilisation des outils de suivi avec VSS](using-tracing-tools-with-vss.md).

## <a name="lun-resynchronization"></a>Resynchronisation des LUN

Dans Windows Server 2008 R2 et Windows 7, les demandeurs VSS peuvent utiliser une fonctionnalité de fournisseur matériel de clichés instantanés appelée resynchronisation de numéro d’unité logique. Il s’agit d’un schéma de récupération rapide qui permet à un administrateur d’application de restaurer des données à partir d’un cliché instantané vers le numéro d’unité logique (LUN) d’origine ou vers un nouveau LUN. Le cliché instantané peut être un clone complet ou un cliché instantané différentiel. Dans les deux cas, à la fin de l’opération de resynchronisation, le numéro d’unité logique de destination présente le même contenu que le numéro d’unité logique du cliché instantané. Pendant l’opération de resynchronisation, la baie effectue une copie au niveau du bloc du cliché instantané vers le numéro d’unité logique de destination. Pour plus d’informations, consultez les rubriques suivantes :

-   [Resynchronisation des LUN-un scénario de récupération rapide dans le serveur 2008 R2](https://blogs.technet.com/filecab/archive/2009/04/11/lun-resync-a-fast-recovery-scenario-in-server-2008-r2.aspx)
-   « Utilisation des clichés instantanés » dans [service VSS](/windows-server/storage/file-server/volume-shadow-copy-service)
-   [Pièges courants de resynchronisation des LUN](https://blogs.msdn.com/gregd/archive/2009/07/27/common-lun-resync-gotchas.aspx)

## <a name="express-writers"></a>Writers Express

Dans Windows Server 2008 R2 et Windows 7, l’interface VSS Express permet à une application d’enregistrer l’emplacement de ses fichiers de données sans avoir à implémenter un enregistreur VSS. Pour plus d’informations, consultez [service VSS (VSS) enregistreurs Express](https://blogs.technet.com/filecab/archive/2009/06/17/volume-shadow-copy-service-vss-express-writers.aspx).

## <a name="new-vss-writers"></a>Nouveaux enregistreurs VSS

Windows Server 2008 R2 et Windows 7 présentent les enregistreurs VSS suivants :

-   Enregistreur des compteurs de performances
-   Rédacteur de Planificateur de tâches
-   Enregistreur du magasin de métadonnées VSS

Ces nouveaux enregistreurs sont documentés dans les [enregistreurs VSS](in-box-vss-writers.md).

 

 
