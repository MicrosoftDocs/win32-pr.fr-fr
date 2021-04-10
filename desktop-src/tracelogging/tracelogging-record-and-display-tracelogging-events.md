---
title: Enregistrer et afficher les événements TraceLogging
description: Enregistrez les événements TraceLogging avec l’enregistreur de performances Windows (WPR) et affichez-les à l’aide de l’analyseur de performances Windows (WPA).
ms.assetid: 906589FA-F48D-4105-9E56-1EC8B86542FB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09be054d274fc2c2c62635cc7bf12e8cf8acdef3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842685"
---
# <a name="record-and-view-tracelogging-events"></a><span data-ttu-id="b456d-103">Enregistrer et afficher les événements TraceLogging</span><span class="sxs-lookup"><span data-stu-id="b456d-103">Record and View TraceLogging Events</span></span>

<span data-ttu-id="b456d-104">Enregistrez les événements TraceLogging avec l’enregistreur de performances Windows (WPR) et affichez-les à l’aide de l’analyseur de performances Windows (WPA).</span><span class="sxs-lookup"><span data-stu-id="b456d-104">Record TraceLogging events with the Windows Performance Recorder (WPR) and view them with the Windows Performance Analyzer (WPA).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b456d-105">Prérequis</span><span class="sxs-lookup"><span data-stu-id="b456d-105">Prerequisites</span></span>

-   <span data-ttu-id="b456d-106">Windows 10</span><span class="sxs-lookup"><span data-stu-id="b456d-106">Windows 10</span></span>
-   <span data-ttu-id="b456d-107">La version Windows 10 de l’enregistreur de performances Windows (WPR) et la version Windows 10 de Windows Performance Analyzer (WPA) qui fait partie du kit de déploiement et d’évaluation Windows® (Windows ADK).</span><span class="sxs-lookup"><span data-stu-id="b456d-107">The Windows 10 version of Windows Performance Recorder (WPR), and the Windows 10 version of Windows Performance Analyzer (WPA) which is part of the Windows® Assessment and Deployment Kit (Windows ADK).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b456d-108">Les traces capturées avec TraceLogging doivent être capturées avec la version Windows 10 de l’enregistreur de performances Windows et affichées avec la version Windows 10 de Windows Performance Analyzer.</span><span class="sxs-lookup"><span data-stu-id="b456d-108">Traces captured with TraceLogging must be captured with the Windows 10 version of Windows Performance Recorder and viewed with the Windows 10 version of Windows Performance Analyzer.</span></span> <span data-ttu-id="b456d-109">Si vous ne parvenez pas à capturer ou à décoder vos événements, vérifiez que vous utilisez la version Windows 10 des outils.</span><span class="sxs-lookup"><span data-stu-id="b456d-109">If you are unable to capture or decode your events, verify that you are using the Windows 10 version of the tools.</span></span>

 

### <a name="1-capture-trace-data-with-wpr"></a><span data-ttu-id="b456d-110">1. capturer les données de trace avec WPR</span><span class="sxs-lookup"><span data-stu-id="b456d-110">1. Capture trace data with WPR</span></span>

<span data-ttu-id="b456d-111">Pour capturer une trace sur Windows Phone, consultez capturer des événements TraceLogging sur Windows Phone ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="b456d-111">To capture a trace on Windows Phone, see Capture TraceLogging events on Windows Phone below.</span></span>

<span data-ttu-id="b456d-112">Créez un profil d’enregistreur de performances Windows (. WPRP) afin de pouvoir utiliser WPR pour capturer vos événements Tracelogging.</span><span class="sxs-lookup"><span data-stu-id="b456d-112">Create a Windows Performance Recorder profile (.wprp) so that you can use WPR to capture your Tracelogging events.</span></span>

<span data-ttu-id="b456d-113">**Créez un. Fichier WPRP**</span><span class="sxs-lookup"><span data-stu-id="b456d-113">**Create a .WPRP file**</span></span>

