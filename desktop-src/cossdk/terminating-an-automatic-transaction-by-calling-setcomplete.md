---
description: Fin d’une transaction automatique en appelant SetComplete
ms.assetid: 5bd06cfd-1ee0-48ac-84ab-3737d76bccc0
title: Fin d’une transaction automatique en appelant SetComplete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba4bf09e631acf69a9b663d68d7eb82cfaa4490f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544574"
---
# <a name="terminating-an-automatic-transaction-by-calling-setcomplete"></a>Fin d’une transaction automatique en appelant SetComplete

Pour utiliser efficacement les transactions automatiques, chaque composant transactionnel doit indiquer qu’il a terminé son travail. Quand une instance d’objet termine sa tâche avec succès, elle doit affecter la valeur true à ses indicateurs consistent et Done en appelant la méthode [**IObjectContext :: SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) , exposée à l’aide de l’interface [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) et de l’objet [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) .

La méthode la plus efficace pour effectuer une transaction automatique consiste à désactiver explicitement l’objet racine à l’aide de la méthode [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) . En indiquant explicitement qu’un objet racine a terminé son travail, vous pouvez réduire la longueur de la transaction.

L’exemple de Visual Basic suivant montre comment indiquer qu’un objet transactionnel a terminé son travail :


```VB
Sub MyObjMethod1()
  Dim ObjCtx As ObjectContext
  Dim InteriorObj1 As Cinterior  ' Cinterior is a user-defined object.

  Set ObjCtx = GetObjectContext()
  Set InteriorObj1 = CreateObject ("MyDll.Cinterior")
  InteriorObj1.Method1
  ' If the call completed successfully, then...
  objCtx.SetComplete
End Sub
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Indicateurs cohérents et terminés](consistent-and-done-flags.md)
</dt> <dt>

[Gestion des transactions automatiques dans COM+](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 



