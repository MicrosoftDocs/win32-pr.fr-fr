---
description: Les fonctions de téléphonie de base sont répertoriées par catégorie dans les tableaux suivants.
ms.assetid: 09d10789-bc36-47c7-b77d-8698ae75541a
title: Informations de référence sur les services de téléphonie de base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abe1282a406ea6746f1bb3af11d65164d8af0ce0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534437"
---
# <a name="basic-telephony-services-reference"></a><span data-ttu-id="2aedf-103">Informations de référence sur les services de téléphonie de base</span><span class="sxs-lookup"><span data-stu-id="2aedf-103">Basic Telephony Services Reference</span></span>

<span data-ttu-id="2aedf-104">Les fonctions de téléphonie de base sont répertoriées par catégorie dans les tableaux suivants.</span><span class="sxs-lookup"><span data-stu-id="2aedf-104">The Basic Telephony functions are listed by category in the following tables.</span></span> <span data-ttu-id="2aedf-105">Une fonction est identifiée comme [*asynchrone*](a-tapgloss.md) si elle indique la fin d’un message de réponse à l’application.</span><span class="sxs-lookup"><span data-stu-id="2aedf-105">A function is identified as [*asynchronous*](a-tapgloss.md) if it indicates completion in a REPLY message to the application.</span></span> <span data-ttu-id="2aedf-106">Si la fonction retourne toujours son résultat à l’application immédiatement, la fonction est considérée comme [*synchrone*](s-tapgloss.md).</span><span class="sxs-lookup"><span data-stu-id="2aedf-106">If the function always returns its result to the application immediately, the function is considered [*synchronous*](s-tapgloss.md).</span></span>

<span data-ttu-id="2aedf-107">Voici un regroupement fonctionnel des fonctions de base de service de téléphonie :</span><span class="sxs-lookup"><span data-stu-id="2aedf-107">Following is a functional grouping of the basic telephony service functions:</span></span>

