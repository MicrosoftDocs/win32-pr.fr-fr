---
title: EVENT, élément (kit de développement logiciel (SDK) WMP)
description: L’élément EVENT définit un comportement ou une action entreprise par le lecteur Windows Media lorsqu’il reçoit une commande de script appelée comme un événement.
ms.assetid: d12af3bd-a63e-4022-aa84-0386eeef1390
keywords:
- Élément d’événement lecteur Windows Media
topic_type:
- apiref
api_name:
- EVENT Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: befc5f8462f66c1b3fbe37f0acf1a35e7f704fbf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545361"
---
# <a name="event-element"></a><span data-ttu-id="2bc33-104">Élément EVENT</span><span class="sxs-lookup"><span data-stu-id="2bc33-104">EVENT Element</span></span>

<span data-ttu-id="2bc33-105">L’élément **Event** définit un comportement ou une action entreprise par le lecteur Windows Media lorsqu’il reçoit une commande de script appelée comme un événement.</span><span class="sxs-lookup"><span data-stu-id="2bc33-105">The **EVENT** element defines a behavior or action taken by Windows Media Player when it receives a script command labeled as an event.</span></span>

``` syntax
<EVENT   
   NAME = "text string"
   WHENDONE = "RESUME" | "NEXT" | "BREAK"
>
</EVENT>
```

## <a name="attributes"></a><span data-ttu-id="2bc33-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="2bc33-106">Attributes</span></span>

<span data-ttu-id="2bc33-107">**Nom** (obligatoire)</span><span class="sxs-lookup"><span data-stu-id="2bc33-107">**NAME** (required)</span></span>

<span data-ttu-id="2bc33-108">Nom de l’événement.</span><span class="sxs-lookup"><span data-stu-id="2bc33-108">The name of the event.</span></span>

<span data-ttu-id="2bc33-109">**WHENDONE** (obligatoire)</span><span class="sxs-lookup"><span data-stu-id="2bc33-109">**WHENDONE** (required)</span></span>

<span data-ttu-id="2bc33-110">Valeur qui définit ce que le lecteur Windows Media exécute après la lecture du contenu référencé.</span><span class="sxs-lookup"><span data-stu-id="2bc33-110">A value that defines what Windows Media Player does after playing the referenced content.</span></span>

<span data-ttu-id="2bc33-111">Les valeurs suivantes sont possibles.</span><span class="sxs-lookup"><span data-stu-id="2bc33-111">The following values are possible.</span></span>



| <span data-ttu-id="2bc33-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="2bc33-112">Value</span></span>  | <span data-ttu-id="2bc33-113">Description</span><span class="sxs-lookup"><span data-stu-id="2bc33-113">Description</span></span>                                                                                                                                                                                                                     |
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bc33-114">RESUME</span><span class="sxs-lookup"><span data-stu-id="2bc33-114">RESUME</span></span> | <span data-ttu-id="2bc33-115">L’entrée actuelle (le clip interrompu par l’événement) reprend son exécution.</span><span class="sxs-lookup"><span data-stu-id="2bc33-115">The current entry (the clip interrupted by the event) resumes playing.</span></span> <span data-ttu-id="2bc33-116">Si le contenu est stocké, il reprend à l’endroit où il s’est arrêté ; Si le contenu est Broadcast, il reprend à la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="2bc33-116">If the content is stored content, it resumes at the same point where it stopped; if the content is broadcast, it resumes at the current position.</span></span>        |
| <span data-ttu-id="2bc33-117">NEXT</span><span class="sxs-lookup"><span data-stu-id="2bc33-117">NEXT</span></span>   | <span data-ttu-id="2bc33-118">L’élément d' **entrée** suivant est lu comme si l’événement ne s’était pas produit et le lecteur Windows Media avait atteint la fin du clip en cours.</span><span class="sxs-lookup"><span data-stu-id="2bc33-118">The next **ENTRY** element plays as if the event had not occurred and Windows Media Player had reached the end of the current clip.</span></span>                                                                                             |
| <span data-ttu-id="2bc33-119">BREAK</span><span class="sxs-lookup"><span data-stu-id="2bc33-119">BREAK</span></span>  | <span data-ttu-id="2bc33-120">Si l’entrée actuelle se trouve dans une boucle **REPEAT** , la boucle se termine comme si le nombre de répétitions avait été terminé.</span><span class="sxs-lookup"><span data-stu-id="2bc33-120">If the current entry is within a **REPEAT** loop, the loop terminates as if the repeat count had been completed.</span></span> <span data-ttu-id="2bc33-121">Dans le cas contraire, le lecteur Windows Media passe à la fin de la sélection comme si la dernière entrée était terminée normalement.</span><span class="sxs-lookup"><span data-stu-id="2bc33-121">Otherwise, Windows Media Player jumps to the end of the playlist as if the final entry had completed as usual.</span></span> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="2bc33-122">Éléments parent/enfant</span><span class="sxs-lookup"><span data-stu-id="2bc33-122">Parent/Child Elements</span></span>



