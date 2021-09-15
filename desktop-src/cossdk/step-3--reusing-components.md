---
description: 'Étape 3 : réutilisation des composants'
ms.assetid: d9c14cf8-5bc9-4a6c-9421-c16c3f41b10d
title: 'Étape 3 : réutilisation des composants'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f44446ee20baa6dc8c947ef0650f4478847a1c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127310922"
---
# <a name="step-3-reusing-components"></a>Étape 3 : réutilisation des composants

## <a name="objectives"></a>Objectifs

Au cours de cette étape, vous allez découvrir les éléments suivants :

-   Composants réutilisables.
-   Comment planifier la réutilisation.

## <a name="description"></a>Description

deux parties précédentes de cette version d’origine des services COM+, [étape 1 : création d’un composant transactionnel](step-1--creating-a-transactional-component.md) et [étape 2 : extension d’une Transaction sur plusieurs composants](step-2--extending-a-transaction-across-multiple-components.md) , expliquent comment écrire un composant qui appelle un deuxième composant pour faciliter le travail, en mettant à jour les informations sur l’auteur dans la base de données Pubs Microsoft SQL Server ; tout le travail est protégé par une seule transaction. Les exemples de composants se concentrent sur le travail de mise à jour des données d’un auteur et de vérification de l’adresse de l’auteur, et le traitement des transactions, [l’activation JIT](com--just-in-time-activation.md)et la [protection d’accès concurrentiel](com--synchronization.md)fournies par com+.

Cette étape montre comment réutiliser les composants créés aux étapes 1 et 2 et examine ce que cela signifie pour la conception de ces composants. Comme indiqué dans l’illustration suivante, cela implique la création d’un nouveau composant, `AddNewAuthor` , qui ajoute de nouveaux auteurs à la base de données en appelant `UpdateAuthorAddress` .

![Diagramme qui montre le Flow lors de la réutilisation des composants.](images/e746f50e-2e86-4e59-82f9-f407d2b0325c.png)

En plus de réutiliser la fonctionnalité de composant existante, `AddNewAuthor` appelle un autre nouveau composant appelé `ValidateAuthorName` . Comme le montre l’illustration précédente, `ValidateAuthorName` est non transactionnel. La valeur de l’attribut de transaction de ce composant est laissée à son paramètre par défaut (**non pris en charge**) pour exclure son travail de la transaction. Comme indiqué dans l’exemple de code Step 3, `ValidateAuthorName` exécute des requêtes en lecture seule sur la base de données, et l’échec de cette tâche mineure ne doit pas avoir la possibilité d’abandonner la transaction. Toutefois, la valeur de l’attribut transaction du `AddNewAuthor` composant est définie sur **obligatoire**.

Les `AddNewAuthor` `UpdateAuthorAddress` composants, et `ValidateAuthorAddress` votent tous dans la transaction. Dans cette transaction, `AddNewAuthor` est l’objet racine. COM+ rend toujours le premier objet créé dans la transaction l’objet racine.

Dans cet exemple, il est facile de réutiliser le `UpdateAuthorAddress` composant : com + fournit automatiquement les services attendus. Toutefois, les résultats seraient différents si la valeur d’attribut de transaction du `UpdateAuthorAddress` composant a été initialement définie sur **nécessite New** au lieu de **Required**. Sur la surface, les deux paramètres sont similaires. tous deux garantissent une transaction. L’argument **Requires New**, cependant, démarre toujours une nouvelle transaction, tandis que **Required** démarre une nouvelle transaction uniquement lorsque l’appelant de l’objet est non transactionnel. À partir de là, il est important de configurer `UpdateAuthorAddress` attentivement et avec prudence. Dans le cas contraire, COM+ peut avoir interprété différemment la demande de service, générant deux transactions non liées, comme indiqué dans l’illustration suivante, au lieu d’une.

![Diagramme qui montre le Flow lors de la réutilisation des composants avec « nécessite New ».](images/24b9edf6-af00-4994-8fa1-cee4ace16379.png)

> [!Note]  
> Lorsque vous réutilisez des composants, assurez-vous que les services sont configurés pour prendre en charge le résultat souhaité.

 

## <a name="sample-code"></a>Exemple de code

Le composant AddNewAuthor effectue des ajouts de nouveaux auteurs par lots en permettant à l’objet de rester actif jusqu’à ce que le client libère sa référence à l’objet.


