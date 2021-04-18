---
title: Glossaire Windows animation
description: Ce glossaire contient des termes et des acronymes intéressants pour les développeurs qui utilisent le gestionnaire d’animations Windows.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 66e9cfb4-b9ae-4c21-9b1f-532c7d750903
keywords:
- Animation Windows Animation Windows, Glossaire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36b7f276b0f20efc35057a9ee7c006c3cf170ac3
ms.sourcegitcommit: fdd00b445ee88366e9cdd1eed0cb3e42e2a73eca
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2019
ms.locfileid: "104507762"
---
# <a name="windows-animation-glossary"></a><span data-ttu-id="e53ff-104">Glossaire Windows animation</span><span class="sxs-lookup"><span data-stu-id="e53ff-104">Windows Animation Glossary</span></span>

<span data-ttu-id="e53ff-105">Ce glossaire contient des termes et des acronymes intéressants pour les développeurs qui utilisent le gestionnaire d’animations Windows.</span><span class="sxs-lookup"><span data-stu-id="e53ff-105">This glossary contains terms and acronyms of interest to developers using the Windows Animation Manager.</span></span>

<dl> <dt>

<span data-ttu-id="e53ff-106"><span id="uianimation.term.animation"></span><span id="UIANIMATION.TERM.ANIMATION"></span>**animation**</span><span class="sxs-lookup"><span data-stu-id="e53ff-106"><span id="uianimation.term.animation"></span><span id="UIANIMATION.TERM.ANIMATION"></span> **animation**</span></span> 
</dt> <dd>

<span data-ttu-id="e53ff-107">Séquence de synthèse, images continues consécutives qui produisent une illusion de mouvement lors de la lecture.</span><span class="sxs-lookup"><span data-stu-id="e53ff-107">A sequence of synthetic, successive still images that produces an illusion of movement when played back.</span></span>

</dd> <dt>

<span data-ttu-id="e53ff-108"><span id="uianimation.term.animation_manager"></span><span id="UIANIMATION.TERM.ANIMATION_MANAGER"></span>**Gestionnaire d’animations**</span><span class="sxs-lookup"><span data-stu-id="e53ff-108"><span id="uianimation.term.animation_manager"></span><span id="UIANIMATION.TERM.ANIMATION_MANAGER"></span> **animation manager**</span></span> 
</dt> <dd>

<span data-ttu-id="e53ff-109">Composant principal de Windows animation et interface de programmation centrale pour la gestion (création, planification et contrôle) d’animations.</span><span class="sxs-lookup"><span data-stu-id="e53ff-109">A core component of Windows Animation and the central programmatic interface for managing (creating, scheduling, and controlling) animations.</span></span>

</dd> <dt>

<span data-ttu-id="e53ff-110"><span id="uianimation.term.animation_timer"></span><span id="UIANIMATION.TERM.ANIMATION_TIMER"></span>**minuteur d’animation**</span><span class="sxs-lookup"><span data-stu-id="e53ff-110"><span id="uianimation.term.animation_timer"></span><span id="UIANIMATION.TERM.ANIMATION_TIMER"></span>**animation timer**</span></span>
</dt> <dd>

<span data-ttu-id="e53ff-111">Composant permettant de fournir des services de minutage qui peuvent être utilisés conjointement avec le gestionnaire d’animations.</span><span class="sxs-lookup"><span data-stu-id="e53ff-111">A component to provide timing services that can be used in conjunction with the animation manager.</span></span> <span data-ttu-id="e53ff-112">Il limite de manière dynamique la fréquence d’images en fonction de la charge de l’application et du système ou en mode de faible alimentation.</span><span class="sxs-lookup"><span data-stu-id="e53ff-112">It dynamically throttles the frame rate based on application and system load or in low-power mode.</span></span> <span data-ttu-id="e53ff-113">Voir aussi : limitation.</span><span class="sxs-lookup"><span data-stu-id="e53ff-113">See also: throttling.</span></span>

</dd> <dt>

