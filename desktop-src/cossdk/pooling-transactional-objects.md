---
description: Les composants transactionnels à regrouper ont des exigences particulières.
ms.assetid: 32e2f830-c30a-4dbc-8e69-dd2038851998
title: Regroupement d’objets transactionnels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 006ba32ad2ac550be4fa4418dde322ded26c64c7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516180"
---
# <a name="pooling-transactional-objects"></a><span data-ttu-id="82bf4-103">Regroupement d’objets transactionnels</span><span class="sxs-lookup"><span data-stu-id="82bf4-103">Pooling Transactional Objects</span></span>

<span data-ttu-id="82bf4-104">Les composants transactionnels à regrouper ont des exigences particulières.</span><span class="sxs-lookup"><span data-stu-id="82bf4-104">Transactional components that are to be pooled have special requirements.</span></span>

## <a name="manually-enlisting-resources"></a><span data-ttu-id="82bf4-105">Inscription manuelle des ressources</span><span class="sxs-lookup"><span data-stu-id="82bf4-105">Manually Enlisting Resources</span></span>

<span data-ttu-id="82bf4-106">Les objets regroupables qui participent à des transactions doivent inscrire manuellement les ressources managées.</span><span class="sxs-lookup"><span data-stu-id="82bf4-106">Poolable objects that participate in transactions must manually enlist managed resources.</span></span> <span data-ttu-id="82bf4-107">Si un objet contient des ressources managées entre des clients, le gestionnaire de ressources n’aura aucun moyen de s’inscrire automatiquement dans une transaction lorsque l’objet est activé dans un contexte donné.</span><span class="sxs-lookup"><span data-stu-id="82bf4-107">If an object holds managed resources between clients, there will be no way for the resource manager to automatically enlist in a transaction when the object is activated in a given context.</span></span>

<span data-ttu-id="82bf4-108">L’objet lui-même doit gérer la logique de détection de la transaction, de désactivation de l’inscription automatique de Resource Manager et de l’inscription manuelle des ressources qu’il contient.</span><span class="sxs-lookup"><span data-stu-id="82bf4-108">The object itself must handle the logic of detecting the transaction, turning off the resource manager's auto-enlistment, and manually enlisting any resources that it holds.</span></span> <span data-ttu-id="82bf4-109">Les étapes de cette procédure sont spécifiques au gestionnaire de ressources que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="82bf4-109">The steps for doing this are specific to the resource manager that you are using.</span></span> <span data-ttu-id="82bf4-110">Si vous devez effectuer une inscription manuelle, consultez la documentation de votre gestionnaire de ressources.</span><span class="sxs-lookup"><span data-stu-id="82bf4-110">If you need to do manual enlistment, consult the documentation for your resource manager.</span></span>

<span data-ttu-id="82bf4-111">Comme décrit ci-dessous, les objets peuvent être regroupés avec l’affinité de transaction alors qu’une transaction est active et peuvent être activés avec l’affinité de transaction si elle est appelée par un client associé à cette transaction.</span><span class="sxs-lookup"><span data-stu-id="82bf4-111">As described below, objects can be pooled with transaction affinity while a transaction is active and can be activated with transaction affinity if called by a client associated with that transaction.</span></span> <span data-ttu-id="82bf4-112">Avant d’inscrit des ressources, vous devez d’abord vérifier l’affinité de transaction.</span><span class="sxs-lookup"><span data-stu-id="82bf4-112">Before enlisting resources, you should first check for transaction affinity.</span></span> <span data-ttu-id="82bf4-113">Si l’objet a été extrait du pool spécifique à cette transaction, il a déjà effectué un travail dans cette transaction et inscrit ses ressources.</span><span class="sxs-lookup"><span data-stu-id="82bf4-113">If the object has been taken from the pool specific to that transaction, it has already done work in that transaction and enlisted its resources.</span></span>

## <a name="turning-off-automatic-enlistment"></a><span data-ttu-id="82bf4-114">Désactivation de l’inscription automatique</span><span class="sxs-lookup"><span data-stu-id="82bf4-114">Turning Off Automatic Enlistment</span></span>

<span data-ttu-id="82bf4-115">L’inscription automatique doit être désactivée après l’acquisition de la ressource, généralement dans le constructeur de l’objet.</span><span class="sxs-lookup"><span data-stu-id="82bf4-115">Automatic enlistment should be turned off after the resource is acquired, usually in the object's constructor.</span></span> <span data-ttu-id="82bf4-116">Autrement dit, vous désactivez l’inscription automatique, puis vous vous connectez.</span><span class="sxs-lookup"><span data-stu-id="82bf4-116">That is, you disable automatic enlistment and then connect.</span></span>

<span data-ttu-id="82bf4-117">La désactivation de l’inscription automatique peut parfois être une procédure subtile, en particulier dans le cas de fournisseurs d’accès aux données en couches.</span><span class="sxs-lookup"><span data-stu-id="82bf4-117">Disabling auto-enlistment can sometimes be a subtle procedure, particularly in the case of layered data access providers.</span></span> <span data-ttu-id="82bf4-118">L’inscription automatique est parfois couplée au regroupement de connexions, comme avec ODBC, et parfois pas, comme avec OLE DB.</span><span class="sxs-lookup"><span data-stu-id="82bf4-118">Auto-enlistment is sometimes coupled with connection pooling, as with ODBC, and sometimes not, as with OLE DB.</span></span> <span data-ttu-id="82bf4-119">Vous devrez peut-être vous assurer que l’inscription automatique est désactivée à plusieurs niveaux de fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="82bf4-119">You might need to ensure that auto-enlistment is off at several levels of providers.</span></span>

