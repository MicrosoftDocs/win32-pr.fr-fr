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
# <a name="tracing-wmi-activity"></a>Suivi de l’activité WMI

À compter de Windows Vista, le service WMI n’utilise pas les [fichiers journaux WMI](wmi-log-files.md). Au lieu de cela, il utilise [suivi d’v nements pour Windows (ETW)](/windows/desktop/ETW/event-tracing-portal) et les événements sont disponibles via **Observateur d’événements** ou l’outil en ligne de commande Wevtutil.

Les sections suivantes sont présentées dans cette rubrique :

-   [Obtention d’événements WMI via observateur d’événements](#obtaining-wmi-events-through-event-viewer)
-   [Activation du suivi WMI à l’invite de commandes](#enabling-wmi-tracing-at-command-prompt)
-   [Utilisation du suivi WMI basé sur WPP](#using-wpp-based-wmi-tracing)
-   [Rubriques connexes](#related-topics)

## <a name="obtaining-wmi-events-through-event-viewer"></a>Obtention d’événements WMI via observateur d’événements

Le fichier WMITracing. log contient les événements suivis par WMI. Toutefois, il s’agit d’un fichier binaire. Pour afficher ces événements dans un format lisible par l’homme, utilisez l' **Observateur d’événements**.

Par défaut, les événements WMI ne sont pas suivis. Cette procédure décrit comment utiliser **Observateur d’événements** pour activer le suivi d’événements WMI et localiser les événements WMI. Vous pouvez effectuer les mêmes opérations à l’aide de l’outil en ligne de commande Wevtutil.

**Pour afficher les événements WMI dans observateur d’événements**

1.  Ouvrez l’ **Observateur d’événements**. Dans le menu **Affichage**, cliquez sur **Afficher les journaux d'analyse et de débogage**. Recherchez le journal des canaux de **suivi** pour WMI sous applications et journaux des services \| \| activité Microsoft Windows \| WMI.
2.  Cliquez avec le bouton droit sur le journal de **suivi** et sélectionnez **Propriétés du journal**. Activez la case à cocher **activer la journalisation** pour démarrer le suivi d’événements WMI. Pour plus d’informations sur les canaux, consultez [journaux des événements et canaux dans le journal des événements Windows](/previous-versions//aa385225(v=vs.85)).
3.  Les événements WMI s’affichent dans la fenêtre d’événements pour l' **activité WMI**. Double-cliquez sur un événement de la liste pour afficher les informations détaillées. Vous pouvez afficher un événement en **mode XML** ou dans un format d' **affichage convivial** .

Le champ **ID d’événement** affiche une valeur qui contient les informations suivantes.

<dl> <dt>

<span id="Event_1"></span><span id="event_1"></span><span id="EVENT_1"></span>Événement 1
</dt> <dd>

Début de la séquence d’événements pour une opération spécifique. Une occurrence pour chaque séquence.

Les champs d’événement pour un événement 1 sont :

-   **GroupOperationID** est un identificateur unique utilisé pour tous les événements signalés pour un client spécifique.
-   **OperationId** indique la séquence d’opérations.
-   L' **opération** spécifie la connexion ou la demande à WMI.
-   L' **utilisateur** indique le compte qui effectue une requête auprès de WMI en exécutant un script ou via CIM Studio.
-   **Espace** de noms affiche l’espace de noms WMI dans lequel la connexion est établie.

Par exemple, un script peut demander toutes les instances d’une classe WMI, telles que [**le \_ service Win32**](/windows/desktop/CIMWin32Prov/win32-service). La première opération peut être une connexion à WMI.

</dd> <dt>

<span id="Event_2"></span><span id="event_2"></span><span id="EVENT_2"></span>Événement 2
</dt> <dd>

Événements qui composent l’opération. Une ou plusieurs occurrences dans la séquence.

Les champs d’événement pour un événement 2 sont les suivants :

-   **GroupOperationID** indique la séquence dans laquelle l’événement se produit.
-   **GroupOperationID** indique la séquence dans laquelle l’événement se produit.
-   **ProviderName** indique le nom du fournisseur qui fournit les données.
-   **Path** est le chemin d’accès WMI de l’objet.

Par exemple, l’opération peut être une énumération [**de \_ service Win32**](/windows/desktop/CIMWin32Prov/win32-service).

</dd> <dt>

<span id="Event_3"></span><span id="event_3"></span><span id="EVENT_3"></span>Événement 3
</dt> <dd>

Fin de la séquence d’événements pour une opération spécifique. Une occurrence pour chaque séquence.

Seul le **GroupOperationID** est affiché.

</dd> </dl>

## <a name="enabling-wmi-tracing-at-command-prompt"></a>Activation du suivi WMI à l’invite de commandes

Vous pouvez également activer le suivi d’événements WMI via l’outil en ligne de commande Wevtutil. Utilisez la commande suivante : **Wevtutil.exe SL Microsoft-Windows-WMI-Activity/trace/e : true**. La source d’événement WMI est Microsoft-Windows-WMI. Pour plus d’informations sur la Wevtutil.exe, consultez [à propos du journal des événements Windows](/previous-versions//aa382610(v=vs.85)).

## <a name="using-wpp-based-wmi-tracing"></a>Utilisation du suivi WMI basé sur WPP

Dans les systèmes d’exploitation Windows à compter de Windows Vista, WMI crée un canal de trace actif pendant le processus de démarrage. Le nom du canal est session de \_ suivi WMI \_ . Seules les erreurs sont enregistrées dans le canal.

Le préprocesseur de suivi logiciel Windows enregistre les informations dans un fichier binaire. Pour lire le fichier, vous devez d’abord le convertir au format texte lisible. Vous utilisez un outil appelé tracefmt.exe à partir du [Kit de pilotes Windows (WDK)](https://www.microsoft.com/whdc/DevTools/WDK/WDKpkg.mspx) pour effectuer la traduction. L’outil nécessite des informations stockées dans certains fichiers associés. Les fichiers se trouvent dans le répertoire% SystemRoot% \\ system32 \\ WBEM \\ TMF et ont une extension de nom de fichier. TMF. L’outil requiert en fait un seul fichier. TMF. Vous créez ce fichier unique en concaténant tous les fichiers. TMF dans un autre fichier. TMF. Pour plus d’informations sur les fichiers. TMF, consultez [fichier de format de message de trace](/windows-hardware/drivers/devtest/trace-message-format-file).

Après avoir installé le [Kit de pilotes Windows (WDK)](https://www.microsoft.com/whdc/DevTools/WDK/WDKpkg.mspx) pour obtenir les outils en ligne de commande tracelog.exe et tracefmt.exe, procédez comme suit pour collecter un suivi WMI basé sur WPP.

**Pour afficher une trace WMI basée sur WPP**

1.  Pour créer le fichier. TMF unique, ouvrez une fenêtre d’invite de commandes avec élévation de privilèges et accédez au répertoire% SystemRoot% \\ system32 \\ WBEM \\ TMF.

2.  Tapez **Copy/y% systemroot% \\ system32 \\ WBEM \\ TMF \\ \* . TMF% systemroot% \\ system32 \\ WBEM \\ TMF \\ WMI. TMF**. Cette opération crée un fichier nommé WMI. TMF qui comprend le contenu de tous les autres fichiers. TMF.

3.  Tapez **tracelog-Flush \_ \_ session de trace WMI**. Les tampons WPP sont vidés sur le disque.
4.  **Définir le \_ préfixe du format de trace \_ = \[ %9 ! d ! \] %8 ! 04X !. %3 ! 04X !. %3 ! 04X !:: %4 ! s ! \[ %1 ! s ! \] (%! ... :% ! FUNC !: %2 ! s !)**. L’outil tracefmt ajoute des informations par défaut à chaque message de suivi. Vous pouvez configurer les informations incluses en définissant la \_ variable d’environnement de préfixe de format de trace \_ . Pour en savoir plus sur la syntaxe utilisée, consultez [préfixe du message de suivi](https://msdn.microsoft.com/library/aa139695.aspx).
5.  Tapez **tracefmt-TMF% systemroot% \\ system32 \\ WBEM \\ TMF \\ wmi. TMF-o OUTPUT.TXT% systemroot% \\ system32 \\ WBEM \\ journaliss \\ WMITracing. log**. Cela effectue la conversion du format binaire au format texte lisible.
6.  Tapez **Notepad% systemroot% \\ system32 \\ WBEM \\ TMF \\OUTPUT.TXT**. Le fichier de trace s’ouvre dans le bloc-notes.

Voici d’autres tâches liées au WPP que vous devrez peut-être effectuer.

**Pour arrêter le suivi WMI basé sur WPP**

-   Tapez **tracelog-arrêter la \_ \_ session de trace WMI**.

**Pour démarrer le suivi WMI basé sur WPP**

-   Tapez **tracelog-Start WMI \_ trace \_ session-GUID \# 1FF6B227-2CA7-40F9-9A66-980EADAA602E-RT-niveau 5-Flag 0x7-f MYTRACE. EMPLACEMENT**

**Windows Vista :** Par défaut, le suivi WMI basé sur WPP est défini sur le niveau 2, ce qui comprend uniquement les messages d’erreur. Pour inclure également des messages d’information, définissez le niveau sur 4. Toutes les zones de WMI sont suivies par défaut. Il existe trois zones distinctes qui peuvent être suivies : Core (indicateur = 0x1), ESS (indicateur = 0X2) et PROV (indicateur = 0x4). Dans la commande de démarrage ci-dessus, l' **indicateur 0x7** entraîne le suivi de ces trois zones.

**Windows 7 :** Par défaut, le suivi WMI basé sur WPP est désactivé et défini sur le niveau 0. Pour utiliser le suivi WMI basé sur WPP, cette fonctionnalité doit être activée et définie sur le niveau 2 pour les messages d’erreur ou sur le niveau 4 pour les messages d’erreur et d’information.

**Pour répertorier toutes les sessions de suivi WPP**

-   Tapez **tracelog-l**.

**Pour répertorier les informations relatives à la session de trace WMI WPP**

-   Tapez **tracelog-l \| findstr/i "WMI \_ trace"**.

**Pour afficher les paramètres de session de suivi WPP WMI**

-   Tapez **\_ \_ session de trace WMI tracelog-q**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Résolution des problèmes WMI](wmi-troubleshooting.md)
</dt> <dt>

[Fichiers journaux WMI](wmi-log-files.md)
</dt> </dl>

 

 