<span data-ttu-id="e53ff-114"><span id="uianimation.term.animation_variable"></span><span id="UIANIMATION.TERM.ANIMATION_VARIABLE"></span>**variable d’animation**</span><span class="sxs-lookup"><span data-stu-id="e53ff-114"><span id="uianimation.term.animation_variable"></span><span id="UIANIMATION.TERM.ANIMATION_VARIABLE"></span> **animation variable**</span></span> 
</dt> <dd>

<span data-ttu-id="e53ff-115">Valeur qui peut être animée.</span><span class="sxs-lookup"><span data-stu-id="e53ff-115">A value that can be animated.</span></span> <span data-ttu-id="e53ff-116">Les variables d’animation peuvent être utilisées pour représenter la position, la taille, la rotation, la transparence et d’autres qualités d’objets visibles.</span><span class="sxs-lookup"><span data-stu-id="e53ff-116">Animation variables may be used to represent the position, size, rotation, transparency and other qualities of visible objects.</span></span>

</dd> <dt>

<span data-ttu-id="e53ff-117"><span id="uianimation.term.cancellation"></span><span id="UIANIMATION.TERM.CANCELLATION"></span>**Ference**</span><span class="sxs-lookup"><span data-stu-id="e53ff-117"><span id="uianimation.term.cancellation"></span><span id="UIANIMATION.TERM.CANCELLATION"></span>**cancellation**</span></span>
</dt> <dd>

<span data-ttu-id="e53ff-118">Processus de suppression d’une table de montage séquentiel de la planification avant son démarrage.</span><span class="sxs-lookup"><span data-stu-id="e53ff-118">The process of removing a storyboard from the schedule before it has started playing.</span></span>

</dd> <dt>

<span data-ttu-id="e53ff-119"><span id="uianimation.term.compression"></span><span id="UIANIMATION.TERM.COMPRESSION"></span>**compressé**</span><span class="sxs-lookup"><span data-stu-id="e53ff-119"><span id="uianimation.term.compression"></span><span id="UIANIMATION.TERM.COMPRESSION"></span>**compression**</span></span>
</dt> <dd>

<span data-ttu-id="e53ff-120">Déviation du temps d’une table de montage séquentiel.</span><span class="sxs-lookup"><span data-stu-id="e53ff-120">A warping of a storyboard's perception of time.</span></span> <span data-ttu-id="e53ff-121">Le système augmente la vitesse à laquelle le Storyboard progresse en passant les valeurs d’heure d’entrée qui augmentent plus rapidement que l’horloge système.</span><span class="sxs-lookup"><span data-stu-id="e53ff-121">The system increases the rate at which the storyboard progresses by passing input time values that increase faster than the system clock.</span></span>

</dd> <dt>

<span data-ttu-id="e53ff-122"><span id="uianimation.term.conclusion"></span><span id="UIANIMATION.TERM.CONCLUSION"></span>**achèvement**</span><span class="sxs-lookup"><span data-stu-id="e53ff-122"><span id="uianimation.term.conclusion"></span><span id="UIANIMATION.TERM.CONCLUSION"></span>**conclusion**</span></span>
</dt> <dd>

<span data-ttu-id="e53ff-123">Processus de direction d’une table de montage séquentiel pour quitter toutes les boucles indéfinies.</span><span class="sxs-lookup"><span data-stu-id="e53ff-123">The process of directing a storyboard to exit any indefinite loops.</span></span> <span data-ttu-id="e53ff-124">Si la boucle a commencé, l’itération en cours se termine et le reste de la table de montage séquentiel est alors lu.</span><span class="sxs-lookup"><span data-stu-id="e53ff-124">If the loop has begun, the current iteration will complete and the remainder of the storyboard will then play.</span></span> <span data-ttu-id="e53ff-125">Dans le cas contraire, la partie en boucle de la table de montage séquentiel sera ignorée entièrement.</span><span class="sxs-lookup"><span data-stu-id="e53ff-125">Otherwise, the looped portion of the storyboard will be skipped entirely.</span></span>

</dd> <dt>

