---
description: Tous les fournisseurs de services doivent implémenter les fonctions de téléphonie de base.
ms.assetid: 4250f3a0-a66a-4a6e-8566-d71be7463179
title: Fonctions de téléphonie de base TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6276be51482620af32650ad1625eea97bddb8e5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868598"
---
# <a name="tspi-basic-telephony-functions"></a><span data-ttu-id="c95cd-103">Fonctions de téléphonie de base TSPI</span><span class="sxs-lookup"><span data-stu-id="c95cd-103">TSPI Basic Telephony Functions</span></span>

<span data-ttu-id="c95cd-104">Tous les fournisseurs de services doivent implémenter les fonctions de téléphonie de base.</span><span class="sxs-lookup"><span data-stu-id="c95cd-104">All service providers must implement Basic Telephony functions.</span></span> <span data-ttu-id="c95cd-105">Voici une liste de ces fonctions par catégorie.</span><span class="sxs-lookup"><span data-stu-id="c95cd-105">The following is a list of such functions by category.</span></span> <span data-ttu-id="c95cd-106">Une fonction est identifiée comme *asynchrone* si elle indique la fin d’un message de réponse à l’application.</span><span class="sxs-lookup"><span data-stu-id="c95cd-106">A function is identified as *asynchronous* if it indicates completion in a REPLY message to the application.</span></span> <span data-ttu-id="c95cd-107">Si la fonction retourne toujours son résultat immédiatement, la fonction est considérée comme *synchrone*.</span><span class="sxs-lookup"><span data-stu-id="c95cd-107">If the function always returns its result immediately, the function is considered *synchronous*.</span></span>