| <span data-ttu-id="2bc33-123">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="2bc33-123">Hierarchy</span></span>       | <span data-ttu-id="2bc33-124">Éléments</span><span class="sxs-lookup"><span data-stu-id="2bc33-124">Elements</span></span>                |
|-----------------|-------------------------|
| <span data-ttu-id="2bc33-125">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="2bc33-125">Parent elements</span></span> | <span data-ttu-id="2bc33-126">**ASX**</span><span class="sxs-lookup"><span data-stu-id="2bc33-126">**ASX**</span></span>                 |
| <span data-ttu-id="2bc33-127">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="2bc33-127">Child elements</span></span>  | <span data-ttu-id="2bc33-128">**entrée**, **ENTRYREF**</span><span class="sxs-lookup"><span data-stu-id="2bc33-128">**ENTRY**, **ENTRYREF**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="2bc33-129">Notes</span><span class="sxs-lookup"><span data-stu-id="2bc33-129">Remarks</span></span>

<span data-ttu-id="2bc33-130">Cet élément définit un comportement ou une action entreprise par le lecteur Windows Media lorsqu’il reçoit une commande de script appelée comme un événement.</span><span class="sxs-lookup"><span data-stu-id="2bc33-130">This element defines a behavior or action taken by Windows Media Player when it receives a script command labeled as an event.</span></span> <span data-ttu-id="2bc33-131">Un événement est un type particulier de commande de script incorporé dans un flux envoyé au lecteur Windows Media qui se compose d’une chaîne double.</span><span class="sxs-lookup"><span data-stu-id="2bc33-131">An event is a particular type of script command embedded in a stream sent to Windows Media Player that consists of a double string.</span></span> <span data-ttu-id="2bc33-132">La première chaîne est le mot « Event » et la deuxième chaîne est le nom de l’événement.</span><span class="sxs-lookup"><span data-stu-id="2bc33-132">The first string is the word "event", and the second string is the event name.</span></span> <span data-ttu-id="2bc33-133">Le nom de l’événement dans la deuxième chaîne doit correspondre au nom de l’événement défini dans le métafichier.</span><span class="sxs-lookup"><span data-stu-id="2bc33-133">The event name in the second string must match the event name defined in the metafile.</span></span> <span data-ttu-id="2bc33-134">(La correspondance n’est pas sensible à la casse.) Les événements peuvent être envoyés au lecteur Windows Media recevant un flux en temps réel, ou enregistrés dans un fichier. ASF,. WMA ou. wmv qui est remis sous forme de flux de monodiffusion à la demande.</span><span class="sxs-lookup"><span data-stu-id="2bc33-134">(The match is not case-sensitive.) Events can be sent to Windows Media Player receiving a real-time stream, or can be saved in an .asf, .wma, or .wmv file that gets delivered as an on-demand unicast stream.</span></span> <span data-ttu-id="2bc33-135">Lorsque le lecteur Windows Media reçoit la commande de script, il traite l’événement comme défini par l’élément **Event** .</span><span class="sxs-lookup"><span data-stu-id="2bc33-135">When Windows Media Player receives the script command, it processes the event as defined by the **EVENT** element.</span></span>

