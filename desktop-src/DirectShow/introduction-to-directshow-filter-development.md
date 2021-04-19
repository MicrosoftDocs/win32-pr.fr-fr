---
description: Présentation du développement de filtres DirectShow
ms.assetid: d5162ea4-ef37-4993-a82c-782f03b08c64
title: Présentation du développement de filtres DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a42c5d2437b32f521b0efc39775f186267d3c99
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106516745"
---
# <a name="introduction-to-directshow-filter-development"></a><span data-ttu-id="faed6-103">Présentation du développement de filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="faed6-103">Introduction to DirectShow Filter Development</span></span>

<span data-ttu-id="faed6-104">Cette section fournit un bref aperçu des tâches impliquées dans le développement d’un filtre DirectShow personnalisé.</span><span class="sxs-lookup"><span data-stu-id="faed6-104">This section gives a brief outline of the tasks involved in developing a custom DirectShow filter.</span></span> <span data-ttu-id="faed6-105">Il fournit également des liens vers des rubriques qui traitent de ces tâches plus en détail.</span><span class="sxs-lookup"><span data-stu-id="faed6-105">It also provides links to topics that discuss these tasks in greater detail.</span></span> <span data-ttu-id="faed6-106">Avant de lire cette section, lisez les rubriques de la rubrique [à propos de DirectShow](about-directshow.md), qui décrivent l’architecture complète de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="faed6-106">Before reading this section, read the topics in [About DirectShow](about-directshow.md), which describe the overall DirectShow architecture.</span></span>

<span data-ttu-id="faed6-107">**Bibliothèque de classes de base DirectShow**</span><span class="sxs-lookup"><span data-stu-id="faed6-107">**DirectShow Base Class Library**</span></span>

