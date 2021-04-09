---
description: 'En savoir plus sur : champ Server2003Grbits. WaitAllLevel0Commit'
title: Champ Server2003Grbits. WaitAllLevel0Commit (Microsoft. ISAM. esent. Interop. Server2003)
TOCTitle: WaitAllLevel0Commit field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.WaitAllLevel0Commit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003grbits.waitalllevel0commit(v=EXCHG.10)
ms:contentKeyID: 55104104
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.WaitAllLevel0Commit
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.WaitAllLevel0Commit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 16390069adf81ead8e819bc5148a88e30900b508
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865610"
---
# <a name="server2003grbitswaitalllevel0commit-field"></a><span data-ttu-id="3d6c5-103">Champ Server2003Grbits. WaitAllLevel0Commit</span><span class="sxs-lookup"><span data-stu-id="3d6c5-103">Server2003Grbits.WaitAllLevel0Commit field</span></span>

<span data-ttu-id="3d6c5-104">Toutes les transactions précédemment validées par une session qui n’ont pas encore été vidées dans le fichier journal des transactions seront vidées immédiatement.</span><span class="sxs-lookup"><span data-stu-id="3d6c5-104">All transactions previously committed by any session that have not yet been flushed to the transaction log file will be flushed immediately.</span></span> <span data-ttu-id="3d6c5-105">Cette API attend que les transactions aient été vidées avant de retourner à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="3d6c5-105">This API will wait until the transactions have been flushed before returning to the caller.</span></span> <span data-ttu-id="3d6c5-106">Cette option peut être utilisée même si la session n’est pas actuellement dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="3d6c5-106">This option may be used even if the session is not currently in a transaction.</span></span> <span data-ttu-id="3d6c5-107">Cette option ne peut pas être utilisée conjointement avec une autre option.</span><span class="sxs-lookup"><span data-stu-id="3d6c5-107">This option cannot be used in combination with any other option.</span></span>

<span data-ttu-id="3d6c5-108">**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3d6c5-108">**Namespace:**  [Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span></span>  
<span data-ttu-id="3d6c5-109">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3d6c5-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3d6c5-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3d6c5-110">Syntax</span></span>

``` vb
'Declaration
Public Const WaitAllLevel0Commit As CommitTransactionGrbit
'Usage
Dim value As CommitTransactionGrbit

value = Server2003Grbits.WaitAllLevel0Commit
```

``` csharp
public const CommitTransactionGrbit WaitAllLevel0Commit
```

## <a name="see-also"></a><span data-ttu-id="3d6c5-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3d6c5-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3d6c5-112">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="3d6c5-112">Reference</span></span>

[<span data-ttu-id="3d6c5-113">Server2003Grbits, classe</span><span class="sxs-lookup"><span data-stu-id="3d6c5-113">Server2003Grbits class</span></span>](./server2003grbits-class.md)

[<span data-ttu-id="3d6c5-114">Membres Server2003Grbits</span><span class="sxs-lookup"><span data-stu-id="3d6c5-114">Server2003Grbits members</span></span>](./server2003grbits-members.md)

[<span data-ttu-id="3d6c5-115">Espace de noms Microsoft. ISAM. esent. Interop. Server2003</span><span class="sxs-lookup"><span data-stu-id="3d6c5-115">Microsoft.Isam.Esent.Interop.Server2003 namespace</span></span>](./microsoft.isam.esent.interop.server2003-namespace.md)
