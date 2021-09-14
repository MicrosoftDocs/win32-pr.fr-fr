---
description: WMI utilise le suivi d’événements (ETW) et les événements peuvent être obtenus par le biais de l’interface utilisateur observateur d’événements ou de l’outil en ligne de commande Wevtutil. Pour plus d’informations, consultez suivi de l’activité WMI.
ms.assetid: 315b8355-03b9-40f9-a6c1-29a49f5a2cd8
ms.tgt_platform: multiple
title: Fichiers journaux WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a51dfe4efbec32e60812980511676f723fd5aee9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292415"
---
# <a name="wmi-log-files"></a>Fichiers journaux WMI

WMI utilise le [suivi d’événements](/windows/desktop/ETW/event-tracing-portal) (ETW) et les événements peuvent être obtenus par le biais de l’interface utilisateur **Observateur d’événements** ou de l’outil en ligne de commande Wevtutil. Pour plus d’informations, consultez suivi de l' [activité WMI](tracing-wmi-activity.md).

-   [Suivi des événements au lieu des journaux texte](#event-tracing-instead-of-text-logs)
-   [Fichiers journaux WMI](#wmi-log-files)
-   [Rubriques connexes](#related-topics)

## <a name="event-tracing-instead-of-text-logs"></a>Suivi des événements au lieu des journaux texte

L’activité du service WMI est enregistrée dans le fichier WMITracing. log. Pour plus d’informations sur l’activation du suivi d’événements WMI et l’accès au fichier WMITracing. log, consultez suivi de l' [activité WMI](tracing-wmi-activity.md). Windows Les fournisseurs de modèle de pilote (WDM) continuent à se connecter au fichier wbemprov. log.

## <a name="wmi-log-files"></a>Fichiers journaux WMI

Le service WMI et certains fournisseurs écrivent des fichiers journaux de texte pour enregistrer les événements.

<dl> <dt>

<span id="WMI_Provider_Log_Files"></span><span id="wmi_provider_log_files"></span><span id="WMI_PROVIDER_LOG_FILES"></span>[Fichiers journaux du fournisseur WMI](wmi-provider-log-files.md)
</dt> <dd>

Les fournisseurs WMI peuvent également conserver les journaux. Les fichiers journaux qui apparaissent sur un système dépendent des fournisseurs installés.

</dd> </dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence WMI](wmi-reference.md)
</dt> <dt>

[Suivi de l’activité WMI](tracing-wmi-activity.md)
</dt> <dt>

[Journalisation de l’activité WMI](logging-wmi-activity.md)
</dt> </dl>

 

 
