---
description: Les fonctions de service téléphonique supplémentaires sont répertoriées par catégorie dans les rubriques suivantes.
ms.assetid: 0d1a81d2-aa9e-4a85-85d3-aa4eabb26eb5
title: Fonctions de service téléphonique supplémentaires
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527c39441a924a4f9787d22bf8db596882e7f257
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519695"
---
# <a name="supplementary-phone-service-functions"></a><span data-ttu-id="c25f9-103">Fonctions de service téléphonique supplémentaires</span><span class="sxs-lookup"><span data-stu-id="c25f9-103">Supplementary Phone Service Functions</span></span>

<span data-ttu-id="c25f9-104">Les fonctions de service téléphonique supplémentaires sont répertoriées par catégorie dans les rubriques suivantes.</span><span class="sxs-lookup"><span data-stu-id="c25f9-104">The supplementary phone service functions are listed by category in the following topics.</span></span> <span data-ttu-id="c25f9-105">Une fonction est identifiée comme [*asynchrone*](a-tapgloss.md) si elle indique la fin d’un message de réponse à l’application.</span><span class="sxs-lookup"><span data-stu-id="c25f9-105">A function is identified as [*asynchronous*](a-tapgloss.md) if it will indicate completion in a REPLY message to the application.</span></span> <span data-ttu-id="c25f9-106">Si la fonction retourne toujours son résultat à l’application immédiatement, la fonction est considérée comme [*synchrone*](s-tapgloss.md).</span><span class="sxs-lookup"><span data-stu-id="c25f9-106">If the function always returns its result to the application immediately, the function is considered [*synchronous*](s-tapgloss.md).</span></span>

<span data-ttu-id="c25f9-107">Voici un regroupement fonctionnel des fonctions supplémentaires de service téléphonique :</span><span class="sxs-lookup"><span data-stu-id="c25f9-107">Following is a functional grouping of the supplementary phone service functions:</span></span>

