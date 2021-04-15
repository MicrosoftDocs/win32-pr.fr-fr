---
description: Recherche de partitions pendant l’activation
ms.assetid: a5452ed6-ab0f-4d38-bc16-1de6cbf57486
title: Recherche de partitions pendant l’activation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58e8912c8277d79c1a20300a1a880644801d0bcb
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2021
ms.locfileid: "104562136"
---
# <a name="locating-partitions-during-activation"></a><span data-ttu-id="ea72e-103">Recherche de partitions pendant l’activation</span><span class="sxs-lookup"><span data-stu-id="ea72e-103">Locating Partitions During Activation</span></span>

<span data-ttu-id="ea72e-104">La localisation de la partition correcte dans laquelle activer un composant dépend des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="ea72e-104">Locating the correct partition in which to activate a component depends on the following:</span></span>

-   <span data-ttu-id="ea72e-105">L’appel de fonction et les paramètres utilisés dans le programme appelant pour activer le composant</span><span class="sxs-lookup"><span data-stu-id="ea72e-105">The function call and parameters used in the calling program to activate the component</span></span>
-   <span data-ttu-id="ea72e-106">Indique si le composant en cours d’activation est local ou distant</span><span class="sxs-lookup"><span data-stu-id="ea72e-106">Whether the component being activated is local or remote</span></span>
-   <span data-ttu-id="ea72e-107">Utilisation interne du cache de partition</span><span class="sxs-lookup"><span data-stu-id="ea72e-107">The internal use of the partition cache</span></span>

## <a name="the-calling-program"></a><span data-ttu-id="ea72e-108">Programme appelant</span><span class="sxs-lookup"><span data-stu-id="ea72e-108">The Calling Program</span></span>

<span data-ttu-id="ea72e-109">COM+ sélectionne la partition pour l’activation des composants en fonction de la façon dont le programme appelant active le composant.</span><span class="sxs-lookup"><span data-stu-id="ea72e-109">COM+ selects the partition for component activation based on how the calling program activates the component.</span></span>

<span data-ttu-id="ea72e-110">COM+ peut effectuer trois actions différentes lors de la sélection d’une partition pour l’activation d’un composant.</span><span class="sxs-lookup"><span data-stu-id="ea72e-110">There are three different actions that COM+ can take when selecting a partition for component activation.</span></span> <span data-ttu-id="ea72e-111">L’action entreprise dépend de la manière dont le programme appelant instancie l’objet qui est, que l’appel de fonction inclue un moniker de partition, qui se compose d’un ID de partition et d’un CLSID, ou qui inclut un CLSID uniquement.</span><span class="sxs-lookup"><span data-stu-id="ea72e-111">The action taken depends on how the calling program instantiates the object that is, whether the function call includes a partition moniker, which consists of a partition ID and a CLSID, or includes a CLSID only.</span></span>

<span data-ttu-id="ea72e-112">Le tableau suivant répertorie les différentes actions que COM+ peut effectuer, par ordre de priorité, pour localiser une partition.</span><span class="sxs-lookup"><span data-stu-id="ea72e-112">The following table shows the various actions that COM+ can take, in order of precedence, to locate a partition.</span></span>



| <span data-ttu-id="ea72e-113">Appel de fonction</span><span class="sxs-lookup"><span data-stu-id="ea72e-113">Function call</span></span>                                                  | <span data-ttu-id="ea72e-114">Paramètre</span><span class="sxs-lookup"><span data-stu-id="ea72e-114">Parameter</span></span>                                                      | <span data-ttu-id="ea72e-115">Action COM+</span><span class="sxs-lookup"><span data-stu-id="ea72e-115">COM+ action</span></span>                                                                                                                                                                                    |
|----------------------------------------------------------------|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea72e-116">[**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) ou **GetObject**</span><span class="sxs-lookup"><span data-stu-id="ea72e-116">[**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) or **GetObject**</span></span><br/> | <span data-ttu-id="ea72e-117">Moniker de partition (comprend l’ID de partition et le CLSID)</span><span class="sxs-lookup"><span data-stu-id="ea72e-117">Partition moniker (includes partition ID and CLSID)</span></span><br/> | <span data-ttu-id="ea72e-118">Utilise l’ID de partition spécifié dans le moniker de la partition.</span><span class="sxs-lookup"><span data-stu-id="ea72e-118">Uses the partition ID specified in the partition moniker.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="ea72e-119">**CoCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="ea72e-119">**CoCreateInstance**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)<br/>        | <span data-ttu-id="ea72e-120">CLSID</span><span class="sxs-lookup"><span data-stu-id="ea72e-120">CLSID</span></span><br/>                                               | <span data-ttu-id="ea72e-121">Utilise l’ID de partition de la partition par défaut de l’identité de l’utilisateur ou l’ID de partition qui a été ajouté au contexte au cours d’une activation de composant précédente dans le même processus.</span><span class="sxs-lookup"><span data-stu-id="ea72e-121">Uses either the partition ID of the user identity's default partition or the partition ID that was added to the context during a previous component activation in the same process.</span></span><br/> |



 

