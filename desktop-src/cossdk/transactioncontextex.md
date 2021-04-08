---
description: Crée un objet transactionnel générique qui commence une transaction. En appelant les méthodes de cette classe, vous pouvez composer le travail de plusieurs objets COM dans une transaction unique et valider ou abandonner explicitement la transaction.
ms.assetid: 5f3f83e0-33fc-4c43-9327-59485c0d8bd3
title: TransactionContextEx, classe (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TransactionContextEx
api_type:
- COM
ms.openlocfilehash: 8cf5c3aaa7ffe126124a909498a7c54cfb012c65
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748837"
---
# <a name="transactioncontextex-class"></a>TransactionContextEx, classe

Crée un objet transactionnel générique qui commence une transaction. En appelant les méthodes de cette classe, vous pouvez composer le travail de plusieurs objets COM dans une transaction unique et valider ou abandonner explicitement la transaction.

## <a name="when-to-implement"></a>Quand implémenter

Cette classe est implémentée par COM+.



| Condition requise | Valeur |
|------------|--------------------------------------------------------|
| CLSID      | CLSID \_ TransactionContextEx                            |
| ProgID     | L "TxCTx. TransactionContextEx"                          |
| Interfaces | [**ITransactionContextEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontextex) |



 

## <a name="when-to-use"></a>Quand l’utiliser

Un client non transactionnel utilise cette classe pour commencer une transaction. À l’aide des méthodes de cette classe, le client peut appeler des objets COM supplémentaires qui, s’ils sont configurés pour participer à une transaction, s’exécutent dans la limite de transaction de l’objet de contexte de transaction. En fonction de sa logique métier, le client peut explicitement valider ou abandonner la transaction.

La classe **TransactionContextEx** limite la réutilisation de la logique métier qui dirige la transaction. Pour cette raison, il est recommandé d’utiliser des objets instanciés à partir de la classe **TransactionContextEx** avec modération.

## <a name="remarks"></a>Notes

Pour créer cet objet, appelez [**IObjectContext :: CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance).

La classe **TransactionContextEx** n’a pas été conçue pour être utilisée dans Visual Basic. Utilisez la classe [**transactionContext**](transactioncontext.md) à la place.

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

[**ITransactionContextEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontextex)
</dt> <dt>

[**TransactionContext**](transactioncontext.md)
</dt> </dl>

 

 