1.  <span data-ttu-id="b456d-114">Utilisez l’exemple WPRP suivant avec l’exemple de code natif dans le [démarrage rapide C/C++ TraceLogging](tracelogging-native-quick-start.md) ou l’exemple managé dans le [démarrage rapide managé TraceLogging](tracelogging-managed-quick-start.md).</span><span class="sxs-lookup"><span data-stu-id="b456d-114">Use the following WPRP example with the native code example in the [TraceLogging C/C++ Quick Start](tracelogging-native-quick-start.md) or the managed example in the [TraceLogging Managed Quick Start](tracelogging-managed-quick-start.md).</span></span> <span data-ttu-id="b456d-115">Si vous consignez des événements à partir de votre propre fournisseur, remplacez les `TODO` sections par les valeurs appropriées pour votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="b456d-115">If you are logging events from your own provider, replace the `TODO` sections with the appropriate values for your provider.</span></span>

    > <span data-ttu-id="b456d-116">\[! Précieuse\]</span><span class="sxs-lookup"><span data-stu-id="b456d-116">\[!Important\]</span></span>  

     

    <span data-ttu-id="b456d-117">Si vous utilisez le démarrage rapide TraceLogging C/C++, spécifiez le GUID du fournisseur dans l' `Name` attribut de l' `<EventProvider>` élément.</span><span class="sxs-lookup"><span data-stu-id="b456d-117">If you are using the TraceLogging C/C++ quick start, specify the provider GUID in the `Name` attribute of the `<EventProvider>` element.</span></span> <span data-ttu-id="b456d-118">Par exemple : `<EventProvider Id="EventProvider_SimpleTraceLoggingProvider" Name="3970F9cf-2c0c-4f11-b1cc-e3a1e9958833" />`.</span><span class="sxs-lookup"><span data-stu-id="b456d-118">For example: `<EventProvider Id="EventProvider_SimpleTraceLoggingProvider" Name="3970F9cf-2c0c-4f11-b1cc-e3a1e9958833" />`.</span></span> <span data-ttu-id="b456d-119">Si vous utilisez le démarrage rapide Managed TraceLogging, spécifiez le nom du fournisseur précédé de' \* 'dans l' `Name` attribut de l' `<EventProvider />` élément.</span><span class="sxs-lookup"><span data-stu-id="b456d-119">If you are using the managed TraceLogging quick start, specify the provider name prefaced by '\*' in the `Name` attribute of the `<EventProvider />` element.</span></span> <span data-ttu-id="b456d-120">Par exemple : `<EventProvider Name="*SimpleTraceLoggingProvider" />`.</span><span class="sxs-lookup"><span data-stu-id="b456d-120">For example, `<EventProvider Name="*SimpleTraceLoggingProvider" />`.</span></span>

    <span data-ttu-id="b456d-121">Exemple de fichier WPRP.</span><span class="sxs-lookup"><span data-stu-id="b456d-121">Sample WPRP file.</span></span>

    ```XML
    <?xml version="1.0" encoding="utf-8"?>
    <!-- TODO: 
    1. Find and replace "SimpleTraceLoggingProvider" with the name of your provider.
    2. See TODO below to update GUID for your event provider
    -->
    <WindowsPerformanceRecorder Version="1.0" Author="Microsoft Corporation" Copyright="Microsoft Corporation" Company="Microsoft Corporation">
      <Profiles>
        <EventCollector Id="EventCollector_SimpleTraceLoggingProvider" Name="SimpleTraceLoggingProvider">
          <BufferSize Value="64" />
          <Buffers Value="4" />
        </EventCollector>

        <!-- TODO: 
     1. Update Name attribute in EventProvider xml element with your provider GUID, eg: Name="3970F9cf-2c0c-4f11-b1cc-e3a1e9958833". Or
        if you specify an EventSource C# provider or call TraceLoggingRegister(...) without a GUID, use star (*) before your provider
        name, eg: Name="*MyEventSourceProvider" which will enable your provider appropriately.  
     2. This sample lists one EventProvider xml element and references it in a Profile with EventProviderId xml element. 
        For your component wprp, enable the required number of providers and fix the Profile xml element appropriately
    -->
        <EventProvider Id="EventProvider_SimpleTraceLoggingProvider" Name="*SimpleTraceLoggingProvider" />
        
        <Profile Id="SimpleTraceLoggingProvider.Verbose.File" Name="SimpleTraceLoggingProvider" Description="SimpleTraceLoggingProvider" LoggingMode="File" DetailLevel="Verbose">
          <Collectors>
            <EventCollectorId Value="EventCollector_SimpleTraceLoggingProvider">
              <EventProviders>
                <!-- TODO:
     1. Fix your EventProviderId with Value same as the Id attribute on EventProvider xml element above
    -->
                <EventProviderId Value="EventProvider_SimpleTraceLoggingProvider" />
              </EventProviders>
            </EventCollectorId>
          </Collectors>
        </Profile>

        <Profile Id="SimpleTraceLoggingProvider.Light.File" Name="SimpleTraceLoggingProvider" Description="SimpleTraceLoggingProvider" Base="SimpleTraceLoggingProvider.Verbose.File" LoggingMode="File" DetailLevel="Light" />
        <Profile Id="SimpleTraceLoggingProvider.Verbose.Memory" Name="SimpleTraceLoggingProvider" Description="SimpleTraceLoggingProvider" Base="SimpleTraceLoggingProvider.Verbose.File" LoggingMode="Memory" DetailLevel="Verbose" />
        <Profile Id="SimpleTraceLoggingProvider.Light.Memory" Name="SimpleTraceLoggingProvider" Description="SimpleTraceLoggingProvider" Base="SimpleTraceLoggingProvider.Verbose.File" LoggingMode="Memory" DetailLevel="Light" />

      </Profiles>
    </WindowsPerformanceRecorder>
    
    ```

    

