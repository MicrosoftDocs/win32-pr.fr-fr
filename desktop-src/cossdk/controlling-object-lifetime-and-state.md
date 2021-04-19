---
description: Contrôle de la durée de vie et de l’état des objets
ms.assetid: 172e07a2-1711-4353-9099-ff9d31a564c6
title: Contrôle de la durée de vie et de l’état des objets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 525cc1d582d85bc84ef2b1749a427711d1fe26fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517413"
---
# <a name="controlling-object-lifetime-and-state"></a><span data-ttu-id="7fc0d-103">Contrôle de la durée de vie et de l’état des objets</span><span class="sxs-lookup"><span data-stu-id="7fc0d-103">Controlling Object Lifetime and State</span></span>

<span data-ttu-id="7fc0d-104">Un objet mis en pool peut participer à la façon dont COM+ gère son activité dans le pool en implémentant [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol).</span><span class="sxs-lookup"><span data-stu-id="7fc0d-104">A pooled object can participate in how COM+ manages its activity in the pool by implementing [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol).</span></span> <span data-ttu-id="7fc0d-105">Lorsqu’un objet regroupé est créé, il est agrégé dans un objet plus volumineux qui gère l’objet en appelant les méthodes suivantes sur **IObjectControl** à des points réguliers dans le cycle de vie de l’objet :</span><span class="sxs-lookup"><span data-stu-id="7fc0d-105">When a pooled object is created, it is aggregated into a larger object that will manage the object by calling the following methods on **IObjectControl** at regular points in the object's lifecycle:</span></span>

-   <span data-ttu-id="7fc0d-106">[**Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate): appelée chaque fois que l’objet est retourné à un client, activé dans un contexte spécifique.</span><span class="sxs-lookup"><span data-stu-id="7fc0d-106">[**Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate)—Called whenever the object is returned to a client, activated in a specific context.</span></span>
-   <span data-ttu-id="7fc0d-107">[**Deactivate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate): appelée chaque fois qu’un objet est libéré par le client ou, dans le cas d’un objet activé juste-à-temps, lorsqu’il est désactivé.</span><span class="sxs-lookup"><span data-stu-id="7fc0d-107">[**Deactivate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate)—Called whenever an object is released by the client or, in the case of a JIT-activated object, when it is deactivated.</span></span>
-   <span data-ttu-id="7fc0d-108">[**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled): appelée chaque fois qu’un objet doit être retourné au pool général.</span><span class="sxs-lookup"><span data-stu-id="7fc0d-108">[**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled)—Called whenever an object is to be returned to the general pool.</span></span>

<span data-ttu-id="7fc0d-109">L’implémentation de [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) est facultative, à l’exception des objets transactionnels, qui doivent toujours implémenter [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) pour surveiller l’état des ressources qu’ils détiennent.</span><span class="sxs-lookup"><span data-stu-id="7fc0d-109">Implementing [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) is optional, except for transactional objects, which should always implement [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) to monitor the state of the resources they hold.</span></span> <span data-ttu-id="7fc0d-110">Toutefois, il est recommandé d’implémenter **IObjectControl** dans la plupart des cas, car il offre un moyen efficace de gérer le comportement d’un objet regroupé, comme décrit ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="7fc0d-110">However, it is advisable to implement **IObjectControl** in most cases because it provides an efficient way to manage the behavior of a pooled object, as described below.</span></span>

## <a name="performing-context-specific-initialization"></a><span data-ttu-id="7fc0d-111">Exécution d' Context-Specific</span><span class="sxs-lookup"><span data-stu-id="7fc0d-111">Performing Context-Specific Initialization</span></span>

<span data-ttu-id="7fc0d-112">À l’aide de l' [**activation**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate), vous pouvez initialiser l’objet dans le contexte dans lequel il est activé pour un client donné.</span><span class="sxs-lookup"><span data-stu-id="7fc0d-112">Using [**Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate), you can initialize the object in the context in which it is activated for a given client.</span></span> <span data-ttu-id="7fc0d-113">Par exemple, pour déterminer si l’objet a une affinité de transaction (ses ressources peuvent déjà être inscrites), vous pouvez obtenir l’ID de transaction associé au contexte.</span><span class="sxs-lookup"><span data-stu-id="7fc0d-113">For example, to determine whether the object has transaction affinity (its resources may already be enlisted), you might get the transaction ID associated with the context.</span></span>

<span data-ttu-id="7fc0d-114">En général, vous utilisez [**Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate)pour effectuer l’initialisation qui est cohérente dans toutes les méthodes exposées par l’objet, en le traitant comme une partie spécifique au contexte du constructeur de l’objet.</span><span class="sxs-lookup"><span data-stu-id="7fc0d-114">Typically you would use [**Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate)to perform initialization that is consistent across any methods exposed by the object, treating it as the context-specific portion of the object's constructor.</span></span>

