---
description: Définition et récupération de la position
ms.assetid: 06b0e2d7-9539-41ad-a631-7e8da556feeb
title: Définition et récupération de la position
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 776a32eb6193ef456d693b5a133c87d800a0b64e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745412"
---
# <a name="setting-and-retrieving-the-position"></a><span data-ttu-id="6198f-103">Définition et récupération de la position</span><span class="sxs-lookup"><span data-stu-id="6198f-103">Setting and Retrieving the Position</span></span>

<span data-ttu-id="6198f-104">Le graphique de filtre conserve deux valeurs de position, la position actuelle et la position d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="6198f-104">The filter graph maintains two position values, current position and stop position.</span></span> <span data-ttu-id="6198f-105">Ceux-ci sont définis comme suit :</span><span class="sxs-lookup"><span data-stu-id="6198f-105">These are defined as follows:</span></span>

-   <span data-ttu-id="6198f-106">Lorsque le graphique est en cours d’exécution, la position actuelle est la position de lecture actuelle, par rapport au début de la source.</span><span class="sxs-lookup"><span data-stu-id="6198f-106">When the graph is running, the current position is the current playback position, relative to the beginning of the source.</span></span> <span data-ttu-id="6198f-107">Lorsque le graphique est arrêté ou suspendu, la position actuelle est le point où la diffusion en continu commence à la prochaine exécution de la commande.</span><span class="sxs-lookup"><span data-stu-id="6198f-107">When the graph is stopped or paused, the current position is the point where streaming will begin on the next run command.</span></span>
-   <span data-ttu-id="6198f-108">La position d’arrêt est le point où le flux se termine.</span><span class="sxs-lookup"><span data-stu-id="6198f-108">The stop position is the point where the stream will end.</span></span> <span data-ttu-id="6198f-109">Lorsque le graphique atteint la position d’arrêt, aucune donnée n’est diffusée en continu, et le gestionnaire de graphique de filtre publie un événement [**ce \_ complet**](ec-complete.md) .</span><span class="sxs-lookup"><span data-stu-id="6198f-109">When the graph reaches the stop position, no more data is streamed, and the filter graph manager posts an [**EC\_COMPLETE**](ec-complete.md) event.</span></span> <span data-ttu-id="6198f-110">(Toutefois, le graphique ne bascule pas automatiquement vers un état arrêté.</span><span class="sxs-lookup"><span data-stu-id="6198f-110">(The graph does not automatically switch to a stopped state, however.</span></span> <span data-ttu-id="6198f-111">Pour plus d’informations, consultez [réponse aux événements](responding-to-events.md).)</span><span class="sxs-lookup"><span data-stu-id="6198f-111">For more information, see [Responding to Events](responding-to-events.md).)</span></span>

<span data-ttu-id="6198f-112">Pour récupérer ces valeurs, appelez la méthode [**IMediaSeeking :: GetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) .</span><span class="sxs-lookup"><span data-stu-id="6198f-112">To retrieve these values, call the [**IMediaSeeking::GetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) method.</span></span> <span data-ttu-id="6198f-113">Les valeurs retournées sont toujours relatives à la source du média d’origine.</span><span class="sxs-lookup"><span data-stu-id="6198f-113">The returned values are always relative to the original media source.</span></span> <span data-ttu-id="6198f-114">Par défaut, les valeurs sont en unités de temps de référence.</span><span class="sxs-lookup"><span data-stu-id="6198f-114">By default, the values are in reference time units.</span></span> <span data-ttu-id="6198f-115">Dans certains cas, vous pouvez modifier les unités de temps. Pour plus d’informations, consultez [formats d’heure pour les commandes de recherche](time-formats-for-seek-commands.md).</span><span class="sxs-lookup"><span data-stu-id="6198f-115">In some cases, you can change the time units; for more information, see [Time Formats For Seek Commands](time-formats-for-seek-commands.md).</span></span>

<span data-ttu-id="6198f-116">Pour rechercher une nouvelle position ou définir une nouvelle position d’arrêt, appelez la méthode [**IMediaSeeking :: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) , comme indiqué dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="6198f-116">To seek to a new position or set a new stop position, call the [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) method, as shown in the following example:</span></span>


```C++
#define ONE_SECOND 10000000
REFERENCE_TIME rtNow  = 2 * ONE_SECOND, 
               rtStop = 5 * ONE_SECOND;

hr = pSeek->SetPositions(
    &rtNow,  AM_SEEKING_AbsolutePositioning, 
    &rtStop, AM_SEEKING_AbsolutePositioning
    );
```



> [!Note]  
> <span data-ttu-id="6198f-117">Une seconde est 10 millions unités de temps de référence.</span><span class="sxs-lookup"><span data-stu-id="6198f-117">One second is 10,000,000 units of reference time.</span></span> <span data-ttu-id="6198f-118">Pour plus de commodité, l’exemple définit cette valeur comme une \_ seconde.</span><span class="sxs-lookup"><span data-stu-id="6198f-118">For convenience, the example defines this value as ONE\_SECOND.</span></span> <span data-ttu-id="6198f-119">Si vous utilisez la bibliothèque de classes de base DirectShow, les unités constantes ont la même valeur.</span><span class="sxs-lookup"><span data-stu-id="6198f-119">If you are using the DirectShow base-class library, the constant UNITS has the same value.</span></span>

 

