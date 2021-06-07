---
title: Messages d'avertissement
description: Un message d’avertissement est une boîte de dialogue modale, un message sur place, une notification ou une bulle qui avertit l’utilisateur d’une condition susceptible de provoquer un problème à l’avenir.
ms.assetid: 4a2c3be9-9dc6-4d62-bd3d-72a2e5b621f4
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 42f7c669a68790ec290f931165b4aa937b5008d5
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524503"
---
# <a name="warning-messages"></a><span data-ttu-id="6da32-103">Messages d'avertissement</span><span class="sxs-lookup"><span data-stu-id="6da32-103">Warning Messages</span></span>

> [!NOTE]
> <span data-ttu-id="6da32-104">Ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows.</span><span class="sxs-lookup"><span data-stu-id="6da32-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="6da32-105">La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.</span><span class="sxs-lookup"><span data-stu-id="6da32-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="6da32-106">Un message d’avertissement est une boîte de dialogue modale, un message sur place, une notification ou une bulle qui avertit l’utilisateur d’une condition susceptible de provoquer un problème à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="6da32-106">A warning message is a modal dialog box, in-place message, notification, or balloon that alerts the user of a condition that might cause a problem in the future.</span></span>

![capture d’écran d’un message d’avertissement standard](images/mess-warn-image1.png)

<span data-ttu-id="6da32-108">Message d’avertissement modal standard.</span><span class="sxs-lookup"><span data-stu-id="6da32-108">A typical modal warning message.</span></span>

<span data-ttu-id="6da32-109">La caractéristique fondamentale des avertissements est qu’ils impliquent le risque de perdre un ou plusieurs des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="6da32-109">The fundamental characteristic of warnings is that they involve the risk of losing one or more of the following:</span></span>

-   <span data-ttu-id="6da32-110">Une ressource précieuse, telle que des données financières ou autres données importantes.</span><span class="sxs-lookup"><span data-stu-id="6da32-110">A valuable asset, such as important financial or other data.</span></span>
-   <span data-ttu-id="6da32-111">Accès ou intégrité du système.</span><span class="sxs-lookup"><span data-stu-id="6da32-111">System access or integrity.</span></span>
-   <span data-ttu-id="6da32-112">Confidentialité ou contrôle des informations confidentielles.</span><span class="sxs-lookup"><span data-stu-id="6da32-112">Privacy or control over confidential information.</span></span>
-   <span data-ttu-id="6da32-113">Temps de l’utilisateur (quantité significative, par exemple, 30 secondes ou plus).</span><span class="sxs-lookup"><span data-stu-id="6da32-113">User's time (a significant amount, such as 30 seconds or more).</span></span>

<span data-ttu-id="6da32-114">En revanche, une confirmation est une boîte de dialogue modale qui demande si l’utilisateur souhaite effectuer une action.</span><span class="sxs-lookup"><span data-stu-id="6da32-114">By contrast, a confirmation is a modal dialog box that asks if the user wants to proceed with an action.</span></span> <span data-ttu-id="6da32-115">Certains types d’avertissements sont présentés comme des confirmations et, dans ce cas, les instructions de confirmation s’appliquent également.</span><span class="sxs-lookup"><span data-stu-id="6da32-115">Some types of warnings are presented as confirmations, and if so, the confirmation guidelines also apply.</span></span>

<span data-ttu-id="6da32-116">**Remarque :** Les instructions relatives aux [boîtes de dialogue](win-dialog-box.md), aux [confirmations](mess-confirm.md) [, aux](mess-error.md)[icônes standard](vis-std-icons.md), aux [notifications](mess-notif.md)et à la [mise en page](vis-layout.md) sont présentées dans des articles distincts.</span><span class="sxs-lookup"><span data-stu-id="6da32-116">**Note:** Guidelines related to [dialog boxes](win-dialog-box.md), [confirmations](mess-confirm.md), [error messages](mess-error.md)[standard icons](vis-std-icons.md), [notifications](mess-notif.md), and [layout](vis-layout.md) are presented in separate articles.</span></span>

## <a name="is-this-the-right-user-interface"></a><span data-ttu-id="6da32-117">S’agit-il de l’interface utilisateur appropriée ?</span><span class="sxs-lookup"><span data-stu-id="6da32-117">Is this the right user interface?</span></span>

<span data-ttu-id="6da32-118">Pour vous décider, posez-vous les questions suivantes :</span><span class="sxs-lookup"><span data-stu-id="6da32-118">To decide, consider these questions:</span></span>

-   <span data-ttu-id="6da32-119">**L’utilisateur est-il alerté d’une condition susceptible de provoquer un problème à l’avenir ?**</span><span class="sxs-lookup"><span data-stu-id="6da32-119">**Is the user being alerted of a condition that might cause a problem in the future?**</span></span> <span data-ttu-id="6da32-120">Si ce n’est pas le cas, le message n’est pas un avertissement.</span><span class="sxs-lookup"><span data-stu-id="6da32-120">If not, the message isn't a warning.</span></span>
-   <span data-ttu-id="6da32-121">**L’interface utilisateur présente-t-elle une erreur ou un problème qui s’est déjà produit ?**</span><span class="sxs-lookup"><span data-stu-id="6da32-121">**Is the UI presenting an error or problem that has already occurred?**</span></span> <span data-ttu-id="6da32-122">Dans ce cas, utilisez un message d’erreur à la place.</span><span class="sxs-lookup"><span data-stu-id="6da32-122">If so, use an error message instead.</span></span>
-   <span data-ttu-id="6da32-123">**Les utilisateurs sont susceptibles d’effectuer une action ou de modifier leur comportement en tant que résultat du message ?**</span><span class="sxs-lookup"><span data-stu-id="6da32-123">**Are users likely to perform an action or change their behavior as the result of the message?**</span></span> <span data-ttu-id="6da32-124">Si ce n’est pas le cas, la condition ne justifie pas l’interruption de l’utilisateur. il est donc préférable de supprimer l’avertissement.</span><span class="sxs-lookup"><span data-stu-id="6da32-124">If not, the condition doesn't justify interrupting the user so it's better to suppress the warning.</span></span>
-   <span data-ttu-id="6da32-125">**La condition correspond-elle au résultat direct d’une action lancée par l’utilisateur ?**</span><span class="sxs-lookup"><span data-stu-id="6da32-125">**Is the condition the direct result of an action initiated by the user?**</span></span> <span data-ttu-id="6da32-126">Si ce n’est pas le cas, envisagez d’utiliser [des notifications d’événements non critiques](mess-notif.md).</span><span class="sxs-lookup"><span data-stu-id="6da32-126">If not, consider using a [non-critical event notifications](mess-notif.md).</span></span>
-   <span data-ttu-id="6da32-127">**La condition est-elle une condition spéciale dans un contrôle ?**</span><span class="sxs-lookup"><span data-stu-id="6da32-127">**Is the condition a special condition in a control?**</span></span> <span data-ttu-id="6da32-128">Si c’est le cas, utilisez plutôt une [bulle](ctrl-balloons.md) .</span><span class="sxs-lookup"><span data-stu-id="6da32-128">If so, use a [balloon](ctrl-balloons.md) instead.</span></span>
-   <span data-ttu-id="6da32-129">**Pour les confirmations, l’utilisateur est-il sur le sujet d’effectuer une action risquée ?**</span><span class="sxs-lookup"><span data-stu-id="6da32-129">**For confirmations, is the user about to perform a risky action?**</span></span> <span data-ttu-id="6da32-130">Dans ce cas, un avertissement est approprié si l’action a des conséquences importantes ou si elle ne peut pas être facilement annulée.</span><span class="sxs-lookup"><span data-stu-id="6da32-130">If so, a warning is appropriate if the action has significant consequences or cannot be easily undone.</span></span>
-   <span data-ttu-id="6da32-131">**Pour les autres types d’avertissements, l’utilisateur doit-il agir maintenant ou dans le futur ?**</span><span class="sxs-lookup"><span data-stu-id="6da32-131">**For other types of warnings, does the user need to act now or in the immediate future?**</span></span> <span data-ttu-id="6da32-132">N’affiche pas les avertissements si les utilisateurs peuvent continuer à travailler de manière productive sans problèmes immédiats.</span><span class="sxs-lookup"><span data-stu-id="6da32-132">Don't display warnings if users can continue to work productively without immediate problems.</span></span> <span data-ttu-id="6da32-133">Différez l’avertissement jusqu’à ce que la condition soit plus immédiate et pertinente.</span><span class="sxs-lookup"><span data-stu-id="6da32-133">Postpone the warning until the condition is more immediate and relevant.</span></span>

## <a name="design-concepts"></a><span data-ttu-id="6da32-134">Principes de conception</span><span class="sxs-lookup"><span data-stu-id="6da32-134">Design concepts</span></span>

### <a name="avoid-overwarning"></a><span data-ttu-id="6da32-135">Éviter le suravertissement</span><span class="sxs-lookup"><span data-stu-id="6da32-135">Avoid overwarning</span></span>

