---
description: Accélération des transactions en avertissant l’objet racine
ms.assetid: 5737324a-65e5-4a39-b325-762768e171a1
title: Accélération des transactions en avertissant l’objet racine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f3865382434ee070db753a0f9113577531558d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104200955"
---
# <a name="speeding-transactions-by-notifying-the-root-object"></a><span data-ttu-id="02340-103">Accélération des transactions en avertissant l’objet racine</span><span class="sxs-lookup"><span data-stu-id="02340-103">Speeding Transactions by Notifying the Root Object</span></span>

<span data-ttu-id="02340-104">Pour utiliser efficacement les transactions automatiques, chaque composant transactionnel doit indiquer qu’il a terminé son travail.</span><span class="sxs-lookup"><span data-stu-id="02340-104">To use automatic transactions effectively, each transactional component should indicate that it has completed its work.</span></span> <span data-ttu-id="02340-105">Quand une instance d’objet termine sa tâche avec succès, elle doit définir ses indicateurs consistent et Done sur true en appelant la méthode [**IObjectContext :: SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) .</span><span class="sxs-lookup"><span data-stu-id="02340-105">When an object instance completes its task successfully, it should set its consistent and done flags to True by calling the [**IObjectContext::SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) method.</span></span> <span data-ttu-id="02340-106">Lorsque tous les objets intérieurs de la transaction ont appelé **SetComplete**, la transaction peut être arrêtée en désactivant explicitement l’objet racine en appelant sa méthode **SetComplete** .</span><span class="sxs-lookup"><span data-stu-id="02340-106">When all of the interior objects of the transaction have called **SetComplete**, the transaction can be terminated by explicitly deactivating the root object by calling its **SetComplete** method.</span></span> <span data-ttu-id="02340-107">En indiquant explicitement qu’un objet racine a terminé son travail, vous pouvez réduire la longueur de la transaction.</span><span class="sxs-lookup"><span data-stu-id="02340-107">By explicitly indicating that a root object has completed its work, you can reduce the length of the transaction.</span></span>

<span data-ttu-id="02340-108">En cas d’échec d’une méthode d’objet transactionnel, l’objet doit affecter à son indicateur consistent la valeur false et son indicateur Done à la valeur true en appelant la méthode [**IObjectContext :: SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) .</span><span class="sxs-lookup"><span data-stu-id="02340-108">When a transactional object method fails, the object should set its consistent flag to False and its done flag to True by calling the [**IObjectContext::SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) method.</span></span> <span data-ttu-id="02340-109">En appelant la méthode **SetAbort** , un objet retourne le contrôle à son appelant et s’assure que la transaction est finalement abandonnée.</span><span class="sxs-lookup"><span data-stu-id="02340-109">By calling the **SetAbort** method, an object returns control to its caller and ensures that the transaction is ultimately aborted.</span></span>

<span data-ttu-id="02340-110">Toutefois, à moins que l’objet qui appelle [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) soit la racine de la transaction, la transaction continue de s’exécuter même si rien ne peut l’enregistrer à partir de la fin de l’abandon.</span><span class="sxs-lookup"><span data-stu-id="02340-110">However, unless the object calling [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) is the root of the transaction, the transaction continues to run even though nothing can save it from eventually aborting.</span></span> <span data-ttu-id="02340-111">Pour accélérer l’arrêt d’une transaction qui a échoué, vous pouvez générer une erreur pour alerter l’objet racine afin d’appeler également **SetAbort**.</span><span class="sxs-lookup"><span data-stu-id="02340-111">To speed up the termination of a failed transaction, you can raise an error to alert the root object to also call **SetAbort**.</span></span> <span data-ttu-id="02340-112">Pour terminer, l’objet racine doit ensuite envoyer un message d’erreur à son client.</span><span class="sxs-lookup"><span data-stu-id="02340-112">For completion, the root object should then send an error message to its client.</span></span>

<span data-ttu-id="02340-113">Bien qu’il existe de nombreuses approches que vous pouvez prendre pour gérer les erreurs, votre approche doit clairement coordonner les communications entre les objets intérieurs et l’objet racine.</span><span class="sxs-lookup"><span data-stu-id="02340-113">While there are many different approaches you can take to handle errors, your approach should clearly coordinate the communications between interior objects and the root object.</span></span>

<span data-ttu-id="02340-114">Les fragments de code Visual Basic suivants montrent une approche de la gestion des erreurs.</span><span class="sxs-lookup"><span data-stu-id="02340-114">The following Visual Basic code fragments show one approach to error handling.</span></span> <span data-ttu-id="02340-115">Dans le premier fragment, un objet intérieur appelle [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort), génère une erreur et génère un message d’erreur, comme suit :</span><span class="sxs-lookup"><span data-stu-id="02340-115">In the first fragment, an interior object calls [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort), raises an error, and generates an error message, as follows:</span></span>

``` syntax
Dim ObjCtx As ObjectContext
Dim ErrorCode As Long, Description As String

Set ObjCtx = GetObjectContext()
ObjCtx.SetAbort
ErrorCode = vbObjectError + 5
Description = "Some meaningful message"
Err.Raise ErrorCode, , Description
```

<span data-ttu-id="02340-116">Dans le deuxième fragment, l’objet racine gère l’erreur et transmet le message à son client, comme suit :</span><span class="sxs-lookup"><span data-stu-id="02340-116">In the second fragment, the root object handles the error and passes the message to its client, as follows:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="02340-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="02340-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02340-118">Gestion des transactions automatiques dans COM+</span><span class="sxs-lookup"><span data-stu-id="02340-118">Managing Automatic Transactions in COM+</span></span>](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 



