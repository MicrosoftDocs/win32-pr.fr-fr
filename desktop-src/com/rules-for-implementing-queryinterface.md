---
title: Règles d’implémentation de QueryInterface
description: Règles d’implémentation de QueryInterface
ms.assetid: 6db17ed8-06e4-4bae-bc26-113176cc7e0e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e40c743d5306e7dae79bd55ec2c43c01afe742
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "106511100"
---
# <a name="rules-for-implementing-queryinterface"></a><span data-ttu-id="e1487-103">Règles d’implémentation de QueryInterface</span><span class="sxs-lookup"><span data-stu-id="e1487-103">Rules for Implementing QueryInterface</span></span>

<span data-ttu-id="e1487-104">Trois règles principales régissent l’implémentation de la méthode [**IUnknown :: QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) sur un objet com :</span><span class="sxs-lookup"><span data-stu-id="e1487-104">There are three main rules that govern implementing the [**IUnknown::QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) method on a COM object:</span></span>

-   <span data-ttu-id="e1487-105">Les objets doivent avoir une identité.</span><span class="sxs-lookup"><span data-stu-id="e1487-105">Objects must have identity.</span></span>
-   <span data-ttu-id="e1487-106">L’ensemble d’interfaces sur une instance d’objet doit être statique.</span><span class="sxs-lookup"><span data-stu-id="e1487-106">The set of interfaces on an object instance must be static.</span></span>
-   <span data-ttu-id="e1487-107">Il doit être possible d’interroger avec succès toute interface sur un objet à partir d’une autre interface.</span><span class="sxs-lookup"><span data-stu-id="e1487-107">It must be possible to query successfully for any interface on an object from any other interface.</span></span>

## <a name="objects-must-have-identity"></a><span data-ttu-id="e1487-108">Les objets doivent avoir une identité</span><span class="sxs-lookup"><span data-stu-id="e1487-108">Objects Must Have Identity</span></span>

<span data-ttu-id="e1487-109">Pour toute instance d’objet donnée, un appel à [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) avec IID \_ IUnknown doit toujours retourner la même valeur de pointeur physique.</span><span class="sxs-lookup"><span data-stu-id="e1487-109">For any given object instance, a call to [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) with IID\_IUnknown must always return the same physical pointer value.</span></span> <span data-ttu-id="e1487-110">Cela vous permet d’appeler **QueryInterface** sur deux interfaces quelconques et de comparer les résultats pour déterminer s’ils pointent vers la même instance d’un objet.</span><span class="sxs-lookup"><span data-stu-id="e1487-110">This allows you to call **QueryInterface** on any two interfaces and compare the results to determine whether they point to the same instance of an object.</span></span>

## <a name="the-set-of-interfaces-on-an-object-instance-must-be-static"></a><span data-ttu-id="e1487-111">L’ensemble d’interfaces sur une instance d’objet doit être statique</span><span class="sxs-lookup"><span data-stu-id="e1487-111">The Set of Interfaces on an Object Instance Must Be Static</span></span>

<span data-ttu-id="e1487-112">L’ensemble d’interfaces accessible sur un objet via [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) doit être statique et non dynamique.</span><span class="sxs-lookup"><span data-stu-id="e1487-112">The set of interfaces accessible on an object through [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) must be static, not dynamic.</span></span> <span data-ttu-id="e1487-113">En particulier, si **QueryInterface** retourne \_ la valeur OK pour un IID donné une seule fois, il ne doit jamais retourner e \_ nointerface lors des appels suivants sur le même objet. Si **QueryInterface** retourne e \_ nointerface pour un IID donné, les appels suivants pour le même IID sur le même objet ne doivent jamais retourner la valeur \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e1487-113">Specifically, if **QueryInterface** returns S\_OK for a given IID once, it must never return E\_NOINTERFACE on subsequent calls on the same object; and if **QueryInterface** returns E\_NOINTERFACE for a given IID, subsequent calls for the same IID on the same object must never return S\_OK.</span></span>

## <a name="it-must-be-possible-to-query-successfully-for-any-interface-on-an-object-from-any-other-interface"></a><span data-ttu-id="e1487-114">Il doit être possible d’interroger avec succès toute interface sur un objet à partir d’une autre interface</span><span class="sxs-lookup"><span data-stu-id="e1487-114">It Must Be Possible to Query Successfully for Any Interface on an Object from Any Other Interface</span></span>

