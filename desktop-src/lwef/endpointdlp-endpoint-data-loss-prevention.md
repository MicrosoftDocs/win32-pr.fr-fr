---
description: Les API de protection contre la perte de données (DLP) du point de terminaison permettent aux applications de notifier le système d’exploitation avant et après certaines opérations, telles que l’ouverture ou l’enregistrement d’un fichier.
title: Protection contre la perte de données de point de terminaison
ms.topic: article
ms.date: 03/18/2021
ms.openlocfilehash: 3b8576f9eadd0037eca56c0ba183ea1d1825679a
ms.sourcegitcommit: 8b543a86e551cb5b4270a3cc3590ad0758fb6156
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/16/2021
ms.locfileid: "107526087"
---
# <a name="endpoint-data-loss-prevention"></a><span data-ttu-id="1d659-103">Protection contre la perte de données de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="1d659-103">Endpoint data loss prevention</span></span>

<span data-ttu-id="1d659-104">Windows 10 implémente des mécanismes qui permettent d’éviter la perte de données pour les fichiers sensibles.</span><span class="sxs-lookup"><span data-stu-id="1d659-104">Windows 10 implements mechanisms that help to prevent data loss for sensitive files.</span></span> <span data-ttu-id="1d659-105">Les API de protection contre la perte de données (DLP) du point de terminaison permettent aux applications de notifier le système d’exploitation avant et après certaines opérations, telles que l’ouverture ou l’enregistrement d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="1d659-105">The endpoint data loss prevention (DLP) APIs allow applications to notify the OS before and after certain operations, such as opening or saving a file.</span></span> <span data-ttu-id="1d659-106">Ces notifications servent d’indicateurs qui permettent au système d’optimiser les opérations de perte de données.</span><span class="sxs-lookup"><span data-stu-id="1d659-106">These notifications serve as "hints" that allow the system to optimize data loss operations.</span></span>

## <a name="location-of-the-dlp-dll"></a><span data-ttu-id="1d659-107">Emplacement de la dll DLP</span><span class="sxs-lookup"><span data-stu-id="1d659-107">Location of the DLP dll</span></span>

<span data-ttu-id="1d659-108">Étant donné que la dll DLP du point de terminaison n’est pas regroupée avec le SDK Windows, les applications doivent charger la dll manuellement au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="1d659-108">Since the endpoint DLP dll isn't bundled with the Windows SDK, applications will need to load the dll manually at runtime.</span></span> <span data-ttu-id="1d659-109">Le chemin d’accès à l’emplacement de la dll est stocké dans le registre.</span><span class="sxs-lookup"><span data-stu-id="1d659-109">The path to the dll location is stored in the registry.</span></span> <span data-ttu-id="1d659-110">Le tableau suivant répertorie les clés de Registre et les valeurs qui stockent ces informations.</span><span class="sxs-lookup"><span data-stu-id="1d659-110">The following table lists the registry keys and values that store this information.</span></span> <span data-ttu-id="1d659-111">Ces chemins d’accès sont définis en tant que constantes dans l’exemple de code endpointdlp. h fourni ci-dessous pour les développeurs.</span><span class="sxs-lookup"><span data-stu-id="1d659-111">These paths are defined as constants in the sample endpointdlp.h code listing provided below as a convenience for developers.</span></span>

