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
ms.openlocfilehash: e40bde6191759e48e59f535f672d221331fc45956e5af7bfe709d90f4573b38a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118484688"
---
# <a name="transactioncommit-method-committransactiongrbit"></a>Transaction. Commit, méthode (CommitTransactionGrbit)

Valider une transaction. Cet objet doit être dans une transaction.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

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

#### <a name="parameters"></a>Paramètres

  - grbit  
    Type : [Microsoft. ISAM. esent. Interop. CommitTransactionGrbit](./committransactiongrbit-enumeration.md)  
    
    Options JetCommitTransaction.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[classe de transaction](./transaction-class.md)

[Membres de transaction](./transaction-members.md)

[Surcharge de validation](./transaction.commit-method.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
