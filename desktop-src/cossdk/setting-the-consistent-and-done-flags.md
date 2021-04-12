---
description: Définition des indicateurs cohérents et terminés
ms.assetid: d9b6096d-f93c-4f8e-a4d9-ea8309b35f0f
title: Définition des indicateurs cohérents et terminés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd45d457828a222ce7f4ccbdc0080001b0f0b55f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483024"
---
# <a name="setting-the-consistent-and-done-flags"></a>Définition des indicateurs cohérents et terminés

Vous définissez les indicateurs consistent et Done en appelant des méthodes sur les interfaces [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) ou [**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate) . Les stratégies utilisées par ces deux interfaces diffèrent considérablement. **IObjectContext** possède quatre méthodes qui lient les indicateurs consistent et Done dans des combinaisons uniques, tandis que **IContextState** a deux méthodes qui vous permettent de définir chaque indicateur de manière indépendante. Les méthodes de **IObjectContext** sont également exposées par le biais de l’objet [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) .

Pour un contrôle indépendant de chaque indicateur, [**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate) fournit une méthode pour définir l’indicateur consistent sur true ou false et une méthode pour définir l’indicateur Done sur true ou false. Ces méthodes sont [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) et [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn), respectivement. L’interface **IContextState** comprend également des méthodes permettant de récupérer la valeur actuelle de chaque indicateur.

Lorsque vous définissez la valeur de la méthode [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) sur TXCOMMIT, com+ vérifie la présence d’une transaction. Si COM+ ne détecte pas de transaction, il génère une erreur que vous pouvez capturer dans un fichier journal. Par exemple, supposons que quelqu’un configure par inadvertance l’attribut de transaction de votre composant pour qu’il ne soit pas pris en charge, mais que vous pensiez qu’il doit être défini sur obligatoire. En définissant **SetMyTransactionVote** = TxCommit, vous pouvez identifier le conflit et prendre une mesure.

Le tableau suivant décrit les appels de méthode qui peuvent être utilisés pour définir les indicateurs cohérents et terminés.



| Indicateur de cohérence  | Indicateur Done        | Méthode IObjectContext                                            | Méthodes IContextState                                                                                                                                                                                    |
|------------------|------------------|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vrai<br/>  | Faux<br/> | [**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit)<br/>   | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = TxCommit <br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = false<br/> |
| Faux<br/> | False<br/> | [**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit)<br/> | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = TxAbort <br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = false<br/>  |
| False<br/> | True<br/>  | [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)<br/>           | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = TxAbort <br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = true<br/>   |
| True<br/>  | True<br/>  | [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete)<br/>     | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = TxCommit <br/>[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = true              |



 

> [!Note]  
> La propriété Done automatique, définie au niveau de la méthode, peut affecter la définition des indicateurs cohérents et terminés. Pour plus d’informations sur la propriété effectuée automatiquement, consultez [activation de la saisie semi-automatique pour une méthode](enabling-auto-done-for-a-method.md) et [définition du bit terminé](setting-the-done-bit.md).

 

 

 




