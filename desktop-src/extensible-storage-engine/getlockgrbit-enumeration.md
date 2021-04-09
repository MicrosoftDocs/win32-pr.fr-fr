---
description: 'En savoir plus sur : énumération GetLockGrbit'
title: Énumération GetLockGrbit
TOCTitle: GetLockGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.GetLockGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.getlockgrbit(v=EXCHG.10)
ms:contentKeyID: 39512424
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.GetLockGrbit
- Microsoft.Isam.Esent.Interop.GetLockGrbit.Read
- Microsoft.Isam.Esent.Interop.GetLockGrbit.Write
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.GetLockGrbit.Read
- Microsoft.Isam.Esent.Interop.GetLockGrbit
- Microsoft.Isam.Esent.Interop.GetLockGrbit.Write
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2cfcad088fa93d73910a0333d3aca9a700e97996
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951495"
---
# <a name="getlockgrbit-enumeration"></a><span data-ttu-id="20114-103">Énumération GetLockGrbit</span><span class="sxs-lookup"><span data-stu-id="20114-103">GetLockGrbit enumeration</span></span>

<span data-ttu-id="20114-104">Options pour JetGetLock.</span><span class="sxs-lookup"><span data-stu-id="20114-104">Options for JetGetLock.</span></span>

<span data-ttu-id="20114-105">Cette énumération a un attribut [FlagsAttribute](/dotnet/api/system.flagsattribute) qui permet une combinaison au niveau du bit de ses valeurs membres.</span><span class="sxs-lookup"><span data-stu-id="20114-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="20114-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="20114-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="20114-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="20114-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="20114-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="20114-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration GetLockGrbit
'Usage
Dim instance As GetLockGrbit
```

``` csharp
[FlagsAttribute]
public enum GetLockGrbit
```

## <a name="members"></a><span data-ttu-id="20114-109">Membres</span><span class="sxs-lookup"><span data-stu-id="20114-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="20114-110">Nom du membre</span><span class="sxs-lookup"><span data-stu-id="20114-110">Member name</span></span></th>
<th><span data-ttu-id="20114-111">Description</span><span class="sxs-lookup"><span data-stu-id="20114-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="20114-112">Lire</span><span class="sxs-lookup"><span data-stu-id="20114-112">Read</span></span></td>
<td><span data-ttu-id="20114-113">Acquérir un verrou de lecture sur l’enregistrement en cours.</span><span class="sxs-lookup"><span data-stu-id="20114-113">Acquire a read lock on the current record.</span></span> <span data-ttu-id="20114-114">Les verrous de lecture sont incompatibles avec les verrous d’écriture déjà détenues par d’autres sessions, mais sont compatibles avec les verrous de lecture détenus par d’autres sessions.</span><span class="sxs-lookup"><span data-stu-id="20114-114">Read locks are incompatible with write locks already held by other sessions but are compatible with read locks held by other sessions.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="20114-115">Write</span><span class="sxs-lookup"><span data-stu-id="20114-115">Write</span></span></td>
<td><span data-ttu-id="20114-116">Acquérir un verrou d’écriture sur l’enregistrement en cours.</span><span class="sxs-lookup"><span data-stu-id="20114-116">Acquire a write lock on the current record.</span></span> <span data-ttu-id="20114-117">Les verrous d’écriture ne sont pas compatibles avec les verrous d’écriture ou de lecture détenus par d’autres sessions, mais sont compatibles avec les verrous de lecture détenus par la même session.</span><span class="sxs-lookup"><span data-stu-id="20114-117">Write locks are not compatible with write or read locks held by other sessions but are compatible with read locks held by the same session.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="20114-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20114-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="20114-119">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="20114-119">Reference</span></span>

[<span data-ttu-id="20114-120">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="20114-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
