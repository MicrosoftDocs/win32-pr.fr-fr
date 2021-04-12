---
title: Écoute des événements de ruban
description: L’infrastructure de ruban Windows utilise l’infrastructure de Suivi d’v nements pour Windows (ETW) pour permettre aux développeurs d’apprendre comment les utilisateurs interagissent avec le ruban de leur application.
ms.assetid: F29A8E41-C902-410E-BD28-653E078320E9
keywords:
- Ruban Windows, événements
- Ruban, événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcbfb2c6417c1423cb785b6b80de4396146535c2
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2020
ms.locfileid: "104316614"
---
# <a name="listening-for-ribbon-events"></a><span data-ttu-id="6d2bc-105">Écoute des événements de ruban</span><span class="sxs-lookup"><span data-stu-id="6d2bc-105">Listening for Ribbon Events</span></span>

<span data-ttu-id="6d2bc-106">L’infrastructure de ruban Windows utilise l’infrastructure de [suivi d’v nements pour Windows (ETW)](../etw/event-tracing-portal.md) pour permettre aux développeurs d’apprendre comment les utilisateurs interagissent avec le ruban de leur application.</span><span class="sxs-lookup"><span data-stu-id="6d2bc-106">The Windows Ribbon framework uses the [Event Tracing for Windows (ETW)](../etw/event-tracing-portal.md) infrastructure to enable developers to learn how users are interacting with their application's ribbon.</span></span>

## <a name="introduction"></a><span data-ttu-id="6d2bc-107">Introduction</span><span class="sxs-lookup"><span data-stu-id="6d2bc-107">Introduction</span></span>

<span data-ttu-id="6d2bc-108">Le mécanisme d’événement d’infrastructure de ruban est conçu de telle sorte que l’infrastructure signale les événements de l’interface utilisateur du ruban à l’application afin que vous puissiez surveiller l’activité des utilisateurs, apprendre leurs modèles d’interaction et évaluer les tendances d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="6d2bc-108">The Ribbon framework event mechanism is designed such that the framework reports ribbon UI events to the application so you can monitor user activity, learn their interaction patterns, and assess usage trends.</span></span> <span data-ttu-id="6d2bc-109">Ces informations peuvent être utilisées pour affiner l’expérience utilisateur des itérations ultérieures de votre application de ruban.</span><span class="sxs-lookup"><span data-stu-id="6d2bc-109">This information can be used to refine the user experience for future iterations of your ribbon app.</span></span>

<span data-ttu-id="6d2bc-110">L’utilisation des événements de l’infrastructure du ruban implique les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="6d2bc-110">Using the Ribbon framework events involves the following:</span></span>

