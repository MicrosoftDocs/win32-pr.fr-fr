---
description: 'la liste suivante indique les ajouts et les modifications apportées à l’interface Service VSS dans Windows Server 2003 avec Service Pack 1 (SP1) :'
ms.assetid: 9e0dba98-5d23-444d-bd2f-cb72de8fb2d2
title: nouveautés de VSS dans Windows Server 2003 SP1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baed6cde05eb1aabe1bc43f48aa035146e020f23d215e7902d3544414619b4e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118344194"
---
# <a name="whats-new-in-vss-in-windows-server-2003-sp1"></a>nouveautés de VSS dans Windows Server 2003 SP1

la liste suivante indique les ajouts et les modifications apportées à l’interface Service VSS dans Windows Server 2003 avec Service Pack 1 (SP1) :

## <a name="auto-recovery"></a>Récupération automatique

La [*récupération automatique*](vssgloss-a.md) permet aux rédacteurs de mettre à jour les composants d’un cliché instantané avant que le cliché instantané ne soit définitivement modifié en lecture seule. Par exemple, une base de données peut avoir besoin de restaurer toutes les transactions incomplètes pour tous les clichés instantanés (l’enregistreur de base de données définit l’indicateur de **\_ \_ \_ récupération de sauvegarde CF VSS** pour les composants de base de données). La récupération automatique lancée par le demandeur autorise à la fois une restauration affinée (par exemple, la restauration d’une table dans une base de données ou un dossier sur un serveur de messagerie) ou la restauration pour prendre en charge l’exploration de données pour effectuer une analyse trop **lente pour un serveur \_ \_ \_ \_** de production La récupération automatique n’est pas compatible avec les clichés instantanés transportables, mais la même fonctionnalité est prise en charge à l’aide de la [récupération rapide à l’aide de volumes de clichés instantanés transportables](fast-recovery-using-transportable-shadow-copied-volumes.md).

Les éléments de programmation suivants ont des modifications pour prendre en charge la récupération automatique :

Méthodes de classe

-   [**CVssWriter::GetSnapshotDeviceName**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getsnapshotdevicename)
-   [**CVssWriter::OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot)

Énumérations

-   [**\_indicateurs du composant VSS \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags)
-   [**\_attributs de l' \_ instantané du volume VSS \_ \_**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)

Méthodes d’interface

-   [**IVssProviderCreateSnapshotSet ::P reFinalCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-prefinalcommitsnapshots)
-   [**IVssProviderCreateSnapshotSet ::P ostFinalCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postfinalcommitsnapshots)

## <a name="full-support-for-transportable-shadow-copies"></a>Prise en charge complète des clichés instantanés transportables

les clichés instantanés transportables sont pris en charge dans toutes les éditions de Windows Server 2003 avec SP1. Pour plus d’informations, consultez [importation de volumes clichés instantanés transportables](importing-transportable-shadow-copied-volumes.md).

## <a name="fast-recovery-using-transportable-shadow-copied-volumes"></a>Récupération rapide à l’aide de volumes de clichés instantanés transportables

[Récupération rapide à l’aide de volumes de clichés instantanés transportables](fast-recovery-using-transportable-shadow-copied-volumes.md)

## <a name="shadow-copy-storage-area-management"></a>Gestion de la zone de stockage des clichés instantanés

[**IVssSnapshotMgmt2**](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivsssnapshotmgmt2)

 

 



