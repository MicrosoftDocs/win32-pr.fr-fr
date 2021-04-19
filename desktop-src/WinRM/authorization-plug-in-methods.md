---
title: Méthodes de plug-in d’autorisation
description: Tous les points d’entrée de plug-in d’autorisation ont un mécanisme de rappel pour signaler la réussite ou l’échec de l’appel. Certains mécanismes de rappel sont appelés plusieurs fois jusqu’à ce que tous les résultats soient signalés.
ms.assetid: 6d7c1c54-fab5-431b-b123-eee6fd4dfb92
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9253267b87a30c5cc2781440b0ecd430f244e90
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510826"
---
# <a name="authorization-plug-in-methods"></a>Méthodes de plug-in d’autorisation

Tous les points d’entrée de plug-in d’autorisation ont un mécanisme de rappel pour signaler la réussite ou l’échec de l’appel. Certains mécanismes de rappel sont appelés plusieurs fois jusqu’à ce que tous les résultats soient signalés.

Le tableau suivant fournit une vue d’ensemble des méthodes de rappel d’autorisation.



| Méthode                                                                           | Description                                                          |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [**WSManPluginAuthzOperationComplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzoperationcomplete)   | Signale la réussite ou l’échec d’une opération utilisateur.                |
| [**WSManPluginAuthzQueryQuotaComplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzqueryquotacomplete) | Signale les détails de quota pertinents pour l’utilisateur spécifié.      |
| [**WSManPluginAuthzUserComplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzusercomplete)             | Signale une autorisation de connexion utilisateur ayant réussi ou échoué. |



 

 

 




