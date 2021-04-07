---
description: À compter de Windows Vista, le service WMI n’utilise pas les fichiers journaux WMI. Au lieu de cela, il utilise Suivi d’v nements pour Windows (ETW) et les événements sont disponibles via observateur d’événements ou l’outil en ligne de commande Wevtutil.
ms.assetid: bb6401e8-caf7-4f39-ab64-b7532723ce9a
ms.tgt_platform: multiple
title: Suivi de l’activité WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14371a4f18b81019073cd2b428500b12385719e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758007"
---
# <a name="tracing-wmi-activity"></a><span data-ttu-id="750b2-104">Suivi de l’activité WMI</span><span class="sxs-lookup"><span data-stu-id="750b2-104">Tracing WMI Activity</span></span>

<span data-ttu-id="750b2-105">À compter de Windows Vista, le service WMI n’utilise pas les [fichiers journaux WMI](wmi-log-files.md).</span><span class="sxs-lookup"><span data-stu-id="750b2-105">Starting with Windows Vista, the WMI service does not use the [WMI Log Files](wmi-log-files.md).</span></span> <span data-ttu-id="750b2-106">Au lieu de cela, il utilise [suivi d’v nements pour Windows (ETW)](/windows/desktop/ETW/event-tracing-portal) et les événements sont disponibles via **Observateur d’événements** ou l’outil en ligne de commande Wevtutil.</span><span class="sxs-lookup"><span data-stu-id="750b2-106">Instead, it uses [Event Tracing for Windows (ETW)](/windows/desktop/ETW/event-tracing-portal) and events are available through **Event Viewer** or the Wevtutil command-line tool.</span></span>

