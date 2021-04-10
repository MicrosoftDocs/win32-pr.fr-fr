---
description: 'En savoir plus sur : énumération CreateTableColumnIndexGrbit'
title: Énumération CreateTableColumnIndexGrbit
TOCTitle: CreateTableColumnIndexGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.createtablecolumnindexgrbit(v=EXCHG.10)
ms:contentKeyID: 39516657
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.FixedDDL
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.NoFixedVarColumnsInDerivedTables
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.None
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.TemplateTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.TemplateTable
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.NoFixedVarColumnsInDerivedTables
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.FixedDDL
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 72f91c5d41b8262e3b2804159914b0a9ccaaaa7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953033"
---
# <a name="createtablecolumnindexgrbit-enumeration"></a><span data-ttu-id="edabd-103">Énumération CreateTableColumnIndexGrbit</span><span class="sxs-lookup"><span data-stu-id="edabd-103">CreateTableColumnIndexGrbit enumeration</span></span>

<span data-ttu-id="edabd-104">Options pour JetCreateTableColumnIndex.</span><span class="sxs-lookup"><span data-stu-id="edabd-104">Options for JetCreateTableColumnIndex.</span></span>

<span data-ttu-id="edabd-105">Cette énumération a un attribut [FlagsAttribute](/dotnet/api/system.flagsattribute) qui permet une combinaison au niveau du bit de ses valeurs membres.</span><span class="sxs-lookup"><span data-stu-id="edabd-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="edabd-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="edabd-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="edabd-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="edabd-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="edabd-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="edabd-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CreateTableColumnIndexGrbit
'Usage
Dim instance As CreateTableColumnIndexGrbit
```

``` csharp
[FlagsAttribute]
public enum CreateTableColumnIndexGrbit
```

## <a name="members"></a><span data-ttu-id="edabd-109">Membres</span><span class="sxs-lookup"><span data-stu-id="edabd-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="edabd-110">Nom du membre</span><span class="sxs-lookup"><span data-stu-id="edabd-110">Member name</span></span></th>
<th><span data-ttu-id="edabd-111">Description</span><span class="sxs-lookup"><span data-stu-id="edabd-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="edabd-112">Aucune</span><span class="sxs-lookup"><span data-stu-id="edabd-112">None</span></span></td>
<td><span data-ttu-id="edabd-113">Options par défaut.</span><span class="sxs-lookup"><span data-stu-id="edabd-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="edabd-114">FixedDDL</span><span class="sxs-lookup"><span data-stu-id="edabd-114">FixedDDL</span></span></td>
<td><span data-ttu-id="edabd-115">Le DDL est fixe.</span><span class="sxs-lookup"><span data-stu-id="edabd-115">The DDL is fixed.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="edabd-116">TemplateTable</span><span class="sxs-lookup"><span data-stu-id="edabd-116">TemplateTable</span></span></td>
<td><span data-ttu-id="edabd-117">Le DDL peut être hérité.</span><span class="sxs-lookup"><span data-stu-id="edabd-117">The DDL is inheritable.</span></span> <span data-ttu-id="edabd-118">Implique FixedDDL.</span><span class="sxs-lookup"><span data-stu-id="edabd-118">Implies FixedDDL.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="edabd-119">NoFixedVarColumnsInDerivedTables</span><span class="sxs-lookup"><span data-stu-id="edabd-119">NoFixedVarColumnsInDerivedTables</span></span></td>
<td><span data-ttu-id="edabd-120">Utilisé conjointement avec TemplateTable.</span><span class="sxs-lookup"><span data-stu-id="edabd-120">Used in conjunction with TemplateTable.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="edabd-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="edabd-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="edabd-122">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="edabd-122">Reference</span></span>

[<span data-ttu-id="edabd-123">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="edabd-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