| <span data-ttu-id="1d659-112">Constante</span><span class="sxs-lookup"><span data-stu-id="1d659-112">Constant</span></span> | <span data-ttu-id="1d659-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="1d659-113">Value</span></span> | <span data-ttu-id="1d659-114">Description</span><span class="sxs-lookup"><span data-stu-id="1d659-114">Description</span></span>   |
|----------|-------|---------------|
| <span data-ttu-id="1d659-115">ENDPOINTDLP_DLL_NAME</span><span class="sxs-lookup"><span data-stu-id="1d659-115">ENDPOINTDLP_DLL_NAME</span></span> | <span data-ttu-id="1d659-116">« EndpointDlp.dll »</span><span class="sxs-lookup"><span data-stu-id="1d659-116">"EndpointDlp.dll"</span></span> | <span data-ttu-id="1d659-117">Nom de la DLL DLP de point de terminaison qui fournit l’API</span><span class="sxs-lookup"><span data-stu-id="1d659-117">The name of the Endpoint DLP DLL that provides the API</span></span> |
| <span data-ttu-id="1d659-118">ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY</span><span class="sxs-lookup"><span data-stu-id="1d659-118">ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY</span></span> | <span data-ttu-id="1d659-119">« LOGICIEL \\ Microsoft \\ Windows Defender »</span><span class="sxs-lookup"><span data-stu-id="1d659-119">"SOFTWARE\\Microsoft\\Windows Defender"</span></span> | <span data-ttu-id="1d659-120">Clé de Registre Windows Defender sous HKLM où certains paramètres DLP de point de terminaison sont stockés</span><span class="sxs-lookup"><span data-stu-id="1d659-120">Windows Defender registry key under HKLM where some Endpoint DLP settings are stored</span></span> |
| <span data-ttu-id="1d659-121">ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY</span><span class="sxs-lookup"><span data-stu-id="1d659-121">ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY</span></span> | <span data-ttu-id="1d659-122">Valeur de ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY</span><span class="sxs-lookup"><span data-stu-id="1d659-122">Value of ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY</span></span> |  <span data-ttu-id="1d659-123">Chemin d’accès au Registre sous la clé HKLM à partir de laquelle l’emplacement d’installation de EndpointDlp.dll peut être obtenu</span><span class="sxs-lookup"><span data-stu-id="1d659-123">The registry path under HKLM key from which the EndpointDlp.dll install location can be obtained</span></span> |
| <span data-ttu-id="1d659-124">ENDPOINTDLP_DLL_INSTALL_LOCATION_REGVALUE</span><span class="sxs-lookup"><span data-stu-id="1d659-124">ENDPOINTDLP_DLL_INSTALL_LOCATION_REGVALUE</span></span> | <span data-ttu-id="1d659-125">INSTALLLOCATION</span><span class="sxs-lookup"><span data-stu-id="1d659-125">"InstallLocation"</span></span> | <span data-ttu-id="1d659-126">Valeur de Registre sous ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY dans laquelle l’emplacement d’installation du EndpointDlp.dll est stocké</span><span class="sxs-lookup"><span data-stu-id="1d659-126">The registry value under ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY in which the EndpointDlp.dll install location is stored</span></span> |
| <span data-ttu-id="1d659-127">ENDPOINTDLP_DLL_WOW64_X86_INSTALL_LOCATION_SUFFIX</span><span class="sxs-lookup"><span data-stu-id="1d659-127">ENDPOINTDLP_DLL_WOW64_X86_INSTALL_LOCATION_SUFFIX</span></span> | <span data-ttu-id="1d659-128">systèmes</span><span class="sxs-lookup"><span data-stu-id="1d659-128">"x86"</span></span> | <span data-ttu-id="1d659-129">Sur les plateformes x64, concaténez ce répertoire pour obtenir la version x86 de EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="1d659-129">On x64 platforms, concatenate this directory to obtain the x86 version of EndpointDlp.dll</span></span> |

## <a name="check-if-endpoint-dlp-is-enabled"></a><span data-ttu-id="1d659-130">Vérifier si le point de terminaison DLP est activé</span><span class="sxs-lookup"><span data-stu-id="1d659-130">Check if endpoint DLP is enabled</span></span>

<span data-ttu-id="1d659-131">Pour déterminer si le point de terminaison DLP est activé sur le système, vérifiez la valeur de clé de Registre suivante.</span><span class="sxs-lookup"><span data-stu-id="1d659-131">To determine if endpoint DLP is enabled on the system, check the following registry key value.</span></span> 

