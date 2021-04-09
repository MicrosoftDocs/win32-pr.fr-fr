---
description: Transactions et activation JIT COM+
ms.assetid: f7fad383-4081-4a49-aa03-59861fcefc97
title: Transactions et activation JIT COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 281691ebc9c8d5c654ea6ff0c3035d7e285f62c5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861550"
---
# <a name="transactions-and-com-jit-activation"></a><span data-ttu-id="f81da-103">Transactions et activation JIT COM+</span><span class="sxs-lookup"><span data-stu-id="f81da-103">Transactions and COM+ JIT Activation</span></span>

<span data-ttu-id="f81da-104">L’activation JIT COM+ est étroitement liée aux transactions automatiques.</span><span class="sxs-lookup"><span data-stu-id="f81da-104">COM+ JIT Activation is closely bound to automatic transactions.</span></span> <span data-ttu-id="f81da-105">Quand vous configurez un composant pour qu’il nécessite une transaction ou nécessite une nouvelle transaction, l’activation JIT est automatiquement activée.</span><span class="sxs-lookup"><span data-stu-id="f81da-105">When you configure a component so that it requires a transaction or requires a new transaction, JIT Activation is automatically enabled as well.</span></span> <span data-ttu-id="f81da-106">Les deux fonctionnalités fonctionnent naturellement conjointement.</span><span class="sxs-lookup"><span data-stu-id="f81da-106">The two features naturally work in conjunction.</span></span> <span data-ttu-id="f81da-107">Les composants transactionnels activés par le JIT partagent les caractéristiques suivantes :</span><span class="sxs-lookup"><span data-stu-id="f81da-107">Transactional, JIT-activated components share the following characteristics:</span></span>

-   <span data-ttu-id="f81da-108">Abandon.</span><span class="sxs-lookup"><span data-stu-id="f81da-108">Statelessness.</span></span> <span data-ttu-id="f81da-109">Vous ne pouvez pas conserver l’État qui violerait l’isolation des transactions, ni conserver l’État qui serait perdu lors de la désactivation d’un objet.</span><span class="sxs-lookup"><span data-stu-id="f81da-109">You would not hold state that would violate transaction isolation nor would you hold state that would be lost on object deactivation.</span></span>

-   <span data-ttu-id="f81da-110">Utilisation rapide.</span><span class="sxs-lookup"><span data-stu-id="f81da-110">Rapid use.</span></span> <span data-ttu-id="f81da-111">Le modèle d’utilisation canonique d’un objet effectuant un travail dans une transaction automatique consiste à effectuer une petite unité de travail, voter et quitter.</span><span class="sxs-lookup"><span data-stu-id="f81da-111">The canonical use pattern for an object performing work in an automatic transaction is to do some small unit of work, vote, and exit.</span></span>

    > [!Note]  
    > <span data-ttu-id="f81da-112">La façon dont vous votez dans les transactions COM+ et l’état de signal pour l’activation juste-à-temps est également étroitement liée.</span><span class="sxs-lookup"><span data-stu-id="f81da-112">The ways that you vote in COM+ transactions and signal doneness for JIT Activation are also closely bound together.</span></span> <span data-ttu-id="f81da-113">Pour plus d’informations, consultez [définition du bit terminé](setting-the-done-bit.md).</span><span class="sxs-lookup"><span data-stu-id="f81da-113">For more information, see [Setting the Done Bit](setting-the-done-bit.md).</span></span>

     

-   <span data-ttu-id="f81da-114">Utilisation répétée.</span><span class="sxs-lookup"><span data-stu-id="f81da-114">Repeated use.</span></span> <span data-ttu-id="f81da-115">Lorsque le travail transactionnel est correctement divisé, les clients utilisent les mêmes objets pour effectuer des fragments de travail atomique.</span><span class="sxs-lookup"><span data-stu-id="f81da-115">When transactional work is properly broken up, clients use the same objects over and over to perform little parcels of atomic work.</span></span>

-   <span data-ttu-id="f81da-116">Désactivé lors de la validation ou de l’abandon.</span><span class="sxs-lookup"><span data-stu-id="f81da-116">Deactivated on commit or abort.</span></span> <span data-ttu-id="f81da-117">Dans COM+, tous les objets de la limite de transaction sont désactivés lorsque la transaction est validée ou abandonnée.</span><span class="sxs-lookup"><span data-stu-id="f81da-117">In COM+, all objects within the transaction boundary are deactivated when the transaction commits or aborts.</span></span>

<span data-ttu-id="f81da-118">Conjointement avec les composants transactionnels COM+, l’activation JIT fait office d’amélioration importante des performances en gardant le canal ouvert en tant que clients qui contiennent des références à long terme aux objets transactionnels.</span><span class="sxs-lookup"><span data-stu-id="f81da-118">In conjunction with COM+ transactional components, JIT activation serves as a big performance enhancement by keeping the channel open as clients hold long-lived references to transactional objects.</span></span> <span data-ttu-id="f81da-119">Pour d’autres améliorations, vous pouvez choisir de regrouper les objets transactionnels afin de réutiliser les ressources qu’ils contiennent, d’accélérer la réactivation des objets et de gérer de près la façon dont vous utilisez les ressources mémoire pour les objets donnés.</span><span class="sxs-lookup"><span data-stu-id="f81da-119">As further enhancements, you can elect to pool the transactional objects to reuse the resources they hold, speed object reactivation time, and closely manage how you use memory resources for given objects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f81da-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f81da-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f81da-121">Concepts d’activation juste-à-temps de COM+</span><span class="sxs-lookup"><span data-stu-id="f81da-121">COM+ Just-in-Time Activation Concepts</span></span>](com--just-in-time-activation-concepts.md)
</dt> <dt>

[<span data-ttu-id="f81da-122">Activation de l’activation JIT pour un composant</span><span class="sxs-lookup"><span data-stu-id="f81da-122">Enabling JIT Activation for a Component</span></span>](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[<span data-ttu-id="f81da-123">Mise en pool d’objets et activation JIT COM+</span><span class="sxs-lookup"><span data-stu-id="f81da-123">Object Pooling and COM+ JIT Activation</span></span>](object-pooling-and-com--jit-activation.md)
</dt> </dl>

 

 



