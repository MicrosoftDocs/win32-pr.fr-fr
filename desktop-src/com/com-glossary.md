---
title: Glossaire COM
description: Page de glossaire
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9e2c56a2-0572-48b6-a2ef-650f1cf1b62e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c12f3c021988f0349d9eaf6a2bdbd9505ca8a6
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "106510098"
---
# <a name="com-glossary"></a><span data-ttu-id="caf5a-103">Glossaire COM</span><span class="sxs-lookup"><span data-stu-id="caf5a-103">COM Glossary</span></span>

<dl> <dt>

<span data-ttu-id="caf5a-104"><span id="com.activation_gloss"></span><span id="COM.ACTIVATION_GLOSS"></span>**actionne**</span><span class="sxs-lookup"><span data-stu-id="caf5a-104"><span id="com.activation_gloss"></span><span id="COM.ACTIVATION_GLOSS"></span>**activation**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-105">Processus de chargement d’un objet en mémoire, qui le met à l’État en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="caf5a-105">The process of loading an object in memory, which puts it into the running state.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-106"><span id="com.active_state_gloss"></span><span id="COM.ACTIVE_STATE_GLOSS"></span>**État actif**</span><span class="sxs-lookup"><span data-stu-id="caf5a-106"><span id="com.active_state_gloss"></span><span id="COM.ACTIVE_STATE_GLOSS"></span>**active state**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-107">Objet COM qui est à l’État en cours d’exécution et qui a une interface utilisateur visible.</span><span class="sxs-lookup"><span data-stu-id="caf5a-107">A COM object that is in the running state and has a visible user interface.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-108"><span id="com.absolute_moniker_gloss"></span><span id="COM.ABSOLUTE_MONIKER_GLOSS"></span>**moniker absolu**</span><span class="sxs-lookup"><span data-stu-id="caf5a-108"><span id="com.absolute_moniker_gloss"></span><span id="COM.ABSOLUTE_MONIKER_GLOSS"></span>**absolute moniker**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-109">Moniker qui spécifie l’emplacement absolu d’un objet.</span><span class="sxs-lookup"><span data-stu-id="caf5a-109">A moniker that specifies the absolute location of an object.</span></span> <span data-ttu-id="caf5a-110">Un moniker absolu est analogue à un chemin d’accès complet.</span><span class="sxs-lookup"><span data-stu-id="caf5a-110">An absolute moniker is analogous to a full path.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-111"><span id="com.advisory_holder_gloss"></span><span id="COM.ADVISORY_HOLDER_GLOSS"></span>**détenteur de la notification**</span><span class="sxs-lookup"><span data-stu-id="caf5a-111"><span id="com.advisory_holder_gloss"></span><span id="COM.ADVISORY_HOLDER_GLOSS"></span>**advisory holder**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-112">Objet COM qui met en cache, gère et envoie des notifications de modifications aux récepteurs de notifications des applications de conteneur.</span><span class="sxs-lookup"><span data-stu-id="caf5a-112">A COM object that caches, manages, and sends notifications of changes to container applications' advisory sinks.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-113"><span id="com.advisory_sink_gloss"></span><span id="COM.ADVISORY_SINK_GLOSS"></span>**récepteur de notifications**</span><span class="sxs-lookup"><span data-stu-id="caf5a-113"><span id="com.advisory_sink_gloss"></span><span id="COM.ADVISORY_SINK_GLOSS"></span>**advisory sink**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-114">Objet COM qui peut recevoir des notifications de modifications dans un objet incorporé ou lié, car il implémente l’interface [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink) ou [**IAdviseSink2**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink2) .</span><span class="sxs-lookup"><span data-stu-id="caf5a-114">A COM object that can receive notifications of changes in an embedded object or linked object because it implements the [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink) or [**IAdviseSink2**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink2) interface.</span></span> <span data-ttu-id="caf5a-115">Les conteneurs qui doivent être avertis des modifications apportées aux objets implémentent un récepteur de notifications.</span><span class="sxs-lookup"><span data-stu-id="caf5a-115">Containers that need to be notified of changes in objects implement an advisory sink.</span></span> <span data-ttu-id="caf5a-116">Les notifications proviennent du serveur, qui utilise un objet de détenteur de notifications pour mettre en cache et gérer les notifications aux conteneurs.</span><span class="sxs-lookup"><span data-stu-id="caf5a-116">Notifications originate in the server, which uses an advisory holder object to cache and manage notifications to containers.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-117"><span id="com.aggregate_object_gloss"></span><span id="COM.AGGREGATE_OBJECT_GLOSS"></span>**Aggregate (objet)**</span><span class="sxs-lookup"><span data-stu-id="caf5a-117"><span id="com.aggregate_object_gloss"></span><span id="COM.AGGREGATE_OBJECT_GLOSS"></span>**aggregate object**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-118">Objet COM qui est constitué d’un ou de plusieurs autres objets COM.</span><span class="sxs-lookup"><span data-stu-id="caf5a-118">A COM object that is made up of one or more other COM objects.</span></span> <span data-ttu-id="caf5a-119">Un objet de l’agrégat est désigné comme l’objet de contrôle, qui contrôle les interfaces de l’agrégat qui sont exposées et qui sont privées.</span><span class="sxs-lookup"><span data-stu-id="caf5a-119">One object in the aggregate is designated the controlling object, which controls which interfaces in the aggregate are exposed and which are private.</span></span> <span data-ttu-id="caf5a-120">Cet objet de contrôle a une implémentation spéciale de [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) , appelée **IUnknown** de contrôle.</span><span class="sxs-lookup"><span data-stu-id="caf5a-120">This controlling object has a special implementation of [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) called the controlling **IUnknown**.</span></span> <span data-ttu-id="caf5a-121">Tous les objets de l’agrégat doivent passer des appels aux méthodes **IUnknown** via le contrôle **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="caf5a-121">All objects in the aggregate must pass calls to **IUnknown** methods through the controlling **IUnknown**.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-122"><span id="com.aggregation_gloss"></span><span id="COM.AGGREGATION_GLOSS"></span>**agréger**</span><span class="sxs-lookup"><span data-stu-id="caf5a-122"><span id="com.aggregation_gloss"></span><span id="COM.AGGREGATION_GLOSS"></span>**aggregation**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-123">Technique de composition pour l’implémentation d’objets COM.</span><span class="sxs-lookup"><span data-stu-id="caf5a-123">A composition technique for implementing COM objects.</span></span> <span data-ttu-id="caf5a-124">Elle vous permet de générer un nouvel objet en réutilisant une ou plusieurs implémentations d’interface d’objets existantes.</span><span class="sxs-lookup"><span data-stu-id="caf5a-124">It allows you to build a new object by reusing one or more existing objects' interface implementations.</span></span> <span data-ttu-id="caf5a-125">L’objet d’agrégation choisit les interfaces à exposer aux clients, et les interfaces sont exposées comme si elles étaient implémentées par l’objet d’agrégation.</span><span class="sxs-lookup"><span data-stu-id="caf5a-125">The aggregate object chooses which interfaces to expose to clients, and the interfaces are exposed as if they were implemented by the aggregate object.</span></span> <span data-ttu-id="caf5a-126">Les clients de l’objet d’agrégation communiquent uniquement avec l’objet d’agrégation.</span><span class="sxs-lookup"><span data-stu-id="caf5a-126">Clients of the aggregate object communicate only with the aggregate object.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-127"><span id="com.ambient_property_gloss"></span><span id="COM.AMBIENT_PROPERTY_GLOSS"></span>**propriété ambiante**</span><span class="sxs-lookup"><span data-stu-id="caf5a-127"><span id="com.ambient_property_gloss"></span><span id="COM.AMBIENT_PROPERTY_GLOSS"></span>**ambient property**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-128">Propriété au moment de l’exécution qui est gérée et exposée par le conteneur.</span><span class="sxs-lookup"><span data-stu-id="caf5a-128">A run-time property that is managed and exposed by the container.</span></span> <span data-ttu-id="caf5a-129">En règle générale, une propriété ambiante représente une caractéristique d’un formulaire, telle que la couleur d’arrière-plan, qui doit être communiquée à un contrôle afin que le contrôle puisse assumer l’apparence de son environnement environnant.</span><span class="sxs-lookup"><span data-stu-id="caf5a-129">Typically, an ambient property represents a characteristic of a form, such as background color, that needs to be communicated to a control so that the control can assume the look and feel of its surrounding environment.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-130"><span id="com.anti_moniker_gloss"></span><span id="COM.ANTI_MONIKER_GLOSS"></span>**anti-moniker**</span><span class="sxs-lookup"><span data-stu-id="caf5a-130"><span id="com.anti_moniker_gloss"></span><span id="COM.ANTI_MONIKER_GLOSS"></span>**anti-moniker**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-131">Inverse d’un moniker de fichier, d’élément ou de pointeur.</span><span class="sxs-lookup"><span data-stu-id="caf5a-131">The inverse of a file, item, or pointer moniker.</span></span> <span data-ttu-id="caf5a-132">Un anti-moniker est ajouté à la fin d’un fichier, d’un élément ou d’un moniker de pointeur pour l’annuler.</span><span class="sxs-lookup"><span data-stu-id="caf5a-132">An anti-moniker is added to the end of a file, item, or pointer moniker to nullify it.</span></span> <span data-ttu-id="caf5a-133">Les anti-monikers sont utilisés dans la construction de monikers relatifs.</span><span class="sxs-lookup"><span data-stu-id="caf5a-133">Anti-monikers are used in the construction of relative monikers.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-134"><span id="com.artificial_reference_counting_gloss"></span><span id="COM.ARTIFICIAL_REFERENCE_COUNTING_GLOSS"></span>**décompte de références artificielles**</span><span class="sxs-lookup"><span data-stu-id="caf5a-134"><span id="com.artificial_reference_counting_gloss"></span><span id="COM.ARTIFICIAL_REFERENCE_COUNTING_GLOSS"></span>**artificial reference counting**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-135">Technique utilisée pour protéger un objet avant d’appeler une fonction ou une méthode qui pourrait le détruire prématurément.</span><span class="sxs-lookup"><span data-stu-id="caf5a-135">A technique used to help protect an object before calling a function or method that could prematurely destroy it.</span></span> <span data-ttu-id="caf5a-136">Un programme appelle **IUnknown :: AddRef** pour incrémenter le décompte de références de l’objet avant d’effectuer l’appel qui pourrait libérer l’objet.</span><span class="sxs-lookup"><span data-stu-id="caf5a-136">A program calls **IUnknown::AddRef** to increment the object's reference count before making the call that could free the object.</span></span> <span data-ttu-id="caf5a-137">Une fois que la fonction a retourné une valeur, le programme appelle **IUnknown :: Release** pour décrémenter le nombre.</span><span class="sxs-lookup"><span data-stu-id="caf5a-137">After the function returns, the program calls **IUnknown::Release** to decrement the count.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-138"><span id="com.asynchronous_binding_gloss"></span><span id="COM.ASYNCHRONOUS_BINDING_GLOSS"></span>**liaison asynchrone**</span><span class="sxs-lookup"><span data-stu-id="caf5a-138"><span id="com.asynchronous_binding_gloss"></span><span id="COM.ASYNCHRONOUS_BINDING_GLOSS"></span>**asynchronous binding**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-139">Type de liaison dans laquelle il est nécessaire que le processus se produise de façon asynchrone afin d’éviter une dégradation des performances pour l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="caf5a-139">A type of binding in which it is necessary for the process to occur asynchronously to avoid performance degradation for the end user.</span></span> <span data-ttu-id="caf5a-140">En règle générale, la liaison asynchrone est utilisée dans les environnements distribués tels que le World Wide Web.</span><span class="sxs-lookup"><span data-stu-id="caf5a-140">Typically, asynchronous binding is used in distributed environments such as the World Wide Web.</span></span> <span data-ttu-id="caf5a-141">OLE prend en charge les classes de moniker asynchrones et les mécanismes de rappel qui permettent au processus de localisation et d’initialisation d’un objet dans un environnement distribué de se produire pendant l’exécution d’autres opérations.</span><span class="sxs-lookup"><span data-stu-id="caf5a-141">OLE supports asynchronous moniker classes and callback mechanisms that allow the process of locating and initializing an object in a distributed environment to occur while other operations are being carried out.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-142"><span id="com.asynchronous_call_gloss"></span><span id="COM.ASYNCHRONOUS_CALL_GLOSS"></span>**appel asynchrone**</span><span class="sxs-lookup"><span data-stu-id="caf5a-142"><span id="com.asynchronous_call_gloss"></span><span id="COM.ASYNCHRONOUS_CALL_GLOSS"></span>**asynchronous call**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-143">Appel à une fonction exécutée séparément afin que l’appelant puisse continuer à traiter les instructions sans attendre le retour de la fonction.</span><span class="sxs-lookup"><span data-stu-id="caf5a-143">A call to a function that is executed separately so that the caller can continue processing instructions without waiting for the function to return.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-144"><span id="com.asynchronous_moniker_gloss"></span><span id="COM.ASYNCHRONOUS_MONIKER_GLOSS"></span>**moniker asynchrone**</span><span class="sxs-lookup"><span data-stu-id="caf5a-144"><span id="com.asynchronous_moniker_gloss"></span><span id="COM.ASYNCHRONOUS_MONIKER_GLOSS"></span>**asynchronous moniker**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-145">Moniker qui prend en charge la liaison asynchrone.</span><span class="sxs-lookup"><span data-stu-id="caf5a-145">A moniker that supports asynchronous binding.</span></span> <span data-ttu-id="caf5a-146">Par exemple, les instances de la classe moniker d’URL fournie par le système sont des monikers asynchrones.</span><span class="sxs-lookup"><span data-stu-id="caf5a-146">For example, instances of the system-supplied URL moniker class are asynchronous monikers.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-147"><span id="com.automation_gloss"></span><span id="COM.AUTOMATION_GLOSS"></span>**mati**</span><span class="sxs-lookup"><span data-stu-id="caf5a-147"><span id="com.automation_gloss"></span><span id="COM.AUTOMATION_GLOSS"></span>**automation**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-148">Moyen de manipuler les objets d’une application à partir de l’extérieur de l’application.</span><span class="sxs-lookup"><span data-stu-id="caf5a-148">A way to manipulate an application's objects from outside the application.</span></span> <span data-ttu-id="caf5a-149">Automation est généralement utilisé pour créer des applications qui exposent des objets à des outils de programmation et des langages de macro, pour créer et manipuler des objets d’une application à partir d’autres applications, ou pour créer des outils permettant d’accéder aux objets et de les manipuler.</span><span class="sxs-lookup"><span data-stu-id="caf5a-149">Automation is typically used to create applications that expose objects to programming tools and macro languages, create and manipulate one application's objects from another applications, or to create tools for accessing and manipulating objects.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-150"><span id="com.bind_context_gloss"></span><span id="COM.BIND_CONTEXT_GLOSS"></span>**contexte de liaison**</span><span class="sxs-lookup"><span data-stu-id="caf5a-150"><span id="com.bind_context_gloss"></span><span id="COM.BIND_CONTEXT_GLOSS"></span>**bind context**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-151">Objet COM qui implémente l’interface [**IBindCtx**](/windows/desktop/api/ObjIdl/nn-objidl-ibindctx) .</span><span class="sxs-lookup"><span data-stu-id="caf5a-151">A COM object that implements the [**IBindCtx**](/windows/desktop/api/ObjIdl/nn-objidl-ibindctx) interface.</span></span> <span data-ttu-id="caf5a-152">Les contextes de liaison sont utilisés dans les opérations de moniker pour contenir des références aux objets activés lorsqu’un moniker est lié.</span><span class="sxs-lookup"><span data-stu-id="caf5a-152">Bind contexts are used in moniker operations to hold references to the objects activated when a moniker is bound.</span></span> <span data-ttu-id="caf5a-153">Le contexte de liaison contient des paramètres qui s’appliquent à toutes les opérations pendant la liaison d’un moniker composite générique et fournit l’implémentation du moniker avec un accès aux informations sur son environnement.</span><span class="sxs-lookup"><span data-stu-id="caf5a-153">The bind context contains parameters that apply to all operations during the binding of a generic composite moniker and provides the moniker implementation with access to information about its environment.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-154"><span id="com.binding_gloss"></span><span id="COM.BINDING_GLOSS"></span>**liant**</span><span class="sxs-lookup"><span data-stu-id="caf5a-154"><span id="com.binding_gloss"></span><span id="COM.BINDING_GLOSS"></span>**binding**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-155">Association d’un nom à son référent.</span><span class="sxs-lookup"><span data-stu-id="caf5a-155">Associating a name with its referent.</span></span> <span data-ttu-id="caf5a-156">En particulier, en localisant l’objet nommé par un moniker, en le plaçant dans son état d’exécution s’il n’est pas déjà, et en retournant un pointeur d’interface vers celui-ci.</span><span class="sxs-lookup"><span data-stu-id="caf5a-156">Specifically, locating the object named by a moniker, putting it into its running state if it isn't already, and returning an interface pointer to it.</span></span> <span data-ttu-id="caf5a-157">Les objets peuvent être liés au moment de l’exécution (également appelé liaison tardive ou liaison dynamique) ou au moment de la compilation (également appelé liaison statique).</span><span class="sxs-lookup"><span data-stu-id="caf5a-157">Objects can be bound at run time (also called late binding or dynamic binding) or at compile time (also called static binding).</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-158"><span id="com.cache_gloss"></span><span id="COM.CACHE_GLOSS"></span>**en**</span><span class="sxs-lookup"><span data-stu-id="caf5a-158"><span id="com.cache_gloss"></span><span id="COM.CACHE_GLOSS"></span>**cache**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-159">Magasin d’informations local (généralement temporaire).</span><span class="sxs-lookup"><span data-stu-id="caf5a-159">A (usually temporary) local store of information.</span></span> <span data-ttu-id="caf5a-160">Dans OLE, un cache contient des informations qui définissent la présentation d’un objet lié ou incorporé lorsque le conteneur est ouvert.</span><span class="sxs-lookup"><span data-stu-id="caf5a-160">In OLE, a cache contains information that defines the presentation of a linked or embedded object when the container is opened.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-161"><span id="com.cache_initialization_gloss"></span><span id="COM.CACHE_INITIALIZATION_GLOSS"></span>**initialisation du cache**</span><span class="sxs-lookup"><span data-stu-id="caf5a-161"><span id="com.cache_initialization_gloss"></span><span id="COM.CACHE_INITIALIZATION_GLOSS"></span>**cache initialization**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-162">Remplissage du cache d’un objet lié ou incorporé avec les données de présentation.</span><span class="sxs-lookup"><span data-stu-id="caf5a-162">Filling a linked or embedded object's cache with presentation data.</span></span> <span data-ttu-id="caf5a-163">L’interface [**IOleCache**](/windows/desktop/api/OleIdl/nn-oleidl-iolecache) fournit des méthodes qu’un conteneur peut appeler pour contrôler les données mises en cache pour les objets liés ou incorporés.</span><span class="sxs-lookup"><span data-stu-id="caf5a-163">The [**IOleCache**](/windows/desktop/api/OleIdl/nn-oleidl-iolecache) interface provides methods that a container can call to control the data that gets cached for linked or embedded objects.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-164"><span id="com.class_gloss"></span><span id="COM.CLASS_GLOSS"></span>**type**</span><span class="sxs-lookup"><span data-stu-id="caf5a-164"><span id="com.class_gloss"></span><span id="COM.CLASS_GLOSS"></span>**class**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-165">Définition d’un objet dans le code.</span><span class="sxs-lookup"><span data-stu-id="caf5a-165">The definition of an object in code.</span></span> <span data-ttu-id="caf5a-166">En C++, la classe d’un objet est définie comme un type de données, mais ce n’est pas le cas dans d’autres langages.</span><span class="sxs-lookup"><span data-stu-id="caf5a-166">In C++, the class of an object is defined as a data type, but this is not the case in other languages.</span></span> <span data-ttu-id="caf5a-167">Étant donné que OLE peut être codé dans n’importe quel langage, la classe est utilisée pour faire référence à la définition générale de l’objet.</span><span class="sxs-lookup"><span data-stu-id="caf5a-167">Because OLE can be coded in any language, class is used to refer to the general object definition.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-168"><span id="com.class_factory_gloss"></span><span id="COM.CLASS_FACTORY_GLOSS"></span>**fabrique de classes**</span><span class="sxs-lookup"><span data-stu-id="caf5a-168"><span id="com.class_factory_gloss"></span><span id="COM.CLASS_FACTORY_GLOSS"></span>**class factory**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-169">Objet COM qui implémente l’interface [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) et qui crée une ou plusieurs instances d’un objet identifié par un identificateur de classe (CLSID) donné.</span><span class="sxs-lookup"><span data-stu-id="caf5a-169">A COM object that implements the [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) interface and that creates one or more instances of an object identified by a given class identifier(CLSID).</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-170"><span id="com.class_identifier_gloss"></span><span id="COM.CLASS_IDENTIFIER_GLOSS"></span>**identificateur de classe (CLSID)**</span><span class="sxs-lookup"><span data-stu-id="caf5a-170"><span id="com.class_identifier_gloss"></span><span id="COM.CLASS_IDENTIFIER_GLOSS"></span>**class identifier (CLSID)**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-171">Identificateur global unique (GUID) associé à un objet de classe OLE.</span><span class="sxs-lookup"><span data-stu-id="caf5a-171">A globally unique identifier (GUID) associated with an OLE class object.</span></span> <span data-ttu-id="caf5a-172">Si un objet de classe sera utilisé pour créer plusieurs instances d’un objet, l’application serveur associée doit inscrire son CLSID dans le registre système afin que les clients puissent localiser et charger le code exécutable associé aux objets.</span><span class="sxs-lookup"><span data-stu-id="caf5a-172">If a class object will be used to create more than one instance of an object, the associated server application should register its CLSID in the system registry so that clients can locate and load the executable code associated with the object(s).</span></span> <span data-ttu-id="caf5a-173">Chaque serveur ou conteneur OLE qui autorise la liaison à ses objets incorporés doit inscrire un CLSID pour chaque définition d’objet prise en charge.</span><span class="sxs-lookup"><span data-stu-id="caf5a-173">Every OLE server or container that allows linking to its embedded objects must register a CLSID for each supported object definition.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-174"><span id="com.class_object_gloss"></span><span id="COM.CLASS_OBJECT_GLOSS"></span>**objet de classe**</span><span class="sxs-lookup"><span data-stu-id="caf5a-174"><span id="com.class_object_gloss"></span><span id="COM.CLASS_OBJECT_GLOSS"></span>**class object**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-175">Dans la programmation orientée objet, objet dont l’État est partagé par tous les objets d’une classe et dont le comportement agit sur ces données d’État classwide.</span><span class="sxs-lookup"><span data-stu-id="caf5a-175">In object-oriented programming, an object whose state is shared by all the objects in a class and whose behavior acts on that classwide state data.</span></span> <span data-ttu-id="caf5a-176">Dans COM, les objets de classe sont appelés fabriques de classes et n’ont généralement aucun comportement à l’exception de la création de nouvelles instances de la classe.</span><span class="sxs-lookup"><span data-stu-id="caf5a-176">In COM, class objects are called class factories, and typically have no behavior except to create new instances of the class.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-177"><span id="com.client_gloss"></span><span id="COM.CLIENT_GLOSS"></span>**client**</span><span class="sxs-lookup"><span data-stu-id="caf5a-177"><span id="com.client_gloss"></span><span id="COM.CLIENT_GLOSS"></span>**client**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-178">Objet COM qui demande des services à partir d’un autre objet.</span><span class="sxs-lookup"><span data-stu-id="caf5a-178">A COM object that requests services from another object.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-179"><span id="com.client_site_gloss"></span><span id="COM.CLIENT_SITE_GLOSS"></span>**site client**</span><span class="sxs-lookup"><span data-stu-id="caf5a-179"><span id="com.client_site_gloss"></span><span id="COM.CLIENT_SITE_GLOSS"></span>**client site**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-180">Site d’affichage d’un objet incorporé ou lié dans un document composé.</span><span class="sxs-lookup"><span data-stu-id="caf5a-180">The display site for an embedded or linked object within a compound document.</span></span> <span data-ttu-id="caf5a-181">Le site client est le principal moyen par lequel un objet demande des services à partir de son conteneur.</span><span class="sxs-lookup"><span data-stu-id="caf5a-181">The client site is the principal means by which an object requests services from its container.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-182"><span id="com.clsid_gloss"></span><span id="COM.CLSID_GLOSS"></span>**IDENTIFICATEUR**</span><span class="sxs-lookup"><span data-stu-id="caf5a-182"><span id="com.clsid_gloss"></span><span id="COM.CLSID_GLOSS"></span>**CLSID**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-183">Identificateur global unique (GUID) associé à un objet de classe OLE.</span><span class="sxs-lookup"><span data-stu-id="caf5a-183">A globally unique identifier (GUID) associated with an OLE class object.</span></span> <span data-ttu-id="caf5a-184">Si un objet de classe sera utilisé pour créer plusieurs instances d’un objet, l’application serveur associée doit inscrire son CLSID dans le registre système afin que les clients puissent localiser et charger le code exécutable associé aux objets.</span><span class="sxs-lookup"><span data-stu-id="caf5a-184">If a class object will be used to create more than one instance of an object, the associated server application should register its CLSID in the system registry so that clients can locate and load the executable code associated with the object(s).</span></span> <span data-ttu-id="caf5a-185">Chaque serveur ou conteneur OLE qui autorise la liaison à ses objets incorporés doit inscrire un CLSID pour chaque définition d’objet prise en charge.</span><span class="sxs-lookup"><span data-stu-id="caf5a-185">Every OLE server or container that allows linking to its embedded objects must register a CLSID for each supported object definition.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-186"><span id="com.commit_gloss"></span><span id="COM.COMMIT_GLOSS"></span>**valider**</span><span class="sxs-lookup"><span data-stu-id="caf5a-186"><span id="com.commit_gloss"></span><span id="COM.COMMIT_GLOSS"></span>**commit**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-187">Pour enregistrer de façon permanente toute modification apportée à un objet de stockage ou de flux depuis son ouverture ou lors du dernier enregistrement des modifications.</span><span class="sxs-lookup"><span data-stu-id="caf5a-187">To persistently save any changes made to a storage or stream object since it was opened or changes were last saved.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-188"><span id="com.component_gloss"></span><span id="COM.COMPONENT_GLOSS"></span>**-**</span><span class="sxs-lookup"><span data-stu-id="caf5a-188"><span id="com.component_gloss"></span><span id="COM.COMPONENT_GLOSS"></span>**component**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-189">Objet qui encapsule les données et le code, et fournit un ensemble bien spécifié de services disponibles publiquement.</span><span class="sxs-lookup"><span data-stu-id="caf5a-189">An object that encapsulates both data and code, and provides a well-specified set of publicly available services.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-190"><span id="com.component_object_model_gloss"></span><span id="COM.COMPONENT_OBJECT_MODEL_GLOSS"></span>**COM (Component Object Model)**</span><span class="sxs-lookup"><span data-stu-id="caf5a-190"><span id="com.component_object_model_gloss"></span><span id="COM.COMPONENT_OBJECT_MODEL_GLOSS"></span>**Component Object Model (COM)**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-191">Le modèle de programmation orienté objet OLE qui définit la façon dont les objets interagissent au sein d’un même processus ou entre des processus.</span><span class="sxs-lookup"><span data-stu-id="caf5a-191">The OLE object-oriented programming model that defines how objects interact within a single process or between processes.</span></span> <span data-ttu-id="caf5a-192">Dans COM, les clients ont accès à un objet via des interfaces implémentées sur l’objet.</span><span class="sxs-lookup"><span data-stu-id="caf5a-192">In COM, clients have access to an object through interfaces implemented on the object.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-193"><span id="com.composite_menu_bar_gloss"></span><span id="COM.COMPOSITE_MENU_BAR_GLOSS"></span>**barre de menus composite**</span><span class="sxs-lookup"><span data-stu-id="caf5a-193"><span id="com.composite_menu_bar_gloss"></span><span id="COM.COMPOSITE_MENU_BAR_GLOSS"></span>**composite menu bar**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-194">Barre de menus partagée composée de groupes de menus issus d’une application de conteneur et d’une application serveur activée sur place.</span><span class="sxs-lookup"><span data-stu-id="caf5a-194">A shared menu bar composed of menu groups from both a container application and an in-place-activated server application.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-195"><span id="com.composite_moniker_gloss"></span><span id="COM.COMPOSITE_MONIKER_GLOSS"></span>**moniker composite**</span><span class="sxs-lookup"><span data-stu-id="caf5a-195"><span id="com.composite_moniker_gloss"></span><span id="COM.COMPOSITE_MONIKER_GLOSS"></span>**composite moniker**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-196">Moniker qui se compose de deux monikers ou plus qui sont traités comme une unité.</span><span class="sxs-lookup"><span data-stu-id="caf5a-196">A moniker that consists of two or more monikers that are treated as a unit.</span></span> <span data-ttu-id="caf5a-197">Un moniker composite peut être non générique, ce qui signifie que ses monikers de composants ont une connaissance particulière de l’un l’autre, ou générique, ce qui signifie que ses monikers de composants ne savent rien de l’autre, sauf qu’il s’agit de monikers</span><span class="sxs-lookup"><span data-stu-id="caf5a-197">A composite moniker can be non-generic, meaning that its component monikers have special knowledge of each other, or generic, meaning that its component monikers know nothing about each other except that they are monikers</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-198"><span id="com.compound_document_gloss"></span><span id="COM.COMPOUND_DOCUMENT_GLOSS"></span>**document composé**</span><span class="sxs-lookup"><span data-stu-id="caf5a-198"><span id="com.compound_document_gloss"></span><span id="COM.COMPOUND_DOCUMENT_GLOSS"></span>**compound document**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-199">Document qui comprend des objets liés ou incorporés, ainsi que ses propres données natives.</span><span class="sxs-lookup"><span data-stu-id="caf5a-199">A document that includes linked or embedded objects, as well as its own native data.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-200"><span id="com.compound_file_gloss"></span><span id="COM.COMPOUND_FILE_GLOSS"></span>**fichier composé**</span><span class="sxs-lookup"><span data-stu-id="caf5a-200"><span id="com.compound_file_gloss"></span><span id="COM.COMPOUND_FILE_GLOSS"></span>**compound file**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-201">Implémentation de stockage structuré fournie par OLE.</span><span class="sxs-lookup"><span data-stu-id="caf5a-201">An OLE-provided Structured Storage implementation.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-202"><span id="com.com_object_gloss"></span><span id="COM.COM_OBJECT_GLOSS"></span>**Objet COM**</span><span class="sxs-lookup"><span data-stu-id="caf5a-202"><span id="com.com_object_gloss"></span><span id="COM.COM_OBJECT_GLOSS"></span>**COM object**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-203">Objet qui est conforme au modèle COM (Component Object Model) OLE.</span><span class="sxs-lookup"><span data-stu-id="caf5a-203">An object that conforms to the OLE Component Object Model (COM).</span></span> <span data-ttu-id="caf5a-204">Un objet COM est une instance d’une définition d’objet, qui spécifie les données de l’objet et une ou plusieurs implémentations d’interfaces sur l’objet.</span><span class="sxs-lookup"><span data-stu-id="caf5a-204">A COM object is an instance of an object definition, which specifies the object's data and one or more implementations of interfaces on the object.</span></span> <span data-ttu-id="caf5a-205">Les clients interagissent avec un objet COM uniquement par le biais de ses interfaces.</span><span class="sxs-lookup"><span data-stu-id="caf5a-205">Clients interact with a COM object only through its interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-206"><span id="com.connectable_object_gloss"></span><span id="COM.CONNECTABLE_OBJECT_GLOSS"></span>**objet connectable**</span><span class="sxs-lookup"><span data-stu-id="caf5a-206"><span id="com.connectable_object_gloss"></span><span id="COM.CONNECTABLE_OBJECT_GLOSS"></span>**connectable object**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-207">Objet COM qui implémente, au minimum, l’interface [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) , pour la gestion des objets de point de connexion.</span><span class="sxs-lookup"><span data-stu-id="caf5a-207">A COM object that implements, at a minimum, the [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) interface, for the management of connection point objects.</span></span> <span data-ttu-id="caf5a-208">Les objets connectables prennent en charge la communication entre le serveur et le client.</span><span class="sxs-lookup"><span data-stu-id="caf5a-208">Connectable objects support communication from the server to the client.</span></span> <span data-ttu-id="caf5a-209">Un objet connectable crée et gère un ou plusieurs sous-objets de point de connexion qui reçoivent des événements des interfaces implémentées sur d’autres objets et les envoient au client.</span><span class="sxs-lookup"><span data-stu-id="caf5a-209">A connectable object creates and manages one or more connection point subobjects, which receive events from interfaces implemented on other objects and send them on to the client.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-210"><span id="com.connection_point_object_gloss"></span><span id="COM.CONNECTION_POINT_OBJECT_GLOSS"></span>**objet point de connexion**</span><span class="sxs-lookup"><span data-stu-id="caf5a-210"><span id="com.connection_point_object_gloss"></span><span id="COM.CONNECTION_POINT_OBJECT_GLOSS"></span>**connection point object**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-211">Objet COM géré par un objet connectable et qui implémente l’interface [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) .</span><span class="sxs-lookup"><span data-stu-id="caf5a-211">A COM object that is managed by a connectable object and that implements the [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) interface.</span></span> <span data-ttu-id="caf5a-212">Un ou plusieurs objets point de connexion peuvent être créés et gérés par un objet connectable.</span><span class="sxs-lookup"><span data-stu-id="caf5a-212">One or more connection point objects can be created and managed by a connectable object.</span></span> <span data-ttu-id="caf5a-213">Chaque objet de point de connexion gère les événements entrants à partir d’une interface spécifique sur un autre objet et envoie ces événements au client.</span><span class="sxs-lookup"><span data-stu-id="caf5a-213">Each connection point object manages incoming events from a specific interface on another object and sends those events on to the client.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-214"><span id="com.container_application_gloss"></span><span id="COM.CONTAINER_APPLICATION_GLOSS"></span>**application de conteneur**</span><span class="sxs-lookup"><span data-stu-id="caf5a-214"><span id="com.container_application_gloss"></span><span id="COM.CONTAINER_APPLICATION_GLOSS"></span>**container application**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-215">Application qui prend en charge les documents composés.</span><span class="sxs-lookup"><span data-stu-id="caf5a-215">An application that supports compound documents.</span></span> <span data-ttu-id="caf5a-216">L’application de conteneur fournit un stockage pour un objet incorporé ou lié, un site pour son affichage, un accès au site d’affichage et un récepteur de notifications pour recevoir des notifications de modifications de l’objet.</span><span class="sxs-lookup"><span data-stu-id="caf5a-216">The container application provides storage for an embedded or linked object, a site for its display, access to the display site, and an advisory sink for receiving notifications of changes in the object.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-217"><span id="com.containment_gloss"></span><span id="COM.CONTAINMENT_GLOSS"></span>**imbrication**</span><span class="sxs-lookup"><span data-stu-id="caf5a-217"><span id="com.containment_gloss"></span><span id="COM.CONTAINMENT_GLOSS"></span>**containment**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-218">Technique de composition pour l’implémentation d’objets COM.</span><span class="sxs-lookup"><span data-stu-id="caf5a-218">A composition technique for implementing COM objects.</span></span> <span data-ttu-id="caf5a-219">Il permet à un objet de réutiliser une partie ou la totalité des implémentations d’interface d’un ou plusieurs autres objets.</span><span class="sxs-lookup"><span data-stu-id="caf5a-219">It allows one object to reuse some or all of the interface implementations of one or more other objects.</span></span> <span data-ttu-id="caf5a-220">L’objet externe agit comme un client pour les autres objets, en déléguant l’implémentation lorsqu’il souhaite utiliser les services de l’un des objets contenus.</span><span class="sxs-lookup"><span data-stu-id="caf5a-220">The outer object acts as a client to the other objects, delegating implementation when it wishes to use the services of one of the contained objects.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-221"><span id="com.context_gloss"></span><span id="COM.CONTEXT_GLOSS"></span>**contexte**</span><span class="sxs-lookup"><span data-stu-id="caf5a-221"><span id="com.context_gloss"></span><span id="COM.CONTEXT_GLOSS"></span>**context**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-222">Dans COM+, ensemble de propriétés d’exécution associées à un ou plusieurs objets COM utilisés pour fournir des services pour ces objets.</span><span class="sxs-lookup"><span data-stu-id="caf5a-222">In COM+, a set of run-time properties associated with one or more COM objects that are used to provide services for those objects.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-223"><span id="com.control_gloss"></span><span id="COM.CONTROL_GLOSS"></span>**régulation**</span><span class="sxs-lookup"><span data-stu-id="caf5a-223"><span id="com.control_gloss"></span><span id="COM.CONTROL_GLOSS"></span>**control**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-224">Objet COM incorporable et réutilisable qui prend en charge, au minimum, l’interface [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) .</span><span class="sxs-lookup"><span data-stu-id="caf5a-224">An embeddable, reusable COM object that supports, at a minimum, the [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) interface.</span></span> <span data-ttu-id="caf5a-225">Les contrôles sont généralement associés à l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="caf5a-225">Controls are typically associated with the user interface.</span></span> <span data-ttu-id="caf5a-226">Elles prennent également en charge la communication avec un conteneur et peuvent être réutilisées par plusieurs clients, en fonction des critères de licence.</span><span class="sxs-lookup"><span data-stu-id="caf5a-226">They also support communication with a container and can be reused by multiple clients, depending upon licensing criteria.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-227"><span id="com.control_container_gloss"></span><span id="COM.CONTROL_CONTAINER_GLOSS"></span>**conteneur de contrôle**</span><span class="sxs-lookup"><span data-stu-id="caf5a-227"><span id="com.control_container_gloss"></span><span id="COM.CONTROL_CONTAINER_GLOSS"></span>**control container**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-228">Application qui prend en charge l’incorporation de contrôles en implémentant l’interface [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) .</span><span class="sxs-lookup"><span data-stu-id="caf5a-228">An application that supports embedding of controls by implementing the [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) interface.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-229"><span id="com.control_property_gloss"></span><span id="COM.CONTROL_PROPERTY_GLOSS"></span>**Control, propriété**</span><span class="sxs-lookup"><span data-stu-id="caf5a-229"><span id="com.control_property_gloss"></span><span id="COM.CONTROL_PROPERTY_GLOSS"></span>**control property**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-230">Propriété au moment de l’exécution qui est exposée et gérée par le contrôle lui-même.</span><span class="sxs-lookup"><span data-stu-id="caf5a-230">A run-time property that is exposed and managed by the control itself.</span></span> <span data-ttu-id="caf5a-231">Par exemple, la taille de police et de texte utilisée par le contrôle sont des propriétés de contrôle.</span><span class="sxs-lookup"><span data-stu-id="caf5a-231">For example, the font and text size used by the control are control properties.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-232"><span id="com.controlling_object_gloss"></span><span id="COM.CONTROLLING_OBJECT_GLOSS"></span>**contrôle de l’objet**</span><span class="sxs-lookup"><span data-stu-id="caf5a-232"><span id="com.controlling_object_gloss"></span><span id="COM.CONTROLLING_OBJECT_GLOSS"></span>**controlling object**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-233">Objet dans un objet d’agrégation qui contrôle les interfaces de l’objet d’agrégation qui sont exposées et qui sont privées.</span><span class="sxs-lookup"><span data-stu-id="caf5a-233">The object within an aggregate object that controls which interfaces within the aggregate object are exposed and which are private.</span></span> <span data-ttu-id="caf5a-234">L’interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) de l’objet de contrôle est appelée **IUnknown** de contrôle.</span><span class="sxs-lookup"><span data-stu-id="caf5a-234">The [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface of the controlling object is called the controlling **IUnknown**.</span></span> <span data-ttu-id="caf5a-235">Les appels aux méthodes **IUnknown** des autres objets de l’agrégat doivent être passés au contrôle **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="caf5a-235">Calls to **IUnknown** methods of other objects in the aggregate must be passed to the controlling **IUnknown**.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-236"><span id="com.control_site_gloss"></span><span id="COM.CONTROL_SITE_GLOSS"></span>**site de contrôle**</span><span class="sxs-lookup"><span data-stu-id="caf5a-236"><span id="com.control_site_gloss"></span><span id="COM.CONTROL_SITE_GLOSS"></span>**control site**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-237">Structure implémentée par un conteneur de contrôle pour gérer l’affichage et le stockage d’un contrôle.</span><span class="sxs-lookup"><span data-stu-id="caf5a-237">A structure implemented by a control container for managing the display and storage of a control.</span></span> <span data-ttu-id="caf5a-238">Dans un conteneur donné, chaque contrôle dispose d’un site de contrôle correspondant.</span><span class="sxs-lookup"><span data-stu-id="caf5a-238">Within a given container, each control has a corresponding control site.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-239"><span id="com.data_transfer_object_gloss"></span><span id="COM.DATA_TRANSFER_OBJECT_GLOSS"></span>**objet de transfert de données**</span><span class="sxs-lookup"><span data-stu-id="caf5a-239"><span id="com.data_transfer_object_gloss"></span><span id="COM.DATA_TRANSFER_OBJECT_GLOSS"></span>**data transfer object**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-240">Objet qui implémente l’interface [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) et contient les données à transférer d’un objet à un autre par le biais du presse-papiers ou des opérations de glisser-déplacer.</span><span class="sxs-lookup"><span data-stu-id="caf5a-240">An object that implements the [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) interface and contains data to be transferred from one object to another through either the Clipboard or drag-and-drop operations.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-241"><span id="com.default_object_handler_gloss"></span><span id="COM.DEFAULT_OBJECT_HANDLER_GLOSS"></span>**gestionnaire d’objets par défaut**</span><span class="sxs-lookup"><span data-stu-id="caf5a-241"><span id="com.default_object_handler_gloss"></span><span id="COM.DEFAULT_OBJECT_HANDLER_GLOSS"></span>**default object handler**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-242">DLL fournie avec OLE qui agit comme un substitut dans l’espace de traitement de l’application conteneur pour l’objet réel.</span><span class="sxs-lookup"><span data-stu-id="caf5a-242">A DLL provided with OLE that acts as a surrogate in the processing space of the container application for the real object.</span></span>