| <span data-ttu-id="1d659-132">Constante</span><span class="sxs-lookup"><span data-stu-id="1d659-132">Constant</span></span> | <span data-ttu-id="1d659-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="1d659-133">Value</span></span> | <span data-ttu-id="1d659-134">Description</span><span class="sxs-lookup"><span data-stu-id="1d659-134">Description</span></span>   |
|----------|-------|---------------|
| <span data-ttu-id="1d659-135">ENDPOINTDLP_ENABLED_FLAG_REGKEY</span><span class="sxs-lookup"><span data-stu-id="1d659-135">ENDPOINTDLP_ENABLED_FLAG_REGKEY</span></span> |  <span data-ttu-id="1d659-136">« \\ Fonctionnalités »</span><span class="sxs-lookup"><span data-stu-id="1d659-136">"\\Features"</span></span> | <span data-ttu-id="1d659-137">Le chemin d’accès à la clé de l’indicateur de point de terminaison activé par DLP sous (HKLM) ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY</span><span class="sxs-lookup"><span data-stu-id="1d659-137">The path to the Endpoint DLP enabled flag key under (HKLM) ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY</span></span> |
| <span data-ttu-id="1d659-138">ENDPOINTDLP_ENABLED_FLAG_REGVALUE</span><span class="sxs-lookup"><span data-stu-id="1d659-138">ENDPOINTDLP_ENABLED_FLAG_REGVALUE</span></span> | <span data-ttu-id="1d659-139">"SenseDlpEnabled"</span><span class="sxs-lookup"><span data-stu-id="1d659-139">"SenseDlpEnabled"</span></span> | <span data-ttu-id="1d659-140">Valeur de Registre sous ENDPOINTDLP_ENABLED_FLAG_REGKEY contenant la clé de registre de l’indicateur DLP activé</span><span class="sxs-lookup"><span data-stu-id="1d659-140">The registry value under ENDPOINTDLP_ENABLED_FLAG_REGKEY containing the DLP enabled flag registry key</span></span>

## <a name="endpoint-dlp-apis"></a><span data-ttu-id="1d659-141">API DLP de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="1d659-141">Endpoint DLP APIs</span></span>

<span data-ttu-id="1d659-142">Les tableaux suivants répertorient les API fournies par la dll DLP de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="1d659-142">The following tables list the APIs provided by the endpoint DLP dll.</span></span>

### <a name="initialization-and-versioning"></a><span data-ttu-id="1d659-143">Initialisation et contrôle de version</span><span class="sxs-lookup"><span data-stu-id="1d659-143">Initialization and versioning</span></span>

| <span data-ttu-id="1d659-144">API</span><span class="sxs-lookup"><span data-stu-id="1d659-144">API</span></span> | <span data-ttu-id="1d659-145">Description</span><span class="sxs-lookup"><span data-stu-id="1d659-145">Description</span></span> |
|-----|-------------|
| [<span data-ttu-id="1d659-146">DlpInitializeEnforcementMode</span><span class="sxs-lookup"><span data-stu-id="1d659-146">DlpInitializeEnforcementMode</span></span>](endpointdlp-dlpinitializeenforcementmode.md)                       | <span data-ttu-id="1d659-147">Indique au système les modes de mise en conformité souhaités pour un ensemble d’opérations de protection contre la perte de données (DLP) de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="1d659-147">Notifies the system of the desired enforcement modes for a set of endpoint Data Loss Prevention (DLP) operations.</span></span>                                  |
| [<span data-ttu-id="1d659-148">DlpGetEnforcementApiVersion</span><span class="sxs-lookup"><span data-stu-id="1d659-148">DlpGetEnforcementApiVersion</span></span>](endpointdlp-dlpgetenforcementapiversion.md)                       | <span data-ttu-id="1d659-149">Récupère la version de l’API de protection contre la perte de données (DLP) du point de terminaison sur l’appareil actuel.</span><span class="sxs-lookup"><span data-stu-id="1d659-149">Retrieves the version of the endpoint Data Loss Prevention (DLP) API on the current device.</span></span>                                  |


### <a name="document-operations"></a><span data-ttu-id="1d659-150">Opérations de document</span><span class="sxs-lookup"><span data-stu-id="1d659-150">Document operations</span></span>