<span data-ttu-id="e1487-115">Autrement dit, en fonction du code suivant :</span><span class="sxs-lookup"><span data-stu-id="e1487-115">That is, given the following code:</span></span>

``` syntax
IA * pA = (some function returning an IA *); 
IB * pB = NULL; 
HRESULT   hr; 
hr = pA->QueryInterface(IID_IB, &pB); 
 
```

<span data-ttu-id="e1487-116">les règles suivantes s’appliquent :</span><span class="sxs-lookup"><span data-stu-id="e1487-116">the following rules apply:</span></span>

-   <span data-ttu-id="e1487-117">Si vous avez un pointeur vers une interface sur un objet, un appel semblable au suivant à [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) pour cette même interface doit être concluant :</span><span class="sxs-lookup"><span data-stu-id="e1487-117">If you have a pointer to an interface on an object, a call like the following to [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) for that same interface must succeed:</span></span>

    ``` syntax
    pA->QueryInterface(IID_IA, ...) 
     
    ```

-   <span data-ttu-id="e1487-118">Si un appel à [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) pour un deuxième pointeur d’interface se déroule correctement, un appel à **QueryInterface** à partir de ce pointeur pour la première interface doit également être effectué.</span><span class="sxs-lookup"><span data-stu-id="e1487-118">If a call to [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) for a second interface pointer succeeds, a call to **QueryInterface** from that pointer for the first interface must also succeed.</span></span> <span data-ttu-id="e1487-119">Si la commande pB a été obtenue avec succès, les conditions suivantes doivent également réussir :</span><span class="sxs-lookup"><span data-stu-id="e1487-119">If pB was successfully obtained, the following must also succeed:</span></span>

    ``` syntax
    pB->QueryInterface(IID_IA, ...) 
     
    ```

-   <span data-ttu-id="e1487-120">Toute interface doit être en mesure d’interroger une autre interface sur un objet.</span><span class="sxs-lookup"><span data-stu-id="e1487-120">Any interface must be able to query for any other interface on an object.</span></span> <span data-ttu-id="e1487-121">Si la valeur pB a été obtenue avec succès et que vous interrogez avec succès une troisième interface (IC) à l’aide de ce pointeur, vous devez également être en mesure d’interroger avec succès à l’aide du premier pointeur, pA.</span><span class="sxs-lookup"><span data-stu-id="e1487-121">If pB was successfully obtained and you successfully query for a third interface (IC) using that pointer, you must also be able to query successfully for IC using the first pointer, pA.</span></span> <span data-ttu-id="e1487-122">Dans ce cas, la séquence suivante doit être effectuée :</span><span class="sxs-lookup"><span data-stu-id="e1487-122">In this case, the following sequence must succeed:</span></span>

    ``` syntax
    IC * pC = NULL; 
    hr = pB->QueryInterface(IID_IC, &pC); 
    pA->QueryInterface(IID_IC, ...) 
     
    ```

<span data-ttu-id="e1487-123">Les implémentations d’interface doivent conserver un compteur de références de pointeur en suspens à toutes les interfaces sur un objet donné.</span><span class="sxs-lookup"><span data-stu-id="e1487-123">Interface implementations must maintain a counter of outstanding pointer references to all the interfaces on a given object.</span></span> <span data-ttu-id="e1487-124">Vous devez utiliser un **entier non signé** pour le compteur.</span><span class="sxs-lookup"><span data-stu-id="e1487-124">You should use an **unsigned integer** for the counter.</span></span>

<span data-ttu-id="e1487-125">Si un client a besoin de savoir que les ressources ont été libérées, il doit utiliser une méthode dans une interface sur l’objet avec une sémantique de niveau supérieur avant d’appeler [**IUnknown :: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span><span class="sxs-lookup"><span data-stu-id="e1487-125">If a client needs to know that resources have been freed, it must use a method in some interface on the object with higher-level semantics before calling [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e1487-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e1487-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1487-127">Utilisation et implémentation de IUnknown</span><span class="sxs-lookup"><span data-stu-id="e1487-127">Using and Implementing IUnknown</span></span>](using-and-implementing-iunknown.md)
</dt> </dl>

 

 