<span data-ttu-id="caf5a-243">Avec le gestionnaire d’objets par défaut, il est possible d’examiner les données stockées d’un objet sans réellement activer l’objet.</span><span class="sxs-lookup"><span data-stu-id="caf5a-243">With the default object handler, it is possible to look at an object's stored data without actually activating the object.</span></span> <span data-ttu-id="caf5a-244">Le gestionnaire d’objets par défaut effectue d’autres tâches, telles que le rendu d’un objet à partir de son état mis en cache lorsque l’objet est chargé en mémoire.</span><span class="sxs-lookup"><span data-stu-id="caf5a-244">The default object handler performs other tasks, such as rendering an object from its cached state when the object is loaded into memory.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-245"><span id="com.dependent_object_gloss"></span><span id="COM.DEPENDENT_OBJECT_GLOSS"></span>**objet dépendant**</span><span class="sxs-lookup"><span data-stu-id="caf5a-245"><span id="com.dependent_object_gloss"></span><span id="COM.DEPENDENT_OBJECT_GLOSS"></span>**dependent object**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-246">Objet COM qui est généralement initialisé par un autre objet (l’objet hôte).</span><span class="sxs-lookup"><span data-stu-id="caf5a-246">A COM object that is typically initialized by another object (the host object).</span></span> <span data-ttu-id="caf5a-247">Bien que la durée de vie des objets dépendants ne soit utile que pendant la durée de vie de l’objet hôte, l’objet hôte ne fonctionne pas comme le contrôle [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) pour l’objet dépendant.</span><span class="sxs-lookup"><span data-stu-id="caf5a-247">Although the dependent object's lifetime may only make sense during the lifetime of the host object, the host object does not function as the controlling [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) for the dependent object.</span></span> <span data-ttu-id="caf5a-248">En revanche, un objet est un objet agrégé lorsque sa durée de vie (au moyen de son décompte de références) est complètement contrôlé par l’objet de gestion.</span><span class="sxs-lookup"><span data-stu-id="caf5a-248">In contrast, an object is an aggregated object when its lifetime (by means of its reference count) is completely controlled by the managing object.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-249"><span id="com.direct_access_mode_gloss"></span><span id="COM.DIRECT_ACCESS_MODE_GLOSS"></span>**mode d’accès direct**</span><span class="sxs-lookup"><span data-stu-id="caf5a-249"><span id="com.direct_access_mode_gloss"></span><span id="COM.DIRECT_ACCESS_MODE_GLOSS"></span>**direct access mode**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-250">Un des deux modes d’accès dans lesquels un objet de stockage peut être ouvert.</span><span class="sxs-lookup"><span data-stu-id="caf5a-250">One of two access modes in which a storage object can be opened.</span></span> <span data-ttu-id="caf5a-251">En mode direct, toutes les modifications sont immédiatement validées sur l’objet de stockage racine.</span><span class="sxs-lookup"><span data-stu-id="caf5a-251">In direct mode, all changes are immediately committed to the root storage object.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-252"><span id="com.document_object_gloss"></span><span id="COM.DOCUMENT_OBJECT_GLOSS"></span>**objet document**</span><span class="sxs-lookup"><span data-stu-id="caf5a-252"><span id="com.document_object_gloss"></span><span id="COM.DOCUMENT_OBJECT_GLOSS"></span>**document object**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-253">Document OLE qui peut afficher une ou plusieurs vues activées sur place de ses données dans un frame natif ou étranger, tel qu’un navigateur, tout en conservant le contrôle total sur son interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="caf5a-253">An OLE document that can display one or more in-place activated views of its data within a native or foreign frame, such as a browser, while retaining full control over its user interface.</span></span> <span data-ttu-id="caf5a-254">Outre l’implémentation du document OLE habituel et des interfaces d’activation sur place, un objet document doit implémenter [**IOleDocument**](/windows/desktop/api/DocObj/nn-docobj-ioledocument), et chacune de ses vues (sous la forme d’un objet de vue de document) doit implémenter [**IOleDocumentView**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentview).</span><span class="sxs-lookup"><span data-stu-id="caf5a-254">In addition to implementing the usual OLE document and in-place activation interfaces, a document object must implement [**IOleDocument**](/windows/desktop/api/DocObj/nn-docobj-ioledocument), and each of its views (in the form of a document view object) must implement [**IOleDocumentView**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentview).</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-255"><span id="com.document_object_container_gloss"></span><span id="COM.DOCUMENT_OBJECT_CONTAINER_GLOSS"></span>**conteneur d’objets de document**</span><span class="sxs-lookup"><span data-stu-id="caf5a-255"><span id="com.document_object_container_gloss"></span><span id="COM.DOCUMENT_OBJECT_CONTAINER_GLOSS"></span>**document object container**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-256">Application conteneur qui permet d’afficher une ou plusieurs vues d’un ou plusieurs objets document et de gérer tous les objets de document contenus dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="caf5a-256">A container application capable of displaying one or more views of one or more document objects and of managing all contained document objects within a file.</span></span> <span data-ttu-id="caf5a-257">Chaque objet de document est associé à un site de document, et chaque site de document contient un ou plusieurs sites d’affichage de documents correspondant aux vues prises en charge par l’objet de document.</span><span class="sxs-lookup"><span data-stu-id="caf5a-257">Each document object is associated with a document site, and each document site contains one or more document view sites corresponding to the views supported by the document object.</span></span> <span data-ttu-id="caf5a-258">Un conteneur d’objets de document comprend également un frame de conteneur, qui gère la négociation des menus et des barres d’outils, ainsi que l’énumération des objets contenus.</span><span class="sxs-lookup"><span data-stu-id="caf5a-258">A document object container also includes a container frame, which handles menu and toolbar negotiation and the enumeration of contained objects.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-259"><span id="com.document_object_server_gloss"></span><span id="COM.DOCUMENT_OBJECT_SERVER_GLOSS"></span>**serveur d’objets de document**</span><span class="sxs-lookup"><span data-stu-id="caf5a-259"><span id="com.document_object_server_gloss"></span><span id="COM.DOCUMENT_OBJECT_SERVER_GLOSS"></span>**document object server**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-260">Application serveur qui permet de fournir des objets de document.</span><span class="sxs-lookup"><span data-stu-id="caf5a-260">A server application capable of providing document objects.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-261"><span id="com.document_site_gloss"></span><span id="COM.DOCUMENT_SITE_GLOSS"></span>**site de document**</span><span class="sxs-lookup"><span data-stu-id="caf5a-261"><span id="com.document_site_gloss"></span><span id="COM.DOCUMENT_SITE_GLOSS"></span>**document site**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-262">Site client implémenté par un conteneur d’objets de document pour gérer l’affichage et le stockage d’un objet de document.</span><span class="sxs-lookup"><span data-stu-id="caf5a-262">A client site implemented by a document object container for managing the display and storage of a document object.</span></span> <span data-ttu-id="caf5a-263">Chaque objet de document dans un conteneur a un site de document correspondant.</span><span class="sxs-lookup"><span data-stu-id="caf5a-263">Each document object in a container has a corresponding document site.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-264"><span id="com.document_site_object_gloss"></span><span id="COM.DOCUMENT_SITE_OBJECT_GLOSS"></span>**objet site de document**</span><span class="sxs-lookup"><span data-stu-id="caf5a-264"><span id="com.document_site_object_gloss"></span><span id="COM.DOCUMENT_SITE_OBJECT_GLOSS"></span>**document site object**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-265">Objet COM qui implémente l’interface [**IOleDocumentSite**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentsite) , en plus des interfaces de site client habituelles (telles que [**IOleClientSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleclientsite)).</span><span class="sxs-lookup"><span data-stu-id="caf5a-265">A COM object that implements the [**IOleDocumentSite**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentsite) interface, in addition to the usual client-site interfaces (such as [**IOleClientSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleclientsite)).</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-266"><span id="com.document_view_gloss"></span><span id="COM.DOCUMENT_VIEW_GLOSS"></span>**vue de document**</span><span class="sxs-lookup"><span data-stu-id="caf5a-266"><span id="com.document_view_gloss"></span><span id="COM.DOCUMENT_VIEW_GLOSS"></span>**document view**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-267">Présentation particulière des données d’un document.</span><span class="sxs-lookup"><span data-stu-id="caf5a-267">A particular presentation of a document's data.</span></span> <span data-ttu-id="caf5a-268">Un objet document unique peut avoir un ou plusieurs affichages, mais un seul affichage de document peut appartenir à un seul objet document.</span><span class="sxs-lookup"><span data-stu-id="caf5a-268">A single document object can have one or more views, but a single document view can belong to one and only one document object.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-269"><span id="com.document_view_object_gloss"></span><span id="COM.DOCUMENT_VIEW_OBJECT_GLOSS"></span>**objet de vue de document**</span><span class="sxs-lookup"><span data-stu-id="caf5a-269"><span id="com.document_view_object_gloss"></span><span id="COM.DOCUMENT_VIEW_OBJECT_GLOSS"></span>**document view object**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-270">Objet COM qui implémente l’interface [**IOleDocumentView**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentview) et qui correspond à une vue de document particulière.</span><span class="sxs-lookup"><span data-stu-id="caf5a-270">A COM object that implements the [**IOleDocumentView**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentview) interface and corresponds to a particular document view.</span></span> <span data-ttu-id="caf5a-271">Un objet avec plusieurs vues de document agrège un objet d’affichage de document distinct pour chaque vue.</span><span class="sxs-lookup"><span data-stu-id="caf5a-271">An object with multiple document views aggregates a separate document view object for each view.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-272"><span id="com.document_view_site_gloss"></span><span id="COM.DOCUMENT_VIEW_SITE_GLOSS"></span>**site d’affichage de documents**</span><span class="sxs-lookup"><span data-stu-id="caf5a-272"><span id="com.document_view_site_gloss"></span><span id="COM.DOCUMENT_VIEW_SITE_GLOSS"></span>**document view site**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-273">Objet agrégé par un objet site de document pour gérer l’espace d’affichage d’une vue particulière d’un objet document.</span><span class="sxs-lookup"><span data-stu-id="caf5a-273">An object aggregated by a document site object for managing the display space for a particular view of a document object.</span></span> <span data-ttu-id="caf5a-274">Dans un site de document donné, chaque vue de document a un site d’affichage de documents correspondant.</span><span class="sxs-lookup"><span data-stu-id="caf5a-274">Within a given document site, each document view has a corresponding document view site.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-275"><span id="com.document_view_site_object_gloss"></span><span id="COM.DOCUMENT_VIEW_SITE_OBJECT_GLOSS"></span>**objet de site d’affichage de document**</span><span class="sxs-lookup"><span data-stu-id="caf5a-275"><span id="com.document_view_site_object_gloss"></span><span id="COM.DOCUMENT_VIEW_SITE_OBJECT_GLOSS"></span>**document view site object**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-276">Objet COM qui est agrégé dans un objet de site de document et implémente l’interface [**IOleInPlaceSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplacesite) et, éventuellement, l’interface [**IContinueCallback**](/windows/desktop/api/DocObj/nn-docobj-icontinuecallback) .</span><span class="sxs-lookup"><span data-stu-id="caf5a-276">A COM object that is aggregated in a document site object and implements the [**IOleInPlaceSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplacesite) interface and, optionally, the [**IContinueCallback**](/windows/desktop/api/DocObj/nn-docobj-icontinuecallback) interface.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-277"><span id="com.drag_and_drop_gloss"></span><span id="COM.DRAG_AND_DROP_GLOSS"></span>**glisser-déplacer**</span><span class="sxs-lookup"><span data-stu-id="caf5a-277"><span id="com.drag_and_drop_gloss"></span><span id="COM.DRAG_AND_DROP_GLOSS"></span>**drag and drop**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-278">Opération dans laquelle l’utilisateur final utilise la souris ou un autre dispositif de pointage pour déplacer des données vers un autre emplacement dans la même fenêtre ou dans une autre fenêtre.</span><span class="sxs-lookup"><span data-stu-id="caf5a-278">An operation in which the end user uses the mouse or other pointing device to move data to another location in the same window or another window.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-279"><span id="com.embed_gloss"></span><span id="COM.EMBED_GLOSS"></span>**Incorporer**</span><span class="sxs-lookup"><span data-stu-id="caf5a-279"><span id="com.embed_gloss"></span><span id="COM.EMBED_GLOSS"></span>**embed**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-280">Insérer un objet dans un document composé de manière à conserver les formats de données natifs de cet objet et à l’autoriser à être modifié à partir de son conteneur à l’aide d’outils exposés par son serveur.</span><span class="sxs-lookup"><span data-stu-id="caf5a-280">To insert an object into a compound document in such a way as to preserve the data formats native to that object, and to enable it to be edited from within its container using tools exposed by its server.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-281"><span id="com.embedded_object_gloss"></span><span id="COM.EMBEDDED_OBJECT_GLOSS"></span>**objet incorporé**</span><span class="sxs-lookup"><span data-stu-id="caf5a-281"><span id="com.embedded_object_gloss"></span><span id="COM.EMBEDDED_OBJECT_GLOSS"></span>**embedded object**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-282">Objet dont les données sont stockées dans un document composé, mais l’objet s’exécute dans l’espace de processus de son serveur.</span><span class="sxs-lookup"><span data-stu-id="caf5a-282">An object whose data is stored in a compound document, but the object runs in the process space of its server.</span></span> <span data-ttu-id="caf5a-283">Le gestionnaire d’objets par défaut fournit un substitut dans l’espace de traitement de l’application conteneur pour l’objet réel.</span><span class="sxs-lookup"><span data-stu-id="caf5a-283">The default object handler provides a surrogate in the processing space of the container application for the real object.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-284"><span id="com.extended_property_gloss"></span><span id="COM.EXTENDED_PROPERTY_GLOSS"></span>**propriété étendue**</span><span class="sxs-lookup"><span data-stu-id="caf5a-284"><span id="com.extended_property_gloss"></span><span id="COM.EXTENDED_PROPERTY_GLOSS"></span>**extended property**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-285">Une propriété au moment de l’exécution, telle que la position et la taille d’un contrôle, qu’un utilisateur peut supposer être exposée par le contrôle, mais qui est exposée et gérée par le conteneur.</span><span class="sxs-lookup"><span data-stu-id="caf5a-285">A run-time property, such as a control's position and size, that a user would assume to be exposed by the control but is exposed and managed by the container.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-286"><span id="com.file_moniker_gloss"></span><span id="COM.FILE_MONIKER_GLOSS"></span>**moniker de fichier**</span><span class="sxs-lookup"><span data-stu-id="caf5a-286"><span id="com.file_moniker_gloss"></span><span id="COM.FILE_MONIKER_GLOSS"></span>**file moniker**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-287">Moniker basé sur un chemin d’accès dans le système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="caf5a-287">A moniker based on a path in the file system.</span></span> <span data-ttu-id="caf5a-288">Les monikers de fichiers peuvent être utilisés pour identifier les objets enregistrés dans leurs propres fichiers.</span><span class="sxs-lookup"><span data-stu-id="caf5a-288">File monikers can be used to identify objects that are saved in their own files.</span></span> <span data-ttu-id="caf5a-289">Un moniker de fichier est un objet COM qui prend en charge l’implémentation fournie par le système de l’interface [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) pour la classe moniker de fichier.</span><span class="sxs-lookup"><span data-stu-id="caf5a-289">A file moniker is a COM object that supports the system-provided implementation of the [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) interface for the file moniker class.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-290"><span id="com.font_object_gloss"></span><span id="COM.FONT_OBJECT_GLOSS"></span>**objet font**</span><span class="sxs-lookup"><span data-stu-id="caf5a-290"><span id="com.font_object_gloss"></span><span id="COM.FONT_OBJECT_GLOSS"></span>**font object**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-291">Objet COM qui fournit l’accès aux polices Graphics Device Interface (GDI) en implémentant l’interface [**IFont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont) .</span><span class="sxs-lookup"><span data-stu-id="caf5a-291">A COM object that provides access to Graphics Device Interface (GDI) fonts by implementing the [**IFont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont) interface.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-292"><span id="com.format_identifier_gloss"></span><span id="COM.FORMAT_IDENTIFIER_GLOSS"></span>**identificateur de format**</span><span class="sxs-lookup"><span data-stu-id="caf5a-292"><span id="com.format_identifier_gloss"></span><span id="COM.FORMAT_IDENTIFIER_GLOSS"></span>**format identifier**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-293">GUID qui identifie un jeu de propriétés persistantes.</span><span class="sxs-lookup"><span data-stu-id="caf5a-293">A GUID that identifies a persistent property set.</span></span> <span data-ttu-id="caf5a-294">Également appelé FMTID.</span><span class="sxs-lookup"><span data-stu-id="caf5a-294">Also referred to as FMTID.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-295"><span id="com.frame_gloss"></span><span id="COM.FRAME_GLOSS"></span>**Frame**</span><span class="sxs-lookup"><span data-stu-id="caf5a-295"><span id="com.frame_gloss"></span><span id="COM.FRAME_GLOSS"></span>**frame**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-296">Partie d’une application de conteneur responsable de la négociation des menus, des touches accélérateur, des barres d’outils et d’autres éléments partagés de l’interface utilisateur avec un objet COM incorporé ou un objet document.</span><span class="sxs-lookup"><span data-stu-id="caf5a-296">The part of a container application responsible for negotiating menus, accelerator keys, toolbars, and other shared user-interface elements with an embedded COM object or a document object.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-297"><span id="com.frame_object_gloss"></span><span id="COM.FRAME_OBJECT_GLOSS"></span>**objet Frame**</span><span class="sxs-lookup"><span data-stu-id="caf5a-297"><span id="com.frame_object_gloss"></span><span id="COM.FRAME_OBJECT_GLOSS"></span>**frame object**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-298">Objet COM qui implémente l’interface [**IOleInPlaceFrame**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceframe) et, éventuellement, l’interface [**IOleCommandTarget**](/windows/desktop/api/DocObj/nn-docobj-iolecommandtarget) .</span><span class="sxs-lookup"><span data-stu-id="caf5a-298">A COM object that implements the [**IOleInPlaceFrame**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceframe) interface and, optionally, the [**IOleCommandTarget**](/windows/desktop/api/DocObj/nn-docobj-iolecommandtarget) interface.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-299"><span id="com.generic_composite_moniker_gloss"></span><span id="COM.GENERIC_COMPOSITE_MONIKER_GLOSS"></span>**moniker composite générique**</span><span class="sxs-lookup"><span data-stu-id="caf5a-299"><span id="com.generic_composite_moniker_gloss"></span><span id="COM.GENERIC_COMPOSITE_MONIKER_GLOSS"></span>**generic composite moniker**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-300">Collection séquencée de monikers, en commençant par un moniker de fichier pour fournir le chemin d’accès au niveau du document et en continuant avec un ou plusieurs monikers d’élément qui, pris dans son ensemble, identifient un objet de manière unique.</span><span class="sxs-lookup"><span data-stu-id="caf5a-300">A sequenced collection of monikers, starting with a file moniker to provide the document-level path and continuing with one or more item monikers that, taken as a whole, uniquely identifies an object.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-301"><span id="com.helper_function_gloss"></span><span id="COM.HELPER_FUNCTION_GLOSS"></span>**fonction d’assistance**</span><span class="sxs-lookup"><span data-stu-id="caf5a-301"><span id="com.helper_function_gloss"></span><span id="COM.HELPER_FUNCTION_GLOSS"></span>**helper function**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-302">Fonction qui encapsule les appels à d’autres fonctions et méthodes d’interface accessibles publiquement dans le kit de développement logiciel (SDK) OLE.</span><span class="sxs-lookup"><span data-stu-id="caf5a-302">A function that encapsulates calls to other functions and interface methods publicly available in the OLE SDK.</span></span> <span data-ttu-id="caf5a-303">Les fonctions d’assistance sont un moyen pratique d’appeler des séquences fréquemment utilisées d’appels de fonction et de méthode qui accomplissent des tâches courantes.</span><span class="sxs-lookup"><span data-stu-id="caf5a-303">Helper functions are a convenient way to call frequently used sequences of function and method calls that accomplish common tasks.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-304"><span id="com.host_object_gloss"></span><span id="COM.HOST_OBJECT_GLOSS"></span>**objet hôte**</span><span class="sxs-lookup"><span data-stu-id="caf5a-304"><span id="com.host_object_gloss"></span><span id="COM.HOST_OBJECT_GLOSS"></span>**host object**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-305">Objet COM qui forme une relation hiérarchique avec un ou plusieurs autres objets COM, appelés objets dépendants.</span><span class="sxs-lookup"><span data-stu-id="caf5a-305">A COM object that forms a hierarchical relationship with one or more other COM objects, known as the dependent objects.</span></span> <span data-ttu-id="caf5a-306">En règle générale, l’objet hôte instancie les objets dépendants, et leur existence n’est utile que dans la durée de vie de l’objet hôte.</span><span class="sxs-lookup"><span data-stu-id="caf5a-306">Typically, the host object instantiates the dependent objects, and their existence only makes sense within the lifetime of the host object.</span></span> <span data-ttu-id="caf5a-307">Toutefois, l’objet hôte n’agit pas comme le contrôle [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) pour les objets dépendants, pas plus qu’il ne délègue directement aux implémentations d’interface de ces objets.</span><span class="sxs-lookup"><span data-stu-id="caf5a-307">However, the host object does not act as the controlling [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) for the dependent objects, nor does it directly delegate to the interface implementations of those objects.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-308"><span id="com.hresult_gloss"></span><span id="COM.HRESULT_GLOSS"></span>**SIGNÉ**</span><span class="sxs-lookup"><span data-stu-id="caf5a-308"><span id="com.hresult_gloss"></span><span id="COM.HRESULT_GLOSS"></span>**HRESULT**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-309">Une poignée de résultat opaque définie comme égale à zéro pour un retour réussi d’une fonction et une valeur différente de zéro si des informations d’erreur ou d’État sont retournées.</span><span class="sxs-lookup"><span data-stu-id="caf5a-309">An opaque result handle defined to be zero for a successful return from a function and nonzero if error or status information is returned.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-310"><span id="com.hyperlink_object_gloss"></span><span id="COM.HYPERLINK_OBJECT_GLOSS"></span>**objet Hyperlink**</span><span class="sxs-lookup"><span data-stu-id="caf5a-310"><span id="com.hyperlink_object_gloss"></span><span id="COM.HYPERLINK_OBJECT_GLOSS"></span>**hyperlink object**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-311">Objet COM qui implémente, au minimum, l’interface [**IHlink**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767974(v=vs.85)) et agit comme un lien vers un objet à un autre emplacement (la cible).</span><span class="sxs-lookup"><span data-stu-id="caf5a-311">A COM object that implements, at a minimum, the [**IHlink**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767974(v=vs.85)) interface and acts as a link to an object at another location (the target).</span></span> <span data-ttu-id="caf5a-312">Un lien hypertexte est constitué de quatre parties : un moniker qui identifie l’emplacement de la cible ; chaîne pour l’emplacement dans la cible ; nom convivial ou affichable pour la cible ; et une chaîne qui peut contenir des paramètres supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="caf5a-312">A hyperlink is made up of four parts: a moniker that identifies the target's location; a string for the location within the target; a friendly, or displayable, name for the target; and a string that can contain additional parameters.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-313"><span id="com.hyperlink_browse_context_gloss"></span><span id="COM.HYPERLINK_BROWSE_CONTEXT_GLOSS"></span>**contexte de navigation de lien hypertexte**</span><span class="sxs-lookup"><span data-stu-id="caf5a-313"><span id="com.hyperlink_browse_context_gloss"></span><span id="COM.HYPERLINK_BROWSE_CONTEXT_GLOSS"></span>**hyperlink browse context**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-314">Objet COM qui implémente l’interface [**IHlinkBrowseContext**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767949(v=vs.85)) et gère la pile de navigation de lien hypertexte.</span><span class="sxs-lookup"><span data-stu-id="caf5a-314">A COM object that implements the [**IHlinkBrowseContext**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767949(v=vs.85)) interface and maintains the hyperlink navigation stack.</span></span> <span data-ttu-id="caf5a-315">L’objet de contexte de navigation gère la fenêtre frame de lien hypertexte et la fenêtre de l’objet de cible de lien hypertexte.</span><span class="sxs-lookup"><span data-stu-id="caf5a-315">The browse context object manages the hyperlink frame window and hyperlink target object's window.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-316"><span id="com.hyperlink_container_gloss"></span><span id="COM.HYPERLINK_CONTAINER_GLOSS"></span>**conteneur de liens hypertexte**</span><span class="sxs-lookup"><span data-stu-id="caf5a-316"><span id="com.hyperlink_container_gloss"></span><span id="COM.HYPERLINK_CONTAINER_GLOSS"></span>**hyperlink container**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-317">Application conteneur qui prend en charge les liens hypertexte en implémentant l’interface [**IHlinkSite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767933(v=vs.85)) et, si les objets du conteneur peuvent être des cibles d’autres liens hypertexte, l’interface [**IHlinkTarget**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767929(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="caf5a-317">A container application that supports hyperlinks by implementing the [**IHlinkSite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767933(v=vs.85)) interface and, if the container's objects can be targets of other hyperlinks, the [**IHlinkTarget**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767929(v=vs.85)) interface.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-318"><span id="com.hyperlink_frame_object_gloss"></span><span id="COM.HYPERLINK_FRAME_OBJECT_GLOSS"></span>**objet de frame de lien hypertexte**</span><span class="sxs-lookup"><span data-stu-id="caf5a-318"><span id="com.hyperlink_frame_object_gloss"></span><span id="COM.HYPERLINK_FRAME_OBJECT_GLOSS"></span>**hyperlink frame object**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-319">Objet COM qui implémente l’interface [**IHlinkFrame**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767938(v=vs.85)) et contrôle la navigation et l’affichage de niveau supérieur des liens hypertexte pour le conteneur du frame et le serveur de la cible du lien hypertexte.</span><span class="sxs-lookup"><span data-stu-id="caf5a-319">A COM object that implements the [**IHlinkFrame**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767938(v=vs.85)) interface and controls the top-level navigation and display of hyperlinks for the frame's container and the hyperlink target's server.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-320"><span id="com.hyperlink_site_object_gloss"></span><span id="COM.HYPERLINK_SITE_OBJECT_GLOSS"></span>**objet de site de lien hypertexte**</span><span class="sxs-lookup"><span data-stu-id="caf5a-320"><span id="com.hyperlink_site_object_gloss"></span><span id="COM.HYPERLINK_SITE_OBJECT_GLOSS"></span>**hyperlink site object**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-321">Objet COM qui implémente l’interface [**IHlinkSite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767933(v=vs.85)) et fournit soit le moniker, soit l’identificateur d’interface de son conteneur de liens hypertexte.</span><span class="sxs-lookup"><span data-stu-id="caf5a-321">A COM object that implements the [**IHlinkSite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767933(v=vs.85)) interface and supplies either the moniker or interface identifier of its hyperlink container.</span></span> <span data-ttu-id="caf5a-322">Un site de liens hypertexte peut traiter plusieurs liens hypertexte.</span><span class="sxs-lookup"><span data-stu-id="caf5a-322">One hyperlink site can serve multiple hyperlinks.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-323"><span id="com.hyperlink_target_object_gloss"></span><span id="COM.HYPERLINK_TARGET_OBJECT_GLOSS"></span>**objet de cible de lien hypertexte**</span><span class="sxs-lookup"><span data-stu-id="caf5a-323"><span id="com.hyperlink_target_object_gloss"></span><span id="COM.HYPERLINK_TARGET_OBJECT_GLOSS"></span>**hyperlink target object**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-324">Objet COM qui implémente l’interface [**IHlinkTarget**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767929(v=vs.85)) et fournit son moniker, son nom convivial et d’autres informations que d’autres objets Hyperlink utiliseront pour y accéder.</span><span class="sxs-lookup"><span data-stu-id="caf5a-324">A COM object that implements the [**IHlinkTarget**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767929(v=vs.85)) interface and supplies its moniker, friendly name, and other information that other hyperlink objects will use to navigate to it.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-325"><span id="com.in_parameter_gloss"></span><span id="COM.IN_PARAMETER_GLOSS"></span>**dans le paramètre**</span><span class="sxs-lookup"><span data-stu-id="caf5a-325"><span id="com.in_parameter_gloss"></span><span id="COM.IN_PARAMETER_GLOSS"></span>**in parameter**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-326">Paramètre qui est alloué, défini et libéré par l’appelant d’une fonction ou d’une méthode d’interface.</span><span class="sxs-lookup"><span data-stu-id="caf5a-326">A parameter that is allocated, set, and freed by the caller of a function or interface method.</span></span> <span data-ttu-id="caf5a-327">Un paramètre in n’est pas modifié par la fonction appelée.</span><span class="sxs-lookup"><span data-stu-id="caf5a-327">An in parameter is not modified by the called function.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-328"><span id="com.in_out_parameter_gloss"></span><span id="COM.IN_OUT_PARAMETER_GLOSS"></span>**paramètre in/out**</span><span class="sxs-lookup"><span data-stu-id="caf5a-328"><span id="com.in_out_parameter_gloss"></span><span id="COM.IN_OUT_PARAMETER_GLOSS"></span>**in/out parameter**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-329">Paramètre qui est initialement alloué par l’appelant d’une fonction ou d’une méthode d’interface, et défini, libéré et réalloué, si nécessaire, par le processus appelé.</span><span class="sxs-lookup"><span data-stu-id="caf5a-329">A parameter that is initially allocated by the caller of a function or interface method, and set, freed, and reallocated, if necessary, by the process that is called.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-330"><span id="com.in_place_activation_gloss"></span><span id="COM.IN_PLACE_ACTIVATION_GLOSS"></span>**activation sur place**</span><span class="sxs-lookup"><span data-stu-id="caf5a-330"><span id="com.in_place_activation_gloss"></span><span id="COM.IN_PLACE_ACTIVATION_GLOSS"></span>**in-place activation**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-331">Modification d’un objet incorporé dans la fenêtre de son conteneur à l’aide des outils fournis par le serveur.</span><span class="sxs-lookup"><span data-stu-id="caf5a-331">Editing an embedded object within the window of its container, using tools provided by the server.</span></span> <span data-ttu-id="caf5a-332">Les objets liés ne prennent pas en charge l’activation sur place ; ils sont toujours modifiés dans la fenêtre du serveur.</span><span class="sxs-lookup"><span data-stu-id="caf5a-332">Linked objects do not support in-place activation; they are always edited in the window of the server.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-333"><span id="com.in_process_server_gloss"></span><span id="COM.IN_PROCESS_SERVER_GLOSS"></span>**serveur in-process**</span><span class="sxs-lookup"><span data-stu-id="caf5a-333"><span id="com.in_process_server_gloss"></span><span id="COM.IN_PROCESS_SERVER_GLOSS"></span>**in-process server**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-334">Serveur implémenté comme une DLL qui s’exécute dans l’espace de processus du client.</span><span class="sxs-lookup"><span data-stu-id="caf5a-334">A server implemented as a DLL that runs in the process space of the client.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-335"><span id="com.instance_gloss"></span><span id="COM.INSTANCE_GLOSS"></span>**instancié**</span><span class="sxs-lookup"><span data-stu-id="caf5a-335"><span id="com.instance_gloss"></span><span id="COM.INSTANCE_GLOSS"></span>**instance**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-336">Objet pour lequel la mémoire est allouée ou qui est persistante.</span><span class="sxs-lookup"><span data-stu-id="caf5a-336">An object for which memory is allocated or which is persistent.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-337"><span id="com.interface_gloss"></span><span id="COM.INTERFACE_GLOSS"></span>**interface**</span><span class="sxs-lookup"><span data-stu-id="caf5a-337"><span id="com.interface_gloss"></span><span id="COM.INTERFACE_GLOSS"></span>**interface**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-338">Groupe de fonctions sémantiquement associées qui fournissent l’accès à un objet COM.</span><span class="sxs-lookup"><span data-stu-id="caf5a-338">A group of semantically related functions that provide access to a COM object.</span></span> <span data-ttu-id="caf5a-339">Chaque interface OLE définit un contrat qui autorise les objets à interagir en fonction du modèle COM (Component Object Model).</span><span class="sxs-lookup"><span data-stu-id="caf5a-339">Each OLE interface defines a contract that allows objects to interact according to the Component Object Model (COM).</span></span> <span data-ttu-id="caf5a-340">Bien que OLE fournisse de nombreuses implémentations d’interface, la plupart des interfaces peuvent également être implémentées par les développeurs qui conçoivent des applications OLE.</span><span class="sxs-lookup"><span data-stu-id="caf5a-340">While OLE provides many interface implementations, most interfaces can also be implemented by developers designing OLE applications.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-341"><span id="com.interface_identifier_iid_gloss"></span><span id="COM.INTERFACE_IDENTIFIER_IID_GLOSS"></span>**identificateur d’interface (IID)**</span><span class="sxs-lookup"><span data-stu-id="caf5a-341"><span id="com.interface_identifier_iid_gloss"></span><span id="COM.INTERFACE_IDENTIFIER_IID_GLOSS"></span>**interface identifier (IID)**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-342">Identificateur global unique (GUID) associé à une interface.</span><span class="sxs-lookup"><span data-stu-id="caf5a-342">A globally unique identifier (GUID) associated with an interface.</span></span> <span data-ttu-id="caf5a-343">Certaines fonctions prennent les IID comme paramètres pour permettre à l’appelant de spécifier le pointeur d’interface qui doit être retourné.</span><span class="sxs-lookup"><span data-stu-id="caf5a-343">Some functions take IIDs as parameters to allow the caller to specify which interface pointer should be returned.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-344"><span id="com.item_moniker_gloss"></span><span id="COM.ITEM_MONIKER_GLOSS"></span>**moniker d’élément**</span><span class="sxs-lookup"><span data-stu-id="caf5a-344"><span id="com.item_moniker_gloss"></span><span id="COM.ITEM_MONIKER_GLOSS"></span>**item moniker**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-345">Moniker basé sur une chaîne qui identifie un objet dans un conteneur.</span><span class="sxs-lookup"><span data-stu-id="caf5a-345">A moniker based on a string that identifies an object in a container.</span></span> <span data-ttu-id="caf5a-346">Les monikers d’élément peuvent identifier des objets plus petits qu’un fichier, y compris des objets incorporés dans un document composé, ou un pseudo-objet (comme une plage de cellules dans une feuille de calcul).</span><span class="sxs-lookup"><span data-stu-id="caf5a-346">Item monikers can identify objects smaller than a file, including embedded objects in a compound document, or a pseudo-object (like a range of cells in a spreadsheet).</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-347"><span id="com.licensing_gloss"></span><span id="COM.LICENSING_GLOSS"></span>**Licensing**</span><span class="sxs-lookup"><span data-stu-id="caf5a-347"><span id="com.licensing_gloss"></span><span id="COM.LICENSING_GLOSS"></span>**licensing**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-348">Fonctionnalité de COM qui permet de contrôler la création d’objets.</span><span class="sxs-lookup"><span data-stu-id="caf5a-348">A feature of COM that provides control over object creation.</span></span> <span data-ttu-id="caf5a-349">Les objets sous licence ne peuvent être créés que par des clients autorisés à les utiliser.</span><span class="sxs-lookup"><span data-stu-id="caf5a-349">Licensed objects can be created only by clients that are authorized to use them.</span></span> <span data-ttu-id="caf5a-350">La gestion des licences est implémentée dans COM par le biais de l’interface [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) et par la prise en charge d’une clé de licence qui peut être transmise au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="caf5a-350">Licensing is implemented in COM through the [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) interface and by support for a license key that can be passed at run time.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-351"><span id="com.link_object_gloss"></span><span id="COM.LINK_OBJECT_GLOSS"></span>**objet Link**</span><span class="sxs-lookup"><span data-stu-id="caf5a-351"><span id="com.link_object_gloss"></span><span id="COM.LINK_OBJECT_GLOSS"></span>**link object**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-352">Objet COM créé lors de la création ou du chargement d’un objet COM lié.</span><span class="sxs-lookup"><span data-stu-id="caf5a-352">A COM object that is created when a linked COM object is created or loaded.</span></span> <span data-ttu-id="caf5a-353">L’objet Link est fourni par OLE et implémente l’interface [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink) .</span><span class="sxs-lookup"><span data-stu-id="caf5a-353">The link object is provided by OLE and implements the [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink) interface.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-354"><span id="com.linked_object_gloss"></span><span id="COM.LINKED_OBJECT_GLOSS"></span>**objet lié**</span><span class="sxs-lookup"><span data-stu-id="caf5a-354"><span id="com.linked_object_gloss"></span><span id="COM.LINKED_OBJECT_GLOSS"></span>**linked object**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-355">Objet COM dont les données sources résident physiquement là où elles ont été initialement créées.</span><span class="sxs-lookup"><span data-stu-id="caf5a-355">A COM object whose source data physically resides where it was initially created.</span></span> <span data-ttu-id="caf5a-356">Seul un moniker qui représente les données sources et les données de présentation appropriées est conservé avec le document composé.</span><span class="sxs-lookup"><span data-stu-id="caf5a-356">Only a moniker that represents the source data and the appropriate presentation data are kept with the compound document.</span></span> <span data-ttu-id="caf5a-357">Les modifications apportées à la source du lien sont automatiquement reflétées dans l’objet lié.</span><span class="sxs-lookup"><span data-stu-id="caf5a-357">Changes made to the link source are automatically reflected in the linked object.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-358"><span id="com.link_source_gloss"></span><span id="COM.LINK_SOURCE_GLOSS"></span>**lier la source**</span><span class="sxs-lookup"><span data-stu-id="caf5a-358"><span id="com.link_source_gloss"></span><span id="COM.LINK_SOURCE_GLOSS"></span>**link source**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-359">Données qui constituent la source d’un objet lié.</span><span class="sxs-lookup"><span data-stu-id="caf5a-359">The data that is the source of a linked object.</span></span> <span data-ttu-id="caf5a-360">Une source de lien peut être un fichier ou une partie d’un fichier, tel qu’une plage de cellules sélectionnée dans un fichier (également appelé Pseudo-objet).</span><span class="sxs-lookup"><span data-stu-id="caf5a-360">A link source may be a file or a portion of a file, such as a selected range of cells within a file (also called a pseudo object).</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-361"><span id="com.loaded_state_gloss"></span><span id="COM.LOADED_STATE_GLOSS"></span>**État chargé**</span><span class="sxs-lookup"><span data-stu-id="caf5a-361"><span id="com.loaded_state_gloss"></span><span id="COM.LOADED_STATE_GLOSS"></span>**loaded state**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-362">L’état d’un objet après que ses structures de données ont été chargées en mémoire et sont accessibles au processus client.</span><span class="sxs-lookup"><span data-stu-id="caf5a-362">The state of an object after its data structures have been loaded into memory and are accessible to the client process.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-363"><span id="com.local_server_gloss"></span><span id="COM.LOCAL_SERVER_GLOSS"></span>**serveur local**</span><span class="sxs-lookup"><span data-stu-id="caf5a-363"><span id="com.local_server_gloss"></span><span id="COM.LOCAL_SERVER_GLOSS"></span>**local server**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-364">Un serveur hors processus implémenté en tant que. Application EXE s’exécutant sur le même ordinateur que son application cliente.</span><span class="sxs-lookup"><span data-stu-id="caf5a-364">An out-of-process server implemented as an .EXE application running on the same computer as its client application.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-365"><span id="com.lock_gloss"></span><span id="COM.LOCK_GLOSS"></span>**Lock**</span><span class="sxs-lookup"><span data-stu-id="caf5a-365"><span id="com.lock_gloss"></span><span id="COM.LOCK_GLOSS"></span>**lock**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-366">Un pointeur s’est maintenu sur-et éventuellement, un nombre de références incrémenté sur un objet en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="caf5a-366">A pointer held to-and possibly, a reference count incremented on-a running object.</span></span> <span data-ttu-id="caf5a-367">OLE définit deux types de verrous qui peuvent être conservés sur un objet : fort et faible.</span><span class="sxs-lookup"><span data-stu-id="caf5a-367">OLE defines two types of locks that can be held on an object: strong and weak.</span></span> <span data-ttu-id="caf5a-368">Pour implémenter un verrou fort, un serveur doit conserver à la fois un pointeur et un décompte de références, afin que l’objet reste « verrouillé » en mémoire au moins jusqu’à ce que le serveur appelle [**IUnknown :: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span><span class="sxs-lookup"><span data-stu-id="caf5a-368">To implement a strong lock, a server must maintain both a pointer and a reference count, so that the object will remain "locked" in memory at least until the server calls [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span></span> <span data-ttu-id="caf5a-369">Pour implémenter un verrou faible, le serveur gère uniquement un pointeur vers l’objet, afin que l’objet puisse être détruit par un autre processus.</span><span class="sxs-lookup"><span data-stu-id="caf5a-369">To implement a weak lock, the server maintains only a pointer to the object, so that the object can be destroyed by another process.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-370"><span id="com.marshaling_gloss"></span><span id="COM.MARSHALING_GLOSS"></span>**marshaling**</span><span class="sxs-lookup"><span data-stu-id="caf5a-370"><span id="com.marshaling_gloss"></span><span id="COM.MARSHALING_GLOSS"></span>**marshaling**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-371">Empaquetage et envoi d’appels de méthode d’interface à travers les limites de thread ou de processus.</span><span class="sxs-lookup"><span data-stu-id="caf5a-371">Packaging and sending interface method calls across thread or process boundaries.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-372"><span id="com.media_type_gloss"></span><span id="COM.MEDIA_TYPE_GLOSS"></span>**type de média**</span><span class="sxs-lookup"><span data-stu-id="caf5a-372"><span id="com.media_type_gloss"></span><span id="COM.MEDIA_TYPE_GLOSS"></span>**media type**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-373">Extension de MIME qui autorise la négociation de format de données entre un client et un objet.</span><span class="sxs-lookup"><span data-stu-id="caf5a-373">An extension of MIME that allows data format negotiation between a client and an object.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-374"><span id="com.mime_content_type_gloss"></span><span id="COM.MIME_CONTENT_TYPE_GLOSS"></span>**Type de contenu MIME**</span><span class="sxs-lookup"><span data-stu-id="caf5a-374"><span id="com.mime_content_type_gloss"></span><span id="COM.MIME_CONTENT_TYPE_GLOSS"></span>**MIME content type**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-375">Extension de MIME qui autorise la négociation de format de données entre un client et un objet.</span><span class="sxs-lookup"><span data-stu-id="caf5a-375">An extension of MIME that allows data format negotiation between a client and an object.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-376"><span id="com.multipurpose_internet_mail_extension_gloss"></span><span id="COM.MULTIPURPOSE_INTERNET_MAIL_EXTENSION_GLOSS"></span>**MIME (Multipurpose Internet Mail extension)**</span><span class="sxs-lookup"><span data-stu-id="caf5a-376"><span id="com.multipurpose_internet_mail_extension_gloss"></span><span id="COM.MULTIPURPOSE_INTERNET_MAIL_EXTENSION_GLOSS"></span>**Multipurpose Internet Mail Extension (MIME)**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-377">Protocole Internet développé à l’origine pour permettre l’échange de messages électroniques avec du contenu riche sur des environnements de réseau, d’ordinateur et de messagerie hétérogènes.</span><span class="sxs-lookup"><span data-stu-id="caf5a-377">An Internet protocol originally developed to allow exchange of electronic mail messages with rich content across heterogeneous network, computer, and email environments.</span></span> <span data-ttu-id="caf5a-378">En pratique, MIME a également été adopté et étendu par les applications non-messagerie.</span><span class="sxs-lookup"><span data-stu-id="caf5a-378">In practice, MIME has also been adopted and extended by non-mail applications.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-379"><span id="com.moniker_gloss"></span><span id="COM.MONIKER_GLOSS"></span>**moniker**</span><span class="sxs-lookup"><span data-stu-id="caf5a-379"><span id="com.moniker_gloss"></span><span id="COM.MONIKER_GLOSS"></span>**moniker**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-380">Objet qui implémente l’interface [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) .</span><span class="sxs-lookup"><span data-stu-id="caf5a-380">An object that implements the [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) interface.</span></span> <span data-ttu-id="caf5a-381">Un moniker agit comme un nom qui identifie de façon unique un objet COM.</span><span class="sxs-lookup"><span data-stu-id="caf5a-381">A moniker acts as a name that uniquely identifies a COM object.</span></span> <span data-ttu-id="caf5a-382">De la même façon qu’un chemin d’accès identifie un fichier dans le système de fichiers, un moniker identifie un objet COM dans l’espace de noms du répertoire.</span><span class="sxs-lookup"><span data-stu-id="caf5a-382">In the same way that a path identifies a file in the file system, a moniker identifies a COM object in the directory namespace.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-383"><span id="com.moniker_class_gloss"></span><span id="COM.MONIKER_CLASS_GLOSS"></span>**moniker (classe)**</span><span class="sxs-lookup"><span data-stu-id="caf5a-383"><span id="com.moniker_class_gloss"></span><span id="COM.MONIKER_CLASS_GLOSS"></span>**moniker class**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-384">Implémentation de l’interface [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) .</span><span class="sxs-lookup"><span data-stu-id="caf5a-384">An implementation of the [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) interface.</span></span> <span data-ttu-id="caf5a-385">Les classes de moniker fournies par le système incluent les monikers de fichiers, les monikers d’élément, les monikers composites génériques, les anti-monikers, les monikers de pointeur et les monikers d’URL.</span><span class="sxs-lookup"><span data-stu-id="caf5a-385">System-supplied moniker classes include file monikers, item monikers, generic composite monikers, anti-monikers, pointer monikers, and URL monikers.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-386"><span id="com.moniker_client_gloss"></span><span id="COM.MONIKER_CLIENT_GLOSS"></span>**client moniker**</span><span class="sxs-lookup"><span data-stu-id="caf5a-386"><span id="com.moniker_client_gloss"></span><span id="COM.MONIKER_CLIENT_GLOSS"></span>**moniker client**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-387">Application qui utilise des monikers pour obtenir des pointeurs d’interface vers des objets gérés par une autre application.</span><span class="sxs-lookup"><span data-stu-id="caf5a-387">An application that uses monikers to acquire interface pointers to objects managed by another application.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-388"><span id="com.moniker_provider_gloss"></span><span id="COM.MONIKER_PROVIDER_GLOSS"></span>**fournisseur de moniker**</span><span class="sxs-lookup"><span data-stu-id="caf5a-388"><span id="com.moniker_provider_gloss"></span><span id="COM.MONIKER_PROVIDER_GLOSS"></span>**moniker provider**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-389">Application qui rend les monikers disponibles qui identifient les objets qu’il gère, afin que les objets soient accessibles à d’autres applications.</span><span class="sxs-lookup"><span data-stu-id="caf5a-389">An application that makes available monikers that identify the objects it manages, so that the objects are accessible to other applications.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-390"><span id="com.namespace_extension_gloss"></span><span id="COM.NAMESPACE_EXTENSION_GLOSS"></span>**extension de l’espace de noms**</span><span class="sxs-lookup"><span data-stu-id="caf5a-390"><span id="com.namespace_extension_gloss"></span><span id="COM.NAMESPACE_EXTENSION_GLOSS"></span>**namespace extension**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-391">Objet COM in-process qui implémente [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder), [**IPersistFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder)et [**IShellView**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellview), qui sont parfois appelés interfaces d’extension d’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="caf5a-391">An in-process COM object that implements [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder), [**IPersistFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder), and [**IShellView**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellview), which are sometimes referred to as the namespace extension interfaces.</span></span> <span data-ttu-id="caf5a-392">Une extension d’espace de noms est utilisée pour étendre l’espace de noms de l’interpréteur de commandes ou pour créer un espace de noms distinct.</span><span class="sxs-lookup"><span data-stu-id="caf5a-392">A namespace extension is used either to extend the shell's namespace or to create a separate namespace.</span></span> <span data-ttu-id="caf5a-393">Les utilisateurs principaux sont l’Explorateur Windows et les boîtes de dialogue de fichier courantes.</span><span class="sxs-lookup"><span data-stu-id="caf5a-393">Primary users are the Windows Explorer and common file dialog boxes.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-394"><span id="com.native_data_gloss"></span><span id="COM.NATIVE_DATA_GLOSS"></span>**données natives**</span><span class="sxs-lookup"><span data-stu-id="caf5a-394"><span id="com.native_data_gloss"></span><span id="COM.NATIVE_DATA_GLOSS"></span>**native data**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-395">Données utilisées par une application serveur OLE lors de la modification d’un objet incorporé.</span><span class="sxs-lookup"><span data-stu-id="caf5a-395">The data used by an OLE server application when editing an embedded object.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-396"><span id="com.object_gloss"></span><span id="COM.OBJECT_GLOSS"></span>**dessin**</span><span class="sxs-lookup"><span data-stu-id="caf5a-396"><span id="com.object_gloss"></span><span id="COM.OBJECT_GLOSS"></span>**object**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-397">Dans OLE, structure de programmation encapsulant à la fois les données et les fonctionnalités qui sont définies et allouées en tant qu’unité unique et pour lesquelles le seul accès public s’effectue via les interfaces de la structure de programmation.</span><span class="sxs-lookup"><span data-stu-id="caf5a-397">In OLE, a programming structure encapsulating both data and functionality that are defined and allocated as a single unit and for which the only public access is through the programming structure's interfaces.</span></span> <span data-ttu-id="caf5a-398">Un objet COM doit prendre en charge, au minimum, l’interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) , qui maintient l’existence de l’objet pendant son utilisation et fournit l’accès aux autres interfaces de l’objet.</span><span class="sxs-lookup"><span data-stu-id="caf5a-398">A COM object must support, at a minimum, the [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface, which maintains the object's existence while it is being used and provides access to the object's other interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-399"><span id="com.object_state_gloss"></span><span id="COM.OBJECT_STATE_GLOSS"></span>**État de l’objet**</span><span class="sxs-lookup"><span data-stu-id="caf5a-399"><span id="com.object_state_gloss"></span><span id="COM.OBJECT_STATE_GLOSS"></span>**object state**</span></span> 
</dt> <dd>

<span data-ttu-id="caf5a-400">Relation entre un objet de document composé dans son conteneur et l’application responsable de la création de l’objet : active, passive, chargée ou en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="caf5a-400">The relationship between a compound document object in its container and the application responsible for the object's creation: active, passive, loaded, or running.</span></span> <span data-ttu-id="caf5a-401">Les objets passifs sont stockés sur le disque ou dans une base de données, et l’objet n’est pas sélectionné ou actif.</span><span class="sxs-lookup"><span data-stu-id="caf5a-401">Passive objects are stored on disk or in a database, and the object is not selected or active.</span></span> <span data-ttu-id="caf5a-402">Dans l’État chargé, les structures de données de l’objet ont été chargées en mémoire, mais elles ne sont pas disponibles pour les opérations telles que la modification.</span><span class="sxs-lookup"><span data-stu-id="caf5a-402">In the loaded state, the object's data structures have been loaded into memory, but they are not available for operations such as editing.</span></span> <span data-ttu-id="caf5a-403">Les objets en cours d’exécution sont tous deux chargés et disponibles pour toutes les opérations.</span><span class="sxs-lookup"><span data-stu-id="caf5a-403">Running objects are both loaded and available for all operations.</span></span> <span data-ttu-id="caf5a-404">Les objets actifs exécutent des objets qui ont une interface utilisateur visible.</span><span class="sxs-lookup"><span data-stu-id="caf5a-404">Active objects are running objects that have a visible user interface.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-405"><span id="com.object_type_name_gloss"></span><span id="COM.OBJECT_TYPE_NAME_GLOSS"></span>**nom du type d’objet**</span><span class="sxs-lookup"><span data-stu-id="caf5a-405"><span id="com.object_type_name_gloss"></span><span id="COM.OBJECT_TYPE_NAME_GLOSS"></span>**object type name**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-406">Chaîne d’identification unique stockée dans le cadre des informations disponibles pour un objet dans la base de données d’inscription.</span><span class="sxs-lookup"><span data-stu-id="caf5a-406">A unique identification string that is stored as part of the information available for an object in the registration database.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-407"><span id="com.ole_gloss"></span><span id="COM.OLE_GLOSS"></span>**ActiveX**</span><span class="sxs-lookup"><span data-stu-id="caf5a-407"><span id="com.ole_gloss"></span><span id="COM.OLE_GLOSS"></span>**OLE**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-408">Technologie basée sur les objets de Microsoft permettant de partager des informations et des services au-delà des limites des processus et des ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="caf5a-408">Microsoft's object-based technology for sharing information and services across process and computer boundaries.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-409"><span id="com.out_of_process_server_gloss"></span><span id="COM.OUT_OF_PROCESS_SERVER_GLOSS"></span>**serveur hors processus**</span><span class="sxs-lookup"><span data-stu-id="caf5a-409"><span id="com.out_of_process_server_gloss"></span><span id="COM.OUT_OF_PROCESS_SERVER_GLOSS"></span>**out-of-process server**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-410">Un serveur, implémenté en tant que. EXE, qui s’exécute en dehors du processus de son client, soit sur le même ordinateur, soit sur un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="caf5a-410">A server, implemented as an .EXE application, which runs outside the process of its client, either on the same computer or a remote computer.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-411"><span id="com.out_parameter_gloss"></span><span id="COM.OUT_PARAMETER_GLOSS"></span>**paramètre de sortie**</span><span class="sxs-lookup"><span data-stu-id="caf5a-411"><span id="com.out_parameter_gloss"></span><span id="COM.OUT_PARAMETER_GLOSS"></span>**out parameter**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-412">Un paramètre de sortie est alloué par la fonction appelée et libéré par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="caf5a-412">An out parameter is allocated by the function being called, and freed by caller.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-413"><span id="com.passive_state_gloss"></span><span id="COM.PASSIVE_STATE_GLOSS"></span>**état passif**</span><span class="sxs-lookup"><span data-stu-id="caf5a-413"><span id="com.passive_state_gloss"></span><span id="COM.PASSIVE_STATE_GLOSS"></span>**passive state**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-414">État d’un objet COM lorsqu’il est stocké (sur disque ou dans une base de données).</span><span class="sxs-lookup"><span data-stu-id="caf5a-414">The state of a COM object when it is stored (on disk or in a database).</span></span> <span data-ttu-id="caf5a-415">L’objet n’est pas sélectionné ou actif.</span><span class="sxs-lookup"><span data-stu-id="caf5a-415">The object is not selected or active.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-416"><span id="com.persistent_property_gloss"></span><span id="COM.PERSISTENT_PROPERTY_GLOSS"></span>**propriété persistante**</span><span class="sxs-lookup"><span data-stu-id="caf5a-416"><span id="com.persistent_property_gloss"></span><span id="COM.PERSISTENT_PROPERTY_GLOSS"></span>**persistent property**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-417">Informations qui peuvent être stockées de manière permanente dans le cadre d’un objet de stockage, tel qu’un fichier ou un répertoire.</span><span class="sxs-lookup"><span data-stu-id="caf5a-417">Information that can be stored persistently as part of a storage object such as a file or directory.</span></span> <span data-ttu-id="caf5a-418">Les propriétés persistantes sont regroupées dans des jeux de propriétés, qui peuvent être affichés et modifiés.</span><span class="sxs-lookup"><span data-stu-id="caf5a-418">Persistent properties are grouped into property sets, which can be displayed and edited.</span></span>

<span data-ttu-id="caf5a-419">Une propriété persistante est différente des propriétés d’exécution des objets créés avec les contrôles OLE et les technologies d’automatisation, qui peuvent être utilisées pour affecter le comportement du système.</span><span class="sxs-lookup"><span data-stu-id="caf5a-419">A persistent property is different from the run-time properties of objects created with OLE Controls and Automation technologies, which can be used to affect system behavior.</span></span> <span data-ttu-id="caf5a-420">La structure [**PROPVARIANT**](/windows/win32/api/propidl/ns-propidl-propvariant) définit tous les types de propriétés persistantes valides, tandis que la structure **Variant** définit tous les types de propriétés d’exécution valides.</span><span class="sxs-lookup"><span data-stu-id="caf5a-420">The [**PROPVARIANT**](/windows/win32/api/propidl/ns-propidl-propvariant) structure defines all valid types of persistent properties, whereas the **VARIANT** structure defines all valid types of run-time properties.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-421"><span id="com.persistent_storage_gloss"></span><span id="COM.PERSISTENT_STORAGE_GLOSS"></span>**stockage persistant**</span><span class="sxs-lookup"><span data-stu-id="caf5a-421"><span id="com.persistent_storage_gloss"></span><span id="COM.PERSISTENT_STORAGE_GLOSS"></span>**persistent storage**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-422">Stockage d’un fichier ou d’un objet dans un support, tel qu’un système de fichiers ou une base de données, afin que l’objet et ses données soient conservés lorsque le fichier est fermé, puis rouvert ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="caf5a-422">Storage of a file or object in a medium such as a file system or database so that the object and its data persist when the file is closed and then re-opened at a later time.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-423"><span id="com.picture_object_gloss"></span><span id="COM.PICTURE_OBJECT_GLOSS"></span>**image, objet**</span><span class="sxs-lookup"><span data-stu-id="caf5a-423"><span id="com.picture_object_gloss"></span><span id="COM.PICTURE_OBJECT_GLOSS"></span>**picture object**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-424">Objet COM qui fournit l’accès aux images GDI en implémentant l’interface [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) .</span><span class="sxs-lookup"><span data-stu-id="caf5a-424">A COM object that provides access to GDI images by implementing the [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) interface.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-425"><span id="com.pointer_moniker_gloss"></span><span id="COM.POINTER_MONIKER_GLOSS"></span>**moniker du pointeur**</span><span class="sxs-lookup"><span data-stu-id="caf5a-425"><span id="com.pointer_moniker_gloss"></span><span id="COM.POINTER_MONIKER_GLOSS"></span>**pointer moniker**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-426">Moniker qui mappe un pointeur d’interface vers un objet en mémoire.</span><span class="sxs-lookup"><span data-stu-id="caf5a-426">A moniker that maps an interface pointer to an object in memory.</span></span> <span data-ttu-id="caf5a-427">Tandis que la plupart des monikers identifient les objets qui peuvent être stockés de manière permanente, les monikers de pointeur identifient les objets qui ne peuvent pas.</span><span class="sxs-lookup"><span data-stu-id="caf5a-427">Whereas most monikers identify objects that can be persistently stored, pointer monikers identify objects that cannot.</span></span> <span data-ttu-id="caf5a-428">Elles permettent à ces objets de participer à une opération de liaison de moniker.</span><span class="sxs-lookup"><span data-stu-id="caf5a-428">They allow such objects to participate in a moniker binding operation.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-429"><span id="com.presentation_data_gloss"></span><span id="COM.PRESENTATION_DATA_GLOSS"></span>**données de présentation**</span><span class="sxs-lookup"><span data-stu-id="caf5a-429"><span id="com.presentation_data_gloss"></span><span id="COM.PRESENTATION_DATA_GLOSS"></span>**presentation data**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-430">Données utilisées par un conteneur pour afficher des objets incorporés ou liés.</span><span class="sxs-lookup"><span data-stu-id="caf5a-430">The data used by a container to display embedded or linked objects.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-431"><span id="com.primary_verb_gloss"></span><span id="COM.PRIMARY_VERB_GLOSS"></span>**verbe principal**</span><span class="sxs-lookup"><span data-stu-id="caf5a-431"><span id="com.primary_verb_gloss"></span><span id="COM.PRIMARY_VERB_GLOSS"></span>**primary verb**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-432">Action associée aux opérations les plus courantes ou préférées effectuées par les utilisateurs sur un objet.</span><span class="sxs-lookup"><span data-stu-id="caf5a-432">The action associated with the most common or preferred operation users perform on an object.</span></span> <span data-ttu-id="caf5a-433">Le verbe principal est toujours défini comme verbe zéro dans la base de données d’inscription du système.</span><span class="sxs-lookup"><span data-stu-id="caf5a-433">The primary verb is always defined as verb zero in the system registration database.</span></span> <span data-ttu-id="caf5a-434">Le verbe principal d’un objet est exécuté en double-cliquant sur l’objet.</span><span class="sxs-lookup"><span data-stu-id="caf5a-434">An object's primary verb is executed by double-clicking on the object.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-435"><span id="com.property_gloss"></span><span id="COM.PROPERTY_GLOSS"></span>**propriété**</span><span class="sxs-lookup"><span data-stu-id="caf5a-435"><span id="com.property_gloss"></span><span id="COM.PROPERTY_GLOSS"></span>**property**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-436">Informations associées à un objet.</span><span class="sxs-lookup"><span data-stu-id="caf5a-436">Information that is associated with an object.</span></span> <span data-ttu-id="caf5a-437">Dans OLE, les propriétés se répartissent en deux catégories : les propriétés d’exécution et les propriétés persistantes.</span><span class="sxs-lookup"><span data-stu-id="caf5a-437">In OLE, properties fall into two categories: run-time properties and persistent properties.</span></span> <span data-ttu-id="caf5a-438">Les propriétés au moment de l’exécution sont généralement associées à des objets de contrôle ou à leurs conteneurs.</span><span class="sxs-lookup"><span data-stu-id="caf5a-438">Run-time properties are typically associated with control objects or their containers.</span></span> <span data-ttu-id="caf5a-439">Par exemple, la couleur d’arrière-plan est une propriété Runtime définie par le conteneur d’un contrôle.</span><span class="sxs-lookup"><span data-stu-id="caf5a-439">For example, background color is a run-time property set by a control's container.</span></span> <span data-ttu-id="caf5a-440">Les propriétés persistantes sont associées à des objets stockés.</span><span class="sxs-lookup"><span data-stu-id="caf5a-440">Persistent properties are associated with stored objects.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-441"><span id="com.property_frame_gloss"></span><span id="COM.PROPERTY_FRAME_GLOSS"></span>**frame de propriété**</span><span class="sxs-lookup"><span data-stu-id="caf5a-441"><span id="com.property_frame_gloss"></span><span id="COM.PROPERTY_FRAME_GLOSS"></span>**property frame**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-442">Mécanisme d’interface utilisateur qui affiche une ou plusieurs pages de propriétés pour un contrôle.</span><span class="sxs-lookup"><span data-stu-id="caf5a-442">The user interface mechanism that displays one or more property pages for a control.</span></span> <span data-ttu-id="caf5a-443">Le système d’exécution de contrôles OLE fournit une implémentation standard d’un frame de propriété qui est accessible à l’aide de la fonction d’assistance [**OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe) .</span><span class="sxs-lookup"><span data-stu-id="caf5a-443">The OLE Controls run-time system provides a standard implementation of a property frame that can be accessed by using the [**OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe) helper function.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-444"><span id="com.property_identifier_gloss"></span><span id="COM.PROPERTY_IDENTIFIER_GLOSS"></span>**identificateur de propriété**</span><span class="sxs-lookup"><span data-stu-id="caf5a-444"><span id="com.property_identifier_gloss"></span><span id="COM.PROPERTY_IDENTIFIER_GLOSS"></span>**property identifier**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-445">Entier signé de 4 octets qui identifie une propriété persistante dans un jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="caf5a-445">A four-byte signed integer that identifies a persistent property within a property set.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-446"><span id="com.property_page_gloss"></span><span id="COM.PROPERTY_PAGE_GLOSS"></span>**page de propriétés**</span><span class="sxs-lookup"><span data-stu-id="caf5a-446"><span id="com.property_page_gloss"></span><span id="COM.PROPERTY_PAGE_GLOSS"></span>**property page**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-447">Objet COM avec son propre CLSID qui fait partie d’une interface utilisateur, implémenté par un contrôle et qui permet d’afficher et de définir les propriétés du contrôle.</span><span class="sxs-lookup"><span data-stu-id="caf5a-447">A COM object with its own CLSID that is part of a user interface, implemented by a control, and allows the control's properties to be viewed and set.</span></span> <span data-ttu-id="caf5a-448">Les objets page de propriétés implémentent l’interface [**IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) .</span><span class="sxs-lookup"><span data-stu-id="caf5a-448">Property page objects implement the [**IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) interface.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-449"><span id="com.property_page_site_gloss"></span><span id="COM.PROPERTY_PAGE_SITE_GLOSS"></span>**site de la page de propriétés**</span><span class="sxs-lookup"><span data-stu-id="caf5a-449"><span id="com.property_page_site_gloss"></span><span id="COM.PROPERTY_PAGE_SITE_GLOSS"></span>**property page site**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-450">Emplacement dans le frame d’une propriété où une page de propriétés est affichée.</span><span class="sxs-lookup"><span data-stu-id="caf5a-450">The location within a property frame where a property page is displayed.</span></span> <span data-ttu-id="caf5a-451">Le frame de propriété implémente l’interface [**IPropertyPageSite**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypagesite) , qui contient des méthodes pour gérer les sites de chacune des pages de propriétés fournies par un contrôle.</span><span class="sxs-lookup"><span data-stu-id="caf5a-451">The property frame implements the [**IPropertyPageSite**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypagesite) interface, which contains methods to manage the sites of each of the property pages supplied by a control.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-452"><span id="com.property_set_gloss"></span><span id="COM.PROPERTY_SET_GLOSS"></span>**jeu de propriétés**</span><span class="sxs-lookup"><span data-stu-id="caf5a-452"><span id="com.property_set_gloss"></span><span id="COM.PROPERTY_SET_GLOSS"></span>**property set**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-453">Groupe de propriétés logiquement lié qui est associé à un objet stocké de manière permanente.</span><span class="sxs-lookup"><span data-stu-id="caf5a-453">A logically related group of properties that is associated with a persistently stored object.</span></span> <span data-ttu-id="caf5a-454">Pour créer, ouvrir, supprimer ou énumérer un ou plusieurs jeux de propriétés, implémentez l’interface [**IPropertySetStorage**](/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage) .</span><span class="sxs-lookup"><span data-stu-id="caf5a-454">To create, open, delete, or enumerate one or more property sets, implement the [**IPropertySetStorage**](/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage) interface.</span></span> <span data-ttu-id="caf5a-455">Si vous utilisez des fichiers composés, vous pouvez utiliser l’implémentation OLE de cette interface au lieu d’implémenter la vôtre.</span><span class="sxs-lookup"><span data-stu-id="caf5a-455">If you are using compound files, you can use OLE's implementation of this interface rather than implementing your own.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-456"><span id="com.property_set_storage_gloss"></span><span id="COM.PROPERTY_SET_STORAGE_GLOSS"></span>**stockage des jeux de propriétés**</span><span class="sxs-lookup"><span data-stu-id="caf5a-456"><span id="com.property_set_storage_gloss"></span><span id="COM.PROPERTY_SET_STORAGE_GLOSS"></span>**property set storage**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-457">Objet de stockage COM qui contient un jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="caf5a-457">A COM storage object that holds a property set.</span></span> <span data-ttu-id="caf5a-458">Un stockage de jeu de propriétés est un objet dépendant associé à et géré par un objet de stockage.</span><span class="sxs-lookup"><span data-stu-id="caf5a-458">A property set storage is a dependent object associated with and managed by a storage object.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-459"><span id="com.property_sheet_gloss"></span><span id="COM.PROPERTY_SHEET_GLOSS"></span>**feuille de propriétés**</span><span class="sxs-lookup"><span data-stu-id="caf5a-459"><span id="com.property_sheet_gloss"></span><span id="COM.PROPERTY_SHEET_GLOSS"></span>**property sheet**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-460">Ensemble de pages de propriétés pour un ou plusieurs objets.</span><span class="sxs-lookup"><span data-stu-id="caf5a-460">A set of property pages for one or more objects.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-461"><span id="com.proxy_gloss"></span><span id="COM.PROXY_GLOSS"></span>**procur**</span><span class="sxs-lookup"><span data-stu-id="caf5a-461"><span id="com.proxy_gloss"></span><span id="COM.PROXY_GLOSS"></span>**proxy**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-462">Objet spécifique à l’interface qui conditionne les paramètres de cette interface en vue d’un appel de méthode distant.</span><span class="sxs-lookup"><span data-stu-id="caf5a-462">An interface-specific object that packages parameters for that interface in preparation for a remote method call.</span></span> <span data-ttu-id="caf5a-463">Un proxy s’exécute dans l’espace d’adressage de l’expéditeur et communique avec un stub correspondant dans l’espace d’adressage du destinataire.</span><span class="sxs-lookup"><span data-stu-id="caf5a-463">A proxy runs in the address space of the sender and communicates with a corresponding stub in the receiver's address space.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-464"><span id="com.proxy_manager_gloss"></span><span id="COM.PROXY_MANAGER_GLOSS"></span>**gestionnaire proxy**</span><span class="sxs-lookup"><span data-stu-id="caf5a-464"><span id="com.proxy_manager_gloss"></span><span id="COM.PROXY_MANAGER_GLOSS"></span>**proxy manager**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-465">Dans le marshaling standard, proxy qui gère tous les proxies d’interface pour un objet unique.</span><span class="sxs-lookup"><span data-stu-id="caf5a-465">In standard marshaling, a proxy that manages all the interface proxies for a single object.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-466"><span id="com.pseudo_object_gloss"></span><span id="COM.PSEUDO_OBJECT_GLOSS"></span>**Pseudo-objet**</span><span class="sxs-lookup"><span data-stu-id="caf5a-466"><span id="com.pseudo_object_gloss"></span><span id="COM.PSEUDO_OBJECT_GLOSS"></span>**pseudo object**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-467">Partie d’un document ou d’un objet incorporé, tel qu’une plage de cellules dans une feuille de calcul, qui peut être la source d’un objet COM.</span><span class="sxs-lookup"><span data-stu-id="caf5a-467">A portion of a document or embedded object, such as a range of cells in a spreadsheet, that can be the source for a COM object.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-468"><span id="com.reference_counting_gloss"></span><span id="COM.REFERENCE_COUNTING_GLOSS"></span>**décompte de références**</span><span class="sxs-lookup"><span data-stu-id="caf5a-468"><span id="com.reference_counting_gloss"></span><span id="COM.REFERENCE_COUNTING_GLOSS"></span>**reference counting**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-469">Le fait de conserver un décompte de chaque pointeur d’interface sur un objet pour s’assurer que l’objet n’est pas détruit avant que toutes les références à celui-ci ne soient libérées.</span><span class="sxs-lookup"><span data-stu-id="caf5a-469">Keeping a count of each interface pointer held on an object to ensure that the object is not destroyed before all references to it are released.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-470"><span id="com.relative_moniker_gloss"></span><span id="COM.RELATIVE_MONIKER_GLOSS"></span>**moniker relatif**</span><span class="sxs-lookup"><span data-stu-id="caf5a-470"><span id="com.relative_moniker_gloss"></span><span id="COM.RELATIVE_MONIKER_GLOSS"></span>**relative moniker**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-471">Moniker qui spécifie l’emplacement d’un objet par rapport à l’emplacement d’un autre objet.</span><span class="sxs-lookup"><span data-stu-id="caf5a-471">A moniker that specifies the location of an object relative to the location of another object.</span></span> <span data-ttu-id="caf5a-472">Un moniker relatif est analogue à un chemin d’accès relatif, tel que. \\ sauvegarder le \\ rapport. ancien.</span><span class="sxs-lookup"><span data-stu-id="caf5a-472">A relative moniker is analogous to a relative path, such as ..\\backup\\report.old.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-473"><span id="com.remote_server_gloss"></span><span id="COM.REMOTE_SERVER_GLOSS"></span>**serveur distant**</span><span class="sxs-lookup"><span data-stu-id="caf5a-473"><span id="com.remote_server_gloss"></span><span id="COM.REMOTE_SERVER_GLOSS"></span>**remote server**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-474">Une application serveur, implémentée en tant que fichier EXE, qui s’exécute sur un ordinateur différent de l’application cliente qui l’utilise.</span><span class="sxs-lookup"><span data-stu-id="caf5a-474">A server application, implemented as an EXE, running on a different computer from the client application using it.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-475"><span id="com.revert_gloss"></span><span id="COM.REVERT_GLOSS"></span>**rétablir**</span><span class="sxs-lookup"><span data-stu-id="caf5a-475"><span id="com.revert_gloss"></span><span id="COM.REVERT_GLOSS"></span>**revert**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-476">Pour ignorer toutes les modifications apportées à un objet depuis la dernière validation des modifications ou l’ouverture du stockage de l’objet.</span><span class="sxs-lookup"><span data-stu-id="caf5a-476">To discard any changes made to an object since the last time the changes were committed or the object's storage was opened.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-477"><span id="com.root_storage_object_gloss"></span><span id="COM.ROOT_STORAGE_OBJECT_GLOSS"></span>**objet de stockage racine**</span><span class="sxs-lookup"><span data-stu-id="caf5a-477"><span id="com.root_storage_object_gloss"></span><span id="COM.ROOT_STORAGE_OBJECT_GLOSS"></span>**root storage object**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-478">Objet de stockage le plus à l’extérieur dans un document.</span><span class="sxs-lookup"><span data-stu-id="caf5a-478">The outermost storage object in a document.</span></span> <span data-ttu-id="caf5a-479">Un objet de stockage racine peut contenir d’autres objets de flux et de stockage imbriqués.</span><span class="sxs-lookup"><span data-stu-id="caf5a-479">A root storage object can contain other nested storage and stream objects.</span></span> <span data-ttu-id="caf5a-480">Par exemple, un document composé est enregistré sur le disque sous la forme d’une série d’objets de stockage et de flux au sein d’un objet de stockage racine.</span><span class="sxs-lookup"><span data-stu-id="caf5a-480">For example, a compound document is saved on disk as a series of storage and stream objects within a root storage object.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-481"><span id="com.running_state_gloss"></span><span id="COM.RUNNING_STATE_GLOSS"></span>**État en cours d’exécution**</span><span class="sxs-lookup"><span data-stu-id="caf5a-481"><span id="com.running_state_gloss"></span><span id="COM.RUNNING_STATE_GLOSS"></span>**running state**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-482">État d’un objet COM lorsque son application serveur est en cours d’exécution et qu’il est possible d’accéder à ses interfaces et de recevoir des notifications de modifications.</span><span class="sxs-lookup"><span data-stu-id="caf5a-482">The state of a COM object when its server application is running and it is possible to access its interfaces and receive notification of changes.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-483"><span id="com.running_object_table_gloss"></span><span id="COM.RUNNING_OBJECT_TABLE_GLOSS"></span>**table ROT (Running Object Table)**</span><span class="sxs-lookup"><span data-stu-id="caf5a-483"><span id="com.running_object_table_gloss"></span><span id="COM.RUNNING_OBJECT_TABLE_GLOSS"></span>**running object table (ROT)**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-484">Une table accessible globalement sur chaque ordinateur qui effectue le suivi de tous les objets COM dans l’État en cours d’exécution qui peuvent être identifiés par un moniker.</span><span class="sxs-lookup"><span data-stu-id="caf5a-484">A globally accessible table on each computer that keeps track of all COM objects in the running state that can be identified by a moniker.</span></span> <span data-ttu-id="caf5a-485">Les fournisseurs de monikers inscrivent un objet dans la table, ce qui incrémente le décompte de références de l’objet.</span><span class="sxs-lookup"><span data-stu-id="caf5a-485">Moniker providers register an object in the table, which increments the object's reference count.</span></span> <span data-ttu-id="caf5a-486">Pour que l’objet puisse être détruit, son moniker doit être libéré de la table.</span><span class="sxs-lookup"><span data-stu-id="caf5a-486">Before the object can be destroyed, its moniker must be released from the table.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-487"><span id="com.run_time_property_gloss"></span><span id="COM.RUN_TIME_PROPERTY_GLOSS"></span>**propriété au moment de l’exécution**</span><span class="sxs-lookup"><span data-stu-id="caf5a-487"><span id="com.run_time_property_gloss"></span><span id="COM.RUN_TIME_PROPERTY_GLOSS"></span>**run-time property**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-488">Informations d’État discrètes associées à un objet de contrôle ou à son conteneur.</span><span class="sxs-lookup"><span data-stu-id="caf5a-488">Discrete state information associated with a control object or its container.</span></span> <span data-ttu-id="caf5a-489">Il existe trois types de propriétés d’exécution : les propriétés ambiantes, les propriétés de contrôle et les propriétés étendues.</span><span class="sxs-lookup"><span data-stu-id="caf5a-489">There are three types of run-time properties: ambient properties, control properties, and extended properties.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-490"><span id="com.self_registration_gloss"></span><span id="COM.SELF_REGISTRATION_GLOSS"></span>**inscription automatique**</span><span class="sxs-lookup"><span data-stu-id="caf5a-490"><span id="com.self_registration_gloss"></span><span id="COM.SELF_REGISTRATION_GLOSS"></span>**self-registration**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-491">Processus par lequel un serveur peut effectuer ses propres opérations de registre.</span><span class="sxs-lookup"><span data-stu-id="caf5a-491">The process by which a server can perform its own registry operations.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-492"><span id="com.server_application_gloss"></span><span id="COM.SERVER_APPLICATION_GLOSS"></span>**application serveur**</span><span class="sxs-lookup"><span data-stu-id="caf5a-492"><span id="com.server_application_gloss"></span><span id="COM.SERVER_APPLICATION_GLOSS"></span>**server application**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-493">Application qui peut créer des objets COM.</span><span class="sxs-lookup"><span data-stu-id="caf5a-493">An application that can create COM objects.</span></span> <span data-ttu-id="caf5a-494">Les applications de conteneur peuvent ensuite incorporer ou lier ces objets.</span><span class="sxs-lookup"><span data-stu-id="caf5a-494">Container applications can then embed or link to these objects.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-495"><span id="com.static_object_gloss"></span><span id="COM.STATIC_OBJECT_GLOSS"></span>**objet statique**</span><span class="sxs-lookup"><span data-stu-id="caf5a-495"><span id="com.static_object_gloss"></span><span id="COM.STATIC_OBJECT_GLOSS"></span>**static object**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-496">Objet qui contient uniquement une présentation, sans données natives.</span><span class="sxs-lookup"><span data-stu-id="caf5a-496">An object that contains only a presentation, with no native data.</span></span> <span data-ttu-id="caf5a-497">Un conteneur peut traiter un objet statique comme s’il s’agissait d’un objet lié ou incorporé, à ceci près qu’il n’est pas possible de modifier un objet statique.</span><span class="sxs-lookup"><span data-stu-id="caf5a-497">A container can treat a static object as though it were a linked or embedded object, except that it is not possible to edit a static object.</span></span>

<span data-ttu-id="caf5a-498">Un objet statique peut résulter, par exemple, de la rupture d’un lien sur un objet lié, c’est-à-dire que l’application serveur n’est pas disponible ou que l’utilisateur ne souhaite plus mettre à jour l’objet lié.</span><span class="sxs-lookup"><span data-stu-id="caf5a-498">A static object can result, for example, from the breaking of a link on a linked object-that is, the server application is unavailable, or the user doesn't want the linked object to be updated anymore.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-499"><span id="com.storage_object_gloss"></span><span id="COM.STORAGE_OBJECT_GLOSS"></span>**objet de stockage**</span><span class="sxs-lookup"><span data-stu-id="caf5a-499"><span id="com.storage_object_gloss"></span><span id="COM.STORAGE_OBJECT_GLOSS"></span>**storage object**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-500">Objet COM qui implémente l’interface [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) .</span><span class="sxs-lookup"><span data-stu-id="caf5a-500">A COM object that implements the [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) interface.</span></span> <span data-ttu-id="caf5a-501">Un objet de stockage contient des objets de stockage imbriqués ou des objets de flux, ce qui donne l’équivalent d’une structure de répertoires/fichiers dans un seul fichier.</span><span class="sxs-lookup"><span data-stu-id="caf5a-501">A storage object contains nested storage objects or stream objects, resulting in the equivalent of a directory/file structure within a single file.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-502"><span id="com.stream_object_gloss"></span><span id="COM.STREAM_OBJECT_GLOSS"></span>**objet de flux**</span><span class="sxs-lookup"><span data-stu-id="caf5a-502"><span id="com.stream_object_gloss"></span><span id="COM.STREAM_OBJECT_GLOSS"></span>**stream object**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-503">Objet COM qui implémente l’interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) .</span><span class="sxs-lookup"><span data-stu-id="caf5a-503">A COM object that implements the [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface.</span></span> <span data-ttu-id="caf5a-504">Un objet de flux est analogue à un fichier dans un répertoire ou un système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="caf5a-504">A stream object is analogous to a file in a directory/file system.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-505"><span id="com.structured_storage_gloss"></span><span id="COM.STRUCTURED_STORAGE_GLOSS"></span>**Stockage structuré**</span><span class="sxs-lookup"><span data-stu-id="caf5a-505"><span id="com.structured_storage_gloss"></span><span id="COM.STRUCTURED_STORAGE_GLOSS"></span>**Structured Storage**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-506">Technologie OLE permettant de stocker des fichiers composés dans des systèmes de fichiers natifs.</span><span class="sxs-lookup"><span data-stu-id="caf5a-506">OLE's technology for storing compound files in native file systems.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-507"><span id="com.stub_gloss"></span><span id="COM.STUB_GLOSS"></span>**talon**</span><span class="sxs-lookup"><span data-stu-id="caf5a-507"><span id="com.stub_gloss"></span><span id="COM.STUB_GLOSS"></span>**stub**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-508">Quand les paramètres d’une fonction ou d’une méthode d’interface sont marshalés à travers une limite de processus, le stub est un objet spécifique à l’interface qui décompresse les paramètres marshalés et appelle la méthode requise.</span><span class="sxs-lookup"><span data-stu-id="caf5a-508">When a function's or interface method's parameters are marshaled across a process boundary, the stub is an interface-specific object that unpackages the marshaled parameters and calls the required method.</span></span> <span data-ttu-id="caf5a-509">Le stub s’exécute dans l’espace d’adressage du destinataire et communique avec un proxy correspondant dans l’espace d’adressage de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="caf5a-509">The stub runs in the receiver's address space and communicates with a corresponding proxy in the sender's address space.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-510"><span id="com.stub_manager_gloss"></span><span id="COM.STUB_MANAGER_GLOSS"></span>**Gestionnaire de stub**</span><span class="sxs-lookup"><span data-stu-id="caf5a-510"><span id="com.stub_manager_gloss"></span><span id="COM.STUB_MANAGER_GLOSS"></span>**stub manager**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-511">Gère tous les stubs d’interface pour un seul objet.</span><span class="sxs-lookup"><span data-stu-id="caf5a-511">Manages all of the interface stubs for a single object.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-512"><span id="com.synchronous_call_gloss"></span><span id="COM.SYNCHRONOUS_CALL_GLOSS"></span>**appel synchrone**</span><span class="sxs-lookup"><span data-stu-id="caf5a-512"><span id="com.synchronous_call_gloss"></span><span id="COM.SYNCHRONOUS_CALL_GLOSS"></span>**synchronous call**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-513">Appel de fonction qui n’autorise pas l’exécution des instructions supplémentaires dans le processus appelant tant que la fonction n’est pas retournée.</span><span class="sxs-lookup"><span data-stu-id="caf5a-513">A function call that does not allow further instructions in the calling process to be executed until the function returns.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-514"><span id="com.system_registry_gloss"></span><span id="COM.SYSTEM_REGISTRY_GLOSS"></span>**Registre système**</span><span class="sxs-lookup"><span data-stu-id="caf5a-514"><span id="com.system_registry_gloss"></span><span id="COM.SYSTEM_REGISTRY_GLOSS"></span>**system registry**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-515">Référentiel à l’ensemble du système d’informations pris en charge par Windows, qui contient des informations sur le système et ses applications, y compris les clients et les serveurs OLE.</span><span class="sxs-lookup"><span data-stu-id="caf5a-515">A system-wide repository of information supported by Windows, which contains information about the system and its applications, including OLE clients and servers.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-516"><span id="com.transacted_access_mode_gloss"></span><span id="COM.TRANSACTED_ACCESS_MODE_GLOSS"></span>**mode d’accès transactionnel**</span><span class="sxs-lookup"><span data-stu-id="caf5a-516"><span id="com.transacted_access_mode_gloss"></span><span id="COM.TRANSACTED_ACCESS_MODE_GLOSS"></span>**transacted access mode**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-517">Un des deux modes d’accès dans lesquels un objet de stockage peut être ouvert.</span><span class="sxs-lookup"><span data-stu-id="caf5a-517">One of two access modes in which a storage object can be opened.</span></span> <span data-ttu-id="caf5a-518">Lorsqu’ils sont ouverts en mode traité, les modifications sont stockées dans des mémoires tampons jusqu’à ce que l’objet de stockage racine valide ses modifications.</span><span class="sxs-lookup"><span data-stu-id="caf5a-518">When opened in transacted mode, changes are stored in buffers until the root storage object commits its changes.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-519"><span id="com.type_information_gloss"></span><span id="COM.TYPE_INFORMATION_GLOSS"></span>**informations de type**</span><span class="sxs-lookup"><span data-stu-id="caf5a-519"><span id="com.type_information_gloss"></span><span id="COM.TYPE_INFORMATION_GLOSS"></span>**type information**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-520">Informations sur la classe d’un objet fournie par une bibliothèque de types.</span><span class="sxs-lookup"><span data-stu-id="caf5a-520">Information about an object's class provided by a type library.</span></span> <span data-ttu-id="caf5a-521">Pour fournir des informations de type, un objet COM implémente l’interface [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) .</span><span class="sxs-lookup"><span data-stu-id="caf5a-521">To provide type information, a COM object implements the [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) interface.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-522"><span id="com.uniform_data_transfer_gloss"></span><span id="COM.UNIFORM_DATA_TRANSFER_GLOSS"></span>**transfert de données uniforme**</span><span class="sxs-lookup"><span data-stu-id="caf5a-522"><span id="com.uniform_data_transfer_gloss"></span><span id="COM.UNIFORM_DATA_TRANSFER_GLOSS"></span>**uniform data transfer**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-523">Modèle pour le transfert de données via le presse-papiers, le glisser-déplacer ou l’automatisation.</span><span class="sxs-lookup"><span data-stu-id="caf5a-523">A model for transferring data through the clipboard, drag and drop, or Automation.</span></span> <span data-ttu-id="caf5a-524">Les objets conformes à ce modèle implémentent l’interface [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) .</span><span class="sxs-lookup"><span data-stu-id="caf5a-524">Objects conforming to this model implement the [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) interface.</span></span> <span data-ttu-id="caf5a-525">Ce modèle remplace l’échange dynamique de données (DDE).</span><span class="sxs-lookup"><span data-stu-id="caf5a-525">This model replaces DDE (dynamic data exchange).</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-526"><span id="com.unmarshaling_gloss"></span><span id="COM.UNMARSHALING_GLOSS"></span>**unmarshaling**</span><span class="sxs-lookup"><span data-stu-id="caf5a-526"><span id="com.unmarshaling_gloss"></span><span id="COM.UNMARSHALING_GLOSS"></span>**unmarshaling**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-527">Décompression des paramètres qui ont été envoyés à un proxy au-delà des limites du processus.</span><span class="sxs-lookup"><span data-stu-id="caf5a-527">Unpacking parameters that have been sent to a proxy across process boundaries.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-528"><span id="com.universal_resource_locator_gloss"></span><span id="COM.UNIVERSAL_RESOURCE_LOCATOR_GLOSS"></span>**URL (Universal Resource Locator)**</span><span class="sxs-lookup"><span data-stu-id="caf5a-528"><span id="com.universal_resource_locator_gloss"></span><span id="COM.UNIVERSAL_RESOURCE_LOCATOR_GLOSS"></span>**universal resource locator (URL)**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-529">Identificateur utilisé par le World Wide Web pour les noms et les emplacements des objets sur Internet.</span><span class="sxs-lookup"><span data-stu-id="caf5a-529">The identifier used by the World Wide Web for the names and locations of objects on the Internet.</span></span> <span data-ttu-id="caf5a-530">OLE fournit une classe de moniker, un moniker d’URL, dont l’implémentation peut être utilisée pour lier un client aux objets identifiés par une URL.</span><span class="sxs-lookup"><span data-stu-id="caf5a-530">OLE provides a moniker class, URL moniker, whose implementation can be used to bind a client to objects identified by a URL.</span></span>

</dd> <dt>

<span data-ttu-id="caf5a-531"><span id="com.url_moniker_gloss"></span><span id="COM.URL_MONIKER_GLOSS"></span>**Moniker d’URL**</span><span class="sxs-lookup"><span data-stu-id="caf5a-531"><span id="com.url_moniker_gloss"></span><span id="COM.URL_MONIKER_GLOSS"></span>**URL moniker**</span></span>
</dt> <dd>

<span data-ttu-id="caf5a-532">Moniker basé sur une URL (Universal Resource Locator).</span><span class="sxs-lookup"><span data-stu-id="caf5a-532">A moniker based on a universal resource locator (URL).</span></span> <span data-ttu-id="caf5a-533">Un client peut utiliser des monikers d’URL pour se lier aux objets qui résident sur Internet.</span><span class="sxs-lookup"><span data-stu-id="caf5a-533">A client can use URL monikers to bind to objects that reside on the Internet.</span></span> <span data-ttu-id="caf5a-534">La classe moniker d’URL fournie par le système prend en charge les liaisons synchrones et asynchrones.</span><span class="sxs-lookup"><span data-stu-id="caf5a-534">The system-supplied URL moniker class supports both synchronous and asynchronous binding.</span></span>

</dd> </dl>

 

 