---
description: 'En savoir plus sur : structure JET_INSTANCE_INFO'
title: Structure JET_INSTANCE_INFO
TOCTitle: JET_INSTANCE_INFO Structure
ms:assetid: 8cdd2e48-f1bb-465b-aefc-ffe441bf88a1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269331(v=EXCHG.10)
ms:contentKeyID: 32765621
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fd07d11a8b30e75f30bc5bfcaa3aca665baf1209
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868381"
---
# <a name="jet_instance_info-structure"></a><span data-ttu-id="2d64e-103">Structure JET_INSTANCE_INFO</span><span class="sxs-lookup"><span data-stu-id="2d64e-103">JET_INSTANCE_INFO Structure</span></span>


<span data-ttu-id="2d64e-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="2d64e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_instance_info-structure"></a><span data-ttu-id="2d64e-105">Structure JET_INSTANCE_INFO</span><span class="sxs-lookup"><span data-stu-id="2d64e-105">JET_INSTANCE_INFO Structure</span></span>

<span data-ttu-id="2d64e-106">La structure **JET_INSTANCE_INFO** reçoit des informations sur l’exécution d’instances de base de données lorsqu’elle est utilisée avec les fonctions [JetGetInstanceInfo](./jetgetinstanceinfo-function.md) et [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) .</span><span class="sxs-lookup"><span data-stu-id="2d64e-106">The **JET_INSTANCE_INFO** structure receives information about running database instances when used with the [JetGetInstanceInfo](./jetgetinstanceinfo-function.md) and [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) functions.</span></span>

```cpp
    typedef struct _JET_INSTANCE_INFO {
      JET_INSTANCE hInstanceId;
      tchar* szInstanceName;
      JET_API_PTR cDatabases;
      tchar** szDatabaseFileName;
      tchar** szDatabaseDisplayName;
      tchar** szDatabaseSLVFileName;
    } JET_INSTANCE_INFO;
```

### <a name="members"></a><span data-ttu-id="2d64e-107">Membres</span><span class="sxs-lookup"><span data-stu-id="2d64e-107">Members</span></span>

<span data-ttu-id="2d64e-108">**hInstanceId**</span><span class="sxs-lookup"><span data-stu-id="2d64e-108">**hInstanceId**</span></span>

<span data-ttu-id="2d64e-109">[JET_INSTANCE](./jet-instance.md) de l’instance donnée.</span><span class="sxs-lookup"><span data-stu-id="2d64e-109">The [JET_INSTANCE](./jet-instance.md) of the given instance.</span></span>

<span data-ttu-id="2d64e-110">**szInstanceName**</span><span class="sxs-lookup"><span data-stu-id="2d64e-110">**szInstanceName**</span></span>

<span data-ttu-id="2d64e-111">Nom de l'instance de base de données.</span><span class="sxs-lookup"><span data-stu-id="2d64e-111">The name of the database instance.</span></span> <span data-ttu-id="2d64e-112">Cette valeur peut être **null** si l’instance n’a pas de nom.</span><span class="sxs-lookup"><span data-stu-id="2d64e-112">This value can be **NULL** if the instance does not have a name.</span></span>

<span data-ttu-id="2d64e-113">**cDatabases**</span><span class="sxs-lookup"><span data-stu-id="2d64e-113">**cDatabases**</span></span>

<span data-ttu-id="2d64e-114">Nombre de bases de données attachées à l’instance de base de données.</span><span class="sxs-lookup"><span data-stu-id="2d64e-114">The number of databases that are attached to the database instance.</span></span> <span data-ttu-id="2d64e-115">**cDatabases** contient également la taille des tableaux de chaînes retournées dans **szDatabaseFileName**, **szDatabaseDisplayName** et **szDatabaseSLVFileName**.</span><span class="sxs-lookup"><span data-stu-id="2d64e-115">**cDatabases** also holds the size of the arrays of strings that are returned in **szDatabaseFileName**, **szDatabaseDisplayName**, and **szDatabaseSLVFileName**.</span></span>

<span data-ttu-id="2d64e-116">**szDatabaseFileName**</span><span class="sxs-lookup"><span data-stu-id="2d64e-116">**szDatabaseFileName**</span></span>

<span data-ttu-id="2d64e-117">Tableau de chaînes, chacune contenant le nom de fichier d’une base de données attachée à l’instance de base de données.</span><span class="sxs-lookup"><span data-stu-id="2d64e-117">An array of strings, each holding the file name of a database that is attached to the database instance.</span></span> <span data-ttu-id="2d64e-118">Le tableau contient des éléments **cDatabases** .</span><span class="sxs-lookup"><span data-stu-id="2d64e-118">The array has **cDatabases** elements.</span></span>

