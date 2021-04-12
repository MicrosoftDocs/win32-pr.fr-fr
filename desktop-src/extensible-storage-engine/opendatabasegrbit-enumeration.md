---
description: 'En savoir plus sur : énumération OpenDatabaseGrbit'
title: Énumération OpenDatabaseGrbit
TOCTitle: OpenDatabaseGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.opendatabasegrbit(v=EXCHG.10)
ms:contentKeyID: 39514563
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit.Exclusive
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit.ReadOnly
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit.ReadOnly
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit.Exclusive
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d14fb779ec02137f6a4fce1cfdd92f46dedcb832
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203130"
---
# <a name="opendatabasegrbit-enumeration"></a><span data-ttu-id="8a5ec-103">Énumération OpenDatabaseGrbit</span><span class="sxs-lookup"><span data-stu-id="8a5ec-103">OpenDatabaseGrbit enumeration</span></span>

<span data-ttu-id="8a5ec-104">Options pour [JetOpenDatabase (JET_SESID, String, String, JET_DBID, OpenDatabaseGrbit)](./api.jetopendatabase-method.md).</span><span class="sxs-lookup"><span data-stu-id="8a5ec-104">Options for [JetOpenDatabase(JET_SESID, String, String, JET_DBID, OpenDatabaseGrbit)](./api.jetopendatabase-method.md).</span></span>

<span data-ttu-id="8a5ec-105">Cette énumération a un attribut [FlagsAttribute](/dotnet/api/system.flagsattribute) qui permet une combinaison au niveau du bit de ses valeurs membres.</span><span class="sxs-lookup"><span data-stu-id="8a5ec-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="8a5ec-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8a5ec-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8a5ec-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8a5ec-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8a5ec-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8a5ec-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration OpenDatabaseGrbit
'Usage
Dim instance As OpenDatabaseGrbit
```

``` csharp
[FlagsAttribute]
public enum OpenDatabaseGrbit
```

## <a name="members"></a><span data-ttu-id="8a5ec-109">Membres</span><span class="sxs-lookup"><span data-stu-id="8a5ec-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="8a5ec-110">Nom du membre</span><span class="sxs-lookup"><span data-stu-id="8a5ec-110">Member name</span></span></th>
<th><span data-ttu-id="8a5ec-111">Description</span><span class="sxs-lookup"><span data-stu-id="8a5ec-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="8a5ec-112">Aucune</span><span class="sxs-lookup"><span data-stu-id="8a5ec-112">None</span></span></td>
<td><span data-ttu-id="8a5ec-113">Options par défaut.</span><span class="sxs-lookup"><span data-stu-id="8a5ec-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="8a5ec-114">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8a5ec-114">ReadOnly</span></span></td>
<td><span data-ttu-id="8a5ec-115">Empêche toute modification de la base de données.</span><span class="sxs-lookup"><span data-stu-id="8a5ec-115">Prevents modifications to the database.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="8a5ec-116">Exclusif</span><span class="sxs-lookup"><span data-stu-id="8a5ec-116">Exclusive</span></span></td>
<td><span data-ttu-id="8a5ec-117">Autorise une seule session à attacher une base de données.</span><span class="sxs-lookup"><span data-stu-id="8a5ec-117">Allows only a single session to attach a database.</span></span> <span data-ttu-id="8a5ec-118">En règle générale, plusieurs sessions peuvent ouvrir une base de données.</span><span class="sxs-lookup"><span data-stu-id="8a5ec-118">Normally, several sessions can open a database.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="8a5ec-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a5ec-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8a5ec-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="8a5ec-120">Reference</span></span>

[<span data-ttu-id="8a5ec-121">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="8a5ec-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