<span data-ttu-id="ea72e-122">Les actions COM+ répertoriées dans le tableau précédent sont expliquées dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="ea72e-122">The COM+ actions listed in the preceding table are explained in the following sections.</span></span>

## <a name="use-of-partition-monikers"></a><span data-ttu-id="ea72e-123">Utilisation des monikers de partition</span><span class="sxs-lookup"><span data-stu-id="ea72e-123">Use of Partition Monikers</span></span>

<span data-ttu-id="ea72e-124">Une partition peut être sélectionnée explicitement dans un appel de fonction à l’aide d’un *moniker de partition*.</span><span class="sxs-lookup"><span data-stu-id="ea72e-124">A partition can be selected explicitly within a function call by using a *partition moniker*.</span></span> <span data-ttu-id="ea72e-125">Un moniker de partition est utilisé dans le code pour spécifier explicitement la partition du composant activé.</span><span class="sxs-lookup"><span data-stu-id="ea72e-125">A partition moniker is used within code to explicitly specify the partition of the activated component.</span></span> <span data-ttu-id="ea72e-126">Si un moniker de partition est utilisé pour localiser la partition, l’activation se produit à partir de cette partition.</span><span class="sxs-lookup"><span data-stu-id="ea72e-126">If a partition moniker is used to locate the partition, the activation occurs from that partition.</span></span> <span data-ttu-id="ea72e-127">Autrement dit, l’ID de partition inclus dans le moniker est prioritaire sur la partition par défaut de l’utilisateur ou sur un ID de partition qui existe dans le contexte de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="ea72e-127">That is, the partition ID included in the moniker takes precedence over the user's default partition or over a partition ID that exists in the caller's context.</span></span>

<span data-ttu-id="ea72e-128">Dans le code C++, la syntaxe d’utilisation d’un moniker de partition est la suivante :</span><span class="sxs-lookup"><span data-stu-id="ea72e-128">In C++ code, the syntax for the use of a partition moniker is as follows:</span></span>


```C++
HRESULT CoGetObject(
  L"partition:partitionGUID/new:clsid",
  pBindOptions,
  IID_IUnknown,
  (void**)&pIUnknown);
```



<span data-ttu-id="ea72e-129">L’exemple suivant montre un extrait de code C++, dans lequel un moniker de partition est utilisé en tant qu’argument de la fonction [**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) :</span><span class="sxs-lookup"><span data-stu-id="ea72e-129">The following example shows a snippet of C++ code, in which a partition moniker is being used as an argument to the [**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) function:</span></span>


```C++
// Create CLSID1 configured in the Production partition.
HRESULT hr = CoGetObject(
  L"partition:{35056070-D5B7-4b59-9FBF-0D23417F6937}/new:CLSID1",
  pBindOptions, IID_IUnknown, (void**)&pIUnknown);
```



<span data-ttu-id="ea72e-130">Dans Visual Basic Code, la syntaxe d’un moniker de partition est la suivante :</span><span class="sxs-lookup"><span data-stu-id="ea72e-130">In Visual Basic code, the syntax for a partition moniker is as follows:</span></span>


```VB
GetObject("partition:partitionGUID/new:CLSID") As Object
```



<span data-ttu-id="ea72e-131">L’exemple suivant montre un extrait de code Visual Basic, dans lequel un moniker de partition est utilisé en tant qu’argument de la fonction **GetObject** :</span><span class="sxs-lookup"><span data-stu-id="ea72e-131">The following example shows a snippet of Visual Basic code, in which a partition moniker is being used as an argument to the **GetObject** function:</span></span>


```VB
Dim objCLSID1 As Object
Set objCLSID1 = GetObject( _
   "partition:{35056070-D5B7-4b59-9FBF-0D23417F6937}/new:CLSID1")
```



## <a name="use-of-default-mapping"></a><span data-ttu-id="ea72e-132">Utilisation du mappage par défaut</span><span class="sxs-lookup"><span data-stu-id="ea72e-132">Use of Default Mapping</span></span>