<span data-ttu-id="faed6-108">Le kit de développement logiciel (SDK) DirectShow comprend un ensemble de classes C++ pour l’écriture de filtres.</span><span class="sxs-lookup"><span data-stu-id="faed6-108">The DirectShow SDK includes a set of C++ classes for writing filters.</span></span> <span data-ttu-id="faed6-109">Bien qu’elles ne soient pas requises, ces classes constituent la méthode recommandée pour écrire un nouveau filtre.</span><span class="sxs-lookup"><span data-stu-id="faed6-109">Although they are not required, these classes are the recommended way to write a new filter.</span></span> <span data-ttu-id="faed6-110">Pour utiliser les classes de base, compilez-les dans une bibliothèque statique et liez le fichier. lib à votre projet, comme décrit dans [génération de filtres DirectShow](building-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="faed6-110">To use the base classes, compile them into a static library and link the .lib file to your project, as described in [Building DirectShow Filters](building-directshow-filters.md).</span></span>

<span data-ttu-id="faed6-111">La bibliothèque de classes de base définit une classe racine pour les filtres, la classe [**CBaseFilter**](cbasefilter.md) .</span><span class="sxs-lookup"><span data-stu-id="faed6-111">The base class library defines a root class for filters, the [**CBaseFilter**](cbasefilter.md) class.</span></span> <span data-ttu-id="faed6-112">Plusieurs autres classes dérivent de **CBaseFilter** et sont spécialisées pour des genres particuliers de filtres.</span><span class="sxs-lookup"><span data-stu-id="faed6-112">Several other classes derive from **CBaseFilter**, and are specialized for particular kinds of filters.</span></span> <span data-ttu-id="faed6-113">Par exemple, la classe [**CTransformFilter**](ctransformfilter.md) est conçue pour les filtres de transformation.</span><span class="sxs-lookup"><span data-stu-id="faed6-113">For example, the [**CTransformFilter**](ctransformfilter.md) class is designed for transform filters.</span></span> <span data-ttu-id="faed6-114">Pour créer un nouveau filtre, implémentez une classe qui hérite de l’une des classes de filtre.</span><span class="sxs-lookup"><span data-stu-id="faed6-114">To create a new filter, implement a class that inherits from one of the filter classes.</span></span> <span data-ttu-id="faed6-115">Par exemple, votre déclaration de classe peut être la suivante :</span><span class="sxs-lookup"><span data-stu-id="faed6-115">For example, your class declaration might be as follows:</span></span>


```C++
class CMyFilter : public CTransformFilter
{
private:
    /* Declare variables and methods that are specific to your filter.
public:
    /* Override various methods in CTransformFilter */
};
```



<span data-ttu-id="faed6-116">Pour plus d’informations sur les classes de base DirectShow, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="faed6-116">For more information about the DirectShow base classes, see the following topics:</span></span>

-   [<span data-ttu-id="faed6-117">Classes de base DirectShow</span><span class="sxs-lookup"><span data-stu-id="faed6-117">DirectShow Base Classes</span></span>](directshow-base-classes.md)
-   [<span data-ttu-id="faed6-118">Génération de filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="faed6-118">Building DirectShow Filters</span></span>](building-directshow-filters.md)

<span data-ttu-id="faed6-119">**Création de codes confidentiels**</span><span class="sxs-lookup"><span data-stu-id="faed6-119">**Creating Pins**</span></span>

<span data-ttu-id="faed6-120">Un filtre doit créer un ou plusieurs codes confidentiels.</span><span class="sxs-lookup"><span data-stu-id="faed6-120">A filter must create one or more pins.</span></span> <span data-ttu-id="faed6-121">Le nombre de codes confidentiels peut être corrigé au moment de la conception, ou le filtre peut créer des codes confidentiels en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="faed6-121">The number of pins can be fixed at design time, or the filter can create new pins as needed.</span></span> <span data-ttu-id="faed6-122">Les codes confidentiels dérivent généralement de la classe [**CBasePin**](cbasepin.md) , ou d’une classe qui hérite de **CBasePin**, comme [**CBaseInputPin**](cbaseinputpin.md).</span><span class="sxs-lookup"><span data-stu-id="faed6-122">Pins generally derive from the [**CBasePin**](cbasepin.md) class, or from a class that inherits **CBasePin**, such as [**CBaseInputPin**](cbaseinputpin.md).</span></span> <span data-ttu-id="faed6-123">Les codes confidentiels du filtre doivent être déclarés en tant que variables de membre dans la classe de filtre.</span><span class="sxs-lookup"><span data-stu-id="faed6-123">The filter's pins should be declared as member variables in the filter class.</span></span> <span data-ttu-id="faed6-124">Certaines des classes de filtre définissent déjà les codes confidentiels, mais si votre filtre hérite directement de **CBaseFilter**, vous devez déclarer les codes confidentiels dans votre classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="faed6-124">Some of the filter classes already define the pins, but if your filter inherits directly from **CBaseFilter**, you must declare the pins in your derived class.</span></span>

<span data-ttu-id="faed6-125">**Négociation des connexions de pin**</span><span class="sxs-lookup"><span data-stu-id="faed6-125">**Negotiating Pin Connections**</span></span>

<span data-ttu-id="faed6-126">Lorsque le gestionnaire de graphes de filtre tente de connecter deux filtres, les broches doivent s’entendre sur différentes choses.</span><span class="sxs-lookup"><span data-stu-id="faed6-126">When the Filter Graph Manager tries to connect two filters, the pins must agree on various things.</span></span> <span data-ttu-id="faed6-127">Si ce n’est pas le cas, la tentative de connexion échoue.</span><span class="sxs-lookup"><span data-stu-id="faed6-127">If they cannot, the connection attempt fails.</span></span> <span data-ttu-id="faed6-128">En règle générale, les codes confidentiels négocient les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="faed6-128">Generally, pins negotiate the following:</span></span>

-   <span data-ttu-id="faed6-129">Transport.</span><span class="sxs-lookup"><span data-stu-id="faed6-129">Transport.</span></span> <span data-ttu-id="faed6-130">Le transport est le mécanisme utilisé par les filtres pour déplacer des échantillons de média à partir de la broche de sortie vers la broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="faed6-130">The transport is the mechanism that the filters will use to move media samples from the output pin to the input pin.</span></span> <span data-ttu-id="faed6-131">Par exemple, ils peuvent utiliser l’interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) (« push Model ») ou l’interface [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) (« pull Model »).</span><span class="sxs-lookup"><span data-stu-id="faed6-131">For example, they can use the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface ("push model") or the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface ("pull model").</span></span>
-   <span data-ttu-id="faed6-132">Type de média.</span><span class="sxs-lookup"><span data-stu-id="faed6-132">Media type.</span></span> <span data-ttu-id="faed6-133">Presque tous les codes confidentiels utilisent des types de médias pour décrire le format des données qu’ils fournissent.</span><span class="sxs-lookup"><span data-stu-id="faed6-133">Almost all pins use media types to describe the format of the data they will deliver.</span></span>
-   <span data-ttu-id="faed6-134">Allocateur.</span><span class="sxs-lookup"><span data-stu-id="faed6-134">Allocator.</span></span> <span data-ttu-id="faed6-135">L’Allocator est l’objet qui crée les mémoires tampons qui contiennent les données.</span><span class="sxs-lookup"><span data-stu-id="faed6-135">The allocator is the object that creates the buffers that hold the data.</span></span> <span data-ttu-id="faed6-136">Les pin doivent s’accorder sur le code confidentiel qui fournira l’allocateur.</span><span class="sxs-lookup"><span data-stu-id="faed6-136">The pins must agree which pin will provide the allocator.</span></span> <span data-ttu-id="faed6-137">Ils doivent également accepter la taille des mémoires tampons, le nombre de mémoires tampons à créer et d’autres propriétés de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="faed6-137">They must also agree on the size of the buffers, the number of buffers to create, and other buffer properties.</span></span>

