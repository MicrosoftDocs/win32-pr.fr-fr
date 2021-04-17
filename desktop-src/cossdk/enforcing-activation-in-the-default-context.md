---
description: Un composant COM configuré est généralement activé dans son propre contexte. autrement dit, COM+ référence les informations du catalogue de composants pour fournir tous les services configurés.
ms.assetid: 09dc7165-22b1-4eca-9591-d83e85556f3f
title: Application de l’activation dans le contexte par défaut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41599f71dc37c37c1a9a574d274ca2858835e2df
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524364"
---
# <a name="enforcing-activation-in-the-default-context"></a><span data-ttu-id="980a1-103">Application de l’activation dans le contexte par défaut</span><span class="sxs-lookup"><span data-stu-id="980a1-103">Enforcing Activation in the Default Context</span></span>

<span data-ttu-id="980a1-104">Un composant COM configuré est généralement activé dans son propre contexte. autrement dit, COM+ référence les informations du catalogue du composant pour fournir tous les services configurés.</span><span class="sxs-lookup"><span data-stu-id="980a1-104">A configured COM component is usually activated in its own context; that is, COM+ references the component's catalog information to provide any configured services.</span></span> <span data-ttu-id="980a1-105">Toutefois, vous pouvez choisir d’activer un composant configuré dans le contexte par défaut.</span><span class="sxs-lookup"><span data-stu-id="980a1-105">However, you can choose to activate a configured component in the default context.</span></span> <span data-ttu-id="980a1-106">Un composant COM de base (un composant inscrit qui n’a pas d’informations de catalogue COM+) est généralement activé dans le contexte par défaut.</span><span class="sxs-lookup"><span data-stu-id="980a1-106">A base COM component—a registered component that has no COM+ catalog information—is usually activated in the default context.</span></span>

<span data-ttu-id="980a1-107">L’activation d’un composant COM dans le contexte par défaut offre trois principaux avantages en matière de performances, comme suit :</span><span class="sxs-lookup"><span data-stu-id="980a1-107">Activating a COM component in the default context provides three major performance benefits, as follows:</span></span>

-   <span data-ttu-id="980a1-108">Vous enregistrez des ressources système en limitant le nombre de contextes créés.</span><span class="sxs-lookup"><span data-stu-id="980a1-108">You save system resources by limiting the number of contexts that are created.</span></span>
-   <span data-ttu-id="980a1-109">Vous augmentez les performances en limitant le nombre d’appels entre les contextes.</span><span class="sxs-lookup"><span data-stu-id="980a1-109">You increase performance by limiting the number of cross-context calls.</span></span> <span data-ttu-id="980a1-110">Étant donné que les appels entre les contextes nécessitent un marshaling, il est beaucoup plus rapide pour un objet COM activé dans le contexte par défaut d’effectuer des appels à d’autres objets dans le contexte par défaut.</span><span class="sxs-lookup"><span data-stu-id="980a1-110">Because calls across contexts require marshaling, it is much faster for a COM object activated in the default context to make calls to other objects in the default context.</span></span> <span data-ttu-id="980a1-111">Dans ce cas, les performances (des appels dans le même contexte) sont similaires à celles de l’appel d’une sous-routine.</span><span class="sxs-lookup"><span data-stu-id="980a1-111">The performance in this case (of calls within the same context) is similar to that of calling a subroutine.</span></span>
-   <span data-ttu-id="980a1-112">Vous pouvez importer des applications COM plus anciennes dans COM+ et les exécuter sans problème.</span><span class="sxs-lookup"><span data-stu-id="980a1-112">You can import older COM applications into COM+ and run them without a problem.</span></span> <span data-ttu-id="980a1-113">Par exemple, plusieurs applications COM plus anciennes peuvent être implémentées en supposant qu’elles étaient autorisées à passer des références d’objet au sein d’un cloisonnement sans marshaler les références.</span><span class="sxs-lookup"><span data-stu-id="980a1-113">For example, you may have several older COM applications implemented under the assumption that it was allowable to pass object references within an apartment without marshaling the references.</span></span> <span data-ttu-id="980a1-114">Ces applications COM ne fonctionnent pas lorsqu’elles sont importées dans COM+, car les références d’objet sont passées entre les limites de contexte.</span><span class="sxs-lookup"><span data-stu-id="980a1-114">These COM applications do not work when imported into COM+ because the object references are passed across context boundaries.</span></span> <span data-ttu-id="980a1-115">Toutefois, vous pouvez faire en sorte que ce type d’application COM s’exécute lors de l’importation si vous utilisez l’outil d’administration Services de composants pour marquer toutes les classes de l’application comme **devant être activées dans le contexte par défaut**.</span><span class="sxs-lookup"><span data-stu-id="980a1-115">However, you can make this type of COM application run when imported if you use the Component Services administrative tool to mark all the classes in the application as **Must be activated in the default context**.</span></span>

<span data-ttu-id="980a1-116">Le principal inconvénient de l’activation d’un composant configuré dans le contexte par défaut est que COM+ ne fournit aucun des services configurés du composant.</span><span class="sxs-lookup"><span data-stu-id="980a1-116">The major disadvantage to activating a configured component in the default context is that COM+ does not provide any of the component's configured services.</span></span> <span data-ttu-id="980a1-117">Il existe un compromis entre les performances améliorées et la possibilité d’utiliser les services COM+.</span><span class="sxs-lookup"><span data-stu-id="980a1-117">There is a trade-off between enhanced performance and the ability to use COM+ services.</span></span>

