---
description: 'En savoir plus sur : structure JET_DBINFOUPGRADE'
title: Structure JET_DBINFOUPGRADE
TOCTitle: JET_DBINFOUPGRADE Structure
ms:assetid: dd8a881a-33b5-4314-8cfb-b1d75ad37b21
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294114(v=EXCHG.10)
ms:contentKeyID: 32765728
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9652b0050805ad116a7087cb2ec4cd146255b6a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512962"
---
# <a name="jet_dbinfoupgrade-structure"></a><span data-ttu-id="9e4c2-103">Structure JET_DBINFOUPGRADE</span><span class="sxs-lookup"><span data-stu-id="9e4c2-103">JET_DBINFOUPGRADE Structure</span></span>


<span data-ttu-id="9e4c2-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="9e4c2-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_dbinfoupgrade-structure"></a><span data-ttu-id="9e4c2-105">Structure JET_DBINFOUPGRADE</span><span class="sxs-lookup"><span data-stu-id="9e4c2-105">JET_DBINFOUPGRADE Structure</span></span>

<span data-ttu-id="9e4c2-106">La structure **JET_DBINFOUPGRADE** contient des informations sur l’état de mise à niveau de la base de données.</span><span class="sxs-lookup"><span data-stu-id="9e4c2-106">The **JET_DBINFOUPGRADE** structure holds information about the upgrade status of the database.</span></span> <span data-ttu-id="9e4c2-107">Cette valeur est récupérée uniquement si **JET_DBINFOUPGRADE** a été passé à [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) ou [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="9e4c2-107">This value is retrieved only if **JET_DBINFOUPGRADE** was passed to [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) or [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md).</span></span> <span data-ttu-id="9e4c2-108">Cette structure n’est pas requise pour les versions de système d’exploitation actuelles du moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="9e4c2-108">This structure is not required for current operating system versions of the database engine.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long cbFilesizeLow;
      unsigned long cbFilesizeHigh;
      unsigned long cbFreeSpaceRequiredLow;
      unsigned long  cbFreeSpaceRequiredHigh;
      unsigned long csecToUpgrade;
      union {
        unsigned long ulFlags;
        struct {
          unsigned long fUpgradable  :1;
          unsigned long fAlreadyUpgraded  :1;
        };
      };
    } JET_DBINFOUPGRADE;
