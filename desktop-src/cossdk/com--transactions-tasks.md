---
description: Tâches des transactions COM+
ms.assetid: fe4374f1-2452-4316-be57-b866c438404d
title: Tâches des transactions COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70aaebd3e788e1ff12e86b7831979f055367fea7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111038"
---
# <a name="com-transactions-tasks"></a><span data-ttu-id="8ba75-103">Tâches des transactions COM+</span><span class="sxs-lookup"><span data-stu-id="8ba75-103">COM+ Transactions Tasks</span></span>

<span data-ttu-id="8ba75-104">Bien que le traitement automatique des transactions dans COM+ vous permette de consacrer un temps de développement plus productif à la création et à la configuration d’objets que vous souhaitez faire participer aux transactions automatiques, vous pouvez effectuer certaines tâches de programmation pour adapter le comportement des transactions aux besoins de votre application.</span><span class="sxs-lookup"><span data-stu-id="8ba75-104">While automatic transaction processing in COM+ allows you to spend more productive development time in creating and configuring objects that you want to participate in automatic transactions, there are some programming tasks you can perform to tailor transaction behavior to your application requirements.</span></span>

<span data-ttu-id="8ba75-105">Les rubriques suivantes présentent des options de programmation spécifiques liées au traitement des transactions.</span><span class="sxs-lookup"><span data-stu-id="8ba75-105">The following topics discuss specific programming options related to transaction processing.</span></span>



| <span data-ttu-id="8ba75-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="8ba75-106">Topic</span></span>                                                                                             | <span data-ttu-id="8ba75-107">Description</span><span class="sxs-lookup"><span data-stu-id="8ba75-107">Description</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8ba75-108">Définition de l’attribut de transaction</span><span class="sxs-lookup"><span data-stu-id="8ba75-108">Setting the Transaction Attribute</span></span>](setting-the-transaction-attribute.md)<br/>             | <span data-ttu-id="8ba75-109">Décrit comment définir des valeurs d’attribut de transaction pour vos objets de transaction.</span><span class="sxs-lookup"><span data-stu-id="8ba75-109">Describes how to set transaction attribute values for your transaction objects.</span></span><br/>         |
| [<span data-ttu-id="8ba75-110">Définition du niveau d’isolation des transactions</span><span class="sxs-lookup"><span data-stu-id="8ba75-110">Setting the Transaction Isolation Level</span></span>](setting-the-transaction-isolation-level.md)<br/> | <span data-ttu-id="8ba75-111">Décrit comment définir les niveaux d’isolation des transactions pour vos objets de transaction.</span><span class="sxs-lookup"><span data-stu-id="8ba75-111">Describes how to set the transaction isolation levels for your transaction objects.</span></span><br/>     |
| [<span data-ttu-id="8ba75-112">Définition du délai d’expiration de la transaction</span><span class="sxs-lookup"><span data-stu-id="8ba75-112">Setting the Transaction Time-Out</span></span>](setting-the-transaction-time-out.md)<br/>               | <span data-ttu-id="8ba75-113">Décrit comment définir des intervalles de délai d’attente pour vos transactions.</span><span class="sxs-lookup"><span data-stu-id="8ba75-113">Describes how to set time-out intervals for your transactions.</span></span><br/>                          |
| [<span data-ttu-id="8ba75-114">Définition des indicateurs cohérents et terminés</span><span class="sxs-lookup"><span data-stu-id="8ba75-114">Setting the Consistent and Done Flags</span></span>](setting-the-consistent-and-done-flags.md)<br/>     | <span data-ttu-id="8ba75-115">Montre comment utiliser les indicateurs cohérents et terminés pour contrôler le résultat d’une transaction.</span><span class="sxs-lookup"><span data-stu-id="8ba75-115">Shows how to use the consistent and done flags to control the outcome of a transaction.</span></span><br/> |
| [<span data-ttu-id="8ba75-116">Création d’objets BYOT</span><span class="sxs-lookup"><span data-stu-id="8ba75-116">Creating BYOT Objects</span></span>](creating-byot-objects.md)<br/>                                     | <span data-ttu-id="8ba75-117">Décrit comment créer des objets pour que vous puissiez apporter votre propre transaction (BYOT).</span><span class="sxs-lookup"><span data-stu-id="8ba75-117">Describes how to create objects so you can Bring Your Own Transaction (BYOT).</span></span><br/>           |



 

> [!Note]  
> <span data-ttu-id="8ba75-118">En règle générale, tout composant qui met à jour l’état persistant doit prendre en charge les transactions.</span><span class="sxs-lookup"><span data-stu-id="8ba75-118">As a general rule, any component that updates persistent state should support transactions.</span></span> <span data-ttu-id="8ba75-119">Les composants qui combinent les opérations d’au moins deux objets en une seule tâche doivent utiliser des transactions pour simplifier la récupération des erreurs.</span><span class="sxs-lookup"><span data-stu-id="8ba75-119">Components that combine the operations of two or more objects into a single task should use transactions to simplify error recovery.</span></span> <span data-ttu-id="8ba75-120">En outre, pour libérer des ressources, telles que des connexions de base de données, les transactions dans COM+ doivent être aussi courtes que possible.</span><span class="sxs-lookup"><span data-stu-id="8ba75-120">Also, to release resources, such as database connections, transactions in COM+ should be as short as you can make them.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="8ba75-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8ba75-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ba75-122">Concepts des transactions COM+</span><span class="sxs-lookup"><span data-stu-id="8ba75-122">COM+ Transactions Concepts</span></span>](com--transactions-concepts.md)
</dt> </dl>

 

 