<span data-ttu-id="faed6-138">Les classes de base implémentent une infrastructure pour ces négociations.</span><span class="sxs-lookup"><span data-stu-id="faed6-138">The base classes implement a framework for these negotiations.</span></span> <span data-ttu-id="faed6-139">Vous devez compléter les détails en remplaçant différentes méthodes dans la classe de base.</span><span class="sxs-lookup"><span data-stu-id="faed6-139">You must complete the details by overriding various methods in the base class.</span></span> <span data-ttu-id="faed6-140">L’ensemble de méthodes que vous devez substituer dépend de la classe et de la fonctionnalité de votre filtre.</span><span class="sxs-lookup"><span data-stu-id="faed6-140">The set of methods that you must override depends on the class and on the functionality of your filter.</span></span> <span data-ttu-id="faed6-141">Pour plus d’informations, consultez [la page Comment les filtres se connectent](how-filters-connect.md).</span><span class="sxs-lookup"><span data-stu-id="faed6-141">For more information, see [How Filters Connect](how-filters-connect.md).</span></span>

<span data-ttu-id="faed6-142">**Traitement et diffusion des données**</span><span class="sxs-lookup"><span data-stu-id="faed6-142">**Processing and Delivering Data**</span></span>

<span data-ttu-id="faed6-143">La principale fonction de la plupart des filtres consiste à traiter et à fournir des données multimédias.</span><span class="sxs-lookup"><span data-stu-id="faed6-143">The primary function of most filters is to process and deliver media data.</span></span> <span data-ttu-id="faed6-144">La façon dont cela se produit dépend du type de filtre :</span><span class="sxs-lookup"><span data-stu-id="faed6-144">How that occurs depends on the type of filter:</span></span>