2.  <span data-ttu-id="b456d-122">Enregistrez le fichier avec un. Extension de nom de fichier WPRP.</span><span class="sxs-lookup"><span data-stu-id="b456d-122">Save the file with a .WPRP file name extension.</span></span>
3.  <span data-ttu-id="b456d-123">Démarrez la capture à l’aide de la commande WPR à partir d’une fenêtre d’invite de commandes avec élévation de privilèges (exécuter en tant qu’administrateur).</span><span class="sxs-lookup"><span data-stu-id="b456d-123">Start the capture using WPR from an elevated (run as Administrator) Command Prompt window.</span></span>

    <span data-ttu-id="b456d-124">**<path to wpr>\\wpr.exe-Start GeneralProfile-Start TraceLoggingProvider. WPRP**</span><span class="sxs-lookup"><span data-stu-id="b456d-124">**<path to wpr>\\wpr.exe -start GeneralProfile -start TraceLoggingProvider.wprp**</span></span>

    > <span data-ttu-id="b456d-125">\[! Accélératrice\]</span><span class="sxs-lookup"><span data-stu-id="b456d-125">\[!Tip\]</span></span>  
    > <span data-ttu-id="b456d-126">À des fins de profilage général, vous pouvez également ajouter **– Start GeneralProfile** à la ligne de commande wpr.exe pour capturer des événements système, ainsi que les événements de votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="b456d-126">For general profiling purposes, you can also add **–start GeneralProfile** to the wpr.exe command line to capture system events along with the events from your provider.</span></span> <span data-ttu-id="b456d-127">Si vous souhaitez uniquement rassembler vos événements, omettez **-Start GeneralProfile**.</span><span class="sxs-lookup"><span data-stu-id="b456d-127">If you only want to gather your events, omit **-start GeneralProfile**.</span></span>

     

4.  <span data-ttu-id="b456d-128">Exécutez l’application qui contient vos événements.</span><span class="sxs-lookup"><span data-stu-id="b456d-128">Run the application that contains your events.</span></span>
5.  <span data-ttu-id="b456d-129">Arrêtez la capture de trace.</span><span class="sxs-lookup"><span data-stu-id="b456d-129">Stop the trace capture.</span></span>

    <span data-ttu-id="b456d-130">**<path to wpr>\\wpr.exe-arrêter la description de TraceCaptureFile. etl**</span><span class="sxs-lookup"><span data-stu-id="b456d-130">**<path to wpr>\\wpr.exe -stop TraceCaptureFile.etl description**</span></span>

    > <span data-ttu-id="b456d-131">\[! Accélératrice\]</span><span class="sxs-lookup"><span data-stu-id="b456d-131">\[!Tip\]</span></span>  
    > <span data-ttu-id="b456d-132">Si vous avez ajouté- **Start GeneralProfile** pour collecter les événements système, ajoutez **-Stop GeneralProfile** à la ligne de commande **wpr.exe** ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="b456d-132">If you added **–start GeneralProfile** to gather system events, add **-stop GeneralProfile** to the **wpr.exe** command line above.</span></span>

     