```VB
Option Explicit
'
'   Purpose:   This class is used for adding a new author.
'
'   Notes:    IMPT:  This component implicitly assumes that it will
'             always run in a transaction. Undefined results may 
'             otherwise occur.
'
'  AddNewAuthor
'
Public Sub AddNewAuthor( _
                        ByVal strAuthorFirstName As String, _
                        ByVal strAuthorLastName As String, _
                        ByVal strPhone As String, _
                        ByVal strAddress As String, _
                        ByVal strCity As String, _
                        ByVal strState As String, _
                        ByVal strZip As String, _
                        ByVal boolContracted As Boolean)
  ' Handle any errors.
  On Error GoTo UnexpectedError

  ' Verify component is in a transaction.
  ' The VerifyInTxn subroutine is described in Step 1.
  VerifyInTxn

  ' Get our object context.
  Dim objcontext As COMSVCSLib.ObjectContext
  Set objcontext = GetObjectContext

  ' Get the IContextState object.
  Dim contextstate As COMSVCSLib.IContextState
  Set contextstate = objcontext

  ' Validate that the author is OK.
  ' The ValidateAuthorName function is described after this function.
  Dim oValidateAuthName As Object
  Dim bValidAuthor As Boolean
  Set oValidateAuthName = CreateObject("ComplusPrimer.ValidateAuthorName")
  bValidAuthor = oValidateAuthName.ValidateAuthorName( _
    strAuthorFirstName, strAuthorLastName)
  If Not bValidAuthor Then
    Err.Raise 999999, "The AddNewAuthor component", _
      "You tried to add an author on the banned list!"
  End If
  
  ' Open the connection to the database.
  Dim conn As ADODB.Connection
  Set conn = CreateObject("ADODB.Connection")

  ' Specify the OLE DB provider.
  conn.Provider = "SQLOLEDB"

  ' Connect using Windows Authentication.
  Dim strProv As String
  strProv = "Server=MyDBServer;Database=pubs;Trusted_Connection=yes"

  ' Open the database.
  conn.Open strProv

  ' Tell the database to actually add the author; use empty strings 
  ' for this part and rely on the UpdateAuthorAddress 
  ' component to validate the address/phone/etc data.
  ' Default Contract flag is off.
  Dim strUpdateString As String
  strUpdateString = "insert into authors values(_
                     '789-65-1234'," & _
                     strAuthorLastName & ", " & _
                     strAuthorFirstName & ", " & _
                     "'(555) 555-5555', ', ', ', '98765', "

  If boolContracted Then
    strUpdateString = strUpdateString + "1)"
  Else
    strUpdateString = strUpdateString + "0)"
  End If

  conn.Execute strUpdateString
  
  ' Close the connection; this potentially allows 
  ' another component in the same transaction to
  ' reuse the connection from the connection pool.
  conn.Close
  Set conn = Nothing
  
  ' Create the UpdateAuthorAddress component.
  Dim oUpdateAuthAddr As Object
  Set oUpdateAuthAddr = CreateObject("ComplusPrimer.UpdateAuthorAddress")
  
  ' The component throws an error if anything goes wrong.
  oUpdateAuthAddr.UpdateAuthorAddress "", strPhone, _
    strAddress, strCity, strState, strZip
    
  Set oUpdateAuthAddr = Nothing
  
  ' Everything works--commit the transaction.
  contextstate.SetMyTransactionVote TxCommit
  
  '  Design issue:  Allow batch additions of new
  '  authors in one transaction, or should each new author be added
  '  in a single new transaction?
  contextstate.SetDeactivateOnReturn False
  Exit Sub
  
UnexpectedError:
  ' There's an error.
  contextstate.SetMyTransactionVote TxAbort
  contextstate.SetDeactivateOnReturn True
  
End Sub
```



Le `ValidateAuthorName` composant valide les noms des auteurs avant `AddNewAuthor` d’ajouter le nom à la base de données. Ce composant renvoie une erreur à son appelant si un événement inattendu se produit.


```VB
Option Explicit
'
'   Purpose:   This class is used for validating authors before
'              adding them to the database.
'
'   Notes:   This component doesn't need to be in a transaction because
'            it is performing read-only queries on the database,
'            especially since these queries are not overlapping with
'            any updates of end-user data. If an unexpected error
'            happens, let the error go back to the caller who
'            needs to handle it.
'

Public Function ValidateAuthorName( _
                        ByVal strAuthorFirstName As String, _
                        ByVal strAuthorLastName As String _
                        ) As Boolean
  ValidateAuthorName = False

  ' Open the connection to the database.
  Dim conn As ADODB.Connection
  Set conn = CreateObject("ADODB.Connection")

  ' Specify the OLE DB provider.
  conn.Provider = "SQLOLEDB"

  ' Connect using Windows Authentication.
  Dim strProv As String
  strProv = "Server=MyDBServer;Database=pubs;Trusted_Connection=yes"

  ' Open the database.
  conn.Open strProv

  ' Suppose another hypothetical table has been added to the Pubs 
  ' database, one that contains a list of banned authors.
  Dim rs As ADODB.Recordset
  Set rs = conn.Execute("select * from banned_authors")
  
  ' Loop through the banned-author list looking for the specified
  ' author.
  While Not rs.EOF
    If rs.Fields("FirstName") = strAuthorFirstName And _
      rs.Fields("LastName") = strAuthorLastName Then
        ' This is a banned author.
        conn.Close
        Set conn = Nothing
        Set rs = Nothing
        Exit Function
    End If
    rs.MoveNext
  Wend
  
  ' None of the added authors found in the banned list.
  ValidateAuthorName = True
  conn.Close
  Set conn = Nothing
  Set rs = Nothing
End Function
```



## <a name="summary"></a>Résumé

-   Il peut arriver que vous ne souhaitiez pas qu’un composant vote dans la transaction.
-   COM+ n’applique pas l’activation JIT ou la protection d’accès concurrentiel sur les composants non transactionnels. Vous pouvez configurer ces services séparément.
-   La configuration d’un composant appelant affecte la manière dont COM+ interprète les demandes de service du composant appelé.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Étape 1 : création d’un composant transactionnel](step-1--creating-a-transactional-component.md)
</dt> <dt>

[Étape 2 : extension d’une transaction à travers plusieurs composants](step-2--extending-a-transaction-across-multiple-components.md)
</dt> <dt>

[Configuration des transactions](configuring-transactions.md)
</dt> <dt>

[Conception pour l’évolutivité](designing-for-scalability.md)
</dt> </dl>

 

 



