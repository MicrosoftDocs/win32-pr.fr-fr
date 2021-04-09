---
description: Vous pouvez configurer un composant à regrouper uniquement lorsqu’il est correctement écrit pour prendre en charge la mise en pool. Pour plus d’informations sur ces conditions requises, consultez Configuration requise pour les objets regroupables.
ms.assetid: ffd812cc-811e-4f2a-8736-d1cb22d5abb7
title: Configuration d’un composant à regrouper
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 780f7e1d9128b213b138e63b9dfa7e0f40642681
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111447"
---
# <a name="configuring-a-component-to-be-pooled"></a><span data-ttu-id="eed23-104">Configuration d’un composant à regrouper</span><span class="sxs-lookup"><span data-stu-id="eed23-104">Configuring a Component to Be Pooled</span></span>

<span data-ttu-id="eed23-105">Vous pouvez configurer un composant à regrouper uniquement lorsqu’il est correctement écrit pour prendre en charge la mise en pool.</span><span class="sxs-lookup"><span data-stu-id="eed23-105">You can configure a component to be pooled only when it is correctly written to support being pooled.</span></span> <span data-ttu-id="eed23-106">Pour plus d’informations sur ces conditions requises, consultez [Configuration requise pour les objets regroupables](requirements-for-poolable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="eed23-106">For details of these requirements, see [Requirements for Poolable Objects](requirements-for-poolable-objects.md).</span></span>

> [!Note]  
> <span data-ttu-id="eed23-107">Par défaut, un composant n’est pas configuré pour être regroupé.</span><span class="sxs-lookup"><span data-stu-id="eed23-107">By default, a component is not configured to be pooled.</span></span>

 

<span data-ttu-id="eed23-108">Quand vous configurez un composant à regrouper, vous pouvez spécifier les propriétés suivantes pour déterminer comment COM+ gère le pool :</span><span class="sxs-lookup"><span data-stu-id="eed23-108">When you configure a component to be pooled, you can specify the following properties to determine how COM+ maintains the pool:</span></span>

-   <span data-ttu-id="eed23-109">**Taille de pool minimale.**</span><span class="sxs-lookup"><span data-stu-id="eed23-109">**Minimum pool size.**</span></span> <span data-ttu-id="eed23-110">Représente le nombre d’objets qui sont créés lorsque l’application démarre et le nombre minimal d’objets qui sont conservés dans le pool pendant que l’application est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="eed23-110">Represents the number of objects that are created when the application starts and the minimum number of objects that are maintained in the pool while the application is running.</span></span> <span data-ttu-id="eed23-111">Si le nombre d’objets disponibles dans le pool descend en dessous de la valeur minimale spécifiée, les nouveaux objets sont créés pour répondre aux demandes d’objets en suspens et le rechargement du pool.</span><span class="sxs-lookup"><span data-stu-id="eed23-111">If the number of available objects in the pool drops below the specified minimum, new objects are created to meet any outstanding object requests and refill the pool.</span></span> <span data-ttu-id="eed23-112">Si le nombre d’objets disponibles dans le pool est supérieur au nombre minimal, ces objets excédentaires sont détruits au cours d’un cycle de nettoyage.</span><span class="sxs-lookup"><span data-stu-id="eed23-112">If the number of available objects in the pool is greater than the minimum number, those surplus objects are destroyed during a clean-up cycle.</span></span>
-   <span data-ttu-id="eed23-113">**Taille maximale du pool.**</span><span class="sxs-lookup"><span data-stu-id="eed23-113">**Maximum pool size.**</span></span> <span data-ttu-id="eed23-114">Représente le nombre maximal d’objets regroupés qui seront créés par le gestionnaire de regroupement, les deux étant activement utilisés par les clients et inactifs dans le pool.</span><span class="sxs-lookup"><span data-stu-id="eed23-114">Represents the maximum number of pooled objects that the pooling manager will create, both actively used by clients and inactive in the pool.</span></span> <span data-ttu-id="eed23-115">Lors de la création d’objets, le gestionnaire de regroupement vérifie que la taille maximale du pool n’a pas été atteinte et, si ce n’est pas le cas, le gestionnaire de pool crée une nouvelle instance de l’objet à distribuer au client.</span><span class="sxs-lookup"><span data-stu-id="eed23-115">When creating objects, the pooling manager checks to verify that the maximum pool size has not been reached and, if it hasn't, the pool manager creates a new instance of the object to dispense to the client.</span></span> <span data-ttu-id="eed23-116">Si la taille maximale du pool a été atteinte, les demandes des clients seront mises en file d’attente et recevront le premier objet disponible du pool sur un premier servi.</span><span class="sxs-lookup"><span data-stu-id="eed23-116">If the maximum pool size has been reached, client requests will be queued and will receive the first available object from the pool on a first-come first-served basis.</span></span> <span data-ttu-id="eed23-117">Les demandes de création d’objet expirent après une période spécifiée.</span><span class="sxs-lookup"><span data-stu-id="eed23-117">Object creation requests will time-out after a specified period.</span></span>
-   <span data-ttu-id="eed23-118">**Délai de création (MS).**</span><span class="sxs-lookup"><span data-stu-id="eed23-118">**Creation timeout (ms).**</span></span> <span data-ttu-id="eed23-119">Spécifie la durée d’attente d’un client, en millisecondes, pour qu’un objet soit retourné à partir du pool après un appel à [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="eed23-119">Specifies how long a client will wait, in milliseconds, for an object to be returned from the pool after a call to [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span> <span data-ttu-id="eed23-120">Si l’appel client échoue, le délai d’attente de l’erreur E \_ est retourné.</span><span class="sxs-lookup"><span data-stu-id="eed23-120">If the client call is unsuccessful, the error E\_TIMEOUT is returned.</span></span>

<span data-ttu-id="eed23-121">**Pour définir les propriétés liées au regroupement**</span><span class="sxs-lookup"><span data-stu-id="eed23-121">**To set pooling-related properties**</span></span>

1.  <span data-ttu-id="eed23-122">Dans le volet d’informations de l’outil d’administration Services de composants, cliquez avec le bouton droit sur le composant que vous souhaitez configurer, puis cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="eed23-122">In the details pane of the Component Services administrative tool, right-click the component that you want to configure, and then click **Properties**.</span></span>

2.  <span data-ttu-id="eed23-123">Dans la boîte de dialogue Propriétés du composant, cliquez sur l’onglet **activation** .</span><span class="sxs-lookup"><span data-stu-id="eed23-123">In the component properties dialog box, click the **Activation** tab.</span></span>

3.  <span data-ttu-id="eed23-124">Pour activer la mise en pool d’objets pour le composant, activez la case à cocher **activer le regroupement d’objets** .</span><span class="sxs-lookup"><span data-stu-id="eed23-124">To enable object pooling for the component, select the **Enable object pooling** check box.</span></span>

4.  <span data-ttu-id="eed23-125">Dans la zone **taille minimale du pool** , entrez le nombre minimal d’objets de ce type dans le pool.</span><span class="sxs-lookup"><span data-stu-id="eed23-125">In the **Minimum pool size** box, enter the minimum number of objects of this type in the pool.</span></span> <span data-ttu-id="eed23-126">Le pool est conservé pour avoir au moins ce nombre d’objets.</span><span class="sxs-lookup"><span data-stu-id="eed23-126">The pool will be maintained to have at least this many objects.</span></span>

5.  <span data-ttu-id="eed23-127">Dans la zone u, entrez le nombre maximal d’objets de ce type dans le pool.</span><span class="sxs-lookup"><span data-stu-id="eed23-127">In the u box, enter the maximum number of objects of this type in the pool.</span></span> <span data-ttu-id="eed23-128">Le nombre d’objets, activés et désactivés, ne dépassera jamais cette valeur.</span><span class="sxs-lookup"><span data-stu-id="eed23-128">The number of objects, both activated and deactivated, will never exceed this value.</span></span>

6.  <span data-ttu-id="eed23-129">Dans la zone **délai de création (MS)** , entrez la durée, en millisecondes, pendant laquelle un client attendra un objet regroupé si celui-ci n’est pas immédiatement disponible.</span><span class="sxs-lookup"><span data-stu-id="eed23-129">In the **Creation timeout (ms)** box, enter the amount of time, in milliseconds, a client will wait for a pooled object if one is not immediately available.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eed23-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="eed23-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eed23-131">Analyse des statistiques des objets</span><span class="sxs-lookup"><span data-stu-id="eed23-131">Monitoring Object Statistics</span></span>](monitoring-object-statistics.md)
</dt> </dl>

 

 
