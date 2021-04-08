---
description: Crée un objet transactionnel générique qui commence une transaction. En appelant les méthodes de cette classe, vous pouvez composer le travail de plusieurs objets COM dans une transaction unique et valider ou abandonner explicitement la transaction.
ms.assetid: 5f3f83e0-33fc-4c43-9327-59485c0d8bd3
title: TransactionContextEx, classe (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TransactionContextEx
api_type:
- COM
ms.openlocfilehash: 8cf5c3aaa7ffe126124a909498a7c54cfb012c65
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748837"
---
# <a name="transactioncontextex-class"></a><span data-ttu-id="cb342-104">TransactionContextEx, classe</span><span class="sxs-lookup"><span data-stu-id="cb342-104">TransactionContextEx class</span></span>

<span data-ttu-id="cb342-105">Crée un objet transactionnel générique qui commence une transaction.</span><span class="sxs-lookup"><span data-stu-id="cb342-105">Creates a generic transactional object that begins a transaction.</span></span> <span data-ttu-id="cb342-106">En appelant les méthodes de cette classe, vous pouvez composer le travail de plusieurs objets COM dans une transaction unique et valider ou abandonner explicitement la transaction.</span><span class="sxs-lookup"><span data-stu-id="cb342-106">By calling the methods of this class, you can compose the work of multiple COM objects in a single transaction and explicitly commit or abort the transaction.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="cb342-107">Quand implémenter</span><span class="sxs-lookup"><span data-stu-id="cb342-107">When to implement</span></span>

<span data-ttu-id="cb342-108">Cette classe est implémentée par COM+.</span><span class="sxs-lookup"><span data-stu-id="cb342-108">This class is implemented by COM+.</span></span>



| <span data-ttu-id="cb342-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cb342-109">Requirement</span></span> | <span data-ttu-id="cb342-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb342-110">Value</span></span> |
|------------|--------------------------------------------------------|
| <span data-ttu-id="cb342-111">CLSID</span><span class="sxs-lookup"><span data-stu-id="cb342-111">CLSID</span></span>      | <span data-ttu-id="cb342-112">CLSID \_ TransactionContextEx</span><span class="sxs-lookup"><span data-stu-id="cb342-112">CLSID\_TransactionContextEx</span></span>                            |
| <span data-ttu-id="cb342-113">ProgID</span><span class="sxs-lookup"><span data-stu-id="cb342-113">ProgID</span></span>     | <span data-ttu-id="cb342-114">L "TxCTx. TransactionContextEx"</span><span class="sxs-lookup"><span data-stu-id="cb342-114">L"TxCTx.TransactionContextEx"</span></span>                          |
| <span data-ttu-id="cb342-115">Interfaces</span><span class="sxs-lookup"><span data-stu-id="cb342-115">Interfaces</span></span> | [<span data-ttu-id="cb342-116">**ITransactionContextEx**</span><span class="sxs-lookup"><span data-stu-id="cb342-116">**ITransactionContextEx**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontextex) |



 

## <a name="when-to-use"></a><span data-ttu-id="cb342-117">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="cb342-117">When to use</span></span>

<span data-ttu-id="cb342-118">Un client non transactionnel utilise cette classe pour commencer une transaction.</span><span class="sxs-lookup"><span data-stu-id="cb342-118">A non-transactional client uses this class to begin a transaction.</span></span> <span data-ttu-id="cb342-119">À l’aide des méthodes de cette classe, le client peut appeler des objets COM supplémentaires qui, s’ils sont configurés pour participer à une transaction, s’exécutent dans la limite de transaction de l’objet de contexte de transaction.</span><span class="sxs-lookup"><span data-stu-id="cb342-119">Using the methods of this class, the client can call additional COM objects that, if configured to participate in a transaction, run within the transaction boundary of the transaction context object.</span></span> <span data-ttu-id="cb342-120">En fonction de sa logique métier, le client peut explicitement valider ou abandonner la transaction.</span><span class="sxs-lookup"><span data-stu-id="cb342-120">Based on its business logic, the client can explicitly commit or abort the transaction.</span></span>

<span data-ttu-id="cb342-121">La classe **TransactionContextEx** limite la réutilisation de la logique métier qui dirige la transaction.</span><span class="sxs-lookup"><span data-stu-id="cb342-121">The **TransactionContextEx** class limits reuse of the business logic driving the transaction.</span></span> <span data-ttu-id="cb342-122">Pour cette raison, il est recommandé d’utiliser des objets instanciés à partir de la classe **TransactionContextEx** avec modération.</span><span class="sxs-lookup"><span data-stu-id="cb342-122">For this reason, it is recommended that objects instantiated from the **TransactionContextEx** class be used sparingly.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb342-123">Notes</span><span class="sxs-lookup"><span data-stu-id="cb342-123">Remarks</span></span>

<span data-ttu-id="cb342-124">Pour créer cet objet, appelez [**IObjectContext :: CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance).</span><span class="sxs-lookup"><span data-stu-id="cb342-124">To create this object, call [**IObjectContext::CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance).</span></span>

<span data-ttu-id="cb342-125">La classe **TransactionContextEx** n’a pas été conçue pour être utilisée dans Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="cb342-125">The **TransactionContextEx** class was not designed to be used in Visual Basic.</span></span> <span data-ttu-id="cb342-126">Utilisez la classe [**transactionContext**](transactioncontext.md) à la place.</span><span class="sxs-lookup"><span data-stu-id="cb342-126">Use the [**TransactionContext**](transactioncontext.md) class instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb342-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cb342-127">Requirements</span></span>



| <span data-ttu-id="cb342-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cb342-128">Requirement</span></span> | <span data-ttu-id="cb342-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb342-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cb342-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb342-130">Minimum supported client</span></span><br/> | <span data-ttu-id="cb342-131">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cb342-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="cb342-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb342-132">Minimum supported server</span></span><br/> | <span data-ttu-id="cb342-133">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cb342-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="cb342-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="cb342-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb342-135"><dt>ComSvcs. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb342-135"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb342-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cb342-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb342-137">Configuration des transactions</span><span class="sxs-lookup"><span data-stu-id="cb342-137">Configuring Transactions</span></span>](configuring-transactions.md)
</dt> <dt>

[<span data-ttu-id="cb342-138">**ITransactionContextEx**</span><span class="sxs-lookup"><span data-stu-id="cb342-138">**ITransactionContextEx**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontextex)
</dt> <dt>

[<span data-ttu-id="cb342-139">**TransactionContext**</span><span class="sxs-lookup"><span data-stu-id="cb342-139">**TransactionContext**</span></span>](transactioncontext.md)
</dt> </dl>

 

 