## <a name="cleaning-up-any-client-state"></a><span data-ttu-id="7fc0d-115">Nettoyage de l’état du client</span><span class="sxs-lookup"><span data-stu-id="7fc0d-115">Cleaning Up Any Client State</span></span>

<span data-ttu-id="7fc0d-116">À l’aide de la fonction [**Deactivate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate), vous pouvez supprimer tout état spécifique du client qui peut exister afin que votre objet retourne au pool dans un état totalement générique et puisse ensuite être utilisé par n’importe quel client sans compromettre la sécurité ou l’isolation.</span><span class="sxs-lookup"><span data-stu-id="7fc0d-116">Using [**Deactivate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate), you can get rid of any client-specific state that might exist so that your object returns to the pool in a completely generic state and can then be used by any client without compromising security or isolation.</span></span>

## <a name="controlling-reuse-of-the-object"></a><span data-ttu-id="7fc0d-117">Contrôle de la réutilisation de l’objet</span><span class="sxs-lookup"><span data-stu-id="7fc0d-117">Controlling Reuse of the Object</span></span>

<span data-ttu-id="7fc0d-118">À l’aide de [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled), vous pouvez surveiller l’état interne de votre objet et signaler s’il est adapté à sa réutilisation.</span><span class="sxs-lookup"><span data-stu-id="7fc0d-118">Using [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled), you can monitor the internal state of your object and report on whether it is fit for its reuse.</span></span> <span data-ttu-id="7fc0d-119">Si **CanBePooled** retourne la valeur true et que le nombre maximal de pools n’a pas été atteint, l’objet est remis dans le pool général.</span><span class="sxs-lookup"><span data-stu-id="7fc0d-119">If **CanBePooled** returns True and the pool maximum has not been reached, the object is placed back in the general pool.</span></span> <span data-ttu-id="7fc0d-120">Si **CanBePooled** retourne la valeur false, l’objet est ignoré.</span><span class="sxs-lookup"><span data-stu-id="7fc0d-120">If **CanBePooled** returns False, the object is discarded.</span></span> <span data-ttu-id="7fc0d-121">Dans le cas des composants transactionnels, retourner false arrête la transaction en cours.</span><span class="sxs-lookup"><span data-stu-id="7fc0d-121">In the case of transactional components, returning False will doom the current transaction.</span></span>

<span data-ttu-id="7fc0d-122">En règle générale, vous conservez un membre de données global pour l’objet et, si vous détectez une connexion comme étant incorrecte ou une ressource d’un type dont l’État est incorrect, définissez cette valeur pour refléter la situation actuelle et la renvoyer via [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled).</span><span class="sxs-lookup"><span data-stu-id="7fc0d-122">Typically, you would keep some global data member for the object, and if you detect a connection to be bad or a resource of some kind to be in a bad state, set this to reflect the current situation and return it through [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled).</span></span>

<span data-ttu-id="7fc0d-123">Si un objet n’implémente pas [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled), les instances continuent à être réutilisées jusqu’à ce que le niveau maximal du pool soit atteint.</span><span class="sxs-lookup"><span data-stu-id="7fc0d-123">If an object does not implement [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled), instances will continue to be reused until the pool maximum level is reached.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7fc0d-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7fc0d-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7fc0d-125">Chaînes du constructeur d’objet COM+</span><span class="sxs-lookup"><span data-stu-id="7fc0d-125">COM+ Object Constructor Strings</span></span>](com--object-constructor-strings.md)
</dt> <dt>

[<span data-ttu-id="7fc0d-126">Fonctionnement du regroupement d’objets</span><span class="sxs-lookup"><span data-stu-id="7fc0d-126">How Object Pooling Works</span></span>](how-object-pooling-works.md)
</dt> <dt>

[<span data-ttu-id="7fc0d-127">Amélioration des performances avec la mise en pool d’objets</span><span class="sxs-lookup"><span data-stu-id="7fc0d-127">Improving Performance with Object Pooling</span></span>](improving-performance-with-object-pooling.md)
</dt> <dt>

[<span data-ttu-id="7fc0d-128">Regroupement d’objets transactionnels</span><span class="sxs-lookup"><span data-stu-id="7fc0d-128">Pooling Transactional Objects</span></span>](pooling-transactional-objects.md)
</dt> <dt>

[<span data-ttu-id="7fc0d-129">Conditions requises pour les objets regroupables</span><span class="sxs-lookup"><span data-stu-id="7fc0d-129">Requirements for Poolable Objects</span></span>](requirements-for-poolable-objects.md)
</dt> </dl>

 

 



