---
description: 'Étape 1 : création d’un composant transactionnel'
ms.assetid: 9ab9ac2d-bf1d-419c-8f6b-e2ee80a4bf20
title: 'Étape 1 : création d’un composant transactionnel'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87f5c87fb5c5f615ee04a3233f1a563d5ae5230e4dd18908c78e94092ff0f5c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118305407"
---
# <a name="step-1-creating-a-transactional-component"></a>Étape 1 : création d’un composant transactionnel

## <a name="objectives"></a>Objectifs

Dans cette étape, vous allez apprendre ce qui suit :

-   Comment écrire un composant transactionnel dans Microsoft Visual Basic
-   Les paramètres par défaut des services COM+
-   Comment configurer les services COM+

## <a name="description"></a>Description

Le composant UpdateAuthorAddress, le composant à créer dans cette section, met à jour l’adresse d’un auteur existant dans la base de données pubs. La base de données pubs est un exemple de base de données fourni avec Microsoft SQL Server. Il contient des informations de publication telles que des noms d’auteur, des adresses et des titres de livres.

> [!Note]  
> Pubs est le magasin de données utilisé dans ce premier.

 

Comme UpdateAuthorAddress met à jour un magasin de données, il est recommandé d’inclure le travail dans une transaction, comme indiqué dans l’illustration suivante, de sorte que lorsqu’un client appelle le composant, COM+ démarre automatiquement une transaction et inscrit la base de données (Resource Manager) dans cette transaction. (Pour plus d’informations sur les transactions dans COM+, consultez [transactions com+](com--transactions.md).)

![Diagramme illustrant une transaction COM+ avec UpdateAuthorAddress.](images/d5a47e03-c07e-4db3-b328-111ca9e50bef.png)

Pour faire de UpdateAuthorAddress un composant transactionnel, les étapes suivantes sont requises :

1.  Le composant doit être écrit. Pour une protection supplémentaire, une sous-routine est ajoutée, en vérifiant que COM+ a créé l’objet dans une transaction. En outre, la gestion des erreurs de base est incluse dans le composant pour simplifier la récupération des erreurs. La vérification des transactions et la gestion des erreurs améliorent la fiabilité du composant. (Pour obtenir une liste complète du composant UpdateAuthorAddress, consultez l’exemple de code de l’étape 1.)
2.  Après l’ajout du composant à une application COM+ et l’installation de l’application, l’attribut de transaction doit être défini sur **obligatoire**, ce qui garantit que com+ crée chaque objet UpdateAuthorAddress dans une transaction. Pour obtenir des instructions sur la façon de définir l’attribut de transaction pour un composant, consultez [définition de l’attribut de transaction](setting-the-transaction-attribute.md).
    > [!Note]  
    > La définition de l’attribut de transaction sur un composant définit la manière dont COM+ crée chaque objet en ce qui concerne les transactions. Les valeurs d’attribut de transaction sont **ignorées**, **non prises en** charge, **prises en charge**, **obligatoires** et **nouvelles**. La valeur **requise** n’est pas l’une des valeurs d’attribut par défaut d’un composant.

     

COM+ lie le service de transactions avec l’activation juste-à-temps (JIT) et l’accès concurrentiel. Lorsque vous déclarez un composant comme étant transactionnel, COM+ applique également l’activation JIT et la protection d’accès concurrentiel (synchronisation).

## <a name="sample-code"></a>Exemple de code

Le composant UpdateAuthorAddress ouvre une connexion à la base de données pubs, ce qui permet à l’utilisateur de modifier le nom, l’adresse ou le statut du contrat d’un auteur. Il appelle également un deuxième composant, qui est abordé à l' [étape 2 : extension d’une transaction sur plusieurs composants](step-2--extending-a-transaction-across-multiple-components.md).

pour utiliser le code suivant dans un projet microsoft Visual Basic, ouvrez un nouveau projet ActiveX.dll et ajoutez des références à la bibliothèque microsoft ActiveX Data Objects et à la bibliothèque de types Services COM+.

> [!Note]  
> L’exemple de code de ce premier plan est à des fins d’illustration et peut ne pas être le plus efficace pour la mise en lots et la production réelles.

 


