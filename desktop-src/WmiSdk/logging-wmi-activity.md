---
description: Les fichiers journaux WMI ne sont plus pris en charge.
ms.assetid: 4ba80063-7aa6-42df-a620-1b366b795034
ms.tgt_platform: multiple
title: Journalisation de l’activité WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6ced8645eb7ad9005e6ba751d011ae7f0ccb3dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527665"
---
# <a name="logging-wmi-activity"></a><span data-ttu-id="bbab7-103">Journalisation de l’activité WMI</span><span class="sxs-lookup"><span data-stu-id="bbab7-103">Logging WMI Activity</span></span>

<span data-ttu-id="bbab7-104">Les fichiers journaux WMI ne sont plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="bbab7-104">The WMI log files are no longer supported.</span></span> <span data-ttu-id="bbab7-105">À compter de Windows Vista, WMI utilise [suivi d’v nements pour Windows (ETW](/windows/desktop/ETW/event-tracing-portal)) et les événements qui sont disponibles via l’interface utilisateur **Observateur d’événements** ou l’outil en ligne de commande Wevtutil.</span><span class="sxs-lookup"><span data-stu-id="bbab7-105">Starting with Windows Vista, WMI uses [Event Tracing for Windows (ETW](/windows/desktop/ETW/event-tracing-portal)) and events that are available through the **Event Viewer** UI or the Wevtutil command line tool.</span></span> <span data-ttu-id="bbab7-106">Pour plus d’informations, consultez le fournisseur ETW et la documentation de la ligne de commande [wevutil](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc732848(v=ws.11)) .</span><span class="sxs-lookup"><span data-stu-id="bbab7-106">For more information, see the ETW provider and the [Wevutil](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc732848(v=ws.11)) command-line documentation.</span></span>