<span data-ttu-id="6198f-120">Le paramètre *rtNow* spécifie la nouvelle position actuelle.</span><span class="sxs-lookup"><span data-stu-id="6198f-120">The *rtNow* parameter specifies the new current position.</span></span> <span data-ttu-id="6198f-121">Le deuxième paramètre est un indicateur qui définit comment interpréter *rtNow*.</span><span class="sxs-lookup"><span data-stu-id="6198f-121">The second parameter is a flag that defines how to interpret *rtNow*.</span></span> <span data-ttu-id="6198f-122">Dans cet exemple, l' \_ indicateur AM recherché \_ AbsolutePositioning indique que *rtNow* spécifie une position absolue dans la source.</span><span class="sxs-lookup"><span data-stu-id="6198f-122">In this example, the AM\_SEEKING\_AbsolutePositioning flag indicates that *rtNow* specifies an absolute position in the source.</span></span> <span data-ttu-id="6198f-123">Par conséquent, le graphique de filtre effectue une recherche sur une position de deux secondes à partir du début du flux.</span><span class="sxs-lookup"><span data-stu-id="6198f-123">Therefore, the filter graph will seek to a position two seconds from the start of the stream.</span></span> <span data-ttu-id="6198f-124">Le paramètre *rtStop* indique l’heure d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="6198f-124">The *rtStop* parameter gives the stop time.</span></span> <span data-ttu-id="6198f-125">Le dernier paramètre spécifie que *rtStop* est également une position absolue.</span><span class="sxs-lookup"><span data-stu-id="6198f-125">The last parameter specifies that *rtStop* is also an absolute position.</span></span>

<span data-ttu-id="6198f-126">Pour spécifier une position par rapport à la valeur de position précédente, utilisez l' \_ indicateur AM recherché \_ RelativePositioning.</span><span class="sxs-lookup"><span data-stu-id="6198f-126">To specify a position relative to the previous position value, use the AM\_SEEKING\_RelativePositioning flag.</span></span> <span data-ttu-id="6198f-127">Pour ne pas modifier l’une des valeurs de position, utilisez l' \_ indicateur AM recherché \_ noposition.</span><span class="sxs-lookup"><span data-stu-id="6198f-127">To leave one of the position values unchanged, use the AM\_SEEKING\_NoPositioning flag.</span></span> <span data-ttu-id="6198f-128">Dans ce cas, le paramètre de temps correspondant peut avoir la **valeur null** .</span><span class="sxs-lookup"><span data-stu-id="6198f-128">The corresponding time parameter can be **NULL** in that case.</span></span> <span data-ttu-id="6198f-129">L’exemple suivant recherche par progression de 10 secondes, mais laisse la position d’arrêt inchangée :</span><span class="sxs-lookup"><span data-stu-id="6198f-129">The following example seeks forward by 10 seconds but leaves the stop position unchanged:</span></span>


```C++
REFERENCE_TIME rtNow = 10 * ONE_SECOND;
hr = pSeek->SetPositions(
    &rtNow, AM_SEEKING_RelativePositioning, 
    NULL, AM_SEEKING_NoPositioning
    );
```



<span data-ttu-id="6198f-130">Si le graphique de filtre est arrêté, le convertisseur vidéo ne met pas à jour l’image après une opération de recherche.</span><span class="sxs-lookup"><span data-stu-id="6198f-130">If the filter graph is stopped, the video renderer does not update the image after a seek operation.</span></span> <span data-ttu-id="6198f-131">Pour l’utilisateur, il apparaît comme si la recherche ne s’est pas déproduite.</span><span class="sxs-lookup"><span data-stu-id="6198f-131">To the user, it will appear as if the seek did not happen.</span></span> <span data-ttu-id="6198f-132">Pour mettre à jour l’image, suspendez le graphique après l’opération de recherche.</span><span class="sxs-lookup"><span data-stu-id="6198f-132">To update the image, pause the graph after the seek operation.</span></span> <span data-ttu-id="6198f-133">La suspension du graphique signale une nouvelle image vidéo pour le convertisseur vidéo.</span><span class="sxs-lookup"><span data-stu-id="6198f-133">Pausing the graph cues a new video frame for the video renderer.</span></span> <span data-ttu-id="6198f-134">Vous pouvez utiliser la méthode [**IMediaControl :: StopWhenReady**](/windows/desktop/api/Control/nf-control-imediacontrol-stopwhenready) , qui suspend le graphique, puis l’arrête.</span><span class="sxs-lookup"><span data-stu-id="6198f-134">You can use the [**IMediaControl::StopWhenReady**](/windows/desktop/api/Control/nf-control-imediacontrol-stopwhenready) method, which pauses the graph and then stops it.</span></span>

 

 