| <span data-ttu-id="1d659-151">API</span><span class="sxs-lookup"><span data-stu-id="1d659-151">API</span></span> | <span data-ttu-id="1d659-152">Description</span><span class="sxs-lookup"><span data-stu-id="1d659-152">Description</span></span> |
|-----|-------------|
| [<span data-ttu-id="1d659-153">DlpNotifyPreOpenDocument</span><span class="sxs-lookup"><span data-stu-id="1d659-153">DlpNotifyPreOpenDocument</span></span>](endpointdlp-dlpnotifypreopendocument.md) | <span data-ttu-id="1d659-154">Fournit au système des informations sur un document avant le lancement de l’opération d’ouverture.</span><span class="sxs-lookup"><span data-stu-id="1d659-154">Provides the system with information about a document before the open operation is initiated.</span></span> |
| [<span data-ttu-id="1d659-155">DlpNotifyPostOpenDocument</span><span class="sxs-lookup"><span data-stu-id="1d659-155">DlpNotifyPostOpenDocument</span></span>](endpointdlp-dlpnotifypostopendocument.md) | <span data-ttu-id="1d659-156">Fournit au système des informations sur un document une fois l’opération d’ouverture terminée.</span><span class="sxs-lookup"><span data-stu-id="1d659-156">Provides the system with information about a document after the open operation is completed.</span></span>  |
| [<span data-ttu-id="1d659-157">DlpNotifyCloseDocument</span><span class="sxs-lookup"><span data-stu-id="1d659-157">DlpNotifyCloseDocument</span></span>](endpointdlp-dlpnotifyclosedocument.md)                       | <span data-ttu-id="1d659-158">Fournit au système des informations sur un document avant le lancement de l’opération de fermeture du document.</span><span class="sxs-lookup"><span data-stu-id="1d659-158">Provides the system with information about a document before the document close operation is initiated.</span></span>                                  |
| [<span data-ttu-id="1d659-159">DlpNotifyPreOpenDocumentFile</span><span class="sxs-lookup"><span data-stu-id="1d659-159">DlpNotifyPreOpenDocumentFile</span></span>](endpointdlp-dlpnotifypreopendocumentfile.md)                         | <span data-ttu-id="1d659-160">Fournit au système des informations sur un document avant le lancement de l’opération d’ouverture.</span><span class="sxs-lookup"><span data-stu-id="1d659-160">Provides the system with information about a document before the open operation is initiated.</span></span>  |
| [<span data-ttu-id="1d659-161">DlpNotifyPostOpenDocumentFile</span><span class="sxs-lookup"><span data-stu-id="1d659-161">DlpNotifyPostOpenDocumentFile</span></span>](endpointdlp-dlpnotifypostopendocumentfile.md)                       | <span data-ttu-id="1d659-162">Fournit au système des informations sur un document une fois l’opération d’ouverture terminée.</span><span class="sxs-lookup"><span data-stu-id="1d659-162">Provides the system with information about a document after the open operation is completed.</span></span>                                  |
| [<span data-ttu-id="1d659-163">DlpNotifyCloseDocumentFile</span><span class="sxs-lookup"><span data-stu-id="1d659-163">DlpNotifyCloseDocumentFile</span></span>](endpointdlp-dlpnotifyclosedocumentfile.md)                       | <span data-ttu-id="1d659-164">Fournit au système des informations sur un document avant le lancement de l’opération de fermeture du document.</span><span class="sxs-lookup"><span data-stu-id="1d659-164">Provides the system with information about a document before the document close operation is initiated.</span></span>                                  |

### <a name="save-as-operations"></a><span data-ttu-id="1d659-165">Enregistrer en tant que opérations</span><span class="sxs-lookup"><span data-stu-id="1d659-165">Save as operations</span></span>
| <span data-ttu-id="1d659-166">API</span><span class="sxs-lookup"><span data-stu-id="1d659-166">API</span></span> | <span data-ttu-id="1d659-167">Description</span><span class="sxs-lookup"><span data-stu-id="1d659-167">Description</span></span> |
|-----|-------------|
| [<span data-ttu-id="1d659-168">DlpNotifyPreSaveAsDocument</span><span class="sxs-lookup"><span data-stu-id="1d659-168">DlpNotifyPreSaveAsDocument</span></span>](endpointdlp-dlpnotifypresaveasdocument.md)                       | <span data-ttu-id="1d659-169">Fournit au système des informations sur un document avant le lancement d’une opération Enregistrer sous.</span><span class="sxs-lookup"><span data-stu-id="1d659-169">Provides the system with information about a document before a save as operation is initiated.</span></span>                                  |
| [<span data-ttu-id="1d659-170">DlpNotifyPostSaveAsDocument</span><span class="sxs-lookup"><span data-stu-id="1d659-170">DlpNotifyPostSaveAsDocument</span></span>](endpointdlp-dlpnotifypostsaveasdocument.md)                       | <span data-ttu-id="1d659-171">Fournit au système des informations sur un document après la fin de l’opération Enregistrer sous.</span><span class="sxs-lookup"><span data-stu-id="1d659-171">Provides the system with information about a document after the save as operation is completed.</span></span>                                  |


### <a name="drag-and-drop-operations"></a><span data-ttu-id="1d659-172">Opérations de glisser-déplacer</span><span class="sxs-lookup"><span data-stu-id="1d659-172">Drag and drop operations</span></span>