1.  <span data-ttu-id="6d2bc-111">L’application ruban doit inscrire un écouteur de [suivi d’v nements pour Windows (ETW)](../etw/event-tracing-portal.md) pour recevoir des notifications d’événements de ruban à partir de l’infrastructure du ruban.</span><span class="sxs-lookup"><span data-stu-id="6d2bc-111">The ribbon application must register an [Event Tracing for Windows (ETW)](../etw/event-tracing-portal.md) listener to receive ribbon event notifications from the Ribbon framework.</span></span>
2.  <span data-ttu-id="6d2bc-112">L’infrastructure du ruban déclenche des rappels d’événements de l’interface utilisateur du ruban au moment de l’exécution, si l’application a inscrit un écouteur [de suivi d’v nements pour Windows (ETW)](../etw/event-tracing-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="6d2bc-112">The Ribbon framework fires ribbon UI event callbacks at run time, if the application has registered an [Event Tracing for Windows (ETW)](../etw/event-tracing-portal.md) listener.</span></span>

## <a name="supported-events"></a><span data-ttu-id="6d2bc-113">Événements pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d2bc-113">Supported events</span></span>

<span data-ttu-id="6d2bc-114">Les événements exposés aux applications du ruban sont décrits dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="6d2bc-114">The events exposed to ribbon applications are described in the following table.</span></span> 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6d2bc-115">Événement</span><span class="sxs-lookup"><span data-stu-id="6d2bc-115">Event</span></span></th>
<th><span data-ttu-id="6d2bc-116">Rapport d’événements</span><span class="sxs-lookup"><span data-stu-id="6d2bc-116">Event report</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6d2bc-117">Onglet activé</span><span class="sxs-lookup"><span data-stu-id="6d2bc-117">Tab activated</span></span></td>
<td><span data-ttu-id="6d2bc-118">ID de commande</span><span class="sxs-lookup"><span data-stu-id="6d2bc-118">Command ID</span></span><br/> <span data-ttu-id="6d2bc-119">Nom de commande</span><span class="sxs-lookup"><span data-stu-id="6d2bc-119">Command name</span></span><br/> <span data-ttu-id="6d2bc-120">Verbe d’événement</span><span class="sxs-lookup"><span data-stu-id="6d2bc-120">Event verb</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d2bc-121">Onglet contextuel activé</span><span class="sxs-lookup"><span data-stu-id="6d2bc-121">Contextual tab activated</span></span></td>
<td><span data-ttu-id="6d2bc-122">ID de commande</span><span class="sxs-lookup"><span data-stu-id="6d2bc-122">Command ID</span></span><br/> <span data-ttu-id="6d2bc-123">Nom de commande</span><span class="sxs-lookup"><span data-stu-id="6d2bc-123">Command name</span></span><br/> <span data-ttu-id="6d2bc-124">Verbe d’événement</span><span class="sxs-lookup"><span data-stu-id="6d2bc-124">Event verb</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6d2bc-125">Menu de l’application ouvert</span><span class="sxs-lookup"><span data-stu-id="6d2bc-125">Application Menu opened</span></span></td>
<td><span data-ttu-id="6d2bc-126">Verbe d’événement</span><span class="sxs-lookup"><span data-stu-id="6d2bc-126">Event verb</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d2bc-127">Menu de l’application fermé</span><span class="sxs-lookup"><span data-stu-id="6d2bc-127">Application Menu closed</span></span></td>
<td><span data-ttu-id="6d2bc-128">Verbe d’événement</span><span class="sxs-lookup"><span data-stu-id="6d2bc-128">Event verb</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6d2bc-129">Menu (normal ou Galerie ouvert)</span><span class="sxs-lookup"><span data-stu-id="6d2bc-129">Menu (regular or gallery) opened</span></span></td>
<td><span data-ttu-id="6d2bc-130">ID de commande</span><span class="sxs-lookup"><span data-stu-id="6d2bc-130">Command ID</span></span><br/> <span data-ttu-id="6d2bc-131">Nom de commande</span><span class="sxs-lookup"><span data-stu-id="6d2bc-131">Command name</span></span><br/> <span data-ttu-id="6d2bc-132">Verbe d’événement</span><span class="sxs-lookup"><span data-stu-id="6d2bc-132">Event verb</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="6d2bc-133">Les événements de menu QAT ne sont pas exposés.</span><span class="sxs-lookup"><span data-stu-id="6d2bc-133">QAT menu events are not exposed.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d2bc-134">Menu (normal ou Galerie fermé)</span><span class="sxs-lookup"><span data-stu-id="6d2bc-134">Menu (regular or gallery) closed</span></span></td>
<td><span data-ttu-id="6d2bc-135">ID de commande</span><span class="sxs-lookup"><span data-stu-id="6d2bc-135">Command ID</span></span><br/> <span data-ttu-id="6d2bc-136">Nom de commande</span><span class="sxs-lookup"><span data-stu-id="6d2bc-136">Command name</span></span><br/> <span data-ttu-id="6d2bc-137">Verbe d’événement</span><span class="sxs-lookup"><span data-stu-id="6d2bc-137">Event verb</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="6d2bc-138">Les événements de menu QAT ne sont pas exposés.</span><span class="sxs-lookup"><span data-stu-id="6d2bc-138">QAT menu events are not exposed.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6d2bc-139">Commande</span><span class="sxs-lookup"><span data-stu-id="6d2bc-139">Command</span></span></td>
<td><span data-ttu-id="6d2bc-140">ID de commande</span><span class="sxs-lookup"><span data-stu-id="6d2bc-140">Command ID</span></span><br/> <span data-ttu-id="6d2bc-141">Nom de commande</span><span class="sxs-lookup"><span data-stu-id="6d2bc-141">Command name</span></span><br/> <span data-ttu-id="6d2bc-142">Verbe d’événement</span><span class="sxs-lookup"><span data-stu-id="6d2bc-142">Event verb</span></span><br/> <span data-ttu-id="6d2bc-143">L’un des emplacements d’événements suivants :</span><span class="sxs-lookup"><span data-stu-id="6d2bc-143">One of the following event locations:</span></span>
<ul>
<li><span data-ttu-id="6d2bc-144">DERNIER</span><span class="sxs-lookup"><span data-stu-id="6d2bc-144">RIBBON</span></span></li>
<li><span data-ttu-id="6d2bc-145">QUICKACCESSTOOLBAR</span><span class="sxs-lookup"><span data-stu-id="6d2bc-145">QUICKACCESSTOOLBAR</span></span></li>
<li><span data-ttu-id="6d2bc-146">APPLICATIONMENU</span><span class="sxs-lookup"><span data-stu-id="6d2bc-146">APPLICATIONMENU</span></span></li>
<li><span data-ttu-id="6d2bc-147">CONTEXTPOPUP</span><span class="sxs-lookup"><span data-stu-id="6d2bc-147">CONTEXTPOPUP</span></span></li>
</ul>
<br/> <span data-ttu-id="6d2bc-148">ID de commande parent</span><span class="sxs-lookup"><span data-stu-id="6d2bc-148">Parent Command ID</span></span><br/> <span data-ttu-id="6d2bc-149">Nom de la commande parente</span><span class="sxs-lookup"><span data-stu-id="6d2bc-149">Parent Command name</span></span><br/> <span data-ttu-id="6d2bc-150">L’une des méthodes d’appel suivantes :</span><span class="sxs-lookup"><span data-stu-id="6d2bc-150">One of the following invoke methods:</span></span>
<ul>
<li><span data-ttu-id="6d2bc-151">Cliquez sur</span><span class="sxs-lookup"><span data-stu-id="6d2bc-151">CLICK</span></span></li>
<li><span data-ttu-id="6d2bc-152">KEYTIP</span><span class="sxs-lookup"><span data-stu-id="6d2bc-152">KEYTIP</span></span></li>
<li><span data-ttu-id="6d2bc-153">CLAVIER</span><span class="sxs-lookup"><span data-stu-id="6d2bc-153">KEYBOARD</span></span></li>
<li><span data-ttu-id="6d2bc-154">INTERFACE</span><span class="sxs-lookup"><span data-stu-id="6d2bc-154">TOUCH</span></span></li>
</ul>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="6d2bc-155">Les galeries d’éléments et les zones de liste déroulante incluent l’index d’élément sélectionné, mais n’incluent pas les valeurs de chaîne et d’entier.</span><span class="sxs-lookup"><span data-stu-id="6d2bc-155">Item galleries and combo boxes include the selected item index but do not include string and integer values.</span></span> <span data-ttu-id="6d2bc-156">Les jointures n’incluent pas la valeur entière.</span><span class="sxs-lookup"><span data-stu-id="6d2bc-156">Spinners do not include the integer value.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d2bc-157">Ruban réduit</span><span class="sxs-lookup"><span data-stu-id="6d2bc-157">Ribbon minimized</span></span></td>
<td><span data-ttu-id="6d2bc-158">Verbe d’événement</span><span class="sxs-lookup"><span data-stu-id="6d2bc-158">Event verb</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6d2bc-159">Ruban développé (bouton de développement cliqué ou appui sur épinglé)</span><span class="sxs-lookup"><span data-stu-id="6d2bc-159">Ribbon expanded (expand button clicked or tap pinned)</span></span></td>
<td><span data-ttu-id="6d2bc-160">Verbe d’événement</span><span class="sxs-lookup"><span data-stu-id="6d2bc-160">Event verb</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6d2bc-161">Mode d’application basculé</span><span class="sxs-lookup"><span data-stu-id="6d2bc-161">Application mode switched</span></span></td>
<td><span data-ttu-id="6d2bc-162">Verbe d’événement</span><span class="sxs-lookup"><span data-stu-id="6d2bc-162">Event verb</span></span><br/> <span data-ttu-id="6d2bc-163">ID de mode (valeur définie par <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes"><strong>SetModes</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="6d2bc-163">Mode ID (value set through <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes"><strong>SetModes</strong></a>)</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="6d2bc-164">L’application est chargée de décompresser cet entier pour déterminer les modes qui ont été définis.</span><span class="sxs-lookup"><span data-stu-id="6d2bc-164">The application is responsible for unpacking this integer to determine which modes were set.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6d2bc-165">Info-bulle affichée</span><span class="sxs-lookup"><span data-stu-id="6d2bc-165">Tooltip displayed</span></span></td>
<td><span data-ttu-id="6d2bc-166">Verbe d’événement</span><span class="sxs-lookup"><span data-stu-id="6d2bc-166">Event verb</span></span><br/> <span data-ttu-id="6d2bc-167">ID de commande parent</span><span class="sxs-lookup"><span data-stu-id="6d2bc-167">Parent Command ID</span></span><br/> <span data-ttu-id="6d2bc-168">Nom de la commande parente</span><span class="sxs-lookup"><span data-stu-id="6d2bc-168">Parent Command name</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="6d2bc-169">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6d2bc-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d2bc-170">Guides du développeur de l’infrastructure de ruban Windows</span><span class="sxs-lookup"><span data-stu-id="6d2bc-170">Windows Ribbon Framework Developer Guides</span></span>](windowsribbon-guides-entry.md)
</dt> <dt>

[<span data-ttu-id="6d2bc-171">Déclaration des commandes et des contrôles avec le balisage du ruban</span><span class="sxs-lookup"><span data-stu-id="6d2bc-171">Declaring Commands and Controls with Ribbon Markup</span></span>](./windowsribbon-schema.md)
</dt> <dt>

[<span data-ttu-id="6d2bc-172">Instructions relatives à l’expérience utilisateur du ruban</span><span class="sxs-lookup"><span data-stu-id="6d2bc-172">Ribbon User Experience Guidelines</span></span>](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[<span data-ttu-id="6d2bc-173">Processus de conception du ruban</span><span class="sxs-lookup"><span data-stu-id="6d2bc-173">Ribbon Design Process</span></span>](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

