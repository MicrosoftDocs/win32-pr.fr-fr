---
description: 'En savoir plus sur : transaction. Commit, méthode (CommitTransactionGrbit)'
title: Transaction. Commit, méthode (CommitTransactionGrbit)
TOCTitle: Commit method (CommitTransactionGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Transaction.Commit(Microsoft.Isam.Esent.Interop.CommitTransactionGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.transaction.commit(v=EXCHG.10)
ms:contentKeyID: 55104071
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Transaction.Commit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 048071a08d1211d6091fb6c2c23f9cfe302f8872
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204064"
---
# <a name="transactioncommit-method-committransactiongrbit"></a><span data-ttu-id="8b38d-103">Transaction. Commit, méthode (CommitTransactionGrbit)</span><span class="sxs-lookup"><span data-stu-id="8b38d-103">Transaction.Commit method (CommitTransactionGrbit)</span></span>

<span data-ttu-id="8b38d-104">Valider une transaction.</span><span class="sxs-lookup"><span data-stu-id="8b38d-104">Commit a transaction.</span></span> <span data-ttu-id="8b38d-105">Cet objet doit être dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="8b38d-105">This object should be in a transaction.</span></span>

<span data-ttu-id="8b38d-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8b38d-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8b38d-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8b38d-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8b38d-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8b38d-108">Syntax</span></span>

``` vb
'Declaration
Public Sub Commit ( _
    grbit As CommitTransactionGrbit _
)
'Usage
Dim instance As Transaction
Dim grbit As CommitTransactionGrbit

instance.Commit(grbit)
```

``` csharp
public void Commit(
    CommitTransactionGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="8b38d-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8b38d-109">Parameters</span></span>

  - <span data-ttu-id="8b38d-110">grbit</span><span class="sxs-lookup"><span data-stu-id="8b38d-110">grbit</span></span>  
    <span data-ttu-id="8b38d-111">Type : [Microsoft. ISAM. esent. Interop. CommitTransactionGrbit](./committransactiongrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="8b38d-111">Type: [Microsoft.Isam.Esent.Interop.CommitTransactionGrbit](./committransactiongrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="8b38d-112">Options JetCommitTransaction.</span><span class="sxs-lookup"><span data-stu-id="8b38d-112">JetCommitTransaction options.</span></span>

## <a name="see-also"></a><span data-ttu-id="8b38d-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b38d-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8b38d-114">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="8b38d-114">Reference</span></span>

[<span data-ttu-id="8b38d-115">classe de transaction</span><span class="sxs-lookup"><span data-stu-id="8b38d-115">Transaction class</span></span>](./transaction-class.md)

[<span data-ttu-id="8b38d-116">Membres de transaction</span><span class="sxs-lookup"><span data-stu-id="8b38d-116">Transaction members</span></span>](./transaction-members.md)

[<span data-ttu-id="8b38d-117">Surcharge de validation</span><span class="sxs-lookup"><span data-stu-id="8b38d-117">Commit overload</span></span>](./transaction.commit-method.md)

[<span data-ttu-id="8b38d-118">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="8b38d-118">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