<span data-ttu-id="ea72e-133">Lorsque la fonction [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) est utilisée pour activer un composant à l’aide du CLSID du composant, com+ utilise le mappage d’identité d’utilisateur par défaut, c’est-à-dire le jeu de partitions auquel l’utilisateur est mappé dans Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ea72e-133">When the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function is used to activate a component, using the component's CLSID, COM+ uses the default user-identity mapping that is, the partition set that the user is mapped to within Active Directory.</span></span> <span data-ttu-id="ea72e-134">Toutefois, si l’utilisateur n’est pas mappé à un ensemble de partitions dans Active Directory, la partition globale est sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="ea72e-134">However, if the user is not mapped to a partition set within Active Directory, the Global Partition is selected.</span></span>

## <a name="use-of-partition-ids-and-object-context"></a><span data-ttu-id="ea72e-135">Utilisation des ID de partition et du contexte de l’objet</span><span class="sxs-lookup"><span data-stu-id="ea72e-135">Use of Partition IDs and Object Context</span></span>

<span data-ttu-id="ea72e-136">L’une des cinq propriétés assignées à une nouvelle partition est l’ID de partition.</span><span class="sxs-lookup"><span data-stu-id="ea72e-136">One of the five properties assigned to a new partition is the partition ID.</span></span> <span data-ttu-id="ea72e-137">Lorsque le programme client appelle la fonction [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) pour instancier un objet, l’ID de partition est ajouté au contexte.</span><span class="sxs-lookup"><span data-stu-id="ea72e-137">When the client program calls the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function to instantiate an object, the partition ID is added to the context.</span></span> <span data-ttu-id="ea72e-138">L’utilisation de l’ID de partition du contexte pour localiser la partition est importante, car elle garantit qu’une fois qu’une chaîne d’activations a commencé, l’ID de partition reste le même, sauf si elle est modifiée explicitement via un moniker de partition.</span><span class="sxs-lookup"><span data-stu-id="ea72e-138">Using the partition ID from the context to locate the partition is important because it ensures that after a chain of activations has begun, the partition ID remains the same unless it is changed explicitly through a partition moniker.</span></span>

<span data-ttu-id="ea72e-139">Pour plus d’informations sur la localisation des partitions lors de l’activation, consultez [composants et partitions en file d’attente com+](com--queued-components-and-partitions.md).</span><span class="sxs-lookup"><span data-stu-id="ea72e-139">For additional information on locating partitions during activation, see [COM+ Queued Components and Partitions](com--queued-components-and-partitions.md).</span></span>

## <a name="local-and-remote-activation"></a><span data-ttu-id="ea72e-140">Activation locale et à distance</span><span class="sxs-lookup"><span data-stu-id="ea72e-140">Local and Remote Activation</span></span>

-   <span data-ttu-id="ea72e-141">Si le composant appelé existe sur un autre ordinateur, les propriétés de partition (y compris l’ID de partition) sont marshalées vers l’autre ordinateur et le composant est activé à partir de la partition marshalée.</span><span class="sxs-lookup"><span data-stu-id="ea72e-141">If the component being called exists on another computer, the partition properties (including the partition ID) are marshaled to the other computer and the component is activated from the marshaled partition.</span></span> <span data-ttu-id="ea72e-142">Si aucun ID de partition n’a été marshalé, COM+ utilise l’ensemble de partitions par défaut mappé à l’identité de l’utilisateur dans Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ea72e-142">If no partition ID was marshaled, COM+ uses the default partition set mapped to the user identity within Active Directory.</span></span>

## <a name="the-partition-cache"></a><span data-ttu-id="ea72e-143">Cache de partition</span><span class="sxs-lookup"><span data-stu-id="ea72e-143">The Partition Cache</span></span>

<span data-ttu-id="ea72e-144">Dans un environnement de domaine, COM+ utilise les mappages dans Active Directory pour localiser la partition correcte pour l’activation des composants.</span><span class="sxs-lookup"><span data-stu-id="ea72e-144">In a domain environment, COM+ uses the mappings in Active Directory to locate the correct partition for component activation.</span></span> <span data-ttu-id="ea72e-145">Toutefois, les recherches fréquentes dans Active Directory peuvent entraîner un trafic réseau excessif.</span><span class="sxs-lookup"><span data-stu-id="ea72e-145">However, frequent lookups in Active Directory can result in excessive network traffic.</span></span> <span data-ttu-id="ea72e-146">Pour réduire le trafic réseau résultant des recherches fréquentes de mappages d’utilisateur à partition dans Active Directory, COM+ utilise un *cache de partition*.</span><span class="sxs-lookup"><span data-stu-id="ea72e-146">To minimize network traffic resulting from frequent lookups of user-to-partition-set mapping in Active Directory, COM+ uses a *partition cache*.</span></span>

