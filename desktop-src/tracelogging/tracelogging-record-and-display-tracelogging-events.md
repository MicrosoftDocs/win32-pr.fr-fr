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
# <a name="record-and-view-tracelogging-events"></a>Enregistrer et afficher les événements TraceLogging

Enregistrez les événements TraceLogging avec l’enregistreur de performances Windows (WPR) et affichez-les à l’aide de l’analyseur de performances Windows (WPA).

## <a name="prerequisites"></a>Prérequis

-   Windows 10
-   La version Windows 10 de l’enregistreur de performances Windows (WPR) et la version Windows 10 de Windows Performance Analyzer (WPA) qui fait partie du kit de déploiement et d’évaluation Windows® (Windows ADK).

> [!IMPORTANT]
> Les traces capturées avec TraceLogging doivent être capturées avec la version Windows 10 de l’enregistreur de performances Windows et affichées avec la version Windows 10 de Windows Performance Analyzer. Si vous ne parvenez pas à capturer ou à décoder vos événements, vérifiez que vous utilisez la version Windows 10 des outils.

 

### <a name="1-capture-trace-data-with-wpr"></a>1. capturer les données de trace avec WPR

Pour capturer une trace sur Windows Phone, consultez capturer des événements TraceLogging sur Windows Phone ci-dessous.

Créez un profil d’enregistreur de performances Windows (. WPRP) afin de pouvoir utiliser WPR pour capturer vos événements Tracelogging.

**Créez un. Fichier WPRP**

1.  Utilisez l’exemple WPRP suivant avec l’exemple de code natif dans le [démarrage rapide C/C++ TraceLogging](tracelogging-native-quick-start.md) ou l’exemple managé dans le [démarrage rapide managé TraceLogging](tracelogging-managed-quick-start.md). Si vous consignez des événements à partir de votre propre fournisseur, remplacez les `TODO` sections par les valeurs appropriées pour votre fournisseur.

    > \[! Précieuse\]  

     

    Si vous utilisez le démarrage rapide TraceLogging C/C++, spécifiez le GUID du fournisseur dans l' `Name` attribut de l' `<EventProvider>` élément. Par exemple : `<EventProvider Id="EventProvider_SimpleTraceLoggingProvider" Name="3970F9cf-2c0c-4f11-b1cc-e3a1e9958833" />`. Si vous utilisez le démarrage rapide Managed TraceLogging, spécifiez le nom du fournisseur précédé de' \* 'dans l' `Name` attribut de l' `<EventProvider />` élément. Par exemple : `<EventProvider Name="*SimpleTraceLoggingProvider" />`.

    Exemple de fichier WPRP.

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

    

2.  Enregistrez le fichier avec un. Extension de nom de fichier WPRP.
3.  Démarrez la capture à l’aide de la commande WPR à partir d’une fenêtre d’invite de commandes avec élévation de privilèges (exécuter en tant qu’administrateur).

    **<path to wpr>\\wpr.exe-Start GeneralProfile-Start TraceLoggingProvider. WPRP**

    > \[! Accélératrice\]  
    > À des fins de profilage général, vous pouvez également ajouter **– Start GeneralProfile** à la ligne de commande wpr.exe pour capturer des événements système, ainsi que les événements de votre fournisseur. Si vous souhaitez uniquement rassembler vos événements, omettez **-Start GeneralProfile**.

     

4.  Exécutez l’application qui contient vos événements.
5.  Arrêtez la capture de trace.

    **<path to wpr>\\wpr.exe-arrêter la description de TraceCaptureFile. etl**

    > \[! Accélératrice\]  
    > Si vous avez ajouté- **Start GeneralProfile** pour collecter les événements système, ajoutez **-Stop GeneralProfile** à la ligne de commande **wpr.exe** ci-dessus.

     

### <a name="2-capture-tracelogging-events-on-windows-phone"></a>2. capturer des événements TraceLogging sur Windows Phone

<span id="capturephone"></span><span id="CAPTUREPHONE"></span>

1.  Démarrez tracelog pour capturer les événements de votre fournisseur.

    **CMDD tracelog-Start test-f c : \\ test. etl-GUID \# ProviderGuid**

2.  Exécutez votre scénario de test pour consigner les événements.
3.  Arrêter la capture de trace.

    **CMDD tracelog-arrêter le test**

4.  Fusionnez les résultats de trace du système avec les résultats de trace.

    **CMDD Xperf-Merge c : \\ test. etl c : \\ testmerged. etl**

5.  Récupérez le fichier journal fusionné.

    **getd c : \\ testmerged. etl**

### <a name="3-view-tracelogging-data-using-windows-performance-analyzer"></a>3. Affichez les données TraceLogging à l’aide de l’analyseur de performances Windows.

WPA est actuellement la seule visionneuse que vous pouvez utiliser pour afficher les fichiers de trace TraceLogging (. ETL).

1.  Démarrez WPA.

    **<path to wpr>\\wpa.exe traceLoggingResults. etl**

2.  Chargez le fichier de trace (. ETL) que vous avez spécifié dans la commande wpa.exe ci-dessus, par exemple traceLoggingResults. etl.
3.  Affichez vos événements de fournisseur. Dans l’Explorateur de graphiques WPA, développez **activité système**.
4.  Double-cliquez dans le volet **événements génériques** pour afficher les événements dans le volet **analyse** .

    ![développer les événements génériques](images/expandsystemactivity.png)

5.  Dans le volet analyse, recherchez les événements de votre fournisseur pour vérifier que TraceLogging fonctionne.

    Dans la colonne **nom du fournisseur** de la table **événements génériques** , recherchez et sélectionnez la ligne avec le nom de votre fournisseur.

    Si vous avez plusieurs fournisseurs à trier, cliquez sur l’en-tête de colonne pour trier par nom de colonne, ce qui peut faciliter la recherche de votre fournisseur.

    Lorsque vous avez trouvé votre fournisseur, cliquez avec le bouton droit sur le nom et sélectionnez **Filtrer par sélection**.

    ![filtrer la sélection vers le fournisseur](images/filtertoselection.png)

    L’événement pour SimpleTraceLoggingProvider et sa valeur s’affichent dans le volet inférieur de la fenêtre d’analyse. Développez le nom du fournisseur pour afficher les événements.

    ![afficher l’événement à partir du simpletraceloggingprovider](images/eventview.png)

    Pour plus d’informations sur l’utilisation de WPA, voir [Analyseur de performances Windows](/previous-versions/windows/it-pro/windows-8.1-and-8/hh448170(v=win.10)).

## <a name="summary-and-next-steps"></a>Résumé et étapes suivantes

Le processus d’enregistrement et d’affichage des événements ETW à l’aide de WPR et WPA s’applique aussi bien aux événements TraceLogging.

Pour obtenir des exemples de TraceLogging supplémentaires, consultez [exemples Tracelogging C/C++](tracelogging-c-cpp-tracelogging-examples.md) .

 

 