-   [<span data-ttu-id="c95cd-108">Adresses</span><span class="sxs-lookup"><span data-stu-id="c95cd-108">Addresses</span></span>](#addresses)
-   [<span data-ttu-id="c95cd-109">Réponse aux appels entrants</span><span class="sxs-lookup"><span data-stu-id="c95cd-109">Answering Incoming Calls</span></span>](#answering-incoming-calls)
-   [<span data-ttu-id="c95cd-110">Appeler des fonctions Drop</span><span class="sxs-lookup"><span data-stu-id="c95cd-110">Call Drop Functions</span></span>](#call-drop-functions)
-   [<span data-ttu-id="c95cd-111">États d’appel et événements</span><span class="sxs-lookup"><span data-stu-id="c95cd-111">Call States and Events</span></span>](#call-states-and-events)
-   [<span data-ttu-id="c95cd-112">État de ligne et fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="c95cd-112">Line Status and Capabilities</span></span>](#line-status-and-capabilities)
-   [<span data-ttu-id="c95cd-113">Négociation de version de ligne</span><span class="sxs-lookup"><span data-stu-id="c95cd-113">Line Version Negotiation</span></span>](#line-version-negotiation)
-   [<span data-ttu-id="c95cd-114">Appels effectués</span><span class="sxs-lookup"><span data-stu-id="c95cd-114">Making Calls</span></span>](#making-calls)
-   [<span data-ttu-id="c95cd-115">Ouverture et fermeture des appareils en ligne</span><span class="sxs-lookup"><span data-stu-id="c95cd-115">Opening and Closing Line Devices</span></span>](#opening-and-closing-line-devices)
-   [<span data-ttu-id="c95cd-116">Négociation de version de téléphone</span><span class="sxs-lookup"><span data-stu-id="c95cd-116">Phone Version Negotiation</span></span>](#phone-version-negotiation)
-   [<span data-ttu-id="c95cd-117">Initialisation et arrêt du TSP</span><span class="sxs-lookup"><span data-stu-id="c95cd-117">TSP Initialization and Shutdown</span></span>](#tsp-initialization-and-shutdown)

## <a name="tsp-initialization-and-shutdown"></a><span data-ttu-id="c95cd-118">Initialisation et arrêt du TSP</span><span class="sxs-lookup"><span data-stu-id="c95cd-118">TSP Initialization and Shutdown</span></span>



|                                                           |                                                           |
|-----------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="c95cd-119">**TUISPI \_ providerInstall**</span><span class="sxs-lookup"><span data-stu-id="c95cd-119">**TUISPI\_providerInstall**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providerinstall) | <span data-ttu-id="c95cd-120">Installe un TSP.</span><span class="sxs-lookup"><span data-stu-id="c95cd-120">Installs a TSP.</span></span> <span data-ttu-id="c95cd-121">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="c95cd-121">Synchronous.</span></span>                              |
| [<span data-ttu-id="c95cd-122">**TSPI \_ providerInstall**</span><span class="sxs-lookup"><span data-stu-id="c95cd-122">**TSPI\_providerInstall**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerinstall)     | <span data-ttu-id="c95cd-123">Installe le TSP.</span><span class="sxs-lookup"><span data-stu-id="c95cd-123">Installs the TSP.</span></span> <span data-ttu-id="c95cd-124">Obsolète avec la version 2,0.</span><span class="sxs-lookup"><span data-stu-id="c95cd-124">Obsolete with Version 2.0.</span></span> <span data-ttu-id="c95cd-125">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="c95cd-125">Synchronous.</span></span> |
| [<span data-ttu-id="c95cd-126">**TSPI \_ providerInit**</span><span class="sxs-lookup"><span data-stu-id="c95cd-126">**TSPI\_providerInit**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerinit)           | <span data-ttu-id="c95cd-127">Initialise le TSP.</span><span class="sxs-lookup"><span data-stu-id="c95cd-127">Initializes the TSP.</span></span> <span data-ttu-id="c95cd-128">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="c95cd-128">Synchronous.</span></span>                         |
| [<span data-ttu-id="c95cd-129">**TSPI \_ providerShutdown**</span><span class="sxs-lookup"><span data-stu-id="c95cd-129">**TSPI\_providerShutdown**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providershutdown)   | <span data-ttu-id="c95cd-130">Arrête le fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="c95cd-130">Shuts down the service provider.</span></span>                          |
| [<span data-ttu-id="c95cd-131">**TUISPI \_ providerRemove**</span><span class="sxs-lookup"><span data-stu-id="c95cd-131">**TUISPI\_providerRemove**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providerremove)   | <span data-ttu-id="c95cd-132">Supprime un TSP.</span><span class="sxs-lookup"><span data-stu-id="c95cd-132">Removes a TSP.</span></span> <span data-ttu-id="c95cd-133">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="c95cd-133">Synchronous.</span></span>                               |
| [<span data-ttu-id="c95cd-134">**TSPI \_ providerRemove**</span><span class="sxs-lookup"><span data-stu-id="c95cd-134">**TSPI\_providerRemove**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerremove)       | <span data-ttu-id="c95cd-135">Supprime un TSP.</span><span class="sxs-lookup"><span data-stu-id="c95cd-135">Removes a TSP.</span></span> <span data-ttu-id="c95cd-136">Obsolète avec la version 2,0.</span><span class="sxs-lookup"><span data-stu-id="c95cd-136">Obsolete with Version 2.0.</span></span> <span data-ttu-id="c95cd-137">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="c95cd-137">Synchronous.</span></span>    |



 

## <a name="phone-version-negotiation"></a><span data-ttu-id="c95cd-138">Négociation de version de téléphone</span><span class="sxs-lookup"><span data-stu-id="c95cd-138">Phone Version Negotiation</span></span>



|                                                                           |                                                                                         |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="c95cd-139">**TSPI \_ phoneNegotiateTSPIVersion**</span><span class="sxs-lookup"><span data-stu-id="c95cd-139">**TSPI\_phoneNegotiateTSPIVersion**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiatetspiversion) | <span data-ttu-id="c95cd-140">Retourne la version SPI la plus élevée que le fournisseur de services peut utiliser pour cet appareil.</span><span class="sxs-lookup"><span data-stu-id="c95cd-140">Returns the highest SPI version the service provider can operate under for this device.</span></span> |



 

## <a name="line-version-negotiation"></a><span data-ttu-id="c95cd-141">Négociation de version de ligne</span><span class="sxs-lookup"><span data-stu-id="c95cd-141">Line Version Negotiation</span></span>



|                                                                         |                                                                                                 |
|-------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c95cd-142">**TSPI \_ lineNegotiateTSPIVersion**</span><span class="sxs-lookup"><span data-stu-id="c95cd-142">**TSPI\_lineNegotiateTSPIVersion**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) | <span data-ttu-id="c95cd-143">Permet à une application de négocier une version de TSPI à utiliser avec un périphérique de ligne donné.</span><span class="sxs-lookup"><span data-stu-id="c95cd-143">Allows an application to negotiate a TSPI version to use with a given line device.</span></span> <span data-ttu-id="c95cd-144">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="c95cd-144">Synchronous.</span></span> |



 

## <a name="line-status-and-capabilities"></a><span data-ttu-id="c95cd-145">État de ligne et fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="c95cd-145">Line Status and Capabilities</span></span>



|                                                                     |                                                                                                                                                                |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c95cd-146">**TSPI \_ lineGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="c95cd-146">**TSPI\_lineGetDevCaps**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps)                 | <span data-ttu-id="c95cd-147">Retourne les fonctionnalités d’un périphérique de ligne donné.</span><span class="sxs-lookup"><span data-stu-id="c95cd-147">Returns the capabilities of a given line device.</span></span> <span data-ttu-id="c95cd-148">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="c95cd-148">Synchronous.</span></span>                                                                                                  |
| [<span data-ttu-id="c95cd-149">**TSPI \_ lineGetDevConfig**</span><span class="sxs-lookup"><span data-stu-id="c95cd-149">**TSPI\_lineGetDevConfig**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevconfig)             | <span data-ttu-id="c95cd-150">Retourne la configuration d’un périphérique de flux multimédia.</span><span class="sxs-lookup"><span data-stu-id="c95cd-150">Returns configuration of a media stream device.</span></span> <span data-ttu-id="c95cd-151">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="c95cd-151">Synchronous.</span></span>                                                                                                   |
| [<span data-ttu-id="c95cd-152">**TSPI \_ lineGetLineDevStatus**</span><span class="sxs-lookup"><span data-stu-id="c95cd-152">**TSPI\_lineGetLineDevStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetlinedevstatus)     | <span data-ttu-id="c95cd-153">Retourne l’état actuel du périphérique en ligne ouvert spécifié.</span><span class="sxs-lookup"><span data-stu-id="c95cd-153">Returns current status of the specified open line device.</span></span> <span data-ttu-id="c95cd-154">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="c95cd-154">Synchronous.</span></span>                                                                                         |
| [<span data-ttu-id="c95cd-155">**TSPI \_ lineSetDevConfig**</span><span class="sxs-lookup"><span data-stu-id="c95cd-155">**TSPI\_lineSetDevConfig**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetdevconfig)             | <span data-ttu-id="c95cd-156">Définit la configuration du périphérique de flux multimédia spécifié.</span><span class="sxs-lookup"><span data-stu-id="c95cd-156">Sets the configuration of the specified media stream device.</span></span> <span data-ttu-id="c95cd-157">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="c95cd-157">Synchronous.</span></span>                                                                                      |
| [<span data-ttu-id="c95cd-158">**TSPI \_ lineSetStatusMessages**</span><span class="sxs-lookup"><span data-stu-id="c95cd-158">**TSPI\_lineSetStatusMessages**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages)   | <span data-ttu-id="c95cd-159">Spécifie les modifications d’État pour lesquelles l’application doit être notifiée.</span><span class="sxs-lookup"><span data-stu-id="c95cd-159">Specifies the status changes for which the application needs to be notified.</span></span> <span data-ttu-id="c95cd-160">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="c95cd-160">Synchronous.</span></span>                                                                      |
| [<span data-ttu-id="c95cd-161">**TSPI \_ lineGetID**</span><span class="sxs-lookup"><span data-stu-id="c95cd-161">**TSPI\_lineGetID**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetid)                           | <span data-ttu-id="c95cd-162">Récupère un ID d’appareil associé à l’ouverture de ligne, à l’adresse ou à l’appel spécifié.</span><span class="sxs-lookup"><span data-stu-id="c95cd-162">Retrieves a device ID associated with the specified open line, address, or call.</span></span> <span data-ttu-id="c95cd-163">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="c95cd-163">Synchronous.</span></span>                                                                  |
| [<span data-ttu-id="c95cd-164">**TSPI \_ lineGetIcon**</span><span class="sxs-lookup"><span data-stu-id="c95cd-164">**TSPI\_lineGetIcon**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegeticon)                       | <span data-ttu-id="c95cd-165">Permet à une application de récupérer une icône à afficher à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c95cd-165">Allows an application to retrieve an icon for display to the user.</span></span> <span data-ttu-id="c95cd-166">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="c95cd-166">Synchronous.</span></span>                                                                                |
| [<span data-ttu-id="c95cd-167">**TUISPI \_ lineConfigDialog**</span><span class="sxs-lookup"><span data-stu-id="c95cd-167">**TUISPI\_lineConfigDialog**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog)         | <span data-ttu-id="c95cd-168">Fait en sorte que le fournisseur du périphérique de ligne spécifié affiche une boîte de dialogue qui permet à l’utilisateur de configurer les paramètres liés au périphérique de ligne.</span><span class="sxs-lookup"><span data-stu-id="c95cd-168">Causes the provider of the specified line device to display a dialog box that allows the user to configure parameters related to the line device.</span></span> <span data-ttu-id="c95cd-169">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="c95cd-169">Synchronous.</span></span> |
| [<span data-ttu-id="c95cd-170">**TUISPI \_ lineConfigDialogEdit**</span><span class="sxs-lookup"><span data-stu-id="c95cd-170">**TUISPI\_lineConfigDialogEdit**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialogedit) | <span data-ttu-id="c95cd-171">Affiche une boîte de dialogue qui permet à l’utilisateur de modifier les informations de configuration d’un périphérique en ligne.</span><span class="sxs-lookup"><span data-stu-id="c95cd-171">Displays a dialog box allowing the user to change configuration information for a line device.</span></span> <span data-ttu-id="c95cd-172">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="c95cd-172">Synchronous.</span></span>                                                    |



 

## <a name="addresses"></a><span data-ttu-id="c95cd-173">Adresses</span><span class="sxs-lookup"><span data-stu-id="c95cd-173">Addresses</span></span>



|                                                                 |                                                                                          |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c95cd-174">**TSPI \_ lineGetAddressCaps**</span><span class="sxs-lookup"><span data-stu-id="c95cd-174">**TSPI\_lineGetAddressCaps**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps)     | <span data-ttu-id="c95cd-175">Retourne les fonctions de téléphonie d’une adresse.</span><span class="sxs-lookup"><span data-stu-id="c95cd-175">Returns the telephony capabilities of an address.</span></span> <span data-ttu-id="c95cd-176">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="c95cd-176">Synchronous.</span></span>                           |
| [<span data-ttu-id="c95cd-177">**TSPI \_ lineGetAddressStatus**</span><span class="sxs-lookup"><span data-stu-id="c95cd-177">**TSPI\_lineGetAddressStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressstatus) | <span data-ttu-id="c95cd-178">Retourne l’état actuel d’une adresse spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c95cd-178">Returns current status of a specified address.</span></span> <span data-ttu-id="c95cd-179">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="c95cd-179">Synchronous.</span></span>                              |
| [<span data-ttu-id="c95cd-180">**TSPI \_ lineGetNumAddressIDs**</span><span class="sxs-lookup"><span data-stu-id="c95cd-180">**TSPI\_lineGetNumAddressIDs**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetnumaddressids) | <span data-ttu-id="c95cd-181">Récupère le nombre d’identificateurs d’adresse pris en charge sur la ligne indiquée.</span><span class="sxs-lookup"><span data-stu-id="c95cd-181">Retrieves the number of address identifiers supported on the indicated line.</span></span>             |
| [<span data-ttu-id="c95cd-182">**TSPI \_ lineGetAddressID**</span><span class="sxs-lookup"><span data-stu-id="c95cd-182">**TSPI\_lineGetAddressID**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressid)         | <span data-ttu-id="c95cd-183">Récupère l’ID d’adresse d’une adresse spécifiée à l’aide d’un autre format.</span><span class="sxs-lookup"><span data-stu-id="c95cd-183">Retrieves the address ID of an address specified using an alternate format.</span></span> <span data-ttu-id="c95cd-184">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="c95cd-184">Synchronous.</span></span> |



 

## <a name="opening-and-closing-line-devices"></a><span data-ttu-id="c95cd-185">Ouverture et fermeture des appareils en ligne</span><span class="sxs-lookup"><span data-stu-id="c95cd-185">Opening and Closing Line Devices</span></span>



|                                           |                                                                                                            |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c95cd-186">**TSPI \_ lineOpen**</span><span class="sxs-lookup"><span data-stu-id="c95cd-186">**TSPI\_lineOpen**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineopen)   | <span data-ttu-id="c95cd-187">Ouvre un appareil de ligne spécifié pour fournir une surveillance et/ou un contrôle ultérieurs de la ligne.</span><span class="sxs-lookup"><span data-stu-id="c95cd-187">Opens a specified line device for providing subsequent monitoring and/or control of the line.</span></span> <span data-ttu-id="c95cd-188">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="c95cd-188">Synchronous.</span></span> |
| [<span data-ttu-id="c95cd-189">**TSPI \_ lineClose**</span><span class="sxs-lookup"><span data-stu-id="c95cd-189">**TSPI\_lineClose**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineclose) | <span data-ttu-id="c95cd-190">Ferme un appareil de ligne ouvert spécifié.</span><span class="sxs-lookup"><span data-stu-id="c95cd-190">Closes a specified opened line device.</span></span> <span data-ttu-id="c95cd-191">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="c95cd-191">Synchronous.</span></span>                                                        |



 

## <a name="call-states-and-events"></a><span data-ttu-id="c95cd-192">États d’appel et événements</span><span class="sxs-lookup"><span data-stu-id="c95cd-192">Call States and Events</span></span>



|                                                             |                                                                                     |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="c95cd-193">**TSPI \_ lineGetCallInfo**</span><span class="sxs-lookup"><span data-stu-id="c95cd-193">**TSPI\_lineGetCallInfo**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallinfo)       | <span data-ttu-id="c95cd-194">Retourne des informations fixes sur un appel.</span><span class="sxs-lookup"><span data-stu-id="c95cd-194">Returns fixed information about a call.</span></span> <span data-ttu-id="c95cd-195">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="c95cd-195">Synchronous.</span></span>                                |
| [<span data-ttu-id="c95cd-196">**TSPI \_ lineGetCallStatus**</span><span class="sxs-lookup"><span data-stu-id="c95cd-196">**TSPI\_lineGetCallStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallstatus)   | <span data-ttu-id="c95cd-197">Retourne les informations d’état de l’appel complet pour l’appel spécifié.</span><span class="sxs-lookup"><span data-stu-id="c95cd-197">Returns complete call status information for the specified call.</span></span> <span data-ttu-id="c95cd-198">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="c95cd-198">Synchronous.</span></span>       |
| [<span data-ttu-id="c95cd-199">**TSPI \_ lineSetAppSpecific**</span><span class="sxs-lookup"><span data-stu-id="c95cd-199">**TSPI\_lineSetAppSpecific**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetappspecific) | <span data-ttu-id="c95cd-200">Définit le champ propre à l’application de la structure d’informations d’un appel.</span><span class="sxs-lookup"><span data-stu-id="c95cd-200">Sets the application-specific field of a call's information structure.</span></span> <span data-ttu-id="c95cd-201">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="c95cd-201">Synchronous.</span></span> |



 

## <a name="making-calls"></a><span data-ttu-id="c95cd-202">Appels effectués</span><span class="sxs-lookup"><span data-stu-id="c95cd-202">Making Calls</span></span>



|                                                 |                                                                        |
|-------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="c95cd-203">**TSPI \_ lineMakeCall**</span><span class="sxs-lookup"><span data-stu-id="c95cd-203">**TSPI\_lineMakeCall**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall) | <span data-ttu-id="c95cd-204">Effectue un appel sortant et retourne un handle d’appel pour celui-ci.</span><span class="sxs-lookup"><span data-stu-id="c95cd-204">Makes an outbound call and returns a call handle for it.</span></span> <span data-ttu-id="c95cd-205">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="c95cd-205">Asynchronous.</span></span> |
| [<span data-ttu-id="c95cd-206">**TSPI \_ lineDial**</span><span class="sxs-lookup"><span data-stu-id="c95cd-206">**TSPI\_lineDial**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linedial)         | <span data-ttu-id="c95cd-207">Compose des adresses (parties d’une ou de plusieurs) adresses à distance.</span><span class="sxs-lookup"><span data-stu-id="c95cd-207">Dials (parts of one or more) dialable addresses.</span></span> <span data-ttu-id="c95cd-208">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="c95cd-208">Asynchronous.</span></span>         |



 

## <a name="answering-incoming-calls"></a><span data-ttu-id="c95cd-209">Réponse aux appels entrants</span><span class="sxs-lookup"><span data-stu-id="c95cd-209">Answering Incoming Calls</span></span>



|                                             |                                         |
|---------------------------------------------|-----------------------------------------|
| [<span data-ttu-id="c95cd-210">**TSPI \_ lineAnswer**</span><span class="sxs-lookup"><span data-stu-id="c95cd-210">**TSPI\_lineAnswer**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineanswer) | <span data-ttu-id="c95cd-211">Répond à un appel entrant.</span><span class="sxs-lookup"><span data-stu-id="c95cd-211">Answers an incoming call.</span></span> <span data-ttu-id="c95cd-212">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="c95cd-212">Asynchronous.</span></span> |



 

## <a name="call-drop-functions"></a><span data-ttu-id="c95cd-213">Appeler des fonctions Drop</span><span class="sxs-lookup"><span data-stu-id="c95cd-213">Call Drop Functions</span></span>



|                                         |                                                                           |
|-----------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="c95cd-214">**TSPI \_ lineDrop**</span><span class="sxs-lookup"><span data-stu-id="c95cd-214">**TSPI\_lineDrop**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) | <span data-ttu-id="c95cd-215">Déconnecte un appel ou abandonne une tentative d’appel en cours.</span><span class="sxs-lookup"><span data-stu-id="c95cd-215">Disconnects a call, or abandons a call attempt in progress.</span></span> <span data-ttu-id="c95cd-216">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="c95cd-216">Asynchronous.</span></span> |



 

 

 
