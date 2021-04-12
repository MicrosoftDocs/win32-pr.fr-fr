---
description: Un composant avec au moins une interface de mise en file d’attente est un composant de mise en file d’attente.
ms.assetid: 8183f640-4bf3-4555-8837-90a26130c618
title: Création de composants de mise en file d’attente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03533168a24da1e1f7279a6f2108e25717054103
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393072"
---
# <a name="creating-queuable-components"></a><span data-ttu-id="1eaee-103">Création de composants de mise en file d’attente</span><span class="sxs-lookup"><span data-stu-id="1eaee-103">Creating Queuable Components</span></span>

<span data-ttu-id="1eaee-104">Un composant avec au moins une interface de mise en file d’attente est un composant de mise en *file d’attente*.</span><span class="sxs-lookup"><span data-stu-id="1eaee-104">A component with at least one queuable interface is a *queuable component*.</span></span> <span data-ttu-id="1eaee-105">Pour qu’un composant soit appelé par une file d’attente, les interfaces doivent être marquées comme étant en file d’attente et le composant doit être installé dans une application en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="1eaee-105">For a component to be invoked by a queue, the interfaces must be marked as queuable and the component must be installed in a queued application.</span></span> <span data-ttu-id="1eaee-106">Toutefois, un composant pouvant être mis en file d’attente peut être un composant d’une application qui n’est pas en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="1eaee-106">However, a queuable component can be a component of a non-queued application.</span></span>

<span data-ttu-id="1eaee-107">Une interface de mise en file d’attente ne doit contenir que des paramètres in, aucun paramètre de sortie ni aucune valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="1eaee-107">A queuable interface must contain only in parameters—no out parameters and no return values.</span></span> <span data-ttu-id="1eaee-108">Ces caractéristiques sont vérifiées en analysant les informations de type lors de l’installation du composant.</span><span class="sxs-lookup"><span data-stu-id="1eaee-108">These characteristics are verified by analyzing the type information during component installation.</span></span> <span data-ttu-id="1eaee-109">Si l’interface n’est pas mise en file d’attente, la file d’attente de l’application contenant le composant ne peut pas être activée.</span><span class="sxs-lookup"><span data-stu-id="1eaee-109">If the interface is not queuable, the queue of the application containing the component cannot be activated.</span></span>

<span data-ttu-id="1eaee-110">Pour spécifier une interface COM+ en tant que file d’attente, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="1eaee-110">To specify a COM+ interface as queuable, use the following steps:</span></span>

1.  <span data-ttu-id="1eaee-111">Dans l’arborescence de la console de l’outil d’administration Services de composants, sous **services de composants**, ouvrez le dossier **applications com+** associé à l’ordinateur que vous souhaitez gérer.</span><span class="sxs-lookup"><span data-stu-id="1eaee-111">In the console tree of the Component Services administrative tool, under **Component Services**, open the **COM+ Applications** folder associated with the computer you wish to manage.</span></span>

2.  <span data-ttu-id="1eaee-112">Ouvrez le dossier **interfaces** du composant de l’application com+ que vous souhaitez mettre en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="1eaee-112">Open the **Interfaces** folder of the component of the COM+ application that you want to make queuable.</span></span>

3.  <span data-ttu-id="1eaee-113">Cliquez avec le bouton droit sur l’interface que vous souhaitez marquer comme étant en file d’attente, puis cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="1eaee-113">Right-click the interface that you want to mark as queuable, and then click **Properties**.</span></span>

4.  <span data-ttu-id="1eaee-114">Sélectionnez l’onglet mise en **file d’attente** dans la boîte de dialogue Propriétés.</span><span class="sxs-lookup"><span data-stu-id="1eaee-114">Select the **Queuing** tab in the properties dialog.</span></span>

5.  <span data-ttu-id="1eaee-115">Activez la case à cocher intitulée en **attente**.</span><span class="sxs-lookup"><span data-stu-id="1eaee-115">Activate the check box labeled **Queued**.</span></span>

    > [!Note]  
    > <span data-ttu-id="1eaee-116">Si la case à cocher en file d’attente est grisée, l’interface ne satisfait pas aux contraintes de mise en **file d’attente** décrites ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="1eaee-116">If the **Queued** check box is grayed out, the interface does not satisfy the queuable constraints described above.</span></span>

     

6.  <span data-ttu-id="1eaee-117">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="1eaee-117">Click **OK**.</span></span>

    <span data-ttu-id="1eaee-118">Un composant pouvant être mis en file d’attente peut être identifié en tant que tel, en ajoutant la macro d’attribut QUEUEable à la section interface du fichier source IDL (Interface Definition Language) pour toutes les interfaces qui peuvent être mises en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="1eaee-118">A queuable component can be identified as such by adding the QUEUEABLE attribute macro to the Interface section of the Interface Definition Language (IDL) source file for all interfaces that are queuable.</span></span>

    ``` syntax
#include "mtxattr.h"
    [ object, dual, uuid(), helpstring(IShiphip"), QUEUEABLE ]
    interface IShip:IDispatch{
       [propput, id(1)] HRESULT CustomerId ([in] long CustId);
       [propput, id(2)] HRESULT OrderId ([in] long OrderID);
       [id(3)] HRESULT LineItem ([in] long Qty);
       [id(4)] HRESULT Process ();
    }
    ```

## <a name="related-topics"></a><span data-ttu-id="1eaee-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1eaee-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1eaee-120">Création de files d’attente de composants</span><span class="sxs-lookup"><span data-stu-id="1eaee-120">Creating Component Queues</span></span>](creating-component-queues.md)
</dt> <dt>

[<span data-ttu-id="1eaee-121">Développement de composants en file d’attente</span><span class="sxs-lookup"><span data-stu-id="1eaee-121">Developing Queued Components</span></span>](developing-queued-components.md)
</dt> </dl>

 

 



