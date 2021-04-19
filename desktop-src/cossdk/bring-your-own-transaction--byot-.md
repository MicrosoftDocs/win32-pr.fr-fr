---
description: Transférer votre propre transaction (BYOT)
ms.assetid: 492875cb-52a7-484f-810e-bd838373b603
title: Transférer votre propre transaction (BYOT)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16ca6f7f12babbf3ad183c4695a68591d9e181a1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516576"
---
# <a name="bring-your-own-transaction-byot"></a><span data-ttu-id="0ddb8-103">Transférer votre propre transaction (BYOT)</span><span class="sxs-lookup"><span data-stu-id="0ddb8-103">Bring Your Own Transaction (BYOT)</span></span>

<span data-ttu-id="0ddb8-104">BYOT permet la création d’un composant avec ou pour hériter d’une transaction externe.</span><span class="sxs-lookup"><span data-stu-id="0ddb8-104">BYOT allows a component to be created with or to inherit an external transaction.</span></span> <span data-ttu-id="0ddb8-105">Autrement dit, un composant qui n’a pas encore de transaction associée peut acquérir une transaction.</span><span class="sxs-lookup"><span data-stu-id="0ddb8-105">That is, a component that does not already have an associated transaction can acquire a transaction.</span></span> <span data-ttu-id="0ddb8-106">Actuellement, les transactions MTS sont automatiques ; le fait qu’une instance de composant réside dans une transaction est déterminé au moment de la création.</span><span class="sxs-lookup"><span data-stu-id="0ddb8-106">Currently, MTS transactions are automatic; whether a component instance lives in a transaction is determined at creation time.</span></span> <span data-ttu-id="0ddb8-107">Les attributs transactionnels d’un composant et son créateur déterminent la transaction associée à une instance donnée.</span><span class="sxs-lookup"><span data-stu-id="0ddb8-107">The transactional attributes of a component and its creator determine what transaction is associated with a given instance.</span></span> <span data-ttu-id="0ddb8-108">Dans tous les cas, MTS contrôle les durées de vie des transactions.</span><span class="sxs-lookup"><span data-stu-id="0ddb8-108">In all cases, MTS controls transaction lifetimes.</span></span> <span data-ttu-id="0ddb8-109">COM+ l’étend pour permettre la définition d’une transaction DTC ou TIP préexistante arbitraire en tant que propriété de transaction du contexte d’un nouveau composant.</span><span class="sxs-lookup"><span data-stu-id="0ddb8-109">COM+ extends this to allow setting an arbitrary pre-existing DTC or TIP transaction as the transaction property of a new component's context.</span></span> <span data-ttu-id="0ddb8-110">Cela permet aux composants configurés d’être associés à des transactions dont les durées de vie sont contrôlées par une analyse de TP, un OTS ou un SGBD.</span><span class="sxs-lookup"><span data-stu-id="0ddb8-110">This allows configured components to be associated with transactions whose lifetimes are controlled by a TP monitor, OTS, or DBMS.</span></span>

> [!Note]  
> <span data-ttu-id="0ddb8-111">Les transactions BYOT doivent être utilisées avec précaution.</span><span class="sxs-lookup"><span data-stu-id="0ddb8-111">BYOT transactions must be used with caution.</span></span> <span data-ttu-id="0ddb8-112">Dans certaines situations, elles peuvent entraîner la répartition d’une transaction sur plusieurs domaines de synchronisation, c’est-à-dire qu’ils autorisent le parallélisme avec une transaction, provoquant une condition de blocage.</span><span class="sxs-lookup"><span data-stu-id="0ddb8-112">In certain situations, they can result in a transaction spanning multiple synchronization domains—that is, they allow parallelism with a transaction, causing a deadlock condition.</span></span> <span data-ttu-id="0ddb8-113">Les transactions automatiques, plutôt que les transactions BYOT, sont le modèle de programmation par défaut pour les rédacteurs de composants métier.</span><span class="sxs-lookup"><span data-stu-id="0ddb8-113">Automatic transactions, rather than BYOT transactions, are the preferred programming model for writers of business components.</span></span>

 

<span data-ttu-id="0ddb8-114">Les interfaces des transactions BYOT incluent l’interface [**ICreateWithTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtransactionex) et l’interface [**ICreateWithTipTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtiptransactionex) .</span><span class="sxs-lookup"><span data-stu-id="0ddb8-114">The interfaces for BYOT transactions include the [**ICreateWithTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtransactionex) interface and the [**ICreateWithTipTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtiptransactionex) interface.</span></span> <span data-ttu-id="0ddb8-115">L’interface **ICreateWithTransactionEx** crée un objet qui est inscrit dans une transaction manuelle.</span><span class="sxs-lookup"><span data-stu-id="0ddb8-115">The **ICreateWithTransactionEx** interface creates an object that is enlisted within a manual transaction.</span></span> <span data-ttu-id="0ddb8-116">L’interface **ICreateWithTipTransactionEx** crée un objet qui est inscrit dans une transaction manuelle à l’aide du TIP (transaction Internet Protocol).</span><span class="sxs-lookup"><span data-stu-id="0ddb8-116">The **ICreateWithTipTransactionEx** interface creates an object that is enlisted within a manual transaction using the Transaction Internet Protocol (TIP).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0ddb8-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0ddb8-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ddb8-118">Héritage de transactions manuelles</span><span class="sxs-lookup"><span data-stu-id="0ddb8-118">Inheriting Manual Transactions</span></span>](inheriting-manual-transactions.md)
</dt> </dl>

 

 



