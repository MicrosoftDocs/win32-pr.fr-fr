---
description: Cette rubrique décrit comment implémenter la recherche dans un filtre de source Microsoft DirectShow. Elle utilise l’exemple de filtre ball comme point de départ et décrit le code supplémentaire nécessaire pour prendre en charge la recherche dans ce filtre.
ms.assetid: a2b4be09-2fd6-4aac-8ad6-c3d62377c1f2
title: Prise en charge de la recherche dans un filtre source
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42ac4bbb63410adf9cb4e8d69064679143b84d67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868521"
---
# <a name="supporting-seeking-in-a-source-filter"></a><span data-ttu-id="fb28f-104">Prise en charge de la recherche dans un filtre source</span><span class="sxs-lookup"><span data-stu-id="fb28f-104">Supporting Seeking in a Source Filter</span></span>

<span data-ttu-id="fb28f-105">Cette rubrique décrit comment implémenter la recherche dans un filtre de source Microsoft DirectShow.</span><span class="sxs-lookup"><span data-stu-id="fb28f-105">This topic describes how to implement seeking in a Microsoft DirectShow source filter.</span></span> <span data-ttu-id="fb28f-106">Elle utilise l’exemple de [filtre ball](ball-filter-sample.md) comme point de départ et décrit le code supplémentaire nécessaire pour prendre en charge la recherche dans ce filtre.</span><span class="sxs-lookup"><span data-stu-id="fb28f-106">It uses the [Ball Filter](ball-filter-sample.md) sample as the starting point and describes the additional code needed to support seeking in this filter.</span></span>

<span data-ttu-id="fb28f-107">L’exemple de [filtre ball](ball-filter-sample.md) est un filtre source qui crée une balle de rebond animée.</span><span class="sxs-lookup"><span data-stu-id="fb28f-107">The [Ball Filter](ball-filter-sample.md) sample is a source filter that creates an animated bouncing ball.</span></span> <span data-ttu-id="fb28f-108">Cet article explique comment ajouter des fonctionnalités de recherche à ce filtre.</span><span class="sxs-lookup"><span data-stu-id="fb28f-108">This article describes how to add seeking functionality to this filter.</span></span> <span data-ttu-id="fb28f-109">Une fois que vous avez ajouté cette fonctionnalité, vous pouvez afficher le filtre dans GraphEdit et contrôler la balle en faisant glisser le curseur GraphEdit.</span><span class="sxs-lookup"><span data-stu-id="fb28f-109">Once you have added this functionality, you can render the filter in GraphEdit and control the ball by dragging the GraphEdit slider.</span></span>

