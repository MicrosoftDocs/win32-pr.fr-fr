---
description: 'En savoir plus sur : énumération DetachDatabaseGrbit'
title: Énumération DetachDatabaseGrbit
TOCTitle: DetachDatabaseGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.detachdatabasegrbit(v=EXCHG.10)
ms:contentKeyID: 55100985
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit.ForceClose
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit.ForceCloseAndDetach
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit.ForceDetach
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit.ForceClose
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit.ForceCloseAndDetach
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit.ForceDetach
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8e67962420ee0179571da8262f17ea5279f59016
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210518"
---
# <a name="detachdatabasegrbit-enumeration"></a><span data-ttu-id="23373-103">Énumération DetachDatabaseGrbit</span><span class="sxs-lookup"><span data-stu-id="23373-103">DetachDatabaseGrbit enumeration</span></span>

<span data-ttu-id="23373-104">Options pour [JetDetachDatabase2 (JET_SESID, String, DetachDatabaseGrbit)](./api.jetdetachdatabase2-method.md).</span><span class="sxs-lookup"><span data-stu-id="23373-104">Options for [JetDetachDatabase2(JET_SESID, String, DetachDatabaseGrbit)](./api.jetdetachdatabase2-method.md).</span></span>

<span data-ttu-id="23373-105">Cette énumération a un attribut [FlagsAttribute](/dotnet/api/system.flagsattribute) qui permet une combinaison au niveau du bit de ses valeurs membres.</span><span class="sxs-lookup"><span data-stu-id="23373-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="23373-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="23373-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="23373-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="23373-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="23373-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="23373-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration DetachDatabaseGrbit
'Usage
Dim instance As DetachDatabaseGrbit
```

``` csharp
[FlagsAttribute]
public enum DetachDatabaseGrbit
```

## <a name="members"></a><span data-ttu-id="23373-109">Membres</span><span class="sxs-lookup"><span data-stu-id="23373-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="23373-110">Nom du membre</span><span class="sxs-lookup"><span data-stu-id="23373-110">Member name</span></span></th>
<th><span data-ttu-id="23373-111">Description</span><span class="sxs-lookup"><span data-stu-id="23373-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="23373-112">Aucune</span><span class="sxs-lookup"><span data-stu-id="23373-112">None</span></span></td>
<td><span data-ttu-id="23373-113">Options par défaut.</span><span class="sxs-lookup"><span data-stu-id="23373-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="23373-114">ForceDetach</span><span class="sxs-lookup"><span data-stu-id="23373-114">ForceDetach</span></span></td>
<td><span data-ttu-id="23373-115"><strong>Obsolète.</strong></span><span class="sxs-lookup"><span data-stu-id="23373-115"><strong>Obsolete.</strong></span></span> <span data-ttu-id="23373-116">Si ForceDetach est utilisé, <a href="dn350463(v=exchg.10).md">EsentForceDetachNotAllowedException</a> est retourné.</span><span class="sxs-lookup"><span data-stu-id="23373-116">If ForceDetach is used, <a href="dn350463(v=exchg.10).md">EsentForceDetachNotAllowedException</a> will be returned.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="23373-117">Fermeture forcée</span><span class="sxs-lookup"><span data-stu-id="23373-117">ForceClose</span></span></td>
<td><span data-ttu-id="23373-118"><strong>Obsolète.</strong></span><span class="sxs-lookup"><span data-stu-id="23373-118"><strong>Obsolete.</strong></span></span> <span data-ttu-id="23373-119">Fermeture forcée n’est plus utilisé.</span><span class="sxs-lookup"><span data-stu-id="23373-119">ForceClose is no longer used.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="23373-120">ForceCloseAndDetach</span><span class="sxs-lookup"><span data-stu-id="23373-120">ForceCloseAndDetach</span></span></td>
<td><span data-ttu-id="23373-121"><strong>Obsolète.</strong></span><span class="sxs-lookup"><span data-stu-id="23373-121"><strong>Obsolete.</strong></span></span> <span data-ttu-id="23373-122">Si ForceCloseAndDetach est utilisé, <a href="dn350463(v=exchg.10).md">EsentForceDetachNotAllowedException</a> est retourné.</span><span class="sxs-lookup"><span data-stu-id="23373-122">If ForceCloseAndDetach is used, <a href="dn350463(v=exchg.10).md">EsentForceDetachNotAllowedException</a> will be returned.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="23373-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="23373-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="23373-124">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="23373-124">Reference</span></span>

[<span data-ttu-id="23373-125">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="23373-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