<span data-ttu-id="e53ff-126"><span id="uianimation.term.frame"></span><span id="UIANIMATION.TERM.FRAME"></span>**Frame**</span><span class="sxs-lookup"><span data-stu-id="e53ff-126"><span id="uianimation.term.frame"></span><span id="UIANIMATION.TERM.FRAME"></span> **frame**</span></span> 
</dt> <dd>

<span data-ttu-id="e53ff-127">Image unique dans un film ou une animation.</span><span class="sxs-lookup"><span data-stu-id="e53ff-127">A single image in a movie or an animation.</span></span>

</dd> <dt>

<span data-ttu-id="e53ff-128"><span id="uianimation.term.frame_rate"></span><span id="UIANIMATION.TERM.FRAME_RATE"></span>**fréquence d’images**</span><span class="sxs-lookup"><span data-stu-id="e53ff-128"><span id="uianimation.term.frame_rate"></span><span id="UIANIMATION.TERM.FRAME_RATE"></span> **frame rate**</span></span> 
</dt> <dd>

<span data-ttu-id="e53ff-129">Nombre de frames affichés par seconde.</span><span class="sxs-lookup"><span data-stu-id="e53ff-129">The number of frames displayed per second.</span></span> <span data-ttu-id="e53ff-130">Des fréquences d’images supérieures produisent généralement un mouvement plus lisse dans l’image.</span><span class="sxs-lookup"><span data-stu-id="e53ff-130">Higher frame rates generally produce smoother movement in the picture.</span></span>

</dd> <dt>

<span data-ttu-id="e53ff-131"><span id="uianimation.term.interpolator"></span><span id="UIANIMATION.TERM.INTERPOLATOR"></span>**interpolateur**</span><span class="sxs-lookup"><span data-stu-id="e53ff-131"><span id="uianimation.term.interpolator"></span><span id="UIANIMATION.TERM.INTERPOLATOR"></span>**interpolator**</span></span>
</dt> <dd>

<span data-ttu-id="e53ff-132">Objet de programmation qui effectue l’interpolation mathématique de la valeur et de la vélocité d’une variable pour une transition.</span><span class="sxs-lookup"><span data-stu-id="e53ff-132">The programming object that does the mathematical interpolation of the value and velocity of a variable for a transition.</span></span>

</dd> <dt>

<span data-ttu-id="e53ff-133"><span id="uianimation.term.keyframe"></span><span id="UIANIMATION.TERM.KEYFRAME"></span>**image clé**</span><span class="sxs-lookup"><span data-stu-id="e53ff-133"><span id="uianimation.term.keyframe"></span><span id="UIANIMATION.TERM.KEYFRAME"></span>**keyframe**</span></span>
</dt> <dd>

<span data-ttu-id="e53ff-134">Un moment dans le temps dans un Storyboard, qui peut être spécifié par rapport au début de la table de montage séquentiel, par rapport à une autre image clé, ou à l’heure de fin d’une transition, et utilisé pour spécifier l’heure de début et de fin d’autres transitions ou d’un cycle dans le Storyboard.</span><span class="sxs-lookup"><span data-stu-id="e53ff-134">A moment in time within a storyboard, which can be specified relative to the start of the storyboard, relative to another keyframe, or at the end time of a transition, and used to specify the start and end time of other transitions or a cycle within the storyboard.</span></span>

</dd> <dt>

<span data-ttu-id="e53ff-135"><span id="uianimation.term.loop"></span><span id="UIANIMATION.TERM.LOOP"></span>**circuit**</span><span class="sxs-lookup"><span data-stu-id="e53ff-135"><span id="uianimation.term.loop"></span><span id="UIANIMATION.TERM.LOOP"></span>**loop**</span></span>
</dt> <dd>

