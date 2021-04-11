---
title: Création et gestion d’un point de connexion de service
description: Lors de la publication avec un SCP, n’oubliez pas qu’il doit contenir les données actuelles sur l’instance de service.
ms.assetid: 2350cb65-3439-4a5f-adc5-b71476793247
ms.tgt_platform: multiple
keywords:
- Création et gestion d’une publicité de point de connexion de service
- point de connexion de service Active Directory, création et maintenance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc6c4ad02b92fa6567fc3b709e45f2f64ce66318
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104031029"
---
# <a name="creating-and-maintaining-a-service-connection-point"></a><span data-ttu-id="01ba4-105">Création et gestion d’un point de connexion de service</span><span class="sxs-lookup"><span data-stu-id="01ba4-105">Creating and Maintaining a Service Connection Point</span></span>

<span data-ttu-id="01ba4-106">Lors de la publication avec un SCP, n’oubliez pas qu’il doit contenir les données actuelles sur l’instance de service.</span><span class="sxs-lookup"><span data-stu-id="01ba4-106">When publishing with an SCP, remember that it must contain current data about the service instance.</span></span> <span data-ttu-id="01ba4-107">Dans le cas contraire, les clients qui se lient au SCP récupèrent les données obsolètes.</span><span class="sxs-lookup"><span data-stu-id="01ba4-107">Otherwise, clients that bind to the SCP retrieve outdated data.</span></span> <span data-ttu-id="01ba4-108">Votre programme d’installation de service, qui crée un SCP, spécifie les valeurs initiales des attributs SCP.</span><span class="sxs-lookup"><span data-stu-id="01ba4-108">Your service installer, that creates an SCP, specifies the initial values for the SCPs attributes.</span></span> <span data-ttu-id="01ba4-109">Ensuite, lorsque l’instance de service démarre, elle doit localiser le SCP et mettre à jour les valeurs d’attribut, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="01ba4-109">Then, when the service instance starts, it must locate the SCP and update the attribute values, if necessary.</span></span> <span data-ttu-id="01ba4-110">De cette façon, les clients sont assurés des données les plus récentes.</span><span class="sxs-lookup"><span data-stu-id="01ba4-110">In this way, clients are assured the most current data.</span></span>

<span data-ttu-id="01ba4-111">Après avoir créé le SCP, votre programme d’installation de service effectue deux étapes supplémentaires qui permettent à votre service de mettre à jour le SCP :</span><span class="sxs-lookup"><span data-stu-id="01ba4-111">After creating the SCP, your service installer performs two additional steps that enable your service to update the SCP:</span></span>

-   <span data-ttu-id="01ba4-112">Définissez les ACE dans le descripteur de sécurité de l’objet SCP pour permettre au service de modifier les attributs SCP au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="01ba4-112">Set ACEs in the security descriptor of the SCP object to enable the service to modify SCP attributes at run time.</span></span> <span data-ttu-id="01ba4-113">Pour plus d’informations et pour obtenir un exemple de code, consultez [activation du compte de service pour accéder aux propriétés SCP](enabling-service-account-to-access-scp-properties.md).</span><span class="sxs-lookup"><span data-stu-id="01ba4-113">For more information and a code example, see [Enabling Service Account to Access SCP Properties](enabling-service-account-to-access-scp-properties.md).</span></span>
-   <span data-ttu-id="01ba4-114">Mettez en cache l' **objectGUID** du SCP dans le registre sur l’ordinateur hôte du service.</span><span class="sxs-lookup"><span data-stu-id="01ba4-114">Cache the **objectGUID** of the SCP in the registry on the service host computer.</span></span> <span data-ttu-id="01ba4-115">Le service récupère le GUID mis en cache à lier au SCP pour vérifier et mettre à jour ses attributs.</span><span class="sxs-lookup"><span data-stu-id="01ba4-115">The service retrieves the cached GUID to bind to the SCP to verify and update its attributes.</span></span>

