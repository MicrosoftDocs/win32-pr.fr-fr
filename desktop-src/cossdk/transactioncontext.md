---
description: Crée un objet transactionnel générique qui commence une transaction.
ms.assetid: efaf1468-4973-472f-af91-85957a52b7df
title: TransactionContext, classe (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TransactionContext
api_type:
- COM
ms.openlocfilehash: 595b5a3192b87420855eb43f1e1e33df37a45c23
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201098"
---
# <a name="transactioncontext-class"></a><span data-ttu-id="a6ef1-103">TransactionContext, classe</span><span class="sxs-lookup"><span data-stu-id="a6ef1-103">TransactionContext class</span></span>

<span data-ttu-id="a6ef1-104">Crée un objet transactionnel générique qui commence une transaction.</span><span class="sxs-lookup"><span data-stu-id="a6ef1-104">Creates a generic transactional object that begins a transaction.</span></span> <span data-ttu-id="a6ef1-105">En appelant les méthodes de cette classe, vous pouvez composer le travail de plusieurs objets COM dans une transaction unique et valider ou abandonner explicitement la transaction.</span><span class="sxs-lookup"><span data-stu-id="a6ef1-105">By calling the methods of this class, you can compose the work of multiple COM objects in a single transaction and explicitly commit or abort the transaction.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="a6ef1-106">Quand implémenter</span><span class="sxs-lookup"><span data-stu-id="a6ef1-106">When to implement</span></span>

<span data-ttu-id="a6ef1-107">Cette classe est implémentée par COM+.</span><span class="sxs-lookup"><span data-stu-id="a6ef1-107">This class is implemented by COM+.</span></span>



| <span data-ttu-id="a6ef1-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a6ef1-108">Requirement</span></span> | <span data-ttu-id="a6ef1-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="a6ef1-109">Value</span></span> |
|------------|----------------------------------------------------|
| <span data-ttu-id="a6ef1-110">CLSID</span><span class="sxs-lookup"><span data-stu-id="a6ef1-110">CLSID</span></span>      | <span data-ttu-id="a6ef1-111">CLSID \_ transactionContext</span><span class="sxs-lookup"><span data-stu-id="a6ef1-111">CLSID\_TransactionContext</span></span>                          |
| <span data-ttu-id="a6ef1-112">ProgID</span><span class="sxs-lookup"><span data-stu-id="a6ef1-112">ProgID</span></span>     | <span data-ttu-id="a6ef1-113">L "TxCTx. TransactionContext"</span><span class="sxs-lookup"><span data-stu-id="a6ef1-113">L"TxCTx.TransactionContext"</span></span>                        |
| <span data-ttu-id="a6ef1-114">Interfaces</span><span class="sxs-lookup"><span data-stu-id="a6ef1-114">Interfaces</span></span> | [<span data-ttu-id="a6ef1-115">**ITransactionContext**</span><span class="sxs-lookup"><span data-stu-id="a6ef1-115">**ITransactionContext**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontext) |



 

## <a name="when-to-use"></a><span data-ttu-id="a6ef1-116">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="a6ef1-116">When to use</span></span>

<span data-ttu-id="a6ef1-117">Un client non transactionnel utilise cette classe pour commencer une transaction.</span><span class="sxs-lookup"><span data-stu-id="a6ef1-117">A non-transactional client uses this class to begin a transaction.</span></span> <span data-ttu-id="a6ef1-118">À l’aide des méthodes de cette classe, le client peut appeler des objets COM supplémentaires qui, s’ils sont configurés pour participer à une transaction, s’exécutent dans la limite de transaction de l’objet de contexte de transaction.</span><span class="sxs-lookup"><span data-stu-id="a6ef1-118">Using the methods of this class, the client can call additional COM objects that, if configured to participate in a transaction, run within the transaction boundary of the transaction context object.</span></span> <span data-ttu-id="a6ef1-119">En fonction de sa logique métier, le client peut explicitement valider ou abandonner la transaction.</span><span class="sxs-lookup"><span data-stu-id="a6ef1-119">Based on its business logic, the client can explicitly commit or abort the transaction.</span></span>

<span data-ttu-id="a6ef1-120">La classe **transactionContext** limite la réutilisation de la logique métier qui dirige la transaction.</span><span class="sxs-lookup"><span data-stu-id="a6ef1-120">The **TransactionContext** class limits reuse of the business logic driving the transaction.</span></span> <span data-ttu-id="a6ef1-121">Pour cette raison, il est recommandé d’utiliser des objets instanciés à partir de la classe **transactionContext** avec modération.</span><span class="sxs-lookup"><span data-stu-id="a6ef1-121">For this reason, it is recommended that objects instantiated from the **TransactionContext** class be used sparingly.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6ef1-122">Notes</span><span class="sxs-lookup"><span data-stu-id="a6ef1-122">Remarks</span></span>

<span data-ttu-id="a6ef1-123">Pour créer cet objet, appelez [**IObjectContext :: CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance).</span><span class="sxs-lookup"><span data-stu-id="a6ef1-123">To create this object, call [**IObjectContext::CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance).</span></span>

<span data-ttu-id="a6ef1-124">Pour utiliser cette classe à partir de Microsoft Visual Basic, ajoutez une référence à la bibliothèque de types des services COM+.</span><span class="sxs-lookup"><span data-stu-id="a6ef1-124">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="a6ef1-125">Un objet TransactionContext peut être déclaré à l’aide de « COMSVCSLib. TransactionContext » comme nom de classe.</span><span class="sxs-lookup"><span data-stu-id="a6ef1-125">A TransactionContext object can be declared using "COMSVCSLib.TransactionContext" as the class name.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6ef1-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a6ef1-126">Requirements</span></span>



| <span data-ttu-id="a6ef1-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a6ef1-127">Requirement</span></span> | <span data-ttu-id="a6ef1-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="a6ef1-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a6ef1-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a6ef1-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a6ef1-130">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a6ef1-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="a6ef1-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a6ef1-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a6ef1-132">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a6ef1-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a6ef1-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="a6ef1-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6ef1-134"><dt>ComSvcs. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6ef1-134"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6ef1-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a6ef1-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6ef1-136">Configuration des transactions</span><span class="sxs-lookup"><span data-stu-id="a6ef1-136">Configuring Transactions</span></span>](configuring-transactions.md)
</dt> <dt>

[<span data-ttu-id="a6ef1-137">**ITransactionContext**</span><span class="sxs-lookup"><span data-stu-id="a6ef1-137">**ITransactionContext**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontext)
</dt> <dt>

[<span data-ttu-id="a6ef1-138">**TransactionContextEx**</span><span class="sxs-lookup"><span data-stu-id="a6ef1-138">**TransactionContextEx**</span></span>](transactioncontextex.md)
</dt> </dl>

 

 




