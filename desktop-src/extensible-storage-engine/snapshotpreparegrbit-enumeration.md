---
description: 'En savoir plus sur : énumération SnapshotPrepareGrbit'
title: Énumération SnapshotPrepareGrbit
TOCTitle: SnapshotPrepareGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.snapshotpreparegrbit(v=EXCHG.10)
ms:contentKeyID: 39515688
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit
- Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit.CopySnapshot
- Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit.IncrementalSnapshot
- Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit.CopySnapshot
- Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit.IncrementalSnapshot
- Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit.None
- Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 32c11c609f78cc96862f9c2f15d93266f40ae941
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318558"
---
# <a name="snapshotpreparegrbit-enumeration"></a><span data-ttu-id="5bd92-103">Énumération SnapshotPrepareGrbit</span><span class="sxs-lookup"><span data-stu-id="5bd92-103">SnapshotPrepareGrbit enumeration</span></span>

<span data-ttu-id="5bd92-104">Options pour [JetOSSnapshotPrepare (JET_OSSNAPID, SnapshotPrepareGrbit)](./api.jetossnapshotprepare-method.md).</span><span class="sxs-lookup"><span data-stu-id="5bd92-104">Options for [JetOSSnapshotPrepare(JET_OSSNAPID, SnapshotPrepareGrbit)](./api.jetossnapshotprepare-method.md).</span></span>

<span data-ttu-id="5bd92-105">Cette énumération a un attribut [FlagsAttribute](/dotnet/api/system.flagsattribute) qui permet une combinaison au niveau du bit de ses valeurs membres.</span><span class="sxs-lookup"><span data-stu-id="5bd92-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="5bd92-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5bd92-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5bd92-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5bd92-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5bd92-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5bd92-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SnapshotPrepareGrbit
'Usage
Dim instance As SnapshotPrepareGrbit
```

``` csharp
[FlagsAttribute]
public enum SnapshotPrepareGrbit
```

## <a name="members"></a><span data-ttu-id="5bd92-109">Membres</span><span class="sxs-lookup"><span data-stu-id="5bd92-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="5bd92-110">Nom du membre</span><span class="sxs-lookup"><span data-stu-id="5bd92-110">Member name</span></span></th>
<th><span data-ttu-id="5bd92-111">Description</span><span class="sxs-lookup"><span data-stu-id="5bd92-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="5bd92-112">Aucune</span><span class="sxs-lookup"><span data-stu-id="5bd92-112">None</span></span></td>
<td><span data-ttu-id="5bd92-113">Options par défaut.</span><span class="sxs-lookup"><span data-stu-id="5bd92-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="5bd92-114">IncrementalSnapshot</span><span class="sxs-lookup"><span data-stu-id="5bd92-114">IncrementalSnapshot</span></span></td>
<td><span data-ttu-id="5bd92-115">Seuls les fichiers journaux seront pris.</span><span class="sxs-lookup"><span data-stu-id="5bd92-115">Only logfiles will be taken.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="5bd92-116">CopySnapshot</span><span class="sxs-lookup"><span data-stu-id="5bd92-116">CopySnapshot</span></span></td>
<td><span data-ttu-id="5bd92-117">Instantané de copie (normal ou incrémentiel) sans troncation du journal.</span><span class="sxs-lookup"><span data-stu-id="5bd92-117">A copy snapshot (normal or incremental) with no log truncation.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="5bd92-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5bd92-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5bd92-119">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="5bd92-119">Reference</span></span>

[<span data-ttu-id="5bd92-120">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="5bd92-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
