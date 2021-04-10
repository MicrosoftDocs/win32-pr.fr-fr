---
description: Une fois le cliché instantané terminé, le mécanisme le plus important pour obtenir l’accès aux données de fichier qu’il contient consiste à utiliser l’objet appareil du cliché instantané.
ms.assetid: 21efdbd6-a487-4e6f-8e3c-b9224bcf92da
title: Accès du demandeur aux données des clichés instantanés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6265586f70054277170b44f23efc52d56842e3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115150"
---
# <a name="requester-access-to-shadow-copied-data"></a><span data-ttu-id="4c40c-103">Accès du demandeur aux données des clichés instantanés</span><span class="sxs-lookup"><span data-stu-id="4c40c-103">Requester Access to Shadow Copied Data</span></span>

<span data-ttu-id="4c40c-104">Une fois le cliché instantané terminé, le mécanisme le plus important pour obtenir l’accès aux données de fichier qu’il contient consiste à utiliser l' [*objet appareil*](vssgloss-d.md)du cliché instantané.</span><span class="sxs-lookup"><span data-stu-id="4c40c-104">Once the shadow copy has completed, the most important mechanism for getting access to the file data it contains is through the use of the shadow copy's [*device object*](vssgloss-d.md).</span></span>

<span data-ttu-id="4c40c-105">Le membre **m \_ pwszSnapshotDeviceObject** d’une structure de [**\_ \_ Propriétés de capture instantanée VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) est une chaîne contenant un objet périphérique de volume cliché instantané.</span><span class="sxs-lookup"><span data-stu-id="4c40c-105">The **m\_pwszSnapshotDeviceObject** member of a [**VSS\_SNAPSHOT\_PROP**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) structure is a string containing a shadow-copied volume's device object.</span></span> <span data-ttu-id="4c40c-106">Un demandeur peut obtenir l’objet de la **\_ \_ prop instantané VSS** d’un volume cliché instantané s’il connaît l' **\_ ID VSS** du volume (GUID d’identification) et le transmet à [**IVssBackupComponents :: GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties).</span><span class="sxs-lookup"><span data-stu-id="4c40c-106">A requester can obtain a shadow-copied volume's **VSS\_SNAPSHOT\_PROP** object if it knows the volume's **VSS\_ID** (identifying GUID) and passes it to [**IVssBackupComponents::GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties).</span></span>

<span data-ttu-id="4c40c-107">Un demandeur peut également obtenir des informations sur les propriétés des clichés instantanés à l’aide du membre **obj. Snap** de la structure de l' [**\_ objet VSS \_**](/windows/desktop/api/Vss/ns-vss-vss_object_prop) (qui est une structure de [**\_ \_ prop instantanés VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) ) obtenue en utilisant [**IVssEnumObject**](/windows/desktop/api/Vss/nn-vss-ivssenumobject) pour itérer au sein de la liste des objets retournés par un appel à [**IVssBackupComponents :: Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query).</span><span class="sxs-lookup"><span data-stu-id="4c40c-107">A requester can also obtain shadow copy property information by using the **Obj.Snap** member of the [**VSS\_OBJECT\_PROP**](/windows/desktop/api/Vss/ns-vss-vss_object_prop) structure (which is a [**VSS\_SNAPSHOT\_PROP**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) structure) obtained by using [**IVssEnumObject**](/windows/desktop/api/Vss/nn-vss-ivssenumobject) to iterate over the list of objects returned by a call to [**IVssBackupComponents::Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query).</span></span>

<span data-ttu-id="4c40c-108">L’objet appareil doit être interprété comme la racine d’un volume cliché instantané.</span><span class="sxs-lookup"><span data-stu-id="4c40c-108">The device object should be interpreted as the root of a shadow-copied volume.</span></span> <span data-ttu-id="4c40c-109">Pour cette raison, l’objet appareil ne contient pas de barre oblique inverse (« \\ »).</span><span class="sxs-lookup"><span data-stu-id="4c40c-109">For this reason, the device object contains no backslash ("\\").</span></span>

<span data-ttu-id="4c40c-110">Les chemins d’accès sur le volume des clichés instantanés sont obtenus en remplaçant la racine du chemin d’accès d’origine par l’objet de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="4c40c-110">Paths on the shadow copied volume are obtained by replacing the root of the original path with the device object.</span></span> <span data-ttu-id="4c40c-111">Par exemple, à partir d’un chemin sur le volume d’origine de « C : \\ Database \\ \* . mdb » et d’une instance de snapProp de [**\_ capture instantanée \_ VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) , vous obtenez le chemin sur le volume des clichés instantanés en concaténant snapPropm \_ pwszShadow copyDeviceObject, « \\ » et « \\ Database \\ \* . mdb ».</span><span class="sxs-lookup"><span data-stu-id="4c40c-111">For example, given a path on the original volume of "C:\\DATABASE\\\*.mdb" and a [**VSS\_SNAPSHOT\_PROP**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) instance of snapProp, you would obtain the path on the shadow copied volume by concatenating snapPropm\_pwszShadow copyDeviceObject, "\\", and "\\DATABASE\\\*.mdb".</span></span>

<span data-ttu-id="4c40c-112">Les jeux de fichiers VSS peuvent contenir des caractères génériques dans leurs descripteurs de fichiers. pour obtenir une liste complète des fichiers sur un cliché instantané géré par un composant, il peut être nécessaire d’utiliser des méthodes telles que **FindFileFirst**, **FindFileFirstEx** et **FindNextFile**.</span><span class="sxs-lookup"><span data-stu-id="4c40c-112">The VSS file sets might have wildcard characters in their file descriptors, so obtaining a full list of the files on a shadow copy managed by a component might require the use of methods such as **FindFileFirst**, **FindFileFirstEx**, and **FindNextFile**.</span></span>

 

 



