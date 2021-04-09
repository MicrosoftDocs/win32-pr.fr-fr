---
title: Utilisation de Windows Remote Management
description: Windows Remote Management est conçu pour améliorer la gestion du matériel dans un environnement réseau avec différents appareils exécutant différents systèmes d’exploitation.
ms.assetid: 6ee2b238-5bc2-4274-b7ca-49dbc728d8f1
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0c2934694de5913b467521510179fffdb220b601
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102000"
---
# <a name="using-windows-remote-management"></a>Utilisation de Windows Remote Management

Windows Remote Management est conçu pour améliorer la gestion du matériel dans un environnement réseau avec différents appareils exécutant différents systèmes d’exploitation. La conception du service repose sur la surveillance et la gestion des ordinateurs distants par implémentation d’un protocole standard interopérable.

Étant donné que l' [API de script WinRM](winrm-scripting-api.md) et l' [API C++ WinRM](winrm-c---api.md) implémentent et modélisent étroitement les opérations définies pour le protocole WS-Management, les scripts et les applications reçoivent des flux de données XML en réponse aux requêtes. Les paramètres d’entrée des appels de méthode doivent être construits en XML. Vous pouvez utiliser les méthodes de l’API [MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85)) pour afficher ou construire des chaînes XML. Pour obtenir un exemple, consultez [affichage de la sortie XML des scripts WinRM](displaying-xml-output-from-winrm-scripts.md).

La liste suivante contient des rubriques qui décrivent comment utiliser les scripts WinRM :

-   [Détection de la prise en charge du protocole WS-Management par un ordinateur distant](detecting-whether-a-remote-computer-supports-ws-management-protocol.md)
-   [Obtention de données à partir de l’ordinateur local](obtaining-data-from-the-local-computer.md)
-   [Obtention de données à partir d’un ordinateur distant](obtaining-data-from-a-remote-computer.md)
-   [Énumération ou liste de toutes les instances d’une ressource](enumerating-or-listing-all-instances-of-a-resource.md)
-   [Interrogation d’instances spécifiques d’une ressource](querying-for-specific-instances-of-a-resource.md)
-   [Affichage de la sortie XML des scripts WinRM](displaying-xml-output-from-winrm-scripts.md)

## <a name="tracing-winrm-activity"></a>Activité de suivi WinRM

Étant donné que WinRM obtient des données via [Windows Management Instrumentation (WMI)](/windows/desktop/WmiSdk/wmi-start-page), vous pouvez suivre l’activité WMI qui résulte des messages WinRM. À compter de Windows Vista, le service WMI n’utilise plus les [fichiers journaux WMI](/windows/desktop/WmiSdk/wmi-log-files). Au lieu de cela, il utilise le [suivi d’événements](/windows/desktop/ETW/event-tracing-portal) (ETW) et les événements sont disponibles par le biais de l’interface utilisateur **Observateur d’événements** ou de l’outil en ligne de commande Evtutil.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestion à distance de Windows](portal.md)
</dt> <dt>

[À propos de Windows Remote Management](about-windows-remote-management.md)
</dt> <dt>

[Référence Windows Remote Management](windows-remote-management-reference.md)
</dt> <dt>

[Scripts dans Windows Remote Management](scripting-in-windows-remote-management.md)
</dt> </dl>

 

 