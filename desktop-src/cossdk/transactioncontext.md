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
ms.openlocfilehash: 595b5a3192b87420855eb43f1e1e33df37a45c23
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201098"
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

## <a name="remarks"></a>Notes

Pour créer cet objet, appelez [**IObjectContext :: CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance).

Pour utiliser cette classe à partir de Microsoft Visual Basic, ajoutez une référence à la bibliothèque de types des services COM+. Un objet TransactionContext peut être déclaré à l’aide de « COMSVCSLib. TransactionContext » comme nom de classe.

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

 

 




