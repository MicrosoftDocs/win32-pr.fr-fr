---
title: Utilisation de netsh pour gérer les traces
description: Dans Windows 7, netsh.exe peut être utilisé à partir d’une invite de commandes pour activer et configurer des suivis réseau. Cette section décrit quelques-unes des commandes netsh.exe qui peuvent vous aider à résoudre les problèmes de suivi, y compris la nouvelle fonctionnalité de suivi de netsh.
ms.assetid: f0f0fc7b-7cfa-43c7-89a3-3b80050875f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c1cf869f60b69e227e78e19e8e05d3765ddb67d
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119024"
---
# <a name="using-netsh-to-manage-traces"></a>Utilisation de netsh pour gérer les traces

Dans Windows 7, netsh.exe peut être utilisé à partir d’une invite de commandes pour activer et configurer des suivis réseau. Cette section décrit quelques-unes des commandes netsh.exe qui peuvent vous aider à résoudre les problèmes de suivi, y compris la nouvelle fonctionnalité de **suivi de netsh** . Notez que les commandes netsh doivent être exécutées à partir d’une invite de commandes avec élévation de privilèges.

## <a name="collecting-traces"></a>Collecte des traces

Les scénarios sont des ensembles prédéfinis de fournisseurs de suivi qui peuvent être activés pour la résolution des problèmes. Pour afficher la liste des scénarios liés au réseau disponibles, tapez **netsh trace Show Scenarios** (**netsh trace Show Providers** répertorie chacun des fournisseurs disponibles, y compris ceux qui ne sont pas pertinents pour la mise en réseau).

Une fois que vous avez identifié un scénario adapté à vos problèmes, vous pouvez voir une liste de tous les fournisseurs inclus dans ce scénario. Par exemple, pour afficher tous les fournisseurs activés dans le cadre du scénario InternetClient, tapez **netsh trace Show scénario internetclient**.

Vous pouvez démarrer une trace pour tous les fournisseurs dans un scénario ou un ensemble de scénarios donné. Par exemple, pour démarrer une trace pour tous les fournisseurs activés dans le cadre du scénario InternetClient, tapez **netsh trace Start Scenario = internetclient**. Pour capturer des fournisseurs pour plusieurs scénarios, vous pouvez spécifier tous les scénarios appropriés, tels que **netsh trace Start scénario = filesharing Scenario = DirectAccess**. Notez qu’une seule session de suivi peut être activée à la fois ; Il n’est pas possible de capturer simultanément des informations de trace à partir de différents ensembles de fournisseurs dans des fichiers distincts.

Vous pouvez également démarrer une trace pour des fournisseurs supplémentaires non inclus dans ce scénario particulier. Par exemple, vous souhaiterez peut-être démarrer les traces pour tous les fournisseurs activés dans le cadre du scénario de réseau local sans fil et également le fournisseur DHCP. Pour ce faire, tapez **netsh trace Start scénario = WLAN Provider = Microsoft-Windows-DHCP-client**.

Vous pouvez également afficher plus de détails sur un fournisseur spécifique en tapant **netsh trace Show Provider** suivi du nom du fournisseur.

Pour afficher toutes les options et tous les filtres disponibles, vous pouvez taper **netsh trace Start/ ?**.

Pour arrêter le suivi, tapez **netsh trace stop**.

## <a name="using-the-output-files"></a>Utilisation des fichiers de sortie

Lorsque le suivi est arrêté, deux fichiers sont générés par défaut : un fichier journal de suivi d’événements (ETL) et un fichier .cab.

Les événements de trace sont collectés dans le fichier ETL, qui peut être affiché à l’aide d’outils tels que Moniteur réseau. Le fichier ETL est nommé NetTrace. etl par défaut, ou vous pouvez spécifier un autre nom en incluant **tracefile = nom_fichier. etl** lors du démarrage de la trace.

Le fichier .cab contient des informations détaillées sur les logiciels et le matériel du système, tels que les informations de l’adaptateur, la génération, le système d’exploitation et les paramètres sans fil. Le fichier .cab est nommé nettrace.cab par défaut, sauf si un autre nom a été spécifié comme indiqué ci-dessus.

Ce fichier de .cab contient deux fichiers, qui portent toujours le même nom. Report. etl est une autre copie des mêmes informations que celles incluses dans NetTrace. etl. Le fichier report.html contient des informations supplémentaires sur les événements de trace et les autres informations collectées. Pour recevoir le plus de détails disponibles, incluez la commande **Report = Oui** lors du démarrage d’une trace.

## <a name="using-filters-to-reduce-the-amount-of-data-in-the-etl-trace-file"></a>Utilisation de filtres pour réduire la quantité de données dans le fichier de trace ETL

Lorsque les captures se produisent sur une longue période de temps, le fichier de trace ETL peut devenir très volumineux. Dans les scénarios où plusieurs fournisseurs sont activés, ce qui entraîne un trafic élevé, les contraintes de mémoire tampon ETW peuvent entraîner la suppression de certaines traces. Hormis cette considération, la réduction de la quantité de données dans le fichier de trace ETL peut faciliter la résolution des problèmes en réduisant la quantité de données à examiner.

Les filtres de trace netsh peuvent être utilisés pour réduire la taille du fichier de trace ETL. Ces filtres de trace sont des niveaux et des mots clés ETW qui peuvent être appliqués à des fournisseurs individuels.

Pour afficher la liste des filtres qui peuvent être appliqués, tapez **netsh trace Start/ ?**

Voici un exemple de filtre : **netsh trace Start internetclient fournisseur = Microsoft-Windows-tcpip Level = 5 Keywords = UT : ReceivePath, UT : SendPath**.

Dans cet exemple, le niveau est défini sur 5, ce qui signifie que le nombre maximal d’événements est affiché. Le tableau suivant présente les paramètres disponibles :



| Level      | Paramètre              | Description                                                                           |
|-------|---------------|----------------------------------------------------------------------------|
| 1     | Critique      | Seuls les événements critiques seront affichés.                                        |
| 2     | Erreurs        | Les événements critiques et les erreurs s’affichent.                                  |
| 3     | Avertissements      | Les événements critiques, les erreurs et les avertissements s’affichent.                       |
| 4     | Informationnel | Les événements critiques, les erreurs, les avertissements et les événements d’information s’affichent. |
| 5     | Commentaires       | Tous les événements s’affichent.                                                  |



 

Les mots clés **UT : ReceivePath** et **UT : SentPath** filtrent les événements pour afficher uniquement les événements suivis dans le chemin d’envoi ou de réception. Vous trouverez une liste complète des mots clés pour un fournisseur spécifique en tapant **netsh trace Show Provider** suivi du nom du fournisseur. Par exemple, si vous tapez **netsh trace Show Provider Microsoft-Windows-tcpip** , vous affichez des informations sur le fournisseur Microsoft-Windows-tcpip, y compris une liste de mots clés.

Netsh prend également en charge la fonctionnalité de filtrage de paquets (semblable à Moniteur réseau) lorsque la capture de paquets est activée (en définissant **capture = Oui**). Le filtrage de paquets peut être utilisé pour capturer un nombre limité de paquets dans un fichier de trace. Par exemple, **netsh trace Start capture = Oui IPv4. Address = = x.x.x.** x, où x.x. x est l’adresse IP, ne capture que les paquets avec le trafic IPv4 avec cette adresse source ou de destination spécifique...

Pour plus d’informations sur l’utilisation du filtrage de paquets, vous pouvez taper **netsh trace Show capturefilterHelp**.

 

 




