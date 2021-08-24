---
description: Crée un objet transactionnel générique qui commence une transaction.
ms.assetid: efaf1468-4973-472f-af91-85957a52b7df
title: TransactionContext, classe (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TransactionContext
api_type:
- COM
ms.openlocfilehash: aa0a90cee2b0af7d5ebe3679dca46aa04c6326fb5fd62fe5f57699d610b9efe8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678149"
---
# <a name="transactioncontext-class"></a>TransactionContext, classe

Crée un objet transactionnel générique qui commence une transaction. En appelant les méthodes de cette classe, vous pouvez composer le travail de plusieurs objets COM dans une transaction unique et valider ou abandonner explicitement la transaction.

## <a name="when-to-implement"></a>Quand implémenter

Cette classe est implémentée par COM+.



| Condition requise | Valeur |
|------------|----------------------------------------------------|
| CLSID      | CLSID \_ transactionContext                          |
| ProgID     | L "TxCTx. TransactionContext"                        |
| Interfaces | [**ITransactionContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontext) |



 

## <a name="when-to-use"></a>Quand l’utiliser

Un client non transactionnel utilise cette classe pour commencer une transaction. À l’aide des méthodes de cette classe, le client peut appeler des objets COM supplémentaires qui, s’ils sont configurés pour participer à une transaction, s’exécutent dans la limite de transaction de l’objet de contexte de transaction. En fonction de sa logique métier, le client peut explicitement valider ou abandonner la transaction.

La classe **transactionContext** limite la réutilisation de la logique métier qui dirige la transaction. Pour cette raison, il est recommandé d’utiliser des objets instanciés à partir de la classe **transactionContext** avec modération.

## <a name="remarks"></a>Remarques

Pour créer cet objet, appelez [**IObjectContext :: CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance).

pour utiliser cette classe à partir de Microsoft Visual Basic, ajoutez une référence à la bibliothèque de types des Services COM+. Un objet TransactionContext peut être déclaré à l’aide de « COMSVCSLib. TransactionContext » comme nom de classe.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>ComSvcs. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Configuration des transactions](configuring-transactions.md)
</dt> <dt>

[**ITransactionContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontext)
</dt> <dt>

[**TransactionContextEx**](transactioncontextex.md)
</dt> </dl>

 

 




