---
description: 'En savoir plus sur : énumération EndExternalBackupGrbit'
title: Énumération EndExternalBackupGrbit
TOCTitle: EndExternalBackupGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.endexternalbackupgrbit(v=EXCHG.10)
ms:contentKeyID: 39516835
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit.Abort
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit.None
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit.Normal
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit.Abort
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit.None
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit.Normal
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0bb3fb2f3e959d41c042589f3a280e6466fe4970
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210703"
---
# <a name="endexternalbackupgrbit-enumeration"></a><span data-ttu-id="81508-103">Énumération EndExternalBackupGrbit</span><span class="sxs-lookup"><span data-stu-id="81508-103">EndExternalBackupGrbit enumeration</span></span>

<span data-ttu-id="81508-104">Options pour [JetEndExternalBackupInstance (JET_INSTANCE)](./api.jetendexternalbackupinstance-method.md).</span><span class="sxs-lookup"><span data-stu-id="81508-104">Options for [JetEndExternalBackupInstance(JET_INSTANCE)](./api.jetendexternalbackupinstance-method.md).</span></span>

<span data-ttu-id="81508-105">Cette énumération a un attribut [FlagsAttribute](/dotnet/api/system.flagsattribute) qui permet une combinaison au niveau du bit de ses valeurs membres.</span><span class="sxs-lookup"><span data-stu-id="81508-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="81508-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="81508-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="81508-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="81508-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="81508-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="81508-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration EndExternalBackupGrbit
'Usage
Dim instance As EndExternalBackupGrbit
```

``` csharp
[FlagsAttribute]
public enum EndExternalBackupGrbit
```

## <a name="members"></a><span data-ttu-id="81508-109">Membres</span><span class="sxs-lookup"><span data-stu-id="81508-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="81508-110">Nom du membre</span><span class="sxs-lookup"><span data-stu-id="81508-110">Member name</span></span></th>
<th><span data-ttu-id="81508-111">Description</span><span class="sxs-lookup"><span data-stu-id="81508-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="81508-112">Aucune</span><span class="sxs-lookup"><span data-stu-id="81508-112">None</span></span></td>
<td><span data-ttu-id="81508-113">Options par défaut.</span><span class="sxs-lookup"><span data-stu-id="81508-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="81508-114">Normal</span><span class="sxs-lookup"><span data-stu-id="81508-114">Normal</span></span></td>
<td><span data-ttu-id="81508-115">L’application cliente a complètement terminé la sauvegarde et se termine normalement.</span><span class="sxs-lookup"><span data-stu-id="81508-115">The client application finished the backup completely, and is ending normally.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="81508-116">Abandon</span><span class="sxs-lookup"><span data-stu-id="81508-116">Abort</span></span></td>
<td><span data-ttu-id="81508-117">L’application cliente abandonne la sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="81508-117">The client application is aborting the backup.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="81508-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81508-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="81508-119">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="81508-119">Reference</span></span>

[<span data-ttu-id="81508-120">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="81508-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
