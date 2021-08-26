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
ms.openlocfilehash: efe052fc01014d3ebb624dbd4183bc8f0584b145
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481785"
---
# <a name="committransactiongrbit-enumeration"></a>Énumération CommitTransactionGrbit

Options pour JetCommitTransaction.

Cette énumération a un attribut [FlagsAttribute](/dotnet/api/system.flagsattribute) qui permet une combinaison au niveau du bit de ses valeurs membres.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

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

## <a name="members"></a>Membres


|  | Nom du membre | Description | 
|--|-------------|-------------|
|  | None | Options par défaut. | 
|  | LazyFlush | La transaction est validée normalement, mais cette API n’attend pas que la transaction soit vidée dans le fichier journal des transactions avant de retourner à l’appelant. Cela réduit considérablement la durée d’une opération de validation au détriment de la durabilité. Toute transaction qui n’est pas vidée dans le journal avant un incident est automatiquement abandonnée lors de la récupération après incident lors du prochain appel à JetInit. Si WaitLastLevel0Commit ou WaitAllLevel0Commit est spécifié, cette option est ignorée. | 
|  | WaitLastLevel0Commit | Si la session a précédemment validé des transactions et qu’elles n’ont pas encore été vidées dans le fichier journal des transactions, elles doivent être vidées immédiatement. Cette API attend que les transactions aient été vidées avant de retourner à l’appelant. Cela est utile si l’application a précédemment validé plusieurs transactions à l’aide de JET_bitCommitLazyFlush et souhaite maintenant les vider sur le disque.<p>Cette option peut être utilisée même si la session n’est pas actuellement dans une transaction. Cette option ne peut pas être utilisée conjointement avec une autre option.</p> | 



## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Référence

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
