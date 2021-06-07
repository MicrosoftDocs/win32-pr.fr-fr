---
description: Tous les fournisseurs de services doivent implémenter les fonctions de téléphonie de base.
ms.assetid: 4250f3a0-a66a-4a6e-8566-d71be7463179
title: Fonctions de téléphonie de base TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5308def0c94df9fa59f2022bf25c4dbb1843e2f8
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524153"
---
# <a name="tspi-basic-telephony-functions"></a><span data-ttu-id="2c110-103">Fonctions de téléphonie de base TSPI</span><span class="sxs-lookup"><span data-stu-id="2c110-103">TSPI Basic Telephony Functions</span></span>

<span data-ttu-id="2c110-104">Tous les fournisseurs de services doivent implémenter les fonctions de téléphonie de base.</span><span class="sxs-lookup"><span data-stu-id="2c110-104">All service providers must implement Basic Telephony functions.</span></span> <span data-ttu-id="2c110-105">Voici une liste de ces fonctions par catégorie.</span><span class="sxs-lookup"><span data-stu-id="2c110-105">The following is a list of such functions by category.</span></span> <span data-ttu-id="2c110-106">Une fonction est identifiée comme *asynchrone* si elle indique la fin d’un message de réponse à l’application.</span><span class="sxs-lookup"><span data-stu-id="2c110-106">A function is identified as *asynchronous* if it indicates completion in a REPLY message to the application.</span></span> <span data-ttu-id="2c110-107">Si la fonction retourne toujours son résultat immédiatement, la fonction est considérée comme *synchrone*.</span><span class="sxs-lookup"><span data-stu-id="2c110-107">If the function always returns its result immediately, the function is considered *synchronous*.</span></span>