-   <span data-ttu-id="faed6-145">Une source Push a un thread de travail qui remplit continuellement des exemples de données et les remet en aval.</span><span class="sxs-lookup"><span data-stu-id="faed6-145">A push source has a worker thread that continuously fills samples with data and delivers them downstream.</span></span>
-   <span data-ttu-id="faed6-146">Une source de tirage attend que son voisin en aval demande un échantillon.</span><span class="sxs-lookup"><span data-stu-id="faed6-146">A pull source waits for its downstream neighbor to request a sample.</span></span> <span data-ttu-id="faed6-147">Il répond en écrivant des données dans un exemple et en livrant l’exemple au filtre en aval.</span><span class="sxs-lookup"><span data-stu-id="faed6-147">It responds by writing data into a sample and delivering the sample to the downstream filter.</span></span> <span data-ttu-id="faed6-148">Le filtre en aval crée le thread qui pilote le Data Flow.</span><span class="sxs-lookup"><span data-stu-id="faed6-148">The downstream filter creates the thread that drives the data flow.</span></span>
-   <span data-ttu-id="faed6-149">Un filtre de transformation contient des exemples fournis par son voisin en amont.</span><span class="sxs-lookup"><span data-stu-id="faed6-149">A transform filter has samples delivered to it by its upstream neighbor.</span></span> <span data-ttu-id="faed6-150">Lorsqu’il reçoit un exemple, il traite les données et les remet en aval.</span><span class="sxs-lookup"><span data-stu-id="faed6-150">When it receives a sample, it processes the data and delivers it downstream.</span></span>
-   <span data-ttu-id="faed6-151">Un filtre de convertisseur reçoit des exemples de en amont et les planifie pour un rendu basé sur les horodatages.</span><span class="sxs-lookup"><span data-stu-id="faed6-151">A renderer filter receives samples from upstream, and schedules them for rendering based on the time stamps.</span></span>

<span data-ttu-id="faed6-152">Les autres tâches liées à la diffusion en continu incluent le vidage des données du graphique, la gestion de la fin du flux et la réponse aux demandes de recherche.</span><span class="sxs-lookup"><span data-stu-id="faed6-152">Other tasks related to streaming include flushing data from the graph, handling the end of the stream, and responding to seek requests.</span></span> <span data-ttu-id="faed6-153">Pour plus d’informations sur ces problèmes, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="faed6-153">For more information about these issues, see the following topics:</span></span>

-   [<span data-ttu-id="faed6-154">Transmission de données pour les développeurs de filtres</span><span class="sxs-lookup"><span data-stu-id="faed6-154">Data Flow for Filter Developers</span></span>](data-flow-for-filter-developers.md)
-   [<span data-ttu-id="faed6-155">Gestion du contrôle de la qualité</span><span class="sxs-lookup"><span data-stu-id="faed6-155">Quality-Control Management</span></span>](quality-control-management.md)
-   [<span data-ttu-id="faed6-156">Threads et sections critiques</span><span class="sxs-lookup"><span data-stu-id="faed6-156">Threads and Critical Sections</span></span>](threads-and-critical-sections.md)

<span data-ttu-id="faed6-157">**Prise en charge de COM**</span><span class="sxs-lookup"><span data-stu-id="faed6-157">**Supporting COM**</span></span>

<span data-ttu-id="faed6-158">Les filtres DirectShow sont des objets COM, généralement empaquetés dans des dll.</span><span class="sxs-lookup"><span data-stu-id="faed6-158">DirectShow filters are COM objects, typically packaged in DLLs.</span></span> <span data-ttu-id="faed6-159">La bibliothèque de classes de base implémente une infrastructure pour la prise en charge de COM.</span><span class="sxs-lookup"><span data-stu-id="faed6-159">The base class library implements a framework for supporting COM.</span></span> <span data-ttu-id="faed6-160">Elle est décrite dans la section [DirectShow et com](directshow-and-com.md).</span><span class="sxs-lookup"><span data-stu-id="faed6-160">It is described in the section [DirectShow and COM](directshow-and-com.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="faed6-161">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="faed6-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="faed6-162">Écriture de filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="faed6-162">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