<span data-ttu-id="6da32-136">Nous prévoyons des avertissements dans les programmes Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="6da32-136">We overwarn in Microsoft Windows programs.</span></span> <span data-ttu-id="6da32-137">Le programme Windows classique présente des avertissements apparemment partout, en vous avertissant des choses qui ont une importance minime.</span><span class="sxs-lookup"><span data-stu-id="6da32-137">The typical Windows program has warnings seemingly everywhere, warning about things that have little significance.</span></span> <span data-ttu-id="6da32-138">Dans certains programmes, presque toutes les questions sont présentées sous la forme d’un avertissement.</span><span class="sxs-lookup"><span data-stu-id="6da32-138">In some programs, nearly every question is presented as a warning.</span></span> <span data-ttu-id="6da32-139">Le suravertissement permet d’utiliser un programme comme une activité dangereuse et de délivrer des problèmes réellement significatifs.</span><span class="sxs-lookup"><span data-stu-id="6da32-139">Overwarning makes using a program feel like a hazardous activity, and it detracts from truly significant issues.</span></span>

<span data-ttu-id="6da32-140">**Incorrect :**</span><span class="sxs-lookup"><span data-stu-id="6da32-140">**Incorrect:**</span></span>

![<span data-ttu-id="6da32-141">capture d’écran d’un message d’avertissement inutile</span><span class="sxs-lookup"><span data-stu-id="6da32-141">screen shot of an unnecessary warning message</span></span> ](images/mess-warn-image2.png)

<span data-ttu-id="6da32-142">Un suravertissement rend votre programme dangereux et similaire à celui qui a été conçu par les juristes.</span><span class="sxs-lookup"><span data-stu-id="6da32-142">Overwarning makes your program feel hazardous and look like it was designed by lawyers.</span></span>

<span data-ttu-id="6da32-143">Le seul risque de perte de données ou un problème à l’avenir est insuffisant pour appeler un avertissement.</span><span class="sxs-lookup"><span data-stu-id="6da32-143">The mere potential for data loss or a future problem alone is insufficient to call for a warning.</span></span> <span data-ttu-id="6da32-144">En outre, les résultats indésirables doivent être inattendus ou involontaires, et ne peuvent pas être facilement corrigés.</span><span class="sxs-lookup"><span data-stu-id="6da32-144">Additionally, any undesirable results should be unexpected or unintended, and not easily corrected.</span></span> <span data-ttu-id="6da32-145">Dans le cas contraire, une erreur de l’utilisateur peut être interprétée pour entraîner une perte de données ou un problème potentiel et mériter un avertissement.</span><span class="sxs-lookup"><span data-stu-id="6da32-145">Otherwise, just about any user mistake could be construed to result in data loss or a potential problem of some kind and merit a warning.</span></span>

### <a name="characteristics-of-good-warnings"></a><span data-ttu-id="6da32-146">Caractéristiques des avertissements corrects</span><span class="sxs-lookup"><span data-stu-id="6da32-146">Characteristics of good warnings</span></span>

<span data-ttu-id="6da32-147">Bons avertissements :</span><span class="sxs-lookup"><span data-stu-id="6da32-147">Good warnings:</span></span>

-   <span data-ttu-id="6da32-148">**Impliquent un risque.**</span><span class="sxs-lookup"><span data-stu-id="6da32-148">**Involve risk.**</span></span> <span data-ttu-id="6da32-149">Des avertissements bien avertisent les utilisateurs d’un événement important.</span><span class="sxs-lookup"><span data-stu-id="6da32-149">Good warnings alert users of something significant.</span></span>

<span data-ttu-id="6da32-150">**Incorrect :**</span><span class="sxs-lookup"><span data-stu-id="6da32-150">**Incorrect:**</span></span>