```VB
Option Explicit
'
'  Purpose:   This class is used for updating an author's address.
'
'  Notes:     IMPT:  This component implicitly assumes that it will 
'             always run in a transaction. Undefined results may 
'             otherwise occur.
'

'----------------------------------------------------------
'  VerifyInTxn subroutine
'      Verifies that this component is in a transaction.
'      Throws an error if it is not.
'
Private Sub VerifyInTxn()
  If Not GetObjectContext.IsInTransaction Then
    ' Transactions turned off. 
    Err.Raise 99999, "This component", "I need a transaction!"
  End If
  ' Component is in a transaction.
End Sub

'----------------------------------------------------------
'  UpdateAuthorAddress subroutine
'      Procedure to update an author's address.
'
Public Sub UpdateAuthorAddress( _
                        ByVal strAuthorID As String, _
                        ByVal strPhone As String, _
                       ByVal strAddress As String, _
                        ByVal strCity As String, _
                        ByVal strState As String, _
                        ByVal strZip As String)
  ' Handle any errors.
  On Error GoTo UnexpectedError
  
  ' Verify that component is in a transaction.
  VerifyInTxn
  
  ' Get object context.
  Dim objcontext As COMSVCSLib.ObjectContext
  Set objcontext = GetObjectContext
  
  ' Get the IContextState object.
  Dim contextstate As COMSVCSLib.IContextState
  Set contextstate = objcontext
  
  ' Validate the new address information.
  ' The ValidateAuthorAddress function is described in Step 2.
  Dim oValidateAuthAddr As Object
  Dim bValidAddr As Boolean
  Set oValidateAuthAddr = _
    CreateObject("ComplusPrimer.ValidateAuthorAddress") 
  bValidAddr = oValidateAuthAddr.ValidateAuthorAddress( _
    strAddress, strCity, strState, strZip)
  If Not bValidAddr Then
    Err.Raise 99999, "The UpdateAuthorAddress component", _
      "The address of the author is incorrect!"
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

  ' Execute the query.
  conn.Execute "update authors set phone= '" & strPhone & "'" & _
               " set address= '" & strAddress & "'" & _
               " set city= '" & strCity & "'" & _
               " set state= '" & strState & "'" & _
               " set zip= '" & strZip & "'" & _
               " where au_id = '" & strAuthorID & "'"
               
  ' Close the connection.
  conn.Close
  
  ' Get rid of the connection.
  Set conn = Nothing
                 
  ' Everything works--commit the transaction.
  contextstate.SetMyTransactionVote TxCommit
  contextstate.SetDeactivateOnReturn True
  Exit Sub
  
UnexpectedError:
  ' There's an error.
  contextstate.SetMyTransactionVote TxAbort
  contextstate.SetDeactivateOnReturn True
End Sub

```



## <a name="summary"></a>Récapitulatif

-   COM+ affecte des valeurs d’attribut par défaut. Vous pouvez reconfigurer la plupart des attributs de service.
-   L’affectation de la valeur **obligatoire** à l’attribut de transaction d’un composant garantit que com+ doit créer chaque instance de ce composant dans une transaction, mais ne démarre pas nécessairement une nouvelle transaction.
-   La vérification de la présence d’une transaction confirme que la valeur de l’attribut de transaction du composant n’a pas été réinitialisée par inadvertance à une valeur non transactionnelle, telle que **Ignorer** ou **non prise en charge**.
-   La gestion des erreurs rend votre composant plus fiable et plus facile à dépanner.
-   COM+ applique [l’activation JIT](com--just-in-time-activation.md) et les services de [protection d’accès concurrentiel](com--synchronization.md) pour les composants transactionnels.
-   La fermeture de la connexion de base de données lorsque vous avez terminé, permet à un autre composant de la même transaction de réutiliser la connexion à partir du pool de connexions. (Le regroupement de connexions ne doit pas être confondu avec le [regroupement d’objets](com--object-pooling.md).)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Étape 2 : extension d’une transaction à travers plusieurs composants](step-2--extending-a-transaction-across-multiple-components.md)
</dt> <dt>

[Étape 3 : réutilisation des composants](step-3--reusing-components.md)
</dt> <dt>

[Activation juste-à-temps de COM+](com--just-in-time-activation.md)
</dt> <dt>

[Synchronisation COM+](com--synchronization.md)
</dt> <dt>

[Configuration des transactions](configuring-transactions.md)
</dt> <dt>

[Création d’applications COM+](creating-com--applications.md)
</dt> <dt>

[Définition de l’attribut de transaction](setting-the-transaction-attribute.md)
</dt> </dl>

 

 



