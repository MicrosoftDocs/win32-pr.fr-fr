---
description: Les fonctions de service en ligne supplémentaires sont répertoriées par catégorie dans les rubriques suivantes.
ms.assetid: d4338b3c-cd84-4abb-b74e-9df895c8355b
title: Fonctions de service en ligne supplémentaires
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21a29831369fd6b886d57cfae075b5b8bf7a83b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533882"
---
# <a name="supplementary-line-service-functions"></a><span data-ttu-id="acc85-103">Fonctions de service en ligne supplémentaires</span><span class="sxs-lookup"><span data-stu-id="acc85-103">Supplementary Line Service Functions</span></span>

<span data-ttu-id="acc85-104">Les fonctions de service en ligne supplémentaires sont répertoriées par catégorie dans les rubriques suivantes.</span><span class="sxs-lookup"><span data-stu-id="acc85-104">The supplementary line service functions are listed by category in the following topics.</span></span> <span data-ttu-id="acc85-105">Une fonction est identifiée comme [*asynchrone*](a-tapgloss.md) si elle indique la fin d’un message de réponse à l’application.</span><span class="sxs-lookup"><span data-stu-id="acc85-105">A function is identified as [*asynchronous*](a-tapgloss.md) if it will indicate completion in a REPLY message to the application.</span></span> <span data-ttu-id="acc85-106">Si la fonction retourne toujours son résultat à l’application immédiatement, la fonction est considérée comme [*synchrone*](s-tapgloss.md).</span><span class="sxs-lookup"><span data-stu-id="acc85-106">If the function always returns its result to the application immediately, the function is considered [*synchronous*](s-tapgloss.md).</span></span>

<span data-ttu-id="acc85-107">Voici un regroupement fonctionnel des fonctions de service en ligne supplémentaires :</span><span class="sxs-lookup"><span data-stu-id="acc85-107">Following is a functional grouping of the supplementary line service functions:</span></span>