![<span data-ttu-id="6da32-151">capture d’écran de’voulez-vous quitter ? '</span><span class="sxs-lookup"><span data-stu-id="6da32-151">screen shot of 'do you want to exit?'</span></span> <span data-ttu-id="6da32-152">warning</span><span class="sxs-lookup"><span data-stu-id="6da32-152">warning</span></span> ](images/mess-warn-image3.png)

<span data-ttu-id="6da32-153">Et alors?</span><span class="sxs-lookup"><span data-stu-id="6da32-153">So what?</span></span> <span data-ttu-id="6da32-154">Cette confirmation suppose que les utilisateurs quittent souvent les programmes par accident.</span><span class="sxs-lookup"><span data-stu-id="6da32-154">This confirmation assumes that users often exit programs by accident.</span></span>

-   <span data-ttu-id="6da32-155">**Avoir une pertinence immédiate.**</span><span class="sxs-lookup"><span data-stu-id="6da32-155">**Have immediate relevance.**</span></span> <span data-ttu-id="6da32-156">Non seulement les utilisateurs doivent se soucier, mais ils doivent s’en soucier maintenant.</span><span class="sxs-lookup"><span data-stu-id="6da32-156">Not only do users have to care, they have to care now.</span></span> <span data-ttu-id="6da32-157">Les utilisateurs ne sont généralement pas intéressés par les problèmes qu’ils peuvent rencontrer plus tard tant qu’ils peuvent effectuer leur travail maintenant.</span><span class="sxs-lookup"><span data-stu-id="6da32-157">Users typically aren't interested in problems they might have later as long as they can do their work now.</span></span>

<span data-ttu-id="6da32-158">**Incorrect :**</span><span class="sxs-lookup"><span data-stu-id="6da32-158">**Incorrect:**</span></span>

![<span data-ttu-id="6da32-159">capture d’écran de la batterie-avertissement de faible-entrée à trois heures</span><span class="sxs-lookup"><span data-stu-id="6da32-159">screen shot of battery-low-in-three-hours warning</span></span> ](images/mess-warn-image4.png)

<span data-ttu-id="6da32-160">Dans ce cas, il est préférable d’avertir l’utilisateur en trois heures.</span><span class="sxs-lookup"><span data-stu-id="6da32-160">In this case, it's better just to warn the user in three hours.</span></span>

-   <span data-ttu-id="6da32-161">**Mène à l’action.**</span><span class="sxs-lookup"><span data-stu-id="6da32-161">**Lead to action.**</span></span> <span data-ttu-id="6da32-162">Il y a un nom que les utilisateurs doivent faire ou connaître en tant que résultat de l’avertissement.</span><span class="sxs-lookup"><span data-stu-id="6da32-162">There is something users must do or be aware of as the result of the warning.</span></span> <span data-ttu-id="6da32-163">Ils doivent peut-être prendre une mesure à l’avenir immédiatement ou ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="6da32-163">Perhaps they must take an action now or sometime in the immediate future.</span></span> <span data-ttu-id="6da32-164">Peut-être qu’ils exécutent une tâche différemment.</span><span class="sxs-lookup"><span data-stu-id="6da32-164">Perhaps they will perform a task differently as a result.</span></span> <span data-ttu-id="6da32-165">La conséquence de l’ignorance de l’avertissement doit être Clear.</span><span class="sxs-lookup"><span data-stu-id="6da32-165">The consequence of ignoring the warning should be clear.</span></span> <span data-ttu-id="6da32-166">Les avertissements sans action font simplement des utilisateurs le sentiment paranoïaques.</span><span class="sxs-lookup"><span data-stu-id="6da32-166">Warnings without actions just make users feel paranoid.</span></span>

<span data-ttu-id="6da32-167">**Incorrect :**</span><span class="sxs-lookup"><span data-stu-id="6da32-167">**Incorrect:**</span></span>

![<span data-ttu-id="6da32-168">capture d’écran de l’avertissement « Live Messenger est en cours d’exécution »</span><span class="sxs-lookup"><span data-stu-id="6da32-168">screen shot of 'live messenger is running' warning</span></span> ](images/mess-warn-image5.png)

<span data-ttu-id="6da32-169">Pourquoi cette notification a-t-elle un avertissement ?</span><span class="sxs-lookup"><span data-stu-id="6da32-169">Why is this notification a warning?</span></span> <span data-ttu-id="6da32-170">Que sont les utilisateurs censés faire (en plus de la préoccupation) ?</span><span class="sxs-lookup"><span data-stu-id="6da32-170">What are users supposed to do (beside worry)?</span></span>

-   <span data-ttu-id="6da32-171">**Ne sont pas évidents.**</span><span class="sxs-lookup"><span data-stu-id="6da32-171">**Are not obvious.**</span></span> <span data-ttu-id="6da32-172">N’affiche pas d’avertissement pour indiquer la conséquence évidente d’une action.</span><span class="sxs-lookup"><span data-stu-id="6da32-172">Don't display a warning to state the obvious consequence of an action.</span></span> <span data-ttu-id="6da32-173">Par exemple, supposons que les utilisateurs comprennent les conséquences de la non-exécution d’une tâche.</span><span class="sxs-lookup"><span data-stu-id="6da32-173">For example, assume users understand the consequences of not completing a task.</span></span>

<span data-ttu-id="6da32-174">**Incorrect :**</span><span class="sxs-lookup"><span data-stu-id="6da32-174">**Incorrect:**</span></span>

![<span data-ttu-id="6da32-175">capture d’écran de voulez-vous quitter l’Assistant ? tres</span><span class="sxs-lookup"><span data-stu-id="6da32-175">screen shot of do you want to exit wizard? warning</span></span> ](images/mess-warn-image6.png)

<span data-ttu-id="6da32-176">L’annulation d’un Assistant incomplet signifie que la tâche n’est pas terminée... qui savait ?</span><span class="sxs-lookup"><span data-stu-id="6da32-176">Canceling an incomplete wizard means the task doesn't get done...who knew?</span></span>

-   <span data-ttu-id="6da32-177">**Se produisent rarement.**</span><span class="sxs-lookup"><span data-stu-id="6da32-177">**Occur infrequently.**</span></span> <span data-ttu-id="6da32-178">Les avertissements de constante deviennent rapidement inefficaces et ennuyeux.</span><span class="sxs-lookup"><span data-stu-id="6da32-178">Constant warnings quickly become ineffective and annoying.</span></span> <span data-ttu-id="6da32-179">Les utilisateurs sont souvent plus concentrés pour se débarrasser de l’avertissement que pour résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="6da32-179">Users often become more focused on getting rid of the warning than addressing the problem.</span></span>

<span data-ttu-id="6da32-180">**Incorrect :**</span><span class="sxs-lookup"><span data-stu-id="6da32-180">**Incorrect:**</span></span>

![<span data-ttu-id="6da32-181">capture d’écran de l’avertissement « mettre à jour les signatures de virus »</span><span class="sxs-lookup"><span data-stu-id="6da32-181">screen shot of 'update virus signatures' warning</span></span> ](images/mess-warn-image7.png)

<span data-ttu-id="6da32-182">Les utilisateurs sont plus susceptibles de se concentrer sur l’avertissement que de résoudre le problème sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="6da32-182">Users are more likely to focus on getting rid of the warning than fixing the underlying problem.</span></span>

<span data-ttu-id="6da32-183">Un message qui n’a pas ces caractéristiques peut toujours être un bon message, ce qui n’est pas un bon avertissement.</span><span class="sxs-lookup"><span data-stu-id="6da32-183">A message that doesn't have these characteristics might still be a good message, just not a good warning.</span></span>

### <a name="determine-the-appropriate-message-type"></a><span data-ttu-id="6da32-184">Déterminer le type de message approprié</span><span class="sxs-lookup"><span data-stu-id="6da32-184">Determine the appropriate message type</span></span>

<span data-ttu-id="6da32-185">Certains problèmes peuvent être présentés sous la forme d’une erreur, d’un avertissement ou d’informations, en fonction de l’importance et de la formulation.</span><span class="sxs-lookup"><span data-stu-id="6da32-185">Some issues can be presented as an error, warning, or information, depending on the emphasis and phrasing.</span></span> <span data-ttu-id="6da32-186">Par exemple, supposons qu’une page Web ne peut pas charger un contrôle ActiveX non signé basé sur la configuration actuelle de Windows Internet Explorer :</span><span class="sxs-lookup"><span data-stu-id="6da32-186">For example, suppose a Web page cannot load an unsigned ActiveX control based on the current Windows Internet Explorer configuration:</span></span>

-   <span data-ttu-id="6da32-187">**Erreurs.**</span><span class="sxs-lookup"><span data-stu-id="6da32-187">**Error.**</span></span> <span data-ttu-id="6da32-188">« Cette page ne peut pas charger un contrôle ActiveX non signé ».</span><span class="sxs-lookup"><span data-stu-id="6da32-188">"This page cannot load an unsigned ActiveX control."</span></span> <span data-ttu-id="6da32-189">(Formulées en tant que problème existant.)</span><span class="sxs-lookup"><span data-stu-id="6da32-189">(Phrased as an existing problem.)</span></span>
-   <span data-ttu-id="6da32-190">**Tres.**</span><span class="sxs-lookup"><span data-stu-id="6da32-190">**Warning.**</span></span> <span data-ttu-id="6da32-191">« Cette page peut ne pas se comporter comme prévu, car Windows Internet Explorer n’est pas configuré pour charger des contrôles ActiveX non signés ».</span><span class="sxs-lookup"><span data-stu-id="6da32-191">"This page might not behave as expected because Windows Internet Explorer isn't configured to load unsigned ActiveX controls."</span></span> <span data-ttu-id="6da32-192">ou «autoriser cette page à installer un contrôle ActiveX non signé ?</span><span class="sxs-lookup"><span data-stu-id="6da32-192">or "Allow this page to install an unsigned ActiveX Control?</span></span> <span data-ttu-id="6da32-193">Cette opération à partir de sources non approuvées peut endommager votre ordinateur.»</span><span class="sxs-lookup"><span data-stu-id="6da32-193">Doing so from untrusted sources may harm your computer."</span></span> <span data-ttu-id="6da32-194">(Les deux formulées comme des conditions qui peuvent entraîner des problèmes futurs.)</span><span class="sxs-lookup"><span data-stu-id="6da32-194">(Both phrased as conditions that may cause future problems.)</span></span>
-   <span data-ttu-id="6da32-195">**Informations.**</span><span class="sxs-lookup"><span data-stu-id="6da32-195">**Information.**</span></span> <span data-ttu-id="6da32-196">« Vous avez configuré Windows Internet Explorer pour bloquer les contrôles ActiveX non signés ».</span><span class="sxs-lookup"><span data-stu-id="6da32-196">"You have configured Windows Internet Explorer to block unsigned ActiveX controls."</span></span> <span data-ttu-id="6da32-197">(Formulées en tant que déclaration de faits.)</span><span class="sxs-lookup"><span data-stu-id="6da32-197">(Phrased as a statement of fact.)</span></span>

<span data-ttu-id="6da32-198">**Pour déterminer le type de message approprié, concentrez-vous sur l’aspect le plus important du problème que les utilisateurs doivent connaître ou agir.**</span><span class="sxs-lookup"><span data-stu-id="6da32-198">**To determine the appropriate message type, focus on the most important aspect of the issue that users need to know or act upon.**</span></span> <span data-ttu-id="6da32-199">En règle générale, si un problème empêche l’utilisateur de continuer, vous devez le présenter comme une erreur. Si l’utilisateur peut continuer, présentez-le en tant qu’avertissement.</span><span class="sxs-lookup"><span data-stu-id="6da32-199">Typically, if an issue blocks the user from proceeding, you should present it as an error; if the user can proceed, present it as a warning.</span></span> <span data-ttu-id="6da32-200">Élaborez l' [instruction principale](text-ui.md) ou un autre texte correspondant en fonction de ce Focus, puis choisissez une icône ([standard](vis-std-icons.md) ou autre) qui correspond au texte.</span><span class="sxs-lookup"><span data-stu-id="6da32-200">Craft the [main instruction](text-ui.md) or other corresponding text based on that focus, then choose an icon ([standard](vis-std-icons.md) or otherwise) that matches the text.</span></span> <span data-ttu-id="6da32-201">Le texte d’instruction principal et les icônes doivent toujours correspondre.</span><span class="sxs-lookup"><span data-stu-id="6da32-201">The main instruction text and icons should always match.</span></span>

### <a name="be-specific"></a><span data-ttu-id="6da32-202">Être spécifique</span><span class="sxs-lookup"><span data-stu-id="6da32-202">Be specific</span></span>

<span data-ttu-id="6da32-203">Les avertissements sont plus intéressants lorsque les informations suivantes sont spécifiques et claires :</span><span class="sxs-lookup"><span data-stu-id="6da32-203">Warnings are more compelling when the following information is specific and clear:</span></span>

-   <span data-ttu-id="6da32-204">Source de l’avertissement.</span><span class="sxs-lookup"><span data-stu-id="6da32-204">The source of the warning.</span></span>
-   <span data-ttu-id="6da32-205">La condition et le problème potentiels spécifiques.</span><span class="sxs-lookup"><span data-stu-id="6da32-205">The specific condition and potential problem.</span></span>
-   <span data-ttu-id="6da32-206">Ce que l’utilisateur doit faire à son sujet.</span><span class="sxs-lookup"><span data-stu-id="6da32-206">What the user should do about it.</span></span>
-   <span data-ttu-id="6da32-207">Que se passe-t-il si l’utilisateur ne fait rien.</span><span class="sxs-lookup"><span data-stu-id="6da32-207">What happens if the user doesn't do anything.</span></span>

<span data-ttu-id="6da32-208">**Incorrect :**</span><span class="sxs-lookup"><span data-stu-id="6da32-208">**Incorrect:**</span></span>

![<span data-ttu-id="6da32-209">capture d’écran d’un avertissement vague de risque significatif</span><span class="sxs-lookup"><span data-stu-id="6da32-209">screen shot of vague warning of significant risk</span></span> ](images/mess-warn-image8.png)

<span data-ttu-id="6da32-210">Dans cet exemple, quel est le problème potentiel ?</span><span class="sxs-lookup"><span data-stu-id="6da32-210">In this example, what is the potential problem?</span></span> <span data-ttu-id="6da32-211">Qu’est-ce que l’utilisateur est censé faire, hormis le fait de ne pas utiliser le projecteur sur le réseau ?</span><span class="sxs-lookup"><span data-stu-id="6da32-211">What is the user supposed to do, aside from not using the projector over the network?</span></span> <span data-ttu-id="6da32-212">Sans aucune information spécifique, l’utilisateur peut se sentir mal à faire.</span><span class="sxs-lookup"><span data-stu-id="6da32-212">Without more specific information, all the user can do is feel bad about proceeding.</span></span>

<span data-ttu-id="6da32-213">**Correct :**</span><span class="sxs-lookup"><span data-stu-id="6da32-213">**Correct:**</span></span>

![<span data-ttu-id="6da32-214">capture d’écran de l’avertissement de problème et des conséquences</span><span class="sxs-lookup"><span data-stu-id="6da32-214">screen shot of warning of problem and consequences</span></span> ](images/mess-warn-image9.png)

<span data-ttu-id="6da32-215">Dans cet exemple, le problème et les conséquences sont clairs.</span><span class="sxs-lookup"><span data-stu-id="6da32-215">In this example, the problem and consequences are clear.</span></span>

<span data-ttu-id="6da32-216">Parfois, il y a un problème potentiel légitime, digne d’informant les utilisateurs, mais la solution et les conséquences ne sont pas connues.</span><span class="sxs-lookup"><span data-stu-id="6da32-216">Sometimes there is a legitimate potential problem worthy of informing users about, but the solution and consequences aren't known for sure.</span></span> <span data-ttu-id="6da32-217">Au lieu de donner un avertissement vague, soyez précis en donnant les informations les plus probables ou l’exemple le plus courant.</span><span class="sxs-lookup"><span data-stu-id="6da32-217">Rather than give a vague warning, be specific by giving the most likely information or the most common example.</span></span>

<span data-ttu-id="6da32-218">**Correct :**</span><span class="sxs-lookup"><span data-stu-id="6da32-218">**Correct:**</span></span>

![<span data-ttu-id="6da32-219">capture d’écran des avertissements et des solutions d’erreur réseau</span><span class="sxs-lookup"><span data-stu-id="6da32-219">screen shot of network error warning and solutions</span></span> ](images/mess-warn-image10.png)

<span data-ttu-id="6da32-220">Dans cet exemple, l’avertissement est rendu spécifique en fournissant la solution la plus probable.</span><span class="sxs-lookup"><span data-stu-id="6da32-220">In this example, the warning is made specific by providing the most likely solution.</span></span>

<span data-ttu-id="6da32-221">Toutefois, dans ces cas-là, utilisez une formulation qui indique qu’il existe d’autres possibilités.</span><span class="sxs-lookup"><span data-stu-id="6da32-221">However, in such cases, use wording that indicates that there are other possibilities.</span></span> <span data-ttu-id="6da32-222">Dans le cas contraire, les utilisateurs peuvent être trompeurs.</span><span class="sxs-lookup"><span data-stu-id="6da32-222">Otherwise, users might be misled.</span></span>

<span data-ttu-id="6da32-223">**Incorrect :**</span><span class="sxs-lookup"><span data-stu-id="6da32-223">**Incorrect:**</span></span>

![<span data-ttu-id="6da32-224">capture d’écran de l’avertissement de déconnexion du câble réseau</span><span class="sxs-lookup"><span data-stu-id="6da32-224">screen shot of network cable unplugged warning</span></span> ](images/mess-warn-image11.png)

<span data-ttu-id="6da32-225">**Correct :**</span><span class="sxs-lookup"><span data-stu-id="6da32-225">**Correct:**</span></span>

![<span data-ttu-id="6da32-226">la capture d’écran du câble est peut-être débranchée</span><span class="sxs-lookup"><span data-stu-id="6da32-226">screen shot of cable might be unplugged warning</span></span> ](images/mess-warn-image12.png)

<span data-ttu-id="6da32-227">Dans l’exemple incorrect, les utilisateurs sont confondus si le câble est bien branché.</span><span class="sxs-lookup"><span data-stu-id="6da32-227">In the incorrect example, users will be confused if the cable is clearly plugged in.</span></span>

<span data-ttu-id="6da32-228">**Si vous ne faites que deux choses...**</span><span class="sxs-lookup"><span data-stu-id="6da32-228">**If you do only two things...**</span></span>

1. <span data-ttu-id="6da32-229">Ne pas avertir.</span><span class="sxs-lookup"><span data-stu-id="6da32-229">Don't overwarn.</span></span> <span data-ttu-id="6da32-230">Limitez les avertissements aux conditions qui impliquent un risque et qui sont immédiatement pertinentes, exploitables, non évidentes et peu fréquentes.</span><span class="sxs-lookup"><span data-stu-id="6da32-230">Limit warnings to conditions that involve risk and are immediately relevant, actionable, not obvious, and infrequent.</span></span> <span data-ttu-id="6da32-231">Sinon, supprimez ou reformulez le message.</span><span class="sxs-lookup"><span data-stu-id="6da32-231">Otherwise, remove or rephrase the message.</span></span>

2. <span data-ttu-id="6da32-232">Fournir des informations utiles spécifiques.</span><span class="sxs-lookup"><span data-stu-id="6da32-232">Provide specific, useful information.</span></span>

## <a name="usage-patterns"></a><span data-ttu-id="6da32-233">Modèles d’usage</span><span class="sxs-lookup"><span data-stu-id="6da32-233">Usage patterns</span></span>

<span data-ttu-id="6da32-234">Les avertissements ont plusieurs modèles d’utilisation :</span><span class="sxs-lookup"><span data-stu-id="6da32-234">Warnings have several usage patterns:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6da32-235"><strong>Prise de conscience</strong></span><span class="sxs-lookup"><span data-stu-id="6da32-235"><strong>Awareness</strong></span></span><br/> <span data-ttu-id="6da32-236">Rendre l’utilisateur conscient d’une condition ou d’un problème potentiel, mais l’utilisateur n’a peut-être pas à faire quoi que ce soit.</span><span class="sxs-lookup"><span data-stu-id="6da32-236">Make user aware of a condition or potential problem, but user may not have to do anything now.</span></span> <br/></td>
<td><img src="images/mess-warn-image13.png" alt="Screen shot of warning of network problems " /><br/> <img src="images/mess-warn-image14.png" alt="Screen shot of low-battery warning " /><br/> <img src="images/mess-warn-image15.png" alt="Screen shot of &#39;caps-lock-is-on&#39; warning " /><br/> <img src="images/mess-warn-image16.png" alt="Screen shot of &#39;TPM-not-found&#39; warning " /><br/> <span data-ttu-id="6da32-237">Exemples d’avertissements de sensibilisation.</span><span class="sxs-lookup"><span data-stu-id="6da32-237">Examples of awareness warnings.</span></span><br/> <span data-ttu-id="6da32-238">Les avertissements de sensibilisation présentent la présentation suivante :</span><span class="sxs-lookup"><span data-stu-id="6da32-238">Awareness warnings have the following presentation:</span></span> <br/>
<ul>
<li><span data-ttu-id="6da32-239"><strong>Instruction principale :</strong> Décrivez la condition ou le problème potentiel.</span><span class="sxs-lookup"><span data-stu-id="6da32-239"><strong>Main instruction:</strong> Describe the condition or potential problem.</span></span></li>
<li><span data-ttu-id="6da32-240"><strong>Instructions supplémentaires :</strong> Expliquez l’implication et pourquoi elle est importante.</span><span class="sxs-lookup"><span data-stu-id="6da32-240"><strong>Supplemental instruction:</strong> Explain the implication and why it is important.</span></span></li>
<li><span data-ttu-id="6da32-241"><strong>Boutons de validation :</strong> Plus.</span><span class="sxs-lookup"><span data-stu-id="6da32-241"><strong>Commit buttons:</strong> Close.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6da32-242"><strong>Prévention des erreurs</strong></span><span class="sxs-lookup"><span data-stu-id="6da32-242"><strong>Error prevention</strong></span></span><br/> <span data-ttu-id="6da32-243">N’oubliez pas que l’utilisateur a des informations qui peuvent empêcher un problème, en particulier quand vous faites des choix.</span><span class="sxs-lookup"><span data-stu-id="6da32-243">Make user aware of information that might prevent a problem, especially when making choices.</span></span> <br/></td>
<td><span data-ttu-id="6da32-244">Les avertissements de prévention des erreurs sont mieux présentés à l’aide d’une icône d’avertissement sur place et du texte explicatif.</span><span class="sxs-lookup"><span data-stu-id="6da32-244">Error prevention warnings are best presented using an in-place warning icon and explanatory text.</span></span> <br/> <img src="images/mess-warn-image17.png" alt="Screen shot of Not-enough-free-space warning " /><br/> <img src="images/mess-warn-image18.png" alt="Screen shot of Use-installation-CD warning " /><br/> <span data-ttu-id="6da32-245">Exemples d’avertissements de prévention d’erreur.</span><span class="sxs-lookup"><span data-stu-id="6da32-245">Examples of error prevention warnings.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6da32-246"><strong>Problème imminent</strong></span><span class="sxs-lookup"><span data-stu-id="6da32-246"><strong>Imminent problem</strong></span></span><br/> <span data-ttu-id="6da32-247">L’utilisateur doit effectuer une opération pour éviter un problème imminent.</span><span class="sxs-lookup"><span data-stu-id="6da32-247">The user needs to do something now to prevent an imminent problem.</span></span> <br/></td>
<td><img src="images/mess-warn-image19.png" alt="Screen shot of Close-programs warning " /><br/> <span data-ttu-id="6da32-248">Exemple d’avertissement de problème imminent.</span><span class="sxs-lookup"><span data-stu-id="6da32-248">An example of an imminent problem warning.</span></span><br/> <span data-ttu-id="6da32-249">Les avertissements de problèmes imminents présentent la présentation suivante :</span><span class="sxs-lookup"><span data-stu-id="6da32-249">Imminent problem warnings have the following presentation:</span></span> <br/>
<ul>
<li><span data-ttu-id="6da32-250"><strong>Instruction principale :</strong> Décrivez ce que l’utilisateur doit faire maintenant.</span><span class="sxs-lookup"><span data-stu-id="6da32-250"><strong>Main instruction:</strong> Describe what the user needs to do now.</span></span></li>
<li><span data-ttu-id="6da32-251"><strong>Instructions supplémentaires :</strong> Expliquez la condition et pourquoi elle est importante.</span><span class="sxs-lookup"><span data-stu-id="6da32-251"><strong>Supplemental instruction:</strong> Explain the condition and why it is important.</span></span></li>
<li><span data-ttu-id="6da32-252"><strong>Boutons de validation :</strong> Un bouton de commande ou un lien de commande pour chaque option, ou OK si l’action se produit en dehors de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="6da32-252"><strong>Commit buttons:</strong> A command button or command link for each option, or OK if the action occurs outside the dialog box.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6da32-253"><strong>Confirmation de l’action risquée</strong></span><span class="sxs-lookup"><span data-stu-id="6da32-253"><strong>Risky action confirmation</strong></span></span><br/> <span data-ttu-id="6da32-254">Confirmez que l’utilisateur souhaite effectuer une action qui présente un risque et ne peut pas être facilement annulée.</span><span class="sxs-lookup"><span data-stu-id="6da32-254">Confirm that the user wants to proceed with an action that has some risk and can't be easily undone.</span></span> <br/></td>
<td><img src="images/mess-warn-image20.png" alt="Screen shot of Formatting-will-erase-data warning " /><br/> <span data-ttu-id="6da32-255">Exemple de confirmation d’action risquée.</span><span class="sxs-lookup"><span data-stu-id="6da32-255">An example of risky action confirmation.</span></span><br/> <span data-ttu-id="6da32-256">Les confirmations d’action risquées ont la présentation suivante :</span><span class="sxs-lookup"><span data-stu-id="6da32-256">Risky action confirmations have the following presentation:</span></span> <br/>
<ul>
<li><span data-ttu-id="6da32-257"><strong>Instruction principale :</strong> Posez une question pour déterminer si l’utilisateur souhaite continuer.</span><span class="sxs-lookup"><span data-stu-id="6da32-257"><strong>Main instruction:</strong> Ask a question to determine if the user wants to proceed.</span></span></li>
<li><span data-ttu-id="6da32-258"><strong>Instructions supplémentaires :</strong> Expliquez les raisons les plus évidentes pour lesquelles l’utilisateur peut ne pas vouloir continuer.</span><span class="sxs-lookup"><span data-stu-id="6da32-258"><strong>Supplemental instruction:</strong> Explain any non-obvious reasons why the user might not want to proceed.</span></span></li>
<li><span data-ttu-id="6da32-259"><strong>Boutons de validation :</strong> Oui, non.</span><span class="sxs-lookup"><span data-stu-id="6da32-259"><strong>Commit buttons:</strong> Yes, No.</span></span></li>
</ul>
<span data-ttu-id="6da32-260">Pour obtenir des instructions sur ce modèle, consultez <a href="mess-confirm.md">confirmations</a>.</span><span class="sxs-lookup"><span data-stu-id="6da32-260">For guidelines on this pattern, see <a href="mess-confirm.md">Confirmations</a>.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="guidelines"></a><span data-ttu-id="6da32-261">Consignes</span><span class="sxs-lookup"><span data-stu-id="6da32-261">Guidelines</span></span>

### <a name="presentation"></a><span data-ttu-id="6da32-262">Présentation</span><span class="sxs-lookup"><span data-stu-id="6da32-262">Presentation</span></span>

-   <span data-ttu-id="6da32-263">**Choisissez l’interface utilisateur de la présentation en fonction du type d’informations :**</span><span class="sxs-lookup"><span data-stu-id="6da32-263">**Choose the presentation UI based on the type of information:**</span></span>



| <span data-ttu-id="6da32-264">Interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="6da32-264">User interface</span></span>  | <span data-ttu-id="6da32-265">Idéal pour</span><span class="sxs-lookup"><span data-stu-id="6da32-265">Best used for</span></span> |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6da32-266">Boîtes de dialogue modales</span><span class="sxs-lookup"><span data-stu-id="6da32-266">Modal dialog boxes</span></span><br/> | <span data-ttu-id="6da32-267">Avertissements critiques (y compris les confirmations) auxquels les utilisateurs doivent répondre maintenant.</span><span class="sxs-lookup"><span data-stu-id="6da32-267">Critical warnings (including confirmations) that users must respond to now.</span></span><br/>                                                 |
| <span data-ttu-id="6da32-268">Sur place</span><span class="sxs-lookup"><span data-stu-id="6da32-268">In-place</span></span><br/>           | <span data-ttu-id="6da32-269">Informations susceptibles d’empêcher un problème, en particulier lorsque les utilisateurs effectuent des choix.</span><span class="sxs-lookup"><span data-stu-id="6da32-269">Information that might prevent a problem, especially when users are making choices.</span></span><br/>                                         |
| <span data-ttu-id="6da32-270">Bande</span><span class="sxs-lookup"><span data-stu-id="6da32-270">Banners</span></span><br/>            | <span data-ttu-id="6da32-271">Informations susceptibles d’empêcher un problème, en particulier lorsqu’elles sont liées à la réalisation d’une tâche.</span><span class="sxs-lookup"><span data-stu-id="6da32-271">Information that might prevent a problem, especially when related to completing a task.</span></span><br/>                                     |
| <span data-ttu-id="6da32-272">Notifications</span><span class="sxs-lookup"><span data-stu-id="6da32-272">Notifications</span></span><br/>      | <span data-ttu-id="6da32-273">Événements ou États significatifs qui peuvent être ignorés en toute sécurité, au moins temporairement.</span><span class="sxs-lookup"><span data-stu-id="6da32-273">Significant events or status that can be safely ignored, at least temporarily.</span></span><br/>                                              |
| <span data-ttu-id="6da32-274">Bulles</span><span class="sxs-lookup"><span data-stu-id="6da32-274">Balloons</span></span><br/>           | <span data-ttu-id="6da32-275">Un contrôle est dans un État qui affecte l’entrée.</span><span class="sxs-lookup"><span data-stu-id="6da32-275">A control is in a state that affects input.</span></span> <span data-ttu-id="6da32-276">Cet État est probablement involontaire et l’utilisateur peut ne pas se rendre compte qu’une entrée est affectée.</span><span class="sxs-lookup"><span data-stu-id="6da32-276">This state is likely unintended and the user may not realize input is affected.</span></span><br/> |



 

-   <span data-ttu-id="6da32-277">**Pour les boîtes de dialogue modales :**</span><span class="sxs-lookup"><span data-stu-id="6da32-277">**For modal dialog boxes:**</span></span>
    -   <span data-ttu-id="6da32-278">**Utilisez les boîtes de dialogue de tâches chaque fois que nécessaire pour obtenir une apparence et une disposition cohérentes.**</span><span class="sxs-lookup"><span data-stu-id="6da32-278">**Use task dialogs whenever appropriate to achieve a consistent look and layout.**</span></span> <span data-ttu-id="6da32-279">Les boîtes de dialogue de tâches requièrent Windows Vista ou une version ultérieure, donc elles ne conviennent pas aux versions antérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="6da32-279">Task dialogs require Windows Vista or later, so they aren't suitable for earlier versions of Windows.</span></span>
    -   <span data-ttu-id="6da32-280">**Affichez un seul message d’avertissement par condition.**</span><span class="sxs-lookup"><span data-stu-id="6da32-280">**Display only one warning message per condition.**</span></span> <span data-ttu-id="6da32-281">Par exemple, affichez un avertissement unique qui explique complètement une condition au lieu de la décrire un détail à la fois par message.</span><span class="sxs-lookup"><span data-stu-id="6da32-281">For example, display a single warning that completely explains a condition instead of describing it one detail at a time per message.</span></span> <span data-ttu-id="6da32-282">L’affichage d’une séquence de boîtes de dialogue d’avertissement pour une seule condition est confus et ennuyeux.</span><span class="sxs-lookup"><span data-stu-id="6da32-282">Displaying a sequence of warning dialogs for a single condition is confusing and annoying.</span></span>
    -   <span data-ttu-id="6da32-283">**N’affichez pas un avertissement plus d’une fois par condition.**</span><span class="sxs-lookup"><span data-stu-id="6da32-283">**Don't display a warning more than once per condition.**</span></span> <span data-ttu-id="6da32-284">Les avertissements de constante deviennent rapidement inefficaces et ennuyeux.</span><span class="sxs-lookup"><span data-stu-id="6da32-284">Constant warnings quickly become ineffective and annoying.</span></span> <span data-ttu-id="6da32-285">Les utilisateurs sont souvent plus concentrés pour se débarrasser de l’avertissement que pour résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="6da32-285">Users often become more focused on getting rid of the warning than addressing the problem.</span></span> <span data-ttu-id="6da32-286">Si vous devez avertir à plusieurs reprises pour une seule condition, utilisez la [remontée progressive](mess-notif.md).</span><span class="sxs-lookup"><span data-stu-id="6da32-286">If you must warn repeatedly for a single condition, use [progressive escalation](mess-notif.md).</span></span>
-   <span data-ttu-id="6da32-287">**Ne pas accompagner les avertissements avec un effet sonore ou un bip.**</span><span class="sxs-lookup"><span data-stu-id="6da32-287">**Don't accompany warnings with a sound effect or beep.**</span></span> <span data-ttu-id="6da32-288">Cela est transférerez et inutile.</span><span class="sxs-lookup"><span data-stu-id="6da32-288">Doing so is jarring and unnecessary.</span></span>
    -   <span data-ttu-id="6da32-289">**Exception :** Si l’utilisateur doit répondre immédiatement, vous pouvez utiliser un effet sonore.</span><span class="sxs-lookup"><span data-stu-id="6da32-289">**Exception:** If the user must respond immediately, you can use a sound effect.</span></span>

### <a name="icons"></a><span data-ttu-id="6da32-290">Icônes</span><span class="sxs-lookup"><span data-stu-id="6da32-290">Icons</span></span>

-   <span data-ttu-id="6da32-291">Ne placez pas d’icône d’avertissement dans la barre de titre d’une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="6da32-291">Don't place a warning icon in the title bar of a dialog box.</span></span>
-   <span data-ttu-id="6da32-292">**Utilisez une icône d’avertissement.**</span><span class="sxs-lookup"><span data-stu-id="6da32-292">**Use a warning icon.**</span></span> <span data-ttu-id="6da32-293">Exceptions :</span><span class="sxs-lookup"><span data-stu-id="6da32-293">Exceptions:</span></span>
    -   <span data-ttu-id="6da32-294">Si l’avertissement concerne une fonctionnalité qui a une icône, vous pouvez utiliser l’icône de fonctionnalité avec une superposition d’avertissement.</span><span class="sxs-lookup"><span data-stu-id="6da32-294">If the warning is for a feature that has an icon, you can use the feature icon with a warning overlay.</span></span>

        <span data-ttu-id="6da32-295">**Correct :**</span><span class="sxs-lookup"><span data-stu-id="6da32-295">**Correct:**</span></span>

        ![<span data-ttu-id="6da32-296">capture d’écran de l’icône de verrou avec icône d’avertissement superposition</span><span class="sxs-lookup"><span data-stu-id="6da32-296">screen shot of lock icon with warning icon overlay</span></span> ](images/mess-warn-image21.png)

        <span data-ttu-id="6da32-297">Dans cet exemple, l’icône de fonctionnalité a une superposition d’avertissement.</span><span class="sxs-lookup"><span data-stu-id="6da32-297">In this example, the feature icon has a warning overlay.</span></span>

-   <span data-ttu-id="6da32-298">Pour les boîtes de dialogue modales avec un avertissement de note de bas de page, placez l’icône d’avertissement dans la note de bas de page au lieu de la zone de contenu.</span><span class="sxs-lookup"><span data-stu-id="6da32-298">For modal dialog boxes with a warning footnote, put the warning icon in the footnote instead of the content area.</span></span>

    <span data-ttu-id="6da32-299">**Correct :**</span><span class="sxs-lookup"><span data-stu-id="6da32-299">**Correct:**</span></span>

    ![<span data-ttu-id="6da32-300">capture d’écran de l’icône d’avertissement dans la note de bas de boîte de dialogue</span><span class="sxs-lookup"><span data-stu-id="6da32-300">screen shot of warning icon in dialog-box footnote</span></span> ](images/mess-warn-image22.png)

    <span data-ttu-id="6da32-301">Dans cet exemple, la note de bas de page contient l’icône d’avertissement.</span><span class="sxs-lookup"><span data-stu-id="6da32-301">In this example, the footnote has the warning icon.</span></span>

<span data-ttu-id="6da32-302">Pour obtenir des instructions et des exemples supplémentaires, consultez [icônes standard](vis-std-icons.md).</span><span class="sxs-lookup"><span data-stu-id="6da32-302">For more guidelines and examples, see [Standard Icons](vis-std-icons.md).</span></span>

### <a name="dont-show-this-message-again"></a><span data-ttu-id="6da32-303">Ne plus afficher ce message</span><span class="sxs-lookup"><span data-stu-id="6da32-303">Don't show this message again</span></span>

-   <span data-ttu-id="6da32-304">**Si une boîte de dialogue d’avertissement a besoin de cette option, réexaminez l’avertissement et sa fréquence.**</span><span class="sxs-lookup"><span data-stu-id="6da32-304">**If a warning dialog box needs this option, reconsider the warning and its frequency.**</span></span> <span data-ttu-id="6da32-305">S’il possède toutes les caractéristiques d’un bon avertissement (implique un risque, et qu’il est immédiatement pertinent, actionnable, pas évident et peu fréquent), il ne devrait pas être logique pour les utilisateurs de le supprimer.</span><span class="sxs-lookup"><span data-stu-id="6da32-305">If it has all the characteristics of a good warning (involves risk, and is immediately relevant, actionable, not obvious, and infrequent), it shouldn't make sense for users to suppress it.</span></span>

<span data-ttu-id="6da32-306">Pour plus d’instructions, consultez [boîtes de dialogue](win-dialog-box.md).</span><span class="sxs-lookup"><span data-stu-id="6da32-306">For more guidelines, see [Dialog Boxes](win-dialog-box.md).</span></span>

### <a name="progressive-disclosure"></a><span data-ttu-id="6da32-307">Affichage progressif</span><span class="sxs-lookup"><span data-stu-id="6da32-307">Progressive disclosure</span></span>

-   <span data-ttu-id="6da32-308">**Si vous devez inclure des informations avancées dans un message d’avertissement, révélez-les à l’aide de boutons de divulgation progressive** (par exemple, « afficher les détails »).</span><span class="sxs-lookup"><span data-stu-id="6da32-308">**If you must include advanced information in a warning message, reveal it by using progressive disclosure buttons** (for example, "Show details").</span></span> <span data-ttu-id="6da32-309">Cela simplifie l’avertissement pour une utilisation classique.</span><span class="sxs-lookup"><span data-stu-id="6da32-309">Doing so simplifies the warning for typical usage.</span></span> <span data-ttu-id="6da32-310">Ne masquez pas les informations nécessaires, car les utilisateurs ne le trouvent peut-être pas.</span><span class="sxs-lookup"><span data-stu-id="6da32-310">Don't hide needed information because users might not find it.</span></span>
-   <span data-ttu-id="6da32-311">**N’utilisez pas « afficher les détails » à moins qu’il y ait vraiment plus de détails.**</span><span class="sxs-lookup"><span data-stu-id="6da32-311">**Don't use "Show details" unless there really is more detail.**</span></span> <span data-ttu-id="6da32-312">Ne restatez pas uniquement les informations existantes dans un format différent.</span><span class="sxs-lookup"><span data-stu-id="6da32-312">Don't just restate the existing information in a different format.</span></span>

<span data-ttu-id="6da32-313">Pour obtenir des instructions sur l’étiquetage, consultez [Divulgation progressive](ctrl-progressive-disclosure-controls.md).</span><span class="sxs-lookup"><span data-stu-id="6da32-313">For labeling guidelines, see [Progressive Disclosure](ctrl-progressive-disclosure-controls.md).</span></span>

### <a name="default-values"></a><span data-ttu-id="6da32-314">Valeurs par défaut</span><span class="sxs-lookup"><span data-stu-id="6da32-314">Default values</span></span>

-   <span data-ttu-id="6da32-315">**Sélectionnez le niveau de réponse le plus sûr, le moins destructif ou le plus sécurisé par défaut.**</span><span class="sxs-lookup"><span data-stu-id="6da32-315">**Select the safest, least destructive, or most secure response to be the default.**</span></span>

## <a name="text"></a><span data-ttu-id="6da32-316">Text</span><span class="sxs-lookup"><span data-stu-id="6da32-316">Text</span></span>

### <a name="general"></a><span data-ttu-id="6da32-317">Généralités</span><span class="sxs-lookup"><span data-stu-id="6da32-317">General</span></span>

-   <span data-ttu-id="6da32-318">**Supprimez le texte redondant.**</span><span class="sxs-lookup"><span data-stu-id="6da32-318">**Remove redundant text.**</span></span> <span data-ttu-id="6da32-319">Recherchez-en les titres, les instructions principales, les instructions supplémentaires, les zones de contenu, les liens de commande et les boutons de validation.</span><span class="sxs-lookup"><span data-stu-id="6da32-319">Look for it in titles, main instructions, supplemental instructions, content areas, command links, and commit buttons.</span></span> <span data-ttu-id="6da32-320">En règle générale, laissez le texte intégral dans les instructions et les contrôles interactifs, et supprimez toute redondance des autres emplacements.</span><span class="sxs-lookup"><span data-stu-id="6da32-320">Generally, leave full text in instructions and interactive controls, and remove any redundancy from the other places.</span></span>
-   <span data-ttu-id="6da32-321">**N’utilisez pas les termes « avertissement » ou « attention » dans le texte.**</span><span class="sxs-lookup"><span data-stu-id="6da32-321">**Don't use the terms "warning" or "caution" in the text.**</span></span> <span data-ttu-id="6da32-322">Lorsqu’il est [utilisé correctement](vis-std-icons.md), l’icône d’avertissement indique que les utilisateurs doivent procéder avec précaution.</span><span class="sxs-lookup"><span data-stu-id="6da32-322">When [used correctly](vis-std-icons.md), the warning icon sufficiently communicates that users must proceed with caution.</span></span>

<span data-ttu-id="6da32-323">**Incorrect :**</span><span class="sxs-lookup"><span data-stu-id="6da32-323">**Incorrect:**</span></span>

![<span data-ttu-id="6da32-324">capture d’écran de l’utilisation inutile de l’avertissement dans le texte</span><span class="sxs-lookup"><span data-stu-id="6da32-324">screen shot of unnecessary use of warning in text</span></span> ](images/mess-warn-image23.png)

<span data-ttu-id="6da32-325">Dans cet exemple, le terme « avertissement » n’est pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="6da32-325">In this example, the term "warning" is unnecessary.</span></span>

### <a name="titles"></a><span data-ttu-id="6da32-326">Titres</span><span class="sxs-lookup"><span data-stu-id="6da32-326">Titles</span></span>

-   <span data-ttu-id="6da32-327">**Utilisez le titre pour identifier la commande ou la fonctionnalité à partir de laquelle l’avertissement provient.**</span><span class="sxs-lookup"><span data-stu-id="6da32-327">**Use the title to identify the command or feature where the warning came from.**</span></span> <span data-ttu-id="6da32-328">Exceptions :</span><span class="sxs-lookup"><span data-stu-id="6da32-328">Exceptions:</span></span>
    -   <span data-ttu-id="6da32-329">Si un avertissement est affiché par de nombreuses commandes différentes, envisagez d’utiliser le nom du programme à la place.</span><span class="sxs-lookup"><span data-stu-id="6da32-329">If a warning is displayed by many different commands, consider using the program name instead.</span></span>
    -   <span data-ttu-id="6da32-330">Si ce titre est redondant ou confus avec l’instruction principale, utilisez le nom du programme à la place.</span><span class="sxs-lookup"><span data-stu-id="6da32-330">If that title would be redundant or confusing with the main instruction, use the program name instead.</span></span>

<span data-ttu-id="6da32-331">**Incorrect :**</span><span class="sxs-lookup"><span data-stu-id="6da32-331">**Incorrect:**</span></span>

![<span data-ttu-id="6da32-332">capture d’écran du titre de la boîte de dialogue d’avertissement de sécurité</span><span class="sxs-lookup"><span data-stu-id="6da32-332">screen shot of security warning dialog box title</span></span> ](images/mess-warn-image24.png)

<span data-ttu-id="6da32-333">Dans cet exemple, « avertissement de sécurité » n’identifie pas la commande ou la fonctionnalité à partir de laquelle l’avertissement provient.</span><span class="sxs-lookup"><span data-stu-id="6da32-333">In this example, "Security Warning" doesn't identify the command or feature where the warning came from.</span></span>

-   <span data-ttu-id="6da32-334">**N’utilisez pas le titre pour expliquer ce que vous devez faire dans la boîte de dialogue** qui est l’objectif de l’instruction principale.</span><span class="sxs-lookup"><span data-stu-id="6da32-334">**Don't use the title to explain what to do in the dialog** that's the purpose of the main instruction.</span></span>
-   <span data-ttu-id="6da32-335">Utilisez la mise [en majuscules de style titre](glossary.md), sans ponctuation finale.</span><span class="sxs-lookup"><span data-stu-id="6da32-335">Use [title-style capitalization](glossary.md), without ending punctuation.</span></span>

### <a name="main-instructions"></a><span data-ttu-id="6da32-336">Instructions principales</span><span class="sxs-lookup"><span data-stu-id="6da32-336">Main instructions</span></span>

-   <span data-ttu-id="6da32-337">L’instruction principale d’un avertissement est basée sur son modèle de conception :</span><span class="sxs-lookup"><span data-stu-id="6da32-337">The main instruction for a warning is based on its design pattern:</span></span>



| <span data-ttu-id="6da32-338">Modèle</span><span class="sxs-lookup"><span data-stu-id="6da32-338">Pattern</span></span>                        | <span data-ttu-id="6da32-339">Instruction principale</span><span class="sxs-lookup"><span data-stu-id="6da32-339">Main instruction</span></span>                                               |
|--------------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="6da32-340">Sensibilisation</span><span class="sxs-lookup"><span data-stu-id="6da32-340">Awareness</span></span><br/>                 | <span data-ttu-id="6da32-341">Décrivez la condition ou le problème potentiel.</span><span class="sxs-lookup"><span data-stu-id="6da32-341">Describe the condition or potential problem.</span></span><br/>              |
| <span data-ttu-id="6da32-342">Problème imminent</span><span class="sxs-lookup"><span data-stu-id="6da32-342">Imminent problem</span></span><br/>          | <span data-ttu-id="6da32-343">Décrivez ce que l’utilisateur doit faire maintenant.</span><span class="sxs-lookup"><span data-stu-id="6da32-343">Describe what the user needs to do now.</span></span><br/>                   |
| <span data-ttu-id="6da32-344">Confirmation de l’action risquée</span><span class="sxs-lookup"><span data-stu-id="6da32-344">Risky action confirmation</span></span><br/> | <span data-ttu-id="6da32-345">Posez une question pour déterminer si l’utilisateur souhaite continuer.</span><span class="sxs-lookup"><span data-stu-id="6da32-345">Ask a question to determine if the user wants to proceed.</span></span><br/> |



 

-   ![<span data-ttu-id="6da32-346">capture d’écran d’une notification de batterie faible</span><span class="sxs-lookup"><span data-stu-id="6da32-346">screen shot of a low-battery notification</span></span> ](images/mess-warn-image25.png)
-   <span data-ttu-id="6da32-347">Dans cet exemple, la notification de batterie faible est un avertissement de sensibilisation, donc l’instruction principale décrit la condition.</span><span class="sxs-lookup"><span data-stu-id="6da32-347">In this example, the low battery notification is an awareness warning, so the main instruction describes the condition.</span></span>
-   ![<span data-ttu-id="6da32-348">capture d’écran de l’avertissement modifier immédiatement la batterie</span><span class="sxs-lookup"><span data-stu-id="6da32-348">screen shot of change battery immediately warning</span></span> ](images/mess-warn-image1.png)
-   <span data-ttu-id="6da32-349">Dans cet exemple, la boîte de dialogue batterie faible est un problème imminent, donc l’instruction principale décrit ce que l’utilisateur doit faire maintenant.</span><span class="sxs-lookup"><span data-stu-id="6da32-349">In this example, the low battery dialog box is an imminent problem, so the main instruction describes what the user needs to do now.</span></span>
-   <span data-ttu-id="6da32-350">**N’utilisez qu’une seule phrase complète.**</span><span class="sxs-lookup"><span data-stu-id="6da32-350">**Be concise use only a single, complete sentence.**</span></span> <span data-ttu-id="6da32-351">Supprimez l’instruction principale jusqu’aux informations essentielles.</span><span class="sxs-lookup"><span data-stu-id="6da32-351">Strip the main instruction down to the essential information.</span></span> <span data-ttu-id="6da32-352">Si vous devez apporter des explications supplémentaires, utilisez une instruction supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="6da32-352">If you must explain anything more, use a supplemental instruction.</span></span>
-   <span data-ttu-id="6da32-353">**Utilisez des mots tels que « Now » et « immédiatement » si l’utilisateur doit agir immédiatement.**</span><span class="sxs-lookup"><span data-stu-id="6da32-353">**Use words like "now" and "immediately" if the user must act immediately.**</span></span> <span data-ttu-id="6da32-354">N’utilisez pas ces mots s’il n’y a pas d’urgence.</span><span class="sxs-lookup"><span data-stu-id="6da32-354">Don't use these words if there is no urgency.</span></span>
-   <span data-ttu-id="6da32-355">**Être spécifique s’il existe des objets impliqués, donnez-leur un nom complet.**</span><span class="sxs-lookup"><span data-stu-id="6da32-355">**Be specific if there are objects involved, give their full names.**</span></span>
-   <span data-ttu-id="6da32-356">Utilisez la mise [en majuscules de style phrase](glossary.md).</span><span class="sxs-lookup"><span data-stu-id="6da32-356">Use [sentence-style capitalization](glossary.md).</span></span>

### <a name="supplemental-instructions"></a><span data-ttu-id="6da32-357">Instructions supplémentaires</span><span class="sxs-lookup"><span data-stu-id="6da32-357">Supplemental instructions</span></span>

-   <span data-ttu-id="6da32-358">L’instruction supplémentaire pour un avertissement est basée sur son modèle de conception :</span><span class="sxs-lookup"><span data-stu-id="6da32-358">The supplemental instruction for a warning is based on its design pattern:</span></span>



| <span data-ttu-id="6da32-359">Modèle</span><span class="sxs-lookup"><span data-stu-id="6da32-359">Pattern</span></span>            | <span data-ttu-id="6da32-360">Instruction supplémentaire</span><span class="sxs-lookup"><span data-stu-id="6da32-360">Supplemental instruction</span></span>                                            |
|--------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6da32-361">Sensibilisation</span><span class="sxs-lookup"><span data-stu-id="6da32-361">Awareness</span></span><br/>                 | <span data-ttu-id="6da32-362">Expliquez l’implication et pourquoi elle est importante.</span><span class="sxs-lookup"><span data-stu-id="6da32-362">Explain the implication and why it is important.</span></span><br/>                        |
| <span data-ttu-id="6da32-363">Problème imminent</span><span class="sxs-lookup"><span data-stu-id="6da32-363">Imminent problem</span></span><br/>          | <span data-ttu-id="6da32-364">Expliquez la condition et pourquoi elle est importante.</span><span class="sxs-lookup"><span data-stu-id="6da32-364">Explain the condition and why it is important.</span></span><br/>                          |
| <span data-ttu-id="6da32-365">Confirmation de l’action risquée</span><span class="sxs-lookup"><span data-stu-id="6da32-365">Risky action confirmation</span></span><br/> | <span data-ttu-id="6da32-366">Expliquez les raisons les plus évidentes pour lesquelles l’utilisateur peut ne pas vouloir continuer.</span><span class="sxs-lookup"><span data-stu-id="6da32-366">Explain any non-obvious reasons why the user might not want to proceed.</span></span><br/> |



 

-   <span data-ttu-id="6da32-367">**Ne répétez pas l’instruction principale avec un libellé légèrement différent.**</span><span class="sxs-lookup"><span data-stu-id="6da32-367">**Don't repeat the main instruction with slightly different wording.**</span></span> <span data-ttu-id="6da32-368">Au lieu de cela, omettez l’instruction supplémentaire s’il n’y a pas d’autres à ajouter.</span><span class="sxs-lookup"><span data-stu-id="6da32-368">Instead, omit the supplemental instruction if there is not more to add.</span></span>
-   <span data-ttu-id="6da32-369">Utilisez des phrases complètes, des majuscules de style phrase et des signes de ponctuation de fin.</span><span class="sxs-lookup"><span data-stu-id="6da32-369">Use complete sentences, sentence-style capitalization, and ending punctuation.</span></span>

### <a name="commit-buttons"></a><span data-ttu-id="6da32-370">Boutons de validation</span><span class="sxs-lookup"><span data-stu-id="6da32-370">Commit buttons</span></span>

-   <span data-ttu-id="6da32-371">Pour les boîtes de dialogue d’avertissement, les boutons de validation sont basés sur le modèle de conception :</span><span class="sxs-lookup"><span data-stu-id="6da32-371">For warning dialog boxes, the commit buttons are based on its design pattern:</span></span>



| <span data-ttu-id="6da32-372">Modèle</span><span class="sxs-lookup"><span data-stu-id="6da32-372">Pattern</span></span>               | <span data-ttu-id="6da32-373">Boutons de validation</span><span class="sxs-lookup"><span data-stu-id="6da32-373">Commit buttons</span></span>        |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6da32-374">Sensibilisation</span><span class="sxs-lookup"><span data-stu-id="6da32-374">Awareness</span></span><br/>                 | <span data-ttu-id="6da32-375">C’est presque ça.</span><span class="sxs-lookup"><span data-stu-id="6da32-375">Close.</span></span> <span data-ttu-id="6da32-376">N’utilisez pas OK, car cela suggère que des problèmes potentiels sont possibles.</span><span class="sxs-lookup"><span data-stu-id="6da32-376">Don't use OK because it suggests that potential problems are OK.</span></span><br/>                              |
| <span data-ttu-id="6da32-377">Problème imminent</span><span class="sxs-lookup"><span data-stu-id="6da32-377">Imminent problem</span></span><br/>          | <span data-ttu-id="6da32-378">Un bouton de commande ou un lien de commande pour chaque option, ou OK si l’action se produit en dehors de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="6da32-378">A command button or command link for each option, or OK if the action occurs outside the dialog box.</span></span><br/> |
| <span data-ttu-id="6da32-379">Confirmation de l’action risquée</span><span class="sxs-lookup"><span data-stu-id="6da32-379">Risky action confirmation</span></span><br/> | <span data-ttu-id="6da32-380">Oui, non.</span><span class="sxs-lookup"><span data-stu-id="6da32-380">Yes, No.</span></span><br/>                                                                                             |



 

-   <span data-ttu-id="6da32-381">**Incorrect :**</span><span class="sxs-lookup"><span data-stu-id="6da32-381">**Incorrect:**</span></span>
-   ![<span data-ttu-id="6da32-382">capture d’écran de la boîte de dialogue d’avertissement avec le bouton OK</span><span class="sxs-lookup"><span data-stu-id="6da32-382">screen shot of warning dialog box with ok button</span></span> ](images/mess-warn-image26.png)
-   <span data-ttu-id="6da32-383">Les problèmes ne sont pas OK. Utilisez plutôt Close.</span><span class="sxs-lookup"><span data-stu-id="6da32-383">Problems aren't OK, so use Close instead.</span></span>

## <a name="documentation"></a><span data-ttu-id="6da32-384">Documentation</span><span class="sxs-lookup"><span data-stu-id="6da32-384">Documentation</span></span>

<span data-ttu-id="6da32-385">Lorsque vous faites référence aux avertissements :</span><span class="sxs-lookup"><span data-stu-id="6da32-385">When referring to warnings:</span></span>

-   <span data-ttu-id="6da32-386">Si l’avertissement pose une question, reportez-vous à un avertissement par sa question ; dans le cas contraire, utilisez l’instruction principale.</span><span class="sxs-lookup"><span data-stu-id="6da32-386">If the warning asks a question, refer to a warning by its question; otherwise, use the main instruction.</span></span> <span data-ttu-id="6da32-387">Si la question ou l’instruction principale est longue ou détaillée, résumez-la.</span><span class="sxs-lookup"><span data-stu-id="6da32-387">If the question or main instruction is long or detailed, summarize it.</span></span>
-   <span data-ttu-id="6da32-388">Si nécessaire, vous pouvez faire référence à une boîte de dialogue d’avertissement en tant que message.</span><span class="sxs-lookup"><span data-stu-id="6da32-388">If necessary, you may refer to a warning dialog box as a message.</span></span>
-   <span data-ttu-id="6da32-389">Dans la mesure du possible, mettez en forme le texte en gras.</span><span class="sxs-lookup"><span data-stu-id="6da32-389">When possible, format the text using bold.</span></span> <span data-ttu-id="6da32-390">Sinon, placez le texte entre guillemets uniquement si nécessaire pour éviter toute confusion.</span><span class="sxs-lookup"><span data-stu-id="6da32-390">Otherwise, put the text in quotation marks only if required to prevent confusion.</span></span>

<span data-ttu-id="6da32-391">Exemple : dans le message voulez **-vous afficher les éléments non sécurisés ?** , cliquez sur Oui.</span><span class="sxs-lookup"><span data-stu-id="6da32-391">Example: In the **Do you want to display the nonsecure items?** message, click Yes.</span></span>

 

