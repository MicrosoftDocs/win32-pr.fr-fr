---
description: 'En savoir plus sur : énumération BeginTransactionGrbit'
title: Énumération BeginTransactionGrbit
TOCTitle: BeginTransactionGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.BeginTransactionGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.begintransactiongrbit(v=EXCHG.10)
ms:contentKeyID: 39515115
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.BeginTransactionGrbit
- Microsoft.Isam.Esent.Interop.BeginTransactionGrbit.None
- Microsoft.Isam.Esent.Interop.BeginTransactionGrbit.ReadOnly
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.BeginTransactionGrbit.None
- Microsoft.Isam.Esent.Interop.BeginTransactionGrbit
- Microsoft.Isam.Esent.Interop.BeginTransactionGrbit.ReadOnly
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5f407c54b7b6e76ab63dcfb97d1307458ba15277
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758968"
---
# <a name="begintransactiongrbit-enumeration"></a><span data-ttu-id="d931a-103">Énumération BeginTransactionGrbit</span><span class="sxs-lookup"><span data-stu-id="d931a-103">BeginTransactionGrbit enumeration</span></span>

<span data-ttu-id="d931a-104">Options pour [JetBeginTransaction2 (JET_SESID, BeginTransactionGrbit)](./api.jetbegintransaction2-method.md).</span><span class="sxs-lookup"><span data-stu-id="d931a-104">Options for [JetBeginTransaction2(JET_SESID, BeginTransactionGrbit)](./api.jetbegintransaction2-method.md).</span></span>

<span data-ttu-id="d931a-105">Cette énumération a un attribut [FlagsAttribute](/dotnet/api/system.flagsattribute) qui permet une combinaison au niveau du bit de ses valeurs membres.</span><span class="sxs-lookup"><span data-stu-id="d931a-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="d931a-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d931a-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d931a-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d931a-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d931a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d931a-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration BeginTransactionGrbit
'Usage
Dim instance As BeginTransactionGrbit
```

``` csharp
[FlagsAttribute]
public enum BeginTransactionGrbit
```

## <a name="members"></a><span data-ttu-id="d931a-109">Membres</span><span class="sxs-lookup"><span data-stu-id="d931a-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="d931a-110">Nom du membre</span><span class="sxs-lookup"><span data-stu-id="d931a-110">Member name</span></span></th>
<th><span data-ttu-id="d931a-111">Description</span><span class="sxs-lookup"><span data-stu-id="d931a-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="d931a-112">Aucune</span><span class="sxs-lookup"><span data-stu-id="d931a-112">None</span></span></td>
<td><span data-ttu-id="d931a-113">Options par défaut.</span><span class="sxs-lookup"><span data-stu-id="d931a-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="d931a-114">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d931a-114">ReadOnly</span></span></td>
<td><span data-ttu-id="d931a-115">La transaction ne modifie pas la base de données.</span><span class="sxs-lookup"><span data-stu-id="d931a-115">The transaction will not modify the database.</span></span> <span data-ttu-id="d931a-116">Si une mise à jour est tentée, cette opération échoue avec <a href="hh564840(v=exchg.10).md">transreadonly</a>.</span><span class="sxs-lookup"><span data-stu-id="d931a-116">If an update is attempted, that operation will fail with <a href="hh564840(v=exchg.10).md">TransReadOnly</a>.</span></span> <span data-ttu-id="d931a-117">Cette option est ignorée sauf si elle est demandée lorsque la session donnée n’est pas déjà dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="d931a-117">This option is ignored unless it is requested when the given session is not already in a transaction.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="d931a-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d931a-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d931a-119">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="d931a-119">Reference</span></span>

[<span data-ttu-id="d931a-120">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="d931a-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