<span data-ttu-id="2d64e-119">**szDatabaseDisplayName**</span><span class="sxs-lookup"><span data-stu-id="2d64e-119">**szDatabaseDisplayName**</span></span>

<span data-ttu-id="2d64e-120">Tableau de chaînes, chacune contenant le nom complet d’une base de données.</span><span class="sxs-lookup"><span data-stu-id="2d64e-120">An array of strings, each holding the display name of a database.</span></span> <span data-ttu-id="2d64e-121">Actuellement, la chaîne peut être NULL.</span><span class="sxs-lookup"><span data-stu-id="2d64e-121">Currently the string can be NULL.</span></span> <span data-ttu-id="2d64e-122">Le tableau contient des éléments **cDatabases** .</span><span class="sxs-lookup"><span data-stu-id="2d64e-122">The array has **cDatabases** elements.</span></span>

<span data-ttu-id="2d64e-123">**szDatabaseSLVFileName**</span><span class="sxs-lookup"><span data-stu-id="2d64e-123">**szDatabaseSLVFileName**</span></span>

<span data-ttu-id="2d64e-124">Tableau de chaînes contenant le nom de fichier du fichier SLV attaché à l’instance de base de données.</span><span class="sxs-lookup"><span data-stu-id="2d64e-124">An array of strings, each holding the file name of the SLV file that is attached to the database instance.</span></span> <span data-ttu-id="2d64e-125">Le tableau contient des éléments **cDatabases** .</span><span class="sxs-lookup"><span data-stu-id="2d64e-125">The array has **cDatabases** elements.</span></span> <span data-ttu-id="2d64e-126">Comme les fichiers SLV ne sont pas pris en charge, ce champ doit être ignoré.</span><span class="sxs-lookup"><span data-stu-id="2d64e-126">SLV files are not supported, so this field should be ignored.</span></span>

### <a name="remarks"></a><span data-ttu-id="2d64e-127">Notes</span><span class="sxs-lookup"><span data-stu-id="2d64e-127">Remarks</span></span>

<span data-ttu-id="2d64e-128">Plusieurs bases de données peuvent être attachées à chaque instance de base de données.</span><span class="sxs-lookup"><span data-stu-id="2d64e-128">Each database instance can have several databases attached to it.</span></span>

<span data-ttu-id="2d64e-129">Pour une structure de **JET_INSTANCE_INFO** donnée, le tableau de chaînes retourné pour les bases de données est dans le même ordre.</span><span class="sxs-lookup"><span data-stu-id="2d64e-129">For a given **JET_INSTANCE_INFO** structure, the array of strings that is returned for the databases are in the same order.</span></span> <span data-ttu-id="2d64e-130">Par exemple, « szDatabaseDisplayName \[ i \] » et « szDatabaseFileName \[ i \] » font tous deux référence à la même base de données.</span><span class="sxs-lookup"><span data-stu-id="2d64e-130">For example, "szDatabaseDisplayName\[ i \]" and "szDatabaseFileName\[ i \]" both refer to the same database.</span></span>

### <a name="requirements"></a><span data-ttu-id="2d64e-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2d64e-131">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2d64e-132"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="2d64e-132"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="2d64e-133">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="2d64e-133">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d64e-134"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="2d64e-134"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="2d64e-135">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="2d64e-135">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d64e-136"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="2d64e-136"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="2d64e-137">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="2d64e-137">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d64e-138"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="2d64e-138"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="2d64e-139">Implémenté comme <strong>JET_INSTANCE_INFO_W</strong> (Unicode) et <strong>JET_INSTANCE_INFO _a</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="2d64e-139">Implemented as <strong>JET_INSTANCE_INFO_W</strong> (Unicode) and <strong>JET_INSTANCE_INFO _A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="2d64e-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d64e-140">See Also</span></span>

[<span data-ttu-id="2d64e-141">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="2d64e-141">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="2d64e-142">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="2d64e-142">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="2d64e-143">JetGetInstanceInfo</span><span class="sxs-lookup"><span data-stu-id="2d64e-143">JetGetInstanceInfo</span></span>](./jetgetinstanceinfo-function.md)  
[<span data-ttu-id="2d64e-144">JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="2d64e-144">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)