<span data-ttu-id="980a1-118">Par exemple, supposons qu’un composant COM ne nécessite pas de services COM+ (tels que les [transactions](com--transactions.md), [l’activation juste-à-temps](com--just-in-time-activation.md), les [événements](com--events.md), les [composants mis en file d’attente](com--queued-components.md), la [synchronisation](com--synchronization.md)ou le [regroupement d’objets](com--object-pooling.md)) et que le composant effectue un certain nombre d’appels à d’autres composants COM qui peuvent être activés dans le contexte par défaut.</span><span class="sxs-lookup"><span data-stu-id="980a1-118">For example, assume that a COM component does not require any COM+ services (such as [Transactions](com--transactions.md), [Just-in-Time Activation](com--just-in-time-activation.md), [Events](com--events.md), [Queued Components](com--queued-components.md), [Synchronization](com--synchronization.md), or [Object Pooling](com--object-pooling.md)) and that the component makes a number of calls to other COM components that may be activated in the default context.</span></span> <span data-ttu-id="980a1-119">Dans ce cas, il serait judicieux d’activer le composant appelant dans le contexte par défaut.</span><span class="sxs-lookup"><span data-stu-id="980a1-119">In this case, it would be a good idea to activate the calling component in the default context.</span></span>

<span data-ttu-id="980a1-120">Si le composant COM requiert des services COM+, il ne peut pas être marqué comme **devant être activé dans le contexte par défaut**.</span><span class="sxs-lookup"><span data-stu-id="980a1-120">If the COM component requires COM+ services, it cannot be marked as **Must be activated in the default context**.</span></span> <span data-ttu-id="980a1-121">En outre, il n’existe aucun gain de performances réel si un objet COM activé dans le contexte par défaut effectue un certain nombre d’appels à des objets dans d’autres contextes.</span><span class="sxs-lookup"><span data-stu-id="980a1-121">In addition, there is no real performance gain if a COM object activated in the default context makes a number of calls to objects in other contexts.</span></span> <span data-ttu-id="980a1-122">(Pour plus d’informations, consultez [contextes](com--contexts.md).)</span><span class="sxs-lookup"><span data-stu-id="980a1-122">(For more detail, see [Contexts](com--contexts.md).)</span></span>

<span data-ttu-id="980a1-123">**Pour appliquer l’activation dans le contexte par défaut**</span><span class="sxs-lookup"><span data-stu-id="980a1-123">**To enforce activation in the default context**</span></span>

1.  <span data-ttu-id="980a1-124">Dans le volet d’informations de l’outil d’administration Services de composants, cliquez avec le bouton droit sur le composant (situé dans le dossier **composants** de toute application com+ sélectionnée) que vous souhaitez activer dans le contexte par défaut, puis cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="980a1-124">In the details pane of the Component Services administrative tool, right-click the component (located within the **Components** folder of any selected COM+ application) that you want to activate in the default context and then click **Properties**.</span></span>

2.  <span data-ttu-id="980a1-125">Dans la boîte de dialogue Propriétés du composant, cliquez sur l’onglet **activation** .</span><span class="sxs-lookup"><span data-stu-id="980a1-125">In the component properties dialog box, click the **Activation** tab.</span></span>

3.  <span data-ttu-id="980a1-126">Activez la case à cocher **doit être activé dans le contexte par défaut**.</span><span class="sxs-lookup"><span data-stu-id="980a1-126">Select the **Must be activated in the default context** check box.</span></span>

4.  <span data-ttu-id="980a1-127">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="980a1-127">Click **OK**.</span></span>

> [!Note]  
> <span data-ttu-id="980a1-128">Lorsque vous exécutez un composant configuré dans le contexte par défaut, COM+ n’active aucun des services configurés pour ce composant.</span><span class="sxs-lookup"><span data-stu-id="980a1-128">When you run a configured component in the default context, COM+ does not activate any of the configured services for that component.</span></span> <span data-ttu-id="980a1-129">Ces services sont à nouveau disponibles lorsque vous désactivez la case à cocher **doit être activé dans le contexte par défaut** et que vous exécutez ensuite le composant configuré dans son propre contexte.</span><span class="sxs-lookup"><span data-stu-id="980a1-129">These services are available again when you uncheck the **Must be activated in the default context** check box and subsequently run the configured component in its own context.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="980a1-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="980a1-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="980a1-131">Concepts d’activation juste-à-temps de COM+</span><span class="sxs-lookup"><span data-stu-id="980a1-131">COM+ Just-in-Time Activation Concepts</span></span>](com--just-in-time-activation-concepts.md)
</dt> <dt>

[<span data-ttu-id="980a1-132">Application de l’activation dans le contexte de l’appelant</span><span class="sxs-lookup"><span data-stu-id="980a1-132">Enforcing Activation in the Caller's Context</span></span>](enforcing-activation-in-the-caller-s-context.md)
</dt> </dl>

 

 



