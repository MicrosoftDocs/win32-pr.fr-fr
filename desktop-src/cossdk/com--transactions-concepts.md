---
description: Concepts des transactions COM+
ms.assetid: e2198514-c403-4b31-8c8c-0b1c83c4f936
title: Concepts des transactions COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 775537128aa0419d02ad3ab614a3ba2ec5eb5b2a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111039"
---
# <a name="com-transactions-concepts"></a><span data-ttu-id="d1890-103">Concepts des transactions COM+</span><span class="sxs-lookup"><span data-stu-id="d1890-103">COM+ Transactions Concepts</span></span>

<span data-ttu-id="d1890-104">Bien que COM+ gère un grand nombre des détails de programmation fastidieux associés au traitement des transactions, il est utile d’avoir une compréhension conceptuelle de la théorie des transactions lorsque vous devez programmer des transactions dans COM+.</span><span class="sxs-lookup"><span data-stu-id="d1890-104">Although COM+ handles many of the tedious programming details associated with transaction processing, it is useful to have a conceptual understanding of transaction theory when you need to program transactions in COM+.</span></span>

<span data-ttu-id="d1890-105">Les rubriques décrites dans le tableau suivant couvrent les concepts qui s’appliquent au traitement des transactions.</span><span class="sxs-lookup"><span data-stu-id="d1890-105">The topics described in the following table cover the concepts that apply to transaction processing.</span></span>



| <span data-ttu-id="d1890-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="d1890-106">Topic</span></span>                                                                                                                     | <span data-ttu-id="d1890-107">Description</span><span class="sxs-lookup"><span data-stu-id="d1890-107">Description</span></span>                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d1890-108">Propriétés ACID</span><span class="sxs-lookup"><span data-stu-id="d1890-108">ACID Properties</span></span>](acid-properties.md)<br/>                                                                         | <span data-ttu-id="d1890-109">Décrit les propriétés atomiques, cohérentes, isolées et durables des transactions.</span><span class="sxs-lookup"><span data-stu-id="d1890-109">Describes the atomic, consistent, isolated, and durable properties of transactions.</span></span><br/>                                                                                              |
| [<span data-ttu-id="d1890-110">Configuration des transactions</span><span class="sxs-lookup"><span data-stu-id="d1890-110">Configuring Transactions</span></span>](configuring-transactions.md)<br/>                                                       | <span data-ttu-id="d1890-111">Décrit les valeurs d’attribut de transaction que vous pouvez assigner à vos composants pour déterminer le degré de protection des transactions à appliquer.</span><span class="sxs-lookup"><span data-stu-id="d1890-111">Describes the transaction attribute values that you can assign to your components to determine the degree of transaction protection to be enforced.</span></span><br/>                              |
| [<span data-ttu-id="d1890-112">Configuration des niveaux d’isolation des transactions</span><span class="sxs-lookup"><span data-stu-id="d1890-112">Configuring Transaction Isolation Levels</span></span>](configuring-transaction-isolation-levels.md)<br/>                       | <span data-ttu-id="d1890-113">Décrit les niveaux d’isolation que vous pouvez affecter à vos transactions, ce qui vous permet d’augmenter ou de diminuer la concurrence en fonction de vos exigences en matière de performances et d’évolutivité.</span><span class="sxs-lookup"><span data-stu-id="d1890-113">Describes the isolation levels you can assign to your transactions, enabling you to increase or decrease concurrency depending on your performance and scalability requirements.</span></span><br/> |
| [<span data-ttu-id="d1890-114">Gestion des transactions automatiques dans COM+</span><span class="sxs-lookup"><span data-stu-id="d1890-114">Managing Automatic Transactions in COM+</span></span>](managing-automatic-transactions-in-com-.md)<br/>                         | <span data-ttu-id="d1890-115">Vue d’ensemble du processus de transaction automatisée pris en charge par COM+.</span><span class="sxs-lookup"><span data-stu-id="d1890-115">Overview of the automated transaction process supported by COM+.</span></span> <br/>                                                                                                                |
| [<span data-ttu-id="d1890-116">Utilisation de composants non transactionnels dans une transaction</span><span class="sxs-lookup"><span data-stu-id="d1890-116">Using Non-Transactional Components in a Transaction</span></span>](using-non-transactional-components-in-a-transaction.md)<br/> | <span data-ttu-id="d1890-117">Décrit comment utiliser des composants non transactionnels dans une transaction et quand les utiliser.</span><span class="sxs-lookup"><span data-stu-id="d1890-117">Describes how to use non-transactional components in a transaction and when you would use them.</span></span><br/>                                                                                  |
| [<span data-ttu-id="d1890-118">Transférer votre propre transaction (BYOT)</span><span class="sxs-lookup"><span data-stu-id="d1890-118">Bring Your Own Transaction (BYOT)</span></span>](bring-your-own-transaction--byot-.md)<br/>                                     | <span data-ttu-id="d1890-119">Décrit comment permettre à un composant d’hériter d’une transaction externe.</span><span class="sxs-lookup"><span data-stu-id="d1890-119">Describes how to allow a component inherit an external transaction.</span></span><br/>                                                                                                              |



 

## <a name="related-topics"></a><span data-ttu-id="d1890-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d1890-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1890-121">Tâches des transactions COM+</span><span class="sxs-lookup"><span data-stu-id="d1890-121">COM+ Transactions Tasks</span></span>](com--transactions-tasks.md)
</dt> </dl>

 

 




