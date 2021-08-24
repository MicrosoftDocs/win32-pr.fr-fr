---
description: Une fois le cliché instantané terminé, le mécanisme le plus important pour obtenir l’accès aux données de fichier qu’il contient consiste à utiliser l’objet appareil du cliché instantané.
ms.assetid: 21efdbd6-a487-4e6f-8e3c-b9224bcf92da
title: Accès du demandeur aux données des clichés instantanés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 779e3947adff28c8f3190026921c398677afc7efaa484903bf165250f41bc191
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767699"
---
# <a name="requester-access-to-shadow-copied-data"></a>Accès du demandeur aux données des clichés instantanés

Une fois le cliché instantané terminé, le mécanisme le plus important pour obtenir l’accès aux données de fichier qu’il contient consiste à utiliser l' [*objet appareil*](vssgloss-d.md)du cliché instantané.

Le membre **m \_ pwszSnapshotDeviceObject** d’une structure de [**\_ \_ Propriétés de capture instantanée VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) est une chaîne contenant un objet périphérique de volume cliché instantané. Un demandeur peut obtenir l’objet de la **\_ \_ prop instantané VSS** d’un volume cliché instantané s’il connaît l' **\_ ID VSS** du volume (GUID d’identification) et le transmet à [**IVssBackupComponents :: GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties).

Un demandeur peut également obtenir des informations sur les propriétés des clichés instantanés à l’aide du membre **obj. Snap** de la structure de l' [**\_ objet VSS \_**](/windows/desktop/api/Vss/ns-vss-vss_object_prop) (qui est une structure de [**\_ \_ prop instantanés VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) ) obtenue en utilisant [**IVssEnumObject**](/windows/desktop/api/Vss/nn-vss-ivssenumobject) pour itérer au sein de la liste des objets retournés par un appel à [**IVssBackupComponents :: Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query).

L’objet appareil doit être interprété comme la racine d’un volume cliché instantané. Pour cette raison, l’objet appareil ne contient pas de barre oblique inverse (« \\ »).

Les chemins d’accès sur le volume des clichés instantanés sont obtenus en remplaçant la racine du chemin d’accès d’origine par l’objet de l’appareil. Par exemple, à partir d’un chemin sur le volume d’origine de « C : \\ Database \\ \* . mdb » et d’une instance de snapProp de [**\_ capture instantanée \_ VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) , vous obtenez le chemin sur le volume des clichés instantanés en concaténant snapPropm \_ pwszShadow copyDeviceObject, « \\ » et « \\ Database \\ \* . mdb ».

Les jeux de fichiers VSS peuvent contenir des caractères génériques dans leurs descripteurs de fichiers. pour obtenir une liste complète des fichiers sur un cliché instantané géré par un composant, il peut être nécessaire d’utiliser des méthodes telles que **FindFileFirst**, **FindFileFirstEx** et **FindNextFile**.

 

 