<span data-ttu-id="bbab7-107">Les sections suivantes sont présentées dans cette rubrique :</span><span class="sxs-lookup"><span data-stu-id="bbab7-107">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="bbab7-108">Fichiers journaux WMI avant Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bbab7-108">WMI Log Files Before Windows Vista</span></span>](#wmi-log-files-before-windows-vista)
-   [<span data-ttu-id="bbab7-109">Journalisation des activités pour les composants WMI Core avant Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bbab7-109">Logging Activities for WMI Core Components Before Windows Vista</span></span>](#logging-activities-for-wmi-core-components-before-windows-vista)
-   [<span data-ttu-id="bbab7-110">Journalisation des activités pour les composants du fournisseur WMI avant Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bbab7-110">Logging Activities for WMI Provider Components Before Windows Vista</span></span>](#logging-activities-for-wmi-provider-components-before-windows-vista)
-   [<span data-ttu-id="bbab7-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bbab7-111">Related topics</span></span>](#related-topics)

## <a name="wmi-log-files-before-windows-vista"></a><span data-ttu-id="bbab7-112">Fichiers journaux WMI avant Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bbab7-112">WMI Log Files Before Windows Vista</span></span>

<span data-ttu-id="bbab7-113">Les fichiers journaux créés par WMI et différents fournisseurs enregistrent les événements, les données de trace ou de diagnostic, les erreurs et diverses activités.</span><span class="sxs-lookup"><span data-stu-id="bbab7-113">The log files created by WMI and various providers record: events, trace or diagnostic data, errors, and various activities.</span></span> <span data-ttu-id="bbab7-114">Seuls les administrateurs ont accès en lecture au dossier du journal WMI situé dans les \\ journaux WBEM% windir% system32 \\ \\ .</span><span class="sxs-lookup"><span data-stu-id="bbab7-114">Only administrators have read access to the WMI log folder found at %windir%\\system32\\wbem\\logs.</span></span>

<span data-ttu-id="bbab7-115">Seuls les composants WMI Core ou les fournisseurs WMI écrivent dans les fichiers journaux.</span><span class="sxs-lookup"><span data-stu-id="bbab7-115">Only WMI core components or WMI providers write to log files.</span></span> <span data-ttu-id="bbab7-116">Vous pouvez uniquement lire ou afficher les données de ces journaux à des fins de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="bbab7-116">You can only read or view the data in these logs for diagnostic purposes.</span></span> <span data-ttu-id="bbab7-117">Vous pouvez créer et stocker vos propres fichiers journaux dans le répertoire des journaux WMI.</span><span class="sxs-lookup"><span data-stu-id="bbab7-117">You can create and store your own log files in the WMI log directory.</span></span>

## <a name="logging-activities-for-wmi-core-components-before-windows-vista"></a><span data-ttu-id="bbab7-118">Journalisation des activités pour les composants WMI Core avant Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bbab7-118">Logging Activities for WMI Core Components Before Windows Vista</span></span>

<span data-ttu-id="bbab7-119">Ces fichiers ne contiennent pas un format cohérent qui convient pour la lecture par programme.</span><span class="sxs-lookup"><span data-stu-id="bbab7-119">These files do not contain a consistent format that is suitable for reading programmatically.</span></span> <span data-ttu-id="bbab7-120">Pour plus d’informations sur des journaux spécifiques, consultez [fichiers journaux WMI](wmi-log-files.md).</span><span class="sxs-lookup"><span data-stu-id="bbab7-120">For more information about specific logs, see [WMI Log Files](wmi-log-files.md).</span></span>

<span data-ttu-id="bbab7-121">Les activités de journalisation pour les composants WMI Core se produisent lorsque les clés de Registre suivantes sont définies :</span><span class="sxs-lookup"><span data-stu-id="bbab7-121">Logging activities for WMI core components occurs when the following registry keys are set:</span></span>

-   <span data-ttu-id="bbab7-122">Niveau de journalisation</span><span class="sxs-lookup"><span data-stu-id="bbab7-122">Logging level</span></span>

    <span data-ttu-id="bbab7-123">Les modifications apportées à la valeur de Registre du niveau de journalisation prennent effet immédiatement.</span><span class="sxs-lookup"><span data-stu-id="bbab7-123">Changes to the logging level registry value take effect immediately.</span></span> <span data-ttu-id="bbab7-124">Aucun redémarrage du service WMI n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="bbab7-124">No restart of the WMI service is necessary.</span></span>

    <span data-ttu-id="bbab7-125">**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\  \\  \\  \\ **journalisation** CIMOM Microsoft WBEM = 2</span><span class="sxs-lookup"><span data-stu-id="bbab7-125">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**Logging** = 2</span></span>

    <span data-ttu-id="bbab7-126">La liste suivante répertorie les niveaux de journalisation qui peuvent être définis dans le registre.</span><span class="sxs-lookup"><span data-stu-id="bbab7-126">The following list lists the logging levels that can be defined in the registry.</span></span>

    

    | <span data-ttu-id="bbab7-127">Niveau de journalisation</span><span class="sxs-lookup"><span data-stu-id="bbab7-127">Logging level</span></span> | <span data-ttu-id="bbab7-128">Description</span><span class="sxs-lookup"><span data-stu-id="bbab7-128">Description</span></span>               |
    |---------------|---------------------------|
    | <span data-ttu-id="bbab7-129">0</span><span class="sxs-lookup"><span data-stu-id="bbab7-129">0</span></span>             | <span data-ttu-id="bbab7-130">Aucune journalisation</span><span class="sxs-lookup"><span data-stu-id="bbab7-130">No Logging</span></span>                |
    | <span data-ttu-id="bbab7-131">1</span><span class="sxs-lookup"><span data-stu-id="bbab7-131">1</span></span>             | <span data-ttu-id="bbab7-132">Journaliser uniquement les erreurs</span><span class="sxs-lookup"><span data-stu-id="bbab7-132">Log only errors</span></span>           |
    | <span data-ttu-id="bbab7-133">2</span><span class="sxs-lookup"><span data-stu-id="bbab7-133">2</span></span>             | <span data-ttu-id="bbab7-134">Journalisation détaillée (par défaut)</span><span class="sxs-lookup"><span data-stu-id="bbab7-134">Verbose Logging (default)</span></span> |

    

     

-   <span data-ttu-id="bbab7-135">Emplacement du fichier journal</span><span class="sxs-lookup"><span data-stu-id="bbab7-135">Log file location</span></span>

    <span data-ttu-id="bbab7-136">Pour que les modifications apportées à l’emplacement du fichier journal prennent effet, redémarrez le service WMI.</span><span class="sxs-lookup"><span data-stu-id="bbab7-136">For changes to log file location to take effect, restart the WMI service.</span></span>

    <span data-ttu-id="bbab7-137">**HKEY \_ Logiciel d' \_ ordinateur local** répertoire de \\  \\  \\  \\  \\ **journalisation** CIMOM Microsoft WBEM =% windir% \\ system32 \\ \\ journaux WBEM</span><span class="sxs-lookup"><span data-stu-id="bbab7-137">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**Logging Directory** = %windir%\\system32\\wbem\\logs</span></span>

-   <span data-ttu-id="bbab7-138">Taille maximale du fichier journal, en octets</span><span class="sxs-lookup"><span data-stu-id="bbab7-138">Maximum log file size, in bytes</span></span>

    <span data-ttu-id="bbab7-139">**HKEY \_ \_Ordinateur local** \\ **logiciel** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **fichier journal CIMOM taille maximale** = 65536</span><span class="sxs-lookup"><span data-stu-id="bbab7-139">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**Log File Max Size** = 65536</span></span>

<span data-ttu-id="bbab7-140">Vous pouvez modifier ces valeurs de clé de Registre par le biais de l’éditeur du registre ou via le composant logiciel enfichable WMI de la console MMC (Microsoft Management Console).</span><span class="sxs-lookup"><span data-stu-id="bbab7-140">You can change these registry key values through the Registry Editor or through the WMI snap-in for the Microsoft Management Console.</span></span>

<span data-ttu-id="bbab7-141">**Pour définir le niveau de journalisation pour WMI avant Windows Vista**</span><span class="sxs-lookup"><span data-stu-id="bbab7-141">**To set the logging level for WMI before Windows Vista**</span></span>

1.  <span data-ttu-id="bbab7-142">Cliquez sur **Démarrer**, puis sur **Exécuter**.</span><span class="sxs-lookup"><span data-stu-id="bbab7-142">Click **Start**, and then click **Run**.</span></span>
2.  <span data-ttu-id="bbab7-143">Tapez **wmimgmt. msc**</span><span class="sxs-lookup"><span data-stu-id="bbab7-143">Type **wmimgmt.msc**</span></span>
3.  <span data-ttu-id="bbab7-144">Dans le menu **Action**, cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="bbab7-144">On the **Action** menu, click **Properties**.</span></span>
4.  <span data-ttu-id="bbab7-145">Sous l’onglet **journalisation** , définissez le niveau de journalisation sur **désactivé**, **activé** ou **détaillé**.</span><span class="sxs-lookup"><span data-stu-id="bbab7-145">On the **Logging** tab, set the logging level to **Disabled**, **Enabled**, or **Verbose**.</span></span>
5.  <span data-ttu-id="bbab7-146">Dans **emplacement :**, tapez le chemin d’accès au dossier du fichier journal et, dans **taille maximale (octets) :**, définissez la taille maximale, en octets, du fichier journal.</span><span class="sxs-lookup"><span data-stu-id="bbab7-146">In **Location:**, type the path to the log file folder and in **Maximum size (bytes):**, set the maximum size, in bytes, of the log file.</span></span>

<span data-ttu-id="bbab7-147">Pour plus d’informations sur la définition des propriétés du fichier journal, consultez l’aide en ligne de l’application de contrôle WMI.</span><span class="sxs-lookup"><span data-stu-id="bbab7-147">For more information about setting the log file properties, see the online Help for the WMI Control application.</span></span>

## <a name="logging-activities-for-wmi-provider-components-before-windows-vista"></a><span data-ttu-id="bbab7-148">Journalisation des activités pour les composants du fournisseur WMI avant Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bbab7-148">Logging Activities for WMI Provider Components Before Windows Vista</span></span>

<span data-ttu-id="bbab7-149">Lorsque la journalisation des composants principaux de WMI est activée, l’enregistrement est également activé pour n’importe quel fournisseur avec des fonctionnalités de journalisation.</span><span class="sxs-lookup"><span data-stu-id="bbab7-149">When logging for WMI core components is enabled, logging is also enabled for any provider with logging capabilities.</span></span>

<span data-ttu-id="bbab7-150">La liste suivante répertorie les valeurs requises.</span><span class="sxs-lookup"><span data-stu-id="bbab7-150">The following list lists the required values.</span></span>

<dl> <dt>

<span data-ttu-id="bbab7-151"><span id="File"></span><span id="file"></span><span id="FILE"></span>**Txt**</span><span class="sxs-lookup"><span data-stu-id="bbab7-151"><span id="File"></span><span id="file"></span><span id="FILE"></span>**File**</span></span>
</dt> <dd>

<span data-ttu-id="bbab7-152">Chemin d’accès complet et nom de fichier du fichier journal.</span><span class="sxs-lookup"><span data-stu-id="bbab7-152">Full path and file name of the log file.</span></span> <span data-ttu-id="bbab7-153">La valeur par défaut est% windir% \\ system32 \\ WBEM \\ logs.</span><span class="sxs-lookup"><span data-stu-id="bbab7-153">The default value is %windir%\\system32\\wbem\\logs.</span></span> <span data-ttu-id="bbab7-154">La valeur nommée du **type** doit être définie sur = file pour cette valeur nommée à utiliser.</span><span class="sxs-lookup"><span data-stu-id="bbab7-154">The **Type** named value must be set to = File for this named value to be used.</span></span>

</dd> <dt>

<span data-ttu-id="bbab7-155"><span id="Level"></span><span id="level"></span><span id="LEVEL"></span>**Niveau**</span><span class="sxs-lookup"><span data-stu-id="bbab7-155"><span id="Level"></span><span id="level"></span><span id="LEVEL"></span>**Level**</span></span>
</dt> <dd>

<span data-ttu-id="bbab7-156">Masque logique 32 bits qui définit le type de sortie de débogage générée par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="bbab7-156">A 32-bit logical mask that defines the type of debugging output generated by the provider.</span></span> <span data-ttu-id="bbab7-157">Cette valeur dépend du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="bbab7-157">This value is provider-dependent.</span></span> <span data-ttu-id="bbab7-158">La valeur par défaut est 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="bbab7-158">The default value is 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="bbab7-159"><span id="MaxFileSize"></span><span id="maxfilesize"></span><span id="MAXFILESIZE"></span>**MaxFileSize**</span><span class="sxs-lookup"><span data-stu-id="bbab7-159"><span id="MaxFileSize"></span><span id="maxfilesize"></span><span id="MAXFILESIZE"></span>**MaxFileSize**</span></span>
</dt> <dd>

<span data-ttu-id="bbab7-160">Taille de fichier maximale, en octets, du fichier journal.</span><span class="sxs-lookup"><span data-stu-id="bbab7-160">Maximum file size, in bytes, of the log file.</span></span> <span data-ttu-id="bbab7-161">Cette valeur entière doit être comprise entre 1024 et 2 ^ 32-1.</span><span class="sxs-lookup"><span data-stu-id="bbab7-161">This integer value must be in the range 1024 to 2^32-1.</span></span> <span data-ttu-id="bbab7-162">Lorsque la taille du fichier dépasse cette valeur, le fichier est renommé en **~ filename** et un nouveau fichier journal vide est créé.</span><span class="sxs-lookup"><span data-stu-id="bbab7-162">When the file size exceeds this value, the file is renamed to **~filename** and a new, empty log file is created.</span></span> <span data-ttu-id="bbab7-163">L’espace disque requis pour le fichier journal est le double de la valeur de **MaxFileSize**.</span><span class="sxs-lookup"><span data-stu-id="bbab7-163">The disk space required for the log file is twice the value of **MaxFileSize**.</span></span> <span data-ttu-id="bbab7-164">La valeur par défaut est 65 535.</span><span class="sxs-lookup"><span data-stu-id="bbab7-164">The default value is 65,535.</span></span>

</dd> <dt>

<span data-ttu-id="bbab7-165"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Entrer**</span><span class="sxs-lookup"><span data-stu-id="bbab7-165"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Type**</span></span>
</dt> <dd>

<span data-ttu-id="bbab7-166">Peut avoir la valeur = file ou = Debugger.</span><span class="sxs-lookup"><span data-stu-id="bbab7-166">Can be set to = File or = Debugger.</span></span> <span data-ttu-id="bbab7-167">Si la valeur est = file, les informations de trace sont écrites dans le fichier journal spécifié dans le **fichier** nommé value.</span><span class="sxs-lookup"><span data-stu-id="bbab7-167">If set to = File, the trace information is written to the log file specified in the **File** named value.</span></span> <span data-ttu-id="bbab7-168">La valeur par défaut est = file.</span><span class="sxs-lookup"><span data-stu-id="bbab7-168">The default value is = File.</span></span>

</dd> </dl>

<span data-ttu-id="bbab7-169">Par exemple, pour consigner une requête et obtenir des appels d’instance à partir du fournisseur de vues, utilisez les valeurs de clés de Registre suivantes.</span><span class="sxs-lookup"><span data-stu-id="bbab7-169">For example, to log query and get instance calls from the View Provider, use the following registry key values.</span></span> <span data-ttu-id="bbab7-170">Le journal se trouvera dans le dossier log et sera la taille de fichier par défaut.</span><span class="sxs-lookup"><span data-stu-id="bbab7-170">The log will be located in the log folder and will be the default file size.</span></span>

<span data-ttu-id="bbab7-171">**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\  \\ connexion des fournisseurs WBEM Microsoft \\  \\  \\ **ViewProvider** \\ **fichier** = C : \\ Windows \\ system32 \\ WBEM \\ journaux \\ ViewProvider. log</span><span class="sxs-lookup"><span data-stu-id="bbab7-171">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**PROVIDERS**\\**Logging**\\**ViewProvider**\\**File** = C:\\Windows\\system32\\WBEM\\Logs\\ViewProvider.log</span></span>

<span data-ttu-id="bbab7-172">**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\  \\ connexion des fournisseurs **WBEM Microsoft WBEM** \\  \\  \\  \\ **niveau** ViewProvider = 2</span><span class="sxs-lookup"><span data-stu-id="bbab7-172">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**PROVIDERS**\\**Logging**\\**ViewProvider**\\**Level** = 2</span></span>

<span data-ttu-id="bbab7-173">**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\  \\ connexion des fournisseurs WBEM Microsoft \\  \\  \\ **ViewProvider** \\ **MaxFileSize** = 65535</span><span class="sxs-lookup"><span data-stu-id="bbab7-173">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**PROVIDERS**\\**Logging**\\**ViewProvider**\\**MaxFileSize** = 65535</span></span>

<span data-ttu-id="bbab7-174">**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\  \\  \\ journalisation des **fournisseurs** Microsoft WBEM \\  \\ **ViewProvider** \\ **type** = fichier</span><span class="sxs-lookup"><span data-stu-id="bbab7-174">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**PROVIDERS**\\**Logging**\\**ViewProvider**\\**Type** = File</span></span>

> [!Note]  
> <span data-ttu-id="bbab7-175">Pour vos propres fournisseurs avec des fonctionnalités de journalisation, vous devez écrire les clés et valeurs de Registre nécessaires pour activer la journalisation.</span><span class="sxs-lookup"><span data-stu-id="bbab7-175">For your own providers with logging capabilities, you need to write the necessary registry keys and values to enable logging.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="bbab7-176">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bbab7-176">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbab7-177">Résolution des problèmes WMI</span><span class="sxs-lookup"><span data-stu-id="bbab7-177">WMI Troubleshooting</span></span>](wmi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="bbab7-178">Fichiers journaux WMI</span><span class="sxs-lookup"><span data-stu-id="bbab7-178">WMI Log Files</span></span>](wmi-log-files.md)
</dt> <dt>

[<span data-ttu-id="bbab7-179">Classes de résolution des problèmes WMI</span><span class="sxs-lookup"><span data-stu-id="bbab7-179">WMI Troubleshooting Classes</span></span>](wmi-troubleshooting-classes.md)
</dt> <dt>

[<span data-ttu-id="bbab7-180">Suivi de l’activité WMI</span><span class="sxs-lookup"><span data-stu-id="bbab7-180">Tracing WMI Activity</span></span>](tracing-wmi-activity.md)
</dt> </dl>

 

 