-   [<span data-ttu-id="2c110-108">Adresses</span><span class="sxs-lookup"><span data-stu-id="2c110-108">Addresses</span></span>](#addresses)
-   [<span data-ttu-id="2c110-109">Réponse aux appels entrants</span><span class="sxs-lookup"><span data-stu-id="2c110-109">Answering Incoming Calls</span></span>](#answering-incoming-calls)
-   [<span data-ttu-id="2c110-110">Appeler des fonctions Drop</span><span class="sxs-lookup"><span data-stu-id="2c110-110">Call Drop Functions</span></span>](#call-drop-functions)
-   [<span data-ttu-id="2c110-111">États d’appel et événements</span><span class="sxs-lookup"><span data-stu-id="2c110-111">Call States and Events</span></span>](#call-states-and-events)
-   [<span data-ttu-id="2c110-112">État de ligne et fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="2c110-112">Line Status and Capabilities</span></span>](#line-status-and-capabilities)
-   [<span data-ttu-id="2c110-113">Négociation de version de ligne</span><span class="sxs-lookup"><span data-stu-id="2c110-113">Line Version Negotiation</span></span>](#line-version-negotiation)
-   [<span data-ttu-id="2c110-114">Appels effectués</span><span class="sxs-lookup"><span data-stu-id="2c110-114">Making Calls</span></span>](#making-calls)
-   [<span data-ttu-id="2c110-115">Ouverture et fermeture des appareils en ligne</span><span class="sxs-lookup"><span data-stu-id="2c110-115">Opening and Closing Line Devices</span></span>](#opening-and-closing-line-devices)
-   [<span data-ttu-id="2c110-116">Négociation de version de téléphone</span><span class="sxs-lookup"><span data-stu-id="2c110-116">Phone Version Negotiation</span></span>](#phone-version-negotiation)
-   [<span data-ttu-id="2c110-117">Initialisation et arrêt du TSP</span><span class="sxs-lookup"><span data-stu-id="2c110-117">TSP Initialization and Shutdown</span></span>](#tsp-initialization-and-shutdown)

## <a name="tsp-initialization-and-shutdown"></a><span data-ttu-id="2c110-118">Initialisation et arrêt du TSP</span><span class="sxs-lookup"><span data-stu-id="2c110-118">TSP Initialization and Shutdown</span></span>



|  <span data-ttu-id="2c110-119">Fonction</span><span class="sxs-lookup"><span data-stu-id="2c110-119">Function</span></span>                                                         |   <span data-ttu-id="2c110-120">Description</span><span class="sxs-lookup"><span data-stu-id="2c110-120">Description</span></span>                                                        |
|-----------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="2c110-121">**TUISPI \_ providerInstall**</span><span class="sxs-lookup"><span data-stu-id="2c110-121">**TUISPI\_providerInstall**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providerinstall) | <span data-ttu-id="2c110-122">Installe un TSP.</span><span class="sxs-lookup"><span data-stu-id="2c110-122">Installs a TSP.</span></span> <span data-ttu-id="2c110-123">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2c110-123">Synchronous.</span></span>                              |
| [<span data-ttu-id="2c110-124">**TSPI \_ providerInstall**</span><span class="sxs-lookup"><span data-stu-id="2c110-124">**TSPI\_providerInstall**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerinstall)     | <span data-ttu-id="2c110-125">Installe le TSP.</span><span class="sxs-lookup"><span data-stu-id="2c110-125">Installs the TSP.</span></span> <span data-ttu-id="2c110-126">Obsolète avec la version 2,0.</span><span class="sxs-lookup"><span data-stu-id="2c110-126">Obsolete with Version 2.0.</span></span> <span data-ttu-id="2c110-127">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2c110-127">Synchronous.</span></span> |
| [<span data-ttu-id="2c110-128">**TSPI \_ providerInit**</span><span class="sxs-lookup"><span data-stu-id="2c110-128">**TSPI\_providerInit**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerinit)           | <span data-ttu-id="2c110-129">Initialise le TSP.</span><span class="sxs-lookup"><span data-stu-id="2c110-129">Initializes the TSP.</span></span> <span data-ttu-id="2c110-130">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2c110-130">Synchronous.</span></span>                         |
| [<span data-ttu-id="2c110-131">**TSPI \_ providerShutdown**</span><span class="sxs-lookup"><span data-stu-id="2c110-131">**TSPI\_providerShutdown**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providershutdown)   | <span data-ttu-id="2c110-132">Arrête le fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="2c110-132">Shuts down the service provider.</span></span>                          |
| [<span data-ttu-id="2c110-133">**TUISPI \_ providerRemove**</span><span class="sxs-lookup"><span data-stu-id="2c110-133">**TUISPI\_providerRemove**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providerremove)   | <span data-ttu-id="2c110-134">Supprime un TSP.</span><span class="sxs-lookup"><span data-stu-id="2c110-134">Removes a TSP.</span></span> <span data-ttu-id="2c110-135">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2c110-135">Synchronous.</span></span>                               |
| [<span data-ttu-id="2c110-136">**TSPI \_ providerRemove**</span><span class="sxs-lookup"><span data-stu-id="2c110-136">**TSPI\_providerRemove**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerremove)       | <span data-ttu-id="2c110-137">Supprime un TSP.</span><span class="sxs-lookup"><span data-stu-id="2c110-137">Removes a TSP.</span></span> <span data-ttu-id="2c110-138">Obsolète avec la version 2,0.</span><span class="sxs-lookup"><span data-stu-id="2c110-138">Obsolete with Version 2.0.</span></span> <span data-ttu-id="2c110-139">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2c110-139">Synchronous.</span></span>    |



 

## <a name="phone-version-negotiation"></a><span data-ttu-id="2c110-140">Négociation de version de téléphone</span><span class="sxs-lookup"><span data-stu-id="2c110-140">Phone Version Negotiation</span></span>



|  <span data-ttu-id="2c110-141">Fonction</span><span class="sxs-lookup"><span data-stu-id="2c110-141">Function</span></span>                                                         |   <span data-ttu-id="2c110-142">Description</span><span class="sxs-lookup"><span data-stu-id="2c110-142">Description</span></span>                                                        |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="2c110-143">**TSPI \_ phoneNegotiateTSPIVersion**</span><span class="sxs-lookup"><span data-stu-id="2c110-143">**TSPI\_phoneNegotiateTSPIVersion**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiatetspiversion) | <span data-ttu-id="2c110-144">Retourne la version SPI la plus élevée que le fournisseur de services peut utiliser pour cet appareil.</span><span class="sxs-lookup"><span data-stu-id="2c110-144">Returns the highest SPI version the service provider can operate under for this device.</span></span> |



 

## <a name="line-version-negotiation"></a><span data-ttu-id="2c110-145">Négociation de version de ligne</span><span class="sxs-lookup"><span data-stu-id="2c110-145">Line Version Negotiation</span></span>



|  <span data-ttu-id="2c110-146">Fonction</span><span class="sxs-lookup"><span data-stu-id="2c110-146">Function</span></span>                                                         |   <span data-ttu-id="2c110-147">Description</span><span class="sxs-lookup"><span data-stu-id="2c110-147">Description</span></span>                                                        |
|-------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2c110-148">**TSPI \_ lineNegotiateTSPIVersion**</span><span class="sxs-lookup"><span data-stu-id="2c110-148">**TSPI\_lineNegotiateTSPIVersion**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) | <span data-ttu-id="2c110-149">Permet à une application de négocier une version de TSPI à utiliser avec un périphérique de ligne donné.</span><span class="sxs-lookup"><span data-stu-id="2c110-149">Allows an application to negotiate a TSPI version to use with a given line device.</span></span> <span data-ttu-id="2c110-150">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2c110-150">Synchronous.</span></span> |



 

## <a name="line-status-and-capabilities"></a><span data-ttu-id="2c110-151">État de ligne et fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="2c110-151">Line Status and Capabilities</span></span>



|  <span data-ttu-id="2c110-152">Fonction</span><span class="sxs-lookup"><span data-stu-id="2c110-152">Function</span></span>                                                         |   <span data-ttu-id="2c110-153">Description</span><span class="sxs-lookup"><span data-stu-id="2c110-153">Description</span></span>                                                        |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2c110-154">**TSPI \_ lineGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="2c110-154">**TSPI\_lineGetDevCaps**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps)                 | <span data-ttu-id="2c110-155">Retourne les fonctionnalités d’un périphérique de ligne donné.</span><span class="sxs-lookup"><span data-stu-id="2c110-155">Returns the capabilities of a given line device.</span></span> <span data-ttu-id="2c110-156">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2c110-156">Synchronous.</span></span>                                                                                                  |
| [<span data-ttu-id="2c110-157">**TSPI \_ lineGetDevConfig**</span><span class="sxs-lookup"><span data-stu-id="2c110-157">**TSPI\_lineGetDevConfig**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevconfig)             | <span data-ttu-id="2c110-158">Retourne la configuration d’un périphérique de flux multimédia.</span><span class="sxs-lookup"><span data-stu-id="2c110-158">Returns configuration of a media stream device.</span></span> <span data-ttu-id="2c110-159">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2c110-159">Synchronous.</span></span>                                                                                                   |
| [<span data-ttu-id="2c110-160">**TSPI \_ lineGetLineDevStatus**</span><span class="sxs-lookup"><span data-stu-id="2c110-160">**TSPI\_lineGetLineDevStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetlinedevstatus)     | <span data-ttu-id="2c110-161">Retourne l’état actuel du périphérique en ligne ouvert spécifié.</span><span class="sxs-lookup"><span data-stu-id="2c110-161">Returns current status of the specified open line device.</span></span> <span data-ttu-id="2c110-162">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2c110-162">Synchronous.</span></span>                                                                                         |
| [<span data-ttu-id="2c110-163">**TSPI \_ lineSetDevConfig**</span><span class="sxs-lookup"><span data-stu-id="2c110-163">**TSPI\_lineSetDevConfig**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetdevconfig)             | <span data-ttu-id="2c110-164">Définit la configuration du périphérique de flux multimédia spécifié.</span><span class="sxs-lookup"><span data-stu-id="2c110-164">Sets the configuration of the specified media stream device.</span></span> <span data-ttu-id="2c110-165">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2c110-165">Synchronous.</span></span>                                                                                      |
| [<span data-ttu-id="2c110-166">**TSPI \_ lineSetStatusMessages**</span><span class="sxs-lookup"><span data-stu-id="2c110-166">**TSPI\_lineSetStatusMessages**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages)   | <span data-ttu-id="2c110-167">Spécifie les modifications d’État pour lesquelles l’application doit être notifiée.</span><span class="sxs-lookup"><span data-stu-id="2c110-167">Specifies the status changes for which the application needs to be notified.</span></span> <span data-ttu-id="2c110-168">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2c110-168">Synchronous.</span></span>                                                                      |
| [<span data-ttu-id="2c110-169">**TSPI \_ lineGetID**</span><span class="sxs-lookup"><span data-stu-id="2c110-169">**TSPI\_lineGetID**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetid)                           | <span data-ttu-id="2c110-170">Récupère un ID d’appareil associé à l’ouverture de ligne, à l’adresse ou à l’appel spécifié.</span><span class="sxs-lookup"><span data-stu-id="2c110-170">Retrieves a device ID associated with the specified open line, address, or call.</span></span> <span data-ttu-id="2c110-171">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2c110-171">Synchronous.</span></span>                                                                  |
| [<span data-ttu-id="2c110-172">**TSPI \_ lineGetIcon**</span><span class="sxs-lookup"><span data-stu-id="2c110-172">**TSPI\_lineGetIcon**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegeticon)                       | <span data-ttu-id="2c110-173">Permet à une application de récupérer une icône à afficher à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2c110-173">Allows an application to retrieve an icon for display to the user.</span></span> <span data-ttu-id="2c110-174">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2c110-174">Synchronous.</span></span>                                                                                |
| [<span data-ttu-id="2c110-175">**TUISPI \_ lineConfigDialog**</span><span class="sxs-lookup"><span data-stu-id="2c110-175">**TUISPI\_lineConfigDialog**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog)         | <span data-ttu-id="2c110-176">Fait en sorte que le fournisseur du périphérique de ligne spécifié affiche une boîte de dialogue qui permet à l’utilisateur de configurer les paramètres liés au périphérique de ligne.</span><span class="sxs-lookup"><span data-stu-id="2c110-176">Causes the provider of the specified line device to display a dialog box that allows the user to configure parameters related to the line device.</span></span> <span data-ttu-id="2c110-177">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2c110-177">Synchronous.</span></span> |
| [<span data-ttu-id="2c110-178">**TUISPI \_ lineConfigDialogEdit**</span><span class="sxs-lookup"><span data-stu-id="2c110-178">**TUISPI\_lineConfigDialogEdit**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialogedit) | <span data-ttu-id="2c110-179">Affiche une boîte de dialogue qui permet à l’utilisateur de modifier les informations de configuration d’un périphérique en ligne.</span><span class="sxs-lookup"><span data-stu-id="2c110-179">Displays a dialog box allowing the user to change configuration information for a line device.</span></span> <span data-ttu-id="2c110-180">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2c110-180">Synchronous.</span></span>                                                    |



 

## <a name="addresses"></a><span data-ttu-id="2c110-181">Adresses</span><span class="sxs-lookup"><span data-stu-id="2c110-181">Addresses</span></span>



|  <span data-ttu-id="2c110-182">Fonction</span><span class="sxs-lookup"><span data-stu-id="2c110-182">Function</span></span>                                                         |   <span data-ttu-id="2c110-183">Description</span><span class="sxs-lookup"><span data-stu-id="2c110-183">Description</span></span>                                                        |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2c110-184">**TSPI \_ lineGetAddressCaps**</span><span class="sxs-lookup"><span data-stu-id="2c110-184">**TSPI\_lineGetAddressCaps**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps)     | <span data-ttu-id="2c110-185">Retourne les fonctions de téléphonie d’une adresse.</span><span class="sxs-lookup"><span data-stu-id="2c110-185">Returns the telephony capabilities of an address.</span></span> <span data-ttu-id="2c110-186">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2c110-186">Synchronous.</span></span>                           |
| [<span data-ttu-id="2c110-187">**TSPI \_ lineGetAddressStatus**</span><span class="sxs-lookup"><span data-stu-id="2c110-187">**TSPI\_lineGetAddressStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressstatus) | <span data-ttu-id="2c110-188">Retourne l’état actuel d’une adresse spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2c110-188">Returns current status of a specified address.</span></span> <span data-ttu-id="2c110-189">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2c110-189">Synchronous.</span></span>                              |
| [<span data-ttu-id="2c110-190">**TSPI \_ lineGetNumAddressIDs**</span><span class="sxs-lookup"><span data-stu-id="2c110-190">**TSPI\_lineGetNumAddressIDs**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetnumaddressids) | <span data-ttu-id="2c110-191">Récupère le nombre d’identificateurs d’adresse pris en charge sur la ligne indiquée.</span><span class="sxs-lookup"><span data-stu-id="2c110-191">Retrieves the number of address identifiers supported on the indicated line.</span></span>             |
| [<span data-ttu-id="2c110-192">**TSPI \_ lineGetAddressID**</span><span class="sxs-lookup"><span data-stu-id="2c110-192">**TSPI\_lineGetAddressID**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressid)         | <span data-ttu-id="2c110-193">Récupère l’ID d’adresse d’une adresse spécifiée à l’aide d’un autre format.</span><span class="sxs-lookup"><span data-stu-id="2c110-193">Retrieves the address ID of an address specified using an alternate format.</span></span> <span data-ttu-id="2c110-194">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2c110-194">Synchronous.</span></span> |



 

## <a name="opening-and-closing-line-devices"></a><span data-ttu-id="2c110-195">Ouverture et fermeture des appareils en ligne</span><span class="sxs-lookup"><span data-stu-id="2c110-195">Opening and Closing Line Devices</span></span>



|  <span data-ttu-id="2c110-196">Fonction</span><span class="sxs-lookup"><span data-stu-id="2c110-196">Function</span></span>                                                         |   <span data-ttu-id="2c110-197">Description</span><span class="sxs-lookup"><span data-stu-id="2c110-197">Description</span></span>                                                        |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2c110-198">**TSPI \_ lineOpen**</span><span class="sxs-lookup"><span data-stu-id="2c110-198">**TSPI\_lineOpen**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineopen)   | <span data-ttu-id="2c110-199">Ouvre un appareil de ligne spécifié pour fournir une surveillance et/ou un contrôle ultérieurs de la ligne.</span><span class="sxs-lookup"><span data-stu-id="2c110-199">Opens a specified line device for providing subsequent monitoring and/or control of the line.</span></span> <span data-ttu-id="2c110-200">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2c110-200">Synchronous.</span></span> |
| [<span data-ttu-id="2c110-201">**TSPI \_ lineClose**</span><span class="sxs-lookup"><span data-stu-id="2c110-201">**TSPI\_lineClose**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineclose) | <span data-ttu-id="2c110-202">Ferme un appareil de ligne ouvert spécifié.</span><span class="sxs-lookup"><span data-stu-id="2c110-202">Closes a specified opened line device.</span></span> <span data-ttu-id="2c110-203">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2c110-203">Synchronous.</span></span>                                                        |



 

## <a name="call-states-and-events"></a><span data-ttu-id="2c110-204">États d’appel et événements</span><span class="sxs-lookup"><span data-stu-id="2c110-204">Call States and Events</span></span>



|  <span data-ttu-id="2c110-205">Fonction</span><span class="sxs-lookup"><span data-stu-id="2c110-205">Function</span></span>                                                         |   <span data-ttu-id="2c110-206">Description</span><span class="sxs-lookup"><span data-stu-id="2c110-206">Description</span></span>                                                        |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="2c110-207">**TSPI \_ lineGetCallInfo**</span><span class="sxs-lookup"><span data-stu-id="2c110-207">**TSPI\_lineGetCallInfo**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallinfo)       | <span data-ttu-id="2c110-208">Retourne des informations fixes sur un appel.</span><span class="sxs-lookup"><span data-stu-id="2c110-208">Returns fixed information about a call.</span></span> <span data-ttu-id="2c110-209">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2c110-209">Synchronous.</span></span>                                |
| [<span data-ttu-id="2c110-210">**TSPI \_ lineGetCallStatus**</span><span class="sxs-lookup"><span data-stu-id="2c110-210">**TSPI\_lineGetCallStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallstatus)   | <span data-ttu-id="2c110-211">Retourne les informations d’état de l’appel complet pour l’appel spécifié.</span><span class="sxs-lookup"><span data-stu-id="2c110-211">Returns complete call status information for the specified call.</span></span> <span data-ttu-id="2c110-212">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2c110-212">Synchronous.</span></span>       |
| [<span data-ttu-id="2c110-213">**TSPI \_ lineSetAppSpecific**</span><span class="sxs-lookup"><span data-stu-id="2c110-213">**TSPI\_lineSetAppSpecific**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetappspecific) | <span data-ttu-id="2c110-214">Définit le champ propre à l’application de la structure d’informations d’un appel.</span><span class="sxs-lookup"><span data-stu-id="2c110-214">Sets the application-specific field of a call's information structure.</span></span> <span data-ttu-id="2c110-215">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="2c110-215">Synchronous.</span></span> |



 

## <a name="making-calls"></a><span data-ttu-id="2c110-216">Appels effectués</span><span class="sxs-lookup"><span data-stu-id="2c110-216">Making Calls</span></span>



|  <span data-ttu-id="2c110-217">Fonction</span><span class="sxs-lookup"><span data-stu-id="2c110-217">Function</span></span>                                                         |   <span data-ttu-id="2c110-218">Description</span><span class="sxs-lookup"><span data-stu-id="2c110-218">Description</span></span>                                                        |
|-------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="2c110-219">**TSPI \_ lineMakeCall**</span><span class="sxs-lookup"><span data-stu-id="2c110-219">**TSPI\_lineMakeCall**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall) | <span data-ttu-id="2c110-220">Effectue un appel sortant et retourne un handle d’appel pour celui-ci.</span><span class="sxs-lookup"><span data-stu-id="2c110-220">Makes an outbound call and returns a call handle for it.</span></span> <span data-ttu-id="2c110-221">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="2c110-221">Asynchronous.</span></span> |
| [<span data-ttu-id="2c110-222">**TSPI \_ lineDial**</span><span class="sxs-lookup"><span data-stu-id="2c110-222">**TSPI\_lineDial**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linedial)         | <span data-ttu-id="2c110-223">Compose des adresses (parties d’une ou de plusieurs) adresses à distance.</span><span class="sxs-lookup"><span data-stu-id="2c110-223">Dials (parts of one or more) dialable addresses.</span></span> <span data-ttu-id="2c110-224">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="2c110-224">Asynchronous.</span></span>         |



 

## <a name="answering-incoming-calls"></a><span data-ttu-id="2c110-225">Réponse aux appels entrants</span><span class="sxs-lookup"><span data-stu-id="2c110-225">Answering Incoming Calls</span></span>



|  <span data-ttu-id="2c110-226">Fonction</span><span class="sxs-lookup"><span data-stu-id="2c110-226">Function</span></span>                                                         |   <span data-ttu-id="2c110-227">Description</span><span class="sxs-lookup"><span data-stu-id="2c110-227">Description</span></span>                                                        |
|---------------------------------------------|-----------------------------------------|
| [<span data-ttu-id="2c110-228">**TSPI \_ lineAnswer**</span><span class="sxs-lookup"><span data-stu-id="2c110-228">**TSPI\_lineAnswer**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineanswer) | <span data-ttu-id="2c110-229">Répond à un appel entrant.</span><span class="sxs-lookup"><span data-stu-id="2c110-229">Answers an incoming call.</span></span> <span data-ttu-id="2c110-230">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="2c110-230">Asynchronous.</span></span> |



 

## <a name="call-drop-functions"></a><span data-ttu-id="2c110-231">Appeler des fonctions Drop</span><span class="sxs-lookup"><span data-stu-id="2c110-231">Call Drop Functions</span></span>



|  <span data-ttu-id="2c110-232">Fonction</span><span class="sxs-lookup"><span data-stu-id="2c110-232">Function</span></span>                                                         |   <span data-ttu-id="2c110-233">Description</span><span class="sxs-lookup"><span data-stu-id="2c110-233">Description</span></span>                                                        |
|-----------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="2c110-234">**TSPI \_ lineDrop**</span><span class="sxs-lookup"><span data-stu-id="2c110-234">**TSPI\_lineDrop**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) | <span data-ttu-id="2c110-235">Déconnecte un appel ou abandonne une tentative d’appel en cours.</span><span class="sxs-lookup"><span data-stu-id="2c110-235">Disconnects a call, or abandons a call attempt in progress.</span></span> <span data-ttu-id="2c110-236">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="2c110-236">Asynchronous.</span></span> |



 

 

 