<span data-ttu-id="750b2-107">Les sections suivantes sont présentées dans cette rubrique :</span><span class="sxs-lookup"><span data-stu-id="750b2-107">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="750b2-108">Obtention d’événements WMI via observateur d’événements</span><span class="sxs-lookup"><span data-stu-id="750b2-108">Obtaining WMI Events Through Event Viewer</span></span>](#obtaining-wmi-events-through-event-viewer)
-   [<span data-ttu-id="750b2-109">Activation du suivi WMI à l’invite de commandes</span><span class="sxs-lookup"><span data-stu-id="750b2-109">Enabling WMI Tracing at Command Prompt</span></span>](#enabling-wmi-tracing-at-command-prompt)
-   [<span data-ttu-id="750b2-110">Utilisation du suivi WMI basé sur WPP</span><span class="sxs-lookup"><span data-stu-id="750b2-110">Using WPP-based WMI Tracing</span></span>](#using-wpp-based-wmi-tracing)
-   [<span data-ttu-id="750b2-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="750b2-111">Related topics</span></span>](#related-topics)

## <a name="obtaining-wmi-events-through-event-viewer"></a><span data-ttu-id="750b2-112">Obtention d’événements WMI via observateur d’événements</span><span class="sxs-lookup"><span data-stu-id="750b2-112">Obtaining WMI Events Through Event Viewer</span></span>

<span data-ttu-id="750b2-113">Le fichier WMITracing. log contient les événements suivis par WMI.</span><span class="sxs-lookup"><span data-stu-id="750b2-113">The WMITracing.log file contains the events that WMI traces.</span></span> <span data-ttu-id="750b2-114">Toutefois, il s’agit d’un fichier binaire.</span><span class="sxs-lookup"><span data-stu-id="750b2-114">However, this is a binary file.</span></span> <span data-ttu-id="750b2-115">Pour afficher ces événements dans un format lisible par l’homme, utilisez l' **Observateur d’événements**.</span><span class="sxs-lookup"><span data-stu-id="750b2-115">To see these events in a format readable by humans, use the **Event Viewer**.</span></span>

<span data-ttu-id="750b2-116">Par défaut, les événements WMI ne sont pas suivis.</span><span class="sxs-lookup"><span data-stu-id="750b2-116">By default, WMI events are not traced.</span></span> <span data-ttu-id="750b2-117">Cette procédure décrit comment utiliser **Observateur d’événements** pour activer le suivi d’événements WMI et localiser les événements WMI.</span><span class="sxs-lookup"><span data-stu-id="750b2-117">This procedure describes how to use **Event Viewer** to enable WMI event tracing and locate WMI events.</span></span> <span data-ttu-id="750b2-118">Vous pouvez effectuer les mêmes opérations à l’aide de l’outil en ligne de commande Wevtutil.</span><span class="sxs-lookup"><span data-stu-id="750b2-118">You can do the same operations through the wevtutil command-line tool.</span></span>

<span data-ttu-id="750b2-119">**Pour afficher les événements WMI dans observateur d’événements**</span><span class="sxs-lookup"><span data-stu-id="750b2-119">**To view WMI Events in Event Viewer**</span></span>

1.  <span data-ttu-id="750b2-120">Ouvrez l’ **Observateur d’événements**.</span><span class="sxs-lookup"><span data-stu-id="750b2-120">Open **Event Viewer**.</span></span> <span data-ttu-id="750b2-121">Dans le menu **Affichage**, cliquez sur **Afficher les journaux d'analyse et de débogage**.</span><span class="sxs-lookup"><span data-stu-id="750b2-121">On the **View** menu, click **Show Analytic and Debug Logs**.</span></span> <span data-ttu-id="750b2-122">Recherchez le journal des canaux de **suivi** pour WMI sous applications et journaux des services \| \| activité Microsoft Windows \| WMI.</span><span class="sxs-lookup"><span data-stu-id="750b2-122">Locate the **Trace** channel log for WMI under Applications and Service Logs \| Microsoft \| Windows \| WMI Activity.</span></span>
2.  <span data-ttu-id="750b2-123">Cliquez avec le bouton droit sur le journal de **suivi** et sélectionnez **Propriétés du journal**.</span><span class="sxs-lookup"><span data-stu-id="750b2-123">Right-click the **Trace** log and select **Log Properties**.</span></span> <span data-ttu-id="750b2-124">Activez la case à cocher **activer la journalisation** pour démarrer le suivi d’événements WMI.</span><span class="sxs-lookup"><span data-stu-id="750b2-124">Click the **Enable Logging** check box to start the WMI event tracing.</span></span> <span data-ttu-id="750b2-125">Pour plus d’informations sur les canaux, consultez [journaux des événements et canaux dans le journal des événements Windows](/previous-versions//aa385225(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="750b2-125">For more information about channels, see [Event Logs and Channels in Windows Event Log](/previous-versions//aa385225(v=vs.85)).</span></span>
3.  <span data-ttu-id="750b2-126">Les événements WMI s’affichent dans la fenêtre d’événements pour l' **activité WMI**.</span><span class="sxs-lookup"><span data-stu-id="750b2-126">WMI events appear in the event window for **WMI-Activity**.</span></span> <span data-ttu-id="750b2-127">Double-cliquez sur un événement de la liste pour afficher les informations détaillées.</span><span class="sxs-lookup"><span data-stu-id="750b2-127">Double-click an event in the list to see the detailed information.</span></span> <span data-ttu-id="750b2-128">Vous pouvez afficher un événement en **mode XML** ou dans un format d' **affichage convivial** .</span><span class="sxs-lookup"><span data-stu-id="750b2-128">You can view an event in **XML View** or in **Friendly View** format.</span></span>

<span data-ttu-id="750b2-129">Le champ **ID d’événement** affiche une valeur qui contient les informations suivantes.</span><span class="sxs-lookup"><span data-stu-id="750b2-129">The **Event ID** field displays a value that contains the following information.</span></span>

<dl> <dt>

<span data-ttu-id="750b2-130"><span id="Event_1"></span><span id="event_1"></span><span id="EVENT_1"></span>Événement 1</span><span class="sxs-lookup"><span data-stu-id="750b2-130"><span id="Event_1"></span><span id="event_1"></span><span id="EVENT_1"></span>Event 1</span></span>
</dt> <dd>

<span data-ttu-id="750b2-131">Début de la séquence d’événements pour une opération spécifique.</span><span class="sxs-lookup"><span data-stu-id="750b2-131">Start of the event sequence for a specific operation.</span></span> <span data-ttu-id="750b2-132">Une occurrence pour chaque séquence.</span><span class="sxs-lookup"><span data-stu-id="750b2-132">One occurrence for each sequence.</span></span>

<span data-ttu-id="750b2-133">Les champs d’événement pour un événement 1 sont :</span><span class="sxs-lookup"><span data-stu-id="750b2-133">The event fields for an Event 1 are:</span></span>

-   <span data-ttu-id="750b2-134">**GroupOperationID** est un identificateur unique utilisé pour tous les événements signalés pour un client spécifique.</span><span class="sxs-lookup"><span data-stu-id="750b2-134">**GroupOperationID** is a unique identifier that is used for all events reported for a specific client.</span></span>
-   <span data-ttu-id="750b2-135">**OperationId** indique la séquence d’opérations.</span><span class="sxs-lookup"><span data-stu-id="750b2-135">**OperationId** indicates the operation sequence.</span></span>
-   <span data-ttu-id="750b2-136">L' **opération** spécifie la connexion ou la demande à WMI.</span><span class="sxs-lookup"><span data-stu-id="750b2-136">**Operation** specifies the connection or request to WMI.</span></span>
-   <span data-ttu-id="750b2-137">L' **utilisateur** indique le compte qui effectue une requête auprès de WMI en exécutant un script ou via CIM Studio.</span><span class="sxs-lookup"><span data-stu-id="750b2-137">**User** indicates the account that makes a request to WMI by running a script or through CIM Studio.</span></span>
-   <span data-ttu-id="750b2-138">**Espace** de noms affiche l’espace de noms WMI dans lequel la connexion est établie.</span><span class="sxs-lookup"><span data-stu-id="750b2-138">**Namespace** shows the WMI namespace to which the connection is made.</span></span>

<span data-ttu-id="750b2-139">Par exemple, un script peut demander toutes les instances d’une classe WMI, telles que [**le \_ service Win32**](/windows/desktop/CIMWin32Prov/win32-service).</span><span class="sxs-lookup"><span data-stu-id="750b2-139">For example, a script may request all the instances of a WMI class, such as [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span> <span data-ttu-id="750b2-140">La première opération peut être une connexion à WMI.</span><span class="sxs-lookup"><span data-stu-id="750b2-140">The first operation may be a connection to WMI.</span></span>

</dd> <dt>

<span data-ttu-id="750b2-141"><span id="Event_2"></span><span id="event_2"></span><span id="EVENT_2"></span>Événement 2</span><span class="sxs-lookup"><span data-stu-id="750b2-141"><span id="Event_2"></span><span id="event_2"></span><span id="EVENT_2"></span>Event 2</span></span>
</dt> <dd>

<span data-ttu-id="750b2-142">Événements qui composent l’opération.</span><span class="sxs-lookup"><span data-stu-id="750b2-142">Events that make up the operation.</span></span> <span data-ttu-id="750b2-143">Une ou plusieurs occurrences dans la séquence.</span><span class="sxs-lookup"><span data-stu-id="750b2-143">One or more occurrences in the sequence.</span></span>

<span data-ttu-id="750b2-144">Les champs d’événement pour un événement 2 sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="750b2-144">The event fields for an Event 2 are:</span></span>

-   <span data-ttu-id="750b2-145">**GroupOperationID** indique la séquence dans laquelle l’événement se produit.</span><span class="sxs-lookup"><span data-stu-id="750b2-145">**GroupOperationID** indicates the sequence in which the event occurs.</span></span>
-   <span data-ttu-id="750b2-146">**GroupOperationID** indique la séquence dans laquelle l’événement se produit.</span><span class="sxs-lookup"><span data-stu-id="750b2-146">**GroupOperationID** indicates the sequence in which the event occurs.</span></span>
-   <span data-ttu-id="750b2-147">**ProviderName** indique le nom du fournisseur qui fournit les données.</span><span class="sxs-lookup"><span data-stu-id="750b2-147">**ProviderName** indicates the name of the provider which supplies the data.</span></span>
-   <span data-ttu-id="750b2-148">**Path** est le chemin d’accès WMI de l’objet.</span><span class="sxs-lookup"><span data-stu-id="750b2-148">**Path** is the WMI path to the object.</span></span>

<span data-ttu-id="750b2-149">Par exemple, l’opération peut être une énumération [**de \_ service Win32**](/windows/desktop/CIMWin32Prov/win32-service).</span><span class="sxs-lookup"><span data-stu-id="750b2-149">For example, the operation may be an enumeration of [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span>

</dd> <dt>

<span data-ttu-id="750b2-150"><span id="Event_3"></span><span id="event_3"></span><span id="EVENT_3"></span>Événement 3</span><span class="sxs-lookup"><span data-stu-id="750b2-150"><span id="Event_3"></span><span id="event_3"></span><span id="EVENT_3"></span>Event 3</span></span>
</dt> <dd>

<span data-ttu-id="750b2-151">Fin de la séquence d’événements pour une opération spécifique.</span><span class="sxs-lookup"><span data-stu-id="750b2-151">End of the event sequence for a specific operation.</span></span> <span data-ttu-id="750b2-152">Une occurrence pour chaque séquence.</span><span class="sxs-lookup"><span data-stu-id="750b2-152">One occurrence for each sequence.</span></span>

<span data-ttu-id="750b2-153">Seul le **GroupOperationID** est affiché.</span><span class="sxs-lookup"><span data-stu-id="750b2-153">Only the **GroupOperationID** is shown.</span></span>

</dd> </dl>

## <a name="enabling-wmi-tracing-at-command-prompt"></a><span data-ttu-id="750b2-154">Activation du suivi WMI à l’invite de commandes</span><span class="sxs-lookup"><span data-stu-id="750b2-154">Enabling WMI Tracing at Command Prompt</span></span>

<span data-ttu-id="750b2-155">Vous pouvez également activer le suivi d’événements WMI via l’outil en ligne de commande Wevtutil.</span><span class="sxs-lookup"><span data-stu-id="750b2-155">You can also enable WMI event tracing through the Wevtutil command-line tool.</span></span> <span data-ttu-id="750b2-156">Utilisez la commande suivante : **Wevtutil.exe SL Microsoft-Windows-WMI-Activity/trace/e : true**.</span><span class="sxs-lookup"><span data-stu-id="750b2-156">Use the following command: **Wevtutil.exe sl Microsoft-Windows-WMI-Activity/Trace /e:true**.</span></span> <span data-ttu-id="750b2-157">La source d’événement WMI est Microsoft-Windows-WMI.</span><span class="sxs-lookup"><span data-stu-id="750b2-157">The WMI event source is Microsoft-Windows-WMI.</span></span> <span data-ttu-id="750b2-158">Pour plus d’informations sur la Wevtutil.exe, consultez [à propos du journal des événements Windows](/previous-versions//aa382610(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="750b2-158">For more information about Wevtutil.exe, see [About Windows Event Log](/previous-versions//aa382610(v=vs.85)).</span></span>

## <a name="using-wpp-based-wmi-tracing"></a><span data-ttu-id="750b2-159">Utilisation du suivi WMI basé sur WPP</span><span class="sxs-lookup"><span data-stu-id="750b2-159">Using WPP-based WMI Tracing</span></span>

<span data-ttu-id="750b2-160">Dans les systèmes d’exploitation Windows à compter de Windows Vista, WMI crée un canal de trace actif pendant le processus de démarrage.</span><span class="sxs-lookup"><span data-stu-id="750b2-160">In Windows operating systems starting with Windows Vista, WMI creates an active trace channel during the boot process.</span></span> <span data-ttu-id="750b2-161">Le nom du canal est session de \_ suivi WMI \_ .</span><span class="sxs-lookup"><span data-stu-id="750b2-161">The name of the channel is WMI\_Trace\_Session.</span></span> <span data-ttu-id="750b2-162">Seules les erreurs sont enregistrées dans le canal.</span><span class="sxs-lookup"><span data-stu-id="750b2-162">Only errors are logged to the channel.</span></span>

<span data-ttu-id="750b2-163">Le préprocesseur de suivi logiciel Windows enregistre les informations dans un fichier binaire.</span><span class="sxs-lookup"><span data-stu-id="750b2-163">The Windows software trace preprocessor (WPP) records information in a binary file.</span></span> <span data-ttu-id="750b2-164">Pour lire le fichier, vous devez d’abord le convertir au format texte lisible.</span><span class="sxs-lookup"><span data-stu-id="750b2-164">To read the file, you must first translate it into a readable, text format.</span></span> <span data-ttu-id="750b2-165">Vous utilisez un outil appelé tracefmt.exe à partir du [Kit de pilotes Windows (WDK)](https://www.microsoft.com/whdc/DevTools/WDK/WDKpkg.mspx) pour effectuer la traduction.</span><span class="sxs-lookup"><span data-stu-id="750b2-165">You use a tool called tracefmt.exe from the [Windows Driver Kit (WDK)](https://www.microsoft.com/whdc/DevTools/WDK/WDKpkg.mspx) to do the translation.</span></span> <span data-ttu-id="750b2-166">L’outil nécessite des informations stockées dans certains fichiers associés.</span><span class="sxs-lookup"><span data-stu-id="750b2-166">The tool requires information stored in some associated files.</span></span> <span data-ttu-id="750b2-167">Les fichiers se trouvent dans le répertoire% SystemRoot% \\ system32 \\ WBEM \\ TMF et ont une extension de nom de fichier. TMF.</span><span class="sxs-lookup"><span data-stu-id="750b2-167">The files are located in the %SystemRoot%\\System32\\wbem\\tmf directory and have a .tmf file name extension.</span></span> <span data-ttu-id="750b2-168">L’outil requiert en fait un seul fichier. TMF.</span><span class="sxs-lookup"><span data-stu-id="750b2-168">The tool actually requires a single .tmf file .</span></span> <span data-ttu-id="750b2-169">Vous créez ce fichier unique en concaténant tous les fichiers. TMF dans un autre fichier. TMF.</span><span class="sxs-lookup"><span data-stu-id="750b2-169">You make that single file by concatenating all of the .tmf files into another .tmf file.</span></span> <span data-ttu-id="750b2-170">Pour plus d’informations sur les fichiers. TMF, consultez [fichier de format de message de trace](/windows-hardware/drivers/devtest/trace-message-format-file).</span><span class="sxs-lookup"><span data-stu-id="750b2-170">For more information about .tmf files, see [Trace Message Format File](/windows-hardware/drivers/devtest/trace-message-format-file).</span></span>

<span data-ttu-id="750b2-171">Après avoir installé le [Kit de pilotes Windows (WDK)](https://www.microsoft.com/whdc/DevTools/WDK/WDKpkg.mspx) pour obtenir les outils en ligne de commande tracelog.exe et tracefmt.exe, procédez comme suit pour collecter un suivi WMI basé sur WPP.</span><span class="sxs-lookup"><span data-stu-id="750b2-171">After installing the [Windows Driver Kit (WDK)](https://www.microsoft.com/whdc/DevTools/WDK/WDKpkg.mspx) to get the tracelog.exe and tracefmt.exe command-line tools, perform the following steps to collect a WPP-based WMI trace.</span></span>

<span data-ttu-id="750b2-172">**Pour afficher une trace WMI basée sur WPP**</span><span class="sxs-lookup"><span data-stu-id="750b2-172">**To view a WPP-based WMI trace**</span></span>

1.  <span data-ttu-id="750b2-173">Pour créer le fichier. TMF unique, ouvrez une fenêtre d’invite de commandes avec élévation de privilèges et accédez au répertoire% SystemRoot% \\ system32 \\ WBEM \\ TMF.</span><span class="sxs-lookup"><span data-stu-id="750b2-173">To create the single .tmf file, open an elevated Command Prompt window and navigate to the %SystemRoot%\\System32\\wbem\\tmf directory.</span></span>

2.  <span data-ttu-id="750b2-174">Tapez **Copy/y% systemroot% \\ system32 \\ WBEM \\ TMF \\ \* . TMF% systemroot% \\ system32 \\ WBEM \\ TMF \\ WMI. TMF**.</span><span class="sxs-lookup"><span data-stu-id="750b2-174">Type **copy /y %SystemRoot%\\System32\\wbem\\tmf\\\*.tmf %SystemRoot%\\System32\\wbem\\tmf\\wmi.tmf**.</span></span> <span data-ttu-id="750b2-175">Cette opération crée un fichier nommé WMI. TMF qui comprend le contenu de tous les autres fichiers. TMF.</span><span class="sxs-lookup"><span data-stu-id="750b2-175">This will create a file named wmi.tmf that includes the contents of all of the other .tmf files.</span></span>

3.  <span data-ttu-id="750b2-176">Tapez **tracelog-Flush \_ \_ session de trace WMI**.</span><span class="sxs-lookup"><span data-stu-id="750b2-176">Type **tracelog -flush WMI\_Trace\_Session**.</span></span> <span data-ttu-id="750b2-177">Les tampons WPP sont vidés sur le disque.</span><span class="sxs-lookup"><span data-stu-id="750b2-177">This will flush the WPP buffers on the disk.</span></span>
4.  <span data-ttu-id="750b2-178">**Définir le \_ préfixe du format de trace \_ = \[ %9 ! d ! \] %8 ! 04X !. %3 ! 04X !. %3 ! 04X !:: %4 ! s ! \[ %1 ! s ! \] (%! ... :% ! FUNC !: %2 ! s !)**.</span><span class="sxs-lookup"><span data-stu-id="750b2-178">Type **set TRACE\_FORMAT\_PREFIX = \[%9!d!\]%8!04X!.%3!04X!.%3!04X!::%4!s!\[%1!s!\](%!COMPNAME!:%!FUNC !:%2!s!)**.</span></span> <span data-ttu-id="750b2-179">L’outil tracefmt ajoute des informations par défaut à chaque message de suivi.</span><span class="sxs-lookup"><span data-stu-id="750b2-179">The tracefmt tool adds some default information to each trace message.</span></span> <span data-ttu-id="750b2-180">Vous pouvez configurer les informations incluses en définissant la \_ variable d’environnement de préfixe de format de trace \_ .</span><span class="sxs-lookup"><span data-stu-id="750b2-180">You can configure what information is included by setting the TRACE\_FORMAT\_PREFIX environment variable.</span></span> <span data-ttu-id="750b2-181">Pour en savoir plus sur la syntaxe utilisée, consultez [préfixe du message de suivi](https://msdn.microsoft.com/library/aa139695.aspx).</span><span class="sxs-lookup"><span data-stu-id="750b2-181">To learn about the syntax used, see [Trace Message Prefix](https://msdn.microsoft.com/library/aa139695.aspx).</span></span>
5.  <span data-ttu-id="750b2-182">Tapez **tracefmt-TMF% systemroot% \\ system32 \\ WBEM \\ TMF \\ wmi. TMF-o OUTPUT.TXT% systemroot% \\ system32 \\ WBEM \\ journaliss \\ WMITracing. log**.</span><span class="sxs-lookup"><span data-stu-id="750b2-182">Type **tracefmt -tmf %systemroot%\\system32\\wbem\\tmf\\wmi.tmf -o OUTPUT.TXT %systemroot%\\system32\\wbem\\logs\\WMITracing.log**.</span></span> <span data-ttu-id="750b2-183">Cela effectue la conversion du format binaire au format texte lisible.</span><span class="sxs-lookup"><span data-stu-id="750b2-183">This performs the translation from binary format to readable text format.</span></span>
6.  <span data-ttu-id="750b2-184">Tapez **Notepad% systemroot% \\ system32 \\ WBEM \\ TMF \\OUTPUT.TXT**.</span><span class="sxs-lookup"><span data-stu-id="750b2-184">Type **notepad %systemroot%\\system32\\wbem\\tmf\\OUTPUT.TXT**.</span></span> <span data-ttu-id="750b2-185">Le fichier de trace s’ouvre dans le bloc-notes.</span><span class="sxs-lookup"><span data-stu-id="750b2-185">This will open the trace file in Notepad.</span></span>

<span data-ttu-id="750b2-186">Voici d’autres tâches liées au WPP que vous devrez peut-être effectuer.</span><span class="sxs-lookup"><span data-stu-id="750b2-186">The following are some other WPP-related tasks you might need to perform.</span></span>

<span data-ttu-id="750b2-187">**Pour arrêter le suivi WMI basé sur WPP**</span><span class="sxs-lookup"><span data-stu-id="750b2-187">**To stop WPP-based WMI tracing**</span></span>

-   <span data-ttu-id="750b2-188">Tapez **tracelog-arrêter la \_ \_ session de trace WMI**.</span><span class="sxs-lookup"><span data-stu-id="750b2-188">Type **tracelog -stop WMI\_Trace\_Session**.</span></span>

<span data-ttu-id="750b2-189">**Pour démarrer le suivi WMI basé sur WPP**</span><span class="sxs-lookup"><span data-stu-id="750b2-189">**To start WPP-based WMI tracing**</span></span>

-   <span data-ttu-id="750b2-190">Tapez **tracelog-Start WMI \_ trace \_ session-GUID \# 1FF6B227-2CA7-40F9-9A66-980EADAA602E-RT-niveau 5-Flag 0x7-f MYTRACE. EMPLACEMENT**</span><span class="sxs-lookup"><span data-stu-id="750b2-190">Type **tracelog -start WMI\_Trace\_Session -guid \#1FF6B227-2CA7-40f9-9A66-980EADAA602E -rt -level 5 -flag 0x7 -f MYTRACE.BIN**</span></span>

<span data-ttu-id="750b2-191">**Windows Vista :** Par défaut, le suivi WMI basé sur WPP est défini sur le niveau 2, ce qui comprend uniquement les messages d’erreur.</span><span class="sxs-lookup"><span data-stu-id="750b2-191">**Windows Vista:** By default, WPP-based WMI tracing is set to level 2 which includes only error messages.</span></span> <span data-ttu-id="750b2-192">Pour inclure également des messages d’information, définissez le niveau sur 4.</span><span class="sxs-lookup"><span data-stu-id="750b2-192">To include informational messages as well, set the level to 4.</span></span> <span data-ttu-id="750b2-193">Toutes les zones de WMI sont suivies par défaut.</span><span class="sxs-lookup"><span data-stu-id="750b2-193">All areas of WMI are traced by default.</span></span> <span data-ttu-id="750b2-194">Il existe trois zones distinctes qui peuvent être suivies : Core (indicateur = 0x1), ESS (indicateur = 0X2) et PROV (indicateur = 0x4).</span><span class="sxs-lookup"><span data-stu-id="750b2-194">There are three distinct areas that can be traced: Core (flag=0x1), ESS (flag=0x2) and Prov (flag=0x4).</span></span> <span data-ttu-id="750b2-195">Dans la commande de démarrage ci-dessus, l' **indicateur 0x7** entraîne le suivi de ces trois zones.</span><span class="sxs-lookup"><span data-stu-id="750b2-195">In the start command above, **flag 0x7** causes all three areas to be traced.</span></span>

<span data-ttu-id="750b2-196">**Windows 7 :** Par défaut, le suivi WMI basé sur WPP est désactivé et défini sur le niveau 0.</span><span class="sxs-lookup"><span data-stu-id="750b2-196">**Windows 7:** By default, WPP-based WMI tracing is disabled and set to level 0.</span></span> <span data-ttu-id="750b2-197">Pour utiliser le suivi WMI basé sur WPP, cette fonctionnalité doit être activée et définie sur le niveau 2 pour les messages d’erreur ou sur le niveau 4 pour les messages d’erreur et d’information.</span><span class="sxs-lookup"><span data-stu-id="750b2-197">To use WPP-based WMI tracing, this feature must be enabled and set to either level 2 for error messages or level 4 for both error and informational messages.</span></span>

<span data-ttu-id="750b2-198">**Pour répertorier toutes les sessions de suivi WPP**</span><span class="sxs-lookup"><span data-stu-id="750b2-198">**To list all WPP trace sessions**</span></span>

-   <span data-ttu-id="750b2-199">Tapez **tracelog-l**.</span><span class="sxs-lookup"><span data-stu-id="750b2-199">Type **tracelog -l**.</span></span>

<span data-ttu-id="750b2-200">**Pour répertorier les informations relatives à la session de trace WMI WPP**</span><span class="sxs-lookup"><span data-stu-id="750b2-200">**To list info about the WMI WPP trace session**</span></span>

-   <span data-ttu-id="750b2-201">Tapez **tracelog-l \| findstr/i "WMI \_ trace"**.</span><span class="sxs-lookup"><span data-stu-id="750b2-201">Type **tracelog -l \| findstr /i "wmi\_trace"**.</span></span>

<span data-ttu-id="750b2-202">**Pour afficher les paramètres de session de suivi WPP WMI**</span><span class="sxs-lookup"><span data-stu-id="750b2-202">**To view the WMI WPP trace session parameters**</span></span>

-   <span data-ttu-id="750b2-203">Tapez **\_ \_ session de trace WMI tracelog-q**.</span><span class="sxs-lookup"><span data-stu-id="750b2-203">Type **tracelog -q WMI\_Trace\_Session**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="750b2-204">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="750b2-204">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="750b2-205">Résolution des problèmes WMI</span><span class="sxs-lookup"><span data-stu-id="750b2-205">WMI Troubleshooting</span></span>](wmi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="750b2-206">Fichiers journaux WMI</span><span class="sxs-lookup"><span data-stu-id="750b2-206">WMI Log Files</span></span>](wmi-log-files.md)
</dt> </dl>

 

 
