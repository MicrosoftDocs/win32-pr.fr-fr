---
title: Traçage
description: le suivi utilise Suivi d’v nements pour Windows (ETW).
ms.assetid: b008bae2-9423-4e72-ae03-9cd50f73d812
keywords:
- Suivi des services Web pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ace571c2639ddd1eb55ed1e4afd70bcef7318b44
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127225572"
---
# <a name="tracing"></a>Traçage

le suivi utilise Suivi d’v nements pour Windows (ETW). pour tirer parti des outils de suivi disponibles avec Windows Server 2008 R2, installez le Microsoft Windows SDK à partir du site de [téléchargement MSDN](https://www.microsoft.com/download/details.aspx?id=8279) .


Trois niveaux de suivi sont pris en charge :

-   Verbose (toutes les traces disponibles).
-   Info (traces d’informations).
-   Erreur (traces d’erreurs).

Les événements suivants sont suivis :

-   Toutes les erreurs (niveau = erreur, niveau = info ou niveau = détaillé).
-   Entrée/sortie d’une API (Level = info ou level = verbose).
-   Début et fin de toutes les e/s (niveau = info ou niveau = détaillé)
-   messages SOAP échangés (niveau = verbose, disponible sur Windows 2003 SP1 et versions ultérieures)

## <a name="generating-and-viewing-wwsapi-traces"></a>Génération et affichage des traces WWSAPI

WWSAPI utilise les événements basés sur le manifeste sur Windows Vista et versions ultérieures. Par conséquent, l’expérience de suivi présente des différences en fonction de la version du système d’exploitation. La génération de suivis ETW peut être effectuée à l’aide des outils ETW intégrés sur toutes les plateformes prises en charge. toutefois, l’affichage des suivis ETW dans un format attrayant nécessite des outils personnalisés sur Windows XP SP2 et Windows 2003 SP1. Il existe plusieurs façons de collecter et d’afficher les suivis d’événements ETW WWSAPI en fonction de la version du système d’exploitation.

## <a name="enabling-and-viewing-wwsapi-traces-in-event-viewer-works-on-windows-vista-and-above"></a>activation et affichage des traces WWSAPI dans observateur d’événements (fonctionne sur Windows Vista et versions ultérieures)

-   Exécutez eventvwr. msc à partir de la ligne de commande ou du menu exécuter.
-   Cliquez sur le lien Afficher dans le volet actions à droite, puis activez l’option Afficher les journaux d’analyse et de débogage.
-   accédez aux journaux des applications et des services \\ Microsoft \\ Windows \\ les fournisseurs webservices dans le volet gauche.
-   Cliquez avec le bouton droit sur le fournisseur de suivi et sélectionnez Activer le journal.
-   Exécutez votre scénario.
-   Quand vous actualisez la page de l’observateur d’événements, vous devez commencer à voir les entrées de suivi WWSAPI.

## <a name="enabling-and-viewing-wwsapi-traces-using-wstracebat-script-works-on-xpsp2-and-above"></a>Activation et affichage des traces WWSAPI à l’aide d' Wstrace.bat script (fonctionne sur XPSP2 et versions ultérieures)

Le fichier de commandes wstrace.bat offre un moyen pratique d’effectuer les opérations suivantes :

-   Créer un journal des traces
-   Supprimer un journal de suivi
-   Activer et désactiver le suivi
-   Mettre à jour le niveau de suivi (info/erreur/verbose)
-   Conversion des journaux de suivi en fichiers CSV

Le fichier de commandes utilise logman.exe pour toutes les commandes, à l’exception de la conversion des journaux en fichier CSV, qui nécessite un outil personnalisé (wstracedump.exe).

## <a name="using-tracing-commands"></a>Utilisation des commandes de suivi

La commande suivante crée un journal qui utilise les informations, les erreurs ou le niveau de détail. Cette commande requiert des privilèges élevés.

**wstrace.bat de créer des \[ informations détaillées sur l' \| erreur \|\]**

La commande suivante supprime le journal. Cette commande requiert des privilèges élevés.

**wstrace.bat supprimer**

La commande suivante active le suivi. Vous devez d’abord créer un journal.

**wstrace.bat**

Le niveau de suivi (info, erreur ou commentaires) peut être modifié comme suit :

**Informations de mise à jourwstrace.bat \[ informations \| \| détaillées\]**

Pour vider la sortie de trace, utilisez la commande suivante :

**wstrace.bat > de vidage temp.csv**

Les événements seront vidés dans le fichier CSV jusqu’à ce que CTRL-C soit enfoncé ou que le suivi soit désactivé.

## <a name="tracing-file-format"></a>Format de fichier de suivi

Les fichiers CSV créés par wstrace.bat sont des fichiers texte de variables séparées par des virgules simples. ces fichiers peuvent être ouverts dans Excel, Bloc-notes, etc.

Les colonnes du fichier sont les suivantes :

-   Horodatage du moment où l’événement a été enregistré
-   ProcessID-ID ULONG du processus d’enregistrement de l’événement
-   ThreadID-ID ULONG du thread enregistrant l’événement
-   La valeur d’énumération d’événements du type d’événement peut être (« API Enter » " \| API pending" " \| API ExitSyncSuccess" \| "API ExitSyncFailure" \| "API ExitAsyncSuccess" \| "API ExitAsyncFailure" \| "IO Started" \| "e/s terminée « \| » échec de l’e/s « » \| , erreur «réception du message \| reçu » « \| message \| \| \| \| reçu » « réception du message d’arrêt » « l’envoi du message a été envoyé ».
-   Operation : nom de l’opération appelée. En général, il est mappé à l’API appelée.
-   Erreur : numéro d’erreur HRESULT facultatif
-   Info : informations facultatives sur l’événement

## <a name="collecting-wwsapi-etw-trace-file-using-etw-tools-works-on-xpsp2-and-above"></a>Collecte du fichier de trace ETW WWSAPI à l’aide des outils ETW (fonctionne sur XPSP2 et versions ultérieures)

Activation du suivi ETW pour WWSAPI

**logman start wstrace-bs 64-ft 1-rt-p Microsoft-Windows-webservices \[ indicateurs \[ niveau \] \] \[ -o &lt; EtlLogFileName &gt; \] -ets**

pour créer et démarrer la session de suivi ETW. Logman.exe est un outil ETW intégré disponible sur toutes les plateformes prises en charge. notez que vous devez utiliser Microsoft \_ Windows \_ webservices comme nom de fournisseur sur XPSP2 et dans le sp2. Vous pouvez exécuter logman query providers pour afficher la liste des fournisseurs inscrits. le fournisseur microsoft-Windows-webservices (ou microsoft \_ Windows \_ webservices) doit être répertorié, sauf s’il n’est pas inscrit. Le fournisseur est normalement inscrit au cours de l’installation. toutefois, il peut également être enregistré manuellement en exécutant wevtutil.exe &lt; ManifestFileName im &gt; (sur Windows Vista et versions ultérieures) ou mofcomp.exe &lt; MofFileName &gt; (sur XPSP2 et de la version ultérieure).

Les indicateurs peuvent être utilisés pour filtrer les traces par leur genre. Il peut s’agir d’une valeur ou d’un des genres de trace suivants. S’il n’est pas fourni, tous les types de suivi sont activés.

-   0x1-suivis d’entrée/sortie de l’API.
-   0X2-suivi des erreurs.
-   0x4-suivis d’e/s.
-   0x8-suivis des messages SOAP.
-   0x10 : traces des messages binaires.

Le niveau peut être utilisé pour filtrer les traces par niveau. Il doit s’agir de l’une des valeurs suivantes. S’il n’est pas fourni, tous les niveaux de suivi sont activés.

-   0x1-traces irrécupérables.
-   0X2-suivi des erreurs.
-   0x3-traces d’avertissement.
-   0x4-suivis d’information.
-   0x5-suivis détaillés.

EtlLogFileName est le chemin d’accès au fichier journal des événements ETW à créer (utilisez l’extension. ETL). S’il n’est pas fourni, ETW choisit un nom aléatoire qui peut être interrogé ultérieurement. Ce fichier ne doit pas résider dans le répertoire de profil de l’utilisateur. Le fichier journal des événements ETW (fichier. ETL) est au format binaire. Elle peut être consommée par les applications ETW, mais elle n’est pas dans un format lisible par l’utilisateur. L’étape suivante décrit comment afficher son contenu.

Exécuter votre scénario

Collecte du fichier journal des événements ETW.

**logman stop wstrace-ETS**

pour arrêter la session de suivi ETW. C’est à ce moment que ETW arrête l’enregistrement des événements. Le fichier journal des événements ETW (spécifié dans le paramètre EtlLogFileName) est prêt à être consommé. Il peut être affiché localement (les instructions sont fournies ci-dessous) ou envoyées au groupe de produits à des fins d’investigation.

Exemple de bout en bout utilisant les outils ETW :

**logman start wstrace-bs 64-ft 1-rt-p Microsoft-Windows-webservices-o mytrace. etl-ets**

**echo.. Exécutez votre scénario.**

**logman stop wstrace-ETS**

**tracerpt mytrace. etl-o mytrace.xml**

**wstrace.htm**

**echo.. Utilisez mytrace.xml et wstrace. xsl dans la page ouverte..**

## <a name="viewing-wwsapi-etw-trace-file-traces-using-wstracedumpexe-tool-works-on-windows-xp-and-above"></a>affichage des traces du fichier de Trace ETW WWSAPI à l’aide de l’outil wstracedump.exe (fonctionne sur Windows XP et versions ultérieures)

Wstracedump.exe est un outil consommateur ETW développé personnalisé qui traite les événements dans le fichier de trace ETW WWSAPI et produit une sortie lisible par l’utilisateur. Il peut produire une sortie de toutes les plateformes prises en charge. Pour plus d’informations, consultez son utilisation (wstracedump.exe- ?).

## <a name="viewing-wwsapi-etw-trace-file-traces-using-etw-tools-works-on-windows-vista-and-above"></a>affichage des traces du fichier de Trace etw WWSAPI à l’aide des outils etw (fonctionne sur Windows Vista et versions ultérieures)

Tracerpt.exe est l’outil qui permet d’afficher le contenu d’un fichier journal d’événements ETW et est disponible sur toutes les plateformes prises en charge. Il peut être utilisé pour générer des fichiers de vidage CSV, EVTX ou XML à partir d’un fichier journal d’événements ETW. toutefois, le fichier de sortie généré a des traces lisibles par les humains uniquement sur Windows Vista et versions ultérieures. Ces instructions décrivent comment générer le fichier de vidage XML et l’utiliser avec un fichier XSL pour afficher les traces dans un format attrayant (le fichier XSL est très trivial et peut être modifié si vous souhaitez des formats différents).

-   Exécuter

    **tracerpt &lt; EtlLogFileName &gt; -o &lt; OutputXMLFileName&gt;**

    pour créer un vidage XML à partir du fichier ETL binaire (tracerpt.exe crée le fichier de sortie au format XML par défaut. Exécuter tracerpt- ? Pour voir d’autres formats disponibles).

-   À ce stade, vous pouvez voir les informations de suivi dans le fichier XML. En outre, vous pouvez ouvrir le fichier wstrace.htm et utiliser le fichier dump XML et le fichier wstrace. xsl pour voir les traces dans un format plus attrayant. Notez que les fichiers doivent se trouver sur l’ordinateur local pour pouvoir utiliser ce fichier HTML sur Internet Explorer.

## <a name="security"></a>Sécurité

Lors de l’activation du suivi, les administrateurs doivent prendre en compte la consommation d’espace disque supplémentaire et de puissance de calcul. Un client ou une application malveillante peut épuiser les ressources système, sauf si les paramètres de suivi sont configurés avec des limites raisonnables. Lors de l’utilisation de la fonctionnalité de suivi des messages, les messages qui transportent des informations sensibles telles que des informations d’identification, des informations personnelles, etc., peuvent être conservés sur le disque ou être consultés par toute personne ayant accès à l’observateur d’événements système. pour pallier ce problème, le suivi peut être activé par des utilisateurs système ou administrateur sur Windows 2003 et versions ultérieures. le suivi des messages est désactivé sur Windows XP sur lequel n’importe quel utilisateur peut activer le suivi.

L’énumération suivante est utilisée avec le suivi :

-   [**\_API WS trace \_**](/windows/desktop/api/WebServices/ne-webservices-ws_trace_api)

 

 




