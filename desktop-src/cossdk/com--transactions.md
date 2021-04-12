---
description: Transactions COM+
ms.assetid: 40eccce1-a362-4adc-8060-f6923b9162c9
title: Transactions COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aef51f4c8ed5e37101f64d36af385c93ac7e69ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393132"
---
# <a name="com-transactions"></a><span data-ttu-id="e1279-103">Transactions COM+</span><span class="sxs-lookup"><span data-stu-id="e1279-103">COM+ Transactions</span></span>

<span data-ttu-id="e1279-104">Lorsque vous achetez un livre à partir d’une librairie en ligne, vous utilisez une carte de crédit pour commercialiser un livre.</span><span class="sxs-lookup"><span data-stu-id="e1279-104">When you purchase a book from an online bookstore, you use a credit card to trade money for a book.</span></span> <span data-ttu-id="e1279-105">Une fois que vous avez envoyé votre commande, une série d’opérations connexes (validation de votre carte de crédit, vérification de la disponibilité de l’inventaire, etc.) vous permet d’obtenir le livre et de faire en sorte que la librairie récupère votre argent.</span><span class="sxs-lookup"><span data-stu-id="e1279-105">After you submit your order, a series of related operations (validation of your credit card, verification of inventory availability, and so forth) ensures that you get the book and that the bookstore gets your money.</span></span> <span data-ttu-id="e1279-106">Si une seule opération de la série échoue pendant l’échange, la totalité de l’échange échoue.</span><span class="sxs-lookup"><span data-stu-id="e1279-106">If a single operation in the series fails during the exchange, the entire exchange fails.</span></span> <span data-ttu-id="e1279-107">Vous n’avez pas obtenu le livre et la librairie n’obtient pas votre argent.</span><span class="sxs-lookup"><span data-stu-id="e1279-107">You do not get the book, and the bookstore does not get your money.</span></span>

<span data-ttu-id="e1279-108">La technologie chargée de rendre cet échange en ligne équilibré et prévisible est appelée *traitement des transactions*.</span><span class="sxs-lookup"><span data-stu-id="e1279-108">The technology responsible for making this online exchange balanced and predictable is called *transaction processing*.</span></span> <span data-ttu-id="e1279-109">Par programme, une *transaction* est une unité de travail dans laquelle une série d’opérations se produisent.</span><span class="sxs-lookup"><span data-stu-id="e1279-109">Programmatically, a *transaction* is a unit of work in which a series of operations occur.</span></span> <span data-ttu-id="e1279-110">COM+ utilise des transactions de programmation pour s’assurer que les ressources ne sont pas mises à jour de façon permanente, à moins que toutes les opérations dans la transaction se terminent correctement</span><span class="sxs-lookup"><span data-stu-id="e1279-110">COM+ uses programmatic transactions to ensure that resources are not permanently updated unless all operations within the transaction complete successfully.</span></span> <span data-ttu-id="e1279-111">En liant un ensemble d’opérations connexes dans une transaction COM+ qui réussit complètement ou échoue, vous pouvez grandement simplifier la récupération des erreurs.</span><span class="sxs-lookup"><span data-stu-id="e1279-111">By binding a set of related operations together in a COM+ transaction that either completely succeeds or completely fails, you can vastly simplify error recovery.</span></span>

<span data-ttu-id="e1279-112">Les rubriques suivantes présentent la théorie générale du traitement des transactions, fournissent un examen approfondi des transactions dans COM+ et présentent des conseils pratiques pour l’écriture de composants transactionnels.</span><span class="sxs-lookup"><span data-stu-id="e1279-112">The following topics introduce general transaction processing theory, provide a closer look at transactions in COM+, and present practical tips for writing transactional components.</span></span>



| <span data-ttu-id="e1279-113">Rubrique</span><span class="sxs-lookup"><span data-stu-id="e1279-113">Topic</span></span>                                                                   | <span data-ttu-id="e1279-114">Description</span><span class="sxs-lookup"><span data-stu-id="e1279-114">Description</span></span>                                                                    |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="e1279-115">Concepts des transactions COM+</span><span class="sxs-lookup"><span data-stu-id="e1279-115">COM+ Transactions Concepts</span></span>](com--transactions-concepts.md)<br/> | <span data-ttu-id="e1279-116">Présente les termes et les concepts de base.</span><span class="sxs-lookup"><span data-stu-id="e1279-116">Presents basic terms and concepts.</span></span><br/>                                  |
| [<span data-ttu-id="e1279-117">Tâches des transactions COM+</span><span class="sxs-lookup"><span data-stu-id="e1279-117">COM+ Transactions Tasks</span></span>](com--transactions-tasks.md)<br/>       | <span data-ttu-id="e1279-118">Fournit des informations pratiques sur l’écriture de composants transactionnels.</span><span class="sxs-lookup"><span data-stu-id="e1279-118">Provides practical information on writing transactional components.</span></span><br/> |



 

 

 