<span data-ttu-id="e53ff-136">Section d’un Storyboard entre deux images clés qui est jouée à plusieurs reprises.</span><span class="sxs-lookup"><span data-stu-id="e53ff-136">A section of a storyboard between two keyframes that is played repeatedly.</span></span> <span data-ttu-id="e53ff-137">Une boucle peut jouer un nombre fini de fois ou indéfiniment.</span><span class="sxs-lookup"><span data-stu-id="e53ff-137">A loop may play a finite number of times or indefinitely.</span></span>

</dd> <dt>

<span data-ttu-id="e53ff-138"><span id="uianimation.term.priority_comparison"></span><span id="UIANIMATION.TERM.PRIORITY_COMPARISON"></span>**comparaison des priorités**</span><span class="sxs-lookup"><span data-stu-id="e53ff-138"><span id="uianimation.term.priority_comparison"></span><span id="UIANIMATION.TERM.PRIORITY_COMPARISON"></span> **priority comparison**</span></span> 
</dt> <dd>

<span data-ttu-id="e53ff-139">Code défini par le client qui compare deux storyboards, un qui est déjà planifié et l’autre sur le lieu d’être planifié, pour déterminer leur priorité relative.</span><span class="sxs-lookup"><span data-stu-id="e53ff-139">Client-defined code that compares two storyboards, one already scheduled and the other about to be scheduled, to determine their relative priority.</span></span> <span data-ttu-id="e53ff-140">Une table de montage séquentiel planifiée peut être tronquée, compressée, annulée ou conclue pour permettre la planification de la table de montage séquentiel avec une priorité plus élevée.</span><span class="sxs-lookup"><span data-stu-id="e53ff-140">A scheduled storyboard may be trimmed, compressed, canceled, or concluded to enable scheduling of the storyboard with higher priority.</span></span>

</dd> <dt>

<span data-ttu-id="e53ff-141"><span id="uianimation.term.storyboard"></span><span id="UIANIMATION.TERM.STORYBOARD"></span>**Storyboard**</span><span class="sxs-lookup"><span data-stu-id="e53ff-141"><span id="uianimation.term.storyboard"></span><span id="UIANIMATION.TERM.STORYBOARD"></span> **storyboard**</span></span> 
</dt> <dd>

<span data-ttu-id="e53ff-142">Groupe de transitions d’animation synchronisées les unes par rapport aux autres.</span><span class="sxs-lookup"><span data-stu-id="e53ff-142">A group of animation transitions synchronized relative to one another.</span></span>

</dd> <dt>

<span data-ttu-id="e53ff-143"><span id="uianimation.term.tag"></span><span id="UIANIMATION.TERM.TAG"></span>**balise**</span><span class="sxs-lookup"><span data-stu-id="e53ff-143"><span id="uianimation.term.tag"></span><span id="UIANIMATION.TERM.TAG"></span> **tag**</span></span> 
</dt> <dd>

<span data-ttu-id="e53ff-144">Paire composée d’un ID d’entier et d’un objet COM utilisé par une application pour identifier des variables d’animation et des storyboards au sein de l’étendue d’un gestionnaire d’animations spécifique.</span><span class="sxs-lookup"><span data-stu-id="e53ff-144">A pair consisting of an integer ID and a COM object used by an application to identify animation variables and storyboards within the scope of a specific animation manager.</span></span>

</dd> <dt>

<span data-ttu-id="e53ff-145"><span id="uianimation.term.throttling"></span><span id="UIANIMATION.TERM.THROTTLING"></span>**limitation**</span><span class="sxs-lookup"><span data-stu-id="e53ff-145"><span id="uianimation.term.throttling"></span><span id="UIANIMATION.TERM.THROTTLING"></span> **throttling**</span></span> 
</dt> <dd>

<span data-ttu-id="e53ff-146">Ajustement dynamique de la fréquence d’images d’une animation pour répondre à certaines exigences.</span><span class="sxs-lookup"><span data-stu-id="e53ff-146">Dynamically adjusting the frame rate of an animation to meet certain requirements.</span></span> <span data-ttu-id="e53ff-147">La limitation permet de s’assurer que les animations sont rendues à une fréquence d’images cohérente tout en minimisant l’utilisation des ressources système pour le rendu à une vitesse supérieure à ce qui est nécessaire ou utile.</span><span class="sxs-lookup"><span data-stu-id="e53ff-147">Throttling helps to ensure that animations are rendered at a consistent frame rate while minimizing the use of system resources for rendering at a rate that is beyond what is needed or useful.</span></span>

