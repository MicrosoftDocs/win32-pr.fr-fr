---
title: Méthodes de plug-in Operations
description: Méthodes de plug-in Operations
ms.assetid: 81fe751f-51fd-4da6-b44a-0af9007eea9a
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff64a53c4c63b9e552efe90ac057b8a31d603b64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939540"
---
# <a name="operations-plug-in-methods"></a>Méthodes de plug-in Operations

Tous les points d’entrée de plug-in d’opérations ont un mécanisme de rappel pour signaler la réussite ou l’échec de l’appel. Certains mécanismes de rappel sont appelés plusieurs fois, jusqu’à ce que tous les résultats soient signalés.

Le tableau suivant fournit une vue d’ensemble des méthodes de rappel d’opérations.



| Méthode                                                                         | Description                                                                                                                                          |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WSManPluginFreeRequestDetails**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginfreerequestdetails)         | Libère la mémoire allouée pour la structure de [**\_ \_ demande de plug-in WSMan**](/windows/desktop/api/Wsman/ns-wsman-wsman_plugin_request) .                                          |
| [**WSManPluginGetOperationParameters**](/windows/desktop/api/Wsman/nf-wsman-wsmanplugingetoperationparameters) | Obtient des informations opérationnelles, telles que les délais d’attente et les restrictions de données associées à une opération.                                         |
| [**WSManPluginOperationComplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginoperationcomplete)           | Enregistre l’achèvement d’une opération.                                                                                                              |
| [**WSManPluginReceiveResult**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginreceiveresult)                   | Signale les résultats aux plug-ins de Windows Remote Management (WinRM).                                                                                       |
| [**WSManPluginReportContext**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginreportcontext)                   | Signale l’interpréteur de commandes et le contexte de commande à l’infrastructure WinRM afin que d’autres opérations puissent être effectuées sur l’interpréteur de commandes et/ou la commande. |



 

 

 




