---
description: Accélération des transactions en avertissant l’objet racine
ms.assetid: 5737324a-65e5-4a39-b325-762768e171a1
title: Accélération des transactions en avertissant l’objet racine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f3865382434ee070db753a0f9113577531558d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127310930"
---
# <a name="speeding-transactions-by-notifying-the-root-object"></a>Accélération des transactions en avertissant l’objet racine

Pour utiliser efficacement les transactions automatiques, chaque composant transactionnel doit indiquer qu’il a terminé son travail. Quand une instance d’objet termine sa tâche avec succès, elle doit définir ses indicateurs consistent et Done sur true en appelant la méthode [**IObjectContext :: SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) . Lorsque tous les objets intérieurs de la transaction ont appelé **SetComplete**, la transaction peut être arrêtée en désactivant explicitement l’objet racine en appelant sa méthode **SetComplete** . En indiquant explicitement qu’un objet racine a terminé son travail, vous pouvez réduire la longueur de la transaction.

En cas d’échec d’une méthode d’objet transactionnel, l’objet doit affecter à son indicateur consistent la valeur false et son indicateur Done à la valeur true en appelant la méthode [**IObjectContext :: SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) . En appelant la méthode **SetAbort** , un objet retourne le contrôle à son appelant et s’assure que la transaction est finalement abandonnée.

Toutefois, à moins que l’objet qui appelle [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) soit la racine de la transaction, la transaction continue de s’exécuter même si rien ne peut l’enregistrer à partir de la fin de l’abandon. Pour accélérer l’arrêt d’une transaction qui a échoué, vous pouvez générer une erreur pour alerter l’objet racine afin d’appeler également **SetAbort**. Pour terminer, l’objet racine doit ensuite envoyer un message d’erreur à son client.

Bien qu’il existe de nombreuses approches que vous pouvez prendre pour gérer les erreurs, votre approche doit clairement coordonner les communications entre les objets intérieurs et l’objet racine.

les fragments de code Visual Basic suivants montrent une approche de la gestion des erreurs. Dans le premier fragment, un objet intérieur appelle [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort), génère une erreur et génère un message d’erreur, comme suit :

``` syntax
Dim ObjCtx As ObjectContext
Dim ErrorCode As Long, Description As String

Set ObjCtx = GetObjectContext()
ObjCtx.SetAbort
ErrorCode = vbObjectError + 5
Description = "Some meaningful message"
Err.Raise ErrorCode, , Description
```

Dans le deuxième fragment, l’objet racine gère l’erreur et transmet le message à son client, comme suit :

``` syntax
Sub MyObjMethod1()
  On Error GoTo MyObjMethod1_err
  Dim ObjCtx As ObjectContext
  Dim InteriorObj1 As Cinterior  ' Cinterior is a user-defined object.

  Set ObjCtx = GetObjectContext()
  Set InteriorObj1 = CreateObject ("MyDll.Cinterior")
  InteriorObj1.Method1
  ' If the call completed successfully, then...
  ObjCtx.SetComplete
Exit Sub
  MyObjMethod1_err:
  ' Doom the transaction and exit.
  ObjCtx.SetAbort
  ' Pass the message back to client.
  Err.Raise Err.Number, , Err.Description
End Sub
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestion des transactions automatiques dans COM+](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 