</dd> <dt>

<span data-ttu-id="e53ff-148"><span id="uianimation.term.tick"></span><span id="UIANIMATION.TERM.TICK"></span>**cycle**</span><span class="sxs-lookup"><span data-stu-id="e53ff-148"><span id="uianimation.term.tick"></span><span id="UIANIMATION.TERM.TICK"></span> **tick**</span></span> 
</dt> <dd>

<span data-ttu-id="e53ff-149">Événement de minuterie qui déclenche généralement le rendu d’un frame unique.</span><span class="sxs-lookup"><span data-stu-id="e53ff-149">A timer event that typically triggers the rendering of a single frame.</span></span>

</dd> <dt>

<span data-ttu-id="e53ff-150"><span id="uianimation.term.transition"></span><span id="UIANIMATION.TERM.TRANSITION"></span>**transition**</span><span class="sxs-lookup"><span data-stu-id="e53ff-150"><span id="uianimation.term.transition"></span><span id="UIANIMATION.TERM.TRANSITION"></span> **transition**</span></span> 
</dt> <dd>

<span data-ttu-id="e53ff-151">Construction qui définit des mises à jour progressifs pour une variable d’animation sur une période donnée.</span><span class="sxs-lookup"><span data-stu-id="e53ff-151">A construct that defines progressive updates for an animation variable over a period of time.</span></span>

</dd> <dt>

<span data-ttu-id="e53ff-152"><span id="uianimation.term.trimming"></span><span id="UIANIMATION.TERM.TRIMMING"></span>**limitation**</span><span class="sxs-lookup"><span data-stu-id="e53ff-152"><span id="uianimation.term.trimming"></span><span id="UIANIMATION.TERM.TRIMMING"></span>**trimming**</span></span>
</dt> <dd>

<span data-ttu-id="e53ff-153">Préemption du contrôle d’une table de montage séquentiel d’une variable d’animation avec un Storyboard de priorité plus élevée.</span><span class="sxs-lookup"><span data-stu-id="e53ff-153">Preempting a storyboard's control of an animation variable with a higher-priority storyboard.</span></span> <span data-ttu-id="e53ff-154">Si la suppression d’une table de montage séquentiel sur une ou plusieurs variables entraîne la fin prématurée de la table de montage séquentiel, elle est considérée comme tronquée.</span><span class="sxs-lookup"><span data-stu-id="e53ff-154">If trimming a storyboard on one or more variables causes the storyboard to end prematurely, it is considered truncated.</span></span> <span data-ttu-id="e53ff-155">Voir aussi : troncation.</span><span class="sxs-lookup"><span data-stu-id="e53ff-155">See also: truncation.</span></span>

</dd> <dt>

<span data-ttu-id="e53ff-156"><span id="uianimation.term.truncation"></span><span id="UIANIMATION.TERM.TRUNCATION"></span>**troncation**</span><span class="sxs-lookup"><span data-stu-id="e53ff-156"><span id="uianimation.term.truncation"></span><span id="UIANIMATION.TERM.TRUNCATION"></span>**truncation**</span></span>
</dt> <dd>

<span data-ttu-id="e53ff-157">Fin prématurée d’une table de montage séquentiel en préemption le contrôle d’une ou plusieurs des variables qu’elle anime avec une ou plusieurs storyboards de priorité supérieure.</span><span class="sxs-lookup"><span data-stu-id="e53ff-157">Ending a storyboard prematurely by preempting control of one or more of the variables that it animates with one or more higher-priority storyboards.</span></span> <span data-ttu-id="e53ff-158">Voir aussi : suppression.</span><span class="sxs-lookup"><span data-stu-id="e53ff-158">See also: trimming.</span></span>

</dd> </dl>

 

 