<span data-ttu-id="2bc33-136">Cet élément définit une étendue d’éléments d' **entrée** ou de **ENTRYREF** qui sont traités chaque fois que le lecteur Windows Media reçoit la commande de script avec l’événement nommé.</span><span class="sxs-lookup"><span data-stu-id="2bc33-136">This element defines a scope of **ENTRY** or **ENTRYREF** elements that are processed whenever Windows Media Player receives the script command with the named event.</span></span> <span data-ttu-id="2bc33-137">**ENTRYREF** peut être une URL qui pointe vers une page ASP.</span><span class="sxs-lookup"><span data-stu-id="2bc33-137">The **ENTRYREF** can be a URL that points to an ASP page.</span></span> <span data-ttu-id="2bc33-138">Avec cet élément, vous pouvez spécifier un comportement pour le basculement de flux en temps quasi-réel, par opposition aux modifications de flux précréées à l’aide de références à d’autres éléments de contenu ou de sous-fichiers Windows Media.</span><span class="sxs-lookup"><span data-stu-id="2bc33-138">With this element, you can specify a behavior for stream switching in near real time, as opposed to pre-authored stream changes using references to other pieces of content or Windows Media metafiles.</span></span>

<span data-ttu-id="2bc33-139">Lorsque vous utilisez des pages ASP pour générer des sélections, vous devez spécifier une valeur pour la *réponse*. Propriété **ContentType** et la *réponse*. **Expires** dans la page ASP en raison de problèmes de latence avec le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="2bc33-139">When you use ASP pages to generate playlists, you must specify a value for the *Response*.**ContentType** property and the *Response*.**expires** property in the ASP page because of latency issues with Windows Media Player.</span></span> <span data-ttu-id="2bc33-140">*Réponse*. **ContentType** doit être une extension de nom de fichier valide pour les fichiers Windows Media.</span><span class="sxs-lookup"><span data-stu-id="2bc33-140">The *Response*.**ContentType** must be a valid file name extension for Windows Media metafiles.</span></span> <span data-ttu-id="2bc33-141">Les types valides sont. ASF,. asx,. WMA,. Wax,. wmv et. wvx.</span><span class="sxs-lookup"><span data-stu-id="2bc33-141">Valid types include .asf, .asx, .wma, .wax, .wmv, and .wvx.</span></span>

<span data-ttu-id="2bc33-142">Pour plus d’informations sur l’utilisation de l’objet **Response** dans ASP, consultez le kit de développement Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="2bc33-142">See the Platform SDK for details about using the **Response** object in ASP.</span></span>

<span data-ttu-id="2bc33-143">Cet élément peut apparaître n’importe où dans l’élément **ASX** .</span><span class="sxs-lookup"><span data-stu-id="2bc33-143">This element can appear anywhere within the **ASX** element.</span></span> <span data-ttu-id="2bc33-144">Si plusieurs éléments d' **événement** dans un élément **ASX** ont des valeurs identiques pour leurs attributs de **nom** , le lecteur Windows Media utilise la première occurrence dans l’élément **ASX** et ignore tous les autres.</span><span class="sxs-lookup"><span data-stu-id="2bc33-144">If multiple **EVENT** elements within an **ASX** element have identical values for their **NAME** attributes, Windows Media Player uses the first occurrence within the **ASX** element, and ignores all others.</span></span> <span data-ttu-id="2bc33-145">Lorsque les éléments d' **événement** ont des attributs de **nom** distincts, leur ordre dans l’élément **ASX** n’a pas d’importance.</span><span class="sxs-lookup"><span data-stu-id="2bc33-145">When **EVENT** elements have distinct **NAME** attributes, their order within the **ASX** element does not matter.</span></span>

<span data-ttu-id="2bc33-146">Le lecteur Windows Media ignore les événements qu’il reçoit lors du traitement d’un autre événement.</span><span class="sxs-lookup"><span data-stu-id="2bc33-146">Windows Media Player discards events it receives while processing another event.</span></span> <span data-ttu-id="2bc33-147">L’imbrication d’événements n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="2bc33-147">Nesting of events is not supported.</span></span> <span data-ttu-id="2bc33-148">Lorsque le lecteur Windows Media est en mode aperçu, le contenu de l’événement n’est pas imposé par l’élément **PREVIEWDURATION** ; la longueur totale du contenu de l’événement peut s’exécuter même si la durée de l’aperçu de l’élément d' **entrée** actif expire avant la fin de l’événement.</span><span class="sxs-lookup"><span data-stu-id="2bc33-148">When Windows Media Player is in preview mode, event content is not constrained by the **PREVIEWDURATION** element; the full length of event content can play even if the preview duration for the active **ENTRY** element expires prior to the end of the event.</span></span>

