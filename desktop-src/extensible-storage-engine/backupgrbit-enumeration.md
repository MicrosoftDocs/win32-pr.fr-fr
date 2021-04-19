---
description: 'En savoir plus sur : énumération BackupGrbit'
title: Énumération BackupGrbit
TOCTitle: BackupGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.BackupGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.backupgrbit(v=EXCHG.10)
ms:contentKeyID: 39512196
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.BackupGrbit
- Microsoft.Isam.Esent.Interop.BackupGrbit.Atomic
- Microsoft.Isam.Esent.Interop.BackupGrbit.Incremental
- Microsoft.Isam.Esent.Interop.BackupGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.BackupGrbit.Incremental
- Microsoft.Isam.Esent.Interop.BackupGrbit
- Microsoft.Isam.Esent.Interop.BackupGrbit.Atomic
- Microsoft.Isam.Esent.Interop.BackupGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bda9754efcae8ebe353b8272ba57c5640ecdf946
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530762"
---
# <a name="backupgrbit-enumeration"></a><span data-ttu-id="323c7-103">Énumération BackupGrbit</span><span class="sxs-lookup"><span data-stu-id="323c7-103">BackupGrbit enumeration</span></span>

<span data-ttu-id="323c7-104">Options pour [JetBackupInstance (JET_INSTANCE, String, BackupGrbit, JET_PFNSTATUS)](./api.jetbackupinstance-method.md).</span><span class="sxs-lookup"><span data-stu-id="323c7-104">Options for [JetBackupInstance(JET_INSTANCE, String, BackupGrbit, JET_PFNSTATUS)](./api.jetbackupinstance-method.md).</span></span>

<span data-ttu-id="323c7-105">Cette énumération a un attribut [FlagsAttribute](/dotnet/api/system.flagsattribute) qui permet une combinaison au niveau du bit de ses valeurs membres.</span><span class="sxs-lookup"><span data-stu-id="323c7-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="323c7-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="323c7-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="323c7-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="323c7-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="323c7-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="323c7-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration BackupGrbit
'Usage
Dim instance As BackupGrbit
```

``` csharp
[FlagsAttribute]
public enum BackupGrbit
```

## <a name="members"></a><span data-ttu-id="323c7-109">Membres</span><span class="sxs-lookup"><span data-stu-id="323c7-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="323c7-110">Nom du membre</span><span class="sxs-lookup"><span data-stu-id="323c7-110">Member name</span></span></th>
<th><span data-ttu-id="323c7-111">Description</span><span class="sxs-lookup"><span data-stu-id="323c7-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="323c7-112">Aucune</span><span class="sxs-lookup"><span data-stu-id="323c7-112">None</span></span></td>
<td><span data-ttu-id="323c7-113">Options par défaut.</span><span class="sxs-lookup"><span data-stu-id="323c7-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="323c7-114">Incrémentiel</span><span class="sxs-lookup"><span data-stu-id="323c7-114">Incremental</span></span></td>
<td><span data-ttu-id="323c7-115">Crée une sauvegarde incrémentielle par opposition à une sauvegarde complète.</span><span class="sxs-lookup"><span data-stu-id="323c7-115">Creates an incremental backup as opposed to a full backup.</span></span> <span data-ttu-id="323c7-116">Cela signifie que seuls les fichiers journaux créés depuis la dernière sauvegarde complète ou incrémentielle sont sauvegardés.</span><span class="sxs-lookup"><span data-stu-id="323c7-116">This means that only the log files created since the last full or incremental backup will be backed up.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="323c7-117">Atomique</span><span class="sxs-lookup"><span data-stu-id="323c7-117">Atomic</span></span></td>
<td><span data-ttu-id="323c7-118">Crée une sauvegarde complète de la base de données.</span><span class="sxs-lookup"><span data-stu-id="323c7-118">Creates a full backup of the database.</span></span> <span data-ttu-id="323c7-119">Cela permet la conservation d’une sauvegarde existante dans le même répertoire en cas d’échec de la nouvelle sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="323c7-119">This allows the preservation of an existing backup in the same directory if the new backup fails.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="323c7-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="323c7-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="323c7-121">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="323c7-121">Reference</span></span>

[<span data-ttu-id="323c7-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="323c7-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