### <a name="2-capture-tracelogging-events-on-windows-phone"></a><span data-ttu-id="b456d-133">2. capturer des événements TraceLogging sur Windows Phone</span><span class="sxs-lookup"><span data-stu-id="b456d-133">2. Capture TraceLogging events on Windows Phone</span></span>

<span id="capturephone"></span><span id="CAPTUREPHONE"></span>

1.  <span data-ttu-id="b456d-134">Démarrez tracelog pour capturer les événements de votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="b456d-134">Start tracelog to capture events from your provider.</span></span>

    <span data-ttu-id="b456d-135">**CMDD tracelog-Start test-f c : \\ test. etl-GUID \# ProviderGuid**</span><span class="sxs-lookup"><span data-stu-id="b456d-135">**cmdd tracelog -start test -f c:\\test.etl -guid \#providerguid**</span></span>

2.  <span data-ttu-id="b456d-136">Exécutez votre scénario de test pour consigner les événements.</span><span class="sxs-lookup"><span data-stu-id="b456d-136">Run your test scenario to log events.</span></span>
3.  <span data-ttu-id="b456d-137">Arrêter la capture de trace.</span><span class="sxs-lookup"><span data-stu-id="b456d-137">Stop trace capture.</span></span>

    <span data-ttu-id="b456d-138">**CMDD tracelog-arrêter le test**</span><span class="sxs-lookup"><span data-stu-id="b456d-138">**cmdd tracelog -stop test**</span></span>

4.  <span data-ttu-id="b456d-139">Fusionnez les résultats de trace du système avec les résultats de trace.</span><span class="sxs-lookup"><span data-stu-id="b456d-139">Merge the system trace results with your trace results.</span></span>

    <span data-ttu-id="b456d-140">**CMDD Xperf-Merge c : \\ test. etl c : \\ testmerged. etl**</span><span class="sxs-lookup"><span data-stu-id="b456d-140">**cmdd xperf -merge c:\\test.etl c:\\testmerged.etl**</span></span>

5.  <span data-ttu-id="b456d-141">Récupérez le fichier journal fusionné.</span><span class="sxs-lookup"><span data-stu-id="b456d-141">Retrieve the merged log file.</span></span>

    <span data-ttu-id="b456d-142">**getd c : \\ testmerged. etl**</span><span class="sxs-lookup"><span data-stu-id="b456d-142">**getd c:\\testmerged.etl**</span></span>

### <a name="3-view-tracelogging-data-using-windows-performance-analyzer"></a><span data-ttu-id="b456d-143">3. Affichez les données TraceLogging à l’aide de l’analyseur de performances Windows.</span><span class="sxs-lookup"><span data-stu-id="b456d-143">3. View TraceLogging data using Windows Performance Analyzer.</span></span>

<span data-ttu-id="b456d-144">WPA est actuellement la seule visionneuse que vous pouvez utiliser pour afficher les fichiers de trace TraceLogging (. ETL).</span><span class="sxs-lookup"><span data-stu-id="b456d-144">WPA is currently the only viewer you can use to view TraceLogging trace (.etl) files.</span></span>

1.  <span data-ttu-id="b456d-145">Démarrez WPA.</span><span class="sxs-lookup"><span data-stu-id="b456d-145">Start WPA.</span></span>

    <span data-ttu-id="b456d-146">**<path to wpr>\\wpa.exe traceLoggingResults. etl**</span><span class="sxs-lookup"><span data-stu-id="b456d-146">**<path to wpr>\\wpa.exe traceLoggingResults.etl**</span></span>