## <a name="examples"></a><span data-ttu-id="2bc33-149">Exemples</span><span class="sxs-lookup"><span data-stu-id="2bc33-149">Examples</span></span>

<span data-ttu-id="2bc33-150">Dans cet exemple, lorsque le lecteur Windows Media reçoit l’événement de commande de script et la chaîne de commande « Adlink » dans le média de diffusion en continu qu’il restitue, il recherche un **EVENTNAME** « Adlink » dans la sélection.</span><span class="sxs-lookup"><span data-stu-id="2bc33-150">In this example, when Windows Media Player receives the script command EVENT and command string "Adlink" in the streaming media it is rendering, it searches the playlist for an **EVENTNAME** "Adlink".</span></span> <span data-ttu-id="2bc33-151">Le lecteur Windows Media passe du flux qu’il restitue et lit le contenu référencé dans l' **événement**« https://example.microsoft.com/adlink.htm ».</span><span class="sxs-lookup"><span data-stu-id="2bc33-151">Windows Media Player switches from the stream it is rendering and plays the content referenced in the **EVENT**, "https://example.microsoft.com/adlink.htm".</span></span>

<span data-ttu-id="2bc33-152">L’attribut d' **entrée** **CLIENTSKIP** a la valeur no pour empêcher l’omission du clip d' **événement** .</span><span class="sxs-lookup"><span data-stu-id="2bc33-152">**ENTRY** attribute **CLIENTSKIP** is set to NO to prevent the **EVENT** clip from being skipped.</span></span> <span data-ttu-id="2bc33-153">Il doit être lu.</span><span class="sxs-lookup"><span data-stu-id="2bc33-153">It must be played.</span></span>

<span data-ttu-id="2bc33-154">Le script `WHENDONE="RESUME"` indique à Windows Media Player de reprendre la lecture du média précédent à partir duquel il est passé à partir du moment où Adlink. ASF est terminé.</span><span class="sxs-lookup"><span data-stu-id="2bc33-154">The script `WHENDONE="RESUME"` instructs Windows Media Player to resume playing the previous media it switched from as soon as Adlink.asf is finished.</span></span>


```XML
<ASX VERSION="3.0">
<ENTRY CLIENTSKIP="NO">
   <REF HREF="https://example.microsoft.com/clip1.asf" />
</ENTRY>
<EVENT NAME="Adlink" WHENDONE="RESUME">
   <ENTRYREF HREF="https://example.microsoft.com/adlink.htm" 
       CLIENTSKIP="NO" />
</EVENT>
</ASX>
```



## <a name="requirements"></a><span data-ttu-id="2bc33-155">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2bc33-155">Requirements</span></span>



| <span data-ttu-id="2bc33-156">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2bc33-156">Requirement</span></span> | <span data-ttu-id="2bc33-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="2bc33-157">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="2bc33-158">Version</span><span class="sxs-lookup"><span data-stu-id="2bc33-158">Version</span></span><br/> | <span data-ttu-id="2bc33-159">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="2bc33-159">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2bc33-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2bc33-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bc33-161">**Informations de référence sur les éléments de métafichier Windows Media**</span><span class="sxs-lookup"><span data-stu-id="2bc33-161">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="2bc33-162">**Informations de référence sur les métafichiers Windows Media**</span><span class="sxs-lookup"><span data-stu-id="2bc33-162">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> <dt>

[<span data-ttu-id="2bc33-163">**Modèle objet du lecteur Windows Media**</span><span class="sxs-lookup"><span data-stu-id="2bc33-163">**Windows Media Player Object Model**</span></span>](windows-media-player-object-model.md)
</dt> </dl>

 

 





