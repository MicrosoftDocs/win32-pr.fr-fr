---
description: Fin d’une transaction automatique en appelant SetComplete
ms.assetid: 5bd06cfd-1ee0-48ac-84ab-3737d76bccc0
title: Fin d’une transaction automatique en appelant SetComplete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d1d84d18b45309d750864d514728b8e23a3326e5edeba0bf144105bcbaa4797
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499659"
---
# <a name="terminating-an-automatic-transaction-by-calling-setcomplete"></a>Fin d’une transaction automatique en appelant SetComplete

Pour utiliser efficacement les transactions automatiques, chaque composant transactionnel doit indiquer qu’il a terminé son travail. Quand une instance d’objet termine sa tâche avec succès, elle doit affecter la valeur true à ses indicateurs consistent et Done en appelant la méthode [**IObjectContext :: SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) , exposée à l’aide de l’interface [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) et de l’objet [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) .

La méthode la plus efficace pour effectuer une transaction automatique consiste à désactiver explicitement l’objet racine à l’aide de la méthode [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) . En indiquant explicitement qu’un objet racine a terminé son travail, vous pouvez réduire la longueur de la transaction.

l’exemple de Visual Basic suivant montre comment indiquer qu’un objet transactionnel a terminé son travail :


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

 

 



