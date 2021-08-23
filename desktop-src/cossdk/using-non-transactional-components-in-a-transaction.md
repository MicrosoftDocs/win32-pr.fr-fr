---
description: Utilisation de composants non transactionnels dans une transaction
ms.assetid: b83b4bab-1851-48dc-b35a-6467a6dff741
title: Utilisation de composants non transactionnels dans une transaction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 365cf6f8e5c20f328f4308366e9a98916d9277363bba815fdbc00b5e2d8203d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991349"
---
# <a name="using-non-transactional-components-in-a-transaction"></a>Utilisation de composants non transactionnels dans une transaction

Il est souvent utile de placer des composants non transactionnels dans une transaction pour tirer parti des [propriétés ACID](acid-properties.md) des transactions. Par exemple, si vous avez des composants hérités non transactionnels que vous utilisez pour mettre à jour des mots de passe sur un réseau, vous pouvez placer ces composants dans une transaction pour vous assurer que les mises à jour de mot de passe sont cohérentes sur le réseau.

L' *objet de contexte de transaction* est un objet générique qui permet aux clients non transactionnels de combiner le travail de plusieurs objets com en une seule transaction, sans que vous ayez besoin de développer un nouveau composant spécifiquement à cet effet. Contrairement à une transaction automatique, l’objet de contexte de transaction requiert que son client valide ou abandonne explicitement la transaction.

Par défaut, la valeur d’attribut de transaction de l’objet de contexte de transaction est définie sur obligatoire. COM+ abandonne la transaction si le client libère l’objet de contexte de transaction sans émettre explicitement un appel de validation ou d’abandon.

l’exemple de Visual Basic suivant montre comment un client non transactionnel peut composer le travail effectué par plusieurs objets en une seule transaction :


```VB
Dim objTxCtx As TransactionContext
Dim objCat As MyDLL.Ccat  ' Ccat is a user-defined component.
Dim objDog As MyDLL.Cdog  ' Cdog is a user-defined component.

' Get TransactionContext object.
Set objTxCtx = _
  CreateObject ("TxCtx.TransactionContext")

' Create instances of Cat and Dog.
Set objCat = _ 
  objTxCtx.CreateInstance ("MyDLL.Ccat")
Set objDog = _ 
  objTxCtx.CreateInstance ("MyDLL.Cdog")

' Both objects do work.
objDog.Bark
objCat.Hiss

' Commit the transaction.
objTxCtx.Commit

```



## <a name="limitations-of-the-transaction-context-object"></a>Limitations de l’objet de contexte de transaction

Voici quelques limitations importantes de l’objet de contexte de transaction :

-   Lors de l’utilisation d’un objet de contexte de transaction, la logique d’application qui associe le travail de plusieurs objets dans une transaction unique est liée à une implémentation de client non transactionnelle spécifique et certains avantages de l’utilisation des composants COM sont perdus. Ces avantages sont les suivants :
    -   Possibilité de réutiliser la logique d’application dans le cadre d’une transaction encore plus volumineuse
    -   Disposition de la sécurité déclarative
    -   Flexibilité pour exécuter la logique à distance à partir du client
-   L’objet de contexte de transaction s’exécute in-process avec le client non transactionnel, ce qui signifie que COM+ doit être disponible sur l’ordinateur client non transactionnel. Cela peut ne pas être un problème, par exemple lorsque l’objet de contexte de transaction est utilisé à partir d’une page ASP (Active Server Pages) qui s’exécute sur le même serveur que COM+.
-   Vous n’avez pas de contexte pour le client non transactionnel lorsque vous créez un objet de contexte de transaction. Le travail transactionnel ne peut être effectué indirectement que par le biais d’objets COM créés à l’aide de l’objet de contexte de transaction. En particulier, le client non transactionnel ne peut pas utiliser les distributeurs de ressources COM+ (tels que ODBC) et faire en sorte que le travail soit inclus dans la transaction. Par exemple, les développeurs peuvent être familiarisés avec la syntaxe suivante pour le travail transactionnel sur des systèmes de base de données relationnelle :

    ``` syntax
    BEGIN TRANSACTION
      DoWork
    COMMIT TRANSACTION
    ```

    L’utilisation de l’objet de contexte de transaction de façon similaire ne produit pas le résultat souhaité :

    ``` syntax
    Set objTxCtx = CreateObject ("TxCtx.TransactionContext")
      DoWork
      objTxCtx.Commit
    Set objTxCtx = Nothing
    ```

    L’appel à la solution dans cet exemple n’est pas inscrit dans une transaction. Au lieu de cela, vous devez créer un composant COM qui appelle le rôle de travail, créer une instance d’objet de ce composant à l’aide de l’objet de contexte de transaction, puis appeler cet objet à partir du client non transactionnel pour que le travail fasse partie de la transaction contrôlée par le client.

 

 