2.  <span data-ttu-id="b456d-147">Chargez le fichier de trace (. ETL) que vous avez spécifié dans la commande wpa.exe ci-dessus, par exemple traceLoggingResults. etl.</span><span class="sxs-lookup"><span data-stu-id="b456d-147">Load the trace (.etl) file that you specified in the wpa.exe command above, e.g. traceLoggingResults.etl.</span></span>
3.  <span data-ttu-id="b456d-148">Affichez vos événements de fournisseur.</span><span class="sxs-lookup"><span data-stu-id="b456d-148">View your provider events.</span></span> <span data-ttu-id="b456d-149">Dans l’Explorateur de graphiques WPA, développez **activité système**.</span><span class="sxs-lookup"><span data-stu-id="b456d-149">In the WPA Graph Explorer, expand **System Activity**.</span></span>
4.  <span data-ttu-id="b456d-150">Double-cliquez dans le volet **événements génériques** pour afficher les événements dans le volet **analyse** .</span><span class="sxs-lookup"><span data-stu-id="b456d-150">Double-click in the **Generic Events** pane to view the events in the **Analysis** pane.</span></span>

    ![développer les événements génériques](images/expandsystemactivity.png)

5.  <span data-ttu-id="b456d-152">Dans le volet analyse, recherchez les événements de votre fournisseur pour vérifier que TraceLogging fonctionne.</span><span class="sxs-lookup"><span data-stu-id="b456d-152">In the Analysis pane, locate the events from your provider to verify that TraceLogging is working.</span></span>

    <span data-ttu-id="b456d-153">Dans la colonne **nom du fournisseur** de la table **événements génériques** , recherchez et sélectionnez la ligne avec le nom de votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="b456d-153">In the **Provider Name** column of the **Generic Events** table, find and select the row with your provider name.</span></span>

    <span data-ttu-id="b456d-154">Si vous avez plusieurs fournisseurs à trier, cliquez sur l’en-tête de colonne pour trier par nom de colonne, ce qui peut faciliter la recherche de votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="b456d-154">If you have multiple providers to sort through, click the column header to sort by column name which may make it easier to find your provider.</span></span>

    <span data-ttu-id="b456d-155">Lorsque vous avez trouvé votre fournisseur, cliquez avec le bouton droit sur le nom et sélectionnez **Filtrer par sélection**.</span><span class="sxs-lookup"><span data-stu-id="b456d-155">When you find your provider, right click on the name and select **Filter to Selection**.</span></span>

    ![filtrer la sélection vers le fournisseur](images/filtertoselection.png)

    <span data-ttu-id="b456d-157">L’événement pour SimpleTraceLoggingProvider et sa valeur s’affichent dans le volet inférieur de la fenêtre d’analyse.</span><span class="sxs-lookup"><span data-stu-id="b456d-157">The event for the SimpleTraceLoggingProvider and its value will appear in the bottom pane of the Analysis window.</span></span> <span data-ttu-id="b456d-158">Développez le nom du fournisseur pour afficher les événements.</span><span class="sxs-lookup"><span data-stu-id="b456d-158">Expand the provider name to see the events.</span></span>

    ![afficher l’événement à partir du simpletraceloggingprovider](images/eventview.png)

    <span data-ttu-id="b456d-160">Pour plus d’informations sur l’utilisation de WPA, voir [Analyseur de performances Windows](/previous-versions/windows/it-pro/windows-8.1-and-8/hh448170(v=win.10)).</span><span class="sxs-lookup"><span data-stu-id="b456d-160">For more information about using WPA, see [Windows Performance Analyzer](/previous-versions/windows/it-pro/windows-8.1-and-8/hh448170(v=win.10)).</span></span>

## <a name="summary-and-next-steps"></a><span data-ttu-id="b456d-161">Résumé et étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="b456d-161">Summary and next steps</span></span>

<span data-ttu-id="b456d-162">Le processus d’enregistrement et d’affichage des événements ETW à l’aide de WPR et WPA s’applique aussi bien aux événements TraceLogging.</span><span class="sxs-lookup"><span data-stu-id="b456d-162">The process for recording and viewing ETW events using WPR and WPA apply equally well to TraceLogging events.</span></span>

<span data-ttu-id="b456d-163">Pour obtenir des exemples de TraceLogging supplémentaires, consultez [exemples Tracelogging C/C++](tracelogging-c-cpp-tracelogging-examples.md) .</span><span class="sxs-lookup"><span data-stu-id="b456d-163">See [C/C++ Tracelogging Examples](tracelogging-c-cpp-tracelogging-examples.md) for additional TraceLogging examples.</span></span>

 

 