-   [<span data-ttu-id="acc85-108">Agents</span><span class="sxs-lookup"><span data-stu-id="acc85-108">Agents</span></span>](#agents)
-   [<span data-ttu-id="acc85-109">Priorité de l’application</span><span class="sxs-lookup"><span data-stu-id="acc85-109">Application priority</span></span>](#application-priority)
-   [<span data-ttu-id="acc85-110">Taux et mode de support</span><span class="sxs-lookup"><span data-stu-id="acc85-110">Bearer mode and rate</span></span>](#bearer-mode-and-rate)
-   [<span data-ttu-id="acc85-111">Appeler accepter et rediriger</span><span class="sxs-lookup"><span data-stu-id="acc85-111">Call accept and redirect</span></span>](#call-accept-and-redirect)
-   [<span data-ttu-id="acc85-112">Fin de l’appel</span><span class="sxs-lookup"><span data-stu-id="acc85-112">Call completion</span></span>](#call-completion)
-   [<span data-ttu-id="acc85-113">Appeler une conférence</span><span class="sxs-lookup"><span data-stu-id="acc85-113">Call conference</span></span>](#call-conference)
-   [<span data-ttu-id="acc85-114">Transfert d’appels</span><span class="sxs-lookup"><span data-stu-id="acc85-114">Call forwarding</span></span>](#call-forwarding)
-   [<span data-ttu-id="acc85-115">Recevoir un appel</span><span class="sxs-lookup"><span data-stu-id="acc85-115">Call hold</span></span>](#call-hold)
-   [<span data-ttu-id="acc85-116">Parc d’appels</span><span class="sxs-lookup"><span data-stu-id="acc85-116">Call park</span></span>](#call-park)
-   [<span data-ttu-id="acc85-117">Prélèvement d’appels</span><span class="sxs-lookup"><span data-stu-id="acc85-117">Call pickup</span></span>](#call-pickup)
-   [<span data-ttu-id="acc85-118">Appel refusé</span><span class="sxs-lookup"><span data-stu-id="acc85-118">Call reject</span></span>](#call-reject)
-   [<span data-ttu-id="acc85-119">Transfert d’appels</span><span class="sxs-lookup"><span data-stu-id="acc85-119">Call transfer</span></span>](#call-transfer)
-   [<span data-ttu-id="acc85-120">Chiffrer la surveillance et la collecte</span><span class="sxs-lookup"><span data-stu-id="acc85-120">Digit monitoring and gathering</span></span>](#digit-monitoring-and-gathering)
-   [<span data-ttu-id="acc85-121">Génération de chiffres et de tonalités inbande</span><span class="sxs-lookup"><span data-stu-id="acc85-121">Generating inband digits and tones</span></span>](#generating-inband-digits-and-tones)
-   [<span data-ttu-id="acc85-122">Appels effectués</span><span class="sxs-lookup"><span data-stu-id="acc85-122">Making calls</span></span>](basic-telephony-services-reference.md)
-   [<span data-ttu-id="acc85-123">Contrôle multimédia</span><span class="sxs-lookup"><span data-stu-id="acc85-123">Media control</span></span>](#media-control)
-   [<span data-ttu-id="acc85-124">Surveillance des médias</span><span class="sxs-lookup"><span data-stu-id="acc85-124">Media monitoring</span></span>](#media-monitoring)
-   [<span data-ttu-id="acc85-125">Proxies</span><span class="sxs-lookup"><span data-stu-id="acc85-125">Proxies</span></span>](#proxies)
-   [<span data-ttu-id="acc85-126">Qualité de service</span><span class="sxs-lookup"><span data-stu-id="acc85-126">Quality of Service</span></span>](#quality-of-service)
-   [<span data-ttu-id="acc85-127">Envoi d’informations au tiers distant</span><span class="sxs-lookup"><span data-stu-id="acc85-127">Sending information to remote party</span></span>](#sending-information-to-remote-party)
-   [<span data-ttu-id="acc85-128">Gestion des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="acc85-128">Service provider management</span></span>](#service-provider-management)
-   [<span data-ttu-id="acc85-129">Définition d’un terminal pour les conversations sur téléphone</span><span class="sxs-lookup"><span data-stu-id="acc85-129">Setting a terminal for phone conversations</span></span>](#setting-a-terminal-for-phone-conversations)
-   [<span data-ttu-id="acc85-130">Analyse des tons</span><span class="sxs-lookup"><span data-stu-id="acc85-130">Tone monitoring</span></span>](#tone-monitoring)

<span data-ttu-id="acc85-131">Il existe également [diverses](#miscellaneous) fonctions de service de ligne supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="acc85-131">There are also [miscellaneous](#miscellaneous) supplementary line service functions.</span></span>

## <a name="bearer-mode-and-rate"></a><span data-ttu-id="acc85-132">Taux et mode de support</span><span class="sxs-lookup"><span data-stu-id="acc85-132">Bearer Mode and Rate</span></span>



| <span data-ttu-id="acc85-133">Fonction</span><span class="sxs-lookup"><span data-stu-id="acc85-133">Function</span></span>                                       | <span data-ttu-id="acc85-134">Description</span><span class="sxs-lookup"><span data-stu-id="acc85-134">Description</span></span>                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="acc85-135">**lineSetCallParams**</span><span class="sxs-lookup"><span data-stu-id="acc85-135">**lineSetCallParams**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetcallparams) | <span data-ttu-id="acc85-136">Demande une modification des paramètres d’appel d’un appel existant.</span><span class="sxs-lookup"><span data-stu-id="acc85-136">Requests a change in the call parameters of an existing call.</span></span> <span data-ttu-id="acc85-137">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="acc85-137">Synchronous.</span></span> |



 

## <a name="media-monitoring"></a><span data-ttu-id="acc85-138">Surveillance des médias</span><span class="sxs-lookup"><span data-stu-id="acc85-138">Media Monitoring</span></span>



| <span data-ttu-id="acc85-139">Fonction</span><span class="sxs-lookup"><span data-stu-id="acc85-139">Function</span></span>                                     | <span data-ttu-id="acc85-140">Description</span><span class="sxs-lookup"><span data-stu-id="acc85-140">Description</span></span>                                                                   |
|----------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="acc85-141">**lineMonitorMedia**</span><span class="sxs-lookup"><span data-stu-id="acc85-141">**lineMonitorMedia**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemonitormedia) | <span data-ttu-id="acc85-142">Active ou désactive la notification en mode Media sur un appel spécifié.</span><span class="sxs-lookup"><span data-stu-id="acc85-142">Enables or disables media mode notification on a specified call.</span></span> <span data-ttu-id="acc85-143">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="acc85-143">Synchronous.</span></span> |



 

## <a name="digit-monitoring-and-gathering"></a><span data-ttu-id="acc85-144">Chiffrer la surveillance et la collecte</span><span class="sxs-lookup"><span data-stu-id="acc85-144">Digit Monitoring and Gathering</span></span>



| <span data-ttu-id="acc85-145">Fonction</span><span class="sxs-lookup"><span data-stu-id="acc85-145">Function</span></span>                                       | <span data-ttu-id="acc85-146">Description</span><span class="sxs-lookup"><span data-stu-id="acc85-146">Description</span></span>                                                                        |
|------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="acc85-147">**lineMonitorDigits**</span><span class="sxs-lookup"><span data-stu-id="acc85-147">**lineMonitorDigits**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits) | <span data-ttu-id="acc85-148">Active ou désactive la notification de détection de chiffres sur un appel spécifié.</span><span class="sxs-lookup"><span data-stu-id="acc85-148">Enables or disables digit detection notification on a specified call.</span></span> <span data-ttu-id="acc85-149">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="acc85-149">Synchronous.</span></span> |
| [<span data-ttu-id="acc85-150">**lineGatherDigits**</span><span class="sxs-lookup"><span data-stu-id="acc85-150">**lineGatherDigits**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits)   | <span data-ttu-id="acc85-151">Exécute la collecte mise en mémoire tampon des chiffres sur un appel.</span><span class="sxs-lookup"><span data-stu-id="acc85-151">Performs the buffered gathering of digits on a call.</span></span> <span data-ttu-id="acc85-152">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="acc85-152">Synchronous.</span></span>                  |



 

## <a name="tone-monitoring"></a><span data-ttu-id="acc85-153">Analyse des tons</span><span class="sxs-lookup"><span data-stu-id="acc85-153">Tone Monitoring</span></span>



| <span data-ttu-id="acc85-154">Fonction</span><span class="sxs-lookup"><span data-stu-id="acc85-154">Function</span></span>                                     | <span data-ttu-id="acc85-155">Description</span><span class="sxs-lookup"><span data-stu-id="acc85-155">Description</span></span>                                                       |
|----------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="acc85-156">**lineMonitorTones**</span><span class="sxs-lookup"><span data-stu-id="acc85-156">**lineMonitorTones**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemonitortones) | <span data-ttu-id="acc85-157">Spécifie les tonalités à détecter sur un appel spécifié.</span><span class="sxs-lookup"><span data-stu-id="acc85-157">Specifies which tones to detect on a specified call.</span></span> <span data-ttu-id="acc85-158">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="acc85-158">Synchronous.</span></span> |



 

## <a name="media-control"></a><span data-ttu-id="acc85-159">Contrôle multimédia</span><span class="sxs-lookup"><span data-stu-id="acc85-159">Media Control</span></span>



| <span data-ttu-id="acc85-160">Fonction</span><span class="sxs-lookup"><span data-stu-id="acc85-160">Function</span></span>                                           | <span data-ttu-id="acc85-161">Description</span><span class="sxs-lookup"><span data-stu-id="acc85-161">Description</span></span>                                                                                                          |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="acc85-162">**lineSetMediaControl**</span><span class="sxs-lookup"><span data-stu-id="acc85-162">**lineSetMediaControl**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetmediacontrol) | <span data-ttu-id="acc85-163">Définit le flux multimédia d’un appel pour le contrôle multimédia.</span><span class="sxs-lookup"><span data-stu-id="acc85-163">Sets up a call's media stream for media control.</span></span> <span data-ttu-id="acc85-164">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="acc85-164">Synchronous.</span></span>                                                        |
| [<span data-ttu-id="acc85-165">**lineSetMediaMode**</span><span class="sxs-lookup"><span data-stu-id="acc85-165">**lineSetMediaMode**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetmediamode)       | <span data-ttu-id="acc85-166">Définit le (s) mode (s) de support de l’appel spécifié dans sa structure [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) .</span><span class="sxs-lookup"><span data-stu-id="acc85-166">Sets the media mode(s) of the specified call in its [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) structure.</span></span> <span data-ttu-id="acc85-167">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="acc85-167">Synchronous.</span></span> |



 

## <a name="generating-inband-digits-and-tones"></a><span data-ttu-id="acc85-168">Génération de chiffres et de tonalités inbande</span><span class="sxs-lookup"><span data-stu-id="acc85-168">Generating Inband Digits and Tones</span></span>



| <span data-ttu-id="acc85-169">Fonction</span><span class="sxs-lookup"><span data-stu-id="acc85-169">Function</span></span>                                         | <span data-ttu-id="acc85-170">Description</span><span class="sxs-lookup"><span data-stu-id="acc85-170">Description</span></span>                                                   |
|--------------------------------------------------|---------------------------------------------------------------|
| [<span data-ttu-id="acc85-171">**lineGenerateDigits**</span><span class="sxs-lookup"><span data-stu-id="acc85-171">**lineGenerateDigits**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits) | <span data-ttu-id="acc85-172">Génère des chiffres inbandes sur un appel.</span><span class="sxs-lookup"><span data-stu-id="acc85-172">Generates inband digits on a call.</span></span> <span data-ttu-id="acc85-173">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="acc85-173">Synchronous.</span></span>               |
| [<span data-ttu-id="acc85-174">**lineGenerateTone**</span><span class="sxs-lookup"><span data-stu-id="acc85-174">**lineGenerateTone**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegeneratetone)     | <span data-ttu-id="acc85-175">Génère un ensemble donné de tonalités inbande sur un appel.</span><span class="sxs-lookup"><span data-stu-id="acc85-175">Generates a given set of tones inband on a call.</span></span> <span data-ttu-id="acc85-176">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="acc85-176">Synchronous.</span></span> |



 

## <a name="call-accept-and-redirect"></a><span data-ttu-id="acc85-177">Appeler accepter et rediriger</span><span class="sxs-lookup"><span data-stu-id="acc85-177">Call Accept and Redirect</span></span>



| <span data-ttu-id="acc85-178">Fonction</span><span class="sxs-lookup"><span data-stu-id="acc85-178">Function</span></span>                             | <span data-ttu-id="acc85-179">Description</span><span class="sxs-lookup"><span data-stu-id="acc85-179">Description</span></span>                                                                                               |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="acc85-180">**lineAccept**</span><span class="sxs-lookup"><span data-stu-id="acc85-180">**lineAccept**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineaccept)     | <span data-ttu-id="acc85-181">Accepte un appel proposé et démarre l’alerte à la fois de l’appelant (rappel) et du tiers appelé tiers (sonnerie).</span><span class="sxs-lookup"><span data-stu-id="acc85-181">Accepts an offered call and starts alerting both caller (ringback) and called party (ring).</span></span> <span data-ttu-id="acc85-182">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="acc85-182">Asynchronous.</span></span> |
| [<span data-ttu-id="acc85-183">**lineRedirect**</span><span class="sxs-lookup"><span data-stu-id="acc85-183">**lineRedirect**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineredirect) | <span data-ttu-id="acc85-184">Redirige un appel d’offre vers une autre adresse.</span><span class="sxs-lookup"><span data-stu-id="acc85-184">Redirects an offering call to another address.</span></span> <span data-ttu-id="acc85-185">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="acc85-185">Asynchronous.</span></span>                                              |



 

## <a name="call-reject"></a><span data-ttu-id="acc85-186">Appel refusé</span><span class="sxs-lookup"><span data-stu-id="acc85-186">Call Reject</span></span>



| <span data-ttu-id="acc85-187">Fonction</span><span class="sxs-lookup"><span data-stu-id="acc85-187">Function</span></span>                     | <span data-ttu-id="acc85-188">Description</span><span class="sxs-lookup"><span data-stu-id="acc85-188">Description</span></span>                                                               |
|------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="acc85-189">**lineDrop**</span><span class="sxs-lookup"><span data-stu-id="acc85-189">**lineDrop**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedrop) | <span data-ttu-id="acc85-190">Déconnecte un appel ou abandonne une tentative d’appel en cours.</span><span class="sxs-lookup"><span data-stu-id="acc85-190">Disconnects a call, or abandons a call attempt in progress.</span></span> <span data-ttu-id="acc85-191">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="acc85-191">Asynchronous.</span></span> |



 

## <a name="call-hold"></a><span data-ttu-id="acc85-192">Recevoir un appel</span><span class="sxs-lookup"><span data-stu-id="acc85-192">Call Hold</span></span>



| <span data-ttu-id="acc85-193">Fonction</span><span class="sxs-lookup"><span data-stu-id="acc85-193">Function</span></span>                         | <span data-ttu-id="acc85-194">Description</span><span class="sxs-lookup"><span data-stu-id="acc85-194">Description</span></span>                                           |
|----------------------------------|-------------------------------------------------------|
| [<span data-ttu-id="acc85-195">**lineHold**</span><span class="sxs-lookup"><span data-stu-id="acc85-195">**lineHold**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linehold)     | <span data-ttu-id="acc85-196">Place l’appel spécifié sur un blocage matériel.</span><span class="sxs-lookup"><span data-stu-id="acc85-196">Places the specified call on hard hold.</span></span> <span data-ttu-id="acc85-197">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="acc85-197">Asynchronous.</span></span> |
| [<span data-ttu-id="acc85-198">**lineUnhold**</span><span class="sxs-lookup"><span data-stu-id="acc85-198">**lineUnhold**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineunhold) | <span data-ttu-id="acc85-199">Récupère un appel détenu.</span><span class="sxs-lookup"><span data-stu-id="acc85-199">Retrieves a held call.</span></span> <span data-ttu-id="acc85-200">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="acc85-200">Asynchronous.</span></span>                  |



 

## <a name="securing-calls"></a><span data-ttu-id="acc85-201">Sécurisation des appels</span><span class="sxs-lookup"><span data-stu-id="acc85-201">Securing Calls</span></span>



| <span data-ttu-id="acc85-202">Fonction</span><span class="sxs-lookup"><span data-stu-id="acc85-202">Function</span></span>                                 | <span data-ttu-id="acc85-203">Description</span><span class="sxs-lookup"><span data-stu-id="acc85-203">Description</span></span>                                                                                                              |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="acc85-204">**lineSecureCall**</span><span class="sxs-lookup"><span data-stu-id="acc85-204">**lineSecureCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesecurecall) | <span data-ttu-id="acc85-205">Sécurise un appel existant contre les interférences par d’autres événements tels que les bips d’attente d’appels sur les connexions de données.</span><span class="sxs-lookup"><span data-stu-id="acc85-205">Secures an existing call from interference by other events such as call-waiting beeps on data connections.</span></span> <span data-ttu-id="acc85-206">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="acc85-206">Asynchronous.</span></span> |



 

## <a name="call-transfer"></a><span data-ttu-id="acc85-207">Transfert d’appels</span><span class="sxs-lookup"><span data-stu-id="acc85-207">Call Transfer</span></span>



| <span data-ttu-id="acc85-208">Fonction</span><span class="sxs-lookup"><span data-stu-id="acc85-208">Function</span></span>                                             | <span data-ttu-id="acc85-209">Description</span><span class="sxs-lookup"><span data-stu-id="acc85-209">Description</span></span>                                                                                                    |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="acc85-210">**lineSetupTransfer**</span><span class="sxs-lookup"><span data-stu-id="acc85-210">**lineSetupTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)       | <span data-ttu-id="acc85-211">Prépare un appel spécifié pour le transfert vers une autre adresse.</span><span class="sxs-lookup"><span data-stu-id="acc85-211">Prepares a specified call for transfer to another address.</span></span> <span data-ttu-id="acc85-212">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="acc85-212">Asynchronous.</span></span>                                       |
| [<span data-ttu-id="acc85-213">**lineCompleteTransfer**</span><span class="sxs-lookup"><span data-stu-id="acc85-213">**lineCompleteTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) | <span data-ttu-id="acc85-214">Transfère un appel qui a été configuré pour le transfert vers un autre appel ou entre une conférence triple.</span><span class="sxs-lookup"><span data-stu-id="acc85-214">Transfers a call that was set up for transfer to another call, or enters a three-way conference.</span></span> <span data-ttu-id="acc85-215">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="acc85-215">Asynchronous.</span></span> |
| [<span data-ttu-id="acc85-216">**lineBlindTransfer**</span><span class="sxs-lookup"><span data-stu-id="acc85-216">**lineBlindTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineblindtransfer)       | <span data-ttu-id="acc85-217">Transfère un appel à un tiers.</span><span class="sxs-lookup"><span data-stu-id="acc85-217">Transfers a call to another party.</span></span> <span data-ttu-id="acc85-218">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="acc85-218">Asynchronous.</span></span>                                                               |
| [<span data-ttu-id="acc85-219">**lineSwapHold**</span><span class="sxs-lookup"><span data-stu-id="acc85-219">**lineSwapHold**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineswaphold)                 | <span data-ttu-id="acc85-220">Permute l’appel actif avec l’appel actuellement sur la suspension de la consultation.</span><span class="sxs-lookup"><span data-stu-id="acc85-220">Swaps the active call with the call currently on consultation hold.</span></span> <span data-ttu-id="acc85-221">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="acc85-221">Asynchronous.</span></span>                              |



 

## <a name="call-conference"></a><span data-ttu-id="acc85-222">Appeler une conférence</span><span class="sxs-lookup"><span data-stu-id="acc85-222">Call Conference</span></span>



| <span data-ttu-id="acc85-223">Fonction</span><span class="sxs-lookup"><span data-stu-id="acc85-223">Function</span></span>                                                         | <span data-ttu-id="acc85-224">Description</span><span class="sxs-lookup"><span data-stu-id="acc85-224">Description</span></span>                                                                                                                                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="acc85-225">**lineSetupConference**</span><span class="sxs-lookup"><span data-stu-id="acc85-225">**lineSetupConference**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)               | <span data-ttu-id="acc85-226">Prépare un appel donné pour l’ajout d’un tiers.</span><span class="sxs-lookup"><span data-stu-id="acc85-226">Prepares a given call for the addition of another party.</span></span> <span data-ttu-id="acc85-227">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="acc85-227">Asynchronous.</span></span>                                                                                                                               |
| [<span data-ttu-id="acc85-228">**linePrepareAddToConference**</span><span class="sxs-lookup"><span data-stu-id="acc85-228">**linePrepareAddToConference**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference) | <span data-ttu-id="acc85-229">Prépare l’ajout d’un tiers à un appel de conférence existant en plaçant l’appel de conférence dans un état de suspension et en créant un appel de consultation qui peut être ajouté ultérieurement à l’appel de conférence.</span><span class="sxs-lookup"><span data-stu-id="acc85-229">Prepares to add a party to an existing conference call by placing the conference call in a hold state and creating a consultation call that can be added later to the conference call.</span></span> <span data-ttu-id="acc85-230">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="acc85-230">Asynchronous.</span></span> |
| [<span data-ttu-id="acc85-231">**lineAddToConference**</span><span class="sxs-lookup"><span data-stu-id="acc85-231">**lineAddToConference**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineaddtoconference)               | <span data-ttu-id="acc85-232">Ajoute un appel de consultation à un appel de conférence existant.</span><span class="sxs-lookup"><span data-stu-id="acc85-232">Adds a consultation call to an existing conference call.</span></span> <span data-ttu-id="acc85-233">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="acc85-233">Asynchronous.</span></span>                                                                                                                               |
| [<span data-ttu-id="acc85-234">**lineRemoveFromConference**</span><span class="sxs-lookup"><span data-stu-id="acc85-234">**lineRemoveFromConference**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineremovefromconference)     | <span data-ttu-id="acc85-235">Supprime un tiers d’un appel de conférence.</span><span class="sxs-lookup"><span data-stu-id="acc85-235">Removes a party from a conference call.</span></span> <span data-ttu-id="acc85-236">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="acc85-236">Asynchronous.</span></span>                                                                                                                                                |



 

## <a name="call-park"></a><span data-ttu-id="acc85-237">Parc d’appels</span><span class="sxs-lookup"><span data-stu-id="acc85-237">Call Park</span></span>



| <span data-ttu-id="acc85-238">Fonction</span><span class="sxs-lookup"><span data-stu-id="acc85-238">Function</span></span>                         | <span data-ttu-id="acc85-239">Description</span><span class="sxs-lookup"><span data-stu-id="acc85-239">Description</span></span>                                          |
|----------------------------------|------------------------------------------------------|
| [<span data-ttu-id="acc85-240">**linePark**</span><span class="sxs-lookup"><span data-stu-id="acc85-240">**linePark**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linepark)     | <span data-ttu-id="acc85-241">Traite un appel donné à une autre adresse.</span><span class="sxs-lookup"><span data-stu-id="acc85-241">Parks a given call at another address.</span></span> <span data-ttu-id="acc85-242">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="acc85-242">Asynchronous.</span></span> |
| [<span data-ttu-id="acc85-243">**lineUnpark**</span><span class="sxs-lookup"><span data-stu-id="acc85-243">**lineUnpark**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineunpark) | <span data-ttu-id="acc85-244">Récupère un appel parqué.</span><span class="sxs-lookup"><span data-stu-id="acc85-244">Retrieves a parked call.</span></span> <span data-ttu-id="acc85-245">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="acc85-245">Asynchronous.</span></span>               |



 

## <a name="call-forwarding"></a><span data-ttu-id="acc85-246">Transfert d’appels</span><span class="sxs-lookup"><span data-stu-id="acc85-246">Call Forwarding</span></span>



| <span data-ttu-id="acc85-247">Fonction</span><span class="sxs-lookup"><span data-stu-id="acc85-247">Function</span></span>                           | <span data-ttu-id="acc85-248">Description</span><span class="sxs-lookup"><span data-stu-id="acc85-248">Description</span></span>                                             |
|------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="acc85-249">**lineForward**</span><span class="sxs-lookup"><span data-stu-id="acc85-249">**lineForward**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineforward) | <span data-ttu-id="acc85-250">Définit ou annule les demandes de transfert d’appel.</span><span class="sxs-lookup"><span data-stu-id="acc85-250">Sets or cancels call forwarding requests.</span></span> <span data-ttu-id="acc85-251">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="acc85-251">Asynchronous.</span></span> |



 

## <a name="call-pickup"></a><span data-ttu-id="acc85-252">Prélèvement d’appels</span><span class="sxs-lookup"><span data-stu-id="acc85-252">Call Pickup</span></span>



| <span data-ttu-id="acc85-253">Fonction</span><span class="sxs-lookup"><span data-stu-id="acc85-253">Function</span></span>                         | <span data-ttu-id="acc85-254">Description</span><span class="sxs-lookup"><span data-stu-id="acc85-254">Description</span></span>                                                                                                                                                                                      |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="acc85-255">**linePickup**</span><span class="sxs-lookup"><span data-stu-id="acc85-255">**linePickup**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linepickup) | <span data-ttu-id="acc85-256">Récupère une alerte d’appel à une adresse de destination spécifiée et retourne un descripteur d’appel pour l’appel prélevé ([**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) peut également être utilisé pour l’appel en attente).</span><span class="sxs-lookup"><span data-stu-id="acc85-256">Picks up a call alerting at a specified destination address and returns a call handle for the picked-up call ([**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) can also be used for call waiting).</span></span> <span data-ttu-id="acc85-257">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="acc85-257">Asynchronous.</span></span> |



 

## <a name="sending-information-to-remote-party"></a><span data-ttu-id="acc85-258">Envoi d’informations au tiers distant</span><span class="sxs-lookup"><span data-stu-id="acc85-258">Sending Information to Remote Party</span></span>



| <span data-ttu-id="acc85-259">Fonction</span><span class="sxs-lookup"><span data-stu-id="acc85-259">Function</span></span>                                                   | <span data-ttu-id="acc85-260">Description</span><span class="sxs-lookup"><span data-stu-id="acc85-260">Description</span></span>                                                                                                         |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="acc85-261">**lineReleaseUserUserInfo**</span><span class="sxs-lookup"><span data-stu-id="acc85-261">**lineReleaseUserUserInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linereleaseuseruserinfo) | <span data-ttu-id="acc85-262">Libère les informations de l’utilisateur, en permettant au système de remplacer ce stockage par de nouvelles informations.</span><span class="sxs-lookup"><span data-stu-id="acc85-262">Releases user-user information, permitting the system to overwrite this storage with new information.</span></span> <span data-ttu-id="acc85-263">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="acc85-263">Asynchronous.</span></span> |
| [<span data-ttu-id="acc85-264">**lineSendUserUserInfo**</span><span class="sxs-lookup"><span data-stu-id="acc85-264">**lineSendUserUserInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesenduseruserinfo)       | <span data-ttu-id="acc85-265">Envoie des informations utilisateur-utilisateur au tiers distant sur l’appel spécifié.</span><span class="sxs-lookup"><span data-stu-id="acc85-265">Sends user-user information to the remote party on the specified call.</span></span> <span data-ttu-id="acc85-266">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="acc85-266">Asynchronous.</span></span>                                |



 

## <a name="call-completion"></a><span data-ttu-id="acc85-267">Fin de l’appel</span><span class="sxs-lookup"><span data-stu-id="acc85-267">Call Completion</span></span>



| <span data-ttu-id="acc85-268">Fonction</span><span class="sxs-lookup"><span data-stu-id="acc85-268">Function</span></span>                                         | <span data-ttu-id="acc85-269">Description</span><span class="sxs-lookup"><span data-stu-id="acc85-269">Description</span></span>                                      |
|--------------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="acc85-270">**lineCompleteCall**</span><span class="sxs-lookup"><span data-stu-id="acc85-270">**lineCompleteCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linecompletecall)     | <span data-ttu-id="acc85-271">Place une demande d’achèvement d’appel.</span><span class="sxs-lookup"><span data-stu-id="acc85-271">Places a call completion request.</span></span> <span data-ttu-id="acc85-272">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="acc85-272">Asynchronous.</span></span>  |
| [<span data-ttu-id="acc85-273">**lineUncompleteCall**</span><span class="sxs-lookup"><span data-stu-id="acc85-273">**lineUncompleteCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall) | <span data-ttu-id="acc85-274">Annule une demande d’achèvement d’appel.</span><span class="sxs-lookup"><span data-stu-id="acc85-274">Cancels a call completion request.</span></span> <span data-ttu-id="acc85-275">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="acc85-275">Asynchronous.</span></span> |



 

## <a name="setting-a-terminal-for-phone-conversations"></a><span data-ttu-id="acc85-276">Définition d’un terminal pour les conversations sur téléphone</span><span class="sxs-lookup"><span data-stu-id="acc85-276">Setting a Terminal for Phone Conversations</span></span>



| <span data-ttu-id="acc85-277">Fonction</span><span class="sxs-lookup"><span data-stu-id="acc85-277">Function</span></span>                                   | <span data-ttu-id="acc85-278">Description</span><span class="sxs-lookup"><span data-stu-id="acc85-278">Description</span></span>                                                                                                                      |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="acc85-279">**lineSetTerminal**</span><span class="sxs-lookup"><span data-stu-id="acc85-279">**lineSetTerminal**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) | <span data-ttu-id="acc85-280">Spécifie l’appareil Terminal Server vers lequel les événements de ligne, d’adresse ou de flux de média d’appel sont routés.</span><span class="sxs-lookup"><span data-stu-id="acc85-280">Specifies the terminal device to which the specified line, address events, or call media stream events are routed.</span></span> <span data-ttu-id="acc85-281">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="acc85-281">Asynchronous.</span></span> |



 

## <a name="application-priority"></a><span data-ttu-id="acc85-282">Priorité de l’application</span><span class="sxs-lookup"><span data-stu-id="acc85-282">Application Priority</span></span>



| <span data-ttu-id="acc85-283">Fonction</span><span class="sxs-lookup"><span data-stu-id="acc85-283">Function</span></span>                                         | <span data-ttu-id="acc85-284">Description</span><span class="sxs-lookup"><span data-stu-id="acc85-284">Description</span></span>                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="acc85-285">**lineGetAppPriority**</span><span class="sxs-lookup"><span data-stu-id="acc85-285">**lineGetAppPriority**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetapppriority) | <span data-ttu-id="acc85-286">Récupère des informations sur la priorité de la téléphonie et/ou assistée pour une application.</span><span class="sxs-lookup"><span data-stu-id="acc85-286">Retrieves handoff and/or Assisted Telephony priority information for an application.</span></span> <span data-ttu-id="acc85-287">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="acc85-287">Synchronous.</span></span> |
| [<span data-ttu-id="acc85-288">**lineSetAppPriority**</span><span class="sxs-lookup"><span data-stu-id="acc85-288">**lineSetAppPriority**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetapppriority) | <span data-ttu-id="acc85-289">Définit le transfert et/ou la priorité de téléphonie assistée pour une application.</span><span class="sxs-lookup"><span data-stu-id="acc85-289">Sets the handoff and/or Assisted Telephony priority for an application.</span></span> <span data-ttu-id="acc85-290">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="acc85-290">Synchronous.</span></span>              |



 

## <a name="service-provider-management"></a><span data-ttu-id="acc85-291">Gestion des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="acc85-291">Service Provider Management</span></span>



| <span data-ttu-id="acc85-292">Fonction</span><span class="sxs-lookup"><span data-stu-id="acc85-292">Function</span></span>                                           | <span data-ttu-id="acc85-293">Description</span><span class="sxs-lookup"><span data-stu-id="acc85-293">Description</span></span>                                                           |
|----------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="acc85-294">**lineAddProvider**</span><span class="sxs-lookup"><span data-stu-id="acc85-294">**lineAddProvider**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineaddprovider)         | <span data-ttu-id="acc85-295">Installe un fournisseur de services de téléphonie.</span><span class="sxs-lookup"><span data-stu-id="acc85-295">Installs a telephony service provider.</span></span> <span data-ttu-id="acc85-296">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="acc85-296">Synchronous.</span></span>                   |
| [<span data-ttu-id="acc85-297">**lineConfigProvider**</span><span class="sxs-lookup"><span data-stu-id="acc85-297">**lineConfigProvider**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineconfigprovider)   | <span data-ttu-id="acc85-298">Affiche la boîte de dialogue de configuration d’un fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="acc85-298">Displays configuration dialog box of a service provider.</span></span> <span data-ttu-id="acc85-299">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="acc85-299">Synchronous.</span></span> |
| [<span data-ttu-id="acc85-300">**lineRemoveProvider**</span><span class="sxs-lookup"><span data-stu-id="acc85-300">**lineRemoveProvider**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineremoveprovider)   | <span data-ttu-id="acc85-301">Supprime un fournisseur de services de téléphonie existant.</span><span class="sxs-lookup"><span data-stu-id="acc85-301">Removes an existing telephony service provider.</span></span> <span data-ttu-id="acc85-302">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="acc85-302">Synchronous.</span></span>          |
| [<span data-ttu-id="acc85-303">**lineGetProviderList**</span><span class="sxs-lookup"><span data-stu-id="acc85-303">**lineGetProviderList**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetproviderlist) | <span data-ttu-id="acc85-304">Récupère la liste des fournisseurs de services installés.</span><span class="sxs-lookup"><span data-stu-id="acc85-304">Retrieves a list of installed service providers.</span></span> <span data-ttu-id="acc85-305">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="acc85-305">Synchronous.</span></span>         |



 

## <a name="agents"></a><span data-ttu-id="acc85-306">Agents</span><span class="sxs-lookup"><span data-stu-id="acc85-306">Agents</span></span>



| <span data-ttu-id="acc85-307">Fonction</span><span class="sxs-lookup"><span data-stu-id="acc85-307">Function</span></span>                                                     | <span data-ttu-id="acc85-308">Description</span><span class="sxs-lookup"><span data-stu-id="acc85-308">Description</span></span>                                                                                                                             |
|--------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="acc85-309">**lineAgentSpecific**</span><span class="sxs-lookup"><span data-stu-id="acc85-309">**lineAgentSpecific**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific)               | <span data-ttu-id="acc85-310">Permet à l’application d’accéder aux fonctions spécifiques du gestionnaire d’agents associées à l’adresse.</span><span class="sxs-lookup"><span data-stu-id="acc85-310">Allows the application to access proprietary handler-specific functions of the agent handler associated with the address.</span></span> <span data-ttu-id="acc85-311">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="acc85-311">Asynchronous.</span></span> |
| [<span data-ttu-id="acc85-312">**lineGetAgentActivityList**</span><span class="sxs-lookup"><span data-stu-id="acc85-312">**lineGetAgentActivityList**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetagentactivitylista) | <span data-ttu-id="acc85-313">Obtient la liste des activités à partir desquelles une application sélectionne les fonctions qu’un agent exécute.</span><span class="sxs-lookup"><span data-stu-id="acc85-313">Obtains the list of activities from which an application selects the functions an agent is performing.</span></span> <span data-ttu-id="acc85-314">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="acc85-314">Asynchronous.</span></span>                    |
| [<span data-ttu-id="acc85-315">**lineGetAgentCaps**</span><span class="sxs-lookup"><span data-stu-id="acc85-315">**lineGetAgentCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetagentcapsa)                 | <span data-ttu-id="acc85-316">Obtient les fonctionnalités liées à l’agent prises en charge sur le périphérique de ligne spécifié.</span><span class="sxs-lookup"><span data-stu-id="acc85-316">Obtains the agent-related capabilities supported on the specified line device.</span></span> <span data-ttu-id="acc85-317">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="acc85-317">Asynchronous.</span></span>                                            |
| [<span data-ttu-id="acc85-318">**lineGetAgentGroupList**</span><span class="sxs-lookup"><span data-stu-id="acc85-318">**lineGetAgentGroupList**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetagentgrouplista)       | <span data-ttu-id="acc85-319">Obtient la liste des groupes d’agents dans lesquels un agent peut se connecter sur le serveur de distribution d’appels automatique.</span><span class="sxs-lookup"><span data-stu-id="acc85-319">Obtains the list of agent groups into which an agent can log into on the automatic call distributor.</span></span> <span data-ttu-id="acc85-320">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="acc85-320">Asynchronous.</span></span>                      |
| [<span data-ttu-id="acc85-321">**lineGetAgentStatus**</span><span class="sxs-lookup"><span data-stu-id="acc85-321">**lineGetAgentStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa)             | <span data-ttu-id="acc85-322">Obtient l’état relatif à l’agent sur l’adresse spécifiée.</span><span class="sxs-lookup"><span data-stu-id="acc85-322">Obtains the agent-related status on the specified address.</span></span> <span data-ttu-id="acc85-323">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="acc85-323">Asynchronous.</span></span>                                                                |
| [<span data-ttu-id="acc85-324">**lineSetAgentActivity**</span><span class="sxs-lookup"><span data-stu-id="acc85-324">**lineSetAgentActivity**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetagentactivity)         | <span data-ttu-id="acc85-325">Définit le code d’activité de l’agent associé à une adresse particulière.</span><span class="sxs-lookup"><span data-stu-id="acc85-325">Sets the agent activity code associated with a particular address.</span></span> <span data-ttu-id="acc85-326">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="acc85-326">Asynchronous.</span></span>                                                        |
| [<span data-ttu-id="acc85-327">**lineSetAgentGroup**</span><span class="sxs-lookup"><span data-stu-id="acc85-327">**lineSetAgentGroup**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetagentgroup)               | <span data-ttu-id="acc85-328">Définit les groupes d’agents sur lesquels l’agent est connecté à une adresse particulière.</span><span class="sxs-lookup"><span data-stu-id="acc85-328">Sets the agent groups that the agent is logged into on a particular address.</span></span> <span data-ttu-id="acc85-329">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="acc85-329">Asynchronous.</span></span>                                              |
| [<span data-ttu-id="acc85-330">**lineSetAgentState**</span><span class="sxs-lookup"><span data-stu-id="acc85-330">**lineSetAgentState**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetagentstate)               | <span data-ttu-id="acc85-331">Définit l’état de l’agent associé à une adresse particulière.</span><span class="sxs-lookup"><span data-stu-id="acc85-331">Sets the agent state associated with a particular address.</span></span> <span data-ttu-id="acc85-332">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="acc85-332">Asynchronous.</span></span>                                                                |



 

## <a name="proxies"></a><span data-ttu-id="acc85-333">Proxies</span><span class="sxs-lookup"><span data-stu-id="acc85-333">Proxies</span></span>



| <span data-ttu-id="acc85-334">Fonction</span><span class="sxs-lookup"><span data-stu-id="acc85-334">Function</span></span>                                       | <span data-ttu-id="acc85-335">Description</span><span class="sxs-lookup"><span data-stu-id="acc85-335">Description</span></span>                                                                         |
|------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="acc85-336">**lineProxyMessage**</span><span class="sxs-lookup"><span data-stu-id="acc85-336">**lineProxyMessage**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)   | <span data-ttu-id="acc85-337">Utilisé par un gestionnaire de demandes de proxy inscrit pour générer des messages TAPI.</span><span class="sxs-lookup"><span data-stu-id="acc85-337">Used by a registered proxy request handler to generate TAPI messages.</span></span> <span data-ttu-id="acc85-338">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="acc85-338">Synchronous.</span></span>  |
| [<span data-ttu-id="acc85-339">**lineProxyResponse**</span><span class="sxs-lookup"><span data-stu-id="acc85-339">**lineProxyResponse**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) | <span data-ttu-id="acc85-340">Indique la fin d’une demande de proxy par un gestionnaire de proxy inscrit.</span><span class="sxs-lookup"><span data-stu-id="acc85-340">Indicates completion of a proxy request by a registered proxy handler.</span></span> <span data-ttu-id="acc85-341">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="acc85-341">Synchronous.</span></span> |



 

## <a name="quality-of-service"></a><span data-ttu-id="acc85-342">Qualité de service</span><span class="sxs-lookup"><span data-stu-id="acc85-342">Quality of Service</span></span>



| <span data-ttu-id="acc85-343">Fonction</span><span class="sxs-lookup"><span data-stu-id="acc85-343">Function</span></span>                                                           | <span data-ttu-id="acc85-344">Description</span><span class="sxs-lookup"><span data-stu-id="acc85-344">Description</span></span>                                                                                |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="acc85-345">**lineSetCallQualityOfService**</span><span class="sxs-lookup"><span data-stu-id="acc85-345">**lineSetCallQualityOfService**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetcallqualityofservice) | <span data-ttu-id="acc85-346">Demande une modification des paramètres de qualité de service pour un appel existant.</span><span class="sxs-lookup"><span data-stu-id="acc85-346">Requests a change of the quality of service parameters for an existing call.</span></span> <span data-ttu-id="acc85-347">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="acc85-347">Asynchronous.</span></span> |



 

## <a name="miscellaneous"></a><span data-ttu-id="acc85-348">Divers</span><span class="sxs-lookup"><span data-stu-id="acc85-348">Miscellaneous</span></span>



| <span data-ttu-id="acc85-349">Fonction</span><span class="sxs-lookup"><span data-stu-id="acc85-349">Function</span></span>                                             | <span data-ttu-id="acc85-350">Description</span><span class="sxs-lookup"><span data-stu-id="acc85-350">Description</span></span>                                                                                           |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="acc85-351">**lineSetCallData**</span><span class="sxs-lookup"><span data-stu-id="acc85-351">**lineSetCallData**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetcalldata)           | <span data-ttu-id="acc85-352">Définit le membre **CallData** de la structure [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) .</span><span class="sxs-lookup"><span data-stu-id="acc85-352">Sets the **CallData** member of the [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) structure.</span></span> <span data-ttu-id="acc85-353">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="acc85-353">Asynchronous.</span></span> |
| [<span data-ttu-id="acc85-354">**lineSetCallTreatment**</span><span class="sxs-lookup"><span data-stu-id="acc85-354">**lineSetCallTreatment**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetcalltreatment) | <span data-ttu-id="acc85-355">Définit les sons que l’utilisateur entend lorsqu’un appel n’est pas répondu ou qu’il est en attente.</span><span class="sxs-lookup"><span data-stu-id="acc85-355">Sets the sounds that the user hears when a call is unanswered or on hold.</span></span> <span data-ttu-id="acc85-356">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="acc85-356">Asynchronous.</span></span>               |
| [<span data-ttu-id="acc85-357">**lineSetLineDevStatus**</span><span class="sxs-lookup"><span data-stu-id="acc85-357">**lineSetLineDevStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus) | <span data-ttu-id="acc85-358">Définit l’état de l’appareil de ligne.</span><span class="sxs-lookup"><span data-stu-id="acc85-358">Sets the line device status.</span></span> <span data-ttu-id="acc85-359">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="acc85-359">Asynchronous.</span></span>                                                            |



 

 

 