<span data-ttu-id="01ba4-116">Le programme d’installation du service met en cache l' **objectGUID** du SCP plutôt que son DN.</span><span class="sxs-lookup"><span data-stu-id="01ba4-116">The service installer caches the SCP's **objectGUID** rather than its DN.</span></span> <span data-ttu-id="01ba4-117">L' **objectGUID** n’est jamais modifié, que le SCP soit déplacé ou renommé.</span><span class="sxs-lookup"><span data-stu-id="01ba4-117">The **objectGUID** never changes, regardless of whether the SCP is moved or renamed.</span></span> <span data-ttu-id="01ba4-118">Le DN peut changer si un administrateur déplace ou renomme le SCP.</span><span class="sxs-lookup"><span data-stu-id="01ba4-118">The DN can change if an administrator moves or renames the SCP.</span></span> <span data-ttu-id="01ba4-119">Par exemple, si vous créez un SCP en tant qu’enfant d’un objet ordinateur, le nom unique du SCP change si l’ordinateur est renommé ou déplacé vers un autre domaine ou une autre unité d’organisation.</span><span class="sxs-lookup"><span data-stu-id="01ba4-119">For example, if you create an SCP as a child of a computer object, the distinguished name of the SCP changes if the computer is renamed or moved to a different domain or organizational unit.</span></span>

<span data-ttu-id="01ba4-120">Lorsqu’un programme d’installation de service crée un SCP, il doit lire l' **objectGUID** de l’objet nouvellement créé et le mettre en cache dans le registre de l’ordinateur hôte du service.</span><span class="sxs-lookup"><span data-stu-id="01ba4-120">When a service installer creates an SCP, it must read the **objectGUID** of the newly created object and cache it in the registry of the service host computer.</span></span> <span data-ttu-id="01ba4-121">Utilisez la méthode de [**\_ GUID IADs :: obtenir**](/windows/desktop/ADSI/iads-property-methods) pour obtenir la valeur **objectGUID** dans un format de chaîne adapté à la liaison.</span><span class="sxs-lookup"><span data-stu-id="01ba4-121">Use the [**IADs::get\_GUID**](/windows/desktop/ADSI/iads-property-methods) method to get the **objectGUID** value in string format suitable for binding.</span></span> <span data-ttu-id="01ba4-122">Mettez en cache la chaîne GUID sous la forme d’une valeur sous la clé de Registre suivante.</span><span class="sxs-lookup"><span data-stu-id="01ba4-122">Cache the GUID string as a value under the following registry key.</span></span>

```
HKEY_LOCAL_MACHINE
   vendor name
      product name
```

<span data-ttu-id="01ba4-123">Où « nom du fournisseur » et « nom du produit » identifient le fournisseur et le produit.</span><span class="sxs-lookup"><span data-stu-id="01ba4-123">Where "vendor name" and "product name" identify the vendor and product.</span></span>

<span data-ttu-id="01ba4-124">Lorsque le service démarre, il récupère la chaîne GUID mise en cache à partir du Registre et l’utilise pour établir une liaison avec le SCP.</span><span class="sxs-lookup"><span data-stu-id="01ba4-124">When the service starts, it retrieves the cached GUID string from the registry and uses it to bind to the SCP.</span></span> <span data-ttu-id="01ba4-125">Le service lit les attributs SCP importants et les compare aux valeurs actuelles.</span><span class="sxs-lookup"><span data-stu-id="01ba4-125">The service reads the important SCP attributes and compares them to current values.</span></span> <span data-ttu-id="01ba4-126">Si les valeurs SCP sont obsolètes, le service les met à jour.</span><span class="sxs-lookup"><span data-stu-id="01ba4-126">If the SCP values are outdated, the service updates them.</span></span> <span data-ttu-id="01ba4-127">Les valeurs que le service peut nécessiter pour mettre à jour incluent les **Mots clés**, **serviceBindingInformation**, **servicednsname** et **serviceDNSNameType**.</span><span class="sxs-lookup"><span data-stu-id="01ba4-127">Values that the service might require to update include **keywords**, **serviceBindingInformation**, **serviceDNSName**, and **serviceDNSNameType**.</span></span>

## <a name="examples"></a><span data-ttu-id="01ba4-128">Exemples</span><span class="sxs-lookup"><span data-stu-id="01ba4-128">Examples</span></span>

-   [<span data-ttu-id="01ba4-129">Exemples de scripts</span><span class="sxs-lookup"><span data-stu-id="01ba4-129">Script samples</span></span>](script-samples-for-managing-service-connection-points.md)
-   [<span data-ttu-id="01ba4-130">Exemples de code (C/C++)</span><span class="sxs-lookup"><span data-stu-id="01ba4-130">Code (C/C++) samples</span></span>](code-samples-for-managing-service-connection-points.md)

 

 