---
description: 'Étape 2 : extension d’une transaction à travers plusieurs composants'
ms.assetid: 20a30e87-e209-45ae-bf1b-722568758c47
title: 'Étape 2 : extension d’une transaction à travers plusieurs composants'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99c6fc80016904a3ea51b7aea7fa0ec93edc47a6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127310925"
---
# <a name="step-2-extending-a-transaction-across-components"></a>Étape 2 : extension d’une transaction à travers les composants

## <a name="objectives"></a>Objectifs

Au cours de cette étape, vous allez découvrir les éléments suivants :

-   Workflow de transaction
-   Vote de plusieurs objets dans une transaction

## <a name="description"></a>Description

[étape 1 : la création d’un composant transactionnel](step-1--creating-a-transactional-component.md) montre comment écrire un composant transactionnel simple qui met à jour les informations sur l’auteur dans la base de données Pubs Microsoft SQL Server. L’étape 2 montre ce qui se passe lorsqu’une transaction est étendue sur plusieurs composants.

En conservant le modèle de programmation COM+, `UpdateAuthorAddress` appelle un autre composant au cours de l’exécution de son travail. Le deuxième composant, `ValidateAuthorAddress` , valide l’adresse de l’auteur et retourne les résultats à son appelant, `UpdateAuthorAddress` .

Contrairement à son appelant, `ValidateAuthorAddress` ne nécessite pas de transaction, mais il peut toujours participer à la transaction de son appelant. Dans cette étape, sa valeur d’attribut de transaction est définie sur **pris en charge**, comme indiqué dans l’illustration suivante, qui étend la transaction existante au nouvel objet.

![Diagramme qui montre l’extension de la transaction existante au nouvel objet.](images/f58acb34-55db-40a4-8c48-f51ad024ff7e.png)

La valeur d’attribut **prise en charge** étend (ou transmet) une transaction existante uniquement lorsque l’appelant est transactionnel. Lorsque `UpdateAuthorAddress` appelle `ValidateAuthorAddress` , com+ examine d’abord le contexte de l’appelant pour voir s’il est transactionnel. COM+ examine ensuite les attributs de service qui sont définis sur `ValidateAuthorAddress` et attribue au nouvel objet le même identificateur de transaction affecté à l’objet appelant. Pour mieux comprendre ce processus, consultez [activation du contexte](context-activation.md).

Étant donné qu’ils partagent le même identificateur de transaction, les deux objets doivent effectuer leur travail avec succès ou COM+ abandonne la transaction (annulation des modifications apportées à la base de données pubs).

Tous les objets participant à une transaction votent pour valider ou abandonner la transaction. Le vote se produit explicitement lorsque vous incluez des instructions de vote dans votre code, comme le montre l’extraction suivante à partir de l’exemple de code Step 1, qui crée le `UpdateAuthorAddress` composant :


```VB
  ' Everything works.
  contextstate.SetMyTransactionVote TxCommit
  contextstate.SetDeactivateOnReturn True
  Exit Sub
  
UnexpectedError:
  ' There's an error.
  contextstate.SetMyTransactionVote TxAbort
  contextstate.SetDeactivateOnReturn True
```



Le vote se produit également implicitement, comme c’est le cas dans le `ValidateAuthorAddress` composant. À moins que l’objet ne déclare autrement, COM+ suppose qu’un objet a terminé son travail, mais qu’il n’est pas prêt à être désactivé. COM+ effectue l’hypothèse suivante :


```VB
  contextstate.SetMyTransactionVote TxCommit
  contextstate.SetDeactivateOnReturn False
```



Lorsque `ValidateAuthorAddress` retourne à son appelant, com+ lit son vote comme une validation. COM+ ne compte pas les votes tant qu’il n’a pas désactivé l’objet racine, qui est le premier objet dans la transaction dans le cas présent, l' `UpdateAuthorAddress` objet.

## <a name="sample-code"></a>Exemple de code

Le `ValidateAuthorAddress` composant effectue une vérification simple de l’adresse de l’auteur. Étant donné que `UpdateAuthorAddress` ne vote pas explicitement, com+ utilise les paramètres de vote par défaut.


```VB
Option Explicit
'
'   Purpose:   This class is used for validating an author's address
'              (presumably right before updating that address in the
'              database).
'
'   Notes:   This component could be in a transaction or not; it doesn't 
'            matter because it doesn't touch any data in a database.
'
Public Function ValidateAuthorAddress( _
                        ByVal strAddress As String, _
                        ByVal strCity As String, _
                        ByVal strState As String, _
                        ByVal strZip As String) As Boolean
  ' Default is to validate unless something is found to be wrong.
  ValidateAuthorAddress = True
                                                  
  '  Invalidate authors who live in New York City
  '  and authors who live in Montana.
  '
  If strCity = "New York" And strState = "New York" Then
    ValidateAuthorAddress = False
  ElseIf strState = "Montana" Then
    ValidateAuthorAddress = False
  End If
  ' Done
End Function
```



## <a name="summary"></a>Résumé

-   La définition de l’attribut de transaction d’un composant sur **pris en charge** peut entraîner la création du nouvel objet dans la transaction de l’objet appelant. COM+ examine le contexte de l’appelant pour déterminer l’état transactionnel du nouvel objet. Si l’appelant est transactionnel, COM+ transmet la transaction au nouvel objet.
-   Tous les objets qui participent à la même transaction partagent un identificateur de transaction commun, que COM+ lit à partir du contexte de l’objet.
-   Chaque objet dans une transaction est vote indépendamment des autres objets. COM+ compte les votes lorsque l’objet racine est désactivé.
-   Vous pouvez basculer le vote de transaction d’un objet entre commit et Abort jusqu’à ce que COM+ désactive l’objet ou jusqu’à ce que COM+ désactive l’objet racine et mette fin à la transaction. Seul le dernier paramètre de vote compte. Les interfaces [**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate) et [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) fournissent des méthodes et produisent des résultats de vote similaires, comme indiqué dans le tableau suivant. Vous pouvez utiliser l’une ou l’autre des interfaces pour voter de manière explicite dans une transaction. 

    | Méthodes de combinaison [**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate)                                                                                                                                                      | Méthode équivalente [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext)       |
    |-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
    | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote*  =  **TxCommit**<br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate*  =  **true**<br/>  | [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete)<br/>     |
    | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote*  =  **TxCommit**<br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate*  =  **false**<br/> | [**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit)<br/>   |
    | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote*  =  **TxAbort**<br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate*  =  **true**<br/>   | [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)<br/>           |
    | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote*  =  **TxAbort**<br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate*  =  **false**<br/>  | [**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit)<br/> |

    

     

-   COM+ définit le vote d’un objet sur l’équivalent de [**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit) , sauf si le composant vote explicitement.
-   Le vote de manière explicite peut réduire la durée globale de la transaction et libérer des verrous de ressource coûteux.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Étape 1 : création d’un composant transactionnel](step-1--creating-a-transactional-component.md)
</dt> <dt>

[Étape 3 : réutilisation des composants](step-3--reusing-components.md)
</dt> <dt>

[Activation du contexte](context-activation.md)
</dt> <dt>

[Gestion des transactions automatiques dans COM+](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 




