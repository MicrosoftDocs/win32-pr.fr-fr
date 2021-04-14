---
title: Traçage
description: Le suivi utilise Suivi d’v nements pour Windows (ETW).
ms.assetid: b008bae2-9423-4e72-ae03-9cd50f73d812
keywords:
- Suivi des services Web pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82c660884667cefae8067376075a30cbc41f70d4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104383307"
---
# <a name="tracing"></a><span data-ttu-id="4b6cf-106">Traçage</span><span class="sxs-lookup"><span data-stu-id="4b6cf-106">Tracing</span></span>

<span data-ttu-id="4b6cf-107">Le suivi utilise Suivi d’v nements pour Windows (ETW).</span><span class="sxs-lookup"><span data-stu-id="4b6cf-107">Tracing uses Event Tracing for Windows (ETW).</span></span> <span data-ttu-id="4b6cf-108">Pour tirer parti des outils de suivi disponibles avec Windows Server 2008 R2, installez le Microsoft Windows SDK à partir du site de [téléchargement MSDN](https://www.microsoft.com/download/details.aspx?id=8279) .</span><span class="sxs-lookup"><span data-stu-id="4b6cf-108">To take advantage of the tracing tools available with Windows Server 2008 R2, install the Microsoft Windows SDK from the [MSDN Downloads](https://www.microsoft.com/download/details.aspx?id=8279) site.</span></span>


<span data-ttu-id="4b6cf-109">Trois niveaux de suivi sont pris en charge :</span><span class="sxs-lookup"><span data-stu-id="4b6cf-109">There are three tracing levels supported:</span></span>

-   <span data-ttu-id="4b6cf-110">Verbose (toutes les traces disponibles).</span><span class="sxs-lookup"><span data-stu-id="4b6cf-110">Verbose (all available traces).</span></span>
-   <span data-ttu-id="4b6cf-111">Info (traces d’informations).</span><span class="sxs-lookup"><span data-stu-id="4b6cf-111">Info (informational traces).</span></span>
-   <span data-ttu-id="4b6cf-112">Erreur (traces d’erreurs).</span><span class="sxs-lookup"><span data-stu-id="4b6cf-112">Error (error traces).</span></span>

<span data-ttu-id="4b6cf-113">Les événements suivants sont suivis :</span><span class="sxs-lookup"><span data-stu-id="4b6cf-113">The following events are traced:</span></span>

-   <span data-ttu-id="4b6cf-114">Toutes les erreurs (niveau = erreur, niveau = info ou niveau = détaillé).</span><span class="sxs-lookup"><span data-stu-id="4b6cf-114">Any errors (Level=Error, Level=Info or Level=Verbose).</span></span>
-   <span data-ttu-id="4b6cf-115">Entrée/sortie d’une API (Level = info ou level = verbose).</span><span class="sxs-lookup"><span data-stu-id="4b6cf-115">Entry/Exit of an API (Level=Info or Level=Verbose).</span></span>
-   <span data-ttu-id="4b6cf-116">Début et fin de toutes les e/s (niveau = info ou niveau = détaillé)</span><span class="sxs-lookup"><span data-stu-id="4b6cf-116">Start and completion of any IO (Level=Info or Level=Verbose)</span></span>
-   <span data-ttu-id="4b6cf-117">Messages SOAP échangés (niveau = verbose, disponible sur Windows 2003 SP1 et versions ultérieures)</span><span class="sxs-lookup"><span data-stu-id="4b6cf-117">Exchanged SOAP messages (Level=Verbose, available on Windows 2003 SP1 and later)</span></span>

## <a name="generating-and-viewing-wwsapi-traces"></a><span data-ttu-id="4b6cf-118">Génération et affichage des traces WWSAPI</span><span class="sxs-lookup"><span data-stu-id="4b6cf-118">Generating and Viewing WWSAPI Traces</span></span>

<span data-ttu-id="4b6cf-119">WWSAPI utilise les événements basés sur le manifeste sur Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-119">WWSAPI uses the manifest based events on Windows Vista and above.</span></span> <span data-ttu-id="4b6cf-120">Par conséquent, l’expérience de suivi présente des différences en fonction de la version du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-120">As a result, the tracing experience has some differences based on the operating system version.</span></span> <span data-ttu-id="4b6cf-121">La génération de suivis ETW peut être effectuée à l’aide des outils ETW intégrés sur toutes les plateformes prises en charge.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-121">Generating ETW traces can be done by using the in-box ETW tools on all supported platforms.</span></span> <span data-ttu-id="4b6cf-122">Toutefois, l’affichage des suivis ETW dans un format attrayant nécessite des outils personnalisés sur Windows XP SP2 et Windows 2003 SP1.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-122">However viewing the ETW traces in a nice format requires custom tools on Windows XP SP2 and Windows 2003 SP1.</span></span> <span data-ttu-id="4b6cf-123">Il existe plusieurs façons de collecter et d’afficher les suivis d’événements ETW WWSAPI en fonction de la version du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-123">There are few different ways of collecting and viewing WWSAPI ETW event traces depending on the operating system version.</span></span>

## <a name="enabling-and-viewing-wwsapi-traces-in-event-viewer-works-on-windows-vista-and-above"></a><span data-ttu-id="4b6cf-124">Activation et affichage des traces WWSAPI dans observateur d’événements (fonctionne sur Windows Vista et versions ultérieures)</span><span class="sxs-lookup"><span data-stu-id="4b6cf-124">Enabling and Viewing WWSAPI traces in Event Viewer (works on Windows Vista and above)</span></span>

-   <span data-ttu-id="4b6cf-125">Exécutez eventvwr. msc à partir de la ligne de commande ou du menu exécuter.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-125">Run eventvwr.msc from command line or run menu.</span></span>
-   <span data-ttu-id="4b6cf-126">Cliquez sur le lien Afficher dans le volet actions à droite, puis activez l’option Afficher les journaux d’analyse et de débogage.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-126">Click the view link on the Actions pane on the right and enable Show Analytic and Debug logs option.</span></span>
-   <span data-ttu-id="4b6cf-127">Accédez à la fenêtre journaux des applications et des services \\ \\ fournisseurs Microsoft Windows \\ WebServices dans le volet gauche.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-127">Browse to Application and Service Logs\\Microsoft\\Windows\\WebServices providers on the left pane.</span></span>
-   <span data-ttu-id="4b6cf-128">Cliquez avec le bouton droit sur le fournisseur de suivi et sélectionnez Activer le journal.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-128">Right click the Tracing provider and select Enable log.</span></span>
-   <span data-ttu-id="4b6cf-129">Exécutez votre scénario.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-129">Run your scenario.</span></span>
-   <span data-ttu-id="4b6cf-130">Quand vous actualisez la page de l’observateur d’événements, vous devez commencer à voir les entrées de suivi WWSAPI.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-130">When you refresh the event viewer page, you should start seeing the WWSAPI tracing entries.</span></span>

## <a name="enabling-and-viewing-wwsapi-traces-using-wstracebat-script-works-on-xpsp2-and-above"></a><span data-ttu-id="4b6cf-131">Activation et affichage des traces WWSAPI à l’aide d' Wstrace.bat script (fonctionne sur XPSP2 et versions ultérieures)</span><span class="sxs-lookup"><span data-stu-id="4b6cf-131">Enabling and Viewing WWSAPI traces using Wstrace.bat Script (works on XPSP2 and above)</span></span>

<span data-ttu-id="4b6cf-132">Le fichier de commandes wstrace.bat offre un moyen pratique d’effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="4b6cf-132">The wstrace.bat batch file provides a convenient way to:</span></span>

-   <span data-ttu-id="4b6cf-133">Créer un journal des traces</span><span class="sxs-lookup"><span data-stu-id="4b6cf-133">Create a trace log</span></span>
-   <span data-ttu-id="4b6cf-134">Supprimer un journal de suivi</span><span class="sxs-lookup"><span data-stu-id="4b6cf-134">Delete a trace log</span></span>
-   <span data-ttu-id="4b6cf-135">Activer et désactiver le suivi</span><span class="sxs-lookup"><span data-stu-id="4b6cf-135">Enable and disable tracing</span></span>
-   <span data-ttu-id="4b6cf-136">Mettre à jour le niveau de suivi (info/erreur/verbose)</span><span class="sxs-lookup"><span data-stu-id="4b6cf-136">Update the tracing level (info/error/verbose)</span></span>
-   <span data-ttu-id="4b6cf-137">Conversion des journaux de suivi en fichiers CSV</span><span class="sxs-lookup"><span data-stu-id="4b6cf-137">Converting trace logs to CSV files</span></span>

<span data-ttu-id="4b6cf-138">Le fichier de commandes utilise logman.exe pour toutes les commandes, à l’exception de la conversion des journaux en fichier CSV, qui nécessite un outil personnalisé (wstracedump.exe).</span><span class="sxs-lookup"><span data-stu-id="4b6cf-138">The batch file uses logman.exe for all commands, with the exception of converting the logs to CSV file, which requires a custom tool (wstracedump.exe).</span></span>

## <a name="using-tracing-commands"></a><span data-ttu-id="4b6cf-139">Utilisation des commandes de suivi</span><span class="sxs-lookup"><span data-stu-id="4b6cf-139">Using tracing commands</span></span>

<span data-ttu-id="4b6cf-140">La commande suivante crée un journal qui utilise les informations, les erreurs ou le niveau de détail.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-140">The following command creates a log that uses info, error or verbose level.</span></span> <span data-ttu-id="4b6cf-141">Cette commande requiert des privilèges élevés.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-141">This command requires elevated privileges.</span></span>

<span data-ttu-id="4b6cf-142">**wstrace.bat de créer des \[ informations détaillées sur l' \| erreur \|\]**</span><span class="sxs-lookup"><span data-stu-id="4b6cf-142">**wstrace.bat create \[info \| error \| verbose\]**</span></span>

<span data-ttu-id="4b6cf-143">La commande suivante supprime le journal.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-143">The following command deletes the log.</span></span> <span data-ttu-id="4b6cf-144">Cette commande requiert des privilèges élevés.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-144">This command requires elevated privileges.</span></span>

<span data-ttu-id="4b6cf-145">**wstrace.bat supprimer**</span><span class="sxs-lookup"><span data-stu-id="4b6cf-145">**wstrace.bat delete**</span></span>

<span data-ttu-id="4b6cf-146">La commande suivante active le suivi.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-146">The following command enables tracing.</span></span> <span data-ttu-id="4b6cf-147">Vous devez d’abord créer un journal.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-147">You must first create a log.</span></span>

<span data-ttu-id="4b6cf-148">**wstrace.bat**</span><span class="sxs-lookup"><span data-stu-id="4b6cf-148">**wstrace.bat on**</span></span>

<span data-ttu-id="4b6cf-149">Le niveau de suivi (info, erreur ou commentaires) peut être modifié comme suit :</span><span class="sxs-lookup"><span data-stu-id="4b6cf-149">The tracing level (info, error or verbose) can be modified as follows:</span></span>

<span data-ttu-id="4b6cf-150">**Informations de mise à jourwstrace.bat \[ informations \| \| détaillées\]**</span><span class="sxs-lookup"><span data-stu-id="4b6cf-150">**wstrace.bat update \[info \| error \| verbose\]**</span></span>

<span data-ttu-id="4b6cf-151">Pour vider la sortie de trace, utilisez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="4b6cf-151">To dump the trace output, use the following command:</span></span>

<span data-ttu-id="4b6cf-152">**wstrace.bat > de vidage temp.csv**</span><span class="sxs-lookup"><span data-stu-id="4b6cf-152">**wstrace.bat dump > temp.csv**</span></span>

<span data-ttu-id="4b6cf-153">Les événements seront vidés dans le fichier CSV jusqu’à ce que CTRL-C soit enfoncé ou que le suivi soit désactivé.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-153">The events will be dumped to the CSV file until Ctrl-C is pressed or tracing is disabled.</span></span>

## <a name="tracing-file-format"></a><span data-ttu-id="4b6cf-154">Format de fichier de suivi</span><span class="sxs-lookup"><span data-stu-id="4b6cf-154">Tracing File format</span></span>

<span data-ttu-id="4b6cf-155">Les fichiers CSV créés par wstrace.bat sont des fichiers texte de variables séparées par des virgules simples.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-155">The CSV files created by wstrace.bat are simple comma-separated-variable text files.</span></span> <span data-ttu-id="4b6cf-156">Ces fichiers peuvent être ouverts dans Excel, dans le bloc-notes, etc.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-156">These files may be opened in Excel, Notepad, etc.</span></span>

<span data-ttu-id="4b6cf-157">Les colonnes du fichier sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="4b6cf-157">The columns of the file are as follows:</span></span>

-   <span data-ttu-id="4b6cf-158">Horodatage du moment où l’événement a été enregistré</span><span class="sxs-lookup"><span data-stu-id="4b6cf-158">TimeStamp - Time stamp of when the event was recorded</span></span>
-   <span data-ttu-id="4b6cf-159">ProcessID-ID ULONG du processus d’enregistrement de l’événement</span><span class="sxs-lookup"><span data-stu-id="4b6cf-159">ProcessID - ULONG ID of the process recording the event</span></span>
-   <span data-ttu-id="4b6cf-160">ThreadID-ID ULONG du thread enregistrant l’événement</span><span class="sxs-lookup"><span data-stu-id="4b6cf-160">ThreadID - ULONG ID of the thread recording the event</span></span>
-   <span data-ttu-id="4b6cf-161">La valeur d’énumération d’événements du type d’événement peut être (« API Enter » " \| API pending" " \| API ExitSyncSuccess" \| "API ExitSyncFailure" \| "API ExitAsyncSuccess" \| "API ExitAsyncFailure" \| "IO Started" \| "e/s terminée « \| » échec de l’e/s « » \| , erreur «réception du message \| reçu » « \| message \| \| \| \| reçu » « réception du message d’arrêt » « l’envoi du message a été envoyé ».</span><span class="sxs-lookup"><span data-stu-id="4b6cf-161">Event - Enumerated value of the event type may be ("api enter" \| "api pending" \| "api ExitSyncSuccess" \| "api ExitSyncFailure" \| "api ExitAsyncSuccess" \| "api ExitAsyncFailure" \| "io started" \| "io completed" \| "io failed" \| "error" \| "received message start" \| "received message" \| "received message stop" \| "sending message start" \| "sending message" \| "sending message stop")</span></span>
-   <span data-ttu-id="4b6cf-162">Operation : nom de l’opération appelée.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-162">Operation - The name of the operation being invoked.</span></span> <span data-ttu-id="4b6cf-163">En général, il est mappé à l’API appelée.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-163">Typically this maps to the API being called.</span></span>
-   <span data-ttu-id="4b6cf-164">Erreur : numéro d’erreur HRESULT facultatif</span><span class="sxs-lookup"><span data-stu-id="4b6cf-164">Error - Optional HRESULT error number</span></span>
-   <span data-ttu-id="4b6cf-165">Info : informations facultatives sur l’événement</span><span class="sxs-lookup"><span data-stu-id="4b6cf-165">Info - Optional information about the event</span></span>

## <a name="collecting-wwsapi-etw-trace-file-using-etw-tools-works-on-xpsp2-and-above"></a><span data-ttu-id="4b6cf-166">Collecte du fichier de trace ETW WWSAPI à l’aide des outils ETW (fonctionne sur XPSP2 et versions ultérieures)</span><span class="sxs-lookup"><span data-stu-id="4b6cf-166">Collecting WWSAPI ETW Trace File using ETW tools (works on XPSP2 and above)</span></span>

<span data-ttu-id="4b6cf-167">Activation du suivi ETW pour WWSAPI</span><span class="sxs-lookup"><span data-stu-id="4b6cf-167">Enabling ETW tracing for WWSAPI</span></span>

<span data-ttu-id="4b6cf-168">**logman start wstrace-BS 64-ft 1-RT-p Microsoft-Windows-WebServices \[ indicateurs \[ niveau \] \] \[ -o <EtlLogFileName> \] -ETS**</span><span class="sxs-lookup"><span data-stu-id="4b6cf-168">**logman start wstrace -bs 64 -ft 1 -rt -p Microsoft-Windows-WebServices \[flags \[level\]\] \[-o <EtlLogFileName>\] -ets**</span></span>

<span data-ttu-id="4b6cf-169">pour créer et démarrer la session de suivi ETW.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-169">to create and start the ETW tracing session.</span></span> <span data-ttu-id="4b6cf-170">Logman.exe est un outil ETW intégré disponible sur toutes les plateformes prises en charge.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-170">Logman.exe is an in-box ETW tool available on all supported platforms.</span></span> <span data-ttu-id="4b6cf-171">Notez que vous devez utiliser Microsoft \_ Windows \_ WebServices comme nom de fournisseur sur XPSP2 et Windows.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-171">Note that you need to use Microsoft\_Windows\_WebServices as the provider name on XPSP2 and W2K3.</span></span> <span data-ttu-id="4b6cf-172">Vous pouvez exécuter logman query providers pour afficher la liste des fournisseurs inscrits.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-172">You can run logman query providers to see the list of registered providers.</span></span> <span data-ttu-id="4b6cf-173">Le fournisseur Microsoft-Windows-WebServices (ou Microsoft \_ Windows \_ WebServices) doit être répertorié, sauf s’il n’est pas inscrit.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-173">Microsoft-Windows-WebServices (or Microsoft\_Windows\_WebServices) provider should be listed unless it is not registered.</span></span> <span data-ttu-id="4b6cf-174">Le fournisseur est normalement inscrit au cours de l’installation.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-174">The provider is normally registered during setup.</span></span> <span data-ttu-id="4b6cf-175">Toutefois, il peut également être inscrit manuellement en exécutant wevtutil.exe im <ManifestFileName> (sur Windows Vista et versions ultérieures) ou mofcomp.exe <MofFileName> (sur XPSP2 et Windows-version).</span><span class="sxs-lookup"><span data-stu-id="4b6cf-175">However it can also be manually registered by running wevtutil.exe im <ManifestFileName> (on Windows Vista and Later) or mofcomp.exe <MofFileName> (on XPSP2 and W2K3).</span></span>

<span data-ttu-id="4b6cf-176">Les indicateurs peuvent être utilisés pour filtrer les traces par leur genre.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-176">Flags can be used to filter the traces by their kind.</span></span> <span data-ttu-id="4b6cf-177">Il peut s’agir d’une valeur ou d’un des genres de trace suivants.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-177">It can be OR'd value of the following trace kinds.</span></span> <span data-ttu-id="4b6cf-178">S’il n’est pas fourni, tous les types de suivi sont activés.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-178">If not supplied, all trace kinds are enabled.</span></span>

-   <span data-ttu-id="4b6cf-179">0x1-suivis d’entrée/sortie de l’API.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-179">0x1 - API entry/exit traces.</span></span>
-   <span data-ttu-id="4b6cf-180">0X2-suivi des erreurs.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-180">0x2 - Error traces.</span></span>
-   <span data-ttu-id="4b6cf-181">0x4-suivis d’e/s.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-181">0x4 - IO traces.</span></span>
-   <span data-ttu-id="4b6cf-182">0x8-suivis des messages SOAP.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-182">0x8 - SOAP message traces.</span></span>
-   <span data-ttu-id="4b6cf-183">0x10 : traces des messages binaires.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-183">0x10 - Binary message traces.</span></span>

<span data-ttu-id="4b6cf-184">Le niveau peut être utilisé pour filtrer les traces par niveau.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-184">Level can be used to filter the traces by their level.</span></span> <span data-ttu-id="4b6cf-185">Il doit s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-185">It should be one of the following values.</span></span> <span data-ttu-id="4b6cf-186">S’il n’est pas fourni, tous les niveaux de suivi sont activés.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-186">If not supplied, all trace levels are enabled.</span></span>

-   <span data-ttu-id="4b6cf-187">0x1-traces irrécupérables.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-187">0x1 - Fatal traces.</span></span>
-   <span data-ttu-id="4b6cf-188">0X2-suivi des erreurs.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-188">0x2 - Error traces.</span></span>
-   <span data-ttu-id="4b6cf-189">0x3-traces d’avertissement.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-189">0x3 - Warning traces.</span></span>
-   <span data-ttu-id="4b6cf-190">0x4-suivis d’information.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-190">0x4 - Informational traces.</span></span>
-   <span data-ttu-id="4b6cf-191">0x5-suivis détaillés.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-191">0x5 - Verbose traces.</span></span>

<span data-ttu-id="4b6cf-192">EtlLogFileName est le chemin d’accès au fichier journal des événements ETW à créer (utilisez l’extension. ETL).</span><span class="sxs-lookup"><span data-stu-id="4b6cf-192">EtlLogFileName is the path to the ETW event log file to be created (use .etl extension).</span></span> <span data-ttu-id="4b6cf-193">S’il n’est pas fourni, ETW choisit un nom aléatoire qui peut être interrogé ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-193">If not provided, ETW will pick a random name which can be queried later.</span></span> <span data-ttu-id="4b6cf-194">Ce fichier ne doit pas résider dans le répertoire de profil de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-194">This file should not reside on user's profile directory.</span></span> <span data-ttu-id="4b6cf-195">Le fichier journal des événements ETW (fichier. ETL) est au format binaire.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-195">ETW event log file (.etl file) is in binary format.</span></span> <span data-ttu-id="4b6cf-196">Elle peut être consommée par les applications ETW, mais elle n’est pas dans un format lisible par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-196">It can be consumed by ETW applications, but it is not in human readable format.</span></span> <span data-ttu-id="4b6cf-197">L’étape suivante décrit comment afficher son contenu.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-197">Next step describes how to view its content.</span></span>

<span data-ttu-id="4b6cf-198">Exécuter votre scénario</span><span class="sxs-lookup"><span data-stu-id="4b6cf-198">Run your scenario</span></span>

<span data-ttu-id="4b6cf-199">Collecte du fichier journal des événements ETW.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-199">Collecting ETW event log file.</span></span>

<span data-ttu-id="4b6cf-200">**logman stop wstrace-ETS**</span><span class="sxs-lookup"><span data-stu-id="4b6cf-200">**logman stop wstrace -ets**</span></span>

<span data-ttu-id="4b6cf-201">pour arrêter la session de suivi ETW.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-201">to stop the ETW tracing session.</span></span> <span data-ttu-id="4b6cf-202">C’est à ce moment que ETW arrête l’enregistrement des événements.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-202">This is when ETW stops logging the events.</span></span> <span data-ttu-id="4b6cf-203">Le fichier journal des événements ETW (spécifié dans le paramètre EtlLogFileName) est prêt à être consommé.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-203">ETW event log file (specified in EtlLogFileName parameter) is ready to consume.</span></span> <span data-ttu-id="4b6cf-204">Il peut être affiché localement (les instructions sont fournies ci-dessous) ou envoyées au groupe de produits à des fins d’investigation.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-204">It can either be viewed locally (instructions are given below) or sent to the product group for investigation.</span></span>

<span data-ttu-id="4b6cf-205">Exemple de bout en bout utilisant les outils ETW :</span><span class="sxs-lookup"><span data-stu-id="4b6cf-205">End to end example using ETW tools:</span></span>

<span data-ttu-id="4b6cf-206">**logman start wstrace-BS 64-ft 1-RT-p Microsoft-Windows-WebServices-o mytrace. etl-ETS**</span><span class="sxs-lookup"><span data-stu-id="4b6cf-206">**logman start wstrace -bs 64 -ft 1 -rt -p Microsoft-Windows-WebServices -o mytrace.etl -ets**</span></span>

<span data-ttu-id="4b6cf-207">**echo.. Exécutez votre scénario.**</span><span class="sxs-lookup"><span data-stu-id="4b6cf-207">**echo .. run your scenario..**</span></span>

<span data-ttu-id="4b6cf-208">**logman stop wstrace-ETS**</span><span class="sxs-lookup"><span data-stu-id="4b6cf-208">**logman stop wstrace -ets**</span></span>

<span data-ttu-id="4b6cf-209">**tracerpt mytrace. etl-o mytrace.xml**</span><span class="sxs-lookup"><span data-stu-id="4b6cf-209">**tracerpt mytrace.etl -o mytrace.xml**</span></span>

<span data-ttu-id="4b6cf-210">**wstrace.htm**</span><span class="sxs-lookup"><span data-stu-id="4b6cf-210">**wstrace.htm**</span></span>

<span data-ttu-id="4b6cf-211">**echo.. Utilisez mytrace.xml et wstrace. xsl dans la page ouverte..**</span><span class="sxs-lookup"><span data-stu-id="4b6cf-211">**echo .. use mytrace.xml and wstrace.xsl in the opened page ..**</span></span>

## <a name="viewing-wwsapi-etw-trace-file-traces-using-wstracedumpexe-tool-works-on-windows-xp-and-above"></a><span data-ttu-id="4b6cf-212">Affichage des traces du fichier de trace ETW WWSAPI à l’aide de l’outil wstracedump.exe (fonctionne sur Windows XP et versions ultérieures)</span><span class="sxs-lookup"><span data-stu-id="4b6cf-212">Viewing WWSAPI ETW Trace File traces using wstracedump.exe tool (works on Windows XP and above)</span></span>

<span data-ttu-id="4b6cf-213">Wstracedump.exe est un outil consommateur ETW développé personnalisé qui traite les événements dans le fichier de trace ETW WWSAPI et produit une sortie lisible par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-213">Wstracedump.exe is a custom developed ETW consumer tool which processes events in the WWSAPI ETW trace file and produces human readable output.</span></span> <span data-ttu-id="4b6cf-214">Il peut produire une sortie de toutes les plateformes prises en charge.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-214">It can produce output from all supported platforms.</span></span> <span data-ttu-id="4b6cf-215">Pour plus d’informations, consultez son utilisation (wstracedump.exe- ?).</span><span class="sxs-lookup"><span data-stu-id="4b6cf-215">See its usage (wstracedump.exe -?) for more information.</span></span>

## <a name="viewing-wwsapi-etw-trace-file-traces-using-etw-tools-works-on-windows-vista-and-above"></a><span data-ttu-id="4b6cf-216">Affichage des traces du fichier de trace ETW WWSAPI à l’aide des outils ETW (fonctionne sur Windows Vista et versions ultérieures)</span><span class="sxs-lookup"><span data-stu-id="4b6cf-216">Viewing WWSAPI ETW Trace File traces using ETW tools (works on Windows Vista and above)</span></span>

<span data-ttu-id="4b6cf-217">Tracerpt.exe est l’outil qui permet d’afficher le contenu d’un fichier journal d’événements ETW et est disponible sur toutes les plateformes prises en charge.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-217">Tracerpt.exe is the tool to view the content of an ETW event log file and available on all supported platforms.</span></span> <span data-ttu-id="4b6cf-218">Il peut être utilisé pour générer des fichiers de vidage CSV, EVTX ou XML à partir d’un fichier journal d’événements ETW.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-218">It can be used to generate CSV, EVTX or XML dump files from an ETW event log file.</span></span> <span data-ttu-id="4b6cf-219">Toutefois, le fichier de sortie généré a des traces lisibles par les humains uniquement sur Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-219">However the generated output file has human readable traces only on Windows Vista and later.</span></span> <span data-ttu-id="4b6cf-220">Ces instructions décrivent comment générer le fichier de vidage XML et l’utiliser avec un fichier XSL pour afficher les traces dans un format attrayant (le fichier XSL est très trivial et peut être modifié si vous souhaitez des formats différents).</span><span class="sxs-lookup"><span data-stu-id="4b6cf-220">These instructions describes how to generate the XML dump file and use it along with an xsl file to display the traces in a nice format (xsl file is very trivial and may be altered if different formats are desired).</span></span>

-   <span data-ttu-id="4b6cf-221">Exécuter</span><span class="sxs-lookup"><span data-stu-id="4b6cf-221">Run</span></span>

    <span data-ttu-id="4b6cf-222">**tracerpt <EtlLogFileName> -o <OutputXMLFileName>**</span><span class="sxs-lookup"><span data-stu-id="4b6cf-222">**tracerpt <EtlLogFileName> -o <OutputXMLFileName>**</span></span>

    <span data-ttu-id="4b6cf-223">pour créer un vidage XML à partir du fichier ETL binaire (tracerpt.exe crée le fichier de sortie au format XML par défaut.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-223">to create an XML dump from the binary ETL file (tracerpt.exe creates the output file in XML format by default.</span></span> <span data-ttu-id="4b6cf-224">Exécuter tracerpt- ?</span><span class="sxs-lookup"><span data-stu-id="4b6cf-224">Run tracerpt -?</span></span> <span data-ttu-id="4b6cf-225">Pour voir d’autres formats disponibles).</span><span class="sxs-lookup"><span data-stu-id="4b6cf-225">To see other available formats).</span></span>

-   <span data-ttu-id="4b6cf-226">À ce stade, vous pouvez voir les informations de suivi dans le fichier XML.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-226">At this point, you can see the tracing information in the XML file.</span></span> <span data-ttu-id="4b6cf-227">En outre, vous pouvez ouvrir le fichier wstrace.htm et utiliser le fichier dump XML et le fichier wstrace. xsl pour voir les traces dans un format plus attrayant.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-227">Additionally, you can open the wstrace.htm file and use the xml dump file and the wstrace.xsl file to see the traces in a nicer format.</span></span> <span data-ttu-id="4b6cf-228">Notez que les fichiers doivent se trouver sur l’ordinateur local pour pouvoir utiliser ce fichier HTML sur Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-228">Note that the files need to be on the local machine to be able to use this html file on IE.</span></span>

## <a name="security"></a><span data-ttu-id="4b6cf-229">Sécurité</span><span class="sxs-lookup"><span data-stu-id="4b6cf-229">Security</span></span>

<span data-ttu-id="4b6cf-230">Lors de l’activation du suivi, les administrateurs doivent prendre en compte la consommation d’espace disque supplémentaire et de puissance de calcul.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-230">When enabling tracing, administrators should take into account that it consumes additional disk space and computation power.</span></span> <span data-ttu-id="4b6cf-231">Un client ou une application malveillante peut épuiser les ressources système, sauf si les paramètres de suivi sont configurés avec des limites raisonnables.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-231">A malicious client or application may exhaust system resources unless tracing settings are configured with reasonable limits.</span></span> <span data-ttu-id="4b6cf-232">Lors de l’utilisation de la fonctionnalité de suivi des messages, les messages qui transportent des informations sensibles telles que des informations d’identification, des informations personnelles, etc., peuvent être conservés sur le disque ou être consultés par toute personne ayant accès à l’observateur d’événements système.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-232">When using message tracing feature, messages carrying sensitive information such as credentials, personal information, etc. may be persisted to the disk or be viewed by anyone who has access to the system event viewer.</span></span> <span data-ttu-id="4b6cf-233">Pour pallier ce problème, le suivi peut être activé par des utilisateurs système ou administrateur sur Windows 2003 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-233">As a mitigation to this issue, tracing can be enabled by System or Administrator users on Windows 2003 and later.</span></span> <span data-ttu-id="4b6cf-234">Le suivi des messages est désactivé sur Windows XP sur lequel n’importe quel utilisateur peut activer le suivi.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-234">Message tracing is disabled on Windows XP on which any user can turn tracing on.</span></span>

<span data-ttu-id="4b6cf-235">L’énumération suivante est utilisée avec le suivi :</span><span class="sxs-lookup"><span data-stu-id="4b6cf-235">The following enumeration is used with tracing:</span></span>

-   [<span data-ttu-id="4b6cf-236">**\_API WS trace \_**</span><span class="sxs-lookup"><span data-stu-id="4b6cf-236">**WS\_TRACE\_API**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_trace_api)

 

 