| <span data-ttu-id="1d659-173">API</span><span class="sxs-lookup"><span data-stu-id="1d659-173">API</span></span> | <span data-ttu-id="1d659-174">Description</span><span class="sxs-lookup"><span data-stu-id="1d659-174">Description</span></span> |
|-----|-------------|
| [<span data-ttu-id="1d659-175">DlpNotifyEnterDropTarget</span><span class="sxs-lookup"><span data-stu-id="1d659-175">DlpNotifyEnterDropTarget</span></span>](endpointdlp-dlpnotifyenterdroptarget.md)                       | <span data-ttu-id="1d659-176">Fournit au système des informations sur un document quand une cible de déplacement est entrée.</span><span class="sxs-lookup"><span data-stu-id="1d659-176">Provides the system with information about a document when a drop target is entered.</span></span>                                  |
| [<span data-ttu-id="1d659-177">DlpNotifyLeaveDropTarget</span><span class="sxs-lookup"><span data-stu-id="1d659-177">DlpNotifyLeaveDropTarget</span></span>](endpointdlp-dlpnotifyleavedroptarget.md)                       | <span data-ttu-id="1d659-178">Fournit au système des informations sur un document lors de la sortie d’une cible de déplacement.</span><span class="sxs-lookup"><span data-stu-id="1d659-178">Provides the system with information about a document when a drop target is exited.</span></span>                                  |
| [<span data-ttu-id="1d659-179">DlpNotifyPreDragDrop</span><span class="sxs-lookup"><span data-stu-id="1d659-179">DlpNotifyPreDragDrop</span></span>](endpointdlp-dlpnotifypredragdrop.md)                         | <span data-ttu-id="1d659-180">Fournit au système des informations sur un document avant le lancement d’une opération glisser-déplacer.</span><span class="sxs-lookup"><span data-stu-id="1d659-180">Provides the system with information about a document before a drag drop operation is initiated.</span></span>  |
| [<span data-ttu-id="1d659-181">DlpNotifyPostDragDrop</span><span class="sxs-lookup"><span data-stu-id="1d659-181">DlpNotifyPostDragDrop</span></span>](endpointdlp-dlpnotifypostdragdrop.md)                         | <span data-ttu-id="1d659-182">Fournit au système des informations sur un document après l’exécution d’une opération glisser-déplacer.</span><span class="sxs-lookup"><span data-stu-id="1d659-182">Provides the system with information about a document after a drag drop operation is completed.</span></span>  |


### <a name="clipboard-operations"></a><span data-ttu-id="1d659-183">opérations du Presse-papiers</span><span class="sxs-lookup"><span data-stu-id="1d659-183">Clipboard operations</span></span>