```

### <a name="members"></a><span data-ttu-id="9e4c2-109">Membres</span><span class="sxs-lookup"><span data-stu-id="9e4c2-109">Members</span></span>

<span data-ttu-id="9e4c2-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="9e4c2-110">**cbStruct**</span></span>

<span data-ttu-id="9e4c2-111">Défini sur la taille de la structure **JET_DBINFOUPGRADE** , en octets.</span><span class="sxs-lookup"><span data-stu-id="9e4c2-111">Set to the size of the **JET_DBINFOUPGRADE** structure, in bytes.</span></span>

<span data-ttu-id="9e4c2-112">**cbFilesizeLow**</span><span class="sxs-lookup"><span data-stu-id="9e4c2-112">**cbFilesizeLow**</span></span>

<span data-ttu-id="9e4c2-113">**Valeur DWORD** basse qui reflète la taille de fichier actuelle pour la base de données.</span><span class="sxs-lookup"><span data-stu-id="9e4c2-113">The low **DWORD** that reflects the current file size for the database.</span></span>

<span data-ttu-id="9e4c2-114">**cbFilesizeHigh**</span><span class="sxs-lookup"><span data-stu-id="9e4c2-114">**cbFilesizeHigh**</span></span>

<span data-ttu-id="9e4c2-115">**Valeur DWORD** haute qui reflète la taille de fichier actuelle pour la base de données.</span><span class="sxs-lookup"><span data-stu-id="9e4c2-115">The high **DWORD** that reflects the current file size for the database.</span></span>

<span data-ttu-id="9e4c2-116">**cbFreeSpaceRequiredLow**</span><span class="sxs-lookup"><span data-stu-id="9e4c2-116">**cbFreeSpaceRequiredLow**</span></span>

<span data-ttu-id="9e4c2-117">**Valeur DWORD** faible de l’espace disque disponible estimé nécessaire pour une mise à niveau sur place.</span><span class="sxs-lookup"><span data-stu-id="9e4c2-117">The low **DWORD** of estimated free disk space required for an in-place upgrade.</span></span>

<span data-ttu-id="9e4c2-118">**cbFreeSpaceRequiredHigh**</span><span class="sxs-lookup"><span data-stu-id="9e4c2-118">**cbFreeSpaceRequiredHigh**</span></span>

<span data-ttu-id="9e4c2-119">**Valeur DWORD** élevée de l’espace disque disponible estimé requis pour une mise à niveau sur place.</span><span class="sxs-lookup"><span data-stu-id="9e4c2-119">The high **DWORD** of estimated free disk space required for an in-place upgrade.</span></span>

<span data-ttu-id="9e4c2-120">**csecToUpgrade**</span><span class="sxs-lookup"><span data-stu-id="9e4c2-120">**csecToUpgrade**</span></span>

<span data-ttu-id="9e4c2-121">Durée estimée nécessaire à la mise à niveau, en secondes.</span><span class="sxs-lookup"><span data-stu-id="9e4c2-121">The estimated time required to upgrade, in seconds.</span></span>

<span data-ttu-id="9e4c2-122">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="9e4c2-122">**ulFlags**</span></span>

<span data-ttu-id="9e4c2-123">Un champ de bits constitué de zéro, un ou plusieurs des indicateurs suivants : **fUpgradable**, **fAlreadyUpgraded**.</span><span class="sxs-lookup"><span data-stu-id="9e4c2-123">A bit field made of zero or more of the following flags: **fUpgradable**, **fAlreadyUpgraded**.</span></span>

<span data-ttu-id="9e4c2-124">**fUpgradable**</span><span class="sxs-lookup"><span data-stu-id="9e4c2-124">**fUpgradable**</span></span>

<span data-ttu-id="9e4c2-125">La base de données peut être mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="9e4c2-125">The database is upgradeable.</span></span>

<span data-ttu-id="9e4c2-126">**fAlreadyUpgraded**</span><span class="sxs-lookup"><span data-stu-id="9e4c2-126">**fAlreadyUpgraded**</span></span>

<span data-ttu-id="9e4c2-127">La base de données est mise à niveau vers le format de base de données actuel.</span><span class="sxs-lookup"><span data-stu-id="9e4c2-127">The database is upgraded to the current database format.</span></span>

### <a name="remarks"></a><span data-ttu-id="9e4c2-128">Notes</span><span class="sxs-lookup"><span data-stu-id="9e4c2-128">Remarks</span></span>

<span data-ttu-id="9e4c2-129">Une structure **JET_DBINFOUPGRADE** est remplie par un appel à [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) ou [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="9e4c2-129">A **JET_DBINFOUPGRADE** structure is populated by a call to [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) or [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md).</span></span> <span data-ttu-id="9e4c2-130">Si la fonction échoue, le contenu de la structure n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="9e4c2-130">If the function does not succeed, the contents of the structure are undefined.</span></span>

### <a name="requirements"></a><span data-ttu-id="9e4c2-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9e4c2-131">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9e4c2-132"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="9e4c2-132"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9e4c2-133">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="9e4c2-133">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e4c2-134"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="9e4c2-134"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9e4c2-135">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="9e4c2-135">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e4c2-136"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="9e4c2-136"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9e4c2-137">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="9e4c2-137">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="9e4c2-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9e4c2-138">See Also</span></span>

[<span data-ttu-id="9e4c2-139">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="9e4c2-139">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="9e4c2-140">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="9e4c2-140">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="9e4c2-141">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="9e4c2-141">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="9e4c2-142">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="9e4c2-142">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="9e4c2-143">JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="9e4c2-143">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)  
[<span data-ttu-id="9e4c2-144">JetGetObjectInfo</span><span class="sxs-lookup"><span data-stu-id="9e4c2-144">JetGetObjectInfo</span></span>](./jetgetobjectinfo-function.md)  
[<span data-ttu-id="9e4c2-145">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="9e4c2-145">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="9e4c2-146">JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="9e4c2-146">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)