<span data-ttu-id="fb28f-110">Cette rubrique contient les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="fb28f-110">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="fb28f-111">Vue d’ensemble de la recherche dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="fb28f-111">Overview of Seeking in DirectShow</span></span>](#overview-of-seeking-in-directshow)
-   [<span data-ttu-id="fb28f-112">Aperçu rapide du filtre de la balle</span><span class="sxs-lookup"><span data-stu-id="fb28f-112">Quick Overview of the Ball Filter</span></span>](#quick-overview-of-the-ball-filter)
-   [<span data-ttu-id="fb28f-113">Modification du filtre de balle pour la recherche</span><span class="sxs-lookup"><span data-stu-id="fb28f-113">Modifying the Ball Filter for Seeking</span></span>](#modifying-the-ball-filter-for-seeking)
-   [<span data-ttu-id="fb28f-114">Limitations de la classe CSourceSeeking</span><span class="sxs-lookup"><span data-stu-id="fb28f-114">Limitations of the CSourceSeeking Class</span></span>](#limitations-of-the-csourceseeking-class)

## <a name="overview-of-seeking-in-directshow"></a><span data-ttu-id="fb28f-115">Vue d’ensemble de la recherche dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="fb28f-115">Overview of Seeking in DirectShow</span></span>

<span data-ttu-id="fb28f-116">Une application recherche le graphique de filtre en appelant une méthode [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) sur le gestionnaire de graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="fb28f-116">An application seeks the filter graph by calling an [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) method on the Filter Graph Manager.</span></span> <span data-ttu-id="fb28f-117">Le gestionnaire de graphique de filtre distribue ensuite l’appel à chaque convertisseur dans le graphique.</span><span class="sxs-lookup"><span data-stu-id="fb28f-117">The Filter Graph Manager then distributes the call to every renderer in the graph.</span></span> <span data-ttu-id="fb28f-118">Chaque convertisseur envoie l’appel en amont, par le biais de la broche de sortie du filtre amont suivant.</span><span class="sxs-lookup"><span data-stu-id="fb28f-118">Each renderer sends the call upstream, through the output pin of the next upstream filter.</span></span> <span data-ttu-id="fb28f-119">L’appel se déplace en amont jusqu’à ce qu’il atteigne un filtre qui peut exécuter la commande Seek, en général un filtre source ou un filtre d’analyseur.</span><span class="sxs-lookup"><span data-stu-id="fb28f-119">The call travels upstream until it reaches a filter that can execute the seek command, typically a source filter or a parser filter.</span></span> <span data-ttu-id="fb28f-120">En général, le filtre qui est à l’origine de l’horodatage gère également la recherche.</span><span class="sxs-lookup"><span data-stu-id="fb28f-120">In general, the filter that originates the time stamps also handles seeking.</span></span>

<span data-ttu-id="fb28f-121">Un filtre répond à une commande Seek comme suit :</span><span class="sxs-lookup"><span data-stu-id="fb28f-121">A filter responds to a seek command as follows:</span></span>

1.  <span data-ttu-id="fb28f-122">Le filtre vide le graphique.</span><span class="sxs-lookup"><span data-stu-id="fb28f-122">The filter flushes the graph.</span></span> <span data-ttu-id="fb28f-123">Cela efface toutes les données obsolètes du graphique, ce qui améliore la réactivité.</span><span class="sxs-lookup"><span data-stu-id="fb28f-123">This clears any stale data from graph, which improves responsiveness.</span></span> <span data-ttu-id="fb28f-124">Sinon, les exemples qui ont été mis en mémoire tampon avant la commande Seek peuvent être remis.</span><span class="sxs-lookup"><span data-stu-id="fb28f-124">Otherwise, samples that were buffered prior to the seek command might get delivered.</span></span>
2.  <span data-ttu-id="fb28f-125">Le filtre appelle [**IPIN :: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) pour informer les filtres en aval de la nouvelle heure d’arrêt, de l’heure de début et de la vitesse de lecture.</span><span class="sxs-lookup"><span data-stu-id="fb28f-125">The filter calls [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) to inform downstream filters of the new stop time, start time, and playback rate.</span></span>
3.  <span data-ttu-id="fb28f-126">Le filtre définit ensuite l’indicateur de discontinuité sur le premier échantillon après la commande Seek.</span><span class="sxs-lookup"><span data-stu-id="fb28f-126">The filter then sets the discontinuity flag on the first sample after the seek command.</span></span>

<span data-ttu-id="fb28f-127">Les horodatages commencent à zéro après toute commande Seek (y compris les changements de taux).</span><span class="sxs-lookup"><span data-stu-id="fb28f-127">Time stamps start from zero after any seek command (including rate changes).</span></span>

## <a name="quick-overview-of-the-ball-filter"></a><span data-ttu-id="fb28f-128">Aperçu rapide du filtre de la balle</span><span class="sxs-lookup"><span data-stu-id="fb28f-128">Quick Overview of the Ball Filter</span></span>

<span data-ttu-id="fb28f-129">Le filtre bille est une source push, ce qui signifie qu’il utilise un thread de travail pour remettre des exemples en aval, par opposition à une source pull, qui attend passivement un filtre en aval pour demander des exemples.</span><span class="sxs-lookup"><span data-stu-id="fb28f-129">The Ball filter is a push source, which means that it uses a worker thread to deliver samples downstream, as opposed to a pull source, which passively waits for a downstream filter to request samples.</span></span> <span data-ttu-id="fb28f-130">Le filtre balle est construit à partir de la classe [**CSource**](csource.md) , et sa broche de sortie est créée à partir de la classe [**CSourceStream**](csourcestream.md) .</span><span class="sxs-lookup"><span data-stu-id="fb28f-130">The Ball filter is built from the [**CSource**](csource.md) class, and its output pin is built from the [**CSourceStream**](csourcestream.md) class.</span></span> <span data-ttu-id="fb28f-131">La classe **CSourceStream** crée le thread de travail qui pilote le workflow de données.</span><span class="sxs-lookup"><span data-stu-id="fb28f-131">The **CSourceStream** class creates the worker thread that drives the flow of data.</span></span> <span data-ttu-id="fb28f-132">Ce thread entre dans une boucle qui obtient des échantillons de l’allocateur, les remplit avec les données et les remet en aval.</span><span class="sxs-lookup"><span data-stu-id="fb28f-132">This thread enters a loop that gets samples from the allocator, fills them with data, and delivers them downstream.</span></span>

<span data-ttu-id="fb28f-133">La majeure partie de l’action dans [**CSourceStream**](csourcestream.md) se produit dans la méthode [**CSourceStream :: FillBuffer**](csourcestream-fillbuffer.md) , que la classe dérivée implémente.</span><span class="sxs-lookup"><span data-stu-id="fb28f-133">Most of the action in [**CSourceStream**](csourcestream.md) happens in the [**CSourceStream::FillBuffer**](csourcestream-fillbuffer.md) method, which the derived class implements.</span></span> <span data-ttu-id="fb28f-134">L’argument de cette méthode est un pointeur vers l’exemple à remettre.</span><span class="sxs-lookup"><span data-stu-id="fb28f-134">The argument to this method is a pointer to the sample to be delivered.</span></span> <span data-ttu-id="fb28f-135">L’implémentation du filtre ball de **FillBuffer** récupère l’adresse de l’exemple de mémoire tampon et l’insère directement dans la mémoire tampon en définissant des valeurs de pixel individuelles.</span><span class="sxs-lookup"><span data-stu-id="fb28f-135">The Ball filter's implementation of **FillBuffer** retrieves the address of the sample buffer and draws directly to the buffer by setting individual pixel values.</span></span> <span data-ttu-id="fb28f-136">(Le dessin est effectué par une classe d’assistance, CBall, ce qui vous permet d’ignorer les détails concernant les profondeurs de bits, les palettes, etc.).</span><span class="sxs-lookup"><span data-stu-id="fb28f-136">(The drawing is done by a helper class, CBall, so you can ignore the details regarding bit depths, palettes, and so forth.)</span></span>

## <a name="modifying-the-ball-filter-for-seeking"></a><span data-ttu-id="fb28f-137">Modification du filtre de balle pour la recherche</span><span class="sxs-lookup"><span data-stu-id="fb28f-137">Modifying the Ball Filter for Seeking</span></span>

<span data-ttu-id="fb28f-138">Pour rendre le filtre de balle accessible, utilisez la classe [**CSourceSeeking**](csourceseeking.md) , qui est conçue pour l’implémentation de la recherche dans les filtres avec une seule broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="fb28f-138">To make the Ball filter seekable, use the [**CSourceSeeking**](csourceseeking.md) class, which is designed for implementing seeking in filters with one output pin.</span></span> <span data-ttu-id="fb28f-139">Ajoutez la classe **CSourceSeeking** à la liste d’héritage pour la classe CBallStream :</span><span class="sxs-lookup"><span data-stu-id="fb28f-139">Add the **CSourceSeeking** class to the inheritance list for the CBallStream class:</span></span>


```C++
class CBallStream :  // Defines the output pin.
    public CSourceStream, public CSourceSeeking
```



<span data-ttu-id="fb28f-140">En outre, vous devrez ajouter un initialiseur pour [**CSourceSeeking**](csourceseeking.md) au constructeur CBallStream :</span><span class="sxs-lookup"><span data-stu-id="fb28f-140">Also, you will need to add an initializer for [**CSourceSeeking**](csourceseeking.md) to the CBallStream constructor:</span></span>


```C++
    CSourceSeeking(NAME("SeekBall"), (IPin*)this, phr, &m_cSharedState),
```



<span data-ttu-id="fb28f-141">Cette instruction appelle le constructeur de base pour [**CSourceSeeking**](csourceseeking.md).</span><span class="sxs-lookup"><span data-stu-id="fb28f-141">This statement calls the base constructor for [**CSourceSeeking**](csourceseeking.md).</span></span> <span data-ttu-id="fb28f-142">Les paramètres sont un nom, un pointeur vers le code confidentiel propriétaire, une valeur **HRESULT** et l’adresse d’un objet de section critique.</span><span class="sxs-lookup"><span data-stu-id="fb28f-142">The parameters are a name, a pointer to the owning pin, an **HRESULT** value, and the address of a critical section object.</span></span> <span data-ttu-id="fb28f-143">Le nom est utilisé uniquement pour le débogage, et la macro de [**nom**](name.md) se compile en une chaîne vide dans les builds de vente au détail.</span><span class="sxs-lookup"><span data-stu-id="fb28f-143">The name is used only for debugging, and the [**NAME**](name.md) macro compiles to an empty string in retail builds.</span></span> <span data-ttu-id="fb28f-144">Le code PIN hérite directement de **CSourceSeeking**. le deuxième paramètre est donc un pointeur vers lui-même, casté en pointeur [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) .</span><span class="sxs-lookup"><span data-stu-id="fb28f-144">The pin directly inherits **CSourceSeeking**, so the second parameter is a pointer to itself, cast to an [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) pointer.</span></span> <span data-ttu-id="fb28f-145">La valeur **HRESULT** est ignorée dans la version actuelle des classes de base ; Il reste pour la compatibilité avec les versions précédentes.</span><span class="sxs-lookup"><span data-stu-id="fb28f-145">The **HRESULT** value is ignored in the current version of the base classes; it remains for compatibility with previous versions.</span></span> <span data-ttu-id="fb28f-146">La section critique protège les données partagées, telles que l’heure de début, l’heure d’arrêt et la vitesse de lecture actuelles.</span><span class="sxs-lookup"><span data-stu-id="fb28f-146">The critical section protects shared data, such as the current start time, stop time, and playback rate.</span></span>

<span data-ttu-id="fb28f-147">Ajoutez l’instruction suivante à l’intérieur du constructeur [**CSourceSeeking**](csourceseeking.md) :</span><span class="sxs-lookup"><span data-stu-id="fb28f-147">Add the following statement inside the [**CSourceSeeking**](csourceseeking.md) constructor:</span></span>


```C++
m_rtStop = 60 * UNITS;
```



<span data-ttu-id="fb28f-148">La variable *m \_ rtStop* spécifie l’heure d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="fb28f-148">The *m\_rtStop* variable specifies the stop time.</span></span> <span data-ttu-id="fb28f-149">Par défaut, la valeur est \_ I64 \_ Max/2, soit environ 14 600 ans.</span><span class="sxs-lookup"><span data-stu-id="fb28f-149">By default, the value is \_I64\_MAX / 2, which is approximately 14,600 years.</span></span> <span data-ttu-id="fb28f-150">L’instruction précédente la définit sur une durée plus restrictive de 60 secondes.</span><span class="sxs-lookup"><span data-stu-id="fb28f-150">The previous statement sets it to a more conservative 60 seconds.</span></span>

<span data-ttu-id="fb28f-151">Deux variables membres supplémentaires doivent être ajoutées à CBallStream :</span><span class="sxs-lookup"><span data-stu-id="fb28f-151">Two additional member variables must be added to CBallStream:</span></span>


```C++
BOOL            m_bDiscontinuity; // If true, set the discontinuity flag.
REFERENCE_TIME  m_rtBallPosition; // Position of the ball. 
```



<span data-ttu-id="fb28f-152">Après chaque commande Seek, le filtre doit définir l’indicateur discontinu sur l’exemple suivant en appelant [**IMediaSample :: SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity).</span><span class="sxs-lookup"><span data-stu-id="fb28f-152">After every seek command, the filter must set the discontinuity flag on the next sample by calling [**IMediaSample::SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity).</span></span> <span data-ttu-id="fb28f-153">La variable *m \_ bDiscontinuity* effectue le suivi de ce.</span><span class="sxs-lookup"><span data-stu-id="fb28f-153">The *m\_bDiscontinuity* variable will keep track of this.</span></span> <span data-ttu-id="fb28f-154">La variable *m \_ rtBallPosition* spécifie la position de la balle dans le cadre de la vidéo.</span><span class="sxs-lookup"><span data-stu-id="fb28f-154">The *m\_rtBallPosition* variable will specify the position of the ball within the video frame.</span></span> <span data-ttu-id="fb28f-155">Le filtre boule d’origine calcule la position à partir du temps de flux, mais le temps de flux est redéfini à zéro après chaque commande Seek.</span><span class="sxs-lookup"><span data-stu-id="fb28f-155">The original Ball filter calculates the position from the stream time, but the stream time resets to zero after each seek command.</span></span> <span data-ttu-id="fb28f-156">Dans un flux de recherche, la position absolue est indépendante du temps de flux.</span><span class="sxs-lookup"><span data-stu-id="fb28f-156">In a seekable stream, the absolute position is independent of the stream time.</span></span>

### <a name="queryinterface"></a><span data-ttu-id="fb28f-157">QueryInterface</span><span class="sxs-lookup"><span data-stu-id="fb28f-157">QueryInterface</span></span>

<span data-ttu-id="fb28f-158">La classe [**CSourceSeeking**](csourceseeking.md) implémente l’interface [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) .</span><span class="sxs-lookup"><span data-stu-id="fb28f-158">The [**CSourceSeeking**](csourceseeking.md) class implements the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface.</span></span> <span data-ttu-id="fb28f-159">Pour exposer cette interface aux clients, remplacez la méthode [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) :</span><span class="sxs-lookup"><span data-stu-id="fb28f-159">To expose this interface to clients, override the [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) method:</span></span>


```C++
STDMETHODIMP CBallStream::NonDelegatingQueryInterface
    (REFIID riid, void **ppv)
{
    if( riid == IID_IMediaSeeking ) 
    {
        return CSourceSeeking::NonDelegatingQueryInterface( riid, ppv );
    }
    return CSourceStream::NonDelegatingQueryInterface(riid, ppv);
}
```



<span data-ttu-id="fb28f-160">La méthode est appelée « NonDelegating » en raison de la façon dont les classes de base DirectShow prennent en charge l’agrégation COM (Component Object Model).</span><span class="sxs-lookup"><span data-stu-id="fb28f-160">The method is called "NonDelegating" because of the way the DirectShow base classes support Component Object Model (COM) aggregation.</span></span> <span data-ttu-id="fb28f-161">Pour plus d’informations, consultez la rubrique « Comment implémenter IUnknown » dans le kit de développement logiciel (SDK) DirectShow.</span><span class="sxs-lookup"><span data-stu-id="fb28f-161">For more information, see the "How to Implement IUnknown" topic in the DirectShow SDK.</span></span>

### <a name="seeking-methods"></a><span data-ttu-id="fb28f-162">Méthodes de recherche</span><span class="sxs-lookup"><span data-stu-id="fb28f-162">Seeking Methods</span></span>

<span data-ttu-id="fb28f-163">La classe [**CSourceSeeking**](csourceseeking.md) gère plusieurs variables membres relatives à la recherche.</span><span class="sxs-lookup"><span data-stu-id="fb28f-163">The [**CSourceSeeking**](csourceseeking.md) class maintains several member variables relating to seeking.</span></span>



| <span data-ttu-id="fb28f-164">Variable</span><span class="sxs-lookup"><span data-stu-id="fb28f-164">Variable</span></span>          | <span data-ttu-id="fb28f-165">Description</span><span class="sxs-lookup"><span data-stu-id="fb28f-165">Description</span></span>   | <span data-ttu-id="fb28f-166">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="fb28f-166">Default Value</span></span>  |
|-------------------|---------------|----------------|
| <span data-ttu-id="fb28f-167">*m \_ rtStart*</span><span class="sxs-lookup"><span data-stu-id="fb28f-167">*m\_rtStart*</span></span>      | <span data-ttu-id="fb28f-168">Heure de début</span><span class="sxs-lookup"><span data-stu-id="fb28f-168">Start time</span></span>    | <span data-ttu-id="fb28f-169">Zéro</span><span class="sxs-lookup"><span data-stu-id="fb28f-169">Zero</span></span>           |
| <span data-ttu-id="fb28f-170">*m \_ rtStop*</span><span class="sxs-lookup"><span data-stu-id="fb28f-170">*m\_rtStop*</span></span>       | <span data-ttu-id="fb28f-171">Heure d’arrêt</span><span class="sxs-lookup"><span data-stu-id="fb28f-171">Stop time</span></span>     | <span data-ttu-id="fb28f-172">\_I64 \_ Max/2</span><span class="sxs-lookup"><span data-stu-id="fb28f-172">\_I64\_MAX / 2</span></span> |
| <span data-ttu-id="fb28f-173">*m \_ dRateSeeking*</span><span class="sxs-lookup"><span data-stu-id="fb28f-173">*m\_dRateSeeking*</span></span> | <span data-ttu-id="fb28f-174">Vitesse de lecture</span><span class="sxs-lookup"><span data-stu-id="fb28f-174">Playback rate</span></span> | <span data-ttu-id="fb28f-175">1.0</span><span class="sxs-lookup"><span data-stu-id="fb28f-175">1.0</span></span>            |



 

<span data-ttu-id="fb28f-176">L’implémentation [**CSourceSeeking**](csourceseeking.md) de [**IMediaSeeking :: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) met à jour les heures de démarrage et d’arrêt, puis appelle deux méthodes virtuelles pures sur la classe dérivée, [**CSourceSeeking :: modifiez l'**](csourceseeking-changestart.md) et [**CSourceSeeking :: ChangeStop**](csourceseeking-changestop.md).</span><span class="sxs-lookup"><span data-stu-id="fb28f-176">The [**CSourceSeeking**](csourceseeking.md) implementation of [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) updates the start and stop times, and then calls two pure virtual methods on the derived class, [**CSourceSeeking::ChangeStart**](csourceseeking-changestart.md) and [**CSourceSeeking::ChangeStop**](csourceseeking-changestop.md).</span></span> <span data-ttu-id="fb28f-177">L’implémentation de [**IMediaSeeking ::**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) est similaire : elle met à jour la vitesse de lecture, puis appelle la méthode virtuelle pure [**CSourceSeeking :: ChangeRate**](csourceseeking-changerate.md).</span><span class="sxs-lookup"><span data-stu-id="fb28f-177">The implementation of [**IMediaSeeking::SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) is similar: It updates the playback rate and then calls the pure virtual method [**CSourceSeeking::ChangeRate**](csourceseeking-changerate.md).</span></span> <span data-ttu-id="fb28f-178">Dans chacune de ces méthodes virtuelles, le code confidentiel doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="fb28f-178">In each of these virtual methods, the pin must do the following:</span></span>

1.  <span data-ttu-id="fb28f-179">Appelez [**IPIN :: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) pour démarrer le vidage des données.</span><span class="sxs-lookup"><span data-stu-id="fb28f-179">Call [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) to start flushing data.</span></span>
2.  <span data-ttu-id="fb28f-180">Arrêtez le thread de streaming.</span><span class="sxs-lookup"><span data-stu-id="fb28f-180">Halt the streaming thread.</span></span>
3.  <span data-ttu-id="fb28f-181">Appelez [**IPIN :: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush).</span><span class="sxs-lookup"><span data-stu-id="fb28f-181">Call [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush).</span></span>
4.  <span data-ttu-id="fb28f-182">Redémarrez le thread de streaming.</span><span class="sxs-lookup"><span data-stu-id="fb28f-182">Restart the streaming thread.</span></span>
5.  <span data-ttu-id="fb28f-183">Appelez [**IPIN :: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment).</span><span class="sxs-lookup"><span data-stu-id="fb28f-183">Call [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment).</span></span>
6.  <span data-ttu-id="fb28f-184">Définissez l’indicateur de discontinuité sur l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="fb28f-184">Set the discontinuity flag on the next sample.</span></span>

<span data-ttu-id="fb28f-185">L’ordre de ces étapes est essentiel, car le thread de streaming peut se bloquer pendant qu’il attend de remettre un exemple ou d’obtenir un nouvel exemple.</span><span class="sxs-lookup"><span data-stu-id="fb28f-185">The order of these steps is crucial, because the streaming thread can block while it waits to deliver a sample or get a new sample.</span></span> <span data-ttu-id="fb28f-186">La méthode [**BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) garantit que le thread de diffusion en continu n’est pas bloqué et, par conséquent, ne se bloque pas à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="fb28f-186">The [**BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method ensures that the streaming thread is not blocked and therefore will not deadlock in step 2.</span></span> <span data-ttu-id="fb28f-187">L’appel [**EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) informe les filtres en aval qu’ils attendent de nouveaux exemples, donc ils ne les rejettent pas lorsque le thread redémarre à l’étape 4.</span><span class="sxs-lookup"><span data-stu-id="fb28f-187">The [**EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) call informs the downstream filters to expect new samples, so they do not reject them when the thread starts again in step 4.</span></span>

<span data-ttu-id="fb28f-188">La méthode privée suivante effectue les étapes 1 à 4 :</span><span class="sxs-lookup"><span data-stu-id="fb28f-188">The following private method performs steps 1 through 4:</span></span>


```C++
void CBallStream::UpdateFromSeek()
{
    if (ThreadExists()) 
    {
        DeliverBeginFlush();
        // Shut down the thread and stop pushing data.
        Stop();
        DeliverEndFlush();
        // Restart the thread and start pushing data again.
        Pause();
    }
}
```



<span data-ttu-id="fb28f-189">Lorsque le thread de streaming redémarre, il appelle la méthode [**CSourceStream :: OnThreadStartPlay**](csourcestream-onthreadstartplay.md) .</span><span class="sxs-lookup"><span data-stu-id="fb28f-189">When the streaming thread starts again, it calls the [**CSourceStream::OnThreadStartPlay**](csourcestream-onthreadstartplay.md) method.</span></span> <span data-ttu-id="fb28f-190">Remplacez cette méthode pour effectuer les étapes 5 et 6 :</span><span class="sxs-lookup"><span data-stu-id="fb28f-190">Override this method to perform steps 5 and 6:</span></span>


```C++
HRESULT CBallStream::OnThreadStartPlay()
{
    m_bDiscontinuity = TRUE;
    return DeliverNewSegment(m_rtStart, m_rtStop, m_dRateSeeking);
}
```



<span data-ttu-id="fb28f-191">Dans la méthode [**Modifiez l'**](csourceseeking-changestart.md) , définissez le temps de flux sur zéro et la position de la balle sur la nouvelle heure de début.</span><span class="sxs-lookup"><span data-stu-id="fb28f-191">In the [**ChangeStart**](csourceseeking-changestart.md) method, set the stream time to zero and the position of the ball to the new start time.</span></span> <span data-ttu-id="fb28f-192">Appelez ensuite CBallStream :: UpdateFromSeek :</span><span class="sxs-lookup"><span data-stu-id="fb28f-192">Then call CBallStream::UpdateFromSeek:</span></span>


```C++
HRESULT CBallStream::ChangeStart( )
{
    {
        CAutoLock lock(CSourceSeeking::m_pLock);
        m_rtSampleTime = 0;
        m_rtBallPosition = m_rtStart;
    }
    UpdateFromSeek();
    return S_OK;
}
```



<span data-ttu-id="fb28f-193">Dans la méthode [**ChangeStop**](csourceseeking-changestop.md) , appelez CBallStream :: UpdateFromSeek si la nouvelle heure d’arrêt est inférieure à la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="fb28f-193">In the [**ChangeStop**](csourceseeking-changestop.md) method, call CBallStream::UpdateFromSeek if the new stop time is less than the current position.</span></span> <span data-ttu-id="fb28f-194">Dans le cas contraire, l’heure d’arrêt est toujours à l’avenir, il n’est donc pas nécessaire de vider le graphique.</span><span class="sxs-lookup"><span data-stu-id="fb28f-194">Otherwise, the stop time is still in the future, so there's no need to flush the graph.</span></span>


```C++
HRESULT CBallStream::ChangeStop( )
{
    {
        CAutoLock lock(CSourceSeeking::m_pLock);
        if (m_rtBallPosition < m_rtStop)
        {
            return S_OK;
        }
    }

    // We're already past the new stop time. Flush the graph.
    UpdateFromSeek();
    return S_OK;
}
```



<span data-ttu-id="fb28f-195">Pour les changements de taux, la méthode [**CSourceSeeking ::**](csourceseeking-setrate.md) se, définit *m \_ dRateSeeking* sur le nouveau taux (en ignorant l’ancienne valeur) avant d’appeler [**ChangeRate**](csourceseeking-changerate.md).</span><span class="sxs-lookup"><span data-stu-id="fb28f-195">For rate changes, the [**CSourceSeeking::SetRate**](csourceseeking-setrate.md) method sets *m\_dRateSeeking* to the new rate (discarding the old value) before it calls [**ChangeRate**](csourceseeking-changerate.md).</span></span> <span data-ttu-id="fb28f-196">Malheureusement, si l’appelant a donné un taux non valide (par exemple, inférieur à zéro), il est trop tard au moment de l’appel de **ChangeRate** .</span><span class="sxs-lookup"><span data-stu-id="fb28f-196">Unfortunately, if the caller gave an invalid rate—for example, less than zero—it's too late by the time **ChangeRate** is called.</span></span> <span data-ttu-id="fb28f-197">Une solution consiste à remplacer seet à **vérifier les taux** valides :</span><span class="sxs-lookup"><span data-stu-id="fb28f-197">One solution is to override **SetRate** and check for valid rates:</span></span>


```C++
HRESULT CBallStream::SetRate(double dRate)
{
    if (dRate <= 1.0)
    {
        return E_INVALIDARG;
    }
    {
        CAutoLock lock(CSourceSeeking::m_pLock);
        m_dRateSeeking = dRate;
    }
    UpdateFromSeek();
    return S_OK;
}
// Now ChangeRate won't ever be called, but it's pure virtual, so it needs
// a dummy implementation.
HRESULT CBallStream::ChangeRate() { return S_OK; }
```



### <a name="drawing-in-the-buffer"></a><span data-ttu-id="fb28f-198">Dessin dans la mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="fb28f-198">Drawing in the Buffer</span></span>

<span data-ttu-id="fb28f-199">Voici la version modifiée de [**CSourceStream :: FillBuffer**](csourcestream-fillbuffer.md), la routine qui dessine la balle sur chaque image :</span><span class="sxs-lookup"><span data-stu-id="fb28f-199">Here is the modified version of [**CSourceStream::FillBuffer**](csourcestream-fillbuffer.md), the routine that draws the ball on each frame:</span></span>


```C++
HRESULT CBallStream::FillBuffer(IMediaSample *pMediaSample)
{
    BYTE *pData;
    long lDataLen;
    pMediaSample->GetPointer(&pData);
    lDataLen = pMediaSample->GetSize();
    {
        CAutoLock cAutoLockShared(&m_cSharedState);
        if (m_rtBallPosition >= m_rtStop) 
        {
            // End of the stream.
            return S_FALSE;
        }
        // Draw the ball in its current position.
        ZeroMemory( pData, lDataLen );
        m_Ball->MoveBall(m_rtBallPosition);
        m_Ball->PlotBall(pData, m_BallPixel, m_iPixelSize);
        
        // The sample times are modified by the current rate.
        REFERENCE_TIME rtStart, rtStop;
        rtStart = static_cast<REFERENCE_TIME>(
                      m_rtSampleTime / m_dRateSeeking);
        rtStop  = rtStart + static_cast<int>(
                      m_iRepeatTime / m_dRateSeeking);
        pMediaSample->SetTime(&rtStart, &rtStop);

        // Increment for the next loop.
        m_rtSampleTime += m_iRepeatTime;
        m_rtBallPosition += m_iRepeatTime;
    }
    pMediaSample->SetSyncPoint(TRUE);
    if (m_bDiscontinuity) 
    {
        pMediaSample->SetDiscontinuity(TRUE);
        m_bDiscontinuity = FALSE;
    }
    return NOERROR;
}
```



<span data-ttu-id="fb28f-200">Les principales différences entre cette version et l’original sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="fb28f-200">The major differences between this version and the original are the following:</span></span>

-   <span data-ttu-id="fb28f-201">Comme indiqué précédemment, la variable *m \_ rtBallPosition* est utilisée pour définir la position de la balle, plutôt que le temps de flux.</span><span class="sxs-lookup"><span data-stu-id="fb28f-201">As mentioned earlier, the *m\_rtBallPosition* variable is used to set the position of the ball, rather than the stream time.</span></span>
-   <span data-ttu-id="fb28f-202">Après avoir appuyé sur la section critique, la méthode vérifie si la position actuelle dépasse l’heure d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="fb28f-202">After holding the critical section, the method checks whether the current position exceeds the stop time.</span></span> <span data-ttu-id="fb28f-203">Si c’est le cas, elle retourne **S \_ false**, ce qui indique à la classe de base d’arrêter l’envoi de données et de fournir une notification de fin de flux.</span><span class="sxs-lookup"><span data-stu-id="fb28f-203">If so, it returns **S\_FALSE**, which signals the base class to stop sending data and deliver an end-of-stream notification.</span></span>
-   <span data-ttu-id="fb28f-204">Les horodatages sont divisés par le taux actuel.</span><span class="sxs-lookup"><span data-stu-id="fb28f-204">The time stamps are divided by the current rate.</span></span>
-   <span data-ttu-id="fb28f-205">Si *m \_ bDiscontinuity* a la **valeur true**, la méthode définit l’indicateur de discontinuité sur l’exemple.</span><span class="sxs-lookup"><span data-stu-id="fb28f-205">If *m\_bDiscontinuity* is **TRUE**, the method sets the discontinuity flag on the sample.</span></span>

<span data-ttu-id="fb28f-206">Il existe une autre différence mineure.</span><span class="sxs-lookup"><span data-stu-id="fb28f-206">There is another minor difference.</span></span> <span data-ttu-id="fb28f-207">Étant donné que la version d’origine s’appuie sur un seul tampon, elle remplit la totalité de la mémoire tampon avec des zéros une fois, au début de la diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="fb28f-207">Because the original version relies on having exactly one buffer, it fills the entire buffer with zeroes once, when streaming begins.</span></span> <span data-ttu-id="fb28f-208">Après cela, il efface simplement la balle de sa position précédente.</span><span class="sxs-lookup"><span data-stu-id="fb28f-208">After that, it just erases the ball from its previous position.</span></span> <span data-ttu-id="fb28f-209">Toutefois, cette optimisation révèle un léger bogue dans le filtre balle.</span><span class="sxs-lookup"><span data-stu-id="fb28f-209">However, this optimization reveals a slight bug in the Ball filter.</span></span> <span data-ttu-id="fb28f-210">Lorsque la méthode [**CBaseOutputPin ::D ecideallocator**](cbaseoutputpin-decideallocator.md) appelle [**IMemInputPin :: NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator), elle affecte à l’indicateur de lecture seule la **valeur false**.</span><span class="sxs-lookup"><span data-stu-id="fb28f-210">When the [**CBaseOutputPin::DecideAllocator**](cbaseoutputpin-decideallocator.md) method calls [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator), it sets the read-only flag to **FALSE**.</span></span> <span data-ttu-id="fb28f-211">Par conséquent, le filtre en aval est libre d’écrire sur la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="fb28f-211">As a result, the downstream filter is free to write on the buffer.</span></span> <span data-ttu-id="fb28f-212">Une solution consiste à remplacer **DecideAllocator** afin qu’il affecte à l’indicateur de lecture seule la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="fb28f-212">One solution is to override **DecideAllocator** so that it sets the read-only flag to **TRUE**.</span></span> <span data-ttu-id="fb28f-213">Toutefois, pour des raisons de simplicité, la nouvelle version supprime tout simplement l’optimisation.</span><span class="sxs-lookup"><span data-stu-id="fb28f-213">For simplicity, however, the new version simply removes the optimization altogether.</span></span> <span data-ttu-id="fb28f-214">Au lieu de cela, cette version remplit la mémoire tampon avec des zéros à chaque fois.</span><span class="sxs-lookup"><span data-stu-id="fb28f-214">Instead, this version fills the buffer with zeroes each time.</span></span>

### <a name="miscellaneous-changes"></a><span data-ttu-id="fb28f-215">Modifications diverses</span><span class="sxs-lookup"><span data-stu-id="fb28f-215">Miscellaneous Changes</span></span>

<span data-ttu-id="fb28f-216">Dans la nouvelle version, ces deux lignes sont supprimées du constructeur CBall :</span><span class="sxs-lookup"><span data-stu-id="fb28f-216">In the new version, these two lines are removed from the CBall constructor:</span></span>


```C++
    m_iRandX = rand();
    m_iRandY = rand();
```



<span data-ttu-id="fb28f-217">Le filtre boule d’origine utilise ces valeurs pour ajouter du caractère aléatoire à la position initiale de la balle.</span><span class="sxs-lookup"><span data-stu-id="fb28f-217">The original Ball filter uses these values to add some randomness to the initial ball position.</span></span> <span data-ttu-id="fb28f-218">Dans le cadre de nos objectifs, nous voulons que la balle soit déterministe.</span><span class="sxs-lookup"><span data-stu-id="fb28f-218">For our purposes, we want the ball to be deterministic.</span></span> <span data-ttu-id="fb28f-219">En outre, certaines variables ont été modifiées des objets [**CRefTime**](creftime.md) en variables de [**\_ temps de référence**](reference-time.md) .</span><span class="sxs-lookup"><span data-stu-id="fb28f-219">Also, some variables have been changed from [**CRefTime**](creftime.md) objects to [**REFERENCE\_TIME**](reference-time.md) variables.</span></span> <span data-ttu-id="fb28f-220">(La classe **CRefTime** est un wrapper léger pour une valeur de **\_ temps de référence** .) Enfin, l’implémentation de [**IQualityControl :: Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) a été légèrement modifiée. vous pouvez consulter le code source pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="fb28f-220">(The **CRefTime** class is a thin wrapper for a **REFERENCE\_TIME** value.) Lastly, the implementation of [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) has been modified slightly; you can refer to the source code for details.</span></span>

## <a name="limitations-of-the-csourceseeking-class"></a><span data-ttu-id="fb28f-221">Limitations de la classe CSourceSeeking</span><span class="sxs-lookup"><span data-stu-id="fb28f-221">Limitations of the CSourceSeeking Class</span></span>

<span data-ttu-id="fb28f-222">La classe [**CSourceSeeking**](csourceseeking.md) n’est pas destinée aux filtres avec plusieurs broches de sortie, en raison de problèmes de communication entre les broches.</span><span class="sxs-lookup"><span data-stu-id="fb28f-222">The [**CSourceSeeking**](csourceseeking.md) class is not meant for filters with multiple output pins, because of issues with cross-pin communication.</span></span> <span data-ttu-id="fb28f-223">Par exemple, imaginez un filtre d’analyseur qui reçoit un flux audio/vidéo entrelacé, divise le flux en ses composants audio et vidéo et diffuse la vidéo d’une broche de sortie et de l’audio d’une autre.</span><span class="sxs-lookup"><span data-stu-id="fb28f-223">For example, imagine a parser filter that receives an interleaved audio-video stream, splits the stream into its audio and video components, and delivers video from one output pin and audio from another.</span></span> <span data-ttu-id="fb28f-224">Les deux broches de sortie reçoivent chaque commande Seek, mais le filtre ne doit effectuer une recherche qu’une seule fois par commande Seek.</span><span class="sxs-lookup"><span data-stu-id="fb28f-224">Both output pins will receive every seek command, but the filter should seek only once per seek command.</span></span> <span data-ttu-id="fb28f-225">La solution consiste à désigner l’un des codes confidentiels pour contrôler la recherche et à ignorer les commandes de recherche reçues par l’autre code PIN.</span><span class="sxs-lookup"><span data-stu-id="fb28f-225">The solution is to designate one of the pins to control seeking and to ignore seek commands received by the other pin.</span></span>

<span data-ttu-id="fb28f-226">Toutefois, après la commande Seek, les deux codes confidentiels doivent vider les données.</span><span class="sxs-lookup"><span data-stu-id="fb28f-226">After the seek command, however, both pins should flush data.</span></span> <span data-ttu-id="fb28f-227">Pour compliquer davantage les choses, la commande Seek se produit sur le thread d’application, et non sur le thread de streaming.</span><span class="sxs-lookup"><span data-stu-id="fb28f-227">To complicate matters further, the seek command happens on the application thread, not the streaming thread.</span></span> <span data-ttu-id="fb28f-228">Par conséquent, vous devez vous assurer qu’aucun code confidentiel n’est bloqué et qu’il attend qu’un appel [**IMemInputPin :: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) soit retourné, ou qu’il peut provoquer un interblocage.</span><span class="sxs-lookup"><span data-stu-id="fb28f-228">Therefore, you must make certain that neither pin is blocked and waiting for a [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) call to return, or it might cause a deadlock.</span></span> <span data-ttu-id="fb28f-229">Pour plus d’informations sur le vidage thread-safe dans les codes confidentiels, consultez [threads et sections critiques](threads-and-critical-sections.md).</span><span class="sxs-lookup"><span data-stu-id="fb28f-229">For more information about thread-safe flushing in pins, see [Threads and Critical Sections](threads-and-critical-sections.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fb28f-230">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fb28f-230">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb28f-231">Écriture de filtres source</span><span class="sxs-lookup"><span data-stu-id="fb28f-231">Writing Source Filters</span></span>](writing-source-filters.md)
</dt> </dl>

 

 



