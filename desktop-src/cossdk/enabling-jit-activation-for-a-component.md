---
description: Activation de l’activation JIT pour un composant
ms.assetid: ccf7c98b-8b1a-431d-b417-83f79734f691
title: Activation de l’activation JIT pour un composant
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f61cc5c79270a926bb50e3408766df63f4484c8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516380"
---
# <a name="enabling-jit-activation-for-a-component"></a><span data-ttu-id="de233-103">Activation de l’activation JIT pour un composant</span><span class="sxs-lookup"><span data-stu-id="de233-103">Enabling JIT Activation for a Component</span></span>

<span data-ttu-id="de233-104">Vous devez configurer un composant qui doit être activé juste-à-temps uniquement lorsqu’il est écrit correctement pour prendre en charge le service d’activation juste-à-temps (JIT) COM+.</span><span class="sxs-lookup"><span data-stu-id="de233-104">You should configure a component to be JIT activated only when it is correctly written to support the COM+ Just-in-Time (JIT) Activation service.</span></span> <span data-ttu-id="de233-105">Si un composant est désactivé entre les appels de méthode, il perd tout état associé.</span><span class="sxs-lookup"><span data-stu-id="de233-105">If a component is deactivated between method calls, it will lose any associated state.</span></span> <span data-ttu-id="de233-106">Étant donné le comportement par défaut de l’activation JIT, il est peu probable que cela se produise quand vous ne le pensez pas, mais vous devez être conscient des exigences d’un composant avant de modifier sa configuration et des attentes des clients qui appellent le composant.</span><span class="sxs-lookup"><span data-stu-id="de233-106">Given the default behavior of JIT Activation, this is unlikely to occur when you don't expect it to, but you should be aware of a component's requirements prior to changing its configuration and of the expectations of clients that will be calling the component.</span></span>

> [!Note]  
> <span data-ttu-id="de233-107">Si un composant est configuré pour exiger des transactions, le service d’activation JIT COM+ est activé automatiquement.</span><span class="sxs-lookup"><span data-stu-id="de233-107">If a component is configured to require transactions, the COM+ JIT Activation service is enabled automatically.</span></span> <span data-ttu-id="de233-108">Vous ne pouvez pas le désactiver dans ce cas.</span><span class="sxs-lookup"><span data-stu-id="de233-108">You cannot disable it in this case.</span></span> <span data-ttu-id="de233-109">Pour plus d’informations, consultez [Configuration des transactions](configuring-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="de233-109">For more detail, see [Configuring Transactions](configuring-transactions.md).</span></span>

 

<span data-ttu-id="de233-110">Lorsque vous activez l’activation JIT pour un composant, son attribut de synchronisation est défini sur obligatoire pour ce composant.</span><span class="sxs-lookup"><span data-stu-id="de233-110">When you enable JIT Activation for a component, its synchronization attribute is set to required for that component.</span></span> <span data-ttu-id="de233-111">Dans ce cas, vous ne pouvez pas modifier le paramètre de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="de233-111">You cannot change the synchronization setting in this case.</span></span> <span data-ttu-id="de233-112">Pour plus d’informations, consultez [dépendances de synchronisation](synchronization-dependencies.md).</span><span class="sxs-lookup"><span data-stu-id="de233-112">For more detail, see [Synchronization Dependencies](synchronization-dependencies.md).</span></span>

<span data-ttu-id="de233-113">**Pour activer l’activation JIT**</span><span class="sxs-lookup"><span data-stu-id="de233-113">**To enable JIT Activation**</span></span>

1.  <span data-ttu-id="de233-114">Dans le volet d’informations de l’outil d’administration Services de composants, cliquez avec le bouton droit sur le composant que vous souhaitez configurer, puis cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="de233-114">In the details pane of the Component Services administrative tool, right-click the component that you want to configure and then click **Properties**.</span></span>

2.  <span data-ttu-id="de233-115">Dans la boîte de dialogue Propriétés du composant, cliquez sur l’onglet **activation** .</span><span class="sxs-lookup"><span data-stu-id="de233-115">In the component properties dialog box, click the **Activation** tab.</span></span>

3.  <span data-ttu-id="de233-116">Pour activer l’activation JIT pour le composant, activez la case à cocher **activer l’activation juste-à-temps** .</span><span class="sxs-lookup"><span data-stu-id="de233-116">To enable JIT activation for the component, select the **Enable Just In Time Activation** check box.</span></span>

4.  <span data-ttu-id="de233-117">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="de233-117">Click **OK**.</span></span>

<span data-ttu-id="de233-118">Lorsque vous avez activé l’activation JIT pour un composant, vous avez la possibilité d’activer la fonctionnalité de saisie semi-automatique pour toute méthode exposée par ce composant.</span><span class="sxs-lookup"><span data-stu-id="de233-118">When you have enabled JIT Activation for a component, you have the option of enabling the auto-done feature for any method exposed by that component.</span></span> <span data-ttu-id="de233-119">Pour plus d’informations, consultez [activation de la saisie semi-automatique pour une méthode](enabling-auto-done-for-a-method.md) .</span><span class="sxs-lookup"><span data-stu-id="de233-119">See [Enabling Auto-Done for a Method](enabling-auto-done-for-a-method.md) for more information.</span></span>

## <a name="related-topics"></a><span data-ttu-id="de233-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="de233-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de233-121">Activation de la saisie semi-automatique pour une méthode</span><span class="sxs-lookup"><span data-stu-id="de233-121">Enabling Auto-Done for a Method</span></span>](enabling-auto-done-for-a-method.md)
</dt> <dt>

[<span data-ttu-id="de233-122">Définition du bit terminé</span><span class="sxs-lookup"><span data-stu-id="de233-122">Setting the Done Bit</span></span>](setting-the-done-bit.md)
</dt> </dl>

 

 