| <span data-ttu-id="1d659-184">API</span><span class="sxs-lookup"><span data-stu-id="1d659-184">API</span></span> | <span data-ttu-id="1d659-185">Description</span><span class="sxs-lookup"><span data-stu-id="1d659-185">Description</span></span> |
|-----|-------------|
| [<span data-ttu-id="1d659-186">DlpNotifyPreCopyToClipboard</span><span class="sxs-lookup"><span data-stu-id="1d659-186">DlpNotifyPreCopyToClipboard</span></span>](endpointdlp-dlpnotifyprecopytoclipboard.md)                         | <span data-ttu-id="1d659-187">Fournit au système des informations sur un document avant le lancement d’une opération copier dans le presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="1d659-187">Provides the system with information about a document before a copy to clipboard operation is initiated.</span></span>  |
| [<span data-ttu-id="1d659-188">DlpNotifyPostCopyToClipboard</span><span class="sxs-lookup"><span data-stu-id="1d659-188">DlpNotifyPostCopyToClipboard</span></span>](endpointdlp-dlpnotifypostcopytoclipboard.md)                         | <span data-ttu-id="1d659-189">Fournit au système des informations sur un document après l’exécution d’une opération copier dans le presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="1d659-189">Provides the system with information about a document after a copy to clipboard operation is completed.</span></span>  |
| [<span data-ttu-id="1d659-190">DlpNotifyPrePasteFromClipboard</span><span class="sxs-lookup"><span data-stu-id="1d659-190">DlpNotifyPrePasteFromClipboard</span></span>](endpointdlp-dlpnotifyprepastefromclipboard.md)                         | <span data-ttu-id="1d659-191">Fournit au système des informations sur un document avant le lancement d’une opération coller à partir du presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="1d659-191">Provides the system with information about a document before a paste from clipboard operation is initiated.</span></span>  |
| [<span data-ttu-id="1d659-192">DlpNotifyPostPasteFromClipboard</span><span class="sxs-lookup"><span data-stu-id="1d659-192">DlpNotifyPostPasteFromClipboard</span></span>](endpointdlp-dlpnotifypostpastefromclipboard.md)                       | <span data-ttu-id="1d659-193">Fournit au système des informations sur un document après la fin de l’opération coller à partir du presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="1d659-193">Provides the system with information about a document after a paste from clipboard operation has completed.</span></span>                                  |
| [<span data-ttu-id="1d659-194">DlpNotifyPostStashClipboard</span><span class="sxs-lookup"><span data-stu-id="1d659-194">DlpNotifyPostStashClipboard</span></span>](endpointdlp-dlpnotifypoststashclipboard.md)                       | <span data-ttu-id="1d659-195">Fournit au système des informations d’État après la fin d’une opération de presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="1d659-195">Provides the system with status information after a stash clipboard operation is completed.</span></span>                                  |
| [<span data-ttu-id="1d659-196">DlpNotifyPreStashClipboard</span><span class="sxs-lookup"><span data-stu-id="1d659-196">DlpNotifyPreStashClipboard</span></span>](endpointdlp-dlpnotifyprestashclipboard.md)                       | <span data-ttu-id="1d659-197">Notifie le système avant l’initialisation d’une opération de presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="1d659-197">Notifies the system before a stash clipboard operation is initiated.</span></span>                                  |
| [<span data-ttu-id="1d659-198">DlpMustPasteFromSystemClipboard</span><span class="sxs-lookup"><span data-stu-id="1d659-198">DlpMustPasteFromSystemClipboard</span></span>](endpointdlp-dlpmustpastefromsystemclipboard.md)                       | <span data-ttu-id="1d659-199">Détermine si l’application doit extraire les données du presse-papiers du système au lieu de les extraire de son cache interne.</span><span class="sxs-lookup"><span data-stu-id="1d659-199">Determines whether the app must pull the data from the system clipboard rather than taking it from its internal cache.</span></span>                                  |

### <a name="print-operations"></a><span data-ttu-id="1d659-200">Opérations d’impression</span><span class="sxs-lookup"><span data-stu-id="1d659-200">Print operations</span></span>

| <span data-ttu-id="1d659-201">API</span><span class="sxs-lookup"><span data-stu-id="1d659-201">API</span></span> | <span data-ttu-id="1d659-202">Description</span><span class="sxs-lookup"><span data-stu-id="1d659-202">Description</span></span> |
|-----|-------------|
| [<span data-ttu-id="1d659-203">DlpNotifyPrePrint</span><span class="sxs-lookup"><span data-stu-id="1d659-203">DlpNotifyPrePrint</span></span>](endpointdlp-dlpnotifypreprint.md)                         | <span data-ttu-id="1d659-204">Fournit au système des informations sur un document avant le lancement d’une opération d’impression.</span><span class="sxs-lookup"><span data-stu-id="1d659-204">Provides the system with information about a document before a print operation is initiated.</span></span>  |
| [<span data-ttu-id="1d659-205">DlpNotifyPostStartPrint</span><span class="sxs-lookup"><span data-stu-id="1d659-205">DlpNotifyPostStartPrint</span></span>](endpointdlp-dlpnotifypoststartprint.md)                       | <span data-ttu-id="1d659-206">Fournit au système des informations sur un document après le démarrage d’une opération d’impression.</span><span class="sxs-lookup"><span data-stu-id="1d659-206">Provides the system with information about a document after an print operation has started.</span></span>                                  |
| [<span data-ttu-id="1d659-207">DlpNotifyPostPrint</span><span class="sxs-lookup"><span data-stu-id="1d659-207">DlpNotifyPostPrint</span></span>](endpointdlp-dlpnotifypostprint.md)                       | <span data-ttu-id="1d659-208">Fournit au système des informations sur un document une fois l’opération d’impression terminée.</span><span class="sxs-lookup"><span data-stu-id="1d659-208">Provides the system with information about a document after a print operation has completed.</span></span>                                  |

## <a name="endpoint-dlp-example-header"></a><span data-ttu-id="1d659-209">En-tête d’exemple DLP de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="1d659-209">Endpoint DLP example header</span></span>