-   [<span data-ttu-id="2aedf-108">Formats d’adresse</span><span class="sxs-lookup"><span data-stu-id="2aedf-108">Address Formats</span></span>](#address-formats)
-   [<span data-ttu-id="2aedf-109">Adresses</span><span class="sxs-lookup"><span data-stu-id="2aedf-109">Addresses</span></span>](#addresses)
-   [<span data-ttu-id="2aedf-110">Réponse aux appels entrants</span><span class="sxs-lookup"><span data-stu-id="2aedf-110">Answering Incoming Calls</span></span>](#answering-incoming-calls)
-   [<span data-ttu-id="2aedf-111">Appeler des fonctions Drop</span><span class="sxs-lookup"><span data-stu-id="2aedf-111">Call Drop Functions</span></span>](#call-drop-functions)
-   [<span data-ttu-id="2aedf-112">Appeler une manipulation de handle</span><span class="sxs-lookup"><span data-stu-id="2aedf-112">Call Handle Manipulation</span></span>](#call-handle-manipulation)
-   [<span data-ttu-id="2aedf-113">Contrôle des privilèges d’appel</span><span class="sxs-lookup"><span data-stu-id="2aedf-113">Call Privilege Control</span></span>](#call-privilege-control)
-   [<span data-ttu-id="2aedf-114">États d’appel et événements</span><span class="sxs-lookup"><span data-stu-id="2aedf-114">Call States and Events</span></span>](#call-states-and-events)
-   [<span data-ttu-id="2aedf-115">État de ligne et fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="2aedf-115">Line Status and Capabilities</span></span>](#line-status-and-capabilities)
-   [<span data-ttu-id="2aedf-116">Négociation de version de ligne</span><span class="sxs-lookup"><span data-stu-id="2aedf-116">Line Version Negotiation</span></span>](#line-version-negotiation)
-   [<span data-ttu-id="2aedf-117">Informations sur l’emplacement et le pays/la région</span><span class="sxs-lookup"><span data-stu-id="2aedf-117">Location and Country/Region Information</span></span>](#location-and-countryregion-information)
-   [<span data-ttu-id="2aedf-118">Appels effectués</span><span class="sxs-lookup"><span data-stu-id="2aedf-118">Making Calls</span></span>](#making-calls)
-   [<span data-ttu-id="2aedf-119">Ouverture et fermeture des appareils en ligne</span><span class="sxs-lookup"><span data-stu-id="2aedf-119">Opening and Closing Line Devices</span></span>](#opening-and-closing-line-devices)
-   [<span data-ttu-id="2aedf-120">Services de destinataire de la demande</span><span class="sxs-lookup"><span data-stu-id="2aedf-120">Request Recipient Services</span></span>](#request-recipient-services)
-   [<span data-ttu-id="2aedf-121">Initialisation et arrêt de l’interface TAPI</span><span class="sxs-lookup"><span data-stu-id="2aedf-121">TAPI Initialization and Shutdown</span></span>](#tapi-initialization-and-shutdown)
-   [<span data-ttu-id="2aedf-122">Prise en charge de péage Saver</span><span class="sxs-lookup"><span data-stu-id="2aedf-122">Toll Saver Support</span></span>](#toll-saver-support)

## <a name="tapi-initialization-and-shutdown"></a><span data-ttu-id="2aedf-123">Initialisation et arrêt de l’interface TAPI</span><span class="sxs-lookup"><span data-stu-id="2aedf-123">TAPI Initialization and Shutdown</span></span>



| <span data-ttu-id="2aedf-124">Fonction</span><span class="sxs-lookup"><span data-stu-id="2aedf-124">Function</span></span>                                     | <span data-ttu-id="2aedf-125">Description</span><span class="sxs-lookup"><span data-stu-id="2aedf-125">Description</span></span>                                                                             |
|----------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="2aedf-126">**lineInitializeEx**</span><span class="sxs-lookup"><span data-stu-id="2aedf-126">**lineInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa) | <span data-ttu-id="2aedf-127">Initialise l’abstraction de ligne TAPI pour une utilisation par l’application appelante.</span><span class="sxs-lookup"><span data-stu-id="2aedf-127">Initializes the TAPI line abstraction for use by the invoking application.</span></span> <span data-ttu-id="2aedf-128">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2aedf-128">Synchronous.</span></span> |
| [<span data-ttu-id="2aedf-129">**lineShutdown**</span><span class="sxs-lookup"><span data-stu-id="2aedf-129">**lineShutdown**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)         | <span data-ttu-id="2aedf-130">Arrête l’utilisation de l’application de l’abstraction de ligne TAPI.</span><span class="sxs-lookup"><span data-stu-id="2aedf-130">Shuts down the application's use of TAPI's line abstraction.</span></span> <span data-ttu-id="2aedf-131">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2aedf-131">Synchronous.</span></span>               |



 

## <a name="line-version-negotiation"></a><span data-ttu-id="2aedf-132">Négociation de version de ligne</span><span class="sxs-lookup"><span data-stu-id="2aedf-132">Line Version Negotiation</span></span>



| <span data-ttu-id="2aedf-133">Fonction</span><span class="sxs-lookup"><span data-stu-id="2aedf-133">Function</span></span>                                                   | <span data-ttu-id="2aedf-134">Description</span><span class="sxs-lookup"><span data-stu-id="2aedf-134">Description</span></span>                                                            |
|------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="2aedf-135">**lineNegotiateAPIVersion**</span><span class="sxs-lookup"><span data-stu-id="2aedf-135">**lineNegotiateAPIVersion**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion) | <span data-ttu-id="2aedf-136">Permet à une application de négocier une version TAPI à utiliser.</span><span class="sxs-lookup"><span data-stu-id="2aedf-136">Allows an application to negotiate a TAPI version to use.</span></span> <span data-ttu-id="2aedf-137">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2aedf-137">Synchronous.</span></span> |



 

## <a name="line-status-and-capabilities"></a><span data-ttu-id="2aedf-138">État de ligne et fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="2aedf-138">Line Status and Capabilities</span></span>



| <span data-ttu-id="2aedf-139">Fonction</span><span class="sxs-lookup"><span data-stu-id="2aedf-139">Function</span></span>                                               | <span data-ttu-id="2aedf-140">Description</span><span class="sxs-lookup"><span data-stu-id="2aedf-140">Description</span></span>                                                                                                                                                    |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2aedf-141">**lineGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="2aedf-141">**lineGetDevCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)               | <span data-ttu-id="2aedf-142">Retourne les fonctionnalités d’un périphérique de ligne donné.</span><span class="sxs-lookup"><span data-stu-id="2aedf-142">Returns the capabilities of a given line device.</span></span> <span data-ttu-id="2aedf-143">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2aedf-143">Synchronous.</span></span>                                                                                                  |
| [<span data-ttu-id="2aedf-144">**lineGetDevConfig**</span><span class="sxs-lookup"><span data-stu-id="2aedf-144">**lineGetDevConfig**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig)           | <span data-ttu-id="2aedf-145">Retourne la configuration d’un périphérique de flux multimédia.</span><span class="sxs-lookup"><span data-stu-id="2aedf-145">Returns configuration of a media stream device.</span></span> <span data-ttu-id="2aedf-146">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2aedf-146">Synchronous.</span></span>                                                                                                   |
| [<span data-ttu-id="2aedf-147">**lineGetLineDevStatus**</span><span class="sxs-lookup"><span data-stu-id="2aedf-147">**lineGetLineDevStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)   | <span data-ttu-id="2aedf-148">Retourne l’état actuel du périphérique en ligne ouvert spécifié.</span><span class="sxs-lookup"><span data-stu-id="2aedf-148">Returns current status of the specified open line device.</span></span> <span data-ttu-id="2aedf-149">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2aedf-149">Synchronous.</span></span>                                                                                         |
| [<span data-ttu-id="2aedf-150">**lineSetDevConfig**</span><span class="sxs-lookup"><span data-stu-id="2aedf-150">**lineSetDevConfig**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig)           | <span data-ttu-id="2aedf-151">Définit la configuration du périphérique de flux multimédia spécifié.</span><span class="sxs-lookup"><span data-stu-id="2aedf-151">Sets the configuration of the specified media stream device.</span></span> <span data-ttu-id="2aedf-152">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2aedf-152">Synchronous.</span></span>                                                                                      |
| [<span data-ttu-id="2aedf-153">**lineSetStatusMessages**</span><span class="sxs-lookup"><span data-stu-id="2aedf-153">**lineSetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages) | <span data-ttu-id="2aedf-154">Spécifie les modifications d’État pour lesquelles l’application doit être notifiée.</span><span class="sxs-lookup"><span data-stu-id="2aedf-154">Specifies the status changes for which the application needs to be notified.</span></span> <span data-ttu-id="2aedf-155">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2aedf-155">Synchronous.</span></span>                                                                      |
| [<span data-ttu-id="2aedf-156">**lineGetStatusMessages**</span><span class="sxs-lookup"><span data-stu-id="2aedf-156">**lineGetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetstatusmessages) | <span data-ttu-id="2aedf-157">Retourne les paramètres de la ligne actuelle et de l’adresse de l’application.</span><span class="sxs-lookup"><span data-stu-id="2aedf-157">Returns the application's current line and address status message settings.</span></span> <span data-ttu-id="2aedf-158">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2aedf-158">Synchronous.</span></span>                                                                       |
| [<span data-ttu-id="2aedf-159">**lineGetID**</span><span class="sxs-lookup"><span data-stu-id="2aedf-159">**lineGetID**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetid)                         | <span data-ttu-id="2aedf-160">Récupère un ID d’appareil associé à l’ouverture de ligne, à l’adresse ou à l’appel spécifié.</span><span class="sxs-lookup"><span data-stu-id="2aedf-160">Retrieves a device ID associated with the specified open line, address, or call.</span></span> <span data-ttu-id="2aedf-161">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2aedf-161">Synchronous.</span></span>                                                                  |
| [<span data-ttu-id="2aedf-162">**lineGetIcon**</span><span class="sxs-lookup"><span data-stu-id="2aedf-162">**lineGetIcon**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegeticon)                     | <span data-ttu-id="2aedf-163">Permet à une application de récupérer une icône à afficher à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2aedf-163">Allows an application to retrieve an icon for display to the user.</span></span> <span data-ttu-id="2aedf-164">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2aedf-164">Synchronous.</span></span>                                                                                |
| [<span data-ttu-id="2aedf-165">**lineConfigDialog**</span><span class="sxs-lookup"><span data-stu-id="2aedf-165">**lineConfigDialog**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog)           | <span data-ttu-id="2aedf-166">Fait en sorte que le fournisseur du périphérique de ligne spécifié affiche une boîte de dialogue qui permet à l’utilisateur de configurer les paramètres liés au périphérique de ligne.</span><span class="sxs-lookup"><span data-stu-id="2aedf-166">Causes the provider of the specified line device to display a dialog box that allows the user to configure parameters related to the line device.</span></span> <span data-ttu-id="2aedf-167">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2aedf-167">Synchronous.</span></span> |
| [<span data-ttu-id="2aedf-168">**lineConfigDialogEdit**</span><span class="sxs-lookup"><span data-stu-id="2aedf-168">**lineConfigDialogEdit**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialogedit)   | <span data-ttu-id="2aedf-169">Affiche une boîte de dialogue qui permet à l’utilisateur de modifier les informations de configuration d’un périphérique en ligne.</span><span class="sxs-lookup"><span data-stu-id="2aedf-169">Displays a dialog box allowing the user to change configuration information for a line device.</span></span> <span data-ttu-id="2aedf-170">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2aedf-170">Synchronous.</span></span>                                                    |



 

## <a name="addresses"></a><span data-ttu-id="2aedf-171">Adresses</span><span class="sxs-lookup"><span data-stu-id="2aedf-171">Addresses</span></span>



| <span data-ttu-id="2aedf-172">Fonction</span><span class="sxs-lookup"><span data-stu-id="2aedf-172">Function</span></span>                                             | <span data-ttu-id="2aedf-173">Description</span><span class="sxs-lookup"><span data-stu-id="2aedf-173">Description</span></span>                                                                              |
|------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2aedf-174">**lineGetAddressCaps**</span><span class="sxs-lookup"><span data-stu-id="2aedf-174">**lineGetAddressCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)     | <span data-ttu-id="2aedf-175">Retourne les fonctions de téléphonie d’une adresse.</span><span class="sxs-lookup"><span data-stu-id="2aedf-175">Returns the telephony capabilities of an address.</span></span> <span data-ttu-id="2aedf-176">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2aedf-176">Synchronous.</span></span>                           |
| [<span data-ttu-id="2aedf-177">**lineGetAddressStatus**</span><span class="sxs-lookup"><span data-stu-id="2aedf-177">**lineGetAddressStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus) | <span data-ttu-id="2aedf-178">Retourne l’état actuel d’une adresse spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2aedf-178">Returns current status of a specified address.</span></span> <span data-ttu-id="2aedf-179">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2aedf-179">Synchronous.</span></span>                              |
| [<span data-ttu-id="2aedf-180">**lineGetAddressID**</span><span class="sxs-lookup"><span data-stu-id="2aedf-180">**lineGetAddressID**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetaddressid)         | <span data-ttu-id="2aedf-181">Récupère l’ID d’adresse d’une adresse spécifiée à l’aide d’un autre format.</span><span class="sxs-lookup"><span data-stu-id="2aedf-181">Retrieves the address ID of an address specified using an alternate format.</span></span> <span data-ttu-id="2aedf-182">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2aedf-182">Synchronous.</span></span> |



 

## <a name="opening-and-closing-line-devices"></a><span data-ttu-id="2aedf-183">Ouverture et fermeture des appareils en ligne</span><span class="sxs-lookup"><span data-stu-id="2aedf-183">Opening and Closing Line Devices</span></span>



| <span data-ttu-id="2aedf-184">Fonction</span><span class="sxs-lookup"><span data-stu-id="2aedf-184">Function</span></span>                       | <span data-ttu-id="2aedf-185">Description</span><span class="sxs-lookup"><span data-stu-id="2aedf-185">Description</span></span>                                                                                                |
|--------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2aedf-186">**lineOpen**</span><span class="sxs-lookup"><span data-stu-id="2aedf-186">**lineOpen**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineopen)   | <span data-ttu-id="2aedf-187">Ouvre un appareil de ligne spécifié pour fournir une surveillance et/ou un contrôle ultérieurs de la ligne.</span><span class="sxs-lookup"><span data-stu-id="2aedf-187">Opens a specified line device for providing subsequent monitoring and/or control of the line.</span></span> <span data-ttu-id="2aedf-188">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2aedf-188">Synchronous.</span></span> |
| [<span data-ttu-id="2aedf-189">**lineClose**</span><span class="sxs-lookup"><span data-stu-id="2aedf-189">**lineClose**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineclose) | <span data-ttu-id="2aedf-190">Ferme un appareil de ligne ouvert spécifié.</span><span class="sxs-lookup"><span data-stu-id="2aedf-190">Closes a specified opened line device.</span></span> <span data-ttu-id="2aedf-191">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2aedf-191">Synchronous.</span></span>                                                        |



 

## <a name="address-formats"></a><span data-ttu-id="2aedf-192">Formats d’adresse</span><span class="sxs-lookup"><span data-stu-id="2aedf-192">Address Formats</span></span>



| <span data-ttu-id="2aedf-193">Fonction</span><span class="sxs-lookup"><span data-stu-id="2aedf-193">Function</span></span>                                                 | <span data-ttu-id="2aedf-194">Description</span><span class="sxs-lookup"><span data-stu-id="2aedf-194">Description</span></span>                                                                                       |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2aedf-195">**lineTranslateAddress**</span><span class="sxs-lookup"><span data-stu-id="2aedf-195">**lineTranslateAddress**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress)     | <span data-ttu-id="2aedf-196">Traduit entre une adresse au format canonique et une adresse dans un format de numérotation.</span><span class="sxs-lookup"><span data-stu-id="2aedf-196">Translates between an address in canonical format and an address in dialable format.</span></span> <span data-ttu-id="2aedf-197">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2aedf-197">Synchronous.</span></span> |
| [<span data-ttu-id="2aedf-198">**lineSetCurrentLocation**</span><span class="sxs-lookup"><span data-stu-id="2aedf-198">**lineSetCurrentLocation**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetcurrentlocation) | <span data-ttu-id="2aedf-199">Définit l’emplacement utilisé comme contexte pour la traduction d’adresse.</span><span class="sxs-lookup"><span data-stu-id="2aedf-199">Sets the location used as the context for address translation.</span></span> <span data-ttu-id="2aedf-200">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2aedf-200">Synchronous.</span></span>                       |
| [<span data-ttu-id="2aedf-201">**lineSetTollList**</span><span class="sxs-lookup"><span data-stu-id="2aedf-201">**lineSetTollList**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesettolllist)               | <span data-ttu-id="2aedf-202">Manipule la liste de numéros de téléphone.</span><span class="sxs-lookup"><span data-stu-id="2aedf-202">Manipulates the toll list.</span></span> <span data-ttu-id="2aedf-203">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2aedf-203">Synchronous.</span></span>                                                           |
| [<span data-ttu-id="2aedf-204">**lineGetTranslateCaps**</span><span class="sxs-lookup"><span data-stu-id="2aedf-204">**lineGetTranslateCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)     | <span data-ttu-id="2aedf-205">Retourne les fonctionnalités de traduction d’adresses.</span><span class="sxs-lookup"><span data-stu-id="2aedf-205">Returns address translation capabilities.</span></span> <span data-ttu-id="2aedf-206">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2aedf-206">Synchronous.</span></span>                                            |



 

## <a name="call-states-and-events"></a><span data-ttu-id="2aedf-207">États d’appel et événements</span><span class="sxs-lookup"><span data-stu-id="2aedf-207">Call States and Events</span></span>



| <span data-ttu-id="2aedf-208">Fonction</span><span class="sxs-lookup"><span data-stu-id="2aedf-208">Function</span></span>                                         | <span data-ttu-id="2aedf-209">Description</span><span class="sxs-lookup"><span data-stu-id="2aedf-209">Description</span></span>                                                                         |
|--------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="2aedf-210">**lineGetCallInfo**</span><span class="sxs-lookup"><span data-stu-id="2aedf-210">**lineGetCallInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo)       | <span data-ttu-id="2aedf-211">Retourne des informations fixes sur un appel.</span><span class="sxs-lookup"><span data-stu-id="2aedf-211">Returns fixed information about a call.</span></span> <span data-ttu-id="2aedf-212">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2aedf-212">Synchronous.</span></span>                                |
| [<span data-ttu-id="2aedf-213">**lineGetCallStatus**</span><span class="sxs-lookup"><span data-stu-id="2aedf-213">**lineGetCallStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus)   | <span data-ttu-id="2aedf-214">Retourne les informations d’état de l’appel complet pour l’appel spécifié.</span><span class="sxs-lookup"><span data-stu-id="2aedf-214">Returns complete call status information for the specified call.</span></span> <span data-ttu-id="2aedf-215">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2aedf-215">Synchronous.</span></span>       |
| [<span data-ttu-id="2aedf-216">**lineSetAppSpecific**</span><span class="sxs-lookup"><span data-stu-id="2aedf-216">**lineSetAppSpecific**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetappspecific) | <span data-ttu-id="2aedf-217">Définit le champ propre à l’application de la structure d’informations d’un appel.</span><span class="sxs-lookup"><span data-stu-id="2aedf-217">Sets the application-specific field of a call's information structure.</span></span> <span data-ttu-id="2aedf-218">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2aedf-218">Synchronous.</span></span> |



 

## <a name="making-calls"></a><span data-ttu-id="2aedf-219">Appels effectués</span><span class="sxs-lookup"><span data-stu-id="2aedf-219">Making Calls</span></span>



| <span data-ttu-id="2aedf-220">Fonction</span><span class="sxs-lookup"><span data-stu-id="2aedf-220">Function</span></span>                             | <span data-ttu-id="2aedf-221">Description</span><span class="sxs-lookup"><span data-stu-id="2aedf-221">Description</span></span>                                                            |
|--------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="2aedf-222">**lineMakeCall**</span><span class="sxs-lookup"><span data-stu-id="2aedf-222">**lineMakeCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemakecall) | <span data-ttu-id="2aedf-223">Effectue un appel sortant et retourne un handle d’appel pour celui-ci.</span><span class="sxs-lookup"><span data-stu-id="2aedf-223">Makes an outbound call and returns a call handle for it.</span></span> <span data-ttu-id="2aedf-224">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="2aedf-224">Asynchronous.</span></span> |
| [<span data-ttu-id="2aedf-225">**lineDial**</span><span class="sxs-lookup"><span data-stu-id="2aedf-225">**lineDial**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedial)         | <span data-ttu-id="2aedf-226">Compose des adresses (parties d’une ou de plusieurs) adresses à distance.</span><span class="sxs-lookup"><span data-stu-id="2aedf-226">Dials (parts of one or more) dialable addresses.</span></span> <span data-ttu-id="2aedf-227">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="2aedf-227">Asynchronous.</span></span>         |



 

## <a name="answering-incoming-calls"></a><span data-ttu-id="2aedf-228">Réponse aux appels entrants</span><span class="sxs-lookup"><span data-stu-id="2aedf-228">Answering Incoming Calls</span></span>



| <span data-ttu-id="2aedf-229">Fonction</span><span class="sxs-lookup"><span data-stu-id="2aedf-229">Function</span></span>                         | <span data-ttu-id="2aedf-230">Description</span><span class="sxs-lookup"><span data-stu-id="2aedf-230">Description</span></span>                             |
|----------------------------------|-----------------------------------------|
| [<span data-ttu-id="2aedf-231">**lineAnswer**</span><span class="sxs-lookup"><span data-stu-id="2aedf-231">**lineAnswer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineanswer) | <span data-ttu-id="2aedf-232">Répond à un appel entrant.</span><span class="sxs-lookup"><span data-stu-id="2aedf-232">Answers an incoming call.</span></span> <span data-ttu-id="2aedf-233">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="2aedf-233">Asynchronous.</span></span> |



 

## <a name="toll-saver-support"></a><span data-ttu-id="2aedf-234">Prise en charge de péage Saver</span><span class="sxs-lookup"><span data-stu-id="2aedf-234">Toll Saver Support</span></span>



| <span data-ttu-id="2aedf-235">Fonction</span><span class="sxs-lookup"><span data-stu-id="2aedf-235">Function</span></span>                                   | <span data-ttu-id="2aedf-236">Description</span><span class="sxs-lookup"><span data-stu-id="2aedf-236">Description</span></span>                                                                                                 |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2aedf-237">**lineSetNumRings**</span><span class="sxs-lookup"><span data-stu-id="2aedf-237">**lineSetNumRings**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetnumrings) | <span data-ttu-id="2aedf-238">Indique le nombre d’anneaux après lesquels les appels entrants doivent être traités.</span><span class="sxs-lookup"><span data-stu-id="2aedf-238">Indicates the number of rings after which incoming calls are to be answered.</span></span> <span data-ttu-id="2aedf-239">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2aedf-239">Synchronous.</span></span>                   |
| [<span data-ttu-id="2aedf-240">**lineGetNumRings**</span><span class="sxs-lookup"><span data-stu-id="2aedf-240">**lineGetNumRings**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetnumrings) | <span data-ttu-id="2aedf-241">Retourne le nombre minimal d’anneaux demandés avec [**lineSetNumRings**](/windows/desktop/api/Tapi/nf-tapi-linesetnumrings).</span><span class="sxs-lookup"><span data-stu-id="2aedf-241">Returns the minimum number of rings requested with [**lineSetNumRings**](/windows/desktop/api/Tapi/nf-tapi-linesetnumrings).</span></span> <span data-ttu-id="2aedf-242">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2aedf-242">Synchronous.</span></span> |



 

## <a name="call-privilege-control"></a><span data-ttu-id="2aedf-243">Contrôle des privilèges d’appel</span><span class="sxs-lookup"><span data-stu-id="2aedf-243">Call Privilege Control</span></span>



| <span data-ttu-id="2aedf-244">Fonction</span><span class="sxs-lookup"><span data-stu-id="2aedf-244">Function</span></span>                                             | <span data-ttu-id="2aedf-245">Description</span><span class="sxs-lookup"><span data-stu-id="2aedf-245">Description</span></span>                                                               |
|------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="2aedf-246">**lineSetCallPrivilege**</span><span class="sxs-lookup"><span data-stu-id="2aedf-246">**lineSetCallPrivilege**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege) | <span data-ttu-id="2aedf-247">Définit le privilège de l’application sur le privilège spécifié.</span><span class="sxs-lookup"><span data-stu-id="2aedf-247">Sets the application's privilege to the privilege specified.</span></span> <span data-ttu-id="2aedf-248">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2aedf-248">Synchronous.</span></span> |



 

## <a name="call-drop-functions"></a><span data-ttu-id="2aedf-249">Appeler des fonctions Drop</span><span class="sxs-lookup"><span data-stu-id="2aedf-249">Call Drop Functions</span></span>



| <span data-ttu-id="2aedf-250">Fonction</span><span class="sxs-lookup"><span data-stu-id="2aedf-250">Function</span></span>                                         | <span data-ttu-id="2aedf-251">Description</span><span class="sxs-lookup"><span data-stu-id="2aedf-251">Description</span></span>                                                               |
|--------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="2aedf-252">**lineDrop**</span><span class="sxs-lookup"><span data-stu-id="2aedf-252">**lineDrop**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedrop)                     | <span data-ttu-id="2aedf-253">Déconnecte un appel ou abandonne une tentative d’appel en cours.</span><span class="sxs-lookup"><span data-stu-id="2aedf-253">Disconnects a call, or abandons a call attempt in progress.</span></span> <span data-ttu-id="2aedf-254">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="2aedf-254">Asynchronous.</span></span> |
| [<span data-ttu-id="2aedf-255">**lineDeallocateCall**</span><span class="sxs-lookup"><span data-stu-id="2aedf-255">**lineDeallocateCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) | <span data-ttu-id="2aedf-256">Libère le handle d’appel spécifié.</span><span class="sxs-lookup"><span data-stu-id="2aedf-256">Deallocates the specified call handle.</span></span> <span data-ttu-id="2aedf-257">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2aedf-257">Synchronous.</span></span>                       |



 

## <a name="call-handle-manipulation"></a><span data-ttu-id="2aedf-258">Appeler une manipulation de handle</span><span class="sxs-lookup"><span data-stu-id="2aedf-258">Call Handle Manipulation</span></span>



| <span data-ttu-id="2aedf-259">Fonction</span><span class="sxs-lookup"><span data-stu-id="2aedf-259">Function</span></span>                                                   | <span data-ttu-id="2aedf-260">Description</span><span class="sxs-lookup"><span data-stu-id="2aedf-260">Description</span></span>                                                                                                                    |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2aedf-261">**lineHandoff**</span><span class="sxs-lookup"><span data-stu-id="2aedf-261">**lineHandoff**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linehandoff)                         | <span data-ttu-id="2aedf-262">Transmet la propriété de l’appel et/ou modifie les privilèges d’une application en un appel.</span><span class="sxs-lookup"><span data-stu-id="2aedf-262">Hands off call ownership and/or changes an application's privileges to a call.</span></span> <span data-ttu-id="2aedf-263">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2aedf-263">Synchronous.</span></span>                                    |
| [<span data-ttu-id="2aedf-264">**lineGetNewCalls**</span><span class="sxs-lookup"><span data-stu-id="2aedf-264">**lineGetNewCalls**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls)                 | <span data-ttu-id="2aedf-265">Retourne des handles d’appel à des appels sur une ligne ou une adresse spécifiée pour laquelle l’application n’a pas encore de handles.</span><span class="sxs-lookup"><span data-stu-id="2aedf-265">Returns call handles to calls on a specified line or address for which the application does not yet have handles.</span></span> <span data-ttu-id="2aedf-266">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2aedf-266">Synchronous.</span></span> |
| [<span data-ttu-id="2aedf-267">**lineGetConfRelatedCalls**</span><span class="sxs-lookup"><span data-stu-id="2aedf-267">**lineGetConfRelatedCalls**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls) | <span data-ttu-id="2aedf-268">Retourne une liste de handles d’appel qui font partie du même appel de conférence que l’appel spécifié en tant que paramètre.</span><span class="sxs-lookup"><span data-stu-id="2aedf-268">Returns a list of call handles that are part of the same conference call as the call specified as a parameter.</span></span> <span data-ttu-id="2aedf-269">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2aedf-269">Synchronous.</span></span>    |



 

## <a name="location-and-countryregion-information"></a><span data-ttu-id="2aedf-270">Informations sur l’emplacement et le pays/la région</span><span class="sxs-lookup"><span data-stu-id="2aedf-270">Location and Country/Region Information</span></span>



| <span data-ttu-id="2aedf-271">Fonction</span><span class="sxs-lookup"><span data-stu-id="2aedf-271">Function</span></span>                                           | <span data-ttu-id="2aedf-272">Description</span><span class="sxs-lookup"><span data-stu-id="2aedf-272">Description</span></span>                                                                                           |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2aedf-273">**lineTranslateDialog**</span><span class="sxs-lookup"><span data-stu-id="2aedf-273">**lineTranslateDialog**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linetranslatedialog) | <span data-ttu-id="2aedf-274">Affiche une boîte de dialogue qui permet à l’utilisateur de modifier l’emplacement et d’appeler les informations de la carte.</span><span class="sxs-lookup"><span data-stu-id="2aedf-274">Displays a dialog box allowing the user to change location and calling card information.</span></span> <span data-ttu-id="2aedf-275">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2aedf-275">Synchronous.</span></span> |
| [<span data-ttu-id="2aedf-276">**lineGetCountry**</span><span class="sxs-lookup"><span data-stu-id="2aedf-276">**lineGetCountry**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetcountry)           | <span data-ttu-id="2aedf-277">Récupère des règles de numérotation et d’autres informations sur un pays/une région donné (e).</span><span class="sxs-lookup"><span data-stu-id="2aedf-277">Retrieves dialing rules and other information about a given country/region.</span></span> <span data-ttu-id="2aedf-278">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2aedf-278">Synchronous.</span></span>              |



 

## <a name="request-recipient-services"></a><span data-ttu-id="2aedf-279">Services de destinataire de la demande</span><span class="sxs-lookup"><span data-stu-id="2aedf-279">Request Recipient Services</span></span>

<span data-ttu-id="2aedf-280">Les deux fonctions suivantes sont utilisées uniquement pour la prise en charge de la téléphonie assistée.</span><span class="sxs-lookup"><span data-stu-id="2aedf-280">The following two functions are used only in support of Assisted Telephony.</span></span>



| <span data-ttu-id="2aedf-281">Fonction</span><span class="sxs-lookup"><span data-stu-id="2aedf-281">Function</span></span>                                                             | <span data-ttu-id="2aedf-282">Description</span><span class="sxs-lookup"><span data-stu-id="2aedf-282">Description</span></span>                                                                                                  |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2aedf-283">**lineRegisterRequestRecipient**</span><span class="sxs-lookup"><span data-stu-id="2aedf-283">**lineRegisterRequestRecipient**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineregisterrequestrecipient) | <span data-ttu-id="2aedf-284">Inscrit ou annule l’inscription de l’application en tant que destinataire de la demande pour le mode de demande spécifié.</span><span class="sxs-lookup"><span data-stu-id="2aedf-284">Registers or deregisters the application as a request recipient for the specified request mode.</span></span> <span data-ttu-id="2aedf-285">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2aedf-285">Synchronous.</span></span> |
| [<span data-ttu-id="2aedf-286">**lineGetRequest**</span><span class="sxs-lookup"><span data-stu-id="2aedf-286">**lineGetRequest**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetrequest)                             | <span data-ttu-id="2aedf-287">Obtient la requête suivante à partir de la bibliothèque de liens dynamiques de téléphonie.</span><span class="sxs-lookup"><span data-stu-id="2aedf-287">Gets the next request from the Telephony dynamic link library.</span></span> <span data-ttu-id="2aedf-288">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2aedf-288">Synchronous.</span></span>                                  |



 

 

 



