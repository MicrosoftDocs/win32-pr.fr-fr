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
# <a name="terminating-an-automatic-transaction-by-calling-setcomplete"></a><span data-ttu-id="24c34-103">Fin d’une transaction automatique en appelant SetComplete</span><span class="sxs-lookup"><span data-stu-id="24c34-103">Terminating an Automatic Transaction by Calling SetComplete</span></span>

<span data-ttu-id="24c34-104">Pour utiliser efficacement les transactions automatiques, chaque composant transactionnel doit indiquer qu’il a terminé son travail.</span><span class="sxs-lookup"><span data-stu-id="24c34-104">To use automatic transactions effectively, each transactional component should indicate that it has completed its work.</span></span> <span data-ttu-id="24c34-105">Quand une instance d’objet termine sa tâche avec succès, elle doit affecter la valeur true à ses indicateurs consistent et Done en appelant la méthode [**IObjectContext :: SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) , exposée à l’aide de l’interface [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) et de l’objet [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) .</span><span class="sxs-lookup"><span data-stu-id="24c34-105">When an object instance completes its task successfully, it should set its consistent and done flags to True by calling the [**IObjectContext::SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) method, which is exposed through both the [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) interface and the [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) object.</span></span>

<span data-ttu-id="24c34-106">La méthode la plus efficace pour effectuer une transaction automatique consiste à désactiver explicitement l’objet racine à l’aide de la méthode [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) .</span><span class="sxs-lookup"><span data-stu-id="24c34-106">The most efficient way to complete an automatic transaction is to explicitly deactivate the root object by using the [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) method.</span></span> <span data-ttu-id="24c34-107">En indiquant explicitement qu’un objet racine a terminé son travail, vous pouvez réduire la longueur de la transaction.</span><span class="sxs-lookup"><span data-stu-id="24c34-107">By explicitly indicating that a root object has completed its work, you can reduce the length of the transaction.</span></span>

<span data-ttu-id="24c34-108">L’exemple de Visual Basic suivant montre comment indiquer qu’un objet transactionnel a terminé son travail :</span><span class="sxs-lookup"><span data-stu-id="24c34-108">The following Visual Basic example shows how to indicate that a transactional object has completed its work successfully:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="24c34-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="24c34-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24c34-110">Indicateurs cohérents et terminés</span><span class="sxs-lookup"><span data-stu-id="24c34-110">Consistent and Done Flags</span></span>](consistent-and-done-flags.md)
</dt> <dt>

[<span data-ttu-id="24c34-111">Gestion des transactions automatiques dans COM+</span><span class="sxs-lookup"><span data-stu-id="24c34-111">Managing Automatic Transactions in COM+</span></span>](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 



