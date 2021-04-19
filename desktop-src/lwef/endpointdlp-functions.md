---
title: Fonctions de protection contre la perte de données de point de terminaison
description: Fonctions utilisées par la fonctionnalité de protection contre la perte de données du point de terminaison.
ms.topic: article
ms.date: 03/18/2021
ms.openlocfilehash: f8713a6a6051bf477b4f9c7f6f8a7430abf70a52
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495444"
---
# <a name="endpoint-data-loss-prevention-functions"></a>Fonctions de protection contre la perte de données de point de terminaison

Fonctions utilisées par la fonctionnalité de protection contre la perte de données du point de terminaison.



| Fonctions                                                       | Description                                                           |
|-------------------------------------------------------------------|-----------------------------------------------------------------------|
| [DlpNotifyCloseDocument](endpointdlp-dlpnotifyclosedocument.md)                       | Fournit au système des informations sur un document avant le lancement de l’opération de fermeture du document.                                  |
| [DlpNotifyCloseDocumentFile](endpointdlp-dlpnotifyclosedocumentfile.md)                       | Fournit au système des informations sur un document avant le lancement de l’opération de fermeture du document.                                  |
| [DlpNotifyEnterDropTarget](endpointdlp-dlpnotifyenterdroptarget.md)                       | Fournit au système des informations sur un document quand une cible de déplacement est entrée.                                  |
| [DlpGetEnforcementApiVersion](endpointdlp-dlpgetenforcementapiversion.md)                       | Récupère la version de l’API de protection contre la perte de données (DLP) du point de terminaison sur l’appareil actuel.                                  |
| [DlpInitializeEnforcementMode](endpointdlp-dlpinitializeenforcementmode.md)                       | Indique au système les modes de mise en conformité souhaités pour un ensemble d’opérations de protection contre la perte de données (DLP) de point de terminaison.                                  |
| [DlpMustPasteFromSystemClipboard](endpointdlp-dlpmustpastefromsystemclipboard.md)                       | Détermine si l’application doit extraire les données du presse-papiers du système au lieu de les extraire de son cache interne.                                  |
| [DlpNotifyLeaveDropTarget](endpointdlp-dlpnotifyleavedroptarget.md)                       | Fournit au système des informations sur un document lors de la sortie d’une cible de déplacement.                                  |
| [DlpNotifyPostCopyToClipboard](endpointdlp-dlpnotifypostcopytoclipboard.md)                         | Fournit au système des informations sur un document après l’exécution d’une opération copier dans le presse-papiers.  |
| [DlpNotifyPostDragDrop](endpointdlp-dlpnotifypostdragdrop.md)                         | Fournit au système des informations sur un document après l’exécution d’une opération glisser-déplacer.  |
| [DlpNotifyPostOpenDocument](endpointdlp-dlpnotifypostopendocument.md)                       | Fournit au système des informations sur un document une fois l’opération d’ouverture terminée.                                  |
| [DlpNotifyPostOpenDocumentFile](endpointdlp-dlpnotifypostopendocumentfile.md)                       | Fournit au système des informations sur un document une fois l’opération d’ouverture terminée.                                  |
| [DlpNotifyPostPasteFromClipboard](endpointdlp-dlpnotifypostpastefromclipboard.md)                       | Fournit au système des informations sur un document après la fin de l’opération coller à partir du presse-papiers.                                  |
| [DlpNotifyPostPrint](endpointdlp-dlpnotifypostprint.md)                       | Fournit au système des informations sur un document une fois l’opération d’impression terminée.                                  |
| [DlpNotifyPostSaveAsDocument](endpointdlp-dlpnotifypostsaveasdocument.md)                       | Fournit au système des informations sur un document après la fin de l’opération Enregistrer sous.                                  |
| [DlpNotifyPostStartPrint](endpointdlp-dlpnotifypoststartprint.md)                       | Fournit au système des informations sur un document après le démarrage d’une opération d’impression.                                  |
| [DlpNotifyPostStashClipboard](endpointdlp-dlpnotifypoststashclipboard.md)                       | Fournit au système des informations d’État après la fin d’une opération de presse-papiers.                                  |
| [DlpNotifyPreCopyToClipboard](endpointdlp-dlpnotifyprecopytoclipboard.md)                         | Fournit au système des informations sur un document avant le lancement d’une opération copier dans le presse-papiers.  |
| [DlpNotifyPreDragDrop](endpointdlp-dlpnotifypredragdrop.md)                         | Fournit au système des informations sur un document avant le lancement d’une opération glisser-déplacer.  |
| [DlpNotifyPreOpenDocument](endpointdlp-dlpnotifypreopendocument.md)                         | Fournit au système des informations sur un document avant le lancement de l’opération d’ouverture.  |
| [DlpNotifyPreOpenDocumentFile](endpointdlp-dlpnotifypreopendocumentfile.md)                         | Fournit au système des informations sur un document avant le lancement de l’opération d’ouverture.  |
| [DlpNotifyPrePasteFromClipboard](endpointdlp-dlpnotifyprepastefromclipboard.md)                         | Fournit au système des informations sur un document avant le lancement d’une opération coller à partir du presse-papiers.  |
| [DlpNotifyPrePrint](endpointdlp-dlpnotifypreprint.md)                         | Fournit au système des informations sur un document avant le lancement d’une opération d’impression.  |
| [DlpNotifyPreSaveDocument](endpointdlp-dlpnotifypresaveasdocument.md)                       | Fournit au système des informations sur un document avant le lancement d’une opération Enregistrer sous.                                  |
| [DlpNotifyPreStashClipboard](endpointdlp-dlpnotifyprestashclipboard.md)                       | Notifie le système avant l’initialisation d’une opération de presse-papiers.                                  |