-   [<span data-ttu-id="c25f9-108">Boutons</span><span class="sxs-lookup"><span data-stu-id="c25f9-108">Buttons</span></span>](#buttons)
-   [<span data-ttu-id="c25f9-109">Zones de données</span><span class="sxs-lookup"><span data-stu-id="c25f9-109">Data areas</span></span>](#data-areas)
-   [<span data-ttu-id="c25f9-110">Affichage</span><span class="sxs-lookup"><span data-stu-id="c25f9-110">Display</span></span>](#display)
-   [<span data-ttu-id="c25f9-111">Appareils hookswitch</span><span class="sxs-lookup"><span data-stu-id="c25f9-111">Hookswitch devices</span></span>](#hookswitch-devices)
-   [<span data-ttu-id="c25f9-112">Lampes</span><span class="sxs-lookup"><span data-stu-id="c25f9-112">Lamps</span></span>](#lamps)
-   [<span data-ttu-id="c25f9-113">Ouverture et fermeture des appareils téléphoniques</span><span class="sxs-lookup"><span data-stu-id="c25f9-113">Opening and closing phone devices</span></span>](#opening-and-closing-phone-devices)
-   [<span data-ttu-id="c25f9-114">Initialisation et arrêt du téléphone</span><span class="sxs-lookup"><span data-stu-id="c25f9-114">Phone initialization and shutdown</span></span>](#phone-initialization-and-shutdown)
-   [<span data-ttu-id="c25f9-115">État du téléphone et fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="c25f9-115">Phone status and capabilities</span></span>](#phone-status-and-capabilities)
-   [<span data-ttu-id="c25f9-116">Négociation de version de téléphone</span><span class="sxs-lookup"><span data-stu-id="c25f9-116">Phone version negotiation</span></span>](#phone-version-negotiation)
-   [<span data-ttu-id="c25f9-117">Alarme</span><span class="sxs-lookup"><span data-stu-id="c25f9-117">Ring</span></span>](#ring)
-   [<span data-ttu-id="c25f9-118">État</span><span class="sxs-lookup"><span data-stu-id="c25f9-118">Status</span></span>](#status)

## <a name="phone-initialization-and-shutdown"></a><span data-ttu-id="c25f9-119">Initialisation et arrêt du téléphone</span><span class="sxs-lookup"><span data-stu-id="c25f9-119">Phone Initialization and Shutdown</span></span>



| <span data-ttu-id="c25f9-120">Fonction</span><span class="sxs-lookup"><span data-stu-id="c25f9-120">Function</span></span>                                       | <span data-ttu-id="c25f9-121">Description</span><span class="sxs-lookup"><span data-stu-id="c25f9-121">Description</span></span>                                                                          |
|------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="c25f9-122">**phoneInitializeEx**</span><span class="sxs-lookup"><span data-stu-id="c25f9-122">**phoneInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) | <span data-ttu-id="c25f9-123">Initialise l’abstraction de téléphone TAPI pour une utilisation par l’application appelante.</span><span class="sxs-lookup"><span data-stu-id="c25f9-123">Initializes TAPI phone abstraction for use by the invoking application.</span></span> <span data-ttu-id="c25f9-124">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="c25f9-124">Synchronous.</span></span> |
| [<span data-ttu-id="c25f9-125">**phoneShutdown**</span><span class="sxs-lookup"><span data-stu-id="c25f9-125">**phoneShutdown**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)         | <span data-ttu-id="c25f9-126">Arrête l’utilisation par l’application de l’abstraction téléphonique de l’interface TAPI.</span><span class="sxs-lookup"><span data-stu-id="c25f9-126">Shuts down an application's use of TAPI's phone abstraction.</span></span> <span data-ttu-id="c25f9-127">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="c25f9-127">Synchronous.</span></span>            |



 

## <a name="phone-version-negotiation"></a><span data-ttu-id="c25f9-128">Négociation de version de téléphone</span><span class="sxs-lookup"><span data-stu-id="c25f9-128">Phone Version Negotiation</span></span>



| <span data-ttu-id="c25f9-129">Fonction</span><span class="sxs-lookup"><span data-stu-id="c25f9-129">Function</span></span>                                                     | <span data-ttu-id="c25f9-130">Description</span><span class="sxs-lookup"><span data-stu-id="c25f9-130">Description</span></span>                                                            |
|--------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="c25f9-131">**phoneNegotiateAPIVersion**</span><span class="sxs-lookup"><span data-stu-id="c25f9-131">**phoneNegotiateAPIVersion**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion) | <span data-ttu-id="c25f9-132">Permet à une application de négocier une version TAPI à utiliser.</span><span class="sxs-lookup"><span data-stu-id="c25f9-132">Allows an application to negotiate a TAPI version to use.</span></span> <span data-ttu-id="c25f9-133">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="c25f9-133">Synchronous.</span></span> |



 

## <a name="opening-and-closing-phone-devices"></a><span data-ttu-id="c25f9-134">Ouverture et fermeture des appareils téléphoniques</span><span class="sxs-lookup"><span data-stu-id="c25f9-134">Opening and Closing Phone Devices</span></span>



| <span data-ttu-id="c25f9-135">Fonction</span><span class="sxs-lookup"><span data-stu-id="c25f9-135">Function</span></span>                         | <span data-ttu-id="c25f9-136">Description</span><span class="sxs-lookup"><span data-stu-id="c25f9-136">Description</span></span>                                                                                               |
|----------------------------------|-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c25f9-137">**phoneOpen**</span><span class="sxs-lookup"><span data-stu-id="c25f9-137">**phoneOpen**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneopen)   | <span data-ttu-id="c25f9-138">Ouvre l’appareil téléphonique spécifié, en accordant à l’application des privilèges de propriétaire ou de surveillance.</span><span class="sxs-lookup"><span data-stu-id="c25f9-138">Opens the specified phone device, giving the application either owner or monitor privileges.</span></span> <span data-ttu-id="c25f9-139">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="c25f9-139">Synchronous.</span></span> |
| [<span data-ttu-id="c25f9-140">**phoneClose**</span><span class="sxs-lookup"><span data-stu-id="c25f9-140">**phoneClose**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneclose) | <span data-ttu-id="c25f9-141">Ferme un appareil téléphonique ouvert spécifié.</span><span class="sxs-lookup"><span data-stu-id="c25f9-141">Closes a specified open phone device.</span></span> <span data-ttu-id="c25f9-142">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="c25f9-142">Synchronous.</span></span>                                                        |



 

## <a name="phone-status-and-capabilities"></a><span data-ttu-id="c25f9-143">État du téléphone et fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="c25f9-143">Phone Status and Capabilities</span></span>



| <span data-ttu-id="c25f9-144">Fonction</span><span class="sxs-lookup"><span data-stu-id="c25f9-144">Function</span></span>                                       | <span data-ttu-id="c25f9-145">Description</span><span class="sxs-lookup"><span data-stu-id="c25f9-145">Description</span></span>                                                                                                                                                      |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c25f9-146">**phoneGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="c25f9-146">**phoneGetDevCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)     | <span data-ttu-id="c25f9-147">Retourne les fonctionnalités d’un appareil téléphonique donné.</span><span class="sxs-lookup"><span data-stu-id="c25f9-147">Returns the capabilities of a given phone device.</span></span> <span data-ttu-id="c25f9-148">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="c25f9-148">Synchronous.</span></span>                                                                                                   |
| [<span data-ttu-id="c25f9-149">**phoneGetID**</span><span class="sxs-lookup"><span data-stu-id="c25f9-149">**phoneGetID**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetid)               | <span data-ttu-id="c25f9-150">Retourne un ID d’appareil pour la classe d’appareil donnée associée à l’appareil téléphonique spécifié.</span><span class="sxs-lookup"><span data-stu-id="c25f9-150">Returns a device ID for the given device class associated with the specified phone device.</span></span> <span data-ttu-id="c25f9-151">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="c25f9-151">Synchronous.</span></span>                                                          |
| [<span data-ttu-id="c25f9-152">**phoneGetIcon**</span><span class="sxs-lookup"><span data-stu-id="c25f9-152">**phoneGetIcon**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegeticon)           | <span data-ttu-id="c25f9-153">Permet à une application de récupérer une icône à afficher à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c25f9-153">Allows an application to retrieve an icon for display to the user.</span></span> <span data-ttu-id="c25f9-154">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="c25f9-154">Synchronous.</span></span>                                                                                  |
| [<span data-ttu-id="c25f9-155">**phoneConfigDialog**</span><span class="sxs-lookup"><span data-stu-id="c25f9-155">**phoneConfigDialog**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneconfigdialog) | <span data-ttu-id="c25f9-156">Fait en sorte que le fournisseur de l’appareil téléphonique spécifié affiche une boîte de dialogue qui permet à l’utilisateur de configurer les paramètres liés à l’appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="c25f9-156">Causes the provider of the specified phone device to display a dialog box that allows the user to configure parameters related to the phone device.</span></span> <span data-ttu-id="c25f9-157">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="c25f9-157">Synchronous.</span></span> |



 

## <a name="hookswitch-devices"></a><span data-ttu-id="c25f9-158">Appareils hookswitch</span><span class="sxs-lookup"><span data-stu-id="c25f9-158">Hookswitch Devices</span></span>



| <span data-ttu-id="c25f9-159">Fonction</span><span class="sxs-lookup"><span data-stu-id="c25f9-159">Function</span></span>                                         | <span data-ttu-id="c25f9-160">Description</span><span class="sxs-lookup"><span data-stu-id="c25f9-160">Description</span></span>                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c25f9-161">**phoneSetHookSwitch**</span><span class="sxs-lookup"><span data-stu-id="c25f9-161">**phoneSetHookSwitch**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) | <span data-ttu-id="c25f9-162">Définit l’état du raccordement des appareils hookswitch d’un téléphone ouvert sur un mode spécifié.</span><span class="sxs-lookup"><span data-stu-id="c25f9-162">Sets the hook state of an open phone's hookswitch devices to a specified mode.</span></span> <span data-ttu-id="c25f9-163">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="c25f9-163">Asynchronous.</span></span>      |
| [<span data-ttu-id="c25f9-164">**phoneGetHookSwitch**</span><span class="sxs-lookup"><span data-stu-id="c25f9-164">**phoneGetHookSwitch**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) | <span data-ttu-id="c25f9-165">Interroge le mode hookswitch d’un appareil hookswitch sur un appareil téléphonique ouvert.</span><span class="sxs-lookup"><span data-stu-id="c25f9-165">Queries the hookswitch mode of a hookswitch device of an open phone device.</span></span> <span data-ttu-id="c25f9-166">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="c25f9-166">Synchronous.</span></span>          |
| [<span data-ttu-id="c25f9-167">**phoneSetVolume**</span><span class="sxs-lookup"><span data-stu-id="c25f9-167">**phoneSetVolume**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetvolume)         | <span data-ttu-id="c25f9-168">Définit le volume du haut-parleur d’un appareil hookswitch d’un appareil téléphonique ouvert.</span><span class="sxs-lookup"><span data-stu-id="c25f9-168">Sets the volume of a hookswitch device's speaker of an open phone device.</span></span> <span data-ttu-id="c25f9-169">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="c25f9-169">Asynchronous.</span></span>           |
| [<span data-ttu-id="c25f9-170">**phoneGetVolume**</span><span class="sxs-lookup"><span data-stu-id="c25f9-170">**phoneGetVolume**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetvolume)         | <span data-ttu-id="c25f9-171">Retourne le paramètre de volume du haut-parleur d’un appareil hookswitch d’un appareil téléphonique ouvert.</span><span class="sxs-lookup"><span data-stu-id="c25f9-171">Returns the volume setting of a hookswitch device's speaker of an open phone device.</span></span> <span data-ttu-id="c25f9-172">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="c25f9-172">Synchronous.</span></span> |
| [<span data-ttu-id="c25f9-173">**phoneSetGain**</span><span class="sxs-lookup"><span data-stu-id="c25f9-173">**phoneSetGain**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetgain)             | <span data-ttu-id="c25f9-174">Définit le gain du MIC d’un appareil hookswitch d’un appareil téléphonique ouvert.</span><span class="sxs-lookup"><span data-stu-id="c25f9-174">Sets the gain of a hookswitch device's mic of an open phone device.</span></span> <span data-ttu-id="c25f9-175">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="c25f9-175">Asynchronous.</span></span>                 |
| [<span data-ttu-id="c25f9-176">**phoneGetGain**</span><span class="sxs-lookup"><span data-stu-id="c25f9-176">**phoneGetGain**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetgain)             | <span data-ttu-id="c25f9-177">Retourne le paramètre de gain du MIC d’un appareil hookswitch d’un téléphone ouvert.</span><span class="sxs-lookup"><span data-stu-id="c25f9-177">Returns the gain setting of a hookswitch device's mic of an open phone.</span></span> <span data-ttu-id="c25f9-178">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="c25f9-178">Synchronous.</span></span>              |



 

## <a name="display"></a><span data-ttu-id="c25f9-179">Afficher</span><span class="sxs-lookup"><span data-stu-id="c25f9-179">Display</span></span>



| <span data-ttu-id="c25f9-180">Fonction</span><span class="sxs-lookup"><span data-stu-id="c25f9-180">Function</span></span>                                   | <span data-ttu-id="c25f9-181">Description</span><span class="sxs-lookup"><span data-stu-id="c25f9-181">Description</span></span>                                                              |
|--------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="c25f9-182">**phoneSetDisplay**</span><span class="sxs-lookup"><span data-stu-id="c25f9-182">**phoneSetDisplay**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetdisplay) | <span data-ttu-id="c25f9-183">Écrit des informations sur l’affichage d’un appareil téléphonique ouvert.</span><span class="sxs-lookup"><span data-stu-id="c25f9-183">Writes information to the display of an open phone device.</span></span> <span data-ttu-id="c25f9-184">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="c25f9-184">Asynchronous.</span></span> |
| [<span data-ttu-id="c25f9-185">**phoneGetDisplay**</span><span class="sxs-lookup"><span data-stu-id="c25f9-185">**phoneGetDisplay**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetdisplay) | <span data-ttu-id="c25f9-186">Retourne le contenu actuel de l’affichage d’un téléphone.</span><span class="sxs-lookup"><span data-stu-id="c25f9-186">Returns the current contents of a phone's display.</span></span> <span data-ttu-id="c25f9-187">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="c25f9-187">Synchronous.</span></span>          |



 

## <a name="ring"></a><span data-ttu-id="c25f9-188">Anneau</span><span class="sxs-lookup"><span data-stu-id="c25f9-188">Ring</span></span>



| <span data-ttu-id="c25f9-189">Fonction</span><span class="sxs-lookup"><span data-stu-id="c25f9-189">Function</span></span>                             | <span data-ttu-id="c25f9-190">Description</span><span class="sxs-lookup"><span data-stu-id="c25f9-190">Description</span></span>                                                              |
|--------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="c25f9-191">**phoneSetRing**</span><span class="sxs-lookup"><span data-stu-id="c25f9-191">**phoneSetRing**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetring) | <span data-ttu-id="c25f9-192">Sonne un appareil téléphonique ouvert en fonction d’un mode de sonnerie donné.</span><span class="sxs-lookup"><span data-stu-id="c25f9-192">Rings an open phone device according to a given ring mode.</span></span> <span data-ttu-id="c25f9-193">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="c25f9-193">Asynchronous.</span></span> |
| [<span data-ttu-id="c25f9-194">**phoneGetRing**</span><span class="sxs-lookup"><span data-stu-id="c25f9-194">**phoneGetRing**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetring) | <span data-ttu-id="c25f9-195">Retourne le mode de sonnerie actuel d’un appareil téléphonique ouvert.</span><span class="sxs-lookup"><span data-stu-id="c25f9-195">Returns the current ring mode of an opened phone device.</span></span> <span data-ttu-id="c25f9-196">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="c25f9-196">Synchronous.</span></span>    |



 

## <a name="buttons"></a><span data-ttu-id="c25f9-197">Boutons</span><span class="sxs-lookup"><span data-stu-id="c25f9-197">Buttons</span></span>



| <span data-ttu-id="c25f9-198">Fonction</span><span class="sxs-lookup"><span data-stu-id="c25f9-198">Function</span></span>                                         | <span data-ttu-id="c25f9-199">Description</span><span class="sxs-lookup"><span data-stu-id="c25f9-199">Description</span></span>                                                                    |
|--------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="c25f9-200">**phoneSetButtonInfo**</span><span class="sxs-lookup"><span data-stu-id="c25f9-200">**phoneSetButtonInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetbuttoninfo) | <span data-ttu-id="c25f9-201">Définit les informations associées à un bouton sur un appareil téléphonique.</span><span class="sxs-lookup"><span data-stu-id="c25f9-201">Sets the information associated with a button on a phone device.</span></span> <span data-ttu-id="c25f9-202">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="c25f9-202">Asynchronous.</span></span> |
| [<span data-ttu-id="c25f9-203">**phoneGetButtonInfo**</span><span class="sxs-lookup"><span data-stu-id="c25f9-203">**phoneGetButtonInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo) | <span data-ttu-id="c25f9-204">Retourne les informations associées à un bouton sur un appareil téléphonique.</span><span class="sxs-lookup"><span data-stu-id="c25f9-204">Returns information associated with a button on a phone device.</span></span> <span data-ttu-id="c25f9-205">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="c25f9-205">Synchronous.</span></span>   |



 

## <a name="lamps"></a><span data-ttu-id="c25f9-206">Lampes</span><span class="sxs-lookup"><span data-stu-id="c25f9-206">Lamps</span></span>



| <span data-ttu-id="c25f9-207">Fonction</span><span class="sxs-lookup"><span data-stu-id="c25f9-207">Function</span></span>                             | <span data-ttu-id="c25f9-208">Description</span><span class="sxs-lookup"><span data-stu-id="c25f9-208">Description</span></span>                                                                                 |
|--------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c25f9-209">**phoneSetLamp**</span><span class="sxs-lookup"><span data-stu-id="c25f9-209">**phoneSetLamp**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetlamp) | <span data-ttu-id="c25f9-210">Illumine une lampe sur un appareil téléphonique ouvert spécifié dans un mode d’éclairage donné de la lampe.</span><span class="sxs-lookup"><span data-stu-id="c25f9-210">Lights a lamp on a specified open phone device in a given lamp lighting mode.</span></span> <span data-ttu-id="c25f9-211">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="c25f9-211">Asynchronous.</span></span> |
| [<span data-ttu-id="c25f9-212">**phoneGetLamp**</span><span class="sxs-lookup"><span data-stu-id="c25f9-212">**phoneGetLamp**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetlamp) | <span data-ttu-id="c25f9-213">Retourne le mode de lampe actuel de la lampe spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c25f9-213">Returns the current lamp mode of the specified lamp.</span></span> <span data-ttu-id="c25f9-214">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="c25f9-214">Synchronous.</span></span>                           |



 

## <a name="data-areas"></a><span data-ttu-id="c25f9-215">Zones de données</span><span class="sxs-lookup"><span data-stu-id="c25f9-215">Data Areas</span></span>



| <span data-ttu-id="c25f9-216">Fonction</span><span class="sxs-lookup"><span data-stu-id="c25f9-216">Function</span></span>                             | <span data-ttu-id="c25f9-217">Description</span><span class="sxs-lookup"><span data-stu-id="c25f9-217">Description</span></span>                                                                             |
|--------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="c25f9-218">**phoneSetData**</span><span class="sxs-lookup"><span data-stu-id="c25f9-218">**phoneSetData**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetdata) | <span data-ttu-id="c25f9-219">Télécharge une mémoire tampon de données dans une zone de données donnée du périphérique téléphonique.</span><span class="sxs-lookup"><span data-stu-id="c25f9-219">Downloads a buffer of data to a given data area in the phone device.</span></span> <span data-ttu-id="c25f9-220">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="c25f9-220">Asynchronous.</span></span>      |
| [<span data-ttu-id="c25f9-221">**phoneGetData**</span><span class="sxs-lookup"><span data-stu-id="c25f9-221">**phoneGetData**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetdata) | <span data-ttu-id="c25f9-222">Charge le contenu d’une zone de données donnée dans le périphérique téléphonique dans une mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="c25f9-222">Uploads the contents of a given data area in the phone device to a buffer.</span></span> <span data-ttu-id="c25f9-223">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="c25f9-223">Synchronous.</span></span> |



 

## <a name="status"></a><span data-ttu-id="c25f9-224">Statut</span><span class="sxs-lookup"><span data-stu-id="c25f9-224">Status</span></span>



| <span data-ttu-id="c25f9-225">Fonction</span><span class="sxs-lookup"><span data-stu-id="c25f9-225">Function</span></span>                                                 | <span data-ttu-id="c25f9-226">Description</span><span class="sxs-lookup"><span data-stu-id="c25f9-226">Description</span></span>                                                                               |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c25f9-227">**phoneSetStatusMessages**</span><span class="sxs-lookup"><span data-stu-id="c25f9-227">**phoneSetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) | <span data-ttu-id="c25f9-228">Spécifie les modifications d’État pour lesquelles l’application souhaite être notifiée.</span><span class="sxs-lookup"><span data-stu-id="c25f9-228">Specifies the status changes for which the application wants to be notified.</span></span> <span data-ttu-id="c25f9-229">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="c25f9-229">Synchronous.</span></span> |
| [<span data-ttu-id="c25f9-230">**phoneGetStatusMessages**</span><span class="sxs-lookup"><span data-stu-id="c25f9-230">**phoneGetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages) | <span data-ttu-id="c25f9-231">Retourne les modifications d’État pour lesquelles l’application souhaite être notifiée.</span><span class="sxs-lookup"><span data-stu-id="c25f9-231">Returns the status changes for which the application wants to be notified.</span></span> <span data-ttu-id="c25f9-232">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="c25f9-232">Synchronous.</span></span>   |
| [<span data-ttu-id="c25f9-233">**phoneGetStatus**</span><span class="sxs-lookup"><span data-stu-id="c25f9-233">**phoneGetStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus)                 | <span data-ttu-id="c25f9-234">Retourne l’état complet d’un appareil téléphonique ouvert.</span><span class="sxs-lookup"><span data-stu-id="c25f9-234">Returns the complete status of an open phone device.</span></span> <span data-ttu-id="c25f9-235">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="c25f9-235">Synchronous.</span></span>                         |



 

 

 



