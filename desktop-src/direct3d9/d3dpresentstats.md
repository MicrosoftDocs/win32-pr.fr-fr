---
description: Décrit les statistiques utilise permutation relatives aux appels PresentEx.
ms.assetid: aa100b83-6fbf-442d-9891-7fc034a5b1d5
title: Structure D3DPRESENTSTATS (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPRESENTSTATS
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b49a589fa1702f61e5a5daef806a5b36d464d0ec
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211814"
---
# <a name="d3dpresentstats-structure"></a><span data-ttu-id="b52f5-103">D3DPRESENTSTATS, structure</span><span class="sxs-lookup"><span data-stu-id="b52f5-103">D3DPRESENTSTATS structure</span></span>

<span data-ttu-id="b52f5-104">Décrit les statistiques utilise permutation relatives aux appels [**PresentEx**](/windows/win32/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) .</span><span class="sxs-lookup"><span data-stu-id="b52f5-104">Describes swapchain statistics relating to [**PresentEx**](/windows/win32/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) calls.</span></span>

## <a name="syntax"></a><span data-ttu-id="b52f5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b52f5-105">Syntax</span></span>


```C++
typedef struct _D3DPRESENTSTATS {
  UINT          PresentCount;
  UINT          PresentRefreshCount;
  UINT          SyncRefreshCount;
  LARGE_INTEGER SyncQPCTime;
  LARGE_INTEGER SyncGPUTime;
} D3DPRESENTSTATS;
```



## <a name="members"></a><span data-ttu-id="b52f5-106">Membres</span><span class="sxs-lookup"><span data-stu-id="b52f5-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b52f5-107">**PresentCount**</span><span class="sxs-lookup"><span data-stu-id="b52f5-107">**PresentCount**</span></span>
</dt> <dd>

<span data-ttu-id="b52f5-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b52f5-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b52f5-109">Nombre d’appels de présentation réussis effectués par un périphérique d’affichage qui est actuellement en cours de génération sur l’écran.</span><span class="sxs-lookup"><span data-stu-id="b52f5-109">Running count of successful Present calls made by a display device that is currently outputting to screen.</span></span> <span data-ttu-id="b52f5-110">Ce paramètre est véritablement l’ID actuel du dernier appel présent et n’est pas nécessairement le nombre total d’appels d’API présents.</span><span class="sxs-lookup"><span data-stu-id="b52f5-110">This parameter is really the Present ID of the last Present call and is not necessarily the total number of Present API calls made.</span></span>

</dd> <dt>

<span data-ttu-id="b52f5-111">**PresentRefreshCount**</span><span class="sxs-lookup"><span data-stu-id="b52f5-111">**PresentRefreshCount**</span></span>
</dt> <dd>

<span data-ttu-id="b52f5-112">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b52f5-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b52f5-113">Le nombre de vblank à partir duquel le dernier a été affiché à l’écran, le nombre de vblank incrémente une fois tous les vblank intervalle.</span><span class="sxs-lookup"><span data-stu-id="b52f5-113">The vblank count at which the last Present was displayed on screen, the vblank count increments once every vblank interval.</span></span>

</dd> <dt>

<span data-ttu-id="b52f5-114">**SyncRefreshCount**</span><span class="sxs-lookup"><span data-stu-id="b52f5-114">**SyncRefreshCount**</span></span>
</dt> <dd>

<span data-ttu-id="b52f5-115">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b52f5-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b52f5-116">Le nombre de vblank lorsque le planificateur a échantillonné l’heure de la machine en appelant QueryPerformanceCounter.</span><span class="sxs-lookup"><span data-stu-id="b52f5-116">The vblank count when the scheduler last sampled the machine time by calling QueryPerformanceCounter.</span></span>

</dd> <dt>

<span data-ttu-id="b52f5-117">**SyncQPCTime**</span><span class="sxs-lookup"><span data-stu-id="b52f5-117">**SyncQPCTime**</span></span>
</dt> <dd>

<span data-ttu-id="b52f5-118">Type : **[ **\_ entier long**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**</span><span class="sxs-lookup"><span data-stu-id="b52f5-118">Type: **[**LARGE\_INTEGER**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**</span></span>

</dd> <dd>

<span data-ttu-id="b52f5-119">Heure de la dernière machine échantillonnée du planificateur, obtenue en appelant [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span><span class="sxs-lookup"><span data-stu-id="b52f5-119">The scheduler's last sampled machine time, obtained by calling [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span>

</dd> <dt>

<span data-ttu-id="b52f5-120">**SyncGPUTime**</span><span class="sxs-lookup"><span data-stu-id="b52f5-120">**SyncGPUTime**</span></span>
</dt> <dd>

<span data-ttu-id="b52f5-121">Type : **[ **\_ entier long**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**</span><span class="sxs-lookup"><span data-stu-id="b52f5-121">Type: **[**LARGE\_INTEGER**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**</span></span>

</dd> <dd>

<span data-ttu-id="b52f5-122">Cette valeur n'est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="b52f5-122">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b52f5-123">Notes</span><span class="sxs-lookup"><span data-stu-id="b52f5-123">Remarks</span></span>

<span data-ttu-id="b52f5-124">Quand une application 9Ex adopte le mode Flip (D3DSWAPEFFECT \_ FLIPEX), les applications peuvent détecter la suppression de frame en appelant GetPresentStatistics à tout moment.</span><span class="sxs-lookup"><span data-stu-id="b52f5-124">When a 9Ex application adopts Flip Mode present (D3DSWAPEFFECT\_FLIPEX), applications can detect frame dropping by calling GetPresentStatistics at any point in time.</span></span> <span data-ttu-id="b52f5-125">En effet, ils peuvent effectuer les opérations suivantes.</span><span class="sxs-lookup"><span data-stu-id="b52f5-125">In effect, they can do the following.</span></span>

1.  <span data-ttu-id="b52f5-126">Rendre sur la mémoire tampon d’arrière-plan</span><span class="sxs-lookup"><span data-stu-id="b52f5-126">Render to the back buffer</span></span>
2.  <span data-ttu-id="b52f5-127">Appel présent</span><span class="sxs-lookup"><span data-stu-id="b52f5-127">Call Present</span></span>
3.  <span data-ttu-id="b52f5-128">Appeler GetPresentStats et stocker la structure D3DPRESENTSTATS obtenue</span><span class="sxs-lookup"><span data-stu-id="b52f5-128">Call GetPresentStats and store the resulting D3DPRESENTSTATS structure</span></span>
4.  <span data-ttu-id="b52f5-129">Restituer le frame suivant à la mémoire tampon d’arrière-plan</span><span class="sxs-lookup"><span data-stu-id="b52f5-129">Render the next frame to the back buffer</span></span>
5.  <span data-ttu-id="b52f5-130">Appel présent</span><span class="sxs-lookup"><span data-stu-id="b52f5-130">Call Present</span></span>
6.  <span data-ttu-id="b52f5-131">Répétez les étapes 4 et 5 1 ou plus.</span><span class="sxs-lookup"><span data-stu-id="b52f5-131">Repeat steps 4 and 5 one or more times</span></span>
7.  <span data-ttu-id="b52f5-132">Appeler GetPresentStats et stocker la structure D3DPRESENTSTATS obtenue</span><span class="sxs-lookup"><span data-stu-id="b52f5-132">Call GetPresentStats and store the resulting D3DPRESENTSTATS structure</span></span>
8.  <span data-ttu-id="b52f5-133">Comparez les valeurs de PresentRefreshCount à partir des deux structures D3DPRESENTSTATS stockées.</span><span class="sxs-lookup"><span data-stu-id="b52f5-133">Compare the values of PresentRefreshCount from the two stored D3DPRESENTSTATS structures.</span></span> <span data-ttu-id="b52f5-134">L’application peut calculer le PresentRefreshCount correspondant d’un paramètre PresentCount particulier en fonction des hypothèses de l’incrémentation de PresentRefreshCount et de l’assignation PresentCount des images présentées.</span><span class="sxs-lookup"><span data-stu-id="b52f5-134">The application can calculate the corresponding PresentRefreshCount of a particular PresentCount parameter based on the assumptions of PresentRefreshCount increment and PresentCount assignment of frame presents.</span></span> <span data-ttu-id="b52f5-135">Si le dernier échantillonné PresentRefreshCount ne correspond pas au PresentCount (par exemple, si le PresentRefreshCount a été incrémenté mais que PresentCount n’en a pas, il y avait un abandon d’image).</span><span class="sxs-lookup"><span data-stu-id="b52f5-135">If the PresentRefreshCount last sampled does not match the PresentCount (i.e. if the PresentRefreshCount has incremented but PresentCount has not, then there was frame dropping.)</span></span>

<span data-ttu-id="b52f5-136">Les applications peuvent déterminer si un frame a été supprimé en échantillonnant deux instances de PresentCount et GetPresentStats (en appelant l’API GetPresentStats à deux points quelconques dans le temps).</span><span class="sxs-lookup"><span data-stu-id="b52f5-136">Applications can determine whether a frame has been dropped by sampling any two instances of PresentCount and GetPresentStats (by calling GetPresentStats API at any two points in time).</span></span> <span data-ttu-id="b52f5-137">Par exemple, une application multimédia qui présente le même taux de fréquence d’actualisation du moniteur (par exemple, le taux de rafraîchissement de l’analyse est 60 Hz, l’application présente une trame toutes les 1/60 secondes) veut présenter les images A, B, C, D, E, chacune correspondant aux ID de présentation (PresentCount) 1, 2, 3, 7, 8.</span><span class="sxs-lookup"><span data-stu-id="b52f5-137">For example, a media application that is presenting at the same rate as the monitor refresh rate (for example, monitor refresh rate is 60Hz, the application presents a frame every 1/60 seconds) wants to present frames A, B, C, D, E, each corresponding to Present IDs (PresentCount) 1, 2, 3, 7, 8.</span></span>

<span data-ttu-id="b52f5-138">Le code d’application ressemble à la séquence suivante.</span><span class="sxs-lookup"><span data-stu-id="b52f5-138">The application code looks like the following sequence.</span></span>

1.  <span data-ttu-id="b52f5-139">Restituer le frame A à la mémoire tampon d’arrière-plan</span><span class="sxs-lookup"><span data-stu-id="b52f5-139">Render frame A to the back buffer</span></span>
2.  <span data-ttu-id="b52f5-140">Appel présent, PresentCount = 1</span><span class="sxs-lookup"><span data-stu-id="b52f5-140">Call Present, PresentCount = 1</span></span>
3.  <span data-ttu-id="b52f5-141">Appeler GetPresentStats et stocker la structure D3DPRESENTSTATS obtenue</span><span class="sxs-lookup"><span data-stu-id="b52f5-141">Call GetPresentStats and store the resulting D3DPRESENTSTATS structure</span></span>
4.  <span data-ttu-id="b52f5-142">Restituer les 4 frames suivants, B, C, D, E, respectivement</span><span class="sxs-lookup"><span data-stu-id="b52f5-142">Render the next 4 frames, B, C, D, E, respectively</span></span>
5.  <span data-ttu-id="b52f5-143">Appel présent 4 fois, PresentCounts = 2, 3, 7, 8, respectivement</span><span class="sxs-lookup"><span data-stu-id="b52f5-143">Call Present 4 times, PresentCounts = 2, 3, 7, 8, respectively</span></span>
6.  <span data-ttu-id="b52f5-144">Appeler GetPresentStats et stocker la structure D3DPRESENTSTATS obtenue</span><span class="sxs-lookup"><span data-stu-id="b52f5-144">Call GetPresentStats and store the resulting D3DPRESENTSTATS structure</span></span>
7.  <span data-ttu-id="b52f5-145">Comparez les valeurs de PresentRefreshCount à partir des deux structures D3DPRESENTSTATS stockées.</span><span class="sxs-lookup"><span data-stu-id="b52f5-145">Compare the values of PresentRefreshCount from the two stored D3DPRESENTSTATS structures.</span></span> <span data-ttu-id="b52f5-146">Si la différence est 2, par exemple, 2 intervalles vblank se sont écoulés entre les deux appels de l’API GetPresentStats, alors la dernière trame présente doit être Frame C. Étant donné que l’application présente un intervalle très vblank (taux d’actualisation de l’analyse), le temps écoulé entre le moment où la trame A est présentée et le moment où la trame C est présentée doit être 2 vblanks.</span><span class="sxs-lookup"><span data-stu-id="b52f5-146">If the difference is 2, i.e. 2 vblank intervals has elapsed between the two GetPresentStats API calls, then the last presented frame should be frame C. Because the application presents once very vblank interval (the refresh rate of the monitor), the time elapsed between when frame A is presented and when frame C is presented should be 2 vblanks.</span></span>
8.  <span data-ttu-id="b52f5-147">Comparez les valeurs de PresentCount à partir des deux structures D3DPRESENTSTATS stockées.</span><span class="sxs-lookup"><span data-stu-id="b52f5-147">Compare the values of PresentCount from the two stored D3DPRESENTSTATS structures.</span></span> <span data-ttu-id="b52f5-148">Si le premier PresentCount est 1 (correspondant au frame A) et que le deuxième PresentCount est 3 (correspondant à l’image C), aucun cadre n’a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="b52f5-148">If the first PresentCount is 1 (corresponding to frame A) and the second PresentCount is 3 (corresponding to frame C), then no frames have been dropped.</span></span> <span data-ttu-id="b52f5-149">Si le deuxième PresentCount est 3, ce qui correspond au frame D, l’application sait qu’une image a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="b52f5-149">If the second PresentCount is 3, which corresponds to frame D, then the application knows that one frame has been dropped.</span></span>

<span data-ttu-id="b52f5-150">Notez que GetPresentStatistics sera traité après son appel, quel que soit l’état du mode FLIPEX appels PresentEx.</span><span class="sxs-lookup"><span data-stu-id="b52f5-150">Note that GetPresentStatistics will be processed after it is called, regardless of the state of FLIPEX mode PresentEx calls.</span></span>

<span data-ttu-id="b52f5-151">**Windows Vista :** Les appels présents seront mis en file d’attente, puis traités avant que l’appel GetPresentStats ne soit traité.</span><span class="sxs-lookup"><span data-stu-id="b52f5-151">**Windows Vista:** The Present calls will be queued and then processed before GetPresentStats call will be processed.</span></span>

<span data-ttu-id="b52f5-152">Quand une application détecte que la présentation de certains cadres est en arrière-plan, elle peut ignorer ces frames et corriger la présentation pour la resynchronisation avec vblank.</span><span class="sxs-lookup"><span data-stu-id="b52f5-152">When an application detects that the presentation of certain frames are behind, it can skip those frames and correct the presentation to re-synchronize with the vblank.</span></span> <span data-ttu-id="b52f5-153">Pour ce faire, une application peut simplement ne pas restituer les images tardives et démarrer le rendu avec la prochaine image correcte dans la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="b52f5-153">To do this, an application can simply not render the late frames and start rendering with the next correct frame in the queue.</span></span> <span data-ttu-id="b52f5-154">Toutefois, si une application a déjà démarré le rendu des frames tardifs, elle peut utiliser un nouveau paramètre present dans D3D9Ex appelé D3DPRESENT \_ FORCEIMMEDIATE.</span><span class="sxs-lookup"><span data-stu-id="b52f5-154">However, if an application has already started the rendering of late frames, it can use a new Present parameter in D3D9Ex called D3DPRESENT\_FORCEIMMEDIATE.</span></span> <span data-ttu-id="b52f5-155">L’indicateur est passé dans les paramètres de l’appel de l’API présent et indique au runtime que le frame sera traité immédiatement dans l’intervalle de vblank suivant, qui n’est pas visible à l’écran.</span><span class="sxs-lookup"><span data-stu-id="b52f5-155">The flag will be passed in the parameters of Present API call and indicates to the runtime that the frame will be processed immediately within the next vblank interval, effectively not visible on screen at all.</span></span> <span data-ttu-id="b52f5-156">Voici l’exemple d’utilisation de l’application après la dernière étape de l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="b52f5-156">Here is the application usage example after the last step in the previous example.</span></span>

1.  <span data-ttu-id="b52f5-157">Restituer le frame suivant à la mémoire tampon d’arrière-plan</span><span class="sxs-lookup"><span data-stu-id="b52f5-157">Render the next frame to the back buffer</span></span>
2.  <span data-ttu-id="b52f5-158">Découvrir à partir de PresentRefreshCount que le frame suivant est déjà en retard</span><span class="sxs-lookup"><span data-stu-id="b52f5-158">Discover from PresentRefreshCount that the next frame is already late</span></span>
3.  <span data-ttu-id="b52f5-159">Définir l’intervalle présent sur D3DPRESENT \_ FORCEIMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="b52f5-159">Set Present interval to D3DPRESENT\_FORCEIMMEDIATE</span></span>
4.  <span data-ttu-id="b52f5-160">Appel présent sur le frame suivant</span><span class="sxs-lookup"><span data-stu-id="b52f5-160">Call Present on the next frame</span></span>

<span data-ttu-id="b52f5-161">Les applications peuvent synchroniser les flux vidéo et audio de la même manière, car le comportement de GetPresentStatistics ne change pas dans ce scénario.</span><span class="sxs-lookup"><span data-stu-id="b52f5-161">Applications can synchronize video and audio streams in the same manner because the behavior of GetPresentStatistics does not change in that scenario.</span></span>

<span data-ttu-id="b52f5-162">Le mode de basculement D3D9Ex fournit des informations sur les statistiques des frames aux applications Windows et aux applications 9Ex plein écran.</span><span class="sxs-lookup"><span data-stu-id="b52f5-162">D3D9Ex Flip Mode provides frame statistics information to windowed applications and full screen 9Ex applications.</span></span>

<span data-ttu-id="b52f5-163">**Windows Vista :** Utilisez les API DWM pour récupérer les statistiques actuelles.</span><span class="sxs-lookup"><span data-stu-id="b52f5-163">**Windows Vista:** Use the DWM APIs for retrieving present statistics.</span></span>

<span data-ttu-id="b52f5-164">Lorsque Gestionnaire de fenêtrage est désactivé, les applications du mode fenêtre 9Ex utilisant le mode Flip recevront les informations statistiques de précision limitée.</span><span class="sxs-lookup"><span data-stu-id="b52f5-164">When Desktop Window Manager is turned off, windowed mode 9Ex applications using flip mode will receive present statistics information of limited accuracy.</span></span>

<span data-ttu-id="b52f5-165">\* \* Windows Vista : \* \*</span><span class="sxs-lookup"><span data-stu-id="b52f5-165">\*\*Windows Vista:  \*\*</span></span>

<span data-ttu-id="b52f5-166">Si une application n’est pas assez rapide pour suivre la fréquence d’actualisation du moniteur, peut-être en raison d’un matériel lent ou d’un manque de ressources système, il peut rencontrer un problème graphique.</span><span class="sxs-lookup"><span data-stu-id="b52f5-166">If an application is not fast enough to keep up with the monitor's refresh rate, possibly due to slow hardware or lack of system resources, then it can experience a graphics glitch.</span></span> <span data-ttu-id="b52f5-167">Un problème est appelé Visual contretemps.</span><span class="sxs-lookup"><span data-stu-id="b52f5-167">A glitch is a so-called visual hiccup.</span></span> <span data-ttu-id="b52f5-168">Si une analyse est configurée pour s’actualiser à 60 Hz et que l’application ne peut gérer que 30 fps, la moitié des trames aura des problèmes.</span><span class="sxs-lookup"><span data-stu-id="b52f5-168">If a monitor is set to refresh at 60 Hz, and the application can only manage 30 fps, then half of the frames will have glitches.</span></span>

<span data-ttu-id="b52f5-169">Les applications peuvent détecter un problème en effectuant le suivi de SynchRefreshCount.</span><span class="sxs-lookup"><span data-stu-id="b52f5-169">Applications can detect a glitch by keeping track of SynchRefreshCount.</span></span> <span data-ttu-id="b52f5-170">Par exemple, une application peut exécuter la séquence d’actions suivante.</span><span class="sxs-lookup"><span data-stu-id="b52f5-170">For example, an application might perform the following sequence of actions.</span></span>

1.  <span data-ttu-id="b52f5-171">Rendu à la mémoire tampon d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="b52f5-171">Render to the back buffer.</span></span>
2.  <span data-ttu-id="b52f5-172">Appel présent.</span><span class="sxs-lookup"><span data-stu-id="b52f5-172">Call Present.</span></span>
3.  <span data-ttu-id="b52f5-173">Appelez GetPresentStats et stockez la structure D3DPRESENTSTATS résultante.</span><span class="sxs-lookup"><span data-stu-id="b52f5-173">Call GetPresentStats and store the resulting D3DPRESENTSTATS structure.</span></span>
4.  <span data-ttu-id="b52f5-174">Restitue le frame suivant à la mémoire tampon d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="b52f5-174">Render the next frame to the back buffer.</span></span>
5.  <span data-ttu-id="b52f5-175">Appel présent.</span><span class="sxs-lookup"><span data-stu-id="b52f5-175">Call Present.</span></span>
6.  <span data-ttu-id="b52f5-176">Appelez GetPresentStats et stockez la structure D3DPRESENTSTATS résultante.</span><span class="sxs-lookup"><span data-stu-id="b52f5-176">Call GetPresentStats and store the resulting D3DPRESENTSTATS structure.</span></span>
7.  <span data-ttu-id="b52f5-177">Comparez les valeurs de SyncRefreshCount à partir des deux structures D3DPRESENTSTATS stockées.</span><span class="sxs-lookup"><span data-stu-id="b52f5-177">Compare the values of SyncRefreshCount from the two stored D3DPRESENTSTATS structures.</span></span> <span data-ttu-id="b52f5-178">Si la différence est supérieure à un, le frame a été ignoré.</span><span class="sxs-lookup"><span data-stu-id="b52f5-178">If the difference is greater than one, then a frame was skipped.</span></span>

## <a name="requirements"></a><span data-ttu-id="b52f5-179">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b52f5-179">Requirements</span></span>



| <span data-ttu-id="b52f5-180">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b52f5-180">Requirement</span></span> | <span data-ttu-id="b52f5-181">Valeur</span><span class="sxs-lookup"><span data-stu-id="b52f5-181">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b52f5-182">En-tête</span><span class="sxs-lookup"><span data-stu-id="b52f5-182">Header</span></span><br/> | <dl> <span data-ttu-id="b52f5-183"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="b52f5-183"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b52f5-184">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b52f5-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b52f5-185">Structures Direct3D</span><span class="sxs-lookup"><span data-stu-id="b52f5-185">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