## <a name="implementing-iobjectcontrol"></a><span data-ttu-id="82bf4-120">Implémentation de IObjectControl</span><span class="sxs-lookup"><span data-stu-id="82bf4-120">Implementing IObjectControl</span></span>

<span data-ttu-id="82bf4-121">Les objets regroupables qui participent à des transactions doivent surveiller l’état actuel des ressources qu’ils détiennent.</span><span class="sxs-lookup"><span data-stu-id="82bf4-121">Poolable objects that participate in transactions must monitor the current state of resources they are holding.</span></span> <span data-ttu-id="82bf4-122">Si l’objet détecte qu’il est dans un État non réutilisable (par exemple, si une connexion est incorrecte), il doit retourner false pour [**IObjectControl :: CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled).</span><span class="sxs-lookup"><span data-stu-id="82bf4-122">If the object detects that it is in a non-reusable state—for example, if a connection is bad—it should return False for [**IObjectControl::CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled).</span></span> <span data-ttu-id="82bf4-123">Cela aura pour effet d’ignorer l’instance de l’objet et de condamne la transaction en cours.</span><span class="sxs-lookup"><span data-stu-id="82bf4-123">This will have the effect of both discarding the object instance and dooming the current transaction.</span></span>

## <a name="transaction-specific-pools"></a><span data-ttu-id="82bf4-124">Pools de Transaction-Specific</span><span class="sxs-lookup"><span data-stu-id="82bf4-124">Transaction-Specific Pools</span></span>

<span data-ttu-id="82bf4-125">Un pool d’objets est généralement homogène, et tout objet mis en pool qui n’est pas en cours d’utilisation est correct pour revenir à n’importe quel client.</span><span class="sxs-lookup"><span data-stu-id="82bf4-125">A pool of objects is generally homogenous, and any pooled object not currently in use is good to return to any client.</span></span> <span data-ttu-id="82bf4-126">La seule exception à cette règle est dans le cas d’objets transactionnels, pour lesquels la mise en pool d’objets est optimisée.</span><span class="sxs-lookup"><span data-stu-id="82bf4-126">The only exception to this rule is in the case of transactional objects, for which object pooling is optimized.</span></span> <span data-ttu-id="82bf4-127">Lorsque le client qui demande un objet a une transaction associée, COM+ analyse le pool pour rechercher un objet disponible qui est déjà associé à cette transaction.</span><span class="sxs-lookup"><span data-stu-id="82bf4-127">When the client requesting an object has an associated transaction, COM+ will scan the pool for an available object that is already associated with that transaction.</span></span> <span data-ttu-id="82bf4-128">Si un objet avec l’affinité de transaction est trouvé, il est retourné au client ; dans le cas contraire, un objet du pool général est retourné.</span><span class="sxs-lookup"><span data-stu-id="82bf4-128">If an object with transaction affinity is found, it is returned to the client; otherwise, an object from the general pool is returned.</span></span>

<span data-ttu-id="82bf4-129">De cette manière, les sous-pools spéciaux sont conservés et contiennent des objets avec affinité pour une transaction particulière.</span><span class="sxs-lookup"><span data-stu-id="82bf4-129">In this manner, special subpools are maintained containing objects with affinity for a particular transaction.</span></span> <span data-ttu-id="82bf4-130">Lorsque la transaction est validée ou abandonnée, ces objets sont retournés au pool général sans affinité de transaction, prêt à être utilisé par n’importe quel client.</span><span class="sxs-lookup"><span data-stu-id="82bf4-130">When the transaction commits or aborts, these objects are returned to the general pool with no transaction affinity, ready to be used by any client.</span></span>

<span data-ttu-id="82bf4-131">Pour cette raison, lorsque votre composant inscrit manuellement ses ressources managées dans une transaction, il doit d’abord vérifier s’il est déjà inscrit.</span><span class="sxs-lookup"><span data-stu-id="82bf4-131">For this reason, when your component manually enlists its managed resources in a transaction, it should first check to see whether they are already enlisted.</span></span> <span data-ttu-id="82bf4-132">Dans ce cas, il n’est pas nécessaire d’inscrire.</span><span class="sxs-lookup"><span data-stu-id="82bf4-132">If so, there is no need to enlist.</span></span>

## <a name="related-topics"></a><span data-ttu-id="82bf4-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="82bf4-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82bf4-134">Chaînes du constructeur d’objet COM+</span><span class="sxs-lookup"><span data-stu-id="82bf4-134">COM+ Object Constructor Strings</span></span>](com--object-constructor-strings.md)
</dt> <dt>

[<span data-ttu-id="82bf4-135">Contrôle de la durée de vie et de l’état des objets</span><span class="sxs-lookup"><span data-stu-id="82bf4-135">Controlling Object Lifetime and State</span></span>](controlling-object-lifetime-and-state.md)
</dt> <dt>

[<span data-ttu-id="82bf4-136">Fonctionnement du regroupement d’objets</span><span class="sxs-lookup"><span data-stu-id="82bf4-136">How Object Pooling Works</span></span>](how-object-pooling-works.md)
</dt> <dt>

[<span data-ttu-id="82bf4-137">Amélioration des performances avec la mise en pool d’objets</span><span class="sxs-lookup"><span data-stu-id="82bf4-137">Improving Performance with Object Pooling</span></span>](improving-performance-with-object-pooling.md)
</dt> <dt>

[<span data-ttu-id="82bf4-138">Conditions requises pour les objets regroupables</span><span class="sxs-lookup"><span data-stu-id="82bf4-138">Requirements for Poolable Objects</span></span>](requirements-for-poolable-objects.md)
</dt> </dl>

 

 