<span data-ttu-id="ea72e-147">Le cache de partition contient les mappages effectués dans Active Directory entre les identités des utilisateurs ou les unités d’organisation et leurs jeux de partitions.</span><span class="sxs-lookup"><span data-stu-id="ea72e-147">The partition cache contains the mappings that were made in Active Directory between user identities or OUs and their partition sets.</span></span> <span data-ttu-id="ea72e-148">Ce cache de partition se trouve sur le serveur d’applications sur lequel résident les applications COM+.</span><span class="sxs-lookup"><span data-stu-id="ea72e-148">This partition cache is located on the application server on which the COM+ applications reside.</span></span>

<span data-ttu-id="ea72e-149">Lorsque COM+ doit déterminer la partition par défaut d’un utilisateur ou valider les droits d’accès d’un utilisateur à une partition, il vérifie localement le cache de partition pour rechercher le mappage de l’utilisateur, au lieu de vérifier Active Directory à distance.</span><span class="sxs-lookup"><span data-stu-id="ea72e-149">When COM+ needs to determine a user's default partition or validate a user's access rights to a partition, it checks the partition cache locally to look up the user's mapping, instead of checking Active Directory remotely.</span></span>

<span data-ttu-id="ea72e-150">Si la recherche dans le cache de partition échoue, COM+ vérifie Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ea72e-150">If the lookup in the partition cache fails, COM+ then checks Active Directory.</span></span> <span data-ttu-id="ea72e-151">Si la recherche est réussie dans Active Directory, COM+ stocke ce mappage dans le cache de partition.</span><span class="sxs-lookup"><span data-stu-id="ea72e-151">If the lookup is successful in Active Directory, COM+ stores that mapping in the partition cache.</span></span> <span data-ttu-id="ea72e-152">La prochaine fois qu’une recherche est effectuée pour ce mappage d’utilisateur à partition, COM+ la trouvera dans le cache de partition.</span><span class="sxs-lookup"><span data-stu-id="ea72e-152">The next time a lookup is done for that user-to-partition mapping, COM+ will find it in the partition cache.</span></span>

<span data-ttu-id="ea72e-153">L’illustration suivante montre le processus utilisé par COM+ pour localiser une partition pour l’activation d’un composant.</span><span class="sxs-lookup"><span data-stu-id="ea72e-153">The following illustration shows the process that COM+ uses to locate a partition for component activation.</span></span>

![Diagramme illustrant une arborescence de résolution des problèmes pour le processus utilisé par COM+ pour localiser une partition pour l’activation des composants.](images/5d00eb4e-4572-491c-85e9-33ceed2cd753.png)

<span data-ttu-id="ea72e-155">La taille du cache et l’heure d’expiration des entrées du cache sont définies via des clés de registre.</span><span class="sxs-lookup"><span data-stu-id="ea72e-155">The size of the cache and the expiration time for the cache entries are set via registry keys.</span></span> <span data-ttu-id="ea72e-156">Pour plus d’informations sur la configuration de ces clés de Registre, consultez [création et configuration de partitions com+](creating-and-configuring-com--partitions.md).</span><span class="sxs-lookup"><span data-stu-id="ea72e-156">For information on configuring these registry keys, see [Creating and Configuring COM+ Partitions](creating-and-configuring-com--partitions.md).</span></span>

> [!Note]  
> <span data-ttu-id="ea72e-157">Si un ordinateur serveur est déconnecté du réseau et que le mappage utilisateur à partition est modifié alors que le serveur est déconnecté, le cache de partition peut contenir un mappage utilisateur à partition obsolète.</span><span class="sxs-lookup"><span data-stu-id="ea72e-157">If a server computer is disconnected from the network and the user-to-partition mapping is changed while the server is disconnected, the partition cache might contain outdated user-to-partition mapping.</span></span> <span data-ttu-id="ea72e-158">Cela peut entraîner une erreur d’activation si le mappage utilisateur-partition est le mécanisme utilisé pour activer un composant.</span><span class="sxs-lookup"><span data-stu-id="ea72e-158">This could result in an activation error if user-to-partition mapping is the mechanism used to activate a component.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ea72e-159">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ea72e-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea72e-160">Recherche d’un composant pour l’activation</span><span class="sxs-lookup"><span data-stu-id="ea72e-160">Locating a Component for Activation</span></span>](locating-a-component-for-activation.md)
</dt> </dl>

 

