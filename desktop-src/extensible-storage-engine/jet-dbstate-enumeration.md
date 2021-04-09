---
description: 'En savoir plus sur : énumération JET_dbstate'
title: Énumération JET_dbstate
TOCTitle: JET_dbstate enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_dbstate
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbstate(v=EXCHG.10)
ms:contentKeyID: 39511841
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_dbstate
- Microsoft.Isam.Esent.Interop.JET_dbstate.BeingConverted
- Microsoft.Isam.Esent.Interop.JET_dbstate.CleanShutdown
- Microsoft.Isam.Esent.Interop.JET_dbstate.DirtyShutdown
- Microsoft.Isam.Esent.Interop.JET_dbstate.ForceDetach
- Microsoft.Isam.Esent.Interop.JET_dbstate.JustCreated
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_dbstate.JustCreated
- Microsoft.Isam.Esent.Interop.JET_dbstate.BeingConverted
- Microsoft.Isam.Esent.Interop.JET_dbstate.CleanShutdown
- Microsoft.Isam.Esent.Interop.JET_dbstate.ForceDetach
- Microsoft.Isam.Esent.Interop.JET_dbstate.DirtyShutdown
- Microsoft.Isam.Esent.Interop.JET_dbstate
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a83c8a4313e5e6f21ee885ee7936c90503bfbd3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749884"
---
# <a name="jet_dbstate-enumeration"></a><span data-ttu-id="30dd2-103">Énumération JET_dbstate</span><span class="sxs-lookup"><span data-stu-id="30dd2-103">JET_dbstate enumeration</span></span>

<span data-ttu-id="30dd2-104">États de base de données (utilisés dans [JET_DBINFOMISC](./jet-dbinfomisc-class.md)).</span><span class="sxs-lookup"><span data-stu-id="30dd2-104">Database states (used in [JET_DBINFOMISC](./jet-dbinfomisc-class.md)).</span></span>

<span data-ttu-id="30dd2-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="30dd2-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="30dd2-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="30dd2-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="30dd2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="30dd2-107">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_dbstate
'Usage
Dim instance As JET_dbstate
```

``` csharp
public enum JET_dbstate
```

## <a name="members"></a><span data-ttu-id="30dd2-108">Membres</span><span class="sxs-lookup"><span data-stu-id="30dd2-108">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="30dd2-109">Nom du membre</span><span class="sxs-lookup"><span data-stu-id="30dd2-109">Member name</span></span></th>
<th><span data-ttu-id="30dd2-110">Description</span><span class="sxs-lookup"><span data-stu-id="30dd2-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="30dd2-111">JustCreated</span><span class="sxs-lookup"><span data-stu-id="30dd2-111">JustCreated</span></span></td>
<td><span data-ttu-id="30dd2-112">La base de données vient d’être créée.</span><span class="sxs-lookup"><span data-stu-id="30dd2-112">The database was just created.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="30dd2-113">DirtyShutdown</span><span class="sxs-lookup"><span data-stu-id="30dd2-113">DirtyShutdown</span></span></td>
<td><span data-ttu-id="30dd2-114">Base de données d’arrêt (incohérent) incorrecte.</span><span class="sxs-lookup"><span data-stu-id="30dd2-114">Dirty shutdown (inconsistent) database.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="30dd2-115">CleanShutdown</span><span class="sxs-lookup"><span data-stu-id="30dd2-115">CleanShutdown</span></span></td>
<td><span data-ttu-id="30dd2-116">Base de données d’arrêt propre (cohérent).</span><span class="sxs-lookup"><span data-stu-id="30dd2-116">Clean shutdown (consistent) database.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="30dd2-117">BeingConverted</span><span class="sxs-lookup"><span data-stu-id="30dd2-117">BeingConverted</span></span></td>
<td><span data-ttu-id="30dd2-118">La base de données est en cours de conversion.</span><span class="sxs-lookup"><span data-stu-id="30dd2-118">Database is being converted.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="30dd2-119">ForceDetach</span><span class="sxs-lookup"><span data-stu-id="30dd2-119">ForceDetach</span></span></td>
<td><span data-ttu-id="30dd2-120">La base de données a été détachée de force.</span><span class="sxs-lookup"><span data-stu-id="30dd2-120">Database was force-detached.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="30dd2-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30dd2-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="30dd2-122">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="30dd2-122">Reference</span></span>

[<span data-ttu-id="30dd2-123">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="30dd2-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
