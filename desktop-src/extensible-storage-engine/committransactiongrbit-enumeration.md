---
description: 'En savoir plus sur : énumération CommitTransactionGrbit'
title: Énumération CommitTransactionGrbit
TOCTitle: CommitTransactionGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.CommitTransactionGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.committransactiongrbit(v=EXCHG.10)
ms:contentKeyID: 39510830
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.None
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.WaitLastLevel0Commit
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.LazyFlush
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.WaitLastLevel0Commit
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.LazyFlush
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a93504d688d1eddfcde81ae23c87e62f70e0aab0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536221"
---
# <a name="committransactiongrbit-enumeration"></a><span data-ttu-id="9f87c-103">Énumération CommitTransactionGrbit</span><span class="sxs-lookup"><span data-stu-id="9f87c-103">CommitTransactionGrbit enumeration</span></span>

<span data-ttu-id="9f87c-104">Options pour JetCommitTransaction.</span><span class="sxs-lookup"><span data-stu-id="9f87c-104">Options for JetCommitTransaction.</span></span>

<span data-ttu-id="9f87c-105">Cette énumération a un attribut [FlagsAttribute](/dotnet/api/system.flagsattribute) qui permet une combinaison au niveau du bit de ses valeurs membres.</span><span class="sxs-lookup"><span data-stu-id="9f87c-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="9f87c-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9f87c-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9f87c-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9f87c-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9f87c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9f87c-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CommitTransactionGrbit
'Usage
Dim instance As CommitTransactionGrbit
```

``` csharp
[FlagsAttribute]
public enum CommitTransactionGrbit
```

## <a name="members"></a><span data-ttu-id="9f87c-109">Membres</span><span class="sxs-lookup"><span data-stu-id="9f87c-109">Members</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="9f87c-110">Nom du membre</span><span class="sxs-lookup"><span data-stu-id="9f87c-110">Member name</span></span></th>
<th><span data-ttu-id="9f87c-111">Description</span><span class="sxs-lookup"><span data-stu-id="9f87c-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="9f87c-112">Aucune</span><span class="sxs-lookup"><span data-stu-id="9f87c-112">None</span></span></td>
<td><span data-ttu-id="9f87c-113">Options par défaut.</span><span class="sxs-lookup"><span data-stu-id="9f87c-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="9f87c-114">LazyFlush</span><span class="sxs-lookup"><span data-stu-id="9f87c-114">LazyFlush</span></span></td>
<td><span data-ttu-id="9f87c-115">La transaction est validée normalement, mais cette API n’attend pas que la transaction soit vidée dans le fichier journal des transactions avant de retourner à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="9f87c-115">The transaction is committed normally but this Api does not wait for the transaction to be flushed to the transaction log file before returning to the caller.</span></span> <span data-ttu-id="9f87c-116">Cela réduit considérablement la durée d’une opération de validation au détriment de la durabilité.</span><span class="sxs-lookup"><span data-stu-id="9f87c-116">This drastically reduces the duration of a commit operation at the cost of durability.</span></span> <span data-ttu-id="9f87c-117">Toute transaction qui n’est pas vidée dans le journal avant un incident est automatiquement abandonnée lors de la récupération après incident lors du prochain appel à JetInit.</span><span class="sxs-lookup"><span data-stu-id="9f87c-117">Any transaction that is not flushed to the log before a crash will be automatically aborted during crash recovery during the next call to JetInit.</span></span> <span data-ttu-id="9f87c-118">Si WaitLastLevel0Commit ou WaitAllLevel0Commit est spécifié, cette option est ignorée.</span><span class="sxs-lookup"><span data-stu-id="9f87c-118">If WaitLastLevel0Commit or WaitAllLevel0Commit are specified, this option is ignored.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="9f87c-119">WaitLastLevel0Commit</span><span class="sxs-lookup"><span data-stu-id="9f87c-119">WaitLastLevel0Commit</span></span></td>
<td><span data-ttu-id="9f87c-120">Si la session a précédemment validé des transactions et qu’elles n’ont pas encore été vidées dans le fichier journal des transactions, elles doivent être vidées immédiatement.</span><span class="sxs-lookup"><span data-stu-id="9f87c-120">If the session has previously committed any transactions and they have not yet been flushed to the transaction log file, they should be flushed immediately.</span></span> <span data-ttu-id="9f87c-121">Cette API attend que les transactions aient été vidées avant de retourner à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="9f87c-121">This Api will wait until the transactions have been flushed before returning to the caller.</span></span> <span data-ttu-id="9f87c-122">Cela est utile si l’application a précédemment validé plusieurs transactions à l’aide de JET_bitCommitLazyFlush et souhaite maintenant les vider sur le disque.</span><span class="sxs-lookup"><span data-stu-id="9f87c-122">This is useful if the application has previously committed several transactions using JET_bitCommitLazyFlush and now wants to flush all of them to disk.</span></span>
<p><span data-ttu-id="9f87c-123">Cette option peut être utilisée même si la session n’est pas actuellement dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="9f87c-123">This option may be used even if the session is not currently in a transaction.</span></span> <span data-ttu-id="9f87c-124">Cette option ne peut pas être utilisée conjointement avec une autre option.</span><span class="sxs-lookup"><span data-stu-id="9f87c-124">This option cannot be used in combination with any other option.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="9f87c-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9f87c-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9f87c-126">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="9f87c-126">Reference</span></span>

[<span data-ttu-id="9f87c-127">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="9f87c-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
