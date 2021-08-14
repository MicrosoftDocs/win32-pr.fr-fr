---
title: Méthodes de plug-in Operations
description: Méthodes de plug-in Operations
ms.assetid: 81fe751f-51fd-4da6-b44a-0af9007eea9a
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8bcfc2263a9ecd35c050499f0547b5bc5190e5896b430edabe6be8490239b62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118323891"
---
# <a name="operations-plug-in-methods"></a>Méthodes de plug-in Operations

Tous les points d’entrée de plug-in d’opérations ont un mécanisme de rappel pour signaler la réussite ou l’échec de l’appel. Certains mécanismes de rappel sont appelés plusieurs fois, jusqu’à ce que tous les résultats soient signalés.

Le tableau suivant fournit une vue d’ensemble des méthodes de rappel d’opérations.



| Méthode                                                                         | Description                                                                                                                                          |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WSManPluginFreeRequestDetails**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginfreerequestdetails)         | Libère la mémoire allouée pour la structure de [**\_ \_ demande de plug-in WSMan**](/windows/desktop/api/Wsman/ns-wsman-wsman_plugin_request) .                                          |
| [**WSManPluginGetOperationParameters**](/windows/desktop/api/Wsman/nf-wsman-wsmanplugingetoperationparameters) | Obtient des informations opérationnelles, telles que les délais d’attente et les restrictions de données associées à une opération.                                         |
| [**WSManPluginOperationComplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginoperationcomplete)           | Enregistre l’achèvement d’une opération.                                                                                                              |
| [**WSManPluginReceiveResult**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginreceiveresult)                   | signale les résultats aux plug-ins de Windows Remote Management (WinRM).                                                                                       |
| [**WSManPluginReportContext**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginreportcontext)                   | Signale l’interpréteur de commandes et le contexte de commande à l’infrastructure WinRM afin que d’autres opérations puissent être effectuées sur l’interpréteur de commandes et/ou la commande. |



 

 

 




