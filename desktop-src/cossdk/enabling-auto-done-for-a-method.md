---
description: Vous pouvez activer la fonctionnalité de saisie semi-automatique pour toute méthode exposée par un composant pour lequel l’activation JIT COM+ est activée. Si l’activation JIT est désactivée, la saisie semi-automatique n’est pas disponible.
ms.assetid: d699b85c-441f-4ea6-8d03-d1fa9a8a357f
title: Activation de la saisie semi-automatique pour une méthode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0130e5f8b2fde6c6755ef4174892aa35be8a24cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543446"
---
# <a name="enabling-auto-done-for-a-method"></a><span data-ttu-id="d7950-104">Activation de la saisie semi-automatique pour une méthode</span><span class="sxs-lookup"><span data-stu-id="d7950-104">Enabling Auto-Done for a Method</span></span>

<span data-ttu-id="d7950-105">Vous pouvez activer la fonctionnalité de saisie semi-automatique pour toute méthode exposée par un composant pour lequel l’activation JIT COM+ est activée.</span><span class="sxs-lookup"><span data-stu-id="d7950-105">You can enable the auto-done feature for any method exposed by a component for which COM+ JIT activation is enabled.</span></span> <span data-ttu-id="d7950-106">Si l’activation JIT est désactivée, la saisie semi-automatique n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="d7950-106">If JIT activation is disabled, auto-done is unavailable.</span></span>

<span data-ttu-id="d7950-107">Vous devez activer la saisie semi-automatique uniquement pour une méthode qui a intentionnellement été écrite pour en tirer parti, car cette fonctionnalité peut potentiellement modifier le comportement attendu de la méthode.</span><span class="sxs-lookup"><span data-stu-id="d7950-107">You should enable auto-done only for a method that has intentionally been written to take advantage of it because this feature can potentially change the expected behavior of the method.</span></span>

<span data-ttu-id="d7950-108">Lorsque vous activez l’option automatique, vous modifiez le comportement par défaut de l’activation JIT et des transactions automatiques pour cette méthode.</span><span class="sxs-lookup"><span data-stu-id="d7950-108">When you enable auto-done, you are changing the default behavior of both JIT activation and automatic transactions for that method.</span></span> <span data-ttu-id="d7950-109">Vous pouvez utiliser cette fonctionnalité, car elle peut supprimer la nécessité de déclarer explicitement la cohérence et le fait.</span><span class="sxs-lookup"><span data-stu-id="d7950-109">You may want to use this feature because it can remove the necessity to explicitly declare consistency and doneness.</span></span> <span data-ttu-id="d7950-110">Pour ce faire, il suffit de retourner un HRESULT lorsque l’option auto-Done est activée.</span><span class="sxs-lookup"><span data-stu-id="d7950-110">This can instead be done by simply returning an HRESULT when auto-done is enabled.</span></span> <span data-ttu-id="d7950-111">Pour l’essentiel, lorsque vous activez l’exécution automatique, vous demandez à COM+ d’effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="d7950-111">Essentially, when you enable auto-done, you are instructing COM+ to do the following:</span></span>

-   <span data-ttu-id="d7950-112">Définissez le bit Done sur true par défaut dans le contexte dans lequel l’objet s’exécute chaque fois que cette méthode est appelée.</span><span class="sxs-lookup"><span data-stu-id="d7950-112">Set the done bit to True by default on the context in which the object runs whenever this method is called.</span></span>
-   <span data-ttu-id="d7950-113">Inspectez le HRESULT retourné par la méthode. Si elle indique la réussite ou l’échec, définissez le bit de cohérence en conséquence.</span><span class="sxs-lookup"><span data-stu-id="d7950-113">Inspect the HRESULT returned by the method; if it indicates SUCCESS or FAILURE, set the consistency bit accordingly.</span></span> <span data-ttu-id="d7950-114">Cela peut entraîner un appel automatique à [**IObjectContext :: SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) ou [**IObjectContext :: SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort), en fonction également de ce que fait la méthode en interne.</span><span class="sxs-lookup"><span data-stu-id="d7950-114">This can result in an automatic call to [**IObjectContext::SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) or [**IObjectContext::SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort), depending also on what the method does internally.</span></span>

<span data-ttu-id="d7950-115">**Pour activer la saisie semi-automatique pour une méthode**</span><span class="sxs-lookup"><span data-stu-id="d7950-115">**To enable auto-done for a method**</span></span>

1.  <span data-ttu-id="d7950-116">Dans le volet d’informations de l’outil d’administration Services de composants, cliquez avec le bouton droit sur la méthode que vous souhaitez configurer, puis cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="d7950-116">In the details pane of the Component Services administrative tool, right-click the method that you want to configure and then click **Properties**.</span></span>

2.  <span data-ttu-id="d7950-117">Dans la boîte de dialogue Propriétés de la méthode, cliquez sur l’onglet **général** .</span><span class="sxs-lookup"><span data-stu-id="d7950-117">In the method properties dialog box, click the **General** tab.</span></span>

3.  <span data-ttu-id="d7950-118">Pour activer la saisie semi-automatique, activez la case à cocher **désactiver automatiquement cet objet lorsque cette méthode est retournée** .</span><span class="sxs-lookup"><span data-stu-id="d7950-118">To enable auto-done, select the **Automatically deactivate this object when this method returns** check box.</span></span> <span data-ttu-id="d7950-119">Si la case à cocher n’est pas disponible, vous devez d’abord activer l’activation JIT pour le composant.</span><span class="sxs-lookup"><span data-stu-id="d7950-119">If the check box is unavailable, you must first enable JIT Activation for the component.</span></span> <span data-ttu-id="d7950-120">(Pour obtenir des instructions détaillées, consultez[activation de l’activation JIT pour un composant](enabling-jit-activation-for-a-component.md) .)</span><span class="sxs-lookup"><span data-stu-id="d7950-120">(See[Enabling JIT Activation for a Component](enabling-jit-activation-for-a-component.md) for detailed instructions.)</span></span>

4.  <span data-ttu-id="d7950-121">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="d7950-121">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d7950-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d7950-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7950-123">Concepts d’activation juste-à-temps de COM+</span><span class="sxs-lookup"><span data-stu-id="d7950-123">COM+ Just-in-Time Activation Concepts</span></span>](com--just-in-time-activation-concepts.md)
</dt> <dt>

[<span data-ttu-id="d7950-124">Activation de l’activation JIT pour un composant</span><span class="sxs-lookup"><span data-stu-id="d7950-124">Enabling JIT Activation for a Component</span></span>](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[<span data-ttu-id="d7950-125">Définition du bit terminé</span><span class="sxs-lookup"><span data-stu-id="d7950-125">Setting the Done Bit</span></span>](setting-the-done-bit.md)
</dt> </dl>

 

 



