---
description: 'En savoir plus sur : énumération AttachDatabaseGrbit'
title: Énumération AttachDatabaseGrbit
TOCTitle: AttachDatabaseGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.attachdatabasegrbit(v=EXCHG.10)
ms:contentKeyID: 39514410
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit.DeleteCorruptIndexes
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit.ReadOnly
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit.DeleteCorruptIndexes
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit.ReadOnly
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 81525e97f1b6266ba15baab50168404566bd7bcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531407"
---
# <a name="attachdatabasegrbit-enumeration"></a><span data-ttu-id="95e89-103">Énumération AttachDatabaseGrbit</span><span class="sxs-lookup"><span data-stu-id="95e89-103">AttachDatabaseGrbit enumeration</span></span>

<span data-ttu-id="95e89-104">Options pour JetAttachDatabase.</span><span class="sxs-lookup"><span data-stu-id="95e89-104">Options for JetAttachDatabase.</span></span>

<span data-ttu-id="95e89-105">Cette énumération a un attribut [FlagsAttribute](/dotnet/api/system.flagsattribute) qui permet une combinaison au niveau du bit de ses valeurs membres.</span><span class="sxs-lookup"><span data-stu-id="95e89-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="95e89-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="95e89-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="95e89-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="95e89-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="95e89-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="95e89-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration AttachDatabaseGrbit
'Usage
Dim instance As AttachDatabaseGrbit
```

``` csharp
[FlagsAttribute]
public enum AttachDatabaseGrbit
```

## <a name="members"></a><span data-ttu-id="95e89-109">Membres</span><span class="sxs-lookup"><span data-stu-id="95e89-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="95e89-110">Nom du membre</span><span class="sxs-lookup"><span data-stu-id="95e89-110">Member name</span></span></th>
<th><span data-ttu-id="95e89-111">Description</span><span class="sxs-lookup"><span data-stu-id="95e89-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="95e89-112">Aucune</span><span class="sxs-lookup"><span data-stu-id="95e89-112">None</span></span></td>
<td><span data-ttu-id="95e89-113">Options par défaut.</span><span class="sxs-lookup"><span data-stu-id="95e89-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="95e89-114">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95e89-114">ReadOnly</span></span></td>
<td><span data-ttu-id="95e89-115">Empêche toute modification de la base de données.</span><span class="sxs-lookup"><span data-stu-id="95e89-115">Prevents modifications to the database.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="95e89-116">DeleteCorruptIndexes</span><span class="sxs-lookup"><span data-stu-id="95e89-116">DeleteCorruptIndexes</span></span></td>
<td><span data-ttu-id="95e89-117">Si JET_paramEnableIndexChecking a été défini, tous les index sur les données Unicode seront supprimés.</span><span class="sxs-lookup"><span data-stu-id="95e89-117">If JET_paramEnableIndexChecking has been set, all indexes over Unicode data will be deleted.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="95e89-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="95e89-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="95e89-119">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="95e89-119">Reference</span></span>

[<span data-ttu-id="95e89-120">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="95e89-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