<span data-ttu-id="1d659-210">Étant donné que l’en-tête DLP de point de terminaison n’est pas inclus dans la SDK Windows, vous devez créer vous-même le fichier d’en-tête pour pouvoir utiliser les signatures d’API dans votre implémentation.</span><span class="sxs-lookup"><span data-stu-id="1d659-210">Because the endpoint DLP header is not included in the Windows SDK, you must create the header file yourself to get API signatures to use in your implementation.</span></span> <span data-ttu-id="1d659-211">Pour votre commodité, nous fournissons un exemple de code que vous pouvez copier et coller dans votre application.</span><span class="sxs-lookup"><span data-stu-id="1d659-211">For your convenience we're providing example code that you can copy and paste into your application.</span></span> <span data-ttu-id="1d659-212">En plus des déclarations de fonction, cette liste de code définit également des constantes utiles telles que les informations de contrôle de version et les chemins de clés de registre.</span><span class="sxs-lookup"><span data-stu-id="1d659-212">In addition to function declarations, this code listing also defines useful constants such as versioning information and registry key paths.</span></span>

```cpp
//
// EndpointDlp DLL name containing the Endpoint DLP API
//

#define ENDPOINTDLP_DLL_NAME L"EndpointDlp.dll"

//
// Windows Defender registry key under HKLM where some Endpoint DLP settings are stored
//

#define ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY L"SOFTWARE\\Microsoft\\Windows Defender"

//
// EndpointDlp.dll install location can be obtained from the registry under the following HKLM key
//

#define ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY

//
// EndpointDlp.dll install location is stored under ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY in the following registry value
//

#define ENDPOINTDLP_DLL_INSTALL_LOCATION_REGVALUE L"InstallLocation"

//
// On x64 platforms, concatanate the following directory to obtain the x86 version of EndpointDlp.dll
//

#define ENDPOINTDLP_DLL_WOW64_X86_INSTALL_LOCATION_SUFFIX L"x86"

//
// Endpoint DLP enabled flag can be found under the following HKLM key
//

#define ENDPOINTDLP_ENABLED_FLAG_REGKEY ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY L"\\Features"

//
// Endpoint DLP enabled flag can be found under ENDPOINTDLP_ENABLED_REGKEY in the following registry value
//

#define ENDPOINTDLP_ENABLED_FLAG_REGVALUE L"SenseDlpEnabled"


#define DLP_DOCUMENT_INFO_V_1 0x1     

#define DLP_DOCUMENT_INFO_V_LATEST DLP_DOCUMENT_INFO_V_1


//
//  Enlightened app enforcement capablities.
//

typedef enum _DlpAppEnforceLevel {
    DlpAppEnforceLevelNone = 0, // No enforcement, DLP enforces operation.
    DlpAppEnforceLevelNotify,   // App send notifications on operation, DLP enforces operation.
    DlpAppEnforceLevelPrevent,  // Currently not supported (App allows or blocks operation, DLP enforces warning, eventing and UI). 
    DlpAppEnforceLevelFull,     // Currently not supported (App handles all enforcement (blocks operation, enforces warning, UI), DLP will only handle auditing.)
    DlpAppEnforceLevelCount,
}DlpAppEnforceLevel;

typedef enum  
{
    DlpActionTypeCopyToRemovableMedia = 0,
    DlpActionTypeCopyToNetworkShare = 1,
    DlpActionTypeCopyToClipboard = 2,
    DlpActionTypePrint = 3,
    DlpActionTypeScreenClip = 4,
    DlpActionTypeAccessByUnallowedApp = 5,
    DlpActionTypeCloudAppEgress = 6,
    DlpActionTypeAccessByBluetoothApp = 7,
    DlpActionTypeAccessByRDPApp = 8,
    DlpActionTypeCount = 9
} DlpActionType;
    
//
//  The stucture describes the enforcement level for each operation.
//
    
typedef struct _DLP_APP_OP_ENLIGHTENED_LEVEL{
    DlpActionType Operation;
    DlpAppEnforceLevel AppEnforcementLevel;
}DLP_APP_OP_ENLIGHTENED_LEVEL, *PDLP_APP_OP_ENLIGHTENED_LEVEL;


/*
Function description:
     The application calls this functio to declares the enforcement level for each operation.

Parameters:
    _In_ DWORD Count - Number of operations. 
    _In_reads_opt_(Count) PDLP_APP_OP_ENLIGHTENED_LEVEL* OperationEnforcement - Array indicating operations
    supported by the application and enforcement level:
        DlpAppEnforceLevelNone - No enforcement, DLP enforces operation.
        DlpAppEnforceLevelNotify -  App send notifications on operation, DLP enforces operation.

Return:
    S_OK - Function completed successfully.
    E_INVALIDARG - Invalid parameters passed to function.
    E_OUTOFMEMORY - Memory allocation failed.
    E_XXX - Varius error codes.
*/       
HRESULT WINAPI DlpInitializeEnforcementMode(_In_ DWORD Count, _In_reads_(Count) PDLP_APP_OP_ENLIGHTENED_LEVEL OperationEnforcement);


/*
Function description:
    Returns the version of the enforcement API.
    MajorVersion indicates a new interfaces/API.
    MinorVersion indicates changes to existing interfaces/API-s.
   
Parameters:
    None.

Return:
    S_OK - Function completed successfully
    E_XXX - Varius error codes.
*/
HRESULT WINAPI DlpGetEnforcementApiVersion(_Out_ DWORD* MajorVersion, _Out_ DWORD* MinorVersion);


typedef struct _DLP_DOCUMENT_INFO {

    //
    //  Information version. Always set it to DLP_DOCUMENT_INFO_V_LATEST
    //
    
    DWORD Version;

    //
    //  Original path of the document.
    //  
    
    LPCWSTR PersistentFileName;

    //
    //  Path to the real backing file.
    //
    
    LPCWSTR LocalFileName;

}DLP_DOCUMENT_INFO, *PDLP_DOCUMENT_INFO;

//
//  Post operation status information.
//
    
#define DLP_POSTOP_STATUS_V_1 0x1     
        
#define DLP_POSTOP_STATUS_V_LATEST DLP_POSTOP_STATUS_V_1;
    
       
typedef struct _DLP_POSTOP_STATUS {

    //
    //  Information version. Always set it to DLP_POSTOP_STATUS_V_LATEST
    //
    
    DWORD Version;

    //
    //  Set to TRUE if app's operation succeeded, FALSE otherwise. 
    //
    
    BOOL OperationSuccess;  

} DLP_POSTOP_STATUS, *PDLP_POSTOP_STATUS;    


#define DLP_PRINT_INFO_V_1 0x1     
    
#define DLP_PRINT_INFO_V_LATEST DLP_PRINT_INFO_V_1;

typedef struct _DLP_PRINT_INFO {

    //
    //  Information version. Always set it to DLP_PRINT_INFO_V_LATEST
    //
    
    DWORD Version;

    //
    //  Destination printer.
    //
    
    LPCWSTR PrinterName;

    //
    //  Print job name.
    //
    
    LPCWSTR JobName;

    //
    //  Output file, if printing to file.
    //

    LPCWSTR OutputFileName;
    
}DLP_PRINT_INFO, *PDLP_PRINT_INFO;

    
void WINAPI DlpNotifyPreOpenDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostOpenDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus); 

void WINAPI DlpNotifyCloseDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);

void WINAPI DlpNotifyPreOpenDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostOpenDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus); 

void WINAPI DlpNotifyCloseDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);

void WINAPI DlpNotifyPreSaveAsDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ LPCWSTR Destination);
void WINAPI DlpNotifyPostSaveAsDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ LPCWSTR Destination, _In_ const PDLP_POSTOP_STATUS OpStatus); 

void WINAPI DlpNotifyPrePrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo);
void WINAPI DlpNotifyPostStartPrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo);
void WINAPI DlpNotifyPostPrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);

void WINAPI DlpNotifyPreCopyToClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostCopyToClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);

void WINAPI DlpNotifyPrePasteFromClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostPasteFromClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);

void WINAPI DlpNotifyPreStashClipboard();
void WINAPI DlpNotifyPostStashClipboard(_In_ const PDLP_POSTOP_STATUS OpStatus);

void WINAPI DlpNotifyPreDragDrop(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostDragDrop(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);
    
void WINAPI DlpNotifyEnterDropTarget(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyLeaveDropTarget(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus); 


/*
Function description:
    Determines whether the app must pull the data from the system clipboard rather than taking it from its internal cache.

Parameters:
    None

Return:
    TRUE if calling into the OS clipboard is mandatory, FALSE otherwise
*/
BOOL WINAPI DlpMustPasteFromSystemClipboard